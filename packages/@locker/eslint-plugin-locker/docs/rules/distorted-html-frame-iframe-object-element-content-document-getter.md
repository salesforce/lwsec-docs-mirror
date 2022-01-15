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
## get: HTMLFrameElement.prototype.contentDocument

To reduce the surface area of possible exploit we return `null` for the
`contentDocument` property of frames. At a later time we may explore multi
document support, but in the interest of simplicity and moving things along
we have decided to keep things simple.

### Goal

- Do not expose the real raw `contentDocument`

### Design

The value of `contentDocument` may be `null` so we enforce that it is.

### Distorted behavior

- Always return `null` for `contentDocument`
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/HTMLIFrameElement/docs/contentDocument-getter.md -->
## get: HTMLIFrameElement.prototype.contentDocument

To reduce the surface area of possible exploit we return `null` for the
`contentDocument` property of iframes. At a later time we may explore multi
document support, but in the interest of simplicity and moving things along
we have decided to keep things simple.

### Goal

- Do not expose the real raw `contentDocument`

### Design

The value of `contentDocument` may be `null` so we enforce that it is.

### Distorted behavior

- Always return `null` for `contentDocument`
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/HTMLObjectElement/docs/contentDocument-getter.md -->
## get: HTMLObjectElement.prototype.contentDocument

To reduce the surface area of possible exploit we return `null` for the
`contentDocument` property of object elements. At a later time we may explore
multi document support, but in the interest of simplicity and moving things along
we have decided to keep things simple.

### Goal

- Do not expose the real raw `contentDocument`

### Design

The value of `contentDocument` may be `null` so we enforce that it is.

### Distorted behavior

- Always return `null` for `contentDocument`
<!-- END generated embed, please keep comment -->
