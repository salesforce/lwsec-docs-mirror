# Distorted Element|ShadowRoot#setHTMLUnsafe (distorted-element-sethtmlunsafe)

For security the `Element|ShadowRoot#setHTMLUnsafe` is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/Element/docs/setHTMLunsafe-value.md -->
## Element.prototype.setHTMLUnsafe

The [`Element.prototype.setHTMLUnsafe()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/setHTMLUnsafe) method is used to parse a string of HTML into a `DocumentFragment`, which then replaces the element's subtree in the DOM. The input HTML may include declarative shadow roots. It should be used instead of `Element.innerHTML` for inserting untrusted strings of HTML into an element.

### Distorted Behavior

This distortion sanitizes the string provided to `Element.prototype.setHTMLUnsafe()`.
<!-- END generated embed, please keep comment -->
