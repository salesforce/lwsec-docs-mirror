# Prevent access to certain HTMLElement properties (distorted-html-element-blocked-properties)

The following `HTMLElement` properties are prohibited when Lightning Web Security is enabled:
-   nonce
-   onrejectionhandled
-   onunhandledrejection

## Rule Details

Example of **incorrect** code:

```js
script.nonce;
```
