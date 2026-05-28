# Distorted HTMLScriptElement.prototype.text getter (distorted-html-script-element-text-getter)

For security the `HTMLScriptElement.prototype.text` getter is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/HTMLScriptElement/docs/text-getter.md -->
## HTMLScriptElement.prototype.text getter

The [`HTMLScriptElement.prototype.text`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLScriptElement/text) property is a string that joins and returns the contents of all Text nodes inside the `<script>` element in tree order.

This distortion protects `HTMLScriptElement.prototype.text` and prevents sandboxed code from reading the source of inline scripts that were not created by the sandbox.

### Distorted Behavior

The getter returns an empty string when reading the `text` of a script element that was not created by the sandbox.
<!-- END generated embed, please keep comment -->
