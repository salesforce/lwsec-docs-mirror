# Distorted HTML{Frame|IFrame|Object}Element#contentDocument Getter (distorted-html-frame-iframe-object-element-content-document-getter)

For security the `HTML{Frame|IFrame|Object}Element#contentDocument` getter is
distorted in Lightning Locker.

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
<!-- END generated embed please keep comment here to allow auto update -->

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
<!-- END generated embed please keep comment here to allow auto update -->

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
<!-- END generated embed please keep comment here to allow auto update -->
