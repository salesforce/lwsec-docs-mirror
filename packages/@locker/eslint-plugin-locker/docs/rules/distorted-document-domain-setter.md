# Prevent setting value of document.domain (distorted-document-domain-setter)

Setting the value of `document.domain` is not allowed. Although behavior varies across browsers, setting `document.domain` to any value when Lightning Web Security is enabled will result in an error being thrown.

See [Related Distortions](#related-distortions) below for more details.

## Rule Details

Example of **incorrect** code:

```js
document.domain = 'example.com';
```

## Related Distortions

<!-- START generated embed: @locker/distortion/src/Document/docs/domain-setter.md -->
## set: Document.prototype.domain

According to [W3C](https://www.w3.org/TR/DOM-Level-2-HTML/html.html#ID-2250147)
this property should be read-only. Firefox does not allow setting it and throws
a SecurityError but Chrome, Safari and Edge (Webkit) allow it. The property cannot
be set to a random value, it has to be a suffix of the initial domain. So if the
initial value is `my.domain.com` the domain value that can be set is `domain.com`
because that is the suffix. The distortion shouldn't allow a sandbox to change the
domain of the root document.

### Goal

- Prevent domain from being changed from within the sandbox on root document.

### Design

- Patch the setter of Document.prototype.domain to throw an error regardless of
the value that's being used.

### Distorted behavior

- On Firefox we will throw an Error instead of SecurityError. On Chrome, Safari
and Edge (Webkit) we will throw an Error instead of allowing the setter to execute.
<!-- END generated embed, please keep comment -->
