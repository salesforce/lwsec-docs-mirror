# Distorted Range.prototype.extractContents (distorted-range-extract-contents)

For security `Range.prototype.extractContents` is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Range/docs/extractContents-value.md -->
## Range.prototype.extractContents

The `Range` interface represents a fragment of a document that can contain nodes and parts of text nodes.

The [`Range.prototype.extractContents()`](https://developer.mozilla.org/en-US/docs/Web/API/Range/extractContents) method moves contents of the `Range` from the document tree into a `DocumentFragment`.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. The `extractContents()` method can let malicious code move the shared elements. LWS prevents moving any shared elements.

### Distorted Behavior

This distortion prevents `extractContents()` from moving any shared elements.
<!-- END generated embed, please keep comment -->