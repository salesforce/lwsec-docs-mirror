# Distorted HTMLElement#innerText Setter (distorted-html-element-inner-text-setter)

For security the `HTMLElement#innerText` setter is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/HTMLElement/docs/innerText-setter.md -->
## set: HTMLElement.prototype.innerText [Chrome, Edge, Opera, Safari]

### Summary

The innerText property of the HTMLElement interface represents the "rendered" text content of a node and its descendants. As a setter, it can be used to replace the rendered content of the element. Since Lightning Web Security runs in the main window, where the `<html>`, `<head>` and `<body>` elements are shared, malicious code could replace the contents of those elements by assigning a new value to the `.innerText` property, corrupting the DOM of the current rendered page.  

### Distorted Behavior

This distortion sanitizes and prevents text from replacing the text within the shared elements: `<html>`, `<head>` and `<body>`.
<!-- END generated embed, please keep comment -->
