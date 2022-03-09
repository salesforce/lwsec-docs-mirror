# Prevent access to Worker constructor (distorted-worker-constructor)

A `RangeError` will be thrown accessing the `Worker` constructor when Lightning Web Security is enabled.

See [Related Distortions](#related-distortions) below for more details.

## Rule Details

Example of **incorrect** code:

```js
const worker = new Worker('/worker.js');
```

## Related Distortions

<!-- START generated embed: @locker/distortion/src/Worker/docs/constructor-value.md -->
## Worker Constructor

The [`Worker()`](https://developer.mozilla.org/en-US/docs/Web/API/Worker/Worker) constructor creates a `Worker` object that executes the script at the specified URL. This script must obey the same-origin policy.

Malicious code can execute a script at a specified URL to bypass Lightning Web Security evaluation rules.

### Distorted Behavior

Lightning Web Security throws an exception `Lightning Web Security: Cannot create Worker with ${url}` when calling the constructor. Lightning Web Security blocks access to `Worker.prototype`.
<!-- END generated embed, please keep comment -->
