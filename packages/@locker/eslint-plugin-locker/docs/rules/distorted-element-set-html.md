# Distorted Element#setHTML (distorted-element-set-html)

For security the `Element#setHTML` is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/Element/docs/setHTML-value.md -->
## Element.prototype.setHTML

The [`Element.prototype.setHTML()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/setHTML) method is used to parse and sanitize a string of HTML and then insert it into the DOM as a subtree of the element. It should be used instead of `Element.innerHTML` for inserting untrusted strings of HTML into an element.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can prepend nodes or text directly to shared `<head>` and `<body>` elements, corrupting the DOM of the current rendered page.

### Distorted Behavior

This distortion sanitizes and prevents HTML from replacing the DOM within shared `<head>` and `<body>` elements.
<!-- END generated embed, please keep comment -->
