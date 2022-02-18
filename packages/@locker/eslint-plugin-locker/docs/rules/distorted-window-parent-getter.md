# Distorted window.parent Getter (distorted-window-parent-getter)

For security the `window.parent` getter is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Window/docs/parent-getter.md -->
## window.parent getter

The [`window.parent`](https://developer.mozilla.org/en-US/docs/Web/API/Window/parent) property returns a reference to the parent of the current window or subframe. If a window does not have a parent, its `parent` property is a reference to itself.

If window `A` embeds window `B`, `B.parent` returns `A`.

### Distorted Behavior

This distortion returns an artificial `window` object that allows only safe methods.

- `close`
- `focus`
- `postMessage`

[//]: # (This will change after multi-window support)
<!-- END generated embed, please keep comment -->
