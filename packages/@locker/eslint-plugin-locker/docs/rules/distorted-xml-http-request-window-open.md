# Distorted {XMLHttpRequest|Window}#open (distorted-xml-http-request-window-open)

For security `{XMLHttpRequest|Window}#open` is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/XMLHttpRequest/docs/open-value.md -->
## XMLHttpRequest.open

### Goal

To prevent users from making requests to disallowed endpoints.

### Design

Patch the `XMLHttpRequest.open` property and intercept calls to it to block disallowed URLs.

### Distorted Behavior

The `XMLHttpRequest.open` distortion examines the `hostname` and the `pathname` of the URL, and if it matches one of the disallowed entries, it throws an error.

### Disallowed endpoints

Lightning Web Security disallows endpoints:

- Containing `"/aura"` in the URL.
- Containing `"/webruntime"` in the URL.

At the moment this is hard coded, but in the future this will be a configuration option.
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/Window/docs/open-value.md -->
## Window.prototype.open

### Summary

The `open` method, loads the specified resource into a new or existing browsing context with the specified name. If the name doesn't exist, then a new browsing context is opened in a new tab or a new window, and the specified resource is loaded into it. This new context is not sandboxed properly and malicious users can access system mode.

### Distorted Behavior

Lightning Web Security will return an artificial `Window` object that contains specific safe methods we allow.
<!-- END generated embed, please keep comment -->
