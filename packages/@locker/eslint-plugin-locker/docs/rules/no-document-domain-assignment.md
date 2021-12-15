# Disallow document.domain Assignment (no-document-domain-assignment)

For security Lightning Locker prohibits assignment to [`document.domain`][1].

## Rule Details

Example of **incorrect** code:

```js
document.domain = value;
```

[1]: https://developer.mozilla.org/en-US/docs/Web/API/Document/domain
