# Null document.location (null-document-location)

The value of `document.location` in Lightning Locker is `null`. To prevent
code from breaking use the `@locker/rollup-plugin`.

## Rule Details

Example of **incorrect** code:

<!-- eslint-disable no-undef, no-unused-expressions -->
```js
document.location;
document.location.href;
document.location = value;
```
