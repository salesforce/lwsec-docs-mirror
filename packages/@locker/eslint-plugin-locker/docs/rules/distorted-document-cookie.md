# Distorted document.cookie (distorted-document-cookie)

For security the `document.cookie` getter and setter are distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Document/docs/cookie-getter.md -->
## Document.prototype.cookie getter

The [`Document.cookie`](https://developer.mozilla.org/en-US/docs/Web/API/Document/cookie) property lets you read and write cookies associated with the document. It serves as a getter and setter for the actual values of the cookies.

Protecting access to cookies is crucial. If malicious code can access all cookies on a page, it can issue XHR requests impersonating the user who's logged in. This can have catastrophic effects in a multi-tenant environment like Salesforce.

This distortion protects the getter of `Document.prototype.cookie` and limits the view to what is being set from within the sandbox. Cookies inside the sandbox are protected from code outside or in other sandboxes.

### Distorted Behavior

The getter returns only cookies that belong to the sandbox.
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/Document/docs/cookie-setter.md -->
## Document.prototype.cookie setter

The [`Document.cookie`](https://developer.mozilla.org/en-US/docs/Web/API/Document/cookie) property lets you read and write cookies associated with the document. It serves as a getter and setter for the actual values of the cookies.

The setter for `Document.prototype.cookie` is distorted so the getter can retrieve sandbox cookies. Additionally, the distortion prevents changes to critical system cookies that are necessary for Salesforce to function properly. If code in a sandbox is allowed to set system cookies, it can send malicious payloads to the backend using cookies.

### Distorted Behavior

The setter can modify only cookies that belong to the sandbox.
<!-- END generated embed, please keep comment -->
