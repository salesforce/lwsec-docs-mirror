# Distorted Element#outerHTML Setter (distorted-element-outer-html-setter)

For security the `Element#outerHTML` setter is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Element/docs/outerHTML-setter.md -->
## Element.prototype.outerHTML setter

The [`Element.outerHTML`](https://developer.mozilla.org/en-US/docs/Web/API/Element/outerHTML)  property gets or sets the serialized HTML fragment describing the element including its descendants. It can also be set to replace the element with nodes parsed from the given string.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can replace the `<head>` and `<body>` elements, corrupting the DOM.

### Distorted Behavior

This distortion sanitizes and prevents HTML from replacing the shared `<head>` and `<body>` elements.
<!-- END generated embed, please keep comment -->
