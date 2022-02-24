# Distorted HTMLElement#outerText Setter (distorted-html-element-outer-text-setter)

For security the `HTMLElement#outerText` setter is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/HTMLElement/docs/outerText-setter.md -->
## HTMLElement.prototype.outerText setter

[`HTMLElement.prototype.outerText`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/outerText) is a non-standard property. As a getter, it returns the same value as `HTMLElement.prototype.innerText`. As a setter, it removes the current node and replaces it with the given text.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can replace the `<head>` and `<body>` elements, corrupting the DOM.

### Distorted Behavior

This distortion sanitizes the given text and prevents it from replacing the shared elements `<head>` and `<body>`.

As a non-standard property, the `outerText` descriptor could be undefined. Firefox doesn't support the property, so the distortion does nothing in that browser.
<!-- END generated embed, please keep comment -->
