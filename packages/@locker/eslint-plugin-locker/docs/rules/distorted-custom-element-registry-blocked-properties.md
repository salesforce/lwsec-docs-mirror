# Disallowed CustomElementRegistry Properties (disallowed-custom-element-registry-properties)

For security the following `CustomElementRegistry` properties are disallowed in Lightning Locker:

<!-- START generated embed: @locker/distortion/src/CustomElementRegistry/docs/define-value.md -->
## CustomElementRegistry.prototype.define

### Summary
The ['define()'](https://developer.mozilla.org/en-US/docs/Web/API/CustomElementRegistry/define) method of the CustomElementRegistry interface defines a new custom element. Lightning Web Security does not allow Custom Elements.

### Distorted Behavior

This distortion prevents accessing `define()` from CustomElementRegistry. An error is thrown when accessing this method.
<!-- END generated embed please keep comment here to allow auto update -->

