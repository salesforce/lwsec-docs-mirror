# Distorted window.setInterval (distorted-window-set-interval)

For security the `window.setInterval` constructor is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Window/docs/setInterval-value.md -->
## value: Window.prototype.setInterval [Main]

### Summary

The `setInterval` method, repeatedly calls a function or executes a code snippet, with a fixed time delay between each call. But `setInterval` supports string evaluation by specifying a string for its first argument. This escapes the sandbox.

### Distorted Behavior

If the first argument provided to `setInterval` is a string value, this distortion evaluates it in the sandbox.
<!-- END generated embed please keep comment here to allow auto update -->
