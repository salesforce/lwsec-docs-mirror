# Distorted Node.prototype.insertBefore (distorted-node-insertbefore)

For security the `Node.prototype.insertBefore` setter is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/Node/docs/insertBefore-value.md -->
## Node.prototype.insertBefore

The [`Node.prototype.insertBefore()`](https://developer.mozilla.org/en-US/docs/Web/API/Node/insertBefore) method of the `Node` interface inserts a node before a reference node as a child of a specified parent node.

If the given node already exists in the document, `insertBefore()` moves it from its current position to the new position. (That is, it will automatically be removed from its existing parent before appending it to the specified new parent.)

This means that a node cannot be in two locations of the document simultaneously.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can append a child element directly to those shared elements, corrupting the DOM of the current rendered page.

### Distorted Behavior

This distortion allows only a `<script>` or `<link>` element to be appended as a child to `<html>`, `<head>`, and `<body>` elements. It throws an exception if any other element is specified.
<!-- END generated embed, please keep comment -->
