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
## Worker Global Constructor

### Summary

The `Worker()` constructor creates a Worker object that executes the script at the specified URL. This script must obey the same-origin policy. Malicious users can execute script at a specified URL to bypass Lightning Web Security evaluation rules. 

### Distorted Behavior

Lightning Web Security will throw a `RangeError` when calling the constructor. Lightning Web Security will block access to `Worker.prototype`.
<!-- END generated embed, please keep comment -->
