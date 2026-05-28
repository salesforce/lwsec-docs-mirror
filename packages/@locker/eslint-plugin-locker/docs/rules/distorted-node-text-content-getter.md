# Distorted Node.prototype.textContent getter (distorted-node-text-content-getter)

For security the `Node.prototype.textContent` getter is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/Node/docs/textContent-getter.md -->
## Node.prototype.textContent getter

The [`Node.prototype.textContent`](https://developer.mozilla.org/en-US/docs/Web/API/Node/textContent) property represents the text content of the node and its descendants.

This distortion protects `Node.prototype.textContent` and prevents sandboxed code from reading the source of inline scripts that were not created by the sandbox.

### Distorted Behavior

The getter returns an empty string when reading the `textContent` of a script element that was not created by the sandbox.
<!-- END generated embed, please keep comment -->
