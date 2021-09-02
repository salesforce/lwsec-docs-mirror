# Distorted CustomElementRegistry Properties (distorted-custom-element-registry-properties)

For security the following `CustomElementRegistry` properties are distorted in Lightning Locker:

<!-- START generated embed: @locker/distortion/src/CustomElementRegistry/docs/define-value.md -->
## value: CustomElementRegistry.prototype.define

### Goal

 - To prevent sandboxed code to define new custom elements in the global registry unless they are obeying their own namespace.

### Design

- Patch value on `CustomElementRegistry.prototype.define` descriptor to prevent defining a new custom element with the wrong prefix. This prevent them from claiming a custom element name that might affect other sandboxes or the app itself.

### Distorted behavior

- Each time define method is called with the wrong prefix, it throws a `RangeError`.
<!-- END generated embed please keep comment here to allow auto update -->

<!-- START generated embed: @locker/distortion/src/CustomElementRegistry/docs/get-value.md -->
## value: CustomElementRegistry.prototype.get

### Goal

 - To prevent sandboxed code to access custom elements constructors from the global registry unless they are obeying their own namespace.

### Design

- Patch value on `CustomElementRegistry.prototype.get` descriptor to prevent accessing a custom element with the wrong prefix. This prevent them from accessing a constructor that they should not have access to.

### Distorted behavior

- Each time define method is called with the wrong prefix, it throws a `RangeError`.
<!-- END generated embed please keep comment here to allow auto update -->
