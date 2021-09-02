# Distorted window.fetch (distorted-window-fetch)

For security the `window.fetch` constructor is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Window/docs/fetch-value.md -->
## Window.fetch

### Goal

To prevent users from making requests to disallowed endpoints.

### Design

Patch the `Window.fetch` property and intercept calls to it to block disallowed URLs.

### Distorted behavior

The `Window.fetch` distortion examines the `hostname` and the `pathname` of the URL, and if it matches one of the disallowed entries, it rejects the promise.

### Disallowed endpoints

Locker disallows endpoints:

- Containing `"/aura"` in the URL.
- Containing `"/webruntime"` in the URL.

At the moment this is hard coded, but in the future this will be a configuration option.
<!-- END generated embed please keep comment here to allow auto update -->
