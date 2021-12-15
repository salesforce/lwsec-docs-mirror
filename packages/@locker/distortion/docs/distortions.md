# Locker vNext Distortions

This is the list of the currently implemented Locker vNext distortions.

Version: 0.14.14<br>
Generated: Oct 28, 2021

## Table of Contents

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [set: Attr.prototype.value](#set-attrprototypevalue)
  - [Goal](#goal)
  - [Design](#design)
  - [Distorted behavior](#distorted-behavior)
- [get: CookieStore.prototype.delete](#get-cookiestoreprototypedelete)
  - [Goal](#goal-1)
  - [Design](#design-1)
  - [Distorted Behavior](#distorted-behavior)
- [get: CookieStore.prototype.get](#get-cookiestoreprototypeget)
  - [Goal](#goal-2)
  - [Design](#design-2)
  - [Distorted Behavior](#distorted-behavior-1)
- [get: CookieStore.prototype.getAll](#get-cookiestoreprototypegetall)
  - [Goal](#goal-3)
  - [Design](#design-3)
  - [Distorted Behavior](#distorted-behavior-2)
- [set: CookieStore.prototype.set](#set-cookiestoreprototypeset)
  - [Goal](#goal-4)
  - [Design](#design-4)
  - [Distorted Behavior](#distorted-behavior-3)
- [value: CustomElementRegistry.prototype.define](#value-customelementregistryprototypedefine)
  - [Goal](#goal-5)
  - [Design](#design-5)
  - [Distorted behavior](#distorted-behavior-1)
- [value: CustomElementRegistry.prototype.get](#value-customelementregistryprototypeget)
  - [Goal](#goal-6)
  - [Design](#design-6)
  - [Distorted behavior](#distorted-behavior-2)
- [get: Document.prototype.cookie](#get-documentprototypecookie)
  - [Goal](#goal-7)
  - [Design](#design-7)
  - [Distorted behavior](#distorted-behavior-3)
- [set: Document.prototype.cookie](#set-documentprototypecookie)
  - [Goal](#goal-8)
  - [Design](#design-8)
  - [Distorted behavior](#distorted-behavior-4)
- [set: Document.prototype.domain](#set-documentprototypedomain)
  - [Goal](#goal-9)
  - [Design](#design-9)
  - [Distorted behavior](#distorted-behavior-5)
- [value: Document.prototype.execCommand [Main]](#value-documentprototypeexeccommand-main)
  - [Summary](#summary)
  - [Distorted Behavior](#distorted-behavior-4)
- [set: Element.prototype.attachShadow [Main]](#set-elementprototypeattachshadow-main)
  - [Summary](#summary-1)
  - [Distorted Behavior](#distorted-behavior-5)
- [get: Element.attributes](#get-elementattributes)
  - [Goal](#goal-10)
  - [Design](#design-10)
  - [Distorted behavior](#distorted-behavior-6)
- [Fullscreen API: Element.prototype](#fullscreen-api-elementprototype)
- [set: Element.prototype.innerHTML [Main]](#set-elementprototypeinnerhtml-main)
  - [Summary](#summary-2)
  - [Distorted Behavior](#distorted-behavior-6)
- [set: Element.prototype.insertAdjacentHTML [Main]](#set-elementprototypeinsertadjacenthtml-main)
  - [Summary](#summary-3)
  - [Distorted Behavior](#distorted-behavior-7)
- [set: Element.prototype.outerHTML [Main]](#set-elementprototypeouterhtml-main)
  - [Summary](#summary-4)
  - [Distorted Behavior](#distorted-behavior-8)
- [value: Element.prototype.setAttribute](#value-elementprototypesetattribute)
  - [Goal](#goal-11)
  - [Design](#design-11)
  - [Distorted behavior](#distorted-behavior-7)
- [get: Element.prototype.shadowRoot [Main]](#get-elementprototypeshadowroot-main)
  - [Summary](#summary-5)
  - [Distorted Behavior](#distorted-behavior-9)
- [Event.prototype.composedPath [Main]](#eventprototypecomposedpath-main)
  - [Summary](#summary-6)
  - [Distorted Behavior](#distorted-behavior-10)
- [nonce: HTMLElement.prototype](#nonce-htmlelementprototype)
- [WindowEventHandlers: HTMLElement.prototype](#windoweventhandlers-htmlelementprototype)
- [set: Element.prototype.outerText [Chrome, Edge, Opera, Safari]](#set-elementprototypeoutertext-chrome-edge-opera-safari)
  - [Summary](#summary-7)
  - [Distorted Behavior](#distorted-behavior-11)
- [get: HTMLElement.prototype.style [Chrome, Edge, Opera, Safari]](#get-htmlelementprototypestyle-chrome-edge-opera-safari)
  - [Summary](#summary-8)
  - [Distorted Behavior](#distorted-behavior-12)
- [get: HTMLFrameElement.prototype.contentDocument](#get-htmlframeelementprototypecontentdocument)
  - [Goal](#goal-12)
  - [Design](#design-12)
  - [Distorted behavior](#distorted-behavior-8)
- [get: HTMLFrameElement.prototype.contentWindow](#get-htmlframeelementprototypecontentwindow)
  - [Goal](#goal-13)
  - [Design](#design-13)
  - [Distorted behavior](#distorted-behavior-9)
- [get: HTMLIFrameElement.prototype.contentDocument](#get-htmliframeelementprototypecontentdocument)
  - [Goal](#goal-14)
  - [Design](#design-14)
  - [Distorted behavior](#distorted-behavior-10)
- [get: HTMLIFrameElement.prototype.contentWindow](#get-htmliframeelementprototypecontentwindow)
  - [Goal](#goal-15)
  - [Design](#design-15)
  - [Distorted behavior](#distorted-behavior-11)
- [set: HTMLIFrameElement.prototype.src](#set-htmliframeelementprototypesrc)
  - [Goal](#goal-16)
  - [Design](#design-16)
  - [Distorted behavior](#distorted-behavior-12)
- [get: HTMLObjectElement.prototype.contentDocument](#get-htmlobjectelementprototypecontentdocument)
  - [Goal](#goal-17)
  - [Design](#design-17)
  - [Distorted behavior](#distorted-behavior-13)
- [get: HTMLObjectElement.prototype.contentWindow](#get-htmlobjectelementprototypecontentwindow)
  - [Goal](#goal-18)
  - [Design](#design-18)
  - [Distorted behavior](#distorted-behavior-14)
- [get: HTMLScriptElement.prototype.src](#get-htmlscriptelementprototypesrc)
  - [Goal](#goal-19)
  - [Design](#design-19)
  - [Distorted behavior](#distorted-behavior-15)
- [set: HTMLScriptElement.prototype.src](#set-htmlscriptelementprototypesrc)
  - [Goal](#goal-20)
  - [Design](#design-20)
  - [Distorted behavior](#distorted-behavior-16)
- [get: MessageEvent.prototype.source](#get-messageeventprototypesource)
  - [Goal](#goal-21)
  - [Design](#design-21)
  - [Design](#design-22)
  - [Distorted behavior](#distorted-behavior-17)
- [value: NamedNodeMap.prototype.setNamedItem](#value-namednodemapprototypesetnameditem)
  - [Goal](#goal-22)
  - [Design](#design-23)
  - [Distorted behavior](#distorted-behavior-18)
- [get: Navigator.prototype.serviceWorker](#get-navigatorprototypeserviceworker)
  - [Problem statement](#problem-statement)
  - [Goal](#goal-23)
  - [Design](#design-24)
  - [Distorted behavior](#distorted-behavior-19)
- [set: Node.prototype.textContent [Main]](#set-nodeprototypetextcontent-main)
  - [Summary](#summary-9)
  - [Distorted Behavior](#distorted-behavior-13)
- [value: Range.prototype.createContextualFragment [Main]](#value-rangeprototypecreatecontextualfragment-main)
  - [Summary](#summary-10)
  - [Distorted Behavior](#distorted-behavior-14)
- [href attribute on SVGScriptElement](#href-attribute-on-svgscriptelement)
  - [Summary](#summary-11)
  - [Goal](#goal-24)
  - [Distorted Behavior](#distorted-behavior-15)
  - [Distorted Behavior](#distorted-behavior-16)
- [href attribute and xlink:href attribute on SVGUseElement](#href-attribute-and-xlinkhref-attribute-on-svguseelement)
  - [Summary](#summary-12)
  - [Design](#design-25)
  - [Dependencies](#dependencies)
- [value: ServiceWorkerContainer.prototype](#value-serviceworkercontainerprototype)
  - [Problem Statement](#problem-statement)
  - [Goal](#goal-25)
  - [Distorted behavior](#distorted-behavior-20)
- [get: ShadowRoot.prototype.mode](#get-shadowrootprototypemode)
  - [Goal](#goal-26)
  - [Design](#design-26)
  - [Distorted behavior](#distorted-behavior-21)
- [SharedWorker Global Constructor](#sharedworker-global-constructor)
  - [Summary](#summary-13)
  - [Distorted Behavior](#distorted-behavior-17)
- [value: Storage.prototype.clear [Main]](#value-storageprototypeclear-main)
  - [Summary](#summary-14)
  - [Distorted Behavior](#distorted-behavior-18)
- [Storage API: Storage.prototype](#storage-api-storageprototype)
  - [Summary](#summary-15)
  - [Distorted Behavior](#distorted-behavior-19)
- [value: Storage.prototype.getItem [Main]](#value-storageprototypegetitem-main)
  - [Summary](#summary-16)
  - [Distorted Behavior](#distorted-behavior-20)
- [value: Storage.prototype.key [Main]](#value-storageprototypekey-main)
  - [Summary](#summary-17)
  - [Distorted Behavior](#distorted-behavior-21)
- [get: Storage.prototype.length [Main]](#get-storageprototypelength-main)
  - [Summary](#summary-18)
  - [Distorted Behavior](#distorted-behavior-22)
- [value: Storage.prototype.removeItem [Main]](#value-storageprototyperemoveitem-main)
  - [Summary](#summary-19)
  - [Distorted Behavior](#distorted-behavior-23)
- [value: Storage.prototype.setItem [Main]](#value-storageprototypesetitem-main)
  - [Summary](#summary-20)
  - [Distorted Behavior](#distorted-behavior-24)
- [value: URL.createObjectURL](#value-urlcreateobjecturl)
  - [Goal](#goal-27)
  - [Design](#design-27)
  - [Distorted behavior](#distorted-behavior-22)
- [Window.fetch](#windowfetch)
  - [Goal](#goal-28)
  - [Design](#design-28)
  - [Distorted behavior](#distorted-behavior-23)
  - [Disallowed endpoints](#disallowed-endpoints)
- [get: window.frames [Main]](#get-windowframes-main)
  - [Summary](#summary-21)
  - [Distorted Behavior](#distorted-behavior-25)
- [get: window.length [Main]](#get-windowlength-main)
  - [Summary](#summary-22)
  - [Distorted Behavior](#distorted-behavior-26)
- [value: Window.prototype.open [Main]](#value-windowprototypeopen-main)
  - [Summary](#summary-23)
  - [Distorted Behavior](#distorted-behavior-27)
- [get: window.opener [Main]](#get-windowopener-main)
  - [Summary](#summary-24)
  - [Distorted Behavior](#distorted-behavior-28)
- [get: window.parent [Main]](#get-windowparent-main)
  - [Summary](#summary-25)
  - [Distorted Behavior](#distorted-behavior-29)
- [value: Window.prototype.setInterval [Main]](#value-windowprototypesetinterval-main)
  - [Summary](#summary-26)
  - [Distorted Behavior](#distorted-behavior-30)
- [value: window.setTimeout [Main]](#value-windowsettimeout-main)
  - [Summary](#summary-27)
  - [Distorted Behavior](#distorted-behavior-31)
- [Worker Global Constructor](#worker-global-constructor)
  - [Summary](#summary-28)
  - [Distorted Behavior](#distorted-behavior-32)
- [XMLHttpRequest.open](#xmlhttprequestopen)
  - [Goal](#goal-29)
  - [Design](#design-29)
  - [Distorted behavior](#distorted-behavior-24)
  - [Disallowed endpoints](#disallowed-endpoints-1)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


<a name="attrdocsvalue-settermd"></a>

## set: Attr.prototype.value

This distortion acts as a router to subdistortions. It uses a shared registry to
identify whether there are any distortions registered for a particular attribute
name and invokes them.


This only applies to connected attribute nodes, disconnected nodes are covered
by `setAttributeNode` and `setAttributeNodeNS` distortions.

### Goal

- to prevent the following type of attack
```js
const attr = createAttribute('rel');
const el = createElement('link');
el.setAttributeNode(attr); // bypass setAttributeNode distortion
attr.value = 'import'; // attempt to set blocked value
document.head.appendChild(el); // append to head
```
- to invoke distortions registered for particular attributes

### Design

- use an internal registry to allow anyone to register distortions for specific
attribute name and Element constructor
- the register method places markers on the prototype of elements, the markers
represent index numbers in the registry
- if the setter is called check if the element is connected
    - if the element is connected then look for a distortion in the registry and
    invoke it
- attr node is not connected, proceed without a distortion

### Distorted behavior

- when there is a registered distortion the behavior is strictly dependent of the
distortion's behavior
- native like behavior when no distortions are registered.
<hr>
<a name="cookiestoredocsdelete-valuemd"></a>

## get: CookieStore.prototype.delete

Protecting cookies outside of the sandbox is crucial. If a malicious piece of code could delete cookies on a page, it could remove login cookies and make the app unrunnable. It is absolutely necessary to protect cookies outside of the sandbox from `CookieStore.prototype.delete` and limit what is allowed to be deleted from within the sandbox, nothing from outside or other sandboxes.

### Goal

- To prevent deleting cookies outside of the sandbox.

### Design

- The current strategy for isolating cookies between sandboxes is to use a prefix for each key that is specific to each sandbox. The filtering of cookies will be done based on this prefix.

### Distorted Behavior

- The delete value will delete only sandbox cookies. The behavior will seem native-like.

<hr>
<a name="cookiestoredocsget-valuemd"></a>

## get: CookieStore.prototype.get

Protecting access to cookies is absolutely crucial. If a malicious piece of code would get access to all the cookies on a page it could start issuing XHR requests impersonating the currently logged in user. This can have catastrophic effects in a multi-tenant environment like Salesforce. It is absolutely necessary to protect the value of `CookieStore.prototype.get` and limit the view only to what is being retrieved from within the sandbox, nothing from outside or other sandboxes.

### Goal

- To prevent access to cookies not belonging to the sandbox.

### Design

- The current strategy for isolating cookies between sandboxes is to use a prefix for each key that is specific to each sandbox. The filtering of cookies will be done based on this prefix.

### Distorted Behavior

- The get value will return only sandbox cookies. The behavior will seem native-like.

<hr>
<a name="cookiestoredocsgetall-valuemd"></a>

## get: CookieStore.prototype.getAll

Protecting access to cookies is absolutely crucial. If a malicious piece of code would get access to all the cookies on a page it could start issuing XHR requests impersonating the currently logged in user. This can have catastrophic effects in a multi-tenant environment like Salesforce. It is absolutely necessary to protect the value of `CookieStore.prototype.getAll` and limit the view only to what is being retrieved from within the sandbox, nothing from outside or other sandboxes.

### Goal

- To prevent access to cookies not belonging to the sandbox.

### Design

- The current strategy for isolating cookies between sandboxes is to use a prefix for each key that is specific to each sandbox. The filtering of cookies will be done based on this prefix.

### Distorted Behavior

- The getAll value will return only sandbox cookies. The behavior will seem native-like.
<hr>
<a name="cookiestoredocsset-valuemd"></a>

## set: CookieStore.prototype.set

Patching the value of `CookieStore.prototype.set` is required in order for the get value to manage to retrieve sandbox cookies. Additionally, we need to make sure that malicious code does not override critical system cookies that are necessary for a system like Salesforce to function properly. If we would not patch the value then any sandbox would be able to send malicious payloads to the backend using cookies.

### Goal

- To prevent setting cookies outside of the sandbox.

### Design

- The current strategy for isolating cookies between sandboxes is to use a prefix for each key that is specific to each sandbox. The filtering of cookies will be done based on this prefix.

### Distorted Behavior

- The set value will prefix keys for sandbox cookies. The behavior will seem native-like.
<hr>
<a name="customelementregistrydocsdefine-valuemd"></a>

## value: CustomElementRegistry.prototype.define

### Goal

 - To prevent sandboxed code to define new custom elements in the global registry unless they are obeying their own namespace.

### Design

- Patch value on `CustomElementRegistry.prototype.define` descriptor to prevent defining a new custom element with the wrong prefix. This prevent them from claiming a custom element name that might affect other sandboxes or the app itself.

### Distorted behavior

- Each time define method is called with the wrong prefix, it throws a `RangeError`.
<hr>
<a name="customelementregistrydocsget-valuemd"></a>

## value: CustomElementRegistry.prototype.get

### Goal

 - To prevent sandboxed code to access custom elements constructors from the global registry unless they are obeying their own namespace.

### Design

- Patch value on `CustomElementRegistry.prototype.get` descriptor to prevent accessing a custom element with the wrong prefix. This prevent them from accessing a constructor that they should not have access to.

### Distorted behavior

- Each time define method is called with the wrong prefix, it throws a `RangeError`.
<hr>
<a name="documentdocscookie-gettermd"></a>

## get: Document.prototype.cookie

Along access to the global window object, protecting access to cookies is absolutely crucial. If a malicious piece of code would get access to all the cookies on a page it could start issuing XHR requests impersonating the currently logged in user. This can have catastrophic effects in a multi tenant environment like Salesforce. It is absolutely necessary to protect the getter of `Document.prototype.cookie` and limit the view only to what is being set from within the sandbox, nothing from outside or other sandboxes.

### Goal

- To prevent access to cookies not belonging to the sandbox

### Design

- Patch the getter of Document.prototype.cookie to filter out any cookies set from outside the sandbox. This includes system cookies and other sandbox cookies. The current strategy for isolating cookies between sandboxes is to use a prefix for each key that is specific to each sandbox. The filtering of cookies will be done based on this prefix.

### Distorted behavior

- The getter will return only sandbox cookies. The behavior will seem native-like.
<hr>
<a name="documentdocscookie-settermd"></a>

## set: Document.prototype.cookie

Patching the setter of `Document.prototype.cookie` is required in order for the getter to manage to retrieve sandbox cookies. Additionally, we need to make sure that malicious code does not override critical system cookies that are necessary for a system like Salesforce to function properly. If we would not patch the setter then any sandbox would be able to send malicious payloads to the backend using cookies.

### Goal

- To prevent setting cookies that affect global behavior.

### Design

- Patch the setter of Document.prototype.cookie to prefix any cookie keys set from within the sandbox. The prefix is computed based on the namespace of the sandbox. 

### Distorted behavior

- The behavior will seem native like.
<hr>
<a name="documentdocsdomain-settermd"></a>

## set: Document.prototype.domain

According to [W3C](https://www.w3.org/TR/DOM-Level-2-HTML/html.html#ID-2250147)
this property should be read-only. Firefox does not allow setting it and throws
a SecurityError but Chrome, Safari and Edge (Webkit) allow it. The property cannot
be set to a random value, it has to be a suffix of the initial domain. So if the
initial value is `my.domain.com` the domain value that can be set is `domain.com`
because that is the suffix. The distortion shouldn't allow a sandbox to change the
domain of the root document.

### Goal

- Prevent domain from being changed from within the sandbox on root document.

### Design

- Patch the setter of Document.prototype.domain to throw an error regardless of
the value that's being used.

### Distorted behavior

- On Firefox we will throw an Error instead of SecurityError. On Chrome, Safari
and Edge (Webkit) we will throw an Error instead of allowing the setter to execute.
<hr>
<a name="documentdocsexeccommand-valuemd"></a>

## value: Document.prototype.execCommand [Main]

### Summary

When an HTML document has been switched to designMode, its document object exposes an execCommand method to run commands that manipulate the current editable region, such as form inputs or contentEditable elements. One command, "insertHTML" inserts new elements on the currently active editable element. 

In Locker, we share the HEAD and BODY. Even though it doesn't corrupt the existing elements inside or outside the element, if a malicious user can insert specified text as HTML into the DOM tree outside of the shared elements, it gives them the ability to pollute the DOM. We need to sanitize any elements added to this shared DOM.

### Distorted Behavior

This distortion sanitizes HTML string being inserted.
<hr>
<a name="elementdocsattachshadow-valuemd"></a>

## set: Element.prototype.attachShadow [Main]

### Summary

This method attaches a shadow DOM tree to the specified element. By providing
an options object with a `mode` of `'open'` the shadow DOM will be exposed to
the scripting environment allowing other namespaces access.

### Distorted Behavior

This distortion throws for any `mode` that is not `'closed'`, guarding against
additional modes added at later time, to prevent exposing the shadow DOM.
<hr>
<a name="elementdocsattributes-gettermd"></a>

## get: Element.attributes

The attributes collection is of type NamedNodeMap and can be used to set and remove attributes on an element. The distortion on this getter does not alter its functionality but only pairs an element with an NamedNodeMap instance such that the distortions on NamedNodeMap.prototype can retrieve the element.

### Goal

-   pair an Element instance with a NamedNodeMap for distortions on NamedNodeMap.prototype

### Design

-   use provided util `pairElement` to pair current element with NamedNodeMap instance when get accessor is invoked.
-   this pairing is only for bookkeeping and O(1) lookups based on the identity of attributes collection

### Distorted behavior

-   no distorted behavior
<hr>
<a name="elementdocsblocked-propertiesmd"></a>

## Fullscreen API: Element.prototype

Blocked properties from `Element.prototype` on specified browsers:

* `onfullscreenchange` [Chrome, Edge, Firefox]
* `onfullscreenerror` [Chrome, Edge, Firefox]
* `requestFullscreen` [Chrome, Edge, Firefox]
* `webkitRequestFullScreen` [Chrome, Edge, Safari]
* `webkitRequestFullscreen` [Chrome, Edge, Safari]
* `mozRequestFullScreen` [Firefox]

The fullscreen API allows elements to be displayed in "fullscreen" mode. It is supported by all major browsers, with varying implementations. The reason this API is blocked is because it does not adjust the DOM in the element but the native fullscreen hooks on the browser. A malicious user may use the fullscreen API for phishing attacks. For example, because the fullscreen API obscures the main address bar in all major browsers, a user can hide the fake URL on a phishing page. Or, this also allows users the ability to fake an address bar with their own DOM. <hr>
<a name="elementdocsinnerhtml-settermd"></a>

## set: Element.prototype.innerHTML [Main]

### Summary

This property allows users to replace DOM inside the element with nodes parsed from the given specified text as HTML. In Locker, we share the HEAD and BODY. This will allow a malicious user to replace the DOM of the HEAD and BODY with his specified text as HTML. Therefore, corrupting the DOM.

### Distorted Behavior

This distortion sanitizes and prevents HTML from replacing the DOM within shared elements: HEAD and BODY.
<hr>
<a name="elementdocsinsertadjacenthtml-valuemd"></a>

## set: Element.prototype.insertAdjacentHTML [Main]

### Summary

In Locker, we share the HEAD and BODY. Even though it doesn't corrupt the existing elements inside or outside the element, if a malicious user can insert specified text as HTML into the DOM tree outside of the shared elements, it gives them the ability to pollute the DOM.

### Distorted Behavior

This distortion sanitizes HTML being added.
<hr>
<a name="elementdocsouterhtml-settermd"></a>

## set: Element.prototype.outerHTML [Main]

### Summary

This property allows users to replace the element with nodes parsed from the given specified text as HTML. In Locker, we share the HEAD and BODY. This will allow a malicious user to replace the HEAD and BODY with his specified text as HTML. Therefore, corrupting the DOM.

### Distorted Behavior

This distortion sanitizes and prevents HTML from replacing the shared elements: HEAD and BODY.
<hr>
<a name="elementdocssetattribute-family-apismd"></a>

## value: Element.prototype.setAttribute

The `setAttribute*` distortions use internal registries to access already defined
distortions for property names. The only distorted behavior implemented here is a
defensive mechanism against shapeshifting objects. Shapeshifting objects do not
affect native DOM apis because values are automatically coerced, however,
shapeshifting attacks target Locker code in an attempt to bypass distortions.
The following example will attempt to explain this type of attack.

```js
const attrValue = {
    toString() {
        if (this.x) {
            return 'import';
        }

        this.x = true;
        return 'foo';
    },
};

const element = document.createElement('link');
element.setAttribute('rel', attrValue);
```

Because we have distorted setAttribute and the value is read at least twice
(1 time by locker 1 time by the native api), part of our code can be tricked to
think that the value is `'foo'` and it's safe to pass through. At the 2nd read
of attrValue its value will be `'import'`. Pseudo code explanation below:
```text
code in sandbox calls setAttribute with shapeshifting object
    locker reads first returned value and caches it in a local variable
        value 'foo' is cached and further checks rely on it
    locker uses cached value to determine if this is forbidden
        'foo' is allowed, execution is handled to native API using .call(obj, arguments)
    nativeApi coerces the argument to a string and sets it on the element
        shapeshifting occurs and the 2nd read returns now 'import'

```

In the case of setAttributeNode we perform the following operations:

- validate the passed attribute argument is indeed an instance of Attr
	- no actual validation happens the getter utilities will automatically detect
    this is not an instance of Attr


- the value property of the attribute is coerced to a string

### Goal

- To prevent shapeshifting arguments from being passed to lower level distortions
associated with setAttribute* APIs
- To allow execution of sub-distortions interested in handling specific attributes
and/or values

### Design

- expose 4 register methods, one for each type of distortions
(setAttribute, setAttributeNS, setAttributeNode, setAttributeNodeNS). The 4
registries optimize for performance and O(1) lookups because this family of APIs
are highly used.
- any call to `setAttribute*` methods will first sanitize the arguments to prevent
shapeshifting attacks followed by a lookup for a registered distortion
- if a distortion is found, invoke it and transfer control otherwise invoke the
native method with sanitized arguments

### Distorted behavior

- sanitization of arguments to prevent shapeshifting attacks
- Native like behavior unless a registered distortion needs to be executed at
which point the behavior is dependent on the execution of that distortion.
<hr>
<a name="elementdocsshadowroot-gettermd"></a>

## get: Element.prototype.shadowRoot [Main]

### Summary

This property allows retrieving the shadow DOM of custom elements created with `attachShadow({mode: 'open'})`.
Although in the sandbox elements cannot be created with this mode (see attachShadow distortion) other entities (framework code running in system mode) may create custom elements in this mode. This makes it particular dangerous for elements that get passed around as function arguments or are being queried from the DOM (both light or shadow). 

### Distorted Behavior

This distortion will return `null` when trying to access the `shadowRoot` property on a light-dom element.<hr>
<a name="eventdocscomposedpath-valuemd"></a>

## Event.prototype.composedPath [Main]

### Summary

This method returns the event's path which is an array of objects on which listeners will be
invoked. This does not include nodes in shadow trees if the shadow root was created with its
`ShadowRoot.mode` closed.


### Distorted Behavior

This method returns the event’s path which is an array of the objects on which listeners will
be invoked, up to the closed custom element itself, but not including the shadow root, or nodes
inside the shadow root.
<hr>
<a name="htmlelementdocsblocked-propertiesmd"></a>

## nonce: HTMLElement.prototype

This distortion blocks access to `HTMLElement.prototype.nonce` in Chrome, Edge.

In Locker, we do not allow the use of inline scripts. If a malicious user has access to the nonce value, the user may use it to bypass the Content Security Policy used to determine whether a given script will be allowed to proceed. Therefore, allowing them to run inline scripts.

## WindowEventHandlers: HTMLElement.prototype

This distortion blocks access to `HTMLElement.prototype.onrejectionhandled` and `HTMLElement.prototype.onunhandledrejection` in Safari.

This event "onrejectionhandled" is sent to the script's global scope whenever a Promise is rejected but after the promise rejection has been handled. In tandem, the event "onunhandledrejection" is sent whenever a Promise is rejected but there is no handler for the rejection. While most events are DOM related, this Promise related event handler receives an event object containing information about the rejected promise. The type, promise, and reason properties are still available in both event handlers. A malicious user could look into the promise info, which is why this needs to be blocked.
<hr>
<a name="htmlelementdocsoutertext-settermd"></a>

## set: Element.prototype.outerText [Chrome, Edge, Opera, Safari]

### Summary

This property allows users to replace the element with his text. In Locker, we share the HEAD and BODY. This will allow a malicious user to replace the HEAD and BODY with his text. Therefore, corrupting the DOM.

### Distorted Behavior

This distortion sanitizes and prevents text from replacing the shared elements: HEAD and BODY.

Note that `outerText` [is not a standard property](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/outerText#Browser_compatibility), so the descriptor could be undefined, like in the case of Firefox. In this case, this distortion does nothing.
<hr>
<a name="htmlelementdocsstyle-gettermd"></a>

## get: HTMLElement.prototype.style [Chrome, Edge, Opera, Safari]

### Summary

The `style` property on any HTMLElement object allows manipulating CSS styles via JavaScript via assignments (e.g. `element.style.color = 'red'`). Any property set on this object will reflect in the DOM via the `style` attribute on an element, making this object "magical" because of this behavior.

### Distorted Behavior

This distortion alters the getter of the style property for any HTMLElement. The `style` object is being marked as live such that
any properties changed from within the sandbox are reflected on the DOM.

Furthermore, this distortion does not cover a possible but highly improbable scenario: code passing the style object from system mode to the sandbox via function arguments. The distortion will not apply since the getter has been invoked in system mode. The resulting effect is that sandboxed code will not see changes to `style` being reflected in the DOM. If this scenario does happen then the distortion should be upgraded to a patch on the raw `HTMLElement.prototype` in native window.
<hr>
<a name="htmlframeelementdocscontentdocument-gettermd"></a>

## get: HTMLFrameElement.prototype.contentDocument

To reduce the surface area of possible exploit we return `null` for the
`contentDocument` property of frames. At a later time we may explore multi
document support, but in the interest of simplicity and moving things along
we have decided to keep things simple.

### Goal

- Do not expose the real raw `contentDocument`

### Design

The value of `contentDocument` may be `null` so we enforce that it is.

### Distorted behavior

- Always return `null` for `contentDocument`
<hr>
<a name="htmlframeelementdocscontentwindow-gettermd"></a>

## get: HTMLFrameElement.prototype.contentWindow

To reduce the surface area of possible exploit we produce an artificial
`contentWindow` object. At a later time we may explore nesting sandboxes,
but in the interest of simplicity and moving things along we have decided to
keep things simple.

### Goal
- Do not expose the real raw `contentWindow`
- Restrict access to a small curated list of properties

### Design

Create an artificial `contentWindow` object with a curated list of properties
  - close
  - closed
  - focus
  - opener
  - parent
  - postMessage

### Distorted behavior
- Return an artificial `contentWindow` object per frame
- Cache the artificial `contentWindow` object for subsequent accesses
<hr>
<a name="htmliframeelementdocscontentdocument-gettermd"></a>

## get: HTMLIFrameElement.prototype.contentDocument

To reduce the surface area of possible exploit we return `null` for the
`contentDocument` property of iframes. At a later time we may explore multi
document support, but in the interest of simplicity and moving things along
we have decided to keep things simple.

### Goal

- Do not expose the real raw `contentDocument`

### Design

The value of `contentDocument` may be `null` so we enforce that it is.

### Distorted behavior

- Always return `null` for `contentDocument`
<hr>
<a name="htmliframeelementdocscontentwindow-gettermd"></a>

## get: HTMLIFrameElement.prototype.contentWindow

To reduce the surface area of possible exploit we produce an artificial
`contentWindow` object. At a later time we may explore nesting sandboxes,
but in the interest of simplicity and moving things along we have decided to
keep things simple.

### Goal
- Do not expose the real raw `contentWindow`
- Restrict access to a small curated list of properties

### Design

Create an artificial `contentWindow` object with a curated list of properties
  - close
  - closed
  - focus
  - opener
  - parent
  - postMessage

### Distorted behavior
- Return an artificial `contentWindow` object per iframe
- Cache the artificial `contentWindow` object for subsequent accesses
<hr>
<a name="htmliframeelementdocssrc-settermd"></a>

## set: HTMLIFrameElement.prototype.src

Restrict supported src values to those that sanitize to http:// and https://
schemes.

### Goal
- Prevent URL schemes like javascript://

### Design

Only allow `src` values with validated schemes to be set.

### Distorted behavior
- Log a console warning for HTMLIFrameElement.src values that don't sanitize
  to http:// or https:// schemes
<hr>
<a name="htmlobjectelementdocscontentdocument-gettermd"></a>

## get: HTMLObjectElement.prototype.contentDocument

To reduce the surface area of possible exploit we return `null` for the
`contentDocument` property of object elements. At a later time we may explore
multi document support, but in the interest of simplicity and moving things along
we have decided to keep things simple.

### Goal

- Do not expose the real raw `contentDocument`

### Design

The value of `contentDocument` may be `null` so we enforce that it is.

### Distorted behavior

- Always return `null` for `contentDocument`
<hr>
<a name="htmlobjectelementdocscontentwindow-gettermd"></a>

## get: HTMLObjectElement.prototype.contentWindow

To reduce the surface area of possible exploit we produce an artificial
`contentWindow` object. At a later time we may explore nesting sandboxes,
but in the interest of simplicity and moving things along we have decided to
keep things simple.

### Goal
- Do not expose the real raw `contentWindow`
- Restrict access to a small curated list of properties

### Design

Create an artificial `contentWindow` object with a curated list of properties
  - close
  - closed
  - focus
  - opener
  - parent
  - postMessage

### Distorted behavior
- Return an artificial `contentWindow` object per object element
- Cache the artificial `contentWindow` object for subsequent accesses
<hr>
<a name="htmlscriptelementdocssrc-gettermd"></a>

## get: HTMLScriptElement.prototype.src

The setter distortion for the script element works by setting the original url to a different attribute named `data-distorted-src`, while the src attribute points to a distorted value we never reveal in the sandbox. When accessing the getter in the sandbox we need to get the original value thus the getter needs to look for the value on `data-distorted-src`. There are scenarios when a script tag may already be present in the DOM, inserted by the system through some other mechanisms. In this scenario we'll need to fallback to the original `src` attribute.

### Goal

- To mimic native behavior on retrieving `src` attribute value.

### Design

- Patch the getter of `HTMLScriptElement.prototype.src` to retrieve the value from `data-distorted-src` instead of `src` attribute. In case there was no distorted value set and there was already a value set on the `src` attribute, retrieve the value from the `src` attribute.

### Distorted behavior

- The getter will return the value of `data-distorted-src` when code in the sandbox tries to access `src` attribute on a script element.
<hr>
<a name="htmlscriptelementdocssrc-settermd"></a>

## set: HTMLScriptElement.prototype.src

To ensure that loaded Javascript code through a script tag runs in the sandbox, we need to evaluate the source text in the same sandbox. This poses a few challenges due to how the script tag works. We have to grab the source text and evaluate it ourselves rather than letting the browser evaluate it. Thus we need to prevent the native behavior of the script tag from triggering. 

### Goal

- Evaluate script tags in the sandbox.
- Maintain native like behavior, some browsers may load the code when the `src` attribute is being populated, some may load the code only when the element is placed in the DOM. This needs to be respected.

### Design

We need to satisfy a few requirements:

1. Prevent browser from fetching and evaluating the javascript file.

   To prevent the native behavior of the script tag we can populate a different attribute with the given value instead of the 'src' attribute. The original url will be stored on the attribute `data-distorted-src`. This will not trigger a fetch request, thus no triggering of the JIT will happen either but we will be able to retrieve the original value later on. 

2. Fetch and evaluate the file using other mechanisms that achieve the same end result.

   We fetch the file using an XHR request. This has some limitations, more specific, all cross-site origin requests may pose problems but our requirement is to satisfy loading script tags from the same domain so for the time being this behavior is sufficient. Once we have the source code we can evaluate it internally where needed.

3. Maintain native like behavior for errors and when the evaluation actually happens.

   Maintaining native like behavior is browser specific and we're mostly concerned about the success scenario and the 404 scenario. As mentioned already, the moment when the JIT is triggered is dependent on the browser implementation and this needs to be respected. As a workaround, to achieve native like behavior, once the XHR completes and we have the source code, we create a very simple Javascript snippet which is wrapped in a Blob object. We create a URL around this Blob object and use it on the `src` attribute to trigger the native behavior. The browser will read the content stored at the `blob:` URL and trigger the JIT which in turn will kick off the evaluation process in the sandbox. 

### Distorted behavior

- Store original value on `data-distorted-src`, store distorted value on `src`. 
- The behavior will seem native like to code running in the sandbox.
<hr>
<a name="messageeventdocssource-gettermd"></a>

## get: MessageEvent.prototype.source

The source read-only property of the MessageEvent is a property that represents
the message emitter. This issue was discovered during a pentest. A malicious user
can open a new browser tab that contains a postMessage to the current browser. 
After that, the current browser can access the raw window without distortions.

### Goal

- Do not expose the raw `window` in the sandbox.

### Design

Create an artificial `window` object if source property is a window.
Allow certain properties for curated list.

### Design

Create an artificial `window` object with a curated list of properties.
  - close
  - closed
  - focus
  - postMessage

### Distorted behavior
- Return an artificial `window` object for source.
- Cache the artificial `window` object for subsequent accesses.
<hr>
<a name="namednodemapdocssetnameditem-valuemd"></a>

## value: NamedNodeMap.prototype.setNamedItem

It is possible to set an attribute on an element using the methods available on NamedNodeMap. For example:

```js
const el = document.createElement('link');
const attr = document.createAttribute('rel');
attr.value = 'import';
el.attributes.setNamedItem(attr);
```

This would bypass our distortions for named properties and setAttribute\*. For this reason we need to distort `NamedNodeMap.prototype.setNamedItem`.

### Goal

- invoke registered DOM property distortions in situations like `el.attributes.setNamedItem(...)`

### Design
Inside of a NamedNodeMap distortion `this` does not point to an element but to the `attributes` instance. We have no way of understanding which `attributes` instance is for what element. That is why the shared lib of this module provides a `pairElement` utility used in Element.prototype.attributes distortion to pair an element with a NamedNodeMap instance upon accessing the getter of Element.prototype.attributes. Since all operations are synchronous we are guaranteed that the registration happens first followed by invocation later.
Example:

el.attributes.setNamedItem(....)
  |           |
registration  invocation

The registry is a WeakMap since elements can be removed from the page throughout the lifecycle of an application. The distortions are being retrieved from the `setAttributeNode` registry since both methods accept an instance of `Attr`.

### Distorted behavior

- if no distortion is found for an Attr instance then proceed with native invocation of setNamedItem
- if a distortion exists then the distorted behavior is relative to what that distortion does
<hr>
<a name="navigatordocsserviceworker-gettermd"></a>

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
<hr>
<a name="nodedocstextcontent-settermd"></a>

## set: Node.prototype.textContent [Main]

### Summary

This property allows users to replace DOM inside the element with his text. In Locker, we share the HEAD and BODY. This will allow a malicious user to replace the DOM of the HEAD and BODY with his text. Therefore, corrupting the DOM.

### Distorted Behavior

This distortion sanitizes and prevents text from replacing the DOM within shared elements: HEAD and BODY.
<hr>
<a name="rangedocscreatecontextualfragment-valuemd"></a>

## value: Range.prototype.createContextualFragment [Main]

### Summary

The Range.createContextualFragment() method returns a DocumentFragment by invoking the HTML fragment parsing algorithm or the XML fragment parsing algorithm with the start of the range as the context node. This range of HTML elements can be added to the DOM tree.

In Locker, we share the HEAD and BODY. Even though it doesn't corrupt the existing elements inside or outside the element, if a malicious user can insert specified text as HTML into the DOM tree outside of the shared elements, it gives them the ability to pollute the DOM. We need to sanitize any elements added to this shared DOM.

### Distorted Behavior

This distortion sanitizes HTML string that is used to create the DocumentFragment.
<hr>
<a name="svgscriptelementdocshref-attributemd"></a>

## href attribute on SVGScriptElement

### Summary

This distortion is necessary to run the contents of `href` file in the sandbox environment. The setter attribute for `href` is `undefined` in the `SVGScriptElement.prototype`. Access to the raw `window` could be attained by running scripts using the SVG `<script/>` tag.

### Goal

- Evaluate SVGScriptElement tags in the sandbox.
- Maintain native like behavior, some browsers may load the code when the `href` attribute is being populated, some may load the code only when the element is placed in the DOM. This needs to be respected.

### Distorted Behavior

We need to satisfy a few requirements:

1. Prevent browser from fetching and evaluating the javascript file.

   To prevent the native behavior of the script tag we can populate a different attribute with the given value instead of the 'href' attribute. The original url will be stored on the attribute `data-distorted-href`. This will not trigger a fetch request, thus no triggering of the JIT will happen either but we will be able to retrieve the original value later on. 

2. Fetch and evaluate the file using other mechanisms that achieve the same end result.

   We fetch the file using an XHR request. This has some limitations, more specific, all cross-site origin requests may pose problems but our requirement is to satisfy loading script tags from the same domain so for the time being this behavior is sufficient. Once we have the source code we can evaluate it internally where needed.

3. Maintain native like behavior for errors and when the evaluation actually happens.

   Maintaining native like behavior is browser specific and we're mostly concerned about the success scenario and the 404 scenario. As mentioned already, the moment when the JIT is triggered is dependent on the browser implementation and this needs to be respected. As a workaround, to achieve native like behavior, once the XHR completes and we have the source code, we create a very simple Javascript snippet which is wrapped in a Blob object. We create a URL around this Blob object and use it on the `href` attribute to trigger the native behavior. The browser will read the content stored at the `blob:` URL and trigger the JIT which in turn will kick off the evaluation process in the sandbox. 

### Distorted Behavior

- Store original value on `data-distorted-href`, store distorted value on `href`. 
- The behavior will seem native like to code running in the sandbox.
<hr>
<a name="svguseelementdocshref-attributemd"></a>

## href attribute and xlink:href attribute on SVGUseElement

### Summary

This distortion will sanitize the value passed for attribute `href` or `xlink:href`
on an SVGUseElement. The attribute is not on the prototype and can only be set
using the following APIs:

- setAttributeNS
- setAttributeNodeNS

#### Distorted behavior for setAttributeNS
```js
const el = document.createElementNS('http://www.w3.org/2000/svg', 'use');

el.setAttributeNS('http://www.w3.org/1999/xlink', 'href', '/myresource.svg#circle');
console.log(el.getAttributeNS('http://www.w3.org/1999/xlink', 'href')); // httpmycurrenthostmyresourcesvg_circle

// OR for xlink:href
el.setAttributeNS('hhttp://www.w3.org/1999/xlink', 'xlink:href', '/myresource.svg#circle');
console.log(el.getAttributeNS('http://www.w3.org/1999/xlink', 'href')); // httpmycurrenthostmyresourcesvg_circle
console.log(el.getAttributeNS('http://www.w3.org/1999/xlink', 'xlink:href')); // null
```

#### Distorted behavior for setAttributeNodeNS
```js
const el = document.createElementNS('http://www.w3.org/2000/svg', 'use');

let attr = document.createAttributeNS('http://www.w3.org/1999/xlink', 'href');
attr.value = '/myresource.svg#circle';
el.setAttributeNodeNS(attr);
console.log(el.getAttributeNS('http://www.w3.org/1999/xlink', 'href')); // httpmycurrenthostmyresourcesvg_circle

// OR for xlink:href
attr = document.createAttributeNS('http://www.w3.org/1999/xlink', 'xlink:href');
attr.value = '/myresource.svg#circle';
el.setAttributeNodeNS(attr);
console.log(el.getAttributeNS('http://www.w3.org/1999/xlink', 'xlink:href')); // httpmycurrenthostmyresourcesvg_circle
```

Other scenarios that can be used to bypass this distortion are covered by the
underlying architecture of Element distortions. These scenarios are:

- creating an attribute with an empty value, using setAttributeNode/NS to attach
the attribute and update the value post setAttributeNode/NS operation
- using attributes.setItem API to attach an attribute

**setAttribute will not trigger this distortion.**
**setAttributeNode WILL trigger the distortion if the attribute was created in the XLINK SVG namespace.**

### Design

- passthrough if the URL is a document fragment URL (#svg)
- if the URL is an external resource (/resource.svg#circle) then transform this
URL to a document fragment URL composed of current hostname, resource name, extension
followed by an underscore and the id in the referenced resource (#HOSTNAMEresourcesvg_circle).
    - URL transformation is synchronous
    - internally this will map to a hidden div in the page. The div will be empty
    at first
    - the resource is being fetched asynchronously via XHR and sanitized using our
    SVG sanitizer profile
    - the sanitized content will be placed in the hidden div. The content will be
    rendered where the use tag is defined because of how document fragment references
    work in HTML. Dynamic content changes will be picked up by the elements who
    point to the specific document location with each change. Thus, when the DIV
    gets populated with the sanitized SVG, the use tag will see the new content.
    - the sanitizer works recursively, any resources loaded through the initial
    referenced SVG file (myresource.svg) will go through the same process. Thus
    it is not possible to trick the system by loading a simple SVG with a <use>
    tag which points to a malicious resource.

### Dependencies
- DOMPUrify
- html-sanitizer package
<hr>
<a name="serviceworkercontainerdocsprototype-valuemd"></a>

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
<hr>
<a name="shadowrootdocsmode-gettermd"></a>

## get: ShadowRoot.prototype.mode

### Goal

 - To force a reported mode of 'closed'.

### Design

- Patch getter on `ShadowRoot.prototype.mode` descriptor to return `'closed'`.

### Distorted behavior

- Each time code accesses `mode` property on any element with an attached shadow
  DOM this distortion will return `'closed'`.
<hr>
<a name="sharedworkerdocsconstructor-valuemd"></a>

## SharedWorker Global Constructor

### Summary

The `SharedWorker()` constructor creates a SharedWorker object that executes the script at the specified URL. This script must obey the same-origin policy. Malicious users can execute script at a specified URL to bypass Locker evaluation rules. 

### Distorted Behavior

Locker will throw a `RangeError` when calling the constructor. Locker will block access to `SharedWorker.prototype`.<hr>
<a name="storagedocsclear-valuemd"></a>

## value: Storage.prototype.clear [Main]

### Summary

The Storage interface provides access to the a particular domain's session or local storage. It allows the addition, modification, or deletion of stored data items which is shared in system mode.

Since each sandbox uses it's own synthetic storage, we cannot allow a malicious user to clear all the data items in system mode.

### Distorted Behavior

This distortion deletes all data items from its synthetic storage.<hr>
<a name="storagedocsconstructor-valuemd"></a>

## Storage API: Storage.prototype

### Summary

The Storage interface provides access to the a particular domain's session or local storage. It allows the addition, modification, or deletion of stored data items which is shared in system mode. The storage is accessible on the browser and holds its shape across multiple tabs from the same domain. Therefore, we would have to store each namespaces storage in a synthetic storage, where we do not allow malicious users to add, modify, or clear data items in global or from other namespaces.

KEY: The key() method of the Storage interface, when passed a number n, returns the name of the nth key in a given Storage object. The order of keys is user-agent defined, so you should not rely on it. Therefore, it is okay to have the storage items out of order.

### Distorted Behavior

Distorted behaviors from `Storage.prototype`:

* `length`
* `setItem`
* `getItem`
* `key`
* `removeItem`
* `clear`

This distortion prepends an LSKey[NS] to all storage values set in each namespace where NS is the namespace name. This distortion uses a SecureStorage class that implements all methods and properties from the raw Storage. This distoration also uses a proxy to mimic interactibility features that are on the raw Storage. Storage Example:

[Global]
`localStorage.setItem('x','y'); localStorage; // { 'x': 'y', 'LSKey[NS1]x': 'y', 'LSKey[NS2]x': 'y' }`

[NS1]
`localStorage.setItem('x','y'); localStorage; // { 'x': 'y' }`

[NS2]
`localStorage.setItem('x','y'); localStorage; // { 'x': 'y' }`

The proxy wrap has traps that allow for our Storage to have features that are the same as the raw Storage. Such features include getting, setting, iterating and basic object features.

* Set/Get: `localStorage.x = 'y'; localStorage; // { 'x': 'y' }`
* Define Property: `Object.defineProperty(localStorage, 'foo', { value: 'bar' }); // { 'foo': 'bar', 'x': 'y' }`
* Delete Property: `delete localStorage.foo; // { 'x': 'y' }`
* Iteration: `Object.keys(localStorage); // ['x']`
* Has: `'x' in sessionStorage; localStorage.hasOwnProperty('x'); // true, true`<hr>
<a name="storagedocsgetitem-valuemd"></a>

## value: Storage.prototype.getItem [Main]

### Summary

The Storage interface provides access to the a particular domain's session or local storage. It allows the addition, modification, or deletion of stored data items which is shared in system mode.

In order for one sandbox not to retrieve the storage of another sandbox, we must create a synthetic storage for each sandbox.

### Distorted Behavior

This distortion retrieves data items from its synthetic storage.<hr>
<a name="storagedocskey-valuemd"></a>

## value: Storage.prototype.key [Main]

### Summary

The Storage interface provides access to the a particular domain's session or local storage. It allows the addition, modification, or deletion of stored data items which is shared in system mode.

The key() method of the Storage interface, when passed a number n, returns the name of the nth key in a given Storage object. The order of keys is user-agent defined, so you should not rely on it. Therefore, it is okay to have the storage items out of order.

### Distorted Behavior

This distortion retrieves a key value at a specific index from its synthetic storage.<hr>
<a name="storagedocslength-gettermd"></a>

## get: Storage.prototype.length [Main]

### Summary

The Storage interface provides access to the a particular domain's session or local storage. It allows the addition, modification, or deletion of stored data items which is shared in system mode.

In order for one sandbox not to retrieve the storage of another sandbox, we must create a synthetic storage for each sandbox. When looking at length, we must retrieve the number of data items in the synthetic storage rather than the system mode storage.

### Distorted Behavior

This distortion retrieves the number of data items in its synthetic storage.<hr>
<a name="storagedocsremoveitem-valuemd"></a>

## value: Storage.prototype.removeItem [Main]

### Summary

The Storage interface provides access to the a particular domain's session or local storage. It allows the addition, modification, or deletion of stored data items which is shared in system mode.

Since each sandbox uses it's own synthetic storage, we cannot allow a malicious user to clear a data item from another sandbox.

### Distorted Behavior

This distortion deletes a data item from its synthetic storage.<hr>
<a name="storagedocssetitem-valuemd"></a>

## value: Storage.prototype.setItem [Main]

### Summary

The Storage interface provides access to the a particular domain's session or local storage. It allows the addition, modification, or deletion of stored data items which is shared in system mode.

In order for one sandbox not to modify the storage of another sandbox, we must create a synthetic storage for each sandbox.

### Distorted Behavior

This distortion adds or modifies data items in its synthetic storage.<hr>
<a name="urldocscreateobjecturl-valuemd"></a>

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
<hr>
<a name="windowdocsfetch-valuemd"></a>

## Window.fetch

### Goal

To prevent users from making requests to disallowed endpoints.

### Design

Patch the `Window.fetch` property and intercept calls to it to block disallowed URLs.

### Distorted behavior

The `Window.fetch` distortion examines the `hostname` and the `pathname` of the URL, and if it matches one of the disallowed entries, it rejects the promise.

### Disallowed endpoints

Locker disallows endpoints:

- Containing `"/aura"` in the URL.
- Containing `"/webruntime"` in the URL.

At the moment this is hard coded, but in the future this will be a configuration option.
<hr>
<a name="windowdocsframes-gettermd"></a>

## get: window.frames [Main]

### Summary

The Window interface's `frames` property returns an object that is the window
itself, which is an array-like object, listing the direct sub-frames of the
current window.

### Distorted Behavior

The Window interface's `frames` property returns a fake `frameList` that includes
all `<frame>` and `<iframe>` elements in the document, in insertion order. Supports
access via index or name property value. `window.frames` does not allow access to
`window`, ie. `window.frames !== window`, and does not provide proxy access to
`window` properties.
<hr>
<a name="windowdocslength-gettermd"></a>

## get: window.length [Main]

### Summary

The Window interface's `length` property returns the number of frames (either `<frame>` or `<iframe>` elements) attached to the `window`'s `document`.

### Distorted Behavior

The Window interface's `length` property always returns `0`. Application code must use the `window.frames.length` value and `window.frames` object to iterate over the list of frames (either `<frame>` or `<iframe>` elements) attached to the `document`.
<hr>
<a name="windowdocsopen-valuemd"></a>

## value: Window.prototype.open [Main]

### Summary

The `open` method, loads the specified resource into a new or existing browsing context with the specified name. If the name doesn't exist, then a new browsing context is opened in a new tab or a new window, and the specified resource is loaded into it. This new context is not sandboxed properly and malicious users can access system mode.

### Distorted Behavior

Locker will return an artificial `Window` object that contains specific safe methods we allow.
<hr>
<a name="windowdocsopener-gettermd"></a>

## get: window.opener [Main]

### Summary

The Window interface's `opener` property returns a reference to the window that opened the window, either with open(), or by navigating a link with a target attribute.

In other words, if window A opens window B, B.opener returns A.

### Distorted Behavior

Locker will return an artificial `Window` object that contains specific safe methods we allow.
<hr>
<a name="windowdocsparent-gettermd"></a>

## get: window.parent [Main]

### Summary

The Window interface's `parent` property returns a reference to the parent of the current window or subframe. If a window does not have a parent, its parent property is a reference to itself. If window A embeds window B, B.parent returns A.

### Distorted Behavior

Locker will return a patched `Window` object that contains specific safe methods we allow.<hr>
<a name="windowdocssetinterval-valuemd"></a>

## value: Window.prototype.setInterval [Main]

### Summary

The `setInterval` method, repeatedly calls a function or executes a code snippet, with a fixed time delay between each call. But `setInterval` supports string evaluation by specifying a string for its first argument. This escapes the sandbox.

### Distorted Behavior

If the first argument provided to `setInterval` is a string value, this distortion evaluates it in the sandbox.<hr>
<a name="windowdocssettimeout-valuemd"></a>

## value: window.setTimeout [Main]

### Summary

The `setTimeout` method, repeatedly calls a function or executes a code snippet, with a fixed time delay between each call. But `setTimeout` supports string evaluation by specifying a string for its first argument. This escapes the sandbox.

### Distorted Behavior

If the first argument provided to `setTimeout` is a string value, this distortion evaluates it in the sandbox.
<hr>
<a name="workerdocsconstructor-valuemd"></a>

## Worker Global Constructor

### Summary

The `Worker()` constructor creates a Worker object that executes the script at the specified URL. This script must obey the same-origin policy. Malicious users can execute script at a specified URL to bypass Locker evaluation rules. 

### Distorted Behavior

Locker will throw a `RangeError` when calling the constructor. Locker will block access to `Worker.prototype`.
<hr>
<a name="xmlhttprequestdocsopen-valuemd"></a>

## XMLHttpRequest.open

### Goal

To prevent users from making requests to disallowed endpoints.

### Design

Patch the `XMLHttpRequest.open` property and intercept calls to it to block disallowed URLs.

### Distorted behavior

The `XMLHttpRequest.open` distortion examines the `hostname` and the `pathname` of the URL, and if it matches one of the disallowed entries, it throws an error.

### Disallowed endpoints

Locker disallows endpoints:

- Containing `"/aura"` in the URL.
- Containing `"/webruntime"` in the URL.

At the moment this is hard coded, but in the future this will be a configuration option.
