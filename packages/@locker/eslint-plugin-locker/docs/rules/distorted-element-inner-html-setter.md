# Distorted Element#innerHTML Setter (distorted-element-inner-html-setter)

For security the `Element#innerHTML` setter is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Element/docs/innerHTML-setter.md -->
## set: Element.prototype.innerHTML [Main]

### Summary

This property allows users to replace DOM inside the element with nodes parsed from the given specified text as HTML. In Locker, we share the HEAD and BODY. This will allow a malicious user to replace the DOM of the HEAD and BODY with his specified text as HTML. Therefore, corrupting the DOM.

### Distorted Behavior

This distortion sanitizes and prevents HTML from replacing the DOM within shared elements: HEAD and BODY.
<!-- END generated embed please keep comment here to allow auto update -->
