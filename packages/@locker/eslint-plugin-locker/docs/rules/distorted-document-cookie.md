# Distorted document.cookie (distorted-document-cookie)

For security the `document.cookie` getter and setter are distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Document/docs/cookie-getter.md -->
## get: Document.prototype.cookie

Along access to the global window object, protecting access to cookies is absolutely crucial. If a malicious piece of code would get access to all the cookies on a page it could start issuing XHR requests impersonating the currently logged in user. This can have catastrophic effects in a multi tenant environment like Salesforce. It is absolutely necessary to protect the getter of `Document.prototype.cookie` and limit the view only to what is being set from within the sandbox, nothing from outside or other sandboxes.

### Goal

- To prevent access to cookies not belonging to the sandbox

### Design

- Patch the getter of Document.prototype.cookie to filter out any cookies set from outside the sandbox. This includes system cookies and other sandbox cookies. The current strategy for isolating cookies between sandboxes is to use a prefix for each key that is specific to each sandbox. The filtering of cookies will be done based on this prefix.

### Distorted behavior

- The getter will return only sandbox cookies. The behavior will seem native-like.
<!-- END generated embed please keep comment here to allow auto update -->

<!-- START generated embed: @locker/distortion/src/Document/docs/cookie-setter.md -->
## set: Document.prototype.cookie

Patching the setter of `Document.prototype.cookie` is required in order for the getter to manage to retrieve sandbox cookies. Additionally, we need to make sure that malicious code does not override critical system cookies that are necessary for a system like Salesforce to function properly. If we would not patch the setter then any sandbox would be able to send malicious payloads to the backend using cookies.

### Goal

- To prevent setting cookies that affect global behavior.

### Design

- Patch the setter of Document.prototype.cookie to prefix any cookie keys set from within the sandbox. The prefix is computed based on the namespace of the sandbox. 

### Distorted behavior

- The behavior will seem native like.
<!-- END generated embed please keep comment here to allow auto update -->
