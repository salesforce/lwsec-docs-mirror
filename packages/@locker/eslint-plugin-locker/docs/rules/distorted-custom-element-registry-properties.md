# Distorted CustomElementRegistry Properties (distorted-custom-element-registry-properties)

For security the following `CustomElementRegistry` properties are distorted by Lightning Web Security:

<!-- START generated embed: @locker/distortion/src/CustomElementRegistry/docs/define-value.md -->
## CustomElementRegistry.prototype.define

The [`define`](https://developer.mozilla.org/en-US/docs/Web/API/CustomElementRegistry/define) method of the `CustomElementRegistry` interface defines a new custom element.

Lightning Web Security controls the definition of custom elements by virtualizing the registry per sandbox to prevent usage of custom elements defined by system mode or others namespaces.

### Distorted Behavior

Custom Elements defined by the sandbox will never conflict with custom elements with the same name defined by another sandbox or by the system.
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/CustomElementRegistry/docs/get-value.md -->
## CustomElementRegistry.prototype.get

The [`get`](https://developer.mozilla.org/en-US/docs/Web/API/CustomElementRegistry/get) method of `CustomElementRegistry` interface returns the constructor for a previously-defined custom element.

Lightning Web Security controls the access to defined custom elements by virtualizing the registry per sandbox to prevent usage of custom elements defined by system mode or others namespaces.

### Distorted Behavior

The sandbox can only get Custom Elements defined by the sandbox itself for a given name. It will prevent access to conflict with custom elements with the same name defined by another sandbox or by the system.
<!-- END generated embed, please keep comment -->
