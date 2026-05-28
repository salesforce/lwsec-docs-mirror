# Distorted SVGAnimatedString.prototype.baseVal (distorted-svg-animated-string-base-val)

For security `SVGAnimatedString.prototype.baseVal` is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/SVGAnimatedString/docs/baseVal-setter.md -->
## SVGAnimatedString.prototype.baseVal setter

The [`SVGAnimatedString.prototype.baseVal`](https://developer.mozilla.org/en-US/docs/Web/API/SVGAnimatedString/baseVal) property is the writable string value of an SVG animated attribute.

This distortion ensures that scripts loaded via SVG `<script>` elements are evaluated in the sandbox.

### Distorted Behavior

When `baseVal` is set on an `SVGAnimatedString` that belongs to an `SVGScriptElement`'s `href` property, the script is evaluated in the sandbox.
<!-- END generated embed, please keep comment -->
