# Distorted ResizeObserver.prototype.observe (distorted-resize-observer-observe)

For security `ResizeObserver.prototype.observe` is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/ResizeObserver/docs/observe-value.md -->
## ResizeObserver.prototype.observe

The [`ResizeObserver.prototype.observe()`](https://developer.mozilla.org/en-US/docs/Web/API/ResizeObserver/observe) method starts observing an element for resize notifications.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Without this distortion, sandboxed code could observe size changes on those elements and infer layout or DOM activity from trusted code or other sandboxes.

### Distorted Behavior

Calling `observe()` with a shared element (`<html>`, `<head>`, or `<body>`) as the target throws `LockerSecurityError`. Observing non-shared elements is unaffected.
<!-- END generated embed, please keep comment -->
