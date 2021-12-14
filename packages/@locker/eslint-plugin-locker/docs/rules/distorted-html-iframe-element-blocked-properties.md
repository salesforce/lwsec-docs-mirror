# Prevent access to certain HTMLIFrameElement properties (distorted-html-iframe-element-blocked-properties)

For security the following `HTMLIFrameElement` properties are prohibited when Lightning Web Security is enabled:
-   allowPaymentRequest
-   csp
-   featurePolicy
-   referrerPolicy
-   sandbox
-   srcdoc

## Rule Details

Example of **incorrect** code:

```js
document.getElementsByTagName('iframe')[0].allowPaymentRequest;
```
