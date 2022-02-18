# Distorted Range#createContextualFragment (distorted-range-create-contextual-fragment)

For security `Range#createContextualFragment` is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Range/docs/createContextualFragment-value.md -->
## Range.prototype.createContextualFragment

The `Range` interface represents a fragment of a document that can contain nodes and parts of text nodes.

The [`Range.prototype.createContextualFragment()`](https://developer.mozilla.org/en-US/docs/Web/API/Range/createContextualFragment) method returns a `DocumentFragment` created from a given string of text. The string contains text and HTML tags to be converted to a document fragment.

The `createContextualFragment()` method invokes the HTML fragment parsing algorithm or the XML fragment parsing algorithm with the start of the range (the parent of the selected node) as the context node. The document fragment can be added to the DOM tree.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. The `createContextualFragment()` method can let malicious code insert specified text as HTML into the DOM tree. Although the fragment can only be inserted outside of the shared elements, it can pollute the DOM. LWS sanitizes elements added to the shared DOM.

### Distorted Behavior

This distortion sanitizes an HTML string that is used to create the `DocumentFragment`.
<!-- END generated embed, please keep comment -->
