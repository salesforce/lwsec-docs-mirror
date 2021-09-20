# Distorted HTMLElement#outerText Setter (distorted-html-element-outer-text-setter)

For security the `HTMLElement#outerText` setter is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/HTMLElement/docs/outerText-setter.md -->
## set: Element.prototype.outerText [Chrome, Edge, Opera, Safari]

### Summary

This property allows users to replace the element with his text. In Locker, we share the HEAD and BODY. This will allow a malicious user to replace the HEAD and BODY with his text. Therefore, corrupting the DOM.

### Distorted Behavior

This distortion sanitizes and prevents text from replacing the shared elements: HEAD and BODY.

Note that `outerText` [is not a standard property](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/outerText#Browser_compatibility), so the descriptor could be undefined, like in the case of Firefox. In this case, this distortion does nothing.
<!-- END generated embed please keep comment here to allow auto update -->
