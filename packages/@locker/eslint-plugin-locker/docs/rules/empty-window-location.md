# Empty window.location (empty-window-location)

The value of `window.location` in Lightning Locker is an empty location object.
To prevent code from breaking use the `@locker/rollup-plugin` when support is added.

## Rule Details

Example of **incorrect** code:

<!-- eslint-disable-next-line no-unused-expressions -->
```js
window.location.href;
```
