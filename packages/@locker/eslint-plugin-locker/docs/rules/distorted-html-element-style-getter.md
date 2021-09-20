# Distorted HTMLElement#style Getter (distorted-html-element-style-getter)

For security the `HTMLElement#style` getter is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/HTMLElement/docs/style-getter.md -->
## get: HTMLElement.prototype.style [Chrome, Edge, Opera, Safari]

### Summary

The `style` property on any HTMLElement object allows manipulating CSS styles via JavaScript via assignments (e.g. `element.style.color = 'red'`). Any property set on this object will reflect in the DOM via the `style` attribute on an element, making this object "magical" because of this behavior.

### Distorted Behavior

This distortion alters the getter of the style property for any HTMLElement. The `style` object is being marked as live such that
any properties changed from within the sandbox are reflected on the DOM.

Furthermore, this distortion does not cover a possible but highly improbable scenario: code passing the style object from system mode to the sandbox via function arguments. The distortion will not apply since the getter has been invoked in system mode. The resulting effect is that sandboxed code will not see changes to `style` being reflected in the DOM. If this scenario does happen then the distortion should be upgraded to a patch on the raw `HTMLElement.prototype` in native window.
<!-- END generated embed please keep comment here to allow auto update -->
