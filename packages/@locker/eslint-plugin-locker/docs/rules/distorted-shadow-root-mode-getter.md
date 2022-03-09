# Distorted ShadowRoot#mode Getter (distorted-shadow-root-mode-getter)

For security the `ShadowRoot#mode` getter is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/ShadowRoot/docs/mode-getter.md -->
## ShadowRoot.prototype.mode getter

The [`ShadowRoot.prototype.mode`](https://developer.mozilla.org/en-US/docs/Web/API/ShadowRoot/mode) property determines whether the shadow root is accessible from JavaScript. When the value is `closed` the shadow root is not exposed to the scripting environment. The shadow root’s implementation internals are inaccessible and unchangeable from JavaScript.

### Distorted Behavior

This distortion returns `closed` when a getter accesses the `mode` property on any element with an attached shadow DOM.
<!-- END generated embed, please keep comment -->
