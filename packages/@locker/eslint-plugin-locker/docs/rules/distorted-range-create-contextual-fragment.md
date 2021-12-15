# Distorted Range#createContextualFragment (distorted-range-create-contextual-fragment)

For security `Range#createContextualFragment` is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Range/docs/createContextualFragment-value.md -->
## value: Range.prototype.createContextualFragment [Main]

### Summary

The Range.createContextualFragment() method returns a DocumentFragment by invoking the HTML fragment parsing algorithm or the XML fragment parsing algorithm with the start of the range as the context node. This range of HTML elements can be added to the DOM tree.

In Locker, we share the HEAD and BODY. Even though it doesn't corrupt the existing elements inside or outside the element, if a malicious user can insert specified text as HTML into the DOM tree outside of the shared elements, it gives them the ability to pollute the DOM. We need to sanitize any elements added to this shared DOM.

### Distorted Behavior

This distortion sanitizes HTML string that is used to create the DocumentFragment.
<!-- END generated embed please keep comment here to allow auto update -->
