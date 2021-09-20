# Distorted window.opener Getter (distorted-window-opener-getter)

For security the `window.opener` getter is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Window/docs/opener-getter.md -->
## get: window.opener [Main]

### Summary

The Window interface's `opener` property returns a reference to the window that opened the window, either with open(), or by navigating a link with a target attribute.

In other words, if window A opens window B, B.opener returns A.

### Distorted Behavior

Locker will return an artificial `Window` object that contains specific safe methods we allow.
<!-- END generated embed please keep comment here to allow auto update -->
