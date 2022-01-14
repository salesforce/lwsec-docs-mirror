# Distorted Element#insertAdjacentHTML (distorted-element-insert-adjacent-html)

For security `Element#insertAdjacentHTML` is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Element/docs/insertAdjacentHTML-value.md -->
## Element.prototype.insertAdjacentHTML

The [`Element.insertAdjacentHTML()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/insertAdjacentHTML) method parses the specified text as HTML or XML and inserts the resulting nodes into the DOM tree at a specified position. 

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can be added to those elements by using the `insertAdjacentHTML()` method, corrupting the DOM of the current rendered page. 

### Distorted Behavior

This distortion sanitizes the text string to prevent malicious code from being added to the `<html>`, `<head>`, and `<body>` shared elements.
<!-- END generated embed, please keep comment -->
