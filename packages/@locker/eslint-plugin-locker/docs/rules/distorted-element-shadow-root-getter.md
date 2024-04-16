# Access to element.shadowRoot (distorted-element-shadow-root-getter)

Lightning Web Security limits `element.shadowRoot` access to the sandbox that the element was created in.

<!-- START generated embed: @locker/distortion/src/Element/docs/shadowRoot-getter.md -->
## Element.prototype.shadowRoot getter

The [`Element.prototype.shadowRoot`](https://developer.mozilla.org/en-US/docs/Web/API/Element/shadowRoot) read-only property represents the shadow root hosted by the element.

This property allows retrieving the shadow DOM of custom elements created with `attachShadow({mode: 'open'})`.


### Distorted Behavior

This distortion returns `null` when you try to access an element's `shadowRoot` property from outside of the sandbox that it was created in. Elements or `shadowRoot` objects that are passed as function arguments are not protected.
<!-- END generated embed, please keep comment -->
