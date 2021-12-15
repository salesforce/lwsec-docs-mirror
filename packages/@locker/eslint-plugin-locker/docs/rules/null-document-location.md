# Null document.location (null-document-location)

The value of `document.location` in Lightning Locker is `null`. To prevent
code from breaking use the `@locker/rollup-plugin` when support is added.

## Rule Details

Example of **incorrect** code:

<!-- eslint-disable-next-line no-unused-expressions -->
```js
document.location.href;
```

Example of **correct** code:

```js
if (document.location === null) {
    // ...
}
```
