# Distorted Node#textContent Setter (distorted-node-text-content-setter)

For security the `Node#textContent` setter is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Node/docs/textContent-setter.md -->
## set: Node.prototype.textContent [Main]

### Summary

This property allows users to replace DOM inside the element with his text. In Locker, we share the HEAD and BODY. This will allow a malicious user to replace the DOM of the HEAD and BODY with his text. Therefore, corrupting the DOM.

### Distorted Behavior

This distortion sanitizes and prevents text from replacing the DOM within shared elements: HEAD and BODY.
<!-- END generated embed please keep comment here to allow auto update -->
