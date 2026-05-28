# Distorted Range.prototype.cloneContents (distorted-range-clone-contents)

For security `Range.prototype.cloneContents` is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/Range/docs/cloneContents-value.md -->
## Range.prototype.cloneContents

The `Range` interface represents a fragment of a document that can contain nodes and parts of text nodes.

The [`Range.prototype.cloneContents()`](https://developer.mozilla.org/en-US/docs/Web/API/Range/cloneContents) method returns a `DocumentFragment` copying the objects of type `Node` included in the `Range`.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. The `cloneContents()` method can clone content from shared elements, enabling cross-sandbox data exfiltration.

### Distorted Behavior

This distortion prevents `cloneContents()` from cloning any content when the range spans shared elements.
<!-- END generated embed, please keep comment -->
