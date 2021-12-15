# Disallow document.domain Assignment (no-document-domain-assignment)

For security Lightning Locker prohibits assignment to
[`document.domain`](https://developer.mozilla.org/en-US/docs/Web/API/Document/domain).

## Rule Details

Example of **incorrect** code:

<!-- eslint-disable-next-line no-undef -->
```js
document.domain = value;
```
