# Distorted CustomElementRegistry Properties (distorted-custom-element-registry-properties)

For security the following `CustomElementRegistry` properties are distorted in Lightning Locker:

<!-- START generated embed: @locker/distortion/src/CustomElementRegistry/docs/define-value.md -->
## CustomElementRegistry.prototype.define

### Summary
The ['define()'](https://developer.mozilla.org/en-US/docs/Web/API/CustomElementRegistry/define) method of the CustomElementRegistry interface defines a new custom element. Lightning Web Security does not allow Custom Elements.

### Distorted Behavior

This distortion prevents accessing `define()` from CustomElementRegistry. An error is thrown when accessing this method.
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/CustomElementRegistry/docs/get-value.md -->
## value: CustomElementRegistry.prototype.get

### Goal

 - To prevent sandboxed code to access custom elements constructors from the global registry unless they are obeying their own namespace.

### Design

- Patch value on `CustomElementRegistry.prototype.get` descriptor to prevent accessing a custom element with the wrong prefix. This prevent them from accessing a constructor that they should not have access to.

### Distorted behavior

- Each time define method is called with the wrong prefix, it throws a `RangeError`.
<!-- END generated embed, please keep comment -->
