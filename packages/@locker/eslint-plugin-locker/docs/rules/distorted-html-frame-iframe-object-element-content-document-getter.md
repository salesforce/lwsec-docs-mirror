# Prevent access to HTML{Frame|IFrame|Object}Element.contentDocument (distorted-html-frame-iframe-object-element-content-document-getter)

The `HTML{Frame|IFrame|Object}Element.contentDocument` getter returns `null` when Lightning Web Security is enabled.

See [Related Distortions](#related-distortions) below for more details.

## Rule Details

Example of **incorrect** code:

```js
document.getElementsByTagName('iframe')[0].contentDocument;
```

## Related Distortions

<!-- START generated embed: @locker/distortion/src/HTMLFrameElement/docs/contentDocument-getter.md -->
## HTMLFrameElement.prototype.contentDocument getter

The `HTMLFrameElement.prototype.contentDocument` property getter returns the `Document` object of the specified frame. 
The `HTMLFrameElement` interface is deprecated in HTML5.

To reduce the possibility of exploit, Lightning Web Security returns `null` for the `HTMLFrameElement.prototype.contentDocument` property.
### Distorted Behavior

This distortion returns `null` for `contentDocument`.
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/HTMLIFrameElement/docs/contentDocument-getter.md -->
## HTMLIFrameElement.prototype.contentDocument getter

The [`HTMLIFrameElement.contentDocument`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLIFrameElement/contentDocument) property getter returns a `Document` corresponding to the active document in the inline frame's nested browsing context if the iframe and the iframe's parent document are Same Origin. Otherwise, the property returns `null`. 

To reduce the possibility of exploit, Lightning Web Security returns `null` for the `contentDocument` property, even when an iframe and the iframe's parent document have the same origin.

### Distorted Behavior

This distortion returns `null` for `contentDocument`.
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/HTMLObjectElement/docs/contentDocument-getter.md -->
## HTMLObjectElement.prototype.contentDocument getter

The [`HTMLObjectElement.prototype.contentDocument`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLObjectElement/contentDocument) read-only property returns a `Document` representing the active document of the object element's nested browsing context, if any; otherwise null.

To reduce the possibility of exploit, Lightning Web Security returns `null` for the `contentDocument` property of object elements.
### Distorted Behavior

This distortion returns `null` for `contentDocument`.
<!-- END generated embed, please keep comment -->
