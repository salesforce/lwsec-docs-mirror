# Distorted HTMLLinkElement#relList Setter (distorted-html-link-element-rel-list-setter)

For security the `HTMLLinkElement#relList` setter is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/HTMLLinkElement/docs/relList-setter.md -->
## HTMLLinkElement.prototype.relList setter

The [`HTMLLinkElement.relList`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLLinkElement/relList) read-only property reflects the `rel` attribute. It is a live `DOMTokenList` containing the set of link types indicating the relationship between the resource represented by the `<link>` element and the current document. The property itself is read-only, meaning you can substitute the `DOMTokenList` by another one, but the content of the returned list can't be changed.

Malicious code can set `rel` to the value `import`, which allows it to import script resources that can bypass Lightning Web Security distortions and access the raw window.

To reduce the possibility of exploit, Lightning Web Security prevents setting the `import` value to the `rel` property of link elements.


### Distorted Behavior

This distortion prevents code from setting the `relList` property value to `import`.
<!-- END generated embed, please keep comment -->
