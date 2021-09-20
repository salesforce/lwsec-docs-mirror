# Distorted HTML{Frame|IFrame|Object}Element#contentWindow Getter (distorted-html-frame-iframe-object-element-content-window-getter)

For security the `HTML{Frame|IFrame|Object}Element#contentWindow` getter is
distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/HTMLFrameElement/docs/contentWindow-getter.md -->
## get: HTMLFrameElement.prototype.contentWindow

To reduce the surface area of possible exploit we produce an artificial
`contentWindow` object. At a later time we may explore nesting sandboxes,
but in the interest of simplicity and moving things along we have decided to
keep things simple.

### Goal
- Do not expose the real raw `contentWindow`
- Restrict access to a small curated list of properties

### Design

Create an artificial `contentWindow` object with a curated list of properties
  - close
  - closed
  - focus
  - opener
  - parent
  - postMessage

### Distorted behavior
- Return an artificial `contentWindow` object per frame
- Cache the artificial `contentWindow` object for subsequent accesses
<!-- END generated embed please keep comment here to allow auto update -->

<!-- START generated embed: @locker/distortion/src/HTMLIFrameElement/docs/contentWindow-getter.md -->
## get: HTMLIFrameElement.prototype.contentWindow

To reduce the surface area of possible exploit we produce an artificial
`contentWindow` object. At a later time we may explore nesting sandboxes,
but in the interest of simplicity and moving things along we have decided to
keep things simple.

### Goal
- Do not expose the real raw `contentWindow`
- Restrict access to a small curated list of properties

### Design

Create an artificial `contentWindow` object with a curated list of properties
  - close
  - closed
  - focus
  - opener
  - parent
  - postMessage

### Distorted behavior
- Return an artificial `contentWindow` object per iframe
- Cache the artificial `contentWindow` object for subsequent accesses
<!-- END generated embed please keep comment here to allow auto update -->

<!-- START generated embed: @locker/distortion/src/HTMLObjectElement/docs/contentWindow-getter.md -->
## get: HTMLObjectElement.prototype.contentWindow

To reduce the surface area of possible exploit we produce an artificial
`contentWindow` object. At a later time we may explore nesting sandboxes,
but in the interest of simplicity and moving things along we have decided to
keep things simple.

### Goal
- Do not expose the real raw `contentWindow`
- Restrict access to a small curated list of properties

### Design

Create an artificial `contentWindow` object with a curated list of properties
  - close
  - closed
  - focus
  - opener
  - parent
  - postMessage

### Distorted behavior
- Return an artificial `contentWindow` object per object element
- Cache the artificial `contentWindow` object for subsequent accesses
<!-- END generated embed please keep comment here to allow auto update -->
