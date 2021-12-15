# Null shadowRoot.host (null-shadow-root-host)

For security the value of [`shadowRoot.host`](https://developer.mozilla.org/en-US/docs/Web/API/ShadowRoot/host)
in Lightning Locker is `null`.

## Rule Details

Example of **incorrect** code:

<!-- eslint-disable no-undef, no-unused-expressions -->
```js
shadowRoot.host;
shadowRoot.host.nodeName;
```
