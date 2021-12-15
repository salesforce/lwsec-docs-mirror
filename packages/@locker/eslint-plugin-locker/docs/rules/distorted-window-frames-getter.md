# Distorted window.frames Getter (distorted-window-frames-getter)

For security the `window.frames` getter is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Window/docs/frames-getter.md -->
## get: window.frames [Main]

### Summary

The Window interface's `frames` property returns an object that is the window
itself, which is an array-like object, listing the direct sub-frames of the
current window.

### Distorted Behavior

The Window interface's `frames` property returns a fake `frameList` that includes
all `<frame>` and `<iframe>` elements in the document, in insertion order. Supports
access via index or name property value. `window.frames` does not allow access to
`window`, ie. `window.frames !== window`, and does not provide proxy access to
`window` properties.
<!-- END generated embed please keep comment here to allow auto update -->
