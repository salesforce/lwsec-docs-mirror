# Distorted NamedNodeMap#setNamedItem (distorted-named-node-map-set-named-item)

For security `NamedNodeMap#setNamedItem` is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/NamedNodeMap/docs/setNamedItem-value.md -->
## value: NamedNodeMap.prototype.setNamedItem

It is possible to set an attribute on an element using the methods available on NamedNodeMap. For example:

```js
const el = document.createElement('link');
const attr = document.createAttribute('rel');
attr.value = 'import';
el.attributes.setNamedItem(attr);
```

This would bypass our distortions for named properties and setAttribute\*. For this reason we need to distort `NamedNodeMap.prototype.setNamedItem`.

### Goal

- invoke registered DOM property distortions in situations like `el.attributes.setNamedItem(...)`

### Design
Inside of a NamedNodeMap distortion `this` does not point to an element but to the `attributes` instance. We have no way of understanding which `attributes` instance is for what element. That is why the shared lib of this module provides a `pairElement` utility used in Element.prototype.attributes distortion to pair an element with a NamedNodeMap instance upon accessing the getter of Element.prototype.attributes. Since all operations are synchronous we are guaranteed that the registration happens first followed by invocation later.
Example:

el.attributes.setNamedItem(....)
  |           |
registration  invocation

The registry is a WeakMap since elements can be removed from the page throughout the lifecycle of an application. The distortions are being retrieved from the `setAttributeNode` registry since both methods accept an instance of `Attr`.

### Distorted behavior

- if no distortion is found for an Attr instance then proceed with native invocation of setNamedItem
- if a distortion exists then the distorted behavior is relative to what that distortion does
<!-- END generated embed please keep comment here to allow auto update -->
