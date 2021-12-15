# Distorted Element#shadowRoot Getter (distorted-element-shadow-root-getter)

For security the `Element#shadowRoot` getter is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Element/docs/shadowRoot-getter.md -->
## get: Element.prototype.shadowRoot [Main]

### Summary

This property allows retrieving the shadow DOM of custom elements created with `attachShadow({mode: 'open'})`.
Although in the sandbox elements cannot be created with this mode (see attachShadow distortion) other entities (framework code running in system mode) may create custom elements in this mode. This makes it particular dangerous for elements that get passed around as function arguments or are being queried from the DOM (both light or shadow). 

### Distorted Behavior

This distortion will return `null` when trying to access the `shadowRoot` property on a light-dom element.
<!-- END generated embed please keep comment here to allow auto update -->
