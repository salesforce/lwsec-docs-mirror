# Distorted SharedWorker Constructor (distorted-shared-worker-constructor)

For security the `SharedWorker` constructor is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/SharedWorker/docs/constructor-value.md -->
## SharedWorker Global Constructor

### Summary

The `SharedWorker()` constructor creates a SharedWorker object that executes the script at the specified URL. This script must obey the same-origin policy. Malicious users can execute script at a specified URL to bypass Locker evaluation rules. 

### Distorted Behavior

Locker will throw a `RangeError` when calling the constructor. Locker will block access to `SharedWorker.prototype`.
<!-- END generated embed please keep comment here to allow auto update -->
