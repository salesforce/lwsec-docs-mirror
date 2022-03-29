# Distorted Range.prototype.insertNode (distorted-range-insertnode)

For security `Range.prototype.insertNode` is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/Range/docs/insertNode-value.md -->
## Range.prototype.insertNode

The [`Range.prototype.insertNode()`](https://developer.mozilla.org/en-US/docs/Web/API/Range/insertNode) method inserts a node at the start of the `Range`.

The new node is inserted at the start boundary point of the `Range`. If the new node is to be added to a text `Node`, that `Node` is split at the insertion point, and the insertion occurs between the two text nodes.

If the new node is a document fragment, the children of the document fragment are inserted instead.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. The `insertNode()` method can let malicious code move the shared elements. LWS prevents moving any shared elements.

### Distorted Behavior

This distortion allows only a `<script>` or `<link>` element to be inserted as an immediate child to `<html>`, `<head>`, and `<body>` elements. It throws an exception if any other element is specified.
<!-- END generated embed, please keep comment -->
