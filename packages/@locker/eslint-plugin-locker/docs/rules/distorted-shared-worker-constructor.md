# Prevent access to the SharedWorker constructor (distorted-shared-worker-constructor)

A `RangeError` will be thrown accessing the `SharedWorker` constructor when Lightning Web Security is enabled.

See [Related Distortions](#related-distortions) below for more details.

## Rule Details

Example of **incorrect** code:

```js
const worker = new SharedWorker('worker.js');
```

## Related Distortions

<!-- START generated embed: @locker/distortion/src/SharedWorker/docs/constructor-value.md -->
## SharedWorker Global Constructor

The [`SharedWorker()`](https://developer.mozilla.org/en-US/docs/Web/API/SharedWorker/SharedWorker) constructor creates a `SharedWorker` object that executes the script at the specified URL. This script must obey the same-origin policy, a security mechanism that restricts how a document or script loaded by one origin can interact with a resource from another origin.

Malicious code can use `SharedWorker()` to execute script at a specified URL to bypass Lightning Web Security distortions. 

### Distorted Behavior

This distortion throws an exception when calling the constructor, and blocks access to `SharedWorker.prototype`.
<!-- END generated embed, please keep comment -->
