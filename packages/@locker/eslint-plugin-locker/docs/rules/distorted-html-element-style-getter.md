# Distorted HTMLElement#style Getter (distorted-html-element-style-getter)

For security the `HTMLElement#style` getter is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/HTMLElement/docs/style-getter.md -->
## HTMLElement.prototype.style getter [Chrome, Edge, Opera, Safari]

The [`HTMLElement.prototype.style`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) read-only property returns the inline style of an element in the form of a `CSSStyleDeclaration` object that contains a list of all styles properties for that element with values assigned for the attributes that are defined in the element's inline `style` attribute.

The `style` property on any `HTMLElement` object lets you manipulate CSS styles with JavaScript via assignments. For example, you could change an element's text color using `element.style.color = 'red'`. 

A property set on a `HTMLElement` object reflects in the DOM via the `style` attribute on an element, making this object "magical" because of this behavior.

### Distorted Behavior

This distortion alters the getter of the `style` property for any `HTMLElement`. The `style` object is marked as live such that any properties changed from within the sandbox are reflected on the DOM.
<!-- END generated embed, please keep comment -->
