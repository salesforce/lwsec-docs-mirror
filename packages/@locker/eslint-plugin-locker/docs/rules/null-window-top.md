# Null window.top (null-window-top)

The value of `window.top` in Lightning Locker is `null`. To prevent code from
breaking assume code is executing in the topmost window.

The following `window.top` references are prohibited or fixable to `window`:

-   `top`
-   `document.defaultView.top`
-   `frames.top`
-   `globalThis.top`
-   `self.top`
-   `window.top`

:bulb: The [`@locker/rollup-plugin`] may also be used to transform `window.top`
references to `window`.

## Rule Details

Example of **incorrect** code:

```js
window.top.pageXOffset;
```

Example of **correct** code:

```js
if (window.top === null) {
    // ...
}
```

[`@locker/rollup-plugin`]: https://www.npmjs.com/package/@locker/rollup-plugin
