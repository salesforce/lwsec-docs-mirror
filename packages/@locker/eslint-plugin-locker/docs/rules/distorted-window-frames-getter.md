# Distorted window.frames Getter (distorted-window-frames-getter)

For security the `window.frames` getter is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/Window/docs/frames-getter.md -->
## window.frames getter

The [`window.frames`](https://developer.mozilla.org/en-US/docs/Web/API/Window/frames) property returns an array-like object that lists all the `frame` and `iframe` elements in the current window.

```js
frameList = window.frames;
frameList === window; // evaluates to true (normally)
```

Lightning Web Security restricts access by distorting the `frameList` object returned, so that malicious code can't access `window` properties.

### Distorted Behavior

This distortion returns an artificial `frameList` object that includes
all `frame` and `iframe` elements in the document, in insertion order.

The `frameList` object supports access by index value or name property value, as the native one does.

However, the distorted `window.frames` doesn't allow access to `window` or provide proxy access to
`window` properties.

```js
framelist !== window; // evaluates to true with this distortion
```
<!-- END generated embed, please keep comment -->
