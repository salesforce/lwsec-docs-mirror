# Distorted Worker Constructor (distorted-worker-constructor)

For security the `Worker` constructor is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Worker/docs/constructor-value.md -->
## Worker Global Constructor

### Summary

The `Worker()` constructor creates a Worker object that executes the script at the specified URL. This script must obey the same-origin policy. Malicious users can execute script at a specified URL to bypass Locker evaluation rules. 

### Distorted Behavior

Locker will throw a `RangeError` when calling the constructor. Locker will block access to `Worker.prototype`.
<!-- END generated embed please keep comment here to allow auto update -->
