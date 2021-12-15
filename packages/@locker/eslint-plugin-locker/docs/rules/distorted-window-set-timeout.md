# Distorted window.setTimeout (distorted-window-set-timeout)

For security the `window.setTimeout` constructor is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Window/docs/setTimeout-value.md -->
## value: window.setTimeout [Main]

### Summary

The `setTimeout` method, repeatedly calls a function or executes a code snippet, with a fixed time delay between each call. But `setTimeout` supports string evaluation by specifying a string for its first argument. This escapes the sandbox.

### Distorted Behavior

If the first argument provided to `setTimeout` is a string value, this distortion evaluates it in the sandbox.
<!-- END generated embed please keep comment here to allow auto update -->
