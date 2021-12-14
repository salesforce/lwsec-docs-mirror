# Disallowed CookieStore Properties (distorted-cookie-store-blocked-properties)

For security the following `CookieStore` properties are disallowed in Lightning Locker:

<!-- START generated embed: @locker/distortion/src/CookieStore/docs/addEventListener-value.md -->
## CookieStore.addEventListener

### Goal

To prevent accessing cookies outside of the sandbox.

### Distorted Behavior

Currently, Lightning Web Security doesn't support the `CookieStore.onchange` event, so attaching an event listener to `CookieStore` is not allowed.
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/CookieStore/docs/onchange-setter.md -->
## CookieStore.prototype.onchange

### Goal

To prevent accessing cookies outside of the sandbox.

### Distorted Behavior

Currently, Lightning Web Security doesn't support the `CookieStore.onchange` event, so setting the `onchange` property is not allowed.
<!-- END generated embed, please keep comment -->
