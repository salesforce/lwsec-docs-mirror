# Distorted Element#setAttribute APIs (distorted-element-set-attribute)

For security the `Element#setAttribute` and `Element#setAttributeNS` are distorted
in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Element/docs/setAttribute-family-apis.md -->
## Element.prototype.setAttribute*

Distortions for these methods use internal registries to invoke other distortions for specific property names.

 - [`setAttribute()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/setAttribute) sets the value of an attribute on the specified element. If the attribute already exists, the value is updated; otherwise a new attribute is added with the specified name and value.
 - [`setAttributeNS()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/setAttributeNS) adds a new attribute or changes the value of an attribute with the given namespace and name.
 - [`setAttributeNode()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/setAttributeNode) adds a new `Attr` node to the specified element.
 - [`setAttributeNodeNS()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/setAttributeNodeNS) adds a new namespaced attribute node to an element.
 

The `setAttribute*` distortions themselves defend against shape-shifting objects. Shape-shifting objects don't affect native DOM APIs because values are automatically coerced. However, shape-shifting attacks can attempt to bypass Lightning Web Security distortions.

This example explains a shape-shifting attack.

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

Because Lightning Web Security distorts `setAttribute` and the value is read at least twice (once by LWS and once by the native API), LWS can mistakenly determine that the value is `'foo'` and it's safe to pass through. However, at the second read of `attrValue` its value is `'import'`. 



 Pseudo code explanation:
```text
code in sandbox calls setAttribute with shape-shifting object
    Lightning Web Security reads first returned value and caches it in a local variable
        value 'foo' is cached and further checks rely on it
    Lightning Web Security uses cached value to determine if this is forbidden
        'foo' is allowed, execution is handled to native API using .call(obj, arguments)
    nativeApi coerces the argument to a string and sets it on the element
        shape-shifting occurs and the second read now returns 'import'

```

The `setAttribute` distortion sanitizes the passed value to prevent shape-shifting attacks. 

The `setAttributeNode` distortion checks that the passed attribute argument is indeed an instance of `Attr`. No actual validation happens and the getter utilities automatically detect if this is not an instance of `Attr`. The value property of the attribute is coerced to a string.

### Distorted Behavior

- Arguments are sanitized to prevent shape-shifting attacks.
- The behavior varies according to the invoked registered distortion.
- When no distortions are registered, behavior seems like native behavior.
<!-- END generated embed, please keep comment -->
