# Distorted CookieStore Properties (distorted-cookie-store-properties)

For security the following `CookieStore` properties are distorted in Lightning Locker:

<!-- START generated embed: @locker/distortion/src/CookieStore/docs/delete-value.md -->
## CookieStore.prototype.delete getter

The [`delete()`](https://developer.mozilla.org/en-US/docs/Web/API/CookieStore/delete) method of the `CookieStore` interface deletes a cookie with the given name or options object.

If malicious code deletes cookies on a page, it could remove login cookies and make the app unusable. This distortion protects cookies outside the sandbox from `CookieStore.prototype.delete` and limits what can be deleted within the sandbox. Cookies in the sandbox are protected from code outside or in other sandboxes.

### Distorted Behavior

The distortion only permits deletion of sandbox cookies.
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/CookieStore/docs/get-value.md -->
## CookieStore.prototype.get getter

The [`get()`](https://developer.mozilla.org/en-US/docs/Web/API/CookieStore/get) method of the `CookieStore` interface returns a single cookie with the given name or options object.

If malicious code can access any cookie on a page, it can issue XHR requests impersonating the user who's logged in. This behavior can have catastrophic effects in a multi-tenant environment like Salesforce. 

This distortion protects the value of `CookieStore.prototype.get` and limits the view to what is being retrieved from within the sandbox. Cookies in the sandbox are protected from code outside or in other sandboxes.

### Distorted Behavior

The `get()` method returns only sandbox cookies.
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/CookieStore/docs/getAll-value.md -->
## CookieStore.prototype.getAll getter

The [`getAll()`](https://developer.mozilla.org/en-US/docs/Web/API/CookieStore/getAll) method of the `CookieStore` interface returns a list of cookies that match the name or options passed to it. Passing no parameters will return all cookies for the current context.

If malicious code can access all cookies on a page, it can issue XHR requests impersonating the user who's logged in. This behavior can have catastrophic effects in a multi-tenant environment like Salesforce. 

This distortion protects the value of `CookieStore.prototype.getAll` and limits the view to what is being retrieved from within the sandbox. Cookies in the sandbox are protected from code outside or in other sandboxes.

### Distorted Behavior

The `getAll()` method returns only sandbox cookies.
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/CookieStore/docs/set-value.md -->
## CookieStore.prototype.set setter

The [`set()`](https://developer.mozilla.org/en-US/docs/Web/API/CookieStore/set) method of the `CookieStore` interface sets a cookie with the given name and value or options object.

Distortion of `CookieStore.prototype.set` is required so `CookieStore.prototype.get` can retrieve sandbox cookies that are similarly distorted with the sandbox prefix. 

This distortion also prevents malicious code from accessing system cookies that Salesforce uses to function. Otherwise any sandbox can send malicious payloads to the backend using cookies.

### Distorted Behavior

The `set()` method automatically adds the sandbox prefix to keys for sandbox cookies.
<!-- END generated embed, please keep comment -->
