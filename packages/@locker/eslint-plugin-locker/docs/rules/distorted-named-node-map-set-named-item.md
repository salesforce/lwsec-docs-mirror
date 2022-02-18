# Distorted NamedNodeMap#setNamedItem (distorted-named-node-map-set-named-item)

For security `NamedNodeMap#setNamedItem` is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/NamedNodeMap/docs/setNamedItem-value.md -->
## NamedNodeMap.prototype.setNamedItem

The [`NamedNodeMap`](https://developer.mozilla.org/en-US/docs/Web/API/NamedNodeMap) interface represents a collection of `Attr` objects. Objects inside a `NamedNodeMap` are not in any particular order, unlike `NodeList`, although they may be accessed by an index as in an array. A `NamedNodeMap` object is live and will thus be auto-updated if changes are made to its contents internally or elsewhere.

`NamedNodeMap.prototype.setNamedItem()` is a method that replaces or adds the `Attr` identified in the map by the given name. You can use it to set an attribute on an element, so Lightning Web Security must distort `NamedNodeMap.prototype.setNamedItem`.

This code would bypass LWS distortions for named properties and `setAttribute\*` and set the `rel` attribute on a link if `setNamedItem` is not distorted.
```js
const el = document.createElement('link');
const attr = document.createAttribute('rel');
attr.value = 'import';
el.attributes.setNamedItem(attr);
```

The `NamedNodeMap.prototype.setNamedItem` distortion works with the distortion for `Element.attributes getter` to pair elements with `NamedModeMap` instances when the getter is invoked for an attribute. Then the `NamedNodeMap.prototype.setNamedItem` distortion invokes other distortions for specific attributes.

### Distorted Behavior

If there is a distortion registered for an attribute, the behavior depends on the specific distortion. If there's no distortion registered for an attribute, the native invocation of `setNamedItem` is allowed.
<!-- END generated embed, please keep comment -->
