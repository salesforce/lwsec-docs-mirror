# Distorted Observable (distorted-observable)

For security the `Observable.prototype.subscribe` and `Observable.prototype.forEach` methods are distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/Observable/docs/subscribe-value.md -->
## Observable.prototype.subscribe

The [`Observable.prototype.subscribe()`](https://developer.mozilla.org/en-US/docs/Web/API/Observable/subscribe) method subscribes to an observable sequence, invoking callbacks for each emitted value, error, or completion signal.

Passing `eval` or `Function` as a callback to `subscribe()` allows arbitrary string-to-code execution that can escape the sandbox boundary.

### Distorted Behavior

This distortion throws a `LockerSecurityError` if `eval` or `Function` is passed as the `next`, `error`, or `complete` callback (either directly as a function argument or as a property of the observer object).
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/Observable/docs/forEach-value.md -->
## Observable.prototype.forEach

The [`Observable.prototype.forEach()`](https://developer.mozilla.org/en-US/docs/Web/API/Observable/forEach) method subscribes to an observable and invokes a callback for each emitted value, returning a Promise that resolves on completion.

Passing `eval` or `Function` as the callback allows arbitrary string-to-code execution that can escape the sandbox boundary.

### Distorted Behavior

This distortion throws a `LockerSecurityError` if `eval` or `Function` is passed as the callback argument.
<!-- END generated embed, please keep comment -->
