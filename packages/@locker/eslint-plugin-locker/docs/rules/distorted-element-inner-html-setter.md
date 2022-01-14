# Distorted Element#innerHTML Setter (distorted-element-inner-html-setter)

For security the `Element#innerHTML` setter is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Element/docs/innerHTML-setter.md -->
## Element.prototype.innerHTML setter

The [`Element.prototype.innerHTML`](https://developer.mozilla.org/en-US/docs/Web/API/Element/innerHTML) property gets or sets the HTML or XML markup contained within the element. 

You can set `Element.prototype.innerHTML` to replace DOM inside the element with nodes parsed from the given specified text as HTML. 

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can replace the DOM of the `<head>` and `<body>` elements, corrupting the DOM.

### Distorted Behavior

This distortion sanitizes and prevents HTML from replacing the DOM within shared `<head>` and `<body>` elements.
<!-- END generated embed, please keep comment -->
