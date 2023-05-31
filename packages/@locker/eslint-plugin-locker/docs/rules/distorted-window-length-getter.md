# Distorted window.length Getter (distorted-window-length-getter)

For security the `window.length` getter is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/Window/docs/length-getter.md -->
## window.length getter

The [`window.length`](https://developer.mozilla.org/en-US/docs/Web/API/Window/length) property returns the number of frames (either `<frame>` or `<iframe>` elements) attached to the `window` object's `document`.

### Distorted Behavior

The `window.length` property always returns `0`.

Instead of `window.length`, use the `window.frames.length` value and `window.frames` object to iterate over the list of frames (either `<frame>` or `<iframe>` elements) attached to the `document`.
<!-- END generated embed, please keep comment -->
