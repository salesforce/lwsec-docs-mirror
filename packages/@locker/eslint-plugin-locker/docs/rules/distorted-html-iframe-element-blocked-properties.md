# Distorted HTMLIFrameElement Blocked Properties (distorted-html-iframe-element-blocked-properties)

For security the following `HTMLIFrameElement` properties are prohibited in Lightning Locker:
-   allowPaymentRequest
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
