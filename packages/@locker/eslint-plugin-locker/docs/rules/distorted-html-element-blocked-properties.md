# Disallow Blocked HTMLElement Properties (blocked-html-element-properties)

For security the following `HTMLElement` properties are prohibited in Lightning Locker:
-   nonce
-   onrejectionhandled
-   onunhandledrejection

## Rule Details

Example of **incorrect** code:

```js
script.nonce;
```
