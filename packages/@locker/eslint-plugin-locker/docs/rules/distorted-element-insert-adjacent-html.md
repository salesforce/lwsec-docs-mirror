# Distorted Element#insertAdjacentHTML (distorted-element-insert-adjacent-html)

For security `Element#insertAdjacentHTML` is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Element/docs/insertAdjacentHTML-value.md -->
## Element.prototype.insertAdjacentHTML

### Summary

> The [`Element.insertAdjacentHTML()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/insertAdjacentElinsertAdjacentHTMLement) method inserts a `DOMString` object before or after the beggining of the `Element`, or before or after the end of the `Element`. 

Since Lightning Web Security runs in the main window, where the `<html>`, `<head>` and `<body>` elements are shared, malicious code could be added to those elements by using the insertAdjacentHTML method, corrupting the DOM of the current rendered page.  

### Distorted Behavior

This distortion sanitizes and prevents malicious code added to the shared elements: `<html>`, `<head>` and `<body>`.
<!-- END generated embed, please keep comment -->
