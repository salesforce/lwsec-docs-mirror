# Distorted {XMLHttpRequest|Window}#open (distorted-xml-http-request-window-open)

For security `{XMLHttpRequest|Window}#open` is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/XMLHttpRequest/docs/open-value.md -->
## XMLHttpRequest.prototype.open

The [`XMLHttpRequest.prototype.open()`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/open) method initializes a newly-created request, or re-initializes an existing one.

Lightning Web Security disallows access to URL endpoints containing `"/aura"` and `"/webruntime"` because they are part of the Lightning Component framework.

### Distorted Behavior

This distortion examines the `hostname` and the `pathname` of the URL. If there's a match to a disallowed endpoint, it throws an exception.
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/Window/docs/open-value.md -->
## window.open

The [`window.open()`](https://developer.mozilla.org/en-US/docs/Web/API/Window/open) method loads the specified resource into a new or existing browsing context with the specified name. If the name doesn't exist, then a new browsing context is opened in a new tab or a new window, and the specified resource is loaded into it. 

This new browsing context isn’t sandboxed properly and malicious code can access system mode, so Lightning Web Security distorts the `window` object returned.

### Distorted Behavior

This distortion returns an artificial `window` object that allows only safe methods.

- `close`
- `focus`
- `postMessage`

[//]: # (This will change after multi-window support)
<!-- END generated embed, please keep comment -->
