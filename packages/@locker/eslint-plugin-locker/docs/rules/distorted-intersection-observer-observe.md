# Distorted IntersectionObserver.prototype.observe (distorted-intersection-observer-observe)

For security `IntersectionObserver.prototype.observe` is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/IntersectionObserver/docs/observe-value.md -->
## IntersectionObserver.prototype.observe

The [`IntersectionObserver.prototype.observe()`](https://developer.mozilla.org/en-US/docs/Web/API/IntersectionObserver/observe) method registers a target element to be observed for intersection with the observer's root or the viewport.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Without this distortion, sandboxed code could observe those elements (or use them as `root`) and infer visibility and layout signals from trusted code or other sandboxes.

### Distorted Behavior

- Calling `observe()` with a shared element as the **target** throws `LockerSecurityError`.
- If `options.root` is an `Element` and is a shared element, `observe()` throws `LockerSecurityError`.
- Observing with the default viewport root (`root: null` / omitted) is allowed.

Observing non-shared targets with non-shared roots is unaffected.
<!-- END generated embed, please keep comment -->
