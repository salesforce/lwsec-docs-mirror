# Distorted window.parent Getter (distorted-window-parent-getter)

For security the `window.parent` getter is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Window/docs/parent-getter.md -->
## get: window.parent [Main]

### Summary

The Window interface's `parent` property returns a reference to the parent of the current window or subframe. If a window does not have a parent, its parent property is a reference to itself. If window A embeds window B, B.parent returns A.

### Distorted Behavior

Locker will return a patched `Window` object that contains specific safe methods we allow.
<!-- END generated embed please keep comment here to allow auto update -->
