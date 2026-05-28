# Distorted MutationObserver.prototype.observe (distorted-mutation-observer-observe)

For security `MutationObserver.prototype.observe` is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/MutationObserver/docs/observe-value.md -->
## MutationObserver.prototype.observe

The [`MutationObserver.prototype.observe()`](https://developer.mozilla.org/en-US/docs/Web/API/MutationObserver/observe) method configures the `MutationObserver` callback to begin receiving notifications of changes to the DOM that match the given options.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Without this distortion, sandboxed code could observe DOM mutations on shared elements, capturing node references, attribute values, and text content set by trusted code or other sandboxes.

### Distorted Behavior

This distortion prevents calling `observe()` with a shared element (`<html>`, `<head>`, or `<body>`) as the target. Observing non-shared elements is unaffected.
<!-- END generated embed, please keep comment -->
