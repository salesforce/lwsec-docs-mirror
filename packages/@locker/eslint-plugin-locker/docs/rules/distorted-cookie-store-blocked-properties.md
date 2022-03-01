# Disallowed CookieStore Properties (distorted-cookie-store-blocked-properties)

For security the following `CookieStore` properties are disallowed in Lightning Locker:

<!-- START generated embed: @locker/distortion/src/CookieStore/docs/addEventListener-value.md -->
## CookieStore.addEventListener

The [`addEventListener()`](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener) method of the `EventTarget` interface sets up a function that will be called whenever the specified event is delivered to the target.

Common targets are `Element`, or its children, `Document`, and `Window`, but the target may be any object that supports events (such as `XMLHttpRequest`).

This distortion prevents code from accessing cookies outside of the sandbox.

### Distorted Behavior

Currently, Lightning Web Security doesn't support the `CookieStore.onchange` event, so attaching an event listener to `CookieStore` is not allowed. Calls to `CookieStore.addEventListener()` return an error.
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/CookieStore/docs/onchange-setter.md -->
## CookieStore.prototype.onchange

The [`onchange`](https://developer.mozilla.org/en-US/docs/Web/API/CookieStore/onchange) EventHandler of the `CookieStore` interface fires when a change is made to any cookie.

This distortion prevents code from accessing cookies outside of the sandbox.

### Distorted Behavior

Currently, Lightning Web Security doesn't support the `CookieStore.onchange` event, so setting the `onchange` property is not allowed and returns an error.
<!-- END generated embed, please keep comment -->
