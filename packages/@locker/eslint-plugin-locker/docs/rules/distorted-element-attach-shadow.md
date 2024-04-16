# Distorted Element#attachShadow (distorted-element-attach-shadow)

For security `Element#attachShadow` is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/Element/docs/attachShadow-value.md -->
## Element.prototype.attachShadow

The [`Element.prototype.attachShadow()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/attachShadow) method attaches a shadow DOM tree to the specified element and returns a reference to its `ShadowRoot`.

When the `attachShadow()` method provides an options object with `mode` set to `open`, the shadow DOM is exposed to the scripting environment. Other namespaces then have access to the shadow DOM.

### Distorted Behavior

This distortion restricts access to the element's `shadowRoot` property. Only code that's running in the same sandbox can access the property.
<!-- END generated embed, please keep comment -->
