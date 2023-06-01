# Distorted URL.createObjectURL (distorted-url-create-object-url)

For security `URL.createObjectURL` is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/URL/docs/createObjectURL-value.md -->
## URL.createObjectURL

The [`URL.createObjectURL()`](https://developer.mozilla.org/en-US/docs/Web/API/URL/createObjectURL) static method creates a `DOMString` containing a URL representing the object given in the parameter.

The method creates in memory a URL address location that HTML elements with `src` or `href` attributes can use to load stored content. The URL runs on the same domain as the code that loads it.

Malicious code can use `URL.createObjectURL` to create an object of type File or Blob that uses a MIME type that can load malicious JavaScript code.

MIME types of concern include `text/html`, `image/svg+xml`, `text/xml` and `text/javascript`. The first three have valid use cases, but `text/javascript` doesn't since you can load a JavaScript file using the `<script>` tag instead.

Here's a simple example of malicious code:

```javascript
const blob = new Blob([
    '<script type="text/javascript">alert(document.cookie)</script>',
    { type: 'text/html' },
]);
const url = URL.createObjectURL(blob);
const iframe = document.createElement('iframe');
iframe.src = url;
document.body.append(iframe);
```

Without protection from Lightning Web Security, upon loading the content of the `iframe`, the browser runs the code in the `<script>` tag which bypasses the sandbox. If the code is running on the same domain, it gains access to all cookies and displays them in a popup window.

To guard against exploits, Lightning Web Security fetches the content of the URL and scans `Blob` and `File` objects that have their MIME type set to `text/html`, `image/svg+xml` or `text/xml`. If malicious content is detected, the code doesn't execute.

### Distorted Behavior

This distortion throws an exception when MIME types `text/html`, `text/xml`, `image/svg+xml` are used with `Blob` or `File` objects that try to load malicious content: `Lightning Web Security: Cannot 'createObjectURL' using an unsecure [object Blob]!`

If no malicious content is detected when these MIME types are used, the content is allowed to load but the distortion enforces `charset=utf-8` to prevent exploits where the browser auto-interprets charset and special characters that can lead to XSS.

For any unsupported MIME types, including `text/javascript`, the distortion throws an exception with the message `Lightning Web Security: Unsupported MIME type.`

Empty MIME types on `File` and `Blob` objects are treated as `text/plain` since browsers treat this differently.

All commonly used and non-malicious MIME types work as expected.
<!-- END generated embed, please keep comment -->
