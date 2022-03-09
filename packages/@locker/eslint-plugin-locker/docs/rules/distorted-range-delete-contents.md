# Distorted Range.prototype.deleteContents (distorted-range-delete-contents)

For security `Range.prototype.deleteContents` is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/Range/docs/deleteContents-value.md -->
## Range.prototype.deleteContents

The `Range` interface represents a fragment of a document that can contain nodes and parts of text nodes.

The [`Range.prototype.deleteContents()`](https://developer.mozilla.org/en-US/docs/Web/API/Range/deleteContents) method removes the contents of the `Range` from the `Document`.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. The `deleteContents()` method can let malicious code remove the shared elements. LWS prevents the deletion of any shared elements.

### Distorted Behavior

This distortion prevents `deleteContents()` from removing any shared elements.
<!-- END generated embed, please keep comment -->
