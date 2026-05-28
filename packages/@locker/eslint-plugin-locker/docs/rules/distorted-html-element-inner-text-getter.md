# Distorted HTMLElement.prototype.innerText getter (distorted-html-element-inner-text-getter)

For security the `HTMLElement.prototype.innerText` getter is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/HTMLElement/docs/innerText-getter.md -->
## HTMLElement.prototype.innerText getter

The [`HTMLElement.prototype.innerText`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/innerText) property represents the rendered text content of a node and its descendants.

This distortion protects `HTMLElement.prototype.innerText` and prevents sandboxed code from reading the source of inline scripts that were not created by the sandbox.

### Distorted Behavior

The getter returns an empty string when reading the `innerText` of a script element that was not created by the sandbox.
<!-- END generated embed, please keep comment -->
