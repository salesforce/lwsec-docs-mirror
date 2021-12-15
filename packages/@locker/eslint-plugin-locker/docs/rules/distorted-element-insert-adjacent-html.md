# Distorted Element#insertAdjacentHTML (distorted-element-insert-adjacent-html)

For security `Element#insertAdjacentHTML` is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Element/docs/insertAdjacentHTML-value.md -->
## set: Element.prototype.insertAdjacentHTML [Main]

### Summary

In Locker, we share the HEAD and BODY. Even though it doesn't corrupt the existing elements inside or outside the element, if a malicious user can insert specified text as HTML into the DOM tree outside of the shared elements, it gives them the ability to pollute the DOM.

### Distorted Behavior

This distortion sanitizes HTML being added.
<!-- END generated embed please keep comment here to allow auto update -->
