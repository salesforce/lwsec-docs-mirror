# Distorted Element#attributes Getter (distorted-element-attributes-getter)

For security the `Element#attributes` getter is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Element/docs/attributes-getter.md -->
## get: Element.attributes

The attributes collection is of type NamedNodeMap and can be used to set and remove attributes on an element. The distortion on this getter does not alter its functionality but only pairs an element with an NamedNodeMap instance such that the distortions on NamedNodeMap.prototype can retrieve the element.

### Goal

-   pair an Element instance with a NamedNodeMap for distortions on NamedNodeMap.prototype

### Design

-   use provided util `pairElement` to pair current element with NamedNodeMap instance when get accessor is invoked.
-   this pairing is only for bookkeeping and O(1) lookups based on the identity of attributes collection

### Distorted behavior

-   no distorted behavior
<!-- END generated embed please keep comment here to allow auto update -->
