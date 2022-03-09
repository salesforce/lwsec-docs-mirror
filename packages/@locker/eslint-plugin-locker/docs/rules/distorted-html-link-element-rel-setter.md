# Distorted HTMLLinkElement#rel Setter (distorted-html-link-element-rel-setter)

For security the `HTMLLinkElement#rel` setter is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/HTMLLinkElement/docs/rel-setter.md -->
## HTMLLinkElement.prototype.rel setter

The [`HTMLLinkElement.rel`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLLinkElement/rel) property is a `DOMString` containing a space-separated list of link types indicating the relationship between the resource represented by the `<link>` element and the current document.

Malicious code can set `rel` to the value `import`, which allows it to import script resources that can bypass Lightning Web Security distortions and access the raw window.

To reduce the possibility of exploit, Lightning Web Security prevents setting the `import` value to the `rel` property of link elements.

### Distorted Behavior

This distortion prevents code from setting the `rel` property value to `import`.
<!-- END generated embed, please keep comment -->
