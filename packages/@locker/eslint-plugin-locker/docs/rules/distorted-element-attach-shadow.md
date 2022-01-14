# Distorted Element#attachShadow (distorted-element-attach-shadow)

For security `Element#attachShadow` is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Element/docs/attachShadow-value.md -->
## Element.prototype.attachShadow setter

The [`Element.prototype.attachShadow()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/attachShadow) method attaches a shadow DOM tree to the specified element and returns a reference to its `ShadowRoot`.

When the `attachShadow()` method provides an options object with `mode` set to `open`, the shadow DOM is exposed to the scripting environment. Other namespaces then have access to the shadow DOM.

### Distorted Behavior

This distortion throws an exception when the `mode` value is not `closed`, which prevents exposing the shadow DOM and also guards against additional modes potentially added later.
<!-- END generated embed, please keep comment -->
