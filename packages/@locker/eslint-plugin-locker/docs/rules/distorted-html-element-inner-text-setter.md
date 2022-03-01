# Distorted HTMLElement#innerText Setter (distorted-html-element-inner-text-setter)

For security the `HTMLElement#innerText` setter is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/HTMLElement/docs/innerText-setter.md -->
## HTMLElement.prototype.innerText setter [Chrome, Edge, Opera, Safari]

The [`HTMLElement.prototype.innerText`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/innerText) property of represents the "rendered" text content of a node and its descendants. As a setter, it can be used to replace the rendered content of the element. 

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can replace the contents of those elements by assigning a new value to the `.innerText` property, corrupting the DOM of the current rendered page.  

### Distorted Behavior

This distortion sanitizes the given text and prevents it from replacing the text within the shared elements `<html>`, `<head>`, and `<body>`.
<!-- END generated embed, please keep comment -->
