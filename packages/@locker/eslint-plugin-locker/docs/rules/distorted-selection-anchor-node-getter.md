# Distorted Selection.prototype.anchorNode (distorted-selection-anchor-node-getter)

For security `Selection.prototype.anchorNode` is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/Selection/docs/anchorNode-getter.md -->
## Selection.prototype.anchorNode

The [`anchorNode`](https://developer.mozilla.org/en-US/docs/Web/API/Selection/anchorNode) read-only property returns the node in which the selection begins.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. The `anchorNode` getter can leak references to shared elements, which could be used to inspect or manipulate content outside the sandbox boundary.

### Distorted Behavior

This distortion returns `null` when `anchorNode` would return a shared element.
<!-- END generated embed, please keep comment -->
