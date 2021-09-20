# Distorted Element#setAttribute APIs (distorted-element-set-attribute)

For security the `Element#setAttribute` and `Element#setAttributeNS` are distorted
in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Element/docs/setAttribute-family-apis.md -->
## value: Element.prototype.setAttribute

The `setAttribute*` distortions use internal registries to access already defined
distortions for property names. The only distorted behavior implemented here is a
defensive mechanism against shapeshifting objects. Shapeshifting objects do not
affect native DOM apis because values are automatically coerced, however,
shapeshifting attacks target Locker code in an attempt to bypass distortions.
The following example will attempt to explain this type of attack.

```js
const attrValue = {
    toString() {
        if (this.x) {
            return 'import';
        }

        this.x = true;
        return 'foo';
    },
};

const element = document.createElement('link');
element.setAttribute('rel', attrValue);
```

Because we have distorted setAttribute and the value is read at least twice
(1 time by locker 1 time by the native api), part of our code can be tricked to
think that the value is `'foo'` and it's safe to pass through. At the 2nd read
of attrValue its value will be `'import'`. Pseudo code explanation below:
```text
code in sandbox calls setAttribute with shapeshifting object
    locker reads first returned value and caches it in a local variable
        value 'foo' is cached and further checks rely on it
    locker uses cached value to determine if this is forbidden
        'foo' is allowed, execution is handled to native API using .call(obj, arguments)
    nativeApi coerces the argument to a string and sets it on the element
        shapeshifting occurs and the 2nd read returns now 'import'

```

In the case of setAttributeNode we perform the following operations:

- validate the passed attribute argument is indeed an instance of Attr
	- no actual validation happens the getter utilities will automatically detect
    this is not an instance of Attr


- the value property of the attribute is coerced to a string

### Goal

- To prevent shapeshifting arguments from being passed to lower level distortions
associated with setAttribute* APIs
- To allow execution of sub-distortions interested in handling specific attributes
and/or values

### Design

- expose 4 register methods, one for each type of distortions
(setAttribute, setAttributeNS, setAttributeNode, setAttributeNodeNS). The 4
registries optimize for performance and O(1) lookups because this family of APIs
are highly used.
- any call to `setAttribute*` methods will first sanitize the arguments to prevent
shapeshifting attacks followed by a lookup for a registered distortion
- if a distortion is found, invoke it and transfer control otherwise invoke the
native method with sanitized arguments

### Distorted behavior

- sanitization of arguments to prevent shapeshifting attacks
- Native like behavior unless a registered distortion needs to be executed at
which point the behavior is dependent on the execution of that distortion.
<!-- END generated embed please keep comment here to allow auto update -->
