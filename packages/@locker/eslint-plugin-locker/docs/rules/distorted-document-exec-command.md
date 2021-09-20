# Distorted document.execCommand (distorted-document-exec-command)

For security `document.execCommand` is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Document/docs/execCommand-value.md -->
## value: Document.prototype.execCommand [Main]

### Summary

When an HTML document has been switched to designMode, its document object exposes an execCommand method to run commands that manipulate the current editable region, such as form inputs or contentEditable elements. One command, "insertHTML" inserts new elements on the currently active editable element. 

In Locker, we share the HEAD and BODY. Even though it doesn't corrupt the existing elements inside or outside the element, if a malicious user can insert specified text as HTML into the DOM tree outside of the shared elements, it gives them the ability to pollute the DOM. We need to sanitize any elements added to this shared DOM.

### Distorted Behavior

This distortion sanitizes HTML string being inserted.
<!-- END generated embed please keep comment here to allow auto update -->
