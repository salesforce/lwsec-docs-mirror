# Distorted Range.prototype.cloneRange (distorted-range-clone-range)

For security `Range.prototype.cloneRange` is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/Range/docs/cloneRange-value.md -->
## Range.prototype.cloneRange

The `Range` interface represents a fragment of a document that can contain nodes and parts of text nodes.

The [`Range.prototype.cloneRange()`](https://developer.mozilla.org/en-US/docs/Web/API/Range/cloneRange) method returns a `Range` object with boundary points identical to the cloned `Range`.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. The `cloneRange()` method can clone a range that references shared elements, enabling cross-sandbox content access.

### Distorted Behavior

This distortion prevents `cloneRange()` from cloning a range when it spans shared elements.
<!-- END generated embed, please keep comment -->
