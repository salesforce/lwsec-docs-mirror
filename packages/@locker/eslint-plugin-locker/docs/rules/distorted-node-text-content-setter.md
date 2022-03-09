# Distorted Node#textContent Setter (distorted-node-text-content-setter)

For security the `Node#textContent` setter is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/Node/docs/textContent-setter.md -->
## Node.prototype.textContent setter

The [`Node.prototype.textContent`](https://developer.mozilla.org/en-US/docs/Web/API/Node/textContent) property represents the text content of the node and its descendants.

This property allows you to replace DOM inside the element with your own text.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can replace the DOM of those shared elements, corrupting the DOM of the current rendered page.

### Distorted Behavior

This distortion sanitizes the given text to prevent replacing the DOM within the shared elements `<html>`, `<head>`, and `<body>`.
<!-- END generated embed, please keep comment -->
