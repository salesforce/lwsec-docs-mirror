# Distorted window.fetch (distorted-window-fetch)

For security the `window.fetch` constructor is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/Window/docs/fetch-value.md -->
## Window.fetch

The global [`fetch()`](https://developer.mozilla.org/en-US/docs/Web/API/fetch) method starts the process of fetching a resource from the network, returning a promise that is fulfilled when the response is available.

Lightning Web Security disallows access to URL endpoints containing `"/aura"` and `"/webruntime"` because they are part of the Lightning Component framework.

### Distorted Behavior

This distortion examines the `hostname` and the `pathname` of the URL. If there's a match to a disallowed endpoint, it rejects the promise.
<!-- END generated embed, please keep comment -->
