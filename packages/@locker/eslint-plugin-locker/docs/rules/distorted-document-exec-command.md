# Distorted document.execCommand (distorted-document-exec-command)

For security `document.execCommand` is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/Document/docs/execCommand-value.md -->
## Document.prototype.execCommand

When an HTML document has been switched to `designMode`, its `document` object exposes an [`execCommand()`](https://developer.mozilla.org/en-US/docs/Web/API/Document/execCommand) method to run commands that manipulate the current editable region, such as form inputs or `contentEditable` elements.

The `insertHTML` command inserts new elements on the currently active editable element.

Lightning Web Security runs in the main window, where the `<html>`, `<head>` and `<body>` elements are shared. If malicious code can insert any specified text as HTML into the DOM tree, even outside of the shared `<head>` and `<body>` elements, it can pollute the DOM. For this reason, any elements added to this shared DOM are sanitized to strip out malicious code.
### Distorted Behavior

This distortion sanitizes the inserted HTML string.
<!-- END generated embed, please keep comment -->
