# Distorted URL.createObjectURL (distorted-url-create-object-url)

For security `URL.createObjectURL` is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/URL/docs/createObjectURL-value.md -->
## value: URL.createObjectURL

Multiple security vulnerabilities have been reported around URL.createObjectURL. In all situations, the malicious code was creating either a File or a Blob object using a MIME type that would trigger the JIT and attempting to load malicious javascript code. These MIME types include `text/html`, `image/svg+xml`, `text/html` and `text/javascript`. While the first 3 may have valid use cases in a modern application, the latter does not since one can always load a javascript file using the `<script>` tag. 

`URL.createObjectURL` is used to create in memory URL address locations that certain tags can use on their `src` and `href` attributes to load stored content. These URLs run on the same domain as the code that is loading them. Cases where an attacker could load custom code and trigger the JIT include `iframe` and `script` tags, but other creative ways can always be found since these are not the only tags that load remote content. 

Simple example of malicious code:

```javascript
const blob = new Blob([
    '<script type="text/javascript">alert(document.cookie)</script>',
    { type: 'text/html' },
]);
const url = URL.createObjectURL(blob);
const iframe = document.createElement('iframe');
iframe.src = url;
document.body.appendChild(iframe);
```

Upon loading the content of the iframe the browser will see the script tag and run its code. At that point code will bypass the sandbox and, if it's running on the same domain, it will gain access to all cookies. Possibilities are endless here.

Trying to patch all tags and prevent `blob:` URLs is not feasible as the vulnerability does not lie in what type of URLs are supported but the content referenced by them. Reading the content of a `blob:` URL is also quite a challenge since the data is stored in memory in binary format. 

There are ways to read the content of a Blob/File object but they are asynchronous. One such API is the `FileReader` interface. While this may be feasible and elegant in async operations unfortunately `URL.createObjectURL` is a synchronous API therefore this distortion needs to deal with even tougher limitations.

### Goal

- To scan and detect malicious content in Blob/File objects that have their MIME type set to `text/html`, `image/svg+xml` or `text/html`.
- To allow other MIME types which do not trigger the JIT to be used.
- Performance should not be impacted on non-dangerous MIME types.

### Design

- Patch the `URL.createObjectURL` API to scan Blob/File objects that use a potentially dangerous MIME type for dangerous code.
- Use `DOMPurify` to detect whether content is dangerous in the original payload and deny the usage of the specific Blob/File object with `URL.createObjectURL`, if so
- passthrough of any Blob/File/MediaSource objects that use safe MIME types
- For MIME types with `text/html`, `text/xml`, `image/svg+xml` we enforce `charset=utf-8`, i.e. the mime type of the blob becomes `text/html;charset=utf-8`
- To avoid the async-sync issue with this particular API we use a deprecated behavior of `XMLHttpRequest` that allows us to make synchronous XHR requests to a URL. We create an in memory `blob:` URL with the initial content, fetch it synchronously and then scan it using `DOMPurify`. If any content has been removed by `DOMPurify` we mark the content as dangerous. Although marked as deprecated, this API will surely be kept in future browser versions as there is no alternative yet to fetching remote content synchronously. Removing this feature will surely break other web applications thus the risk is quite minimal.

### Distorted behavior

- For any HTML like MIME types used with Blob/File objects that try to load malicious content, the API will throw the error `Locker: Cannot "createObjectURL" using a unsecure [object Blob]!`
- For any non-recognized MIME types the API will throw the error `Unsupported MIME type.`
- All commonly used and non-malicious MIME types will not be affected.
- All Blob/Files using html like MIME types which do not represent a threat will be allowed.
- On HTML like MIME types we enforce charset=utf-8 to prevent exploits where browser auto interprets charset and special characters that can lead to XSS.
<!-- END generated embed please keep comment here to allow auto update -->
