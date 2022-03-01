# Distorted window.setInterval (distorted-window-set-interval)

For security the `window.setInterval` constructor is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Window/docs/setInterval-value.md -->
## window.setInterval

The [`window.setInterval()`](https://developer.mozilla.org/en-US/docs/Web/API/setInterval) method repeatedly calls a function or executes a code snippet, with a fixed time delay between each call. 

Code snippet execution is supported by accepting a string for the first argument. This string evaluation escapes the sandbox.

Lightning Web Security must evaluate the string in the sandbox.

### Distorted Behavior

If the first argument provided to `setInterval` is a string value, this distortion evaluates the string in the sandbox.
<!-- END generated embed, please keep comment -->
