# Distorted Navigator#serviceWorker Getter (distorted-navigator-service-worker-getter)

For security the `Navigator#serviceWorker` getter is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Navigator/docs/serviceWorker-getter.md -->
## get: Navigator.prototype.serviceWorker

### Problem statement

With `ServiceWorker`, it is possible to alter the response of a request to return JavaScript code that would be unsandboxed when evaluated by the browser.

**Example:**
```js
navigator.serviceWorker.register('/static/sw.js').then(() => {
    window.open('/static/aaa', '_self');
});
```

**File /static/sw.js:**
```js
self.addEventListener('fetch', (event) => {
    const unsandboxed = '<body><script>document.body.innerHTML=document.cookie;</script>';
    event.respondWith(new Response(unsandboxed, { headers: { 'Content-Type': 'text/html' } }));
});
```

### Goal

To prevent unsandboxed JavaScript code from leaking data, we want to disallow access to the `navigator.serviceWorker` property.

### Design

Patch getter on `Navigator.prototype.serviceWorker` descriptor to return `undefined`.

### Distorted behavior

Each time code accesses `navigator.serviceWorker` property, this distortion will return `undefined`.
<!-- END generated embed please keep comment here to allow auto update -->

<!-- START generated embed: @locker/distortion/src/ServiceWorkerContainer/docs/prototype-value.md -->
## value: ServiceWorkerContainer.prototype

### Problem Statement

With `ServiceWorker`, it is possible to alter the response of a request to return JavaScript code that would be unsandboxed when evaluated by the browser.

**Example:**
```js
navigator.serviceWorker.register('/static/sw.js').then(() => {
    window.open('/static/aaa', '_self');
});
```

**File /static/sw.js:**
```js
self.addEventListener('fetch', (event) => {
    const unsandboxed = '<body><script>document.body.innerHTML=document.cookie;</script>';
    event.respondWith(new Response(unsandboxed, { headers: { 'Content-Type': 'text/html' } }));
});
```

### Goal

To prevent unsandboxed JavaScript code from leaking data, we want to disallow access to any of the `ServiceWorkerContainer.prototype` properties or methods. We do this because even though we already prevent access to `navigator.serviceWorker`, there are other ways in which user code could get access to the `ServiceWorkerContainer` singleton, so this distortion prevents access to any of its operations.

### Distorted behavior

This distortion will throw a `TypeError` whenever any of the `ServiceWorkerContainer.prototype` properties or methods is accessed.
<!-- END generated embed please keep comment here to allow auto update -->
