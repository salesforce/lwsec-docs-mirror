# Distorted CustomElementRegistry Properties (distorted-custom-element-registry-properties)

For security the following `CustomElementRegistry` properties are distorted in Lightning Locker:

<!-- START generated embed: @locker/distortion/src/CustomElementRegistry/docs/define-value.md -->
## CustomElementRegistry.prototype.define

The [`define()`](https://developer.mozilla.org/en-US/docs/Web/API/CustomElementRegistry/define) method of the `CustomElementRegistry` interface defines a new custom element. 

Lightning Web Security doesn't allow defining custom elements because the registry is global to the page. You can't register custom elements in the sandbox. 
### Distorted Behavior

This distortion prevents invoking `define` method from `CustomElementRegistry` and displays an error.
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/CustomElementRegistry/docs/get-value.md -->
## CustomElementRegistry.prototype.get

The [`get`](https://developer.mozilla.org/en-US/docs/Web/API/CustomElementRegistry/get) method of `CustomElementRegistry` interface returns the constructor for a previously-defined custom element. 

Lightning Web Security allows sandboxed code to access existing custom element constructors from the global registry only if the custom element is prefixed with the same namespace. 

### Distorted Behavior

When called with the wrong prefix, the `get` method returns `undefined`.
<!-- END generated embed, please keep comment -->
