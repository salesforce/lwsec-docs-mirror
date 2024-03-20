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
## Document.prototype.domain setter

The deprecated [`Document.domain`](https://developer.mozilla.org/en-US/docs/Web/API/Document/domain) property gets/sets the domain portion of the origin of the current document, as used by the same-origin policy.

According to [W3C](https://www.w3.org/TR/DOM-Level-2-HTML/html.html#ID-2250147) the `Document.domain` property should be read-only.

Firefox doesn't allow setting this property and throws a SecurityError, but Chrome, Safari, and Edge (Webkit) allow it. In those browsers, the property can't be set to a random value, it must match the suffix of the initial domain. So if the initial value is `my.domain.com` the domain value that can be set is `domain.com` because that is the suffix.

The distortion doesn't allow code in a sandbox to change the domain of the root document even if the browser allows it.
### Distorted Behavior

On Firefox the distortion throws an exception instead of SecurityError.

On Chrome, Safari and Edge (Webkit) it throws an exception instead of allowing the setter to execute.
<!-- END generated embed, please keep comment -->
