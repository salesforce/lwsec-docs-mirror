# Distorted navigator.sendBeacon (distorted-navigator-sendBeacon)

For security the `navigator.sendBeacon()` function is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/Navigator/docs/sendBeacon-value.md -->
## Navigator.sendBeacon()

The [`navigator.sendBeacon()`](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/sendBeacon) method asynchronously sends an HTTP POST request containing a small amount of data to a web server.

Lightning Web Security disallows access to URL endpoints containing `"/aura"` and `"/webruntime"` because they are part of the Lightning Component framework.

### Distorted Behavior 

This distortion examines the `hostname` and the `pathname` of the URL. If there's a match to a disallowed endpoint, it rejects the promise.
<!-- END generated embed, please keep comment -->
