# Distorted Element#attributes Getter (distorted-element-attributes-getter)

For security the `Element#attributes` getter is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Element/docs/attributes-getter.md -->
## Element.prototype.attributes getter

The [`Element.prototype.attributes`](https://developer.mozilla.org/en-US/docs/Web/API/Element/attributes) property returns a live collection of all attribute nodes registered to the specified node. It is a `NamedNodeMap`, not an `Array`, so it has no `Array` methods and the `Attr` nodes' indexes may differ among browsers. 

The `attributes` collection can be used to set and remove attributes on an element. 

The distortion on this getter doesn't alter its functionality. It pairs an `Element` instance with a `NamedNodeMap` instance so that the  distortion on `NamedNodeMap.prototype.setNamedItem` can retrieve the element.

### Distorted Behavior

No distorted behavior.
<!-- END generated embed, please keep comment -->
