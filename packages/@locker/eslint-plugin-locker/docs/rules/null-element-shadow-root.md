# Null element.shadowRoot (null-element-shadow-root)

For security the value of [`element.shadowRoot`](https://developer.mozilla.org/en-US/docs/Web/API/ShadowRoot)
in Lightning Locker is `null`.

## Rule Details

Example of **incorrect** code:

<!-- eslint-disable-next-line no-undef, no-unused-expressions -->
```js
element.shadowRoot.activeElement;
```

Example of **correct** code:

<!-- eslint-disable-next-line no-undef -->
```js
if (element.shadowRoot === null) {
    // ...
}
```
