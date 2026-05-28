# Distorted ReportingObserver constructor (distorted-reporting-observer-constructor)

For security the `ReportingObserver` constructor is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/ReportingObserver/docs/constructor-value.md -->
## ReportingObserver Constructor

The [`ReportingObserver()`](https://developer.mozilla.org/en-US/docs/Web/API/ReportingObserver/ReportingObserver) constructor creates a `ReportingObserver` object that collects reporting events such as CSP violations and deprecation reports.

Those reports can include URLs, document locations, and source metadata from trusted code. On a shared window timeline, sandboxed observers would receive cross-tenant reporting data.

### Distorted Behavior

This distortion throws an exception when calling the constructor, and blocks access to `ReportingObserver.prototype`.
<!-- END generated embed, please keep comment -->
