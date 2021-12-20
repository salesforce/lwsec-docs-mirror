# Distorted CustomElementRegistry Properties (distorted-custom-element-registry-properties)

For security the following `CustomElementRegistry` properties are distorted in Lightning Locker:

<!-- START generated embed: @locker/distortion/src/CustomElementRegistry/docs/define-value.md -->
## CustomElementRegistry.prototype.define

### Summary
The ['define'](https://developer.mozilla.org/en-US/docs/Web/API/CustomElementRegistry/define) method of the `CustomElementRegistry` interface defines a new custom element. Lightning Web Security does not allow Custom Elements.

### Distorted Behavior

This distortion prevents invoking `define` method from CustomElementRegistry. An error is thrown when invoking this method.
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/CustomElementRegistry/docs/get-value.md -->
## value: CustomElementRegistry.prototype.get

### Summary
The [`get`](https://developer.mozilla.org/en-US/docs/Web/API/CustomElementRegistry/get) method of `CustomElementRegistry` interface returns the constructor for a previously-defined custom element. Lightning Web Security prevents sandboxed code to access custom elements constructors from the global registry unless they are obeying their own namespace.

### Distorted behavior
When called with the wrong prefix, the `get` method returns `undefined`.
<!-- END generated embed, please keep comment -->
