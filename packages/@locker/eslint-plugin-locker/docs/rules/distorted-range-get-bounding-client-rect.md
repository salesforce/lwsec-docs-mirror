# Distorted Range.prototype.getBoundingClientRect (distorted-range-get-bounding-client-rect)

For security `Range.prototype.getBoundingClientRect` is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/Range/docs/getBoundingClientRect-value.md -->
## Range.prototype.getBoundingClientRect

The `Range` interface represents a fragment of a document that can contain nodes and parts of text nodes.

The [`Range.prototype.getBoundingClientRect()`](https://developer.mozilla.org/en-US/docs/Web/API/Range/getBoundingClientRect) method returns a `DOMRect` object that bounds the contents of the range.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. The `getBoundingClientRect()` method can leak layout information about shared elements, revealing the position and size of content outside the sandbox boundary.

### Distorted Behavior

This distortion prevents `getBoundingClientRect()` from returning layout information when the range spans shared elements.
<!-- END generated embed, please keep comment -->
