# Distorted Element#getInnerHTML (distorted-element-get-inner-html)

For security the `Element#getInnerHTML` is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/Element/docs/getInnerHTML-value.md -->
## Element.prototype.getInnerHTML

The `Element.prototype.getInnerHTML` property gets the HTML or XML markup contained within the element.

LWC's utilization of a synthetic shadow results in shadows that appear to be closed, but are actually open. To obtain the `innerHTML` of such open shadows, one can retrieve it by utilizing `getInnerHTML` on elements that are the parent of the shadow, with the `includeShadowRoots` option set to `true`.

### Distorted Behavior

This distortion sets the `includeShadowRoots` option from `true` to `false`.
<!-- END generated embed, please keep comment -->
