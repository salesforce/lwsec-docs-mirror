# Disallowed CustomElementRegistry Properties (disallowed-custom-element-registry-properties)

For security the following `CustomElementRegistry` properties are disallowed in Lightning Locker:

<!-- START generated embed: @locker/distortion/src/CustomElementRegistry/docs/define-value.md -->
## CustomElementRegistry.prototype.define

The [`define`](https://developer.mozilla.org/en-US/docs/Web/API/CustomElementRegistry/define) method of the `CustomElementRegistry` interface defines a new custom element.

Lightning Web Security doesn't allow defining custom elements because the registry is global to the page. You can't register custom elements in the sandbox.
### Distorted Behavior

This distortion prevents invoking `define` method from `CustomElementRegistry` and displays an error.
<!-- END generated embed, please keep comment -->

