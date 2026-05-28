# Distorted Selection.prototype.focusNode (distorted-selection-focus-node-getter)

For security `Selection.prototype.focusNode` is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/Selection/docs/focusNode-getter.md -->
## Selection.prototype.focusNode

The [`focusNode`](https://developer.mozilla.org/en-US/docs/Web/API/Selection/focusNode) read-only property returns the node in which the selection ends.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. The `focusNode` getter can leak references to shared elements, which could be used to inspect or manipulate content outside the sandbox boundary.

### Distorted Behavior

This distortion returns `null` when `focusNode` would return a shared element.
<!-- END generated embed, please keep comment -->
