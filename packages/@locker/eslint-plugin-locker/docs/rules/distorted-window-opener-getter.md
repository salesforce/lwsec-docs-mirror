# Distorted window.opener Getter (distorted-window-opener-getter)

For security the `window.opener` getter is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Window/docs/opener-getter.md -->
## window.opener getter

The [`window.opener`](https://developer.mozilla.org/en-US/docs/Web/API/Window/opener) property getter returns a reference to the window that opened the window, either with `open()`, or by navigating a link with a `target` attribute.

In other words, if window `A` opens window `B`, `B.opener` returns `A`.

Lightning Web Security doesn't allow access to the raw `window` object.

### Distorted Behavior

This distortion returns an artificial `window` object that allows only safe methods.

- `close`
- `focus`
- `postMessage`

[//]: # (This will change after multi-window support)
<!-- END generated embed, please keep comment -->
