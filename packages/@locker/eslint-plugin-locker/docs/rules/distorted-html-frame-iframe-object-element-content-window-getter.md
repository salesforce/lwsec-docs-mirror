# Distorted HTML{Frame|IFrame|Object}Element#contentWindow Getter (distorted-html-frame-iframe-object-element-content-window-getter)

For security the `HTML{Frame|IFrame|Object}Element#contentWindow` getter is
distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/HTMLFrameElement/docs/contentWindow-getter.md -->
## HTMLFrameElement.prototype.contentWindow getter

The `HTMLFrameElement.prototype.contentWindow` property returns the `Window` object of the specified frame. You can use this `Window` object to access the frame's document and its internal DOM. This attribute is read-only, but its properties can be manipulated like the global `Window` object. The `HTMLFrameElement` interface is deprecated in HTML5.

To reduce the possibility of exploit, Lightning Web Security creates an artificial `contentWindow` object that allows access to a reduced set of properties.
  - `close`
  - `closed`
  - `focus`
  - `opener`
  - `parent`
  - `postMessage`
### Distorted Behavior

This distortion returns an artificial `contentWindow` object per frame and caches the artificial `contentWindow` object for subsequent accesses.
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/HTMLIFrameElement/docs/contentWindow-getter.md -->
## HTMLIFrameElement.prototype.contentWindow getter

The [`HTMLIFrameElement.prototype.contentWindow`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLIFrameElement/contentWindow) property returns the `Window` object of an `HTMLIFrameElement`. You can use this `Window` object to access the iframe's document and its internal DOM. This attribute is read-only, but its properties can be manipulated like the global `Window` object.

To reduce the possibility of exploit, Lightning Web Security creates an artificial `contentWindow` object that allows access to a reduced set of properties.
  - `close`
  - `closed`
  - `focus`
  - `opener`
  - `parent`
  - `postMessage`

### Distorted Behavior

This distortion returns an artificial `contentWindow` object per iframe and caches the artificial `contentWindow` object for subsequent accesses.
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/HTMLObjectElement/docs/contentWindow-getter.md -->
## HTMLObjectElement.prototype.contentWindow getter

The [`HTMLObjectElement.prototype.contentWindow`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLObjectElement/contentWindow) property returns a `WindowProxy` representing the window proxy of the object element's nested browsing context, if any; otherwise null.

To reduce the possibility of exploit, Lightning Web Security creates an artificial `contentWindow` object that allows access to a reduced set of properties.
  - `close`
  - `closed`
  - `focus`
  - `opener`
  - `parent`
  - `postMessage`

### Distorted Behavior

This distortion returns an artificial `contentWindow` object per iframe and caches the artificial `contentWindow` object for subsequent accesses.
<!-- END generated embed, please keep comment -->
