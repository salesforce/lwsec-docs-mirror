# Distorted Element.prototype.innerHTML getter (distorted-element-inner-html-getter)

For security the `Element.prototype.innerHTML` getter is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/Element/docs/innerHTML-getter.md -->
## Element.prototype.innerHTML getter

The [`Element.prototype.innerHTML`](https://developer.mozilla.org/en-US/docs/Web/API/Element/innerHTML) property gets or sets the HTML or XML markup contained within the element.

This distortion protects `Element.prototype.innerHTML` and prevents sandboxed code from reading the source of inline scripts that were not created by the sandbox. It also removes CSP nonce values from the serialized HTML string.

### Distorted Behavior

The getter returns an empty string when reading the `innerHTML` of a script element that was not created by the sandbox. For other elements, CSP nonce values are stripped from the returned string.
<!-- END generated embed, please keep comment -->
