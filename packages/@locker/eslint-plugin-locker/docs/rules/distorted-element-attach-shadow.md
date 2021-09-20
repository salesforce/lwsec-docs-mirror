# Distorted Element#attachShadow (distorted-element-attach-shadow)

For security `Element#attachShadow` is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Element/docs/attachShadow-value.md -->
## set: Element.prototype.attachShadow [Main]

### Summary

This method attaches a shadow DOM tree to the specified element. By providing
an options object with a `mode` of `'open'` the shadow DOM will be exposed to
the scripting environment allowing other namespaces access.

### Distorted Behavior

This distortion throws for any `mode` that is not `'closed'`, guarding against
additional modes added at later time, to prevent exposing the shadow DOM.
<!-- END generated embed please keep comment here to allow auto update -->
