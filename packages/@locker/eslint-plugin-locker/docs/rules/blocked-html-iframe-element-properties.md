# Disallow Blocked HTMLIframeElement Properties (blocked-html-iframe-element-properties)

For security the following HTMLIframeElement properties are prohibited in Lightning Locker:
  * allowPaymentRequest
  * contentDocument
  * csp
  * featurePolicy
  * referrerPolicy
  * sandbox
  * srcdoc

## Rule Details

Example of **incorrect** code:

<!-- eslint-disable-next-line no-undef, no-unused-expressions -->
```js
iframe.allowPaymentRequest;
```
