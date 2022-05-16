# Distorted TrustedTypePolicyFactory.prototype.createPolicy (distorted-trusted-type-policy-factory-create-policy)

For security `TrustedTypePolicyFactory.prototype.createPolicy` is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/TrustedTypePolicyFactory/docs/createPolicy-value.md -->
## TrustedTypePolicyFactory.createPolicy

The [`TrustedTypePolicyFactory.prototype.createPolicy()`](https://developer.mozilla.org/en-US/docs/Web/API/TrustedTypePolicyFactory/createPolicy) method of the `TrustedTypePolicyFactory` interface creates a `TrustedTypePolicy` object that implements the rules passed as `policyOptions`. 

In Chrome a policy with a name of `'default'` creates a special policy that will be used if a string, rather than a Trusted Type object, is passed to an injection sink. This can be used in a transitional phase while moving from an application that inserted strings into injection sinks.

Malicious code can overwrite the default policy, and pass its own code into an injection sink.

Lightning Web Security prevents setting the `policyName` to the `'default'` value.

### Distorted Behavior

This distortion prevents setting the `policyName` to the `'default'` value.

On a site where Trusted Types are enforced via a Content Security Policy with the [require-trusted-types-for](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/require-trusted-types-for) directive set to `script`, injection even of trusted types won't work in Chrome.
<!-- END generated embed, please keep comment -->
