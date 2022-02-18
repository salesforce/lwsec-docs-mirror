# Prevent access to Navigator.serviceWorker and ServiceWorkerContainer properties and methods(distorted-navigator-service-worker-getter)

`Navigator.serviceWorker` returns `undefined` and accessing `ServiceWorkerContainer` properties and methods throws a `TypeError` when Lightning Web Security is enabled.

See [Related Distortions](#related-distortions) below for more details.

## Rule Details

Example of **incorrect** code:

```js
navigator.serviceWorker.controller;
```

## Related Distortions

<!-- START generated embed: @locker/distortion/src/Navigator/docs/serviceWorker-getter.md -->
## Navigator.prototype.serviceWorker getter

The [`Navigator`](https://developer.mozilla.org/en-US/docs/Web/API/Navigator) interface represents the state and the identity of the user agent. It allows scripts to query it and to register themselves to carry on some activities.

The [`Navigator.prototype.serviceWorker`](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/serviceWorker) read-only property returns the `ServiceWorkerContainer` object for the associated document, which provides access to registration, removal, upgrade, and communication with the `ServiceWorker`.

With access to the `serviceWorker` property, malicious code can alter the response of a request to return JavaScript code that's not in a sandbox when evaluated by the browser.

For example:
```js
navigator.serviceWorker.register('/static/sw.js').then(() => {
    window.open('/static/aaa', '_self');
});
```

```js
//  file /static/sw.js
self.addEventListener('fetch', (event) => {
    const unsandboxed = '<body><script>document.body.innerHTML=document.cookie;</script>';
    event.respondWith(new Response(unsandboxed, { headers: { 'Content-Type': 'text/html' } }));
});
```

To prevent JavaScript code from leaking data outside the sandbox, Lightning Web Security disallows access to the `navigator.serviceWorker` property.

### Distorted Behavior

This distortion returns `undefined` when code accesses the `navigator.serviceWorker` property.
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/ServiceWorkerContainer/docs/prototype-value.md -->
## ServiceWorkerContainer.prototype

The [`ServiceWorkerContainer.prototype`](https://developer.mozilla.org/en-US/docs/Web/API/ServiceWorkerContainer) interface of the Service Worker API provides an object representing the service worker as an overall unit in the network ecosystem. `ServiceWorkerContainer` includes facilities to register, unregister, and update service workers, and access the state of service workers and their registrations.

Most importantly, it exposes the `ServiceWorkerContainer.prototype.register()` method used to register service workers, and the `ServiceWorkerContainer.prototype.controller` property used to determine whether the current page is actively controlled.

With access to `ServiceWorkerContainer.prototype` properties or methods, malicious code can alter the response of a request to return JavaScript code that is outside a sandbox when evaluated by the browser.

For example:
```js
navigator.serviceWorker.register('/static/sw.js').then(() => {
    window.open('/static/aaa', '_self');
});
```

```js
// File /static/sw.js
self.addEventListener('fetch', (event) => {
    const unsandboxed = '<body><script>document.body.innerHTML=document.cookie;</script>';
    event.respondWith(new Response(unsandboxed, { headers: { 'Content-Type': 'text/html' } }));
});
```

To prevent JavaScript code from leaking data outside the sandbox, Lightning Web Security disallows access to any of the `ServiceWorkerContainer.prototype` properties or methods.

Although LWS already prevents access to `navigator.serviceWorker`, malicious code can access the `ServiceWorkerContainer` object in other ways, so this distortion prevents access to any of its operations.

### Distorted Behavior

This distortion throws a `TypeError` whenever any of the `ServiceWorkerContainer.prototype` properties or methods is accessed.
<!-- END generated embed, please keep comment -->
