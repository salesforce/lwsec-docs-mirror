# Disallowed CustomElementRegistry Properties (disallowed-custom-element-registry-properties)

For security the following `CustomElementRegistry` properties are disallowed by Lightning Web Security:

<!-- START generated embed: @locker/distortion/src/CustomElementRegistry/docs/define-value.md -->
## CustomElementRegistry.prototype.define

The [`define`](https://developer.mozilla.org/en-US/docs/Web/API/CustomElementRegistry/define) method of the `CustomElementRegistry` interface defines a new custom element.

Lightning Web Security controls the definition of custom elements by virtualizing the registry per sandbox to prevent usage of custom elements defined by system mode or others namespaces.

### Distorted Behavior

Custom Elements defined by the sandbox will only conflict with custom elements of the same tag name defined by another sandbox or by the system if the definition has a differing value for the static class property `formAssociated`.
<!-- END generated embed, please keep comment -->

