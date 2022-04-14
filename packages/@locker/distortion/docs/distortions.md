# Lightning Web Security Distortions

This is the list of the currently implemented distortions.

Version: 0.15.16<br>
Generated: Apr 13, 2022

## Table of Contents

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Attr.prototype.value setter](#attrprototypevalue-setter)
  - [Distorted Behavior](#distorted-behavior)
- [CSSStyleRule.prototype.style getter](#cssstyleruleprototypestyle-getter)
  - [Distorted Behavior](#distorted-behavior-1)
- [CacheStorage.prototype.delete](#cachestorageprototypedelete)
  - [Distorted Behavior](#distorted-behavior-2)
- [CacheStorage.prototype.has](#cachestorageprototypehas)
  - [Distorted Behavior](#distorted-behavior-3)
- [CacheStorage.prototype.keys](#cachestorageprototypekeys)
  - [Distorted Behavior](#distorted-behavior-4)
- [CacheStorage.prototype.match](#cachestorageprototypematch)
  - [Distorted Behavior](#distorted-behavior-5)
- [CacheStorage.prototype.open](#cachestorageprototypeopen)
  - [Distorted Behavior](#distorted-behavior-6)
- [CookieStore.prototype.addEventListener](#cookiestoreprototypeaddeventlistener)
  - [Distorted Behavior](#distorted-behavior-7)
- [CookieStore.prototype.delete](#cookiestoreprototypedelete)
  - [Distorted Behavior](#distorted-behavior-8)
- [CookieStore.prototype.get](#cookiestoreprototypeget)
  - [Distorted Behavior](#distorted-behavior-9)
- [CookieStore.prototype.getAll](#cookiestoreprototypegetall)
  - [Distorted Behavior](#distorted-behavior-10)
- [CookieStore.prototype.onchange setter](#cookiestoreprototypeonchange-setter)
  - [Distorted Behavior](#distorted-behavior-11)
- [CookieStore.prototype.set](#cookiestoreprototypeset)
  - [Distorted Behavior](#distorted-behavior-12)
- [CustomElementRegistry.prototype.define](#customelementregistryprototypedefine)
  - [Distorted Behavior](#distorted-behavior-13)
- [CustomElementRegistry.prototype.get](#customelementregistryprototypeget)
  - [Distorted Behavior](#distorted-behavior-14)
- [DOMParser.prototype.parseFromString](#domparserprototypeparsefromstring)
  - [Distorted Behavior](#distorted-behavior-15)
- [Document.prototype.cookie getter](#documentprototypecookie-getter)
  - [Distorted Behavior](#distorted-behavior-16)
- [Document.prototype.cookie setter](#documentprototypecookie-setter)
  - [Distorted Behavior](#distorted-behavior-17)
- [Document.prototype.domain setter](#documentprototypedomain-setter)
  - [Distorted Behavior](#distorted-behavior-18)
- [Document.prototype.execCommand](#documentprototypeexeccommand)
  - [Distorted Behavior](#distorted-behavior-19)
- [Document.prototype.open](#documentprototypeopen)
  - [Distorted Behavior](#distorted-behavior-20)
- [Document.prototype.replaceChildren](#documentprototypereplacechildren)
  - [Distorted Behavior](#distorted-behavior-21)
- [Element.prototype.after](#elementprototypeafter)
  - [Distorted Behavior](#distorted-behavior-22)
- [Element.prototype.append](#elementprototypeappend)
  - [Summary](#summary)
  - [Distorted Behavior](#distorted-behavior-23)
- [Element.prototype.attachShadow](#elementprototypeattachshadow)
  - [Distorted Behavior](#distorted-behavior-24)
- [Element.prototype.attributes getter](#elementprototypeattributes-getter)
  - [Distorted Behavior](#distorted-behavior-25)
- [Element.prototype.before](#elementprototypebefore)
  - [Distorted Behavior](#distorted-behavior-26)
- [Fullscreen API: Element.prototype](#fullscreen-api-elementprototype)
  - [Distorted Behavior](#distorted-behavior-27)
- [Element.prototype.innerHTML setter](#elementprototypeinnerhtml-setter)
  - [Distorted Behavior](#distorted-behavior-28)
- [Element.prototype.insertAdjacentElement](#elementprototypeinsertadjacentelement)
  - [Distorted Behavior](#distorted-behavior-29)
- [Element.prototype.insertAdjacentHTML](#elementprototypeinsertadjacenthtml)
  - [Distorted Behavior](#distorted-behavior-30)
- [Element.prototype.outerHTML setter](#elementprototypeouterhtml-setter)
  - [Distorted Behavior](#distorted-behavior-31)
- [Element.prototype.prepend](#elementprototypeprepend)
  - [Distorted Behavior](#distorted-behavior-32)
- [Element.prototype.remove](#elementprototyperemove)
  - [Distorted Behavior](#distorted-behavior-33)
- [Element.prototype.replaceChildren](#elementprototypereplacechildren)
  - [Distorted Behavior](#distorted-behavior-34)
- [Element.prototype.replaceWith](#elementprototypereplacewith)
  - [Distorted Behavior](#distorted-behavior-35)
- [Element.prototype.setAttribute*](#elementprototypesetattribute)
  - [Distorted Behavior](#distorted-behavior-36)
- [Element.prototype.shadowRoot getter](#elementprototypeshadowroot-getter)
  - [Distorted Behavior](#distorted-behavior-37)
- [Event.prototype.composedPath](#eventprototypecomposedpath)
  - [Distorted Behavior](#distorted-behavior-38)
- [HTMLElement.prototype.onrejectionhandled and HTMLElement.prototype.onunhandledrejection [Safari]](#htmlelementprototypeonrejectionhandled-and-htmlelementprototypeonunhandledrejection-safari)
  - [Distorted Behavior](#distorted-behavior-39)
- [HTMLElement.prototype.nonce](#htmlelementprototypenonce)
  - [Distorted Behavior](#distorted-behavior-40)
- [HTMLElement.prototype.dataset getter](#htmlelementprototypedataset-getter)
  - [Distorted Behavior](#distorted-behavior-41)
- [HTMLElement.prototype.innerText setter](#htmlelementprototypeinnertext-setter)
  - [Distorted Behavior](#distorted-behavior-42)
- [HTMLElement.prototype.outerText setter](#htmlelementprototypeoutertext-setter)
  - [Distorted Behavior](#distorted-behavior-43)
- [HTMLElement.prototype.style getter](#htmlelementprototypestyle-getter)
  - [Distorted Behavior](#distorted-behavior-44)
- [HTMLFrameElement.prototype.contentDocument getter](#htmlframeelementprototypecontentdocument-getter)
  - [Distorted Behavior](#distorted-behavior-45)
- [HTMLFrameElement.prototype.contentWindow getter](#htmlframeelementprototypecontentwindow-getter)
  - [Distorted Behavior](#distorted-behavior-46)
- [HTMLIFrameElement.prototype.contentDocument getter](#htmliframeelementprototypecontentdocument-getter)
  - [Distorted Behavior](#distorted-behavior-47)
- [HTMLIFrameElement.prototype.contentWindow getter](#htmliframeelementprototypecontentwindow-getter)
  - [Distorted Behavior](#distorted-behavior-48)
- [HTMLIFrameElement.prototype.src setter](#htmliframeelementprototypesrc-setter)
  - [Distorted Behavior](#distorted-behavior-49)
- [HTMLLinkElement.prototype.rel setter](#htmllinkelementprototyperel-setter)
  - [Distorted Behavior](#distorted-behavior-50)
- [HTMLLinkElement.prototype.relList setter](#htmllinkelementprototyperellist-setter)
  - [Distorted Behavior](#distorted-behavior-51)
- [HTMLObjectElement.prototype.contentDocument getter](#htmlobjectelementprototypecontentdocument-getter)
  - [Distorted Behavior](#distorted-behavior-52)
- [HTMLObjectElement.prototype.contentWindow getter](#htmlobjectelementprototypecontentwindow-getter)
  - [Distorted Behavior](#distorted-behavior-53)
- [HTMLScriptElement.prototype.src getter](#htmlscriptelementprototypesrc-getter)
  - [Distorted Behavior](#distorted-behavior-54)
- [HTMLScriptElement.prototype.src setter](#htmlscriptelementprototypesrc-setter)
  - [Distorted Behavior](#distorted-behavior-55)
- [History.prototype.pushState](#historyprototypepushstate)
  - [Distorted Behavior](#distorted-behavior-56)
- [History.prototype.replaceState](#historyprototypereplacestate)
  - [Distorted Behavior](#distorted-behavior-57)
- [MessageEvent.prototype.source getter](#messageeventprototypesource-getter)
  - [Distorted Behavior](#distorted-behavior-58)
- [NamedNodeMap.prototype.setNamedItem](#namednodemapprototypesetnameditem)
  - [Distorted Behavior](#distorted-behavior-59)
- [NamedNodeMap.prototype.setNamedItemNS](#namednodemapprototypesetnameditemns)
  - [Distorted Behavior](#distorted-behavior-60)
- [Navigator.sendBeacon()](#navigatorsendbeacon)
  - [Distorted Behavior](#distorted-behavior-61)
- [Navigator.prototype.serviceWorker getter](#navigatorprototypeserviceworker-getter)
  - [Distorted Behavior](#distorted-behavior-62)
- [Node.prototype.appendChild](#nodeprototypeappendchild)
  - [Distorted Behavior](#distorted-behavior-63)
- [Node.prototype.insertBefore](#nodeprototypeinsertbefore)
  - [Distorted Behavior](#distorted-behavior-64)
- [Node.prototype.removeChild](#nodeprototyperemovechild)
  - [Distorted Behavior](#distorted-behavior-65)
- [Node.prototype.replaceChild](#nodeprototypereplacechild)
  - [Distorted Behavior](#distorted-behavior-66)
- [Node.prototype.textContent setter](#nodeprototypetextcontent-setter)
  - [Distorted Behavior](#distorted-behavior-67)
- [Notification Constructor](#notification-constructor)
  - [Distorted Behavior](#distorted-behavior-68)
- [Range.prototype.createContextualFragment](#rangeprototypecreatecontextualfragment)
  - [Distorted Behavior](#distorted-behavior-69)
- [Range.prototype.deleteContents](#rangeprototypedeletecontents)
  - [Distorted Behavior](#distorted-behavior-70)
- [Range.prototype.extractContents](#rangeprototypeextractcontents)
  - [Distorted Behavior](#distorted-behavior-71)
- [Range.prototype.insertNode](#rangeprototypeinsertnode)
  - [Distorted Behavior](#distorted-behavior-72)
- [SVGAnimateElement: `attributeName` attribute](#svganimateelement-attributename-attribute)
  - [Distorted Behavior](#distorted-behavior-73)
- [SVGAnimateElement: `from` attribute](#svganimateelement-from-attribute)
  - [Distorted Behavior](#distorted-behavior-74)
- [SVGAnimateElement: `to` attribute](#svganimateelement-to-attribute)
  - [Distorted Behavior](#distorted-behavior-75)
- [SVGAnimateElement: `values` attribute](#svganimateelement-values-attribute)
  - [Distorted Behavior](#distorted-behavior-76)
- [SVGElement.prototype.nonce](#svgelementprototypenonce)
  - [Distorted Behavior](#distorted-behavior-77)
- [SVGElement.prototype.dataset getter](#svgelementprototypedataset-getter)
  - [Distorted Behavior](#distorted-behavior-78)
- [SVGScriptElement.prototype.href](#svgscriptelementprototypehref)
  - [Distorted Behavior](#distorted-behavior-79)
- [SVGSetElement: `attributeName` attribute](#svgsetelement-attributename-attribute)
  - [Distorted Behavior](#distorted-behavior-80)
- [SVGSetElement: `to` attribute](#svgsetelement-to-attribute)
  - [Distorted Behavior](#distorted-behavior-81)
- [SVGUseElement: `href` attribute](#svguseelement-href-attribute)
  - [Distorted Behavior](#distorted-behavior-82)
  - [Distorted Behavior for setAttribute](#distorted-behavior-for-setattribute)
  - [Distorted Behavior for setAttributeNode](#distorted-behavior-for-setattributenode)
  - [Distorted Behavior for setAttributeNS](#distorted-behavior-for-setattributens)
- [ServiceWorkerContainer.prototype](#serviceworkercontainerprototype)
  - [Distorted Behavior](#distorted-behavior-83)
- [ShadowRoot.prototype.innerHTML setter](#shadowrootprototypeinnerhtml-setter)
  - [Distorted Behavior](#distorted-behavior-84)
- [ShadowRoot.prototype.mode getter](#shadowrootprototypemode-getter)
  - [Distorted Behavior](#distorted-behavior-85)
- [SharedWorker Constructor](#sharedworker-constructor)
  - [Distorted Behavior](#distorted-behavior-86)
- [Storage.prototype.clear](#storageprototypeclear)
  - [Distorted Behavior](#distorted-behavior-87)
- [Storage API: Storage.prototype](#storage-api-storageprototype)
  - [Distorted Behavior](#distorted-behavior-88)
- [Storage.prototype.getItem](#storageprototypegetitem)
  - [Distorted Behavior](#distorted-behavior-89)
- [Storage.prototype.key](#storageprototypekey)
  - [Distorted Behavior](#distorted-behavior-90)
- [Storage.prototype.length getter](#storageprototypelength-getter)
  - [Distorted Behavior](#distorted-behavior-91)
- [Storage.prototype.removeItem](#storageprototyperemoveitem)
  - [Distorted Behavior](#distorted-behavior-92)
- [Storage.prototype.setItem](#storageprototypesetitem)
  - [Distorted Behavior](#distorted-behavior-93)
- [TrustedTypePolicyFactory.createPolicy](#trustedtypepolicyfactorycreatepolicy)
  - [Distorted Behavior](#distorted-behavior-94)
- [URL.createObjectURL](#urlcreateobjecturl)
  - [Distorted Behavior](#distorted-behavior-95)
- [Window.fetch](#windowfetch)
  - [Distorted Behavior](#distorted-behavior-96)
- [window.frames getter](#windowframes-getter)
  - [Distorted Behavior](#distorted-behavior-97)
- [Window.prototype.getComputedStyle](#windowprototypegetcomputedstyle)
  - [Distorted Behavior](#distorted-behavior-98)
- [window.length getter](#windowlength-getter)
  - [Distorted Behavior](#distorted-behavior-99)
- [WindowEventHandlers.onstorage](#windoweventhandlersonstorage)
  - [Distorted Behavior](#distorted-behavior-100)
- [window.open](#windowopen)
  - [Distorted Behavior](#distorted-behavior-101)
- [window.opener getter](#windowopener-getter)
  - [Distorted Behavior](#distorted-behavior-102)
- [window.parent getter](#windowparent-getter)
  - [Distorted Behavior](#distorted-behavior-103)
- [Window.prototype.postMessage](#windowprototypepostmessage)
  - [Distorted Behavior](#distorted-behavior-104)
- [window.setInterval](#windowsetinterval)
  - [Distorted Behavior](#distorted-behavior-105)
- [window.setTimeout](#windowsettimeout)
  - [Distorted Behavior](#distorted-behavior-106)
- [Window.prototype.structuredClone](#windowprototypestructuredclone)
  - [Distorted Behavior](#distorted-behavior-107)
- [Worker Constructor](#worker-constructor)
  - [Distorted Behavior](#distorted-behavior-108)
- [XMLHttpRequest.prototype.open](#xmlhttprequestprototypeopen)
  - [Distorted Behavior](#distorted-behavior-109)
- [XMLHttpRequest.prototype.response getter](#xmlhttprequestprototyperesponse-getter)
  - [Distorted Behavior](#distorted-behavior-110)
- [XMLHttpRequest.prototype.responseXML getter](#xmlhttprequestprototyperesponsexml-getter)
  - [Distorted Behavior](#distorted-behavior-111)
- [XSLTProcessor.prototype.transformToDocument](#xsltprocessorprototypetransformtodocument)
  - [Distorted Behavior](#distorted-behavior-112)
- [XSLTProcessor.prototype.transformToDocument](#xsltprocessorprototypetransformtodocument-1)
  - [Distorted Behavior](#distorted-behavior-113)
- [XSLTProcessor.prototype.transformToFragment](#xsltprocessorprototypetransformtofragment)
  - [Distorted Behavior](#distorted-behavior-114)
- [XSLTProcessor.prototype.transformToFragment](#xsltprocessorprototypetransformtofragment-1)
  - [Distorted Behavior](#distorted-behavior-115)

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
<a name="cssstyleruledocsstyle-gettermd"></a>

## CSSStyleRule.prototype.style getter

The [`CSSStyleRule.prototype.style`](https://developer.mozilla.org/en-US/docs/Web/API/CSSStyleRule/style) read-only property is the `CSSStyleDeclaration` interface for the declaration block of the `CSSStyleRule`.

The `style` property of a `CSSStyleRule` object lets you manipulate CSS styles with JavaScript by using  assignments. For example, you could change a style sheet rule's text color using `document.styleSheets[0].cssRules[0].style.color = 'red'`.

### Distorted Behavior

This distortion alters the getter of the `style` property for any `CSSStyleRule`. The `style` object is marked as live so that its native behavior is preserved and any properties changed from within the sandbox are also reflected in the DOM.
<hr>
<a name="cachestoragedocsdelete-valuemd"></a>

## CacheStorage.prototype.delete

The [`CacheStorage.prototype.delete()`](https://developer.mozilla.org/en-US/docs/Web/API/CacheStorage/delete) method of the `CacheStorage` interface finds the `Cache` object matching the `cacheName`, and if found, deletes the `Cache` object and returns a `Promise` that resolves to `true`. If no `Cache` object is found, it resolves to `false`.

If malicious code can access any cache object on a page, it can arbitrarily replace or remove cache objects. This behavior can have catastrophic effects in a multi-tenant environment like Salesforce.

### Distorted Behavior

This distortion prevents deletion of cache objects outside the sandbox. Cache objects in the sandbox are protected from code outside or in other sandboxes.

The `delete()` method is restricted to cache objects created by the requesting sandbox.
<hr>
<a name="cachestoragedocshas-valuemd"></a>

## CacheStorage.prototype.has

The [`CacheStorage.prototype.has()`](https://developer.mozilla.org/en-US/docs/Web/API/CacheStorage/has) method of the `CacheStorage` interface returns a `Promise` that resolves to `true` if a `Cache` object matches the `cacheName`.

If malicious code can detect any cache object on a page, it can potentially modify cache objects. This behavior can have catastrophic effects in a multi-tenant environment like Salesforce.

### Distorted Behavior

This distortion prevents detection of cache objects outside the sandbox. Cache objects in the sandbox are protected from code outside or in other sandboxes.

The `has()` method is restricted to cache objects created by the requesting sandbox.
<hr>
<a name="cachestoragedocskeys-valuemd"></a>

## CacheStorage.prototype.keys

The [`CacheStorage.prototype.keys()`](https://developer.mozilla.org/en-US/docs/Web/API/CacheStorage/keys) method of the `CacheStorage` interface returns a `Promise` that will resolve with an array containing strings corresponding to all of the named `Cache` objects tracked by the `CacheStorage` object in the order they were created. Use this method to iterate over a list of all `Cache` objects.

If malicious code can access any cache object on a page, it can arbitrarily replace or remove cache objects. This behavior can have catastrophic effects in a multi-tenant environment like Salesforce.

### Distorted Behavior

This distortion prevents access to cache objects outside the sandbox. Cache objects in the sandbox are protected from code outside or in other sandboxes.

The `keys()` method is restricted to cache objects created by the requesting sandbox.
<hr>
<a name="cachestoragedocsmatch-valuemd"></a>

## CacheStorage.prototype.match

The [`CacheStorage.prototype.match()`](https://developer.mozilla.org/en-US/docs/Web/API/CacheStorage/match) method of the `CacheStorage` interface checks if a given `Request` or url string is a key for a stored `Response`. This method returns a `Promise` for a `Response`, or a `Promise` which resolves to `undefined` if no match is found.

If malicious code can access any cache object on a page, it can arbitrarily replace or remove cache objects. This behavior can have catastrophic effects in a multi-tenant environment like Salesforce.

### Distorted Behavior

This distortion requires `caches.match()` calls to include the second `options` argument and provide an explicit `cacheName` property value.

The `match()` method rejects the promise if `options` is omitted, or if the `cacheName` property of `options` is omitted.
<hr>
<a name="cachestoragedocsopen-valuemd"></a>

## CacheStorage.prototype.open

The [`CacheStorage.prototype.open()`](https://developer.mozilla.org/en-US/docs/Web/API/CacheStorage/open) method of the `CacheStorage` interface returns a `Promise` that resolves to the `Cache` object matching `cacheName`.

If malicious code can access any cache object on a page, it can arbitrarily replace or remove cache objects. This behavior can have catastrophic effects in a multi-tenant environment like Salesforce.

### Distorted Behavior

This distortion prevents access to cache objects outside the sandbox. Cache objects in the sandbox are protected from code outside or in other sandboxes.

The `open()` method is restricted to cache objects created by the requesting sandbox.
<hr>
<a name="cookiestoredocsaddeventlistener-valuemd"></a>

## CookieStore.prototype.addEventListener

The [`CookieStore.prototype.addEventListener()`](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener) method of the `EventTarget` interface sets up a function that will be called whenever the specified event is delivered to the target.

Common targets are `Element`, or its children, `Document`, and `Window`, but the target may be any object that supports events (such as `XMLHttpRequest`).

This distortion prevents code from accessing cookies outside of the sandbox.

### Distorted Behavior

Lightning Web Security does not support the `change` event of `CookieStore` objects. Calls to `CookieStore.prototype.addEventListener()` for the `change` event throw an exception.
<hr>
<a name="cookiestoredocsdelete-valuemd"></a>

## CookieStore.prototype.delete

The [`CookieStore.prototype.delete()`](https://developer.mozilla.org/en-US/docs/Web/API/CookieStore/delete) method of the `CookieStore` interface deletes a cookie with the given name or options object.

If malicious code deletes cookies on a page, it could remove login cookies and make the app unusable. This distortion protects cookies outside the sandbox from `CookieStore.prototype.delete` and limits what can be deleted within the sandbox. Cookies in the sandbox are protected from code outside or in other sandboxes.

### Distorted Behavior

The distortion only permits deletion of sandbox cookies.

<hr>
<a name="cookiestoredocsget-valuemd"></a>

## CookieStore.prototype.get

The [`CookieStore.prototype.get()`](https://developer.mozilla.org/en-US/docs/Web/API/CookieStore/get) method of the `CookieStore` interface returns a single cookie with the given name or options object.

If malicious code can access any cookie on a page, it can issue XHR requests impersonating the user who's logged in. This behavior can have catastrophic effects in a multi-tenant environment like Salesforce.

This distortion protects the value of `CookieStore.prototype.get` and limits the view to what is being retrieved from within the sandbox. Cookies in the sandbox are protected from code outside or in other sandboxes.

### Distorted Behavior

The `get()` method returns only sandbox cookies.

<hr>
<a name="cookiestoredocsgetall-valuemd"></a>

## CookieStore.prototype.getAll

The [`CookieStore.prototype.getAll()`](https://developer.mozilla.org/en-US/docs/Web/API/CookieStore/getAll) method of the `CookieStore` interface returns a list of cookies that match the name or options passed to it. Passing no parameters will return all cookies for the current context.

If malicious code can access all cookies on a page, it can issue XHR requests impersonating the user who's logged in. This behavior can have catastrophic effects in a multi-tenant environment like Salesforce.

This distortion protects the value of `CookieStore.prototype.getAll` and limits the view to what is being retrieved from within the sandbox. Cookies in the sandbox are protected from code outside or in other sandboxes.

### Distorted Behavior

The `getAll()` method returns only sandbox cookies.
<hr>
<a name="cookiestoredocsonchange-settermd"></a>

## CookieStore.prototype.onchange setter

The [`CookieStore.prototype.onchange()`](https://developer.mozilla.org/en-US/docs/Web/API/CookieStore/onchange) event handler of the `CookieStore` interface fires when a change is made to any cookie.

This distortion prevents code from accessing cookies outside of the sandbox.

### Distorted Behavior

Currently, Lightning Web Security doesn't support the `CookieStore.onchange` event, so setting the `onchange` property is not allowed and returns an error.
<hr>
<a name="cookiestoredocsset-valuemd"></a>

## CookieStore.prototype.set

The [`CookieStore.prototype.set()`](https://developer.mozilla.org/en-US/docs/Web/API/CookieStore/set) method of the `CookieStore` interface sets a cookie with the given name and value or options object.

Distortion of `CookieStore.prototype.set` is required so `CookieStore.prototype.get` can retrieve sandbox cookies that are similarly distorted with the sandbox prefix.

This distortion also prevents malicious code from accessing system cookies that Salesforce uses to function. Otherwise any sandbox can send malicious payloads to the backend using cookies.

### Distorted Behavior

The `set()` method automatically adds the sandbox prefix to keys for sandbox cookies.
<hr>
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

## Document.prototype.open

The [`document.open()`](https://developer.mozilla.org/en-US/docs/Web/API/Document/open) method opens a document for writing.

The `document.open()` method normally takes no arguments. However, there is a lesser-known variation: if you pass three arguments, `document.open()` acts as an alias for `window.open()`. This new window context is not sandboxed properly and malicious code can access system mode, so Lightning Web Security must apply a distortion to prevent such access.

### Distorted Behavior

When `document.open()` is invoked with three arguments, the distortion returns an artificial `window` object that contains safe methods.
<hr>
<a name="documentdocsreplacechildren-valuemd"></a>

## Document.prototype.replaceChildren

The [`Document.prototype.replaceChildren()`](https://developer.mozilla.org/en-US/docs/Web/API/Document/replaceChildren) method replaces the existing children of a `Document` with a specified new set of children.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can replace all the shared elements, corrupting the DOM of the current rendered page.

### Distorted Behavior

This distortion disallows replacing the children of top level `document`.
<hr>
<a name="elementdocsafter-valuemd"></a>

## Element.prototype.after

The [`Element.prototype.after()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/after) method inserts a set of `Node` objects or `DOMString` objects after the `Element`. `DOMString` objects are inserted as equivalent `Text` nodes.

Lightning Web Security runs in the main window, where the `<html>`, `<head>` and `<body>` elements are shared. Malicious code can add nodes or text after those shared elements, corrupting the DOM of the current rendered page.

### Distorted Behavior

This distortion allows only a `<script>` or `<link>` element to be added after `<html>`, `<head>`, and `<body>` elements. It throws an exception if any other element is specified.
<hr>
<a name="elementdocsappend-valuemd"></a>

## Element.prototype.append

### Summary

The [`Element.prototype.append()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/append) method inserts a set of `Node` objects or `DOMString` objects after the last child of the `Element`. `DOMString` objects are inserted as equivalent `Text` nodes.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can append nodes or text directly to those shared elements, corrupting the DOM of the current rendered page.


### Distorted Behavior

This distortion allows only a `<script>` or `<link>` element to be added after `<html>`, `<head>`, and `<body>` elements. It throws an exception if any other element is specified.<hr>
<a name="elementdocsattachshadow-valuemd"></a>

## Element.prototype.attachShadow

The [`Element.prototype.attachShadow()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/attachShadow) method attaches a shadow DOM tree to the specified element and returns a reference to its `ShadowRoot`.

When the `attachShadow()` method provides an options object with `mode` set to `open`, the shadow DOM is exposed to the scripting environment. Other namespaces then have access to the shadow DOM.

### Distorted Behavior

This distortion throws an exception when the `mode` value is not `closed`, which prevents exposing the shadow DOM and also guards against additional modes potentially added later.
<hr>
<a name="elementdocsattributes-gettermd"></a>

## Element.prototype.attributes getter

The [`Element.prototype.attributes`](https://developer.mozilla.org/en-US/docs/Web/API/Element/attributes) property returns a live collection of all attribute nodes registered to the specified node. It is a `NamedNodeMap`, not an `Array`, so it has no `Array` methods and the `Attr` nodes' indexes may differ among browsers.

The `attributes` collection can be used to set and remove attributes on an element.

The distortion on this getter doesn't alter its functionality. It pairs an `Element` instance with a `NamedNodeMap` instance so that the  distortion on `NamedNodeMap.prototype.setNamedItem` can retrieve the element.

### Distorted Behavior

No distorted behavior.
<hr>
<a name="elementdocsbefore-valuemd"></a>

## Element.prototype.before

The [`Element.prototype.before()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/before) method inserts a set of `Node` objects or `DOMString` objects before the `Element` in the child list of the parent of the `Element`. `DOMString` objects are inserted as equivalent `Text` nodes.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can add nodes or text before those shared elements, corrupting the DOM of the current rendered page.

### Distorted Behavior

This distortion allows only a `<script>` or `<link>` element to be added after `<html>`, `<head>`, and `<body>` elements. It throws an exception if any other element is specified.
<hr>
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
* `mozRequestFullScreen` [Firefox]
<hr>
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

This distortion sanitizes HTML to prevent malicious code from being added to the `<html>`, `<head>`, and `<body>` shared elements.
<hr>
<a name="elementdocsinsertadjacenthtml-valuemd"></a>

## Element.prototype.insertAdjacentHTML

The [`Element.prototype.insertAdjacentHTML()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/insertAdjacentHTML) method parses the specified text as HTML or XML and inserts the resulting nodes into the DOM tree at a specified position.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can be added to those elements by using the `insertAdjacentHTML()` method, corrupting the DOM of the current rendered page.

### Distorted Behavior

This distortion sanitizes the text string to prevent malicious code from being added to the `<html>`, `<head>`, and `<body>` shared elements.
<hr>
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
 - [`Element.prototype.toggleAttribute()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/toggleAttribute) toggles a Boolean attribute (removing it if it is present and adding it if it is not present) on the given element.


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
- When no distortions are registered, behavior seems like native behavior.
<hr>
<a name="elementdocsshadowroot-gettermd"></a>

## Element.prototype.shadowRoot getter

The [`Element.prototype.shadowRoot`](https://developer.mozilla.org/en-US/docs/Web/API/Element/shadowRoot) read-only property represents the shadow root hosted by the element.

This property allows retrieving the shadow DOM of custom elements created with `attachShadow({mode: 'open'})`.

In a sandbox, the distortion for `attachShadow()` prevents code from creating elements with `mode: 'open'`, but doesn't prevent code that's running outside a sandbox from creating custom elements in `open` mode. Elements that are passed as function arguments or queried from the Light DOM or shadow DOM are at risk.
### Distorted Behavior

This distortion returns `null` when you try to access the `shadowRoot` property on a Light DOM element.
<hr>
<a name="eventdocscomposedpath-valuemd"></a>

## Event.prototype.composedPath

The [`Event.prototype.composedPath()`](https://developer.mozilla.org/en-US/docs/Web/API/Event/composedPath) method returns the event's path which is an array of objects on which listeners will be invoked. This does not include nodes in shadow trees if the shadow root was created with its `ShadowRoot.mode` closed.

### Distorted Behavior

This distortion returns an array of the objects on which listeners will be invoked, up to the closed custom element itself. The array doesn't include the shadow root, or nodes inside the shadow root.
<hr>
<a name="htmlelementdocsblocked-properties-onrejectionhandledmd"></a>

## HTMLElement.prototype.onrejectionhandled and HTMLElement.prototype.onunhandledrejection [Safari]

The [`WindowEventHandlers`](https://developer.mozilla.org/en-US/docs/Web/API/WindowEventHandlers) mixin describes the event handlers common to several interfaces like `Window`, or `HTMLBodyElement` and `HTMLFrameSetElement`. Each of these interfaces can implement additional specific event handlers.

The [`WindowEventHandlers.onrejectionhandled`](https://developer.mozilla.org/en-US/docs/Web/API/WindowEventHandlers/onrejectionhandled) property is an event handler representing the code to be called when the `rejectionhandled` event is raised, indicating that a Promise was rejected and the rejection has been handled. The event is sent to the script's global scope.

The [`WindowEventHandlers.onunhandledrejection`](https://developer.mozilla.org/en-US/docs/Web/API/WindowEventHandlers/onunhandledrejection) property is an event handler representing the code to be called when the `unhandledrejection` event is raised, indicating that a Promise was rejected but the rejection was not handled. The code handles the event that's sent to the script's global scope when a Promise is rejected, and there is no handler for the rejection.

While most events are DOM related, these event handlers receive an event object containing information about the rejected promise, including the `type`, `promise`, and `reason` properties. Malicious code that accesses the event handler properties can look into the promise info.

### Distorted Behavior

This distortion blocks access to `HTMLElement.prototype.onrejectionhandled` and `HTMLElement.prototype.onunhandledrejection` in Safari.

<hr>
<a name="htmlelementdocsblocked-propertiesmd"></a>

## HTMLElement.prototype.nonce

The [`HTMLElement.prototype.nonce`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/nonce) property returns an element's cryptographic nonce (number used once) that is used by Content Security Policy to determine whether a given fetch will be allowed to proceed.

Lightning Web Security doesn't allow the use of inline scripts even when a nonce is used. Malicious code with access to the `nonce` value can use it to bypass the Content Security Policy that determines whether a given script is allowed to proceed, and then run inline scripts.

### Distorted Behavior

This distortion blocks access to `HTMLElement.prototype.nonce` in Chrome, Edge.<hr>
<a name="htmlelementdocsdataset-gettermd"></a>

## HTMLElement.prototype.dataset getter

The [`HTMLElement.prototype.dataset`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/dataset) read-only property of the HTMLElement interface provides read/write access to custom data attributes (`data-*`) on elements. It exposes a map of strings (`DOMStringMap`) with an entry for each `data-*` attribute.

### Distorted Behavior

This distortion alters the getter of the `dataset` property for any `HTMLElement`. The `dataset` object is marked as live such that any properties changed from within the sandbox are reflected in the DOM.
<hr>
<a name="htmlelementdocsinnertext-settermd"></a>

## HTMLElement.prototype.innerText setter

The [`HTMLElement.prototype.innerText`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/innerText) property of represents the "rendered" text content of a node and its descendants. As a setter, it can be used to replace the rendered content of the element.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can replace the contents of those elements by assigning a new value to the `.innerText` property, corrupting the DOM of the current rendered page.

### Distorted Behavior

This distortion sanitizes the given text and prevents it from replacing the text within the shared elements `<html>`, `<head>`, and `<body>`.
<hr>
<a name="htmlelementdocsoutertext-settermd"></a>

## HTMLElement.prototype.outerText setter

[`HTMLElement.prototype.outerText`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/outerText) is a non-standard property. As a getter, it returns the same value as `HTMLElement.prototype.innerText`. As a setter, it removes the current node and replaces it with the given text.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can replace the `<head>` and `<body>` elements, corrupting the DOM.

### Distorted Behavior

This distortion sanitizes the given text and prevents it from replacing the shared elements `<head>` and `<body>`.

As a non-standard property, the `outerText` descriptor could be undefined. Firefox doesn't support the property, so the distortion does nothing in that browser.
<hr>
<a name="htmlelementdocsstyle-gettermd"></a>

## HTMLElement.prototype.style getter

The [`HTMLElement.prototype.style`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) read-only property returns the inline style of an element in the form of a `CSSStyleDeclaration` object that contains a list of all styles properties for that element with values assigned for the attributes that are defined in the element's inline `style` attribute.

The `style` property of an `HTMLElement` object lets you manipulate CSS styles with JavaScript by using assignments. For example, you could change an element's text color using `element.style.color = 'red'`.

A property set on a `HTMLElement` object reflects in the DOM via the `style` attribute on an element.

### Distorted Behavior

This distortion alters the getter of the `style` property of an `HTMLElement`. The `style` object is marked as live so that its native behavior is preserved and any properties changed from within the sandbox are also reflected in the DOM.
<hr>
<a name="htmlframeelementdocscontentdocument-gettermd"></a>

## HTMLFrameElement.prototype.contentDocument getter

The `HTMLFrameElement.prototype.contentDocument` property getter returns the `Document` object of the specified frame.
The `HTMLFrameElement` interface is deprecated in HTML5.

To reduce the possibility of exploit, Lightning Web Security returns `null` for the `HTMLFrameElement.prototype.contentDocument` property.
### Distorted Behavior

This distortion returns `null` for `contentDocument`.
<hr>
<a name="htmlframeelementdocscontentwindow-gettermd"></a>

## HTMLFrameElement.prototype.contentWindow getter

The `HTMLFrameElement.prototype.contentWindow` property returns the `Window` object of the specified frame. You can use this `Window` object to access the frame's document and its internal DOM. This attribute is read-only, but its properties can be manipulated like the global `Window` object. The `HTMLFrameElement` interface is deprecated in HTML5.

To reduce the possibility of exploit, Lightning Web Security creates an artificial `contentWindow` object that allows access to a reduced set of properties.
  - `close`
  - `closed`
  - `focus`
  - `opener`
  - `parent`
  - `postMessage`
### Distorted Behavior

This distortion returns an artificial `contentWindow` object per frame and caches the artificial `contentWindow` object for subsequent accesses.
<hr>
<a name="htmliframeelementdocscontentdocument-gettermd"></a>

## HTMLIFrameElement.prototype.contentDocument getter

The [`HTMLIFrameElement.contentDocument`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLIFrameElement/contentDocument) property getter returns a `Document` corresponding to the active document in the inline frame's nested browsing context if the iframe and the iframe's parent document are Same Origin. Otherwise, the property returns `null`.

To reduce the possibility of exploit, Lightning Web Security returns `null` for the `contentDocument` property, even when an iframe and the iframe's parent document have the same origin.

### Distorted Behavior

This distortion returns `null` for `contentDocument`.
<hr>
<a name="htmliframeelementdocscontentwindow-gettermd"></a>

## HTMLIFrameElement.prototype.contentWindow getter

The [`HTMLIFrameElement.prototype.contentWindow`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLIFrameElement/contentWindow) property returns the `Window` object of an `HTMLIFrameElement`. You can use this `Window` object to access the iframe's document and its internal DOM. This attribute is read-only, but its properties can be manipulated like the global `Window` object.

To reduce the possibility of exploit, Lightning Web Security creates an artificial `contentWindow` object that allows access to a reduced set of properties.
  - `close`
  - `closed`
  - `focus`
  - `opener`
  - `parent`
  - `postMessage`

### Distorted Behavior

This distortion returns an artificial `contentWindow` object per iframe and caches the artificial `contentWindow` object for subsequent accesses.<hr>
<a name="htmliframeelementdocssrc-settermd"></a>

## HTMLIFrameElement.prototype.src setter

The [`HTMLIFrameElement.prototype.src`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLIFrameElement/src) property reflects the HTML `referrerpolicy` attribute of the `<iframe>` element defining which referrer is sent when fetching the resource. The `src` value is a string that reflects the `src` HTML attribute, containing the address of the content to be embedded.

Lightning Web Security sanitizes the `src` value and only permits `http://` and `https://` schemes. URL schemes like `javascript://` aren't allowed.

### Distorted Behavior

This distortion logs a console warning for `HTMLIFrameElement.src` values that don't sanitize to `http://` or `https://` schemes.
<hr>
<a name="htmllinkelementdocsrel-settermd"></a>

## HTMLLinkElement.prototype.rel setter

The [`HTMLLinkElement.rel`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLLinkElement/rel) property is a `DOMString` containing a space-separated list of link types indicating the relationship between the resource represented by the `<link>` element and the current document.

Malicious code can set `rel` to the value `import`, which allows it to import script resources that can bypass Lightning Web Security distortions and access the raw window.

To reduce the possibility of exploit, Lightning Web Security prevents setting the `import` value to the `rel` property of link elements.

### Distorted Behavior

This distortion prevents code from setting the `rel` property value to `import`.
<hr>
<a name="htmllinkelementdocsrellist-settermd"></a>

## HTMLLinkElement.prototype.relList setter

The [`HTMLLinkElement.relList`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLLinkElement/relList) read-only property reflects the `rel` attribute. It is a live `DOMTokenList` containing the set of link types indicating the relationship between the resource represented by the `<link>` element and the current document. The property itself is read-only, meaning you can substitute the `DOMTokenList` by another one, but the content of the returned list can't be changed.

Malicious code can set `rel` to the value `import`, which allows it to import script resources that can bypass Lightning Web Security distortions and access the raw window.

To reduce the possibility of exploit, Lightning Web Security prevents setting the `import` value to the `rel` property of link elements.


### Distorted Behavior

This distortion prevents code from setting the `relList` property value to `import`.
<hr>
<a name="htmlobjectelementdocscontentdocument-gettermd"></a>

## HTMLObjectElement.prototype.contentDocument getter

The [`HTMLObjectElement.prototype.contentDocument`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLObjectElement/contentDocument) read-only property returns a `Document` representing the active document of the object element's nested browsing context, if any; otherwise null.

To reduce the possibility of exploit, Lightning Web Security returns `null` for the `contentDocument` property of object elements.

### Distorted Behavior

This distortion returns `null` for `contentDocument`.
<hr>
<a name="htmlobjectelementdocscontentwindow-gettermd"></a>

## HTMLObjectElement.prototype.contentWindow getter

The [`HTMLObjectElement.prototype.contentWindow`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLObjectElement/contentWindow) property returns a `WindowProxy` representing the window proxy of the object element's nested browsing context, if any; otherwise null.

To reduce the possibility of exploit, Lightning Web Security creates an artificial `contentWindow` object that allows access to a reduced set of properties.
  - `close`
  - `closed`
  - `focus`
  - `opener`
  - `parent`
  - `postMessage`

### Distorted Behavior

This distortion returns an artificial `contentWindow` object per iframe and caches the artificial `contentWindow` object for subsequent accesses.
<hr>
<a name="htmlscriptelementdocssrc-gettermd"></a>

## HTMLScriptElement.prototype.src getter

[`HTMLScriptElement.prototype.src`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLScriptElement) property is a `DOMString` representing the URL of an external script. It reflects the `src` attribute of the `<script>` element specifying the URL to an external script.

Lightning Web Security sets the original url to a different attribute named `data-distorted-src`, while the `src` attribute points to a distorted value that's not revealed in the sandbox.

Lightning Web Security's distortion for the `src` getter obtains the original value from `data-distorted-src`.

In some scenarios, a `<script>` element is already present in the DOM, inserted by the system through some other mechanisms. In these cases, LWS accesses the original `src` attribute.

### Distorted Behavior

This distortion returns the value of `data-distorted-src` when code in the sandbox tries to access `src` attribute on a `<script>` element.
<hr>
<a name="htmlscriptelementdocssrc-settermd"></a>

## HTMLScriptElement.prototype.src setter

[`HTMLScriptElement.prototype.src`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLScriptElement) property is a `DOMString` representing the URL of an external script. It reflects the `src` attribute of the `script` element specifying the URL to an external script.

To ensure that JavaScript code loaded through a `script` element runs in the sandbox, Lightning Web Security evaluates the source text in the same sandbox before the browser evaluates it. This prevents the native behavior of the `script` element from triggering.

LWS stores the value of `src` in a different attribute `data-distorted-src`. LWS fetches the script file using an XHR request and sets the `src` attribute value to a distorted value that uses the script fetched by LWS. The browser reads the distorted value of the `src` attribute which kicks off the evaluation process in the sandbox.

These steps ensure that different browsers work as expected, while preventing them from running script source before LWS can evaluate it.
### Distorted Behavior

This distortion prevents a script from running before LWS can evaluate it.
<hr>
<a name="historydocspushstate-valuemd"></a>

## History.prototype.pushState

In an HTML document, the [`History.prototype.pushState()`](https://developer.mozilla.org/en-US/docs/Web/API/History/pushState) method adds an entry to the browser's session history stack.

### Distorted Behavior

This distortion preserves the `pushState()` method's native behavior in the sandbox by ensuring that the [structured clone algorithm](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Structured_clone_algorithm) works correctly on the `state` parameter. 
<hr>
<a name="historydocsreplacestate-valuemd"></a>

## History.prototype.replaceState

The [`History.prototype.replaceState()`](https://developer.mozilla.org/en-US/docs/Web/API/History/replaceState) method modifies the current history entry, replacing it with the state object and URL passed in the method parameters. This method is particularly useful when you want to update the state object or URL of the current history entry in response to some user action.

### Distorted Behavior

This distortion preserves the `replaceState()` method's native behavior in the sandbox by ensuring that the [structured clone algorithm](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Structured_clone_algorithm) works correctly on the `state` parameter. 
<hr>
<a name="messageeventdocssource-gettermd"></a>

## MessageEvent.prototype.source getter

The [`MessageEvent.prototype.source`](https://developer.mozilla.org/en-US/docs/Web/API/MessageEvent/source) read-only
property is a `MessageEventSource` (which can be a `WindowProxy`, `MessagePort`, or `ServiceWorker` object) representing the message emitter.

If the property references a `window`, malicious code can open a new browser tab that contains a `postMessage` to the current browser. After that, the current browser can access the raw `window` without protective Lightning Web Security distortions.

To reduce the possibility of exploit, when the `source` property is a window, Lightning Web Security creates an artificial `window` object that allows access to a reduced set of properties.
  - `close`
  - `closed`
  - `focus`
  - `postMessage`

### Distorted Behavior

This distortion returns an artificial `window` object and caches the artificial `window` object for subsequent accesses.
<hr>
<a name="namednodemapdocssetnameditem-valuemd"></a>

## NamedNodeMap.prototype.setNamedItem

The [`NamedNodeMap`](https://developer.mozilla.org/en-US/docs/Web/API/NamedNodeMap) interface represents a collection of `Attr` objects. Objects inside a `NamedNodeMap` are not in any particular order, unlike `NodeList`, although they may be accessed by an index as in an array. A `NamedNodeMap` object is live and will thus be auto-updated if changes are made to its contents internally or elsewhere.

The `NamedNodeMap.prototype.setNamedItem()` method replaces or adds the `Attr` identified in the map by the given name. You can use it to set an attribute on an element, so Lightning Web Security must distort `NamedNodeMap.prototype.setNamedItem`.

This code would bypass LWS distortions for named properties and `setAttribute\*` and set the `rel` attribute on a link if `setNamedItem` is not distorted.
```js
const el = document.createElement('link');
const attr = document.createAttribute('rel');
attr.value = 'import';
el.attributes.setNamedItem(attr);
```

The `NamedNodeMap.prototype.setNamedItem` distortion works with the distortion for `Element.attributes getter` to pair elements with `NamedModeMap` instances when the getter is invoked for an attribute. Then the `NamedNodeMap.prototype.setNamedItem` distortion invokes other distortions for specific attributes.

### Distorted Behavior

If there is a distortion registered for an attribute, the behavior depends on the specific distortion. If there's no distortion registered for an attribute, the native invocation of `setNamedItem` is allowed.
<hr>
<a name="namednodemapdocssetnameditemns-valuemd"></a>

## NamedNodeMap.prototype.setNamedItemNS

The [`NamedNodeMap`](https://developer.mozilla.org/en-US/docs/Web/API/NamedNodeMap) interface represents a collection of `Attr` objects. Objects inside a `NamedNodeMap` are not in any particular order, unlike `NodeList`, although they may be accessed by an index as in an array. A `NamedNodeMap` object is live and will thus be auto-updated if changes are made to its contents internally or elsewhere.

The `NamedNodeMap.prototype.setNamedItemNS()` method replaces or adds the `Attr` identified in the map by the given name. You can use it to set an attribute on an element, so Lightning Web Security must distort `NamedNodeMap.prototype.setNamedItemNS`.

This code would bypass LWS distortions for named properties and `setAttribute\*` and set the `rel` attribute on a link if `setNamedItemNS` is not distorted.
```js
const el = document.createElement('link');
const attr = document.createAttribute('rel');
attr.value = 'import';
el.attributes.setNamedItemNS(attr);
```

The `NamedNodeMap.prototype.setNamedItemNS` distortion works with the distortion for `Element.attributes getter` to pair elements with `NamedModeMap` instances when the getter is invoked for an attribute. Then the `NamedNodeMap.prototype.setNamedItemNS` distortion invokes other distortions for specific attributes.

### Distorted Behavior

If there is a distortion registered for an attribute, the behavior depends on the specific distortion. If there's no distortion registered for an attribute, the native invocation of `setNamedItemNS` is allowed.
<hr>
<a name="navigatordocssendbeacon-valuemd"></a>

## Navigator.sendBeacon()

The [`navigator.sendBeacon()`](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/sendBeacon) method asynchronously sends an HTTP POST request containing a small amount of data to a web server.

Lightning Web Security disallows access to URL endpoints containing `"/aura"` and `"/webruntime"` because they are part of the Lightning Component framework.

### Distorted Behavior 

This distortion examines the `hostname` and the `pathname` of the URL. If there's a match to a disallowed endpoint, it rejects the promise. 
<hr>
<a name="navigatordocsserviceworker-gettermd"></a>

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
<hr>
<a name="nodedocsappendchild-valuemd"></a>

## Node.prototype.appendChild

The [`Node.prototype.appendChild()`](https://developer.mozilla.org/en-US/docs/Web/API/Node/appendChild) method adds a node to the end of the list of children of a specified parent node. If the given child is a reference to an existing node in the document, `appendChild()` moves it from its current position to the new position (there is no requirement to remove the node from its parent node before appending it to some other node).

Lightning Web Security runs in the main window, where the `<html>` and `<head>` elements are shared. Malicious code can append a child element directly to those shared elements, corrupting the DOM of the current rendered page.

### Distorted Behavior

This distortion allows only a `<script>` or `<link>` element to be appended as a child to `<html>` and `<head>` elements. It throws an exception if any other element is specified.<hr>
<a name="nodedocsinsertbefore-valuemd"></a>

## Node.prototype.insertBefore

The [`Node.prototype.insertBefore()`](https://developer.mozilla.org/en-US/docs/Web/API/Node/insertBefore) method of the `Node` interface inserts a node before a reference node as a child of a specified parent node.

If the given node already exists in the document, `insertBefore()` moves it from its current position to the new position. (That is, it will automatically be removed from its existing parent before appending it to the specified new parent.)

This means that a node cannot be in two locations of the document simultaneously.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can append a child element directly to those shared elements, corrupting the DOM of the current rendered page.

### Distorted Behavior

This distortion allows only a `<script>` or `<link>` element to be appended as a child to `<html>`, `<head>`, and `<body>` elements. It throws an exception if any other element is specified.
<hr>
<a name="nodedocsremovechild-valuemd"></a>

## Node.prototype.removeChild

The [`Node.prototype.removeChild()`](https://developer.mozilla.org/en-US/docs/Web/API/Node/removeChild) method of the `Node` interface removes a child node from the DOM and returns the removed node.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can remove any of the shared elements, corrupting the DOM of the current rendered page.

### Distorted Behavior

This distortion prevents removing shared elements `<html>`, `<head>`, and `<body>`.
<hr>
<a name="nodedocsreplacechild-valuemd"></a>

## Node.prototype.replaceChild

The [`Node.prototype.replaceChild()`](https://developer.mozilla.org/en-US/docs/Web/API/Node/replaceChild) method of the `Node` element replaces a child node within the given parent node.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can replace any of the shared elements, corrupting the DOM of the current rendered page.

### Distorted Behavior

This distortion prevents replacing shared elements `<html>`, `<head>`, and `<body>`.
<hr>
<a name="nodedocstextcontent-settermd"></a>

## Node.prototype.textContent setter

The [`Node.prototype.textContent`](https://developer.mozilla.org/en-US/docs/Web/API/Node/textContent) property represents the text content of the node and its descendants.

This property allows you to replace DOM inside the element with your own text.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can replace the DOM of those shared elements, corrupting the DOM of the current rendered page.

### Distorted Behavior

This distortion sanitizes the given text to prevent replacing the DOM within the shared elements `<html>`, `<head>`, and `<body>`.

<hr>
<a name="notificationdocsconstructor-valuemd"></a>

## Notification Constructor

The [`Notification()`](https://developer.mozilla.org/en-US/docs/Web/API/Notification/Notification) constructor creates a new [Notification](https://developer.mozilla.org/en-US/docs/Web/API/Notification) object instance, which represents a user notification.

### Distorted Behavior

This distortion preserves the `Notification()` constructor's native behavior in the sandbox by ensuring that the [structured clone algorithm](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Structured_clone_algorithm) works correctly on the `options.data` parameter. 
<hr>
<a name="rangedocscreatecontextualfragment-valuemd"></a>

## Range.prototype.createContextualFragment

The `Range` interface represents a fragment of a document that can contain nodes and parts of text nodes.

The [`Range.prototype.createContextualFragment()`](https://developer.mozilla.org/en-US/docs/Web/API/Range/createContextualFragment) method returns a `DocumentFragment` created from a given string of text. The string contains text and HTML tags to be converted to a document fragment.

The `createContextualFragment()` method invokes the HTML fragment parsing algorithm or the XML fragment parsing algorithm with the start of the range (the parent of the selected node) as the context node. The document fragment can be added to the DOM tree.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. The `createContextualFragment()` method can let malicious code insert specified text as HTML into the DOM tree. Although the fragment can only be inserted outside of the shared elements, it can pollute the DOM. LWS sanitizes elements added to the shared DOM.

### Distorted Behavior

This distortion sanitizes an HTML string that is used to create the `DocumentFragment`.
<hr>
<a name="rangedocsdeletecontents-valuemd"></a>

## Range.prototype.deleteContents

The `Range` interface represents a fragment of a document that can contain nodes and parts of text nodes.

The [`Range.prototype.deleteContents()`](https://developer.mozilla.org/en-US/docs/Web/API/Range/deleteContents) method removes the contents of the `Range` from the `Document`.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. The `deleteContents()` method can let malicious code remove the shared elements. LWS prevents the deletion of any shared elements.

### Distorted Behavior

This distortion prevents `deleteContents()` from removing any shared elements.
<hr>
<a name="rangedocsextractcontents-valuemd"></a>

## Range.prototype.extractContents

The `Range` interface represents a fragment of a document that can contain nodes and parts of text nodes.

The [`Range.prototype.extractContents()`](https://developer.mozilla.org/en-US/docs/Web/API/Range/extractContents) method moves contents of the `Range` from the document tree into a `DocumentFragment`.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. The `extractContents()` method can let malicious code move the shared elements. LWS prevents moving any shared elements.

### Distorted Behavior

This distortion prevents `extractContents()` from moving any shared elements.<hr>
<a name="rangedocsinsertnode-valuemd"></a>

## Range.prototype.insertNode

The [`Range.prototype.insertNode()`](https://developer.mozilla.org/en-US/docs/Web/API/Range/insertNode) method inserts a node at the start of the `Range`.

The new node is inserted at the start boundary point of the `Range`. If the new node is to be added to a text `Node`, that `Node` is split at the insertion point, and the insertion occurs between the two text nodes.

If the new node is a document fragment, the children of the document fragment are inserted instead.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. The `insertNode()` method can let malicious code move the shared elements. LWS prevents moving any shared elements.

### Distorted Behavior

This distortion allows only a `<script>` or `<link>` element to be inserted as an immediate child to `<html>`, `<head>`, and `<body>` elements. It throws an exception if any other element is specified.
<hr>
<a name="svganimateelementdocsattributename-attributemd"></a>

## SVGAnimateElement: `attributeName` attribute

The [`attributeName`](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/attributeName) attribute indicates the name of the CSS property or attribute of the target element that is going to be changed during an animation.

When you set the `attributeName` to `href`, the element accesses an SVG resource specified with the `from`, `to`, or `value` attribute. Malicious code can bypass Lightning Web Security with an `<iframe>` or `<script>` element inside the SVG resource and run code outside the sandbox. 

This distortion applies when the code sets `href` on the `attributeName` attribute after setting the `from`, `to`, or `value` attribute.

### Distorted Behavior

This distortion sanitizes SVG files that are passed with `from`, `to`, or `value` attributes of the `<animate>` element.

<hr>
<a name="svganimateelementdocsfrom-attributemd"></a>

## SVGAnimateElement: `from` attribute

The [`from`](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/From) attribute indicates the initial value of the attribute that will be modified during the animation.

When used with the `to` attribute, the animation will change the modified attribute from the `from` value to the `to` value. When used with the `by` attribute, the animation will change the attribute relatively from the `from` value by the value specified in `by`.

When you set the SVG resource dynamically with the `from` attribute, the SVG resource isn't sanitized. Malicious code can bypass Lightning Web Security with an `<iframe>` or `<script>` element inside the SVG resource and  run code outside the sandbox. 

### Distorted Behavior

This distortion sanitizes SVG files that are passed with the `from` attribute of the `<animate>` element.
<hr>
<a name="svganimateelementdocsto-attributemd"></a>

## SVGAnimateElement: `to` attribute

The [`to`](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/To) attribute indicates the final value of the attribute that will be modified during the animation.

The value of the attribute will change between the `from` attribute value and this value.

When you set the SVG resource dynamically with the `to` attribute, the SVG resource isn't sanitized. Malicious code can bypass Lightning Web Security with an `<iframe>` or `<script>` element inside the SVG resource and run code outside the sandbox. 

### Distorted Behavior

This distortion sanitizes SVG files that are passed with the `to` attribute of the `<animate>` element.

<hr>
<a name="svganimateelementdocsvalues-attributemd"></a>

## SVGAnimateElement: `values` attribute

The [`values`](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/values#animate_animatecolor_animatemotion_animatetransform) attribute provides a list of values defining the sequence of values over the course of the animation. If this attribute is specified, any `from`, `to`, and `by` attribute values set on the element are ignored.

When you set the SVG resource dynamically with the `values` attribute, the SVG resource isn't sanitized. Malicious code can bypass Lightning Web Security with an `<iframe>` or `<script>` element inside the SVG resource and run code outside the sandbox.

### Distorted Behavior

This distortion sanitizes SVG files that are passed with the `values` attribute of the `<animate>` element.
<hr>
<a name="svgelementdocsblocked-propertiesmd"></a>

## SVGElement.prototype.nonce

The [`SVGElement.prototype.nonce`](https://developer.mozilla.org/en-US/docs/Web/API/SVGElement) property returns an element's cryptographic nonce (number used once) that is used by Content Security Policy to determine whether a given fetch will be allowed to proceed.

Lightning Web Security doesn't allow the use of inline scripts even when a nonce is used. Malicious code with access to the `nonce` value can use it to bypass the Content Security Policy that determines whether a given script is allowed to proceed, and then run inline scripts.

### Distorted Behavior

This distortion blocks access to `SVGElement.prototype.nonce` in Chrome, Edge.<hr>
<a name="svgelementdocsdataset-gettermd"></a>

## SVGElement.prototype.dataset getter

The [`SVGElement.prototype.dataset`](https://developer.mozilla.org/en-US/docs/Web/API/SVGElement/dataset) read-only property of the SVGElement interface provides read/write access to custom data attributes (`data-*`) on elements. It exposes a map of strings (`DOMStringMap`) with an entry for each `data-*` attribute.

### Distorted Behavior

This distortion alters the getter of the `dataset` property for any `SVGElement`. The `dataset` object is marked as live such that any properties changed from within the sandbox are reflected in the DOM.
<hr>
<a name="svgscriptelementdocshref-attributemd"></a>

## SVGScriptElement.prototype.href

The [`SVGScriptElement.prototype.href`](https://developer.mozilla.org/en-US/docs/Web/API/SVGScriptElement) property is an `SVGAnimatedString` corresponding to the `href` or `xlink:href` attribute of the given `<script>` element.

The `SVGScriptElement.prototype.href` property reflects the `href` attribute of a `<script>` element inside an `<svg>` element, specifying the URL to an external script.

The default value for `href` is `undefined` in the `SVGScriptElement.prototype`. Access to the raw `window` object could be attained by running scripts using the SVG `<script>` element.

To ensure that JavaScript code loaded through an SVG `<script>` element runs in the sandbox, Lightning Web Security evaluates the script source in the same sandbox before the browser evaluates it. This preemptive evaluation prevents the native behavior of the SVG `<script>` element from triggering.

Lightning Web Security stores the value of `href` in a different attribute `data-distorted-href`. LWS fetches the script file using an XHR request and sets the `href` attribute value to a distorted value that uses the script fetched by LWS. The browser then reads the distorted value of the `href` attribute, which kicks off the evaluation process in the sandbox.

These steps ensure that different browsers work as expected, while preventing them from running script source before LWS can evaluate it.

### Distorted Behavior

This distortion for the `href` or `xlink:href` getter provides a distorted version of the script to the browser.
<hr>
<a name="svgsetelementdocsattributename-attributemd"></a>

## SVGSetElement: `attributeName` attribute

The [`attributeName`](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/attributeName) attribute indicates the name of the CSS property or attribute of the target element that is going to be changed during an animation.

When you set the `attributeName` to `href`, the element accesses an SVG resource specified with the `to` attribute.  Malicious code can bypass Lightning Web Security with an `<iframe>` or `<script>` element inside the SVG resource and run code outside the sandbox. 

This distortion applies when the code sets `href` on the `attributeName` attribute after setting the `to` attribute.

### Distorted Behavior

This distortion sanitizes SVG files passed with the `to` attribute of the `<set>` element.

<hr>
<a name="svgsetelementdocsto-attributemd"></a>

## SVGSetElement: `to` attribute

The [`to`](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/To#set) attribute specifies the value for the attribute during the duration of the element.

When you set the SVG resource dynamically with the `to` attribute, the SVG resource isn't sanitized. Malicious code can bypass Lightning Web Security with an `<iframe>` or `<script>` element inside the SVG resource and run code outside of sandbox. 

### Distorted Behavior

This distortion sanitizes SVG files that are passed with the `to` attribute of the `<set>` element.

<hr>
<a name="svguseelementdocshref-attributemd"></a>

## SVGUseElement: `href` attribute

The [`SVGUseElement.href`](https://developer.mozilla.org/en-US/docs/Web/API/SVGUseElement) property is an `SVGAnimatedString` corresponding to the `href` or `xlink:href` attribute of the given `<use>` element.

The `SVGUseElement.href` property reflects the `href` attribute of a `<use>` element inside an `<svg>` element, specifying the URL to an element or fragment that is to be duplicated.

The `href` attribute isn’t present on the `SVGUseElement.prototype` and can only be set using these methods of `Element`:

- `setAttribute`
- `setAttributeNode`
- `setAttributeNS`
- `setAttributeNodeNS`

These methods are covered by distortions on `Element` methods, but require more distortion when used in the context of `SVGUseElement`.

### Distorted Behavior

This distortion sanitizes the value passed for attribute `href` or `xlink:href` on an `SVGUseElement`.

For the `href` or `xlink:href` getter, this distortion does nothing if the URL is to a document fragment in the `<svg>`.

If the URL is for an external resource, the distortion transforms the URL to a document fragment URL and assigns it to a hidden `<div>` element in the page. The document fragment URL is composed of current hostname, resource name, extension followed by an underscore and the id in the referenced resource. A URL such as `/resource.svg#circle` becomes `#HOSTNAMEresourcesvg_circle`.

Lightning Web Security fetches the resource asynchronously using an XHR request and sanitizes the content, then places it in the `<div>` element that has the new document fragment URL. The content is rendered where the `<use>` tag is defined in the `<svg>`. 

### Distorted Behavior for setAttribute
```js
const el = document.createElementNS('http://www.w3.org/2000/svg', 'use');

el.setAttribute('href', '/myresource.svg#circle');
console.log(el.getAttribute('href')); // -> httpmycurrenthostmyresourcesvg_circle

// OR for xlink:href
el.setAttribute('xlink:href', '/myresource.svg#circle');
console.log(el.getAttributeNS('http://www.w3.org/1999/xlink', 'href')); // null
console.log(el.getAttributeNS('http://www.w3.org/1999/xlink', 'xlink:href')); // null
console.log(el.getAttribute('xlink:href')); // httpmycurrenthostmyresourcesvg_circle
```

### Distorted Behavior for setAttributeNode
```js
const el = document.createElementNS('http://www.w3.org/2000/svg', 'use');
let attr = document.createAttribute('href');
attr.value = '/myresource.svg#circle';
el.setAttributeNode(attr);
console.log(el.getAttribute('href')); // httpmycurrenthostmyresourcesvg_circle

// OR for xlink:href
attr = document.createAttribute('http://www.w3.org/1999/xlink', 'xlink:href');
attr.value = '/myresource.svg#circle';
el.setAttributeNode(attr);
console.log(el.getAttributeNS('http://www.w3.org/1999/xlink', 'href')); // null
console.log(el.getAttributeNS('http://www.w3.org/1999/xlink', 'xlink:href')); // null
console.log(el.getAttribute('xlink:href')); // null
```

### Distorted Behavior for setAttributeNS
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

<hr>
<a name="serviceworkercontainerdocsprototype-valuemd"></a>

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
<hr>
<a name="shadowrootdocsinnerhtml-settermd"></a>

## ShadowRoot.prototype.innerHTML setter

The [`ShadowRoot.prototype.innerHTML`](https://developer.mozilla.org/en-US/docs/Web/API/ShadowRoot/innerHTML) property sets or returns a reference to the DOM tree inside the `ShadowRoot`.

Malicious code can add `<script>` elements to the DOM tree inside the shadow root. The scripts run without being sanitized.

### Distorted Behavior

This distortion sanitizes the string provided to the `innerHTML` setter.
<hr>
<a name="shadowrootdocsmode-gettermd"></a>

## ShadowRoot.prototype.mode getter

The [`ShadowRoot.prototype.mode`](https://developer.mozilla.org/en-US/docs/Web/API/ShadowRoot/mode) property determines whether the shadow root is accessible from JavaScript. When the value is `closed` the shadow root is not exposed to the scripting environment. The shadow root’s implementation internals are inaccessible and unchangeable from JavaScript.

### Distorted Behavior

This distortion returns `closed` when a getter accesses the `mode` property on any element with an attached shadow DOM. <hr>
<a name="sharedworkerdocsconstructor-valuemd"></a>

## SharedWorker Constructor

The [`SharedWorker()`](https://developer.mozilla.org/en-US/docs/Web/API/SharedWorker/SharedWorker) constructor creates a `SharedWorker` object that executes the script at the specified URL. This script must obey the same-origin policy, a security mechanism that restricts how a document or script loaded by one origin can interact with a resource from another origin.

Malicious code can use `SharedWorker()` to execute script at a specified URL to bypass Lightning Web Security distortions.

### Distorted Behavior

This distortion throws an exception when calling the constructor, and blocks access to `SharedWorker.prototype`.
<hr>
<a name="storagedocsclear-valuemd"></a>

## Storage.prototype.clear

The [`Storage.prototype.clear()`](https://developer.mozilla.org/en-US/docs/Web/API/Storage/clear) method clears all keys and associated data stored in a given `Storage` object.

Each sandbox uses its own synthetic storage. Lightning Web Security prevents `clear()` from clearing all the data items in another sandbox or outside sandboxes.

### Distorted Behavior

This distortion deletes all data items from the sandboxed code's synthetic storage.
<hr>
<a name="storagedocsconstructor-valuemd"></a>

## Storage API: Storage.prototype

The [`Storage`](https://developer.mozilla.org/en-US/docs/Web/API/Storage) interface provides access to a particular domain's session storage or local storage. It allows the addition, modification, or deletion of stored data items, which are shared.

The storage is accessible in the browser and holds its shape across multiple tabs from the same domain.

Lightning Web Security creates synthetic storage for each namespace, where malicious code can't add, modify, or clear data items in global storage or in storage belonging to other namespaces.

Note: The `key()` method of the `Storage` interface, when passed a number n, returns the name of the nth key in a given `Storage` object. The order of keys is defined by the user agent, so you can't rely on it. Therefore, it’s OK to have the storage items out of order.

### Distorted Behavior

This distortion prepends an `LSKey[NS]` to all storage values set in each namespace, where `NS` is the namespace name. This distortion uses a `SecureStorage` class that implements all methods and properties from the raw `Storage`. This distortion also uses a proxy to mimic interactive features that are on the raw `Storage`. Storage Example:

[Global]
`localStorage.setItem('x','y'); localStorage; // { 'x': 'y', 'LSKey[NS1]x': 'y', 'LSKey[NS2]x': 'y' }`

[NS1]
`localStorage.setItem('x','y'); localStorage; // { 'x': 'y' }`

[NS2]
`localStorage.setItem('x','y'); localStorage; // { 'x': 'y' }`

The proxy wrap has traps that allow for our Storage to have features that are the same as the raw Storage. Such features include getting, setting, iterating, and basic object features.

* Set/Get: `localStorage.x = 'y'; localStorage; // { 'x': 'y' }`
* Define Property: `Object.defineProperty(localStorage, 'foo', { value: 'bar' }); // { 'foo': 'bar', 'x': 'y' }`
* Delete Property: `delete localStorage.foo; // { 'x': 'y' }`
* Iteration: `Object.keys(localStorage); // ['x']`
* Has: `'x' in sessionStorage; localStorage.hasOwnProperty('x'); // true, true`<hr>
<a name="storagedocsgetitem-valuemd"></a>

## Storage.prototype.getItem

The [`Storage.prototype.getItem()`](https://developer.mozilla.org/en-US/docs/Web/API/Storage/getItem) method, when passed a key name, returns that key's value, or `null` if the key does not exist, in the given `Storage` object.

Lightning Web Security creates synthetic storage for each sandbox. The synthetic storage prevents code in one sandbox from retrieving data belonging to another namespace or outside sandboxes.

### Distorted Behavior

This distortion ensures sandboxed code retrieves data items from its own synthetic storage.
<hr>
<a name="storagedocskey-valuemd"></a>

## Storage.prototype.key

The [`Storage.prototype.key()`](https://developer.mozilla.org/en-US/docs/Web/API/Storage/key) method, when passed a number n, returns the name of the nth key in a given `Storage` object. The order of keys is user-agent defined, so you can't rely on it. Therefore, it’s OK to have the storage items out of order.

### Distorted Behavior

This distortion retrieves a key value at a specific index from the sandboxed code's synthetic storage.<hr>
<a name="storagedocslength-gettermd"></a>

## Storage.prototype.length getter

The [`Storage.prototype.length`](https://developer.mozilla.org/en-US/docs/Web/API/Storage/length) read-only property returns the number of data items stored in a given `Storage` object.

When the getter for `length` is used, Lightning Web Security retrieves the number of data items in the namespace's synthetic storage rather than the shared storage.

### Distorted Behavior

This distortion retrieves the number of data items in the sandboxed code's synthetic storage.<hr>
<a name="storagedocsremoveitem-valuemd"></a>

## Storage.prototype.removeItem

The [`Storage.prototype.removeItem()`](https://developer.mozilla.org/en-US/docs/Web/API/Storage/removeItem) method, when passed a key name, removes that key from the given `Storage` object if it exists.

Each sandbox uses its own synthetic storage. Lightning Web Security prevents `removeItem()` from removing data items from another sandbox or outside sandboxes.

### Distorted Behavior

This distortion deletes a data item from the sandboxed code's synthetic storage.<hr>
<a name="storagedocssetitem-valuemd"></a>

## Storage.prototype.setItem

The [`Storage.prototype.setItem()`](https://developer.mozilla.org/en-US/docs/Web/API/Storage/setItem) method, when passed a key name and value,  adds that key to the given `Storage` object, or update that key's value if it already exists.

Each sandbox uses its own synthetic storage. Lightning Web Security prevents `setItem()`](https://developer.mozilla.org/en-US/docs/Web/API/Storage/setItem) from adding or modifying data items in another sandbox or outside sandboxes.
### Distorted Behavior

This distortion adds or modifies data items in the sandboxed code's synthetic storage.
<hr>
<a name="trustedtypepolicyfactorydocscreatepolicy-valuemd"></a>

## TrustedTypePolicyFactory.createPolicy

The [`TrustedTypePolicyFactory.prototype.createPolicy()`](https://developer.mozilla.org/en-US/docs/Web/API/TrustedTypePolicyFactory/createPolicy) method of the `TrustedTypePolicyFactory` interface creates a `TrustedTypePolicy` object that implements the rules passed as `policyOptions`. 

In Chrome a policy with a name of `'default'` creates a special policy that will be used if a string, rather than a Trusted Type object, is passed to an injection sink. This can be used in a transitional phase while moving from an application that inserted strings into injection sinks.

Malicious code can overwrite the default policy, and pass its own code into an injection sink.

Lightning Web Security prevents setting the `policyName` to the `'default'` value.

### Distorted Behavior

This distortion prevents setting the `policyName` to the `'default'` value.

On a site where Trusted Types are enforced via a Content Security Policy with the [require-trusted-types-for](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/require-trusted-types-for) directive set to `script`, injection even of trusted types won't work in Chrome.
<hr>
<a name="urldocscreateobjecturl-valuemd"></a>

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
document.body.appendChild(iframe);
```

Without protection from Lightning Web Security, upon loading the content of the `iframe`, the browser runs the code in the `<script>` tag which bypasses the sandbox. If the code is running on the same domain, it gains access to all cookies and displays them in a popup window.

To guard against exploits, Lightning Web Security fetches the content of the URL and scans `Blob` and `File` objects that have their MIME type set to `text/html`, `image/svg+xml` or `text/xml`. If malicious content is detected, the code doesn't execute.

### Distorted Behavior

This distortion throws an exception when MIME types `text/html`, `text/xml`, `image/svg+xml` are used with `Blob` or `File` objects that try to load malicious content: `Lightning Web Security: Cannot "createObjectURL" using an unsecure [object Blob]!`

If no malicious content is detected when these MIME types are used, the content is allowed to load but the distortion enforces `charset=utf-8` to prevent exploits where the browser auto-interprets charset and special characters that can lead to XSS.

For any unsupported MIME types, including `text/javascript`, the distortion throws an exception with the message `Lightning Web Security: Unsupported MIME type.`

Empty MIME types on `File` and `Blob` objects are treated as `text/plain` since browsers treat this differently.

All commonly used and non-malicious MIME types work as expected.
<hr>
<a name="windowdocsfetch-valuemd"></a>

## Window.fetch

The global [`fetch()`](https://developer.mozilla.org/en-US/docs/Web/API/fetch) method starts the process of fetching a resource from the network, returning a promise that is fulfilled when the response is available.

Lightning Web Security disallows access to URL endpoints containing `"/aura"` and `"/webruntime"` because they are part of the Lightning Component framework.

### Distorted Behavior

This distortion examines the `hostname` and the `pathname` of the URL. If there's a match to a disallowed endpoint, it rejects the promise.
<hr>
<a name="windowdocsframes-gettermd"></a>

## window.frames getter

The [`window.frames`](https://developer.mozilla.org/en-US/docs/Web/API/Window/frames) property returns an array-like object that lists all the `frame` and `iframe` elements in the current window.

```js
frameList = window.frames;
frameList === window; // evaluates to true (normally)
```

Lightning Web Security restricts access by distorting the `frameList` object returned, so that malicious code can't access `window` properties.

### Distorted Behavior

This distortion returns an artificial `frameList` object that includes
all `frame` and `iframe` elements in the document, in insertion order.

The `frameList` object supports access by index value or name property value, as the native one does.

However, the distorted `window.frames` doesn't allow access to `window` or provide proxy access to
`window` properties.

```js
framelist !== window; // evaluates to true with this distortion
```
<hr>
<a name="windowdocsgetcomputedstyle-valuemd"></a>

## Window.prototype.getComputedStyle

The [`Window.prototype.getComputedStyle()`](https://developer.mozilla.org/en-US/docs/Web/API/Window/getComputedStyle) method returns an object containing the values of all CSS properties of an element, after applying active style sheets and resolving any basic computation those values may contain.

The returned object is the same `CSSStyleDeclaration` type as the object returned from the element's `style` property. However, the two objects have different purposes:
  - The object returned by `getComputedStyle` is read-only, and should be used to inspect the element's style — including those set by a `<style>` element or an external stylesheet.
  - The `element.style` object should be used to set styles on that element, or inspect styles directly added to it from JavaScript manipulation or the global `style` attribute.

### Distorted Behavior

This distortion alters the returned style object. The style object is marked as live so that its native behavior is preserved and any attempt to mutate its read-only CSS properties results in the expected DOM exception.
<hr>
<a name="windowdocslength-gettermd"></a>

## window.length getter

The [`window.length`](https://developer.mozilla.org/en-US/docs/Web/API/Window/length) property returns the number of frames (either `<frame>` or `<iframe>` elements) attached to the `window` object's `document`.

### Distorted Behavior

The `window.length` property always returns `0`.

Instead of `window.length`, use the `window.frames.length` value and `window.frames` object to iterate over the list of frames (either `<frame>` or `<iframe>` elements) attached to the `document`.
<hr>
<a name="windowdocsonstorage-settermd"></a>

## WindowEventHandlers.onstorage

The [`onstorage`]https://developer.mozilla.org/en-US/docs/Web/API/WindowEventHandlers/onstorage) property of the `WindowEventHandlers` mixin is an event handler for processing storage events.

The `storage` event fires when a storage area has been changed in the context of another document.

### Distorted Behavior

Currently, Lightning Web Security doesn't support the `window.onstorage` event, so setting the `onstorage` property is not allowed and returns an error.
<hr>
<a name="windowdocsopen-valuemd"></a>

## window.open

The [`window.open()`](https://developer.mozilla.org/en-US/docs/Web/API/Window/open) method loads the specified resource into a new or existing browsing context with the specified name. If the name doesn't exist, then a new browsing context is opened in a new tab or a new window, and the specified resource is loaded into it.

This new browsing context isn’t sandboxed properly and malicious code can access system mode, so Lightning Web Security distorts the `window` object returned.

### Distorted Behavior

This distortion returns an artificial `window` object that allows only safe methods.

- `close`
- `focus`
- `postMessage`

[//]: # (This will change after multi-window support)
<hr>
<a name="windowdocsopener-gettermd"></a>

## window.opener getter

The [`window.opener`](https://developer.mozilla.org/en-US/docs/Web/API/Window/opener) property getter returns a reference to the window that opened the window, either with `open()`, or by navigating a link with a `target` attribute.

In other words, if window `A` opens window `B`, `B.opener` returns `A`.

Lightning Web Security doesn't allow access to the raw `window` object.

### Distorted Behavior

This distortion returns an artificial `window` object that allows only safe methods.

- `close`
- `focus`
- `postMessage`

[//]: # (This will change after multi-window support)
<hr>
<a name="windowdocsparent-gettermd"></a>

## window.parent getter

The [`window.parent`](https://developer.mozilla.org/en-US/docs/Web/API/Window/parent) property returns a reference to the parent of the current window or subframe. If a window does not have a parent, its `parent` property is a reference to itself.

If window `A` embeds window `B`, `B.parent` returns `A`.

### Distorted Behavior

This distortion returns an artificial `window` object that allows only safe methods.

- `close`
- `focus`
- `postMessage`

[//]: # (This will change after multi-window support)
<hr>
<a name="windowdocspostmessage-valuemd"></a>

## Window.prototype.postMessage

The [`Window.prototype.postMessage()`](https://developer.mozilla.org/en-US/docs/Web/API/Window/postMessage) method safely enables cross-origin communication between `Window` objects; e.g., between a page and a pop-up that it spawned, or between a page and an iframe embedded within it.

### Distorted Behavior

This distortion preserves the `postMessage()` method's native behavior in the sandbox by ensuring that the [structured clone algorithm](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Structured_clone_algorithm) works correctly on the `message` parameter. 
<hr>
<a name="windowdocssetinterval-valuemd"></a>

## window.setInterval

The [`window.setInterval()`](https://developer.mozilla.org/en-US/docs/Web/API/setInterval) method repeatedly calls a function or executes a code snippet, with a fixed time delay between each call.

Code snippet execution is supported by accepting a string for the first argument. This string evaluation escapes the sandbox.

Lightning Web Security must evaluate the string in the sandbox.

### Distorted Behavior

If the first argument provided to `setInterval` is a string value, this distortion evaluates the string in the sandbox.
<hr>
<a name="windowdocssettimeout-valuemd"></a>

## window.setTimeout

The [`window.setTimeout()`](https://developer.mozilla.org/en-US/docs/Web/API/setTimeout) method sets a timer which executes a function or specified piece of code when the timer expires.

Code snippet execution is supported by accepting a string for the first argument. This string evaluation escapes the sandbox.

Lightning Web Security must evaluate the string in the sandbox.

### Distorted Behavior

If the first argument provided to `setTimeout` is a string value, this distortion evaluates the string in the sandbox.
<hr>
<a name="windowdocsstructuredclone-valuemd"></a>

## Window.prototype.structuredClone

The global [`Window.prototype.structuredClone()`](https://developer.mozilla.org/en-US/docs/Web/API/structuredClone)  method creates a [deep clone](https://developer.mozilla.org/en-US/docs/Glossary/Deep_copy) of a given value using the [structured clone algorithm](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Structured_clone_algorithm).

### Distorted Behavior

This distortion preserves the `structuredClone()` method's native behavior in the sandbox by ensuring that the [structured clone algorithm](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Structured_clone_algorithm) works correctly on the `value` parameter. 
<hr>
<a name="workerdocsconstructor-valuemd"></a>

## Worker Constructor

The [`Worker()`](https://developer.mozilla.org/en-US/docs/Web/API/Worker/Worker) constructor creates a `Worker` object that executes the script at the specified URL. This script must obey the same-origin policy.

Malicious code can execute a script at a specified URL to bypass Lightning Web Security evaluation rules.

### Distorted Behavior

Lightning Web Security throws an exception `Lightning Web Security: Cannot create Worker with ${url}` when calling the constructor. Lightning Web Security blocks access to `Worker.prototype`.
<hr>
<a name="xmlhttprequestdocsopen-valuemd"></a>

## XMLHttpRequest.prototype.open

The [`XMLHttpRequest.prototype.open()`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/open) method initializes a newly-created request, or re-initializes an existing one.

Lightning Web Security disallows access to URL endpoints containing `"/aura"` and `"/webruntime"` because they are part of the Lightning Component framework.

### Distorted Behavior

This distortion examines the `hostname` and the `pathname` of the URL. If there's a match to a disallowed endpoint, it throws an exception.
<hr>
<a name="xmlhttprequestdocsresponse-gettermd"></a>

## XMLHttpRequest.prototype.response getter

The [`XMLHttpRequest.prototype.response`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/response) property returns the response's body content as an `ArrayBuffer`, `Blob`, `Document`, JavaScript `Object`, or `DOMString`, depending on the value of the request's `responseType` property.

If the response's body content is a `Document`, malicious code can add `<script>` tags that run without being sanitized.

### Distorted Behavior

This distortion sanitizes the `response` property value when the body content is a `Document`.
<hr>
<a name="xmlhttprequestdocsresponsexml-gettermd"></a>

## XMLHttpRequest.prototype.responseXML getter

The [`XMLHttpRequest.prototype.responseXML`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/responseXML) read-only property returns a `Document` containing the HTML or XML retrieved by the request. It returns `null` if the request was unsuccessful, hasn't yet been sent, or if the data can't be parsed as XML or HTML.

Malicious code can add `<script>` tags that run without being sanitized.

### Distorted Behavior

This distortion sanitizes the `responseXML` property value.
<hr>
<a name="xsltprocessordocstransformtodocument-valuemd"></a>

## XSLTProcessor.prototype.transformToDocument

**Non-standard**: This feature is non-standard and is not on a standards track. Do not use it on production sites facing the Web: it will not work for every user. There may also be large incompatibilities between implementations and the behavior may change in the future.

`XSLTProcessor.prototype.transformToDocument(Node source, Document owner)` transforms the node source by applying the stylesheet imported using the `XSLTProcessor.prototype.importStylesheet()` function. The owner document of the resulting document fragment is the owner node.

This function can be used to parse and transform XML documents with XSLT into valid HTML documents, which can be inserted into the current DOM. By using XSLT, it is possible to create arbitrary HTML tags and therefore gain access to the raw window object.

### Distorted Behavior

This method is blocked by LWS, and an exception is thrown if code attempts to call it.
<hr>
<a name="xsltprocessordocstransformtodocumentmd"></a>

## XSLTProcessor.prototype.transformToDocument

**Non-standard**: This feature is non-standard and is not on a standards track. Do not use it on production sites facing the Web: it will not work for every user. There may also be large incompatibilities between implementations and the behavior may change in the future.

`XSLTProcessor.prototype.transformToDocument(Node source, Document owner)` transforms the node source by applying the stylesheet imported using the `XSLTProcessor.prototype.importStylesheet()` function. The owner document of the resulting document fragment is the owner node.

This function can be used to parse and transform XML documents with XSLT into valid HTML documents, which can be inserted into the current DOM. By using XSLT, it is possible to create arbitrary HTML tags and therefore gain access to the raw window object.

### Distorted Behavior

This method is blocked by LWS, and an exception is thrown if code attempts to call it.
<hr>
<a name="xsltprocessordocstransformtofragment-valuemd"></a>

## XSLTProcessor.prototype.transformToFragment

**Non-standard**: This feature is non-standard and is not on a standards track. Do not use it on production sites facing the Web: it will not work for every user. There may also be large incompatibilities between implementations and the behavior may change in the future.

`XSLTProcessor.prototype.transformToFragment(Node source, Document owner)` transforms the node source by applying the stylesheet imported using the `XSLTProcessor.prototype.importStylesheet()` function. The owner document of the resulting document fragment is the owner node.

This function can be used to parse and transform XML documents with XSLT into valid HTML documents, which can be inserted into the current DOM. By using XSLT, it is possible to create arbitrary HTML tags and therefore gain access to the raw window object.

### Distorted Behavior

This method is blocked by LWS, and an exception is thrown if code attempts to call it.
<hr>
<a name="xsltprocessordocstransformtofragmentmd"></a>

## XSLTProcessor.prototype.transformToFragment

**Non-standard**: This feature is non-standard and is not on a standards track. Do not use it on production sites facing the Web: it will not work for every user. There may also be large incompatibilities between implementations and the behavior may change in the future.

`XSLTProcessor.prototype.transformToFragment(Node source, Document owner)` transforms the node source by applying the stylesheet imported using the `XSLTProcessor.prototype.importStylesheet()` function. The owner document of the resulting document fragment is the owner node.

This function can be used to parse and transform XML documents with XSLT into valid HTML documents, which can be inserted into the current DOM. By using XSLT, it is possible to create arbitrary HTML tags and therefore gain access to the raw window object.

### Distorted Behavior

This method is blocked by LWS, and an exception is thrown if code attempts to call it.
