# Null element.shadowRoot (null-element-shadow-root)

For security the value of [`element.shadowRoot`][1] in Lightning Locker is `null`.

## Rule Details

Example of **incorrect** code:

<!-- eslint-disable no-undef, no-unused-expressions -->
```js
element.shadowRoot;
element.shadowRoot.activeElement;
```

[1]: https://developer.mozilla.org/en-US/docs/Web/API/ShadowRoot
