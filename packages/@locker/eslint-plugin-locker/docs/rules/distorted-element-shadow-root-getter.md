# Disallow usage of Element.shadowRoot getter (distorted-element-shadow-root-getter)

The `Element.shadowRoot` getter returns `null` when Lightning Web Security is enabled.

See [Related Distortions](#related-distortions) below for more details.

## Rule Details

Example of **incorrect** code:

```js
element.shadowRoot.querySelector('div');
```

## Related Distortions

<!-- START generated embed: @locker/distortion/src/Element/docs/shadowRoot-getter.md -->
## Element.prototype.shadowRoot getter

The [`Element.prototype.shadowRoot`](https://developer.mozilla.org/en-US/docs/Web/API/Element/shadowRoot) read-only property represents the shadow root hosted by the element.

This property allows retrieving the shadow DOM of custom elements created with `attachShadow({mode: 'open'})`.

In a sandbox, the distortion for `attachShadow()` prevents code from creating elements with `mode: 'open'`, but doesn't prevent code that's running outside a sandbox from creating custom elements in `open` mode. Elements that are passed as function arguments or queried from the Light DOM or shadow DOM are at risk.
### Distorted Behavior

This distortion returns `null` when you try to access the `shadowRoot` property on a Light DOM element.
<!-- END generated embed, please keep comment -->
