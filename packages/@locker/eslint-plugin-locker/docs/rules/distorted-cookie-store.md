# Distorted CookieStore Properties (distorted-cookie-store-properties)

For security the following `CookieStore` properties are distorted in Lightning Locker:

<!-- START generated embed: @locker/distortion/src/CookieStore/docs/delete-value.md -->
## get: CookieStore.prototype.delete

Protecting cookies outside of the sandbox is crucial. If a malicious piece of code could delete cookies on a page, it could remove login cookies and make the app unrunnable. It is absolutely necessary to protect cookies outside of the sandbox from `CookieStore.prototype.delete` and limit what is allowed to be deleted from within the sandbox, nothing from outside or other sandboxes.

### Goal

- To prevent deleting cookies outside of the sandbox.

### Design

- The current strategy for isolating cookies between sandboxes is to use a prefix for each key that is specific to each sandbox. The filtering of cookies will be done based on this prefix.

### Distorted Behavior

- The delete value will delete only sandbox cookies. The behavior will seem native-like.
<!-- END generated embed please keep comment here to allow auto update -->

<!-- START generated embed: @locker/distortion/src/CookieStore/docs/get-value.md -->
## get: CookieStore.prototype.get

Protecting access to cookies is absolutely crucial. If a malicious piece of code would get access to all the cookies on a page it could start issuing XHR requests impersonating the currently logged in user. This can have catastrophic effects in a multi-tenant environment like Salesforce. It is absolutely necessary to protect the value of `CookieStore.prototype.get` and limit the view only to what is being retrieved from within the sandbox, nothing from outside or other sandboxes.

### Goal

- To prevent access to cookies not belonging to the sandbox.

### Design

- The current strategy for isolating cookies between sandboxes is to use a prefix for each key that is specific to each sandbox. The filtering of cookies will be done based on this prefix.

### Distorted Behavior

- The get value will return only sandbox cookies. The behavior will seem native-like.
<!-- END generated embed please keep comment here to allow auto update -->

<!-- START generated embed: @locker/distortion/src/CookieStore/docs/getAll-value.md -->
## get: CookieStore.prototype.getAll

Protecting access to cookies is absolutely crucial. If a malicious piece of code would get access to all the cookies on a page it could start issuing XHR requests impersonating the currently logged in user. This can have catastrophic effects in a multi-tenant environment like Salesforce. It is absolutely necessary to protect the value of `CookieStore.prototype.getAll` and limit the view only to what is being retrieved from within the sandbox, nothing from outside or other sandboxes.

### Goal

- To prevent access to cookies not belonging to the sandbox.

### Design

- The current strategy for isolating cookies between sandboxes is to use a prefix for each key that is specific to each sandbox. The filtering of cookies will be done based on this prefix.

### Distorted Behavior

- The getAll value will return only sandbox cookies. The behavior will seem native-like.
<!-- END generated embed please keep comment here to allow auto update -->

<!-- START generated embed: @locker/distortion/src/CookieStore/docs/set-value.md -->
## set: CookieStore.prototype.set

Patching the value of `CookieStore.prototype.set` is required in order for the get value to manage to retrieve sandbox cookies. Additionally, we need to make sure that malicious code does not override critical system cookies that are necessary for a system like Salesforce to function properly. If we would not patch the value then any sandbox would be able to send malicious payloads to the backend using cookies.

### Goal

- To prevent setting cookies outside of the sandbox.

### Design

- The current strategy for isolating cookies between sandboxes is to use a prefix for each key that is specific to each sandbox. The filtering of cookies will be done based on this prefix.

### Distorted Behavior

- The set value will prefix keys for sandbox cookies. The behavior will seem native-like.
<!-- END generated embed please keep comment here to allow auto update -->
