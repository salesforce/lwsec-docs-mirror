# Distorted window.fetchLater (distorted-window-fetchLater)

For security the `window.fetchLater` constructor is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/Window/docs/fetchLater-value.md -->
## Window.fetchLater

A [`fetchLater()`](https://developer.mozilla.org/en-US/docs/Web/API/fetchLater) request is sent once the page is navigated away from (it is destroyed or enters the `bfcache`), or after a provided `activateAfter` timeout — whichever comes first.

The `fetchLater()` methods returns a `FetchLaterResult` object containing a single activated value stating whether the request has been sent yet. Note the method does not return the result of the actual fetch when that happens (since it is often sent after the document has been destroyed) and the whole response of the fetch, including body and headers, is ignored.

Lightning Web Security disallows access to URL endpoints containing `"/aura"` and `"/webruntime"` because they are part of the Lightning Component framework.

### Distorted Behavior

This distortion examines the `hostname` and the `pathname` of the URL. If there's a match to a disallowed endpoint, it throws.
<!-- END generated embed, please keep comment -->
