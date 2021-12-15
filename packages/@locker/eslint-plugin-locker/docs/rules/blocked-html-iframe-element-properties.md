# Disallow Blocked HTMLIFrameElement Properties (blocked-html-iframe-element-properties)

For security the following `HTMLIFrameElement` properties are prohibited in Lightning Locker:
-   allowPaymentRequest
-   contentDocument
-   csp
-   featurePolicy
-   referrerPolicy
-   sandbox
-   srcdoc

## Rule Details

Example of **incorrect** code:

```js
iframe.allowPaymentRequest;
```
