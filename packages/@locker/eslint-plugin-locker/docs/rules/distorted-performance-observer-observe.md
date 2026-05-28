# Distorted PerformanceObserver.prototype.observe (distorted-performance-observer-observe)

For security `PerformanceObserver.prototype.observe` is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/PerformanceObserver/docs/observe-value.md -->
## PerformanceObserver.prototype.observe

The [`PerformanceObserver.prototype.observe()`](https://developer.mozilla.org/en-US/docs/Web/API/PerformanceObserver/observe) method registers the observer for specific performance entry types on the window's shared performance timeline.

Without this distortion, sandboxed code could subscribe to entry types that expose cross-tenant data (for example resource URLs from trusted fetches or navigation timing).

### Distorted Behavior

`observe()` throws `LockerSecurityError` if the `PerformanceObserverInit` requests any of these entry types: `resource`, `navigation`, `longtask`, `element`, `layout-shift`, `largest-contentful-paint`, `first-input`, or `event`.

Other entry types (such as `mark` and `measure`) are unaffected.
<!-- END generated embed, please keep comment -->
