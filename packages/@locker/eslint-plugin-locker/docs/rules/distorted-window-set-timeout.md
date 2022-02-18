# Distorted window.setTimeout (distorted-window-set-timeout)

For security the `window.setTimeout` constructor is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Window/docs/setTimeout-value.md -->
## window.setTimeout

The [`window.setTimeout()`](https://developer.mozilla.org/en-US/docs/Web/API/setTimeout) method sets a timer which executes a function or specified piece of code when the timer expires.

Code snippet execution is supported by accepting a string for the first argument. This string evaluation escapes the sandbox.

Lightning Web Security must evaluate the string in the sandbox.

### Distorted Behavior

If the first argument provided to `setTimeout` is a string value, this distortion evaluates the string in the sandbox.
<!-- END generated embed, please keep comment -->
