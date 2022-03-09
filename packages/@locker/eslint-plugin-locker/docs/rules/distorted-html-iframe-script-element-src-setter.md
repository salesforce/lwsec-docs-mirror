# Distorted HTML{IFrame|Script}Element#src Setter (distorted-html-iframe-script-element-src-setter)

For security the `HTML{IFrame|Script}Element#src` setter is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/HTMLIFrameElement/docs/src-setter.md -->
## HTMLIFrameElement.prototype.src setter

The [`HTMLIFrameElement.prototype.src`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLIFrameElement/src) property reflects the HTML `referrerpolicy` attribute of the `<iframe>` element defining which referrer is sent when fetching the resource. The `src` value is a string that reflects the `src` HTML attribute, containing the address of the content to be embedded.

Lightning Web Security sanitizes the `src` value and only permits `http://` and `https://` schemes. URL schemes like `javascript://` aren't allowed.

### Distorted Behavior

This distortion logs a console warning for `HTMLIFrameElement.src` values that don't sanitize to `http://` or `https://` schemes.
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/HTMLScriptElement/docs/src-setter.md -->
## HTMLScriptElement.prototype.src setter

[`HTMLScriptElement.prototype.src`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLScriptElement) property is a `DOMString` representing the URL of an external script. It reflects the `src` attribute of the `script` element specifying the URL to an external script.

To ensure that JavaScript code loaded through a `script` element runs in the sandbox, Lightning Web Security evaluates the source text in the same sandbox before the browser evaluates it. This prevents the native behavior of the `script` element from triggering.

LWS stores the value of `src` in a different attribute `data-distorted-src`. LWS fetches the script file using an XHR request and sets the `src` attribute value to a distorted value that uses the script fetched by LWS. The browser reads the distorted value of the `src` attribute which kicks off the evaluation process in the sandbox.

These steps ensure that different browsers work as expected, while preventing them from running script source before LWS can evaluate it.
### Distorted Behavior

This distortion prevents a script from running before LWS can evaluate it.
<!-- END generated embed, please keep comment -->
