# Empty window.location (empty-window-location)

The value of `window.location` in Lightning Locker is an empty location object.
To prevent code from breaking use the [`@locker/rollup-plugin`].

## Rule Details

Example of **incorrect** code:

```js
window.location.href;
window.location = value;
```

[`@locker/rollup-plugin`]: https://www.npmjs.com/package/@locker/rollup-plugin
