# Lightning Web Security Distortions

This is the list of the currently implemented distortions.

Version: 0.15.4<br>
Generated: Jan 12, 2022

## Table of Contents

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Attr.prototype.value setter](#attrprototypevalue-setter)
  - [Distorted Behavior](#distorted-behavior)
- [CookieStore.addEventListener](#cookiestoreaddeventlistener)
  - [Distorted Behavior](#distorted-behavior-1)
- [CookieStore.prototype.delete getter](#cookiestoreprototypedelete-getter)
  - [Distorted Behavior](#distorted-behavior-2)
- [CookieStore.prototype.get getter](#cookiestoreprototypeget-getter)
  - [Distorted Behavior](#distorted-behavior-3)
- [CookieStore.prototype.getAll getter](#cookiestoreprototypegetall-getter)
  - [Distorted Behavior](#distorted-behavior-4)
- [CookieStore.prototype.onchange](#cookiestoreprototypeonchange)
  - [Distorted Behavior](#distorted-behavior-5)
- [CookieStore.prototype.set setter](#cookiestoreprototypeset-setter)
  - [Distorted Behavior](#distorted-behavior-6)
- [CustomElementRegistry.prototype.define](#customelementregistryprototypedefine)
  - [Distorted Behavior](#distorted-behavior-7)
- [CustomElementRegistry.prototype.get](#customelementregistryprototypeget)
  - [Distorted Behavior](#distorted-behavior-8)
- [DOMParser.prototype.parseFromString](#domparserprototypeparsefromstring)
  - [Distorted Behavior](#distorted-behavior-9)
- [Document.prototype.cookie getter](#documentprototypecookie-getter)
  - [Distorted Behavior](#distorted-behavior-10)
- [Document.prototype.cookie setter](#documentprototypecookie-setter)
  - [Distorted Behavior](#distorted-behavior-11)
- [Document.prototype.domain setter](#documentprototypedomain-setter)
  - [Distorted Behavior](#distorted-behavior-12)
- [Document.prototype.execCommand](#documentprototypeexeccommand)
  - [Distorted Behavior](#distorted-behavior-13)
- [Document.open](#documentopen)
  - [Distorted Behavior](#distorted-behavior-14)
- [Element.prototype.after](#elementprototypeafter)
  - [Distorted Behavior](#distorted-behavior-15)
- [Element.prototype.append](#elementprototypeappend)
  - [Summary](#summary)
  - [Distorted Behavior](#distorted-behavior-16)
- [Element.prototype.attachShadow setter](#elementprototypeattachshadow-setter)
  - [Distorted Behavior](#distorted-behavior-17)
- [Element.prototype.attributes getter](#elementprototypeattributes-getter)
  - [Distorted Behavior](#distorted-behavior-18)
- [Element.prototype.before](#elementprototypebefore)
  - [Distorted Behavior](#distorted-behavior-19)
- [Fullscreen API: Element.prototype](#fullscreen-api-elementprototype)
  - [Distorted Behavior](#distorted-behavior-20)
- [Element.prototype.innerHTML setter](#elementprototypeinnerhtml-setter)
  - [Distorted Behavior](#distorted-behavior-21)
- [Element.prototype.insertAdjacentElement](#elementprototypeinsertadjacentelement)
  - [Distorted Behavior](#distorted-behavior-22)
- [Element.prototype.insertAdjacentHTML](#elementprototypeinsertadjacenthtml)
  - [Distorted Behavior](#distorted-behavior-23)
- [Element.prototype.outerHTML setter](#elementprototypeouterhtml-setter)
  - [Distorted Behavior](#distorted-behavior-24)
- [Element.prototype.prepend](#elementprototypeprepend)
  - [Distorted Behavior](#distorted-behavior-25)
- [Element.prototype.remove](#elementprototyperemove)
  - [Distorted Behavior](#distorted-behavior-26)
- [Element.prototype.replaceChildren](#elementprototypereplacechildren)
  - [Distorted Behavior](#distorted-behavior-27)
- [Element.prototype.replaceWith](#elementprototypereplacewith)
  - [Distorted Behavior](#distorted-behavior-28)
- [Element.prototype.setAttribute*](#elementprototypesetattribute)
  - [Distorted Behavior](#distorted-behavior-29)
- [Element.prototype.shadowRoot getter](#elementprototypeshadowroot-getter)
  - [Distorted Behavior](#distorted-behavior-30)
- [Event.prototype.composedPath](#eventprototypecomposedpath)
  - [Distorted Behavior](#distorted-behavior-31)
- [HTMLElement.prototype.nonce](#htmlelementprototypenonce)
- [WindowEventHandlers: HTMLElement.prototype](#windoweventhandlers-htmlelementprototype)
- [HTMLElement.prototype.innerText setter [Chrome, Edge, Opera, Safari]](#htmlelementprototypeinnertext-setter-chrome-edge-opera-safari)
  - [Summary](#summary-1)
  - [Distorted Behavior](#distorted-behavior-32)
- [Element.prototype.outerText  setter [Chrome, Edge, Opera, Safari]](#elementprototypeoutertext--setter-chrome-edge-opera-safari)
  - [Summary](#summary-2)
  - [Distorted Behavior](#distorted-behavior-33)
- [HTMLElement.prototype.style getter [Chrome, Edge, Opera, Safari]](#htmlelementprototypestyle-getter-chrome-edge-opera-safari)
  - [Summary](#summary-3)
  - [Distorted Behavior](#distorted-behavior-34)
- [HTMLFrameElement.prototype.contentDocument getter](#htmlframeelementprototypecontentdocument-getter)
  - [Goal](#goal)
  - [Design](#design)
  - [Distorted Behavior](#distorted-behavior-35)
- [HTMLFrameElement.prototype.contentWindow getter](#htmlframeelementprototypecontentwindow-getter)
  - [Goal](#goal-1)
  - [Design](#design-1)
  - [Distorted Behavior](#distorted-behavior-36)
- [HTMLIFrameElement.prototype.contentDocument getter](#htmliframeelementprototypecontentdocument-getter)
  - [Goal](#goal-2)
  - [Design](#design-2)
  - [Distorted Behavior](#distorted-behavior-37)
- [HTMLIFrameElement.prototype.contentWindow getter](#htmliframeelementprototypecontentwindow-getter)
  - [Goal](#goal-3)
  - [Design](#design-3)
  - [Distorted Behavior](#distorted-behavior-38)
- [HTMLIFrameElement.prototype.src setter](#htmliframeelementprototypesrc-setter)
  - [Goal](#goal-4)
  - [Design](#design-4)
  - [Distorted Behavior](#distorted-behavior-39)
- [HTMLObjectElement.prototype.contentDocument getter](#htmlobjectelementprototypecontentdocument-getter)
  - [Goal](#goal-5)
  - [Design](#design-5)
  - [Distorted Behavior](#distorted-behavior-40)
- [HTMLObjectElement.prototype.contentWindow getter](#htmlobjectelementprototypecontentwindow-getter)
  - [Goal](#goal-6)
  - [Design](#design-6)
  - [Distorted Behavior](#distorted-behavior-41)
- [HTMLScriptElement.prototype.src getter](#htmlscriptelementprototypesrc-getter)
  - [Goal](#goal-7)
  - [Design](#design-7)
  - [Distorted Behavior](#distorted-behavior-42)
- [HTMLScriptElement.prototype.src setter](#htmlscriptelementprototypesrc-setter)
  - [Goal](#goal-8)
  - [Design](#design-8)
  - [Distorted Behavior](#distorted-behavior-43)
- [MessageEvent.prototype.source getter](#messageeventprototypesource-getter)
  - [Goal](#goal-9)
  - [Design](#design-9)
  - [Design](#design-10)
  - [Distorted Behavior](#distorted-behavior-44)
- [NamedNodeMap.prototype.setNamedItem](#namednodemapprototypesetnameditem)
  - [Goal](#goal-10)
  - [Design](#design-11)
  - [Distorted Behavior](#distorted-behavior-45)
- [Navigator.prototype.serviceWorker getter](#navigatorprototypeserviceworker-getter)
  - [Problem statement](#problem-statement)
  - [Goal](#goal-11)
  - [Design](#design-12)
  - [Distorted Behavior](#distorted-behavior-46)
- [Node.prototype.appendChild](#nodeprototypeappendchild)
  - [Summary](#summary-4)
  - [Distorted Behavior](#distorted-behavior-47)
- [Node.prototype.textContent setter](#nodeprototypetextcontent-setter)
  - [Summary](#summary-5)
  - [Distorted Behavior](#distorted-behavior-48)
- [Range.prototype.createContextualFragment](#rangeprototypecreatecontextualfragment)
  - [Summary](#summary-6)
  - [Distorted Behavior](#distorted-behavior-49)
- [href attribute on SVGScriptElement](#href-attribute-on-svgscriptelement)
  - [Summary](#summary-7)
  - [Goal](#goal-12)
  - [Distorted Behavior](#distorted-behavior-50)
  - [Distorted Behavior](#distorted-behavior-51)
- [href attribute and xlink:href attribute on SVGUseElement](#href-attribute-and-xlinkhref-attribute-on-svguseelement)
  - [Summary](#summary-8)
  - [Design](#design-13)
  - [Dependencies](#dependencies)
- [ServiceWorkerContainer.prototype](#serviceworkercontainerprototype)
  - [Problem Statement](#problem-statement)
  - [Goal](#goal-13)
  - [Distorted Behavior](#distorted-behavior-52)
- [ShadowRoot.prototype.innerHTML setter](#shadowrootprototypeinnerhtml-setter)
  - [Summary](#summary-9)
  - [Distorted Behavior](#distorted-behavior-53)
- [ShadowRoot.prototype.mode getter](#shadowrootprototypemode-getter)
  - [Goal](#goal-14)
  - [Design](#design-14)
  - [Distorted Behavior](#distorted-behavior-54)
- [SharedWorker Global Constructor](#sharedworker-global-constructor)
  - [Summary](#summary-10)
  - [Distorted Behavior](#distorted-behavior-55)
- [Storage.prototype.clear](#storageprototypeclear)
  - [Summary](#summary-11)
  - [Distorted Behavior](#distorted-behavior-56)
- [Storage API: Storage.prototype](#storage-api-storageprototype)
  - [Summary](#summary-12)
  - [Distorted Behavior](#distorted-behavior-57)
- [Storage.prototype.getItem](#storageprototypegetitem)
  - [Summary](#summary-13)
  - [Distorted Behavior](#distorted-behavior-58)
- [Storage.prototype.key](#storageprototypekey)
  - [Summary](#summary-14)
  - [Distorted Behavior](#distorted-behavior-59)
- [Storage.prototype.length getter](#storageprototypelength-getter)
  - [Summary](#summary-15)
  - [Distorted Behavior](#distorted-behavior-60)
- [Storage.prototype.removeItem](#storageprototyperemoveitem)
  - [Summary](#summary-16)
  - [Distorted Behavior](#distorted-behavior-61)
- [Storage.prototype.setItem](#storageprototypesetitem)
  - [Summary](#summary-17)
  - [Distorted Behavior](#distorted-behavior-62)
- [URL.createObjectURL](#urlcreateobjecturl)
  - [Goal](#goal-15)
  - [Design](#design-15)
  - [Distorted Behavior](#distorted-behavior-63)
- [Window.fetch](#windowfetch)
  - [Goal](#goal-16)
  - [Design](#design-16)
  - [Distorted Behavior](#distorted-behavior-64)
  - [Disallowed endpoints](#disallowed-endpoints)
- [window.frames getter](#windowframes-getter)
  - [Summary](#summary-18)
  - [Distorted Behavior](#distorted-behavior-65)
- [window.length getter](#windowlength-getter)
  - [Summary](#summary-19)
  - [Distorted Behavior](#distorted-behavior-66)
- [Window.prototype.open](#windowprototypeopen)
  - [Summary](#summary-20)
  - [Distorted Behavior](#distorted-behavior-67)
- [window.opener getter](#windowopener-getter)
  - [Summary](#summary-21)
  - [Distorted Behavior](#distorted-behavior-68)
- [window.parent getter](#windowparent-getter)
  - [Summary](#summary-22)
  - [Distorted Behavior](#distorted-behavior-69)
- [Window.prototype.setInterval](#windowprototypesetinterval)
  - [Summary](#summary-23)
  - [Distorted Behavior](#distorted-behavior-70)
- [window.setTimeout](#windowsettimeout)
  - [Summary](#summary-24)
  - [Distorted Behavior](#distorted-behavior-71)
- [Worker Global Constructor](#worker-global-constructor)
  - [Summary](#summary-25)
  - [Distorted Behavior](#distorted-behavior-72)
- [XMLHttpRequest.open](#xmlhttprequestopen)
  - [Goal](#goal-17)
  - [Design](#design-17)
  - [Distorted Behavior](#distorted-behavior-73)
  - [Disallowed endpoints](#disallowed-endpoints-1)
- [XMLHttpRequest.prototype.response getter](#xmlhttprequestprototyperesponse-getter)
  - [Summary](#summary-26)
  - [Distorted Behavior](#distorted-behavior-74)
- [XMLHttpRequest.prototype.responseXML getter](#xmlhttprequestprototyperesponsexml-getter)
  - [Summary](#summary-27)
  - [Distorted Behavior](#distorted-behavior-75)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


<a name="attrdocsvalue-settermd"></a>

## Attr.prototype.value setter

The [`Attr`](https://developer.mozilla.org/en-US/docs/Web/API/Attr/value) interface represents one of an element's attributes as an object.

The core idea of an object of type `Attr` is the association between a name and a value. An attribute may also be part of a namespace and, in this case, it also has a URI identifying the namespace, and a prefix that is an abbreviation for the namespace.

This distortion acts as a router for attribute distortions. It checks a registry for distortions that apply to a particular attribute name and invokes those distortions.

This distortion works only on connected attribute nodes. Disconnected nodes are covered by `setAttributeNode` and `setAttributeNodeNS` distortions.

This example of setting the value of `rel` property of a link shows behavior that's blocked.

```js
const attr = createAttribute('rel');
const el = createElement('link');
el.setAttributeNode(attr); // bypass setAttributeNode distortion
attr.value = 'import'; // attempt to set blocked value
document.head.appendChild(el); // append to head
```
### Distorted Behavior

The behavior varies according to the invoked distortion. If no distortions are registered for an attribute, the behavior seems native.
<hr>
<a name="cookiestoredocsaddeventlistener-valuemd"></a>

## CookieStore.addEventListener

The [`addEventListener()`](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener) method of the `EventTarget` interface sets up a function that will be called whenever the specified event is delivered to the target.

Common targets are `Element`, or its children, `Document`, and `Window`, but the target may be any object that supports events (such as `XMLHttpRequest`).

This distortion prevents code from accessing cookies outside of the sandbox.

### Distorted Behavior

Currently, Lightning Web Security doesn't support the `CookieStore.onchange` event, so attaching an event listener to `CookieStore` is not allowed. Calls to `CookieStore.addEventListener()` return an error.
<hr>
<a name="cookiestoredocsdelete-valuemd"></a>

## CookieStore.prototype.delete getter

The [`delete()`](https://developer.mozilla.org/en-US/docs/Web/API/CookieStore/delete) method of the `CookieStore` interface deletes a cookie with the given name or options object.

If malicious code deletes cookies on a page, it could remove login cookies and make the app unusable. This distortion protects cookies outside the sandbox from `CookieStore.prototype.delete` and limits what can be deleted within the sandbox. Cookies in the sandbox are protected from code outside or in other sandboxes.

### Distorted Behavior

The distortion only permits deletion of sandbox cookies.

<hr>
<a name="cookiestoredocsget-valuemd"></a>

## CookieStore.prototype.get getter

The [`get()`](https://developer.mozilla.org/en-US/docs/Web/API/CookieStore/get) method of the `CookieStore` interface returns a single cookie with the given name or options object.

If malicious code can access any cookie on a page, it can issue XHR requests impersonating the user who's logged in. This behavior can have catastrophic effects in a multi-tenant environment like Salesforce. 

This distortion protects the value of `CookieStore.prototype.get` and limits the view to what is being retrieved from within the sandbox. Cookies in the sandbox are protected from code outside or in other sandboxes.

### Distorted Behavior

The `get()` method returns only sandbox cookies.

<hr>
<a name="cookiestoredocsgetall-valuemd"></a>

## CookieStore.prototype.getAll getter

The [`getAll()`](https://developer.mozilla.org/en-US/docs/Web/API/CookieStore/getAll) method of the `CookieStore` interface returns a list of cookies that match the name or options passed to it. Passing no parameters will return all cookies for the current context.

If malicious code can access all cookies on a page, it can issue XHR requests impersonating the user who's logged in. This behavior can have catastrophic effects in a multi-tenant environment like Salesforce. 

This distortion protects the value of `CookieStore.prototype.getAll` and limits the view to what is being retrieved from within the sandbox. Cookies in the sandbox are protected from code outside or in other sandboxes.

### Distorted Behavior

The `getAll()` method returns only sandbox cookies.
<hr>
<a name="cookiestoredocsonchange-settermd"></a>

## CookieStore.prototype.onchange

The [`onchange`](https://developer.mozilla.org/en-US/docs/Web/API/CookieStore/onchange) EventHandler of the `CookieStore` interface fires when a change is made to any cookie.

This distortion prevents code from accessing cookies outside of the sandbox.

### Distorted Behavior

Currently, Lightning Web Security doesn't support the `CookieStore.onchange` event, so setting the `onchange` property is not allowed and returns an error.
<hr>
<a name="cookiestoredocsset-valuemd"></a>

## CookieStore.prototype.set setter

The [`set()`](https://developer.mozilla.org/en-US/docs/Web/API/CookieStore/set) method of the `CookieStore` interface sets a cookie with the given name and value or options object.

Distortion of `CookieStore.prototype.set` is required so `CookieStore.prototype.get` can retrieve sandbox cookies that are similarly distorted with the sandbox prefix. 

This distortion also prevents malicious code from accessing system cookies that Salesforce uses to function. Otherwise any sandbox can send malicious payloads to the backend using cookies.

### Distorted Behavior

The `set()` method automatically adds the sandbox prefix to keys for sandbox cookies. <hr>
<a name="customelementregistrydocsdefine-valuemd"></a>

## CustomElementRegistry.prototype.define

The [`define`](https://developer.mozilla.org/en-US/docs/Web/API/CustomElementRegistry/define) method of the `CustomElementRegistry` interface defines a new custom element. 

Lightning Web Security doesn't allow defining custom elements because the registry is global to the page. You can't register custom elements in the sandbox. 
### Distorted Behavior

This distortion prevents invoking `define` method from `CustomElementRegistry` and displays an error.
<hr>
<a name="customelementregistrydocsget-valuemd"></a>

## CustomElementRegistry.prototype.get

The [`get`](https://developer.mozilla.org/en-US/docs/Web/API/CustomElementRegistry/get) method of `CustomElementRegistry` interface returns the constructor for a previously-defined custom element. 

Lightning Web Security allows sandboxed code to access existing custom element constructors from the global registry only if the custom element is prefixed with the same namespace. 

### Distorted Behavior

When called with the wrong prefix, the `get` method returns `undefined`.
<hr>
<a name="domparserdocsparsefromstring-valuemd"></a>

## DOMParser.prototype.parseFromString

The [`DOMParser.parseFromString()`](https://developer.mozilla.org/en-US/docs/Web/API/DOMParser/parseFromString) method parses a string containing either HTML or XML, returning an `HTMLDocument` or an `XMLDocument`.

Documents created via `new DOMParser().parseFromString('', 'text/html')` are subject to the same rules that govern `Element.prototype.innerHTML`.

### Distorted Behavior

This distortion sanitizes HTML strings prior to parsing and document creation.
<hr>
<a name="documentdocscookie-gettermd"></a>

## Document.prototype.cookie getter

The [`Document.cookie`](https://developer.mozilla.org/en-US/docs/Web/API/Document/cookie) property lets you read and write cookies associated with the document. It serves as a getter and setter for the actual values of the cookies.

Protecting access to cookies is crucial. If malicious code can access all cookies on a page, it can issue XHR requests impersonating the user who's logged in. This can have catastrophic effects in a multi-tenant environment like Salesforce. 

This distortion protects the getter of `Document.prototype.cookie` and limits the view to what is being set from within the sandbox. Cookies inside the sandbox are protected from code outside or in other sandboxes.

### Distorted Behavior

The getter returns only cookies that belong to the sandbox.
<hr>
<a name="documentdocscookie-settermd"></a>

## Document.prototype.cookie setter

The [`Document.cookie`](https://developer.mozilla.org/en-US/docs/Web/API/Document/cookie) property lets you read and write cookies associated with the document. It serves as a getter and setter for the actual values of the cookies.

The setter for `Document.prototype.cookie` is distorted so the getter can retrieve sandbox cookies. Additionally, the distortion prevents changes to critical system cookies that are necessary for Salesforce to function properly. If code in a sandbox is allowed to set system cookies, it can send malicious payloads to the backend using cookies.

### Distorted Behavior

The setter can modify only cookies that belong to the sandbox.
<hr>
<a name="documentdocsdomain-settermd"></a>

## Document.prototype.domain setter

The deprecated [`Document.domain`](https://developer.mozilla.org/en-US/docs/Web/API/Document/domain) property gets/sets the domain portion of the origin of the current document, as used by the same-origin policy.

According to [W3C](https://www.w3.org/TR/DOM-Level-2-HTML/html.html#ID-2250147) the `Document.domain` property should be read-only. 

Firefox doesn't allow setting this property and throws a SecurityError, but Chrome, Safari, and Edge (Webkit) allow it. In those browsers, the property can't be set to a random value, it must match the suffix of the initial domain. So if the initial value is `my.domain.com` the domain value that can be set is `domain.com` because that is the suffix. 

The distortion doesn't allow code in a sandbox to change the domain of the root document even if the browser allows it.
### Distorted Behavior

On Firefox the distortion throws an Error instead of SecurityError. 

On Chrome, Safari and Edge (Webkit) it throws an Error instead of allowing the setter to execute.
<hr>
<a name="documentdocsexeccommand-valuemd"></a>

## Document.prototype.execCommand

When an HTML document has been switched to `designMode`, its `document` object exposes an [`execCommand()`](https://developer.mozilla.org/en-US/docs/Web/API/Document/execCommand) method to run commands that manipulate the current editable region, such as form inputs or `contentEditable` elements. 

The `insertHTML` command inserts new elements on the currently active editable element. 

Lightning Web Security runs in the main window, where the `<html>`, `<head>` and `<body>` elements are shared. If malicious code can insert any specified text as HTML into the DOM tree, even outside of the shared `<head>` and `<body>` elements, it can pollute the DOM. For this reason, any elements added to this shared DOM are sanitized to strip out malicious code.
### Distorted Behavior

This distortion sanitizes the inserted HTML string.
<hr>
<a name="documentdocsopen-valuemd"></a>

## Document.open

The [`document.open()`](https://developer.mozilla.org/en-US/docs/Web/API/Document/open) method opens a document for writing.

The `document.open()` method normally takes no arguments. However, there is a lesser-known variation: if you pass three arguments, `document.open()` acts as an alias for `window.open()`. This new window context is not sandboxed properly and malicious code can access system mode, so Lightning Web Security must apply a distortion to prevent such access.

### Distorted Behavior

When `document.open()` is invoked with three arguments, the distortion returns an artificial `window` object that contains safe methods.
<hr>
<a name="elementdocsafter-valuemd"></a>

## Element.prototype.after

The [`Element.prototype.after()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/after) method inserts a set of `Node` objects or `DOMString` objects after the `Element`. `DOMString` objects are inserted as equivalent `Text` nodes. 

Lightning Web Security runs in the main window, where the `<html>`, `<head>` and `<body>` elements are shared. Malicious code can add nodes or text after those shared elements, corrupting the DOM of the current rendered page.

### Distorted Behavior

This distortion allows only a `<script>` or `<link>` element to be added after `<html>`, `<head>`, and `<body>` elements. It throws an exception if any other element is specified. <hr>
<a name="elementdocsappend-valuemd"></a>

## Element.prototype.append

### Summary

The [`Element.prototype.append()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/append) method inserts a set of `Node` objects or `DOMString` objects after the last child of the `Element`. `DOMString` objects are inserted as equivalent `Text` nodes.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can append nodes or text directly to those shared elements, corrupting the DOM of the current rendered page.


### Distorted Behavior

This distortion allows only a `<script>` or `<link>` element to be added after `<html>`, `<head>`, and `<body>` elements. It throws an exception if any other element is specified.<hr>
<a name="elementdocsattachshadow-valuemd"></a>

## Element.prototype.attachShadow setter

The [`Element.prototype.attachShadow()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/attachShadow) method attaches a shadow DOM tree to the specified element and returns a reference to its `ShadowRoot`.

When the `attachShadow()` method provides an options object with `mode` set to `open`, the shadow DOM is exposed to the scripting environment. Other namespaces then have access to the shadow DOM.

### Distorted Behavior

This distortion throws an exception when the `mode` value is not `closed`, which prevents exposing the shadow DOM and also guards against additional modes potentially added later.
<hr>
<a name="elementdocsattributes-gettermd"></a>

## Element.prototype.attributes getter

The [`Element.prototype.attributes`](https://developer.mozilla.org/en-US/docs/Web/API/Element/attributes) property returns a live collection of all attribute nodes registered to the specified node. It is a `NamedNodeMap`, not an `Array`, so it has no `Array` methods and the `Attr` nodes' indexes may differ among browsers. 

The `attributes` collection can be used to set and remove attributes on an element. 

The distortion on this getter doesn't alter its functionality. It pairs an `Element` instance with a `NamedNodeMap` instance so that other distortions on `NamedNodeMap.prototype` can retrieve the element.

### Distorted Behavior

No distorted behavior.
<hr>
<a name="elementdocsbefore-valuemd"></a>

## Element.prototype.before

The [`Element.prototype.before()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/before) method inserts a set of `Node` objects or `DOMString` objects before the `Element` in the child list of the parent of the `Element`. `DOMString` objects are inserted as equivalent `Text` nodes. 

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can add nodes or text before those shared elements, corrupting the DOM of the current rendered page.

### Distorted Behavior

This distortion allows only a `<script>` or `<link>` element to be added after `<html>`, `<head>`, and `<body>` elements. It throws an exception if any other element is specified.<hr>
<a name="elementdocsblocked-propertiesmd"></a>

## Fullscreen API: Element.prototype

The [Fullscreen API](https://developer.mozilla.org/en-US/docs/Web/API/Fullscreen_API) adds methods to present a specific `Element` (and its descendants) in full-screen mode, and to exit full-screen mode when it is no longer needed. This API makes it possible to present desired content such as an online game, using the user's entire screen. Full-screen mode removes all browser user interface elements and other applications from the screen until full-screen mode is shut off.

It is supported by all major browsers, with varying implementations.

This API doesn't adjust the DOM in the element. Instead, the native fullscreen hooks onto the browser. Malicious code can use the fullscreen API for phishing attacks. For example, because the fullscreen API obscures the browser's address bar, malicious code can hide the fake URL of a phishing page. Malicious coders can also fake an address bar with their own DOM. 

### Distorted Behavior

This distortion prevents code from requesting full screen by 
blocking these properties from `Element.prototype` on specified browsers:

* `onfullscreenchange` [Chrome, Edge, Firefox]
* `onfullscreenerror` [Chrome, Edge, Firefox]
* `requestFullscreen` [Chrome, Edge, Firefox]
* `webkitRequestFullScreen` [Chrome, Edge, Safari]
* `webkitRequestFullscreen` [Chrome, Edge, Safari]
* `mozRequestFullScreen` [Firefox]<hr>
<a name="elementdocsinnerhtml-settermd"></a>

## Element.prototype.innerHTML setter

The [`Element.prototype.innerHTML`](https://developer.mozilla.org/en-US/docs/Web/API/Element/innerHTML) property gets or sets the HTML or XML markup contained within the element. 

You can set `Element.prototype.innerHTML` to replace DOM inside the element with nodes parsed from the given specified text as HTML. 

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can replace the DOM of the `<head>` and `<body>` elements, corrupting the DOM.

### Distorted Behavior

This distortion sanitizes and prevents HTML from replacing the DOM within shared `<head>` and `<body>` elements.
<hr>
<a name="elementdocsinsertadjacentelement-valuemd"></a>

## Element.prototype.insertAdjacentElement

The [`Element.prototype.insertAdjacentElement()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/insertAdjacentElement) method inserts a given element node at a given position relative to the element it is invoked upon.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can be added to those elements by using the `insertAdjacentElement()` method, corrupting the DOM of the current rendered page. 

### Distorted Behavior

This distortion sanitizes HTML to prevent malicious code from being added to the `<html>`, `<head>`, and `<body>` shared elements.<hr>
<a name="elementdocsinsertadjacenthtml-valuemd"></a>

## Element.prototype.insertAdjacentHTML

The [`Element.prototype.insertAdjacentHTML()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/insertAdjacentHTML) method parses the specified text as HTML or XML and inserts the resulting nodes into the DOM tree at a specified position. 

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can be added to those elements by using the `insertAdjacentHTML()` method, corrupting the DOM of the current rendered page. 

### Distorted Behavior

This distortion sanitizes the text string to prevent malicious code from being added to the `<html>`, `<head>`, and `<body>` shared elements.<hr>
<a name="elementdocsouterhtml-settermd"></a>

## Element.prototype.outerHTML setter

The [`Element.prototype.outerHTML`](https://developer.mozilla.org/en-US/docs/Web/API/Element/outerHTML)  property gets or sets the serialized HTML fragment describing the element including its descendants. It can also be set to replace the element with nodes parsed from the given string.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can replace the `<head>` and `<body>` elements, corrupting the DOM.

### Distorted Behavior

This distortion sanitizes and prevents HTML from replacing the shared `<head>` and `<body>` elements.
<hr>
<a name="elementdocsprepend-valuemd"></a>

## Element.prototype.prepend

The [`Element.prototype.prepend()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/prepend) method inserts a set of `Node` objects or `DOMString` objects after the last child of the `Element`. `DOMString` objects are inserted as equivalent `Text` nodes.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can prepend nodes or text directly to shared `<head>` and `<body>` elements, corrupting the DOM of the current rendered page.

### Distorted Behavior

This distortion allows only a `<script>` or `<link>` element to be prepended to `<head>` and `<body>` elements. It throws an exception if any other element is specified.
<hr>
<a name="elementdocsremove-valuemd"></a>

## Element.prototype.remove

The [`Element.prototype.remove()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/remove) method removes the element from the tree it belongs to. 

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can remove any of the shared elements, corrupting the DOM of the current rendered page. 

### Distorted Behavior

This distortion prevents removing shared elements `<html>`, `<head>`, and `<body>`.
<hr>
<a name="elementdocsreplacechildren-valuemd"></a>

## Element.prototype.replaceChildren

The [`Element.prototype.replaceChildren()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/replaceChildren) method replaces the existing children of a `Node` with a specified new set of children. These can be `DOMString` or `Node` objects. 

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can replace those elements, or the children of those elements, corrupting the DOM of the current rendered page. 

### Distorted Behavior

This distortion prevents replacing all child elements of shared elements `<html>`, `<head>`, and `<body>`.
<hr>
<a name="elementdocsreplacewith-valuemd"></a>

## Element.prototype.replaceWith

The [`Element.prototype.replaceWith()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/replaceWith) method replaces this `Element` in the children list of its parent with a set of `Node` or `DOMString` objects. `DOMString` objects are inserted as equivalent `Text` nodes. 

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can replace those elements, corrupting the DOM of the current rendered page. 

### Distorted Behavior

This distortion prevents replacing shared elements `<html>`, `<head>`, and `<body>`.
<hr>
<a name="elementdocssetattribute-family-apismd"></a>

## Element.prototype.setAttribute*

Distortions for these methods use internal registries to invoke other distortions for specific property names.

 - [`Element.prototype.setAttribute()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/setAttribute) sets the value of an attribute on the specified element. If the attribute already exists, the value is updated; otherwise a new attribute is added with the specified name and value.
 - [`Element.prototype.setAttributeNS()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/setAttributeNS) adds a new attribute or changes the value of an attribute with the given namespace and name.
 - [`Element.prototype.setAttributeNode()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/setAttributeNode) adds a new `Attr` node to the specified element.
 - [`Element.prototype.setAttributeNodeNS()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/setAttributeNodeNS) adds a new namespaced attribute node to an element.
 

The `setAttribute*` distortions themselves defend against shape-shifting objects. Shape-shifting objects don't affect native DOM APIs because values are automatically coerced. However, shape-shifting attacks can attempt to bypass Lightning Web Security distortions.

This example explains a shape-shifting attack.

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

Because Lightning Web Security distorts `setAttribute` and the value is read at least twice (once by LWS and once by the native API), LWS can mistakenly determine that the value is `'foo'` and it's safe to pass through. However, at the second read of `attrValue` its value is `'import'`. 



 Pseudo code explanation:
```text
code in sandbox calls setAttribute with shape-shifting object
    Lightning Web Security reads first returned value and caches it in a local variable
        value 'foo' is cached and further checks rely on it
    Lightning Web Security uses cached value to determine if this is forbidden
        'foo' is allowed, execution is handled to native API using .call(obj, arguments)
    nativeApi coerces the argument to a string and sets it on the element
        shape-shifting occurs and the second read now returns 'import'

```

The `setAttribute` distortion sanitizes the passed value to prevent shape-shifting attacks. 

The `setAttributeNode` distortion checks that the passed attribute argument is indeed an instance of `Attr`. No actual validation happens and the getter utilities automatically detect if this is not an instance of `Attr`. The value property of the attribute is coerced to a string.

### Distorted Behavior

- Arguments are sanitized to prevent shape-shifting attacks.
- The behavior varies according to the invoked registered distortion.
- When no distortions are registered, behavior seems like native behavior.<hr>
<a name="elementdocsshadowroot-gettermd"></a>

## Element.prototype.shadowRoot getter

The [`Element.prototype.shadowRoot`](https://developer.mozilla.org/en-US/docs/Web/API/Element/shadowRoot) read-only property represents the shadow root hosted by the element.

This property allows retrieving the shadow DOM of custom elements created with `attachShadow({mode: 'open'})`. 

In a sandbox, the distortion for `attachShadow()` prevents code from creating elements with `mode: 'open'`, but doesn't prevent code that's running outside a sandbox from creating custom elements in `open` mode. Elements that are passed as function arguments or queried from the Light DOM or shadow DOM are at risk. 
### Distorted Behavior

This distortion returns `null` when you try to access the `shadowRoot` property on a Light DOM element.<hr>
<a name="eventdocscomposedpath-valuemd"></a>

## Event.prototype.composedPath

The `Event.prototype.composedPath` method returns the event's path which is an array of objects on which listeners will be invoked. This does not include nodes in shadow trees if the shadow root was created with its `ShadowRoot.mode` closed.

### Distorted Behavior

This method returns the event’s path which is an array of the objects on which listeners will be invoked, up to the closed custom element itself, but not including the shadow root, or nodes inside the shadow root.
<hr>
<a name="htmlelementdocsblocked-propertiesmd"></a>

## HTMLElement.prototype.nonce

This distortion blocks access to `HTMLElement.prototype.nonce` in Chrome, Edge.

In Lightning Web Security, we do not allow the use of inline scripts. If a malicious user has access to the nonce value, the user may use it to bypass the Content Security Policy used to determine whether a given script will be allowed to proceed. Therefore, allowing them to run inline scripts.

## WindowEventHandlers: HTMLElement.prototype

This distortion blocks access to `HTMLElement.prototype.onrejectionhandled` and `HTMLElement.prototype.onunhandledrejection` in Safari.

This event "onrejectionhandled" is sent to the script's global scope whenever a Promise is rejected but after the promise rejection has been handled. In tandem, the event "onunhandledrejection" is sent whenever a Promise is rejected but there is no handler for the rejection. While most events are DOM related, this Promise related event handler receives an event object containing information about the rejected promise. The type, promise, and reason properties are still available in both event handlers. A malicious user could look into the promise info, which is why this needs to be blocked.
<hr>
<a name="htmlelementdocsinnertext-settermd"></a>

## HTMLElement.prototype.innerText setter [Chrome, Edge, Opera, Safari]

### Summary

The innerText property of the HTMLElement interface represents the "rendered" text content of a node and its descendants. As a setter, it can be used to replace the rendered content of the element. Since Lightning Web Security runs in the main window, where the `<html>`, `<head>` and `<body>` elements are shared, malicious code could replace the contents of those elements by assigning a new value to the `.innerText` property, corrupting the DOM of the current rendered page.  

### Distorted Behavior

This distortion sanitizes and prevents text from replacing the text within the shared elements: `<html>`, `<head>` and `<body>`.
<hr>
<a name="htmlelementdocsoutertext-settermd"></a>

## Element.prototype.outerText  setter [Chrome, Edge, Opera, Safari]

### Summary

This property allows users to replace the element with his text. In Lightning Web Security, we share the HEAD and BODY. This will allow a malicious user to replace the HEAD and BODY with his text. Therefore, corrupting the DOM.

### Distorted Behavior

This distortion sanitizes and prevents text from replacing the shared elements: HEAD and BODY.

Note that `outerText` [is not a standard property](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/outerText#Browser_compatibility), so the descriptor could be undefined, like in the case of Firefox. In this case, this distortion does nothing.
<hr>
<a name="htmlelementdocsstyle-gettermd"></a>

## HTMLElement.prototype.style getter [Chrome, Edge, Opera, Safari]

### Summary

The `style` property on any HTMLElement object allows manipulating CSS styles via JavaScript via assignments (e.g. `element.style.color = 'red'`). Any property set on this object will reflect in the DOM via the `style` attribute on an element, making this object "magical" because of this behavior.

### Distorted Behavior

This distortion alters the getter of the style property for any HTMLElement. The `style` object is being marked as live such that
any properties changed from within the sandbox are reflected on the DOM.

Furthermore, this distortion does not cover a possible but highly improbable scenario: code passing the style object from system mode to the sandbox via function arguments. The distortion will not apply since the getter has been invoked in system mode. The resulting effect is that sandboxed code will not see changes to `style` being reflected in the DOM. If this scenario does happen then the distortion should be upgraded to a patch on the raw `HTMLElement.prototype` in native window.
<hr>
<a name="htmlframeelementdocscontentdocument-gettermd"></a>

## HTMLFrameElement.prototype.contentDocument getter

To reduce the surface area of possible exploit we return `null` for the
`contentDocument` property of frames. At a later time we may explore multi
document support, but in the interest of simplicity and moving things along
we have decided to keep things simple.

### Goal

- Do not expose the real raw `contentDocument`

### Design

The value of `contentDocument` may be `null` so we enforce that it is.

### Distorted Behavior

- Always return `null` for `contentDocument`
<hr>
<a name="htmlframeelementdocscontentwindow-gettermd"></a>

## HTMLFrameElement.prototype.contentWindow getter

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

### Distorted Behavior
- Return an artificial `contentWindow` object per frame
- Cache the artificial `contentWindow` object for subsequent accesses
<hr>
<a name="htmliframeelementdocscontentdocument-gettermd"></a>

## HTMLIFrameElement.prototype.contentDocument getter

To reduce the surface area of possible exploit we return `null` for the
`contentDocument` property of iframes. At a later time we may explore multi
document support, but in the interest of simplicity and moving things along
we have decided to keep things simple.

### Goal

- Do not expose the real raw `contentDocument`

### Design

The value of `contentDocument` may be `null` so we enforce that it is.

### Distorted Behavior

- Always return `null` for `contentDocument`
<hr>
<a name="htmliframeelementdocscontentwindow-gettermd"></a>

## HTMLIFrameElement.prototype.contentWindow getter

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

### Distorted Behavior
- Return an artificial `contentWindow` object per iframe
- Cache the artificial `contentWindow` object for subsequent accesses
<hr>
<a name="htmliframeelementdocssrc-settermd"></a>

## HTMLIFrameElement.prototype.src setter

Restrict supported src values to those that sanitize to http:// and https://
schemes.

### Goal
- Prevent URL schemes like javascript://

### Design

Only allow `src` values with validated schemes to be set.

### Distorted Behavior
- Log a console warning for HTMLIFrameElement.src values that don't sanitize
  to http:// or https:// schemes
<hr>
<a name="htmlobjectelementdocscontentdocument-gettermd"></a>

## HTMLObjectElement.prototype.contentDocument getter

To reduce the surface area of possible exploit we return `null` for the
`contentDocument` property of object elements. At a later time we may explore
multi document support, but in the interest of simplicity and moving things along
we have decided to keep things simple.

### Goal

- Do not expose the real raw `contentDocument`

### Design

The value of `contentDocument` may be `null` so we enforce that it is.

### Distorted Behavior

- Always return `null` for `contentDocument`
<hr>
<a name="htmlobjectelementdocscontentwindow-gettermd"></a>

## HTMLObjectElement.prototype.contentWindow getter

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

### Distorted Behavior
- Return an artificial `contentWindow` object per object element
- Cache the artificial `contentWindow` object for subsequent accesses
<hr>
<a name="htmlscriptelementdocssrc-gettermd"></a>

## HTMLScriptElement.prototype.src getter

The setter distortion for the script element works by setting the original url to a different attribute named `data-distorted-src`, while the src attribute points to a distorted value we never reveal in the sandbox. When accessing the getter in the sandbox we need to get the original value thus the getter needs to look for the value on `data-distorted-src`. There are scenarios when a script tag may already be present in the DOM, inserted by the system through some other mechanisms. In this scenario we'll need to fallback to the original `src` attribute.

### Goal

- To mimic native behavior on retrieving `src` attribute value.

### Design

- Patch the getter of `HTMLScriptElement.prototype.src` to retrieve the value from `data-distorted-src` instead of `src` attribute. In case there was no distorted value set and there was already a value set on the `src` attribute, retrieve the value from the `src` attribute.

### Distorted Behavior

- The getter will return the value of `data-distorted-src` when code in the sandbox tries to access `src` attribute on a script element.
<hr>
<a name="htmlscriptelementdocssrc-settermd"></a>

## HTMLScriptElement.prototype.src setter

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

### Distorted Behavior

- Store original value on `data-distorted-src`, store distorted value on `src`. 
- The behavior will seem native like to code running in the sandbox.
<hr>
<a name="messageeventdocssource-gettermd"></a>

## MessageEvent.prototype.source getter

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

### Distorted Behavior
- Return an artificial `window` object for source.
- Cache the artificial `window` object for subsequent accesses.
<hr>
<a name="namednodemapdocssetnameditem-valuemd"></a>

## NamedNodeMap.prototype.setNamedItem

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

### Distorted Behavior

- if no distortion is found for an Attr instance then proceed with native invocation of setNamedItem
- if a distortion exists then the distorted behavior is relative to what that distortion does
<hr>
<a name="navigatordocsserviceworker-gettermd"></a>

## Navigator.prototype.serviceWorker getter

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

### Distorted Behavior

Each time code accesses `navigator.serviceWorker` property, this distortion will return `undefined`.
<hr>
<a name="nodedocsappendchild-valuemd"></a>

## Node.prototype.appendChild

### Summary

> The [`appendChild()`](https://developer.mozilla.org/en-US/docs/Web/API/Node/appendChild) method of the `Node` interface adds a node to the end of the list of children of a specified parent node. If the given child is a reference to an existing node in the document, `appendChild()` moves it from its current position to the new position (there is no requirement to remove the node from its parent node before appending it to some other node).

Since Lightning Web Security runs in the main window, where the `<html>`, `<head>` and `<body>` elements are shared, malicious code could append a child directly to those shared elements, corrupting the DOM of the current rendered page.

### Distorted Behavior

This distortion throws if the child being appending to a shared element is _anything but_ a `<script>` or `<link>` element.
<hr>
<a name="nodedocstextcontent-settermd"></a>

## Node.prototype.textContent setter

### Summary

This property allows users to replace DOM inside the element with his text. In Lightning Web Security, we share the HEAD and BODY. This will allow a malicious user to replace the DOM of the HEAD and BODY with his text. Therefore, corrupting the DOM.

### Distorted Behavior

This distortion sanitizes and prevents text from replacing the DOM within shared elements: HEAD and BODY.
<hr>
<a name="rangedocscreatecontextualfragment-valuemd"></a>

## Range.prototype.createContextualFragment

### Summary

The Range.createContextualFragment() method returns a DocumentFragment by invoking the HTML fragment parsing algorithm or the XML fragment parsing algorithm with the start of the range as the context node. This range of HTML elements can be added to the DOM tree.

In Lightning Web Security, we share the HEAD and BODY. Even though it doesn't corrupt the existing elements inside or outside the element, if a malicious user can insert specified text as HTML into the DOM tree outside of the shared elements, it gives them the ability to pollute the DOM. We need to sanitize any elements added to this shared DOM.

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

#### Distorted Behavior for setAttributeNS
```js
const el = document.createElementNS('http://www.w3.org/2000/svg', 'use');

el.setAttributeNS('http://www.w3.org/1999/xlink', 'href', '/myresource.svg#circle');
console.log(el.getAttributeNS('http://www.w3.org/1999/xlink', 'href')); // httpmycurrenthostmyresourcesvg_circle

// OR for xlink:href
el.setAttributeNS('hhttp://www.w3.org/1999/xlink', 'xlink:href', '/myresource.svg#circle');
console.log(el.getAttributeNS('http://www.w3.org/1999/xlink', 'href')); // httpmycurrenthostmyresourcesvg_circle
console.log(el.getAttributeNS('http://www.w3.org/1999/xlink', 'xlink:href')); // null
```

#### Distorted Behavior for setAttributeNodeNS
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

## ServiceWorkerContainer.prototype

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

### Distorted Behavior

This distortion will throw a `TypeError` whenever any of the `ServiceWorkerContainer.prototype` properties or methods is accessed.
<hr>
<a name="shadowrootdocsinnerhtml-settermd"></a>

## ShadowRoot.prototype.innerHTML setter

### Summary

The innerHTML property of the ShadowRoot interface sets or returns a reference to the DOM tree inside the ShadowRoot. Malicious users can add script tags that would run without being sanitized.

### Distorted Behavior

This distortion sanitizes the string provided to the innerHTML setter.
<hr>
<a name="shadowrootdocsmode-gettermd"></a>

## ShadowRoot.prototype.mode getter

### Goal

 - To force a reported mode of 'closed'.

### Design

- Patch getter on `ShadowRoot.prototype.mode` descriptor to return `'closed'`.

### Distorted Behavior

- Each time code accesses `mode` property on any element with an attached shadow
  DOM this distortion will return `'closed'`.
<hr>
<a name="sharedworkerdocsconstructor-valuemd"></a>

## SharedWorker Global Constructor

### Summary

The `SharedWorker()` constructor creates a SharedWorker object that executes the script at the specified URL. This script must obey the same-origin policy. Malicious users can execute script at a specified URL to bypass Lightning Web Security evaluation rules. 

### Distorted Behavior

Lightning Web Security will throw a `RangeError` when calling the constructor. Lightning Web Security will block access to `SharedWorker.prototype`.<hr>
<a name="storagedocsclear-valuemd"></a>

## Storage.prototype.clear

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

## Storage.prototype.getItem

### Summary

The Storage interface provides access to the a particular domain's session or local storage. It allows the addition, modification, or deletion of stored data items which is shared in system mode.

In order for one sandbox not to retrieve the storage of another sandbox, we must create a synthetic storage for each sandbox.

### Distorted Behavior

This distortion retrieves data items from its synthetic storage.<hr>
<a name="storagedocskey-valuemd"></a>

## Storage.prototype.key

### Summary

The Storage interface provides access to the a particular domain's session or local storage. It allows the addition, modification, or deletion of stored data items which is shared in system mode.

The key() method of the Storage interface, when passed a number n, returns the name of the nth key in a given Storage object. The order of keys is user-agent defined, so you should not rely on it. Therefore, it is okay to have the storage items out of order.

### Distorted Behavior

This distortion retrieves a key value at a specific index from its synthetic storage.<hr>
<a name="storagedocslength-gettermd"></a>

## Storage.prototype.length getter

### Summary

The Storage interface provides access to the a particular domain's session or local storage. It allows the addition, modification, or deletion of stored data items which is shared in system mode.

In order for one sandbox not to retrieve the storage of another sandbox, we must create a synthetic storage for each sandbox. When looking at length, we must retrieve the number of data items in the synthetic storage rather than the system mode storage.

### Distorted Behavior

This distortion retrieves the number of data items in its synthetic storage.<hr>
<a name="storagedocsremoveitem-valuemd"></a>

## Storage.prototype.removeItem

### Summary

The Storage interface provides access to the a particular domain's session or local storage. It allows the addition, modification, or deletion of stored data items which is shared in system mode.

Since each sandbox uses it's own synthetic storage, we cannot allow a malicious user to clear a data item from another sandbox.

### Distorted Behavior

This distortion deletes a data item from its synthetic storage.<hr>
<a name="storagedocssetitem-valuemd"></a>

## Storage.prototype.setItem

### Summary

The Storage interface provides access to the a particular domain's session or local storage. It allows the addition, modification, or deletion of stored data items which is shared in system mode.

In order for one sandbox not to modify the storage of another sandbox, we must create a synthetic storage for each sandbox.

### Distorted Behavior

This distortion adds or modifies data items in its synthetic storage.<hr>
<a name="urldocscreateobjecturl-valuemd"></a>

## URL.createObjectURL

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

### Distorted Behavior

- For any HTML like MIME types used with Blob/File objects that try to load malicious content, the API will throw the error `Lightning Web Security: Cannot "createObjectURL" using a unsecure [object Blob]!`
- For any non-recognized MIME types the API will throw the error `Unsupported MIME type.`
- All commonly used and non-malicious MIME types will not be affected.
- All Blob/Files using html like MIME types which do not represent a threat will be allowed.
- On HTML like MIME types we enforce charset=utf-8 to prevent exploits where browser auto interprets charset and special characters that can lead to XSS.
- Empty MIME types on File and Blob objects will automatically be normalized to 'text/plain' since browsers treat this differently.
<hr>
<a name="windowdocsfetch-valuemd"></a>

## Window.fetch

### Goal

To prevent users from making requests to disallowed endpoints.

### Design

Patch the `Window.fetch` property and intercept calls to it to block disallowed URLs.

### Distorted Behavior

The `Window.fetch` distortion examines the `hostname` and the `pathname` of the URL, and if it matches one of the disallowed entries, it rejects the promise.

### Disallowed endpoints

Lightning Web Security disallows endpoints:

- Containing `"/aura"` in the URL.
- Containing `"/webruntime"` in the URL.

At the moment this is hard coded, but in the future this will be a configuration option.
<hr>
<a name="windowdocsframes-gettermd"></a>

## window.frames getter

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

## window.length getter

### Summary

The Window interface's `length` property returns the number of frames (either `<frame>` or `<iframe>` elements) attached to the `window`'s `document`.

### Distorted Behavior

The Window interface's `length` property always returns `0`. Application code must use the `window.frames.length` value and `window.frames` object to iterate over the list of frames (either `<frame>` or `<iframe>` elements) attached to the `document`.
<hr>
<a name="windowdocsopen-valuemd"></a>

## Window.prototype.open

### Summary

The `open` method, loads the specified resource into a new or existing browsing context with the specified name. If the name doesn't exist, then a new browsing context is opened in a new tab or a new window, and the specified resource is loaded into it. This new context is not sandboxed properly and malicious users can access system mode.

### Distorted Behavior

Lightning Web Security will return an artificial `Window` object that contains specific safe methods we allow.
<hr>
<a name="windowdocsopener-gettermd"></a>

## window.opener getter

### Summary

The Window interface's `opener` property returns a reference to the window that opened the window, either with open(), or by navigating a link with a target attribute.

In other words, if window A opens window B, B.opener returns A.

### Distorted Behavior

Lightning Web Security will return an artificial `Window` object that contains specific safe methods we allow.
<hr>
<a name="windowdocsparent-gettermd"></a>

## window.parent getter

### Summary

The Window interface's `parent` property returns a reference to the parent of the current window or subframe. If a window does not have a parent, its parent property is a reference to itself. If window A embeds window B, B.parent returns A.

### Distorted Behavior

Lightning Web Security will return a patched `Window` object that contains specific safe methods we allow.<hr>
<a name="windowdocssetinterval-valuemd"></a>

## Window.prototype.setInterval

### Summary

The `setInterval` method, repeatedly calls a function or executes a code snippet, with a fixed time delay between each call. But `setInterval` supports string evaluation by specifying a string for its first argument. This escapes the sandbox.

### Distorted Behavior

If the first argument provided to `setInterval` is a string value, this distortion evaluates it in the sandbox.<hr>
<a name="windowdocssettimeout-valuemd"></a>

## window.setTimeout

### Summary

The `setTimeout` method, repeatedly calls a function or executes a code snippet, with a fixed time delay between each call. But `setTimeout` supports string evaluation by specifying a string for its first argument. This escapes the sandbox.

### Distorted Behavior

If the first argument provided to `setTimeout` is a string value, this distortion evaluates it in the sandbox.
<hr>
<a name="workerdocsconstructor-valuemd"></a>

## Worker Global Constructor

### Summary

The `Worker()` constructor creates a Worker object that executes the script at the specified URL. This script must obey the same-origin policy. Malicious users can execute script at a specified URL to bypass Lightning Web Security evaluation rules. 

### Distorted Behavior

Lightning Web Security will throw a `RangeError` when calling the constructor. Lightning Web Security will block access to `Worker.prototype`.
<hr>
<a name="xmlhttprequestdocsopen-valuemd"></a>

## XMLHttpRequest.open

### Goal

To prevent users from making requests to disallowed endpoints.

### Design

Patch the `XMLHttpRequest.open` property and intercept calls to it to block disallowed URLs.

### Distorted Behavior

The `XMLHttpRequest.open` distortion examines the `hostname` and the `pathname` of the URL, and if it matches one of the disallowed entries, it throws an error.

### Disallowed endpoints

Lightning Web Security disallows endpoints:

- Containing `"/aura"` in the URL.
- Containing `"/webruntime"` in the URL.

At the moment this is hard coded, but in the future this will be a configuration option.
<hr>
<a name="xmlhttprequestdocsresponse-gettermd"></a>

## XMLHttpRequest.prototype.response getter

### Summary

The XMLHttpRequest response property returns the response's body content as an ArrayBuffer, Blob, Document, JavaScript Object, or DOMString, depending on the value of the request's responseType property. 

If the responses's body content is a Document, we need to sanitize the Document, otherwise malicious code can add script tags that would run without being sanitized.

### Distorted Behavior

This distortion sanitizes the XMLHttpRequest response property value.
<hr>
<a name="xmlhttprequestdocsresponsexml-gettermd"></a>

## XMLHttpRequest.prototype.responseXML getter

### Summary

The XMLHttpRequest.responseXML read-only property returns a Document containing the HTML or XML retrieved by the request; or null if the request was unsuccessful, has not yet been sent, or if the data can't be parsed as XML or HTML. We need to sanitize the Document, otherwise malicious code can add script tags that would run without being sanitized.

### Distorted Behavior

This distortion sanitizes the XMLHttpRequest responseXML property value.
