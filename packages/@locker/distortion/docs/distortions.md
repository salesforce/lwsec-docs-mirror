# Lightning Web Security Distortions

This is the list of the currently implemented distortions.

Version: 0.22.5<br>
Generated: Jul 23, 2024

## Table of Contents

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Attr.prototype.value setter](#attrprototypevalue-setter)
  - [Distorted Behavior](#distorted-behavior)
- [CacheStorage.prototype.delete](#cachestorageprototypedelete)
  - [Distorted Behavior](#distorted-behavior-1)
- [CacheStorage.prototype.has](#cachestorageprototypehas)
  - [Distorted Behavior](#distorted-behavior-2)
- [CacheStorage.prototype.keys](#cachestorageprototypekeys)
  - [Distorted Behavior](#distorted-behavior-3)
- [CacheStorage.prototype.match](#cachestorageprototypematch)
  - [Distorted Behavior](#distorted-behavior-4)
- [CacheStorage.prototype.open](#cachestorageprototypeopen)
  - [Distorted Behavior](#distorted-behavior-5)
- [CookieStore.prototype.addEventListener](#cookiestoreprototypeaddeventlistener)
  - [Distorted Behavior](#distorted-behavior-6)
- [CookieStore.prototype.delete](#cookiestoreprototypedelete)
  - [Distorted Behavior](#distorted-behavior-7)
- [CookieStore.prototype.get](#cookiestoreprototypeget)
  - [Distorted Behavior](#distorted-behavior-8)
- [CookieStore.prototype.getAll](#cookiestoreprototypegetall)
  - [Distorted Behavior](#distorted-behavior-9)
- [CookieStore.prototype.onchange setter](#cookiestoreprototypeonchange-setter)
  - [Distorted Behavior](#distorted-behavior-10)
- [CookieStore.prototype.set](#cookiestoreprototypeset)
  - [Distorted Behavior](#distorted-behavior-11)
- [CustomElementRegistry.prototype.define](#customelementregistryprototypedefine)
  - [Distorted Behavior](#distorted-behavior-12)
- [CustomElementRegistry.prototype.get](#customelementregistryprototypeget)
  - [Distorted Behavior](#distorted-behavior-13)
- [CustomElementRegistry.prototype.whenDefined](#customelementregistryprototypewhendefined)
  - [Distorted Behavior](#distorted-behavior-14)
- [DOMParser.prototype.parseFromString](#domparserprototypeparsefromstring)
  - [Distorted Behavior](#distorted-behavior-15)
- [DataTransfer.moz*](#datatransfermoz)
  - [Distorted Behavior](#distorted-behavior-16)
- [Document.prototype.createProcessingInstruction](#documentprototypecreateprocessinginstruction)
  - [Distorted Behavior](#distorted-behavior-17)
- [Fullscreen API: Document.prototype](#fullscreen-api-documentprototype)
  - [Distorted Behavior](#distorted-behavior-18)
- [Document.prototype.onrejectionhandled and Document.prototype.onunhandledrejection [Safari]](#documentprototypeonrejectionhandled-and-documentprototypeonunhandledrejection-safari)
  - [Distorted Behavior](#distorted-behavior-19)
- [onsecuritypolicyviolation](#onsecuritypolicyviolation)
  - [Distorted Behavior](#distorted-behavior-20)
- [Document.prototype.parseHTMLUnsafe](#documentprototypeparsehtmlunsafe)
  - [Distorted Behavior](#distorted-behavior-21)
- [Document.prototype.releaseCapture](#documentprototypereleasecapture)
  - [Distorted Behavior](#distorted-behavior-22)
- [Document.prototype.releaseEvents](#documentprototypereleaseevents)
  - [Distorted Behavior](#distorted-behavior-23)
- [Document.prototype.write](#documentprototypewrite)
  - [Distorted Behavior](#distorted-behavior-24)
- [Document.prototype.writeln](#documentprototypewriteln)
  - [Distorted Behavior](#distorted-behavior-25)
- [Document.prototype.cookie getter](#documentprototypecookie-getter)
  - [Distorted Behavior](#distorted-behavior-26)
- [Document.prototype.cookie setter](#documentprototypecookie-setter)
  - [Distorted Behavior](#distorted-behavior-27)
- [Document.prototype.domain setter](#documentprototypedomain-setter)
  - [Distorted Behavior](#distorted-behavior-28)
- [Document.prototype.execCommand](#documentprototypeexeccommand)
  - [Distorted Behavior](#distorted-behavior-29)
- [Document "securitypolicyviolation" event](#document-securitypolicyviolation-event)
  - [Distorted Behavior](#distorted-behavior-30)
- [Document.prototype.open](#documentprototypeopen)
  - [Distorted Behavior](#distorted-behavior-31)
- [Document.prototype.replaceChildren](#documentprototypereplacechildren)
  - [Distorted Behavior](#distorted-behavior-32)
- [Element.prototype.after](#elementprototypeafter)
  - [Distorted Behavior](#distorted-behavior-33)
- [Element.prototype.append](#elementprototypeappend)
  - [Summary](#summary)
  - [Distorted Behavior](#distorted-behavior-34)
- [Element.prototype.attachShadow](#elementprototypeattachshadow)
  - [Distorted Behavior](#distorted-behavior-35)
- [Element.prototype.before](#elementprototypebefore)
  - [Distorted Behavior](#distorted-behavior-36)
- [Fullscreen API: Element.prototype](#fullscreen-api-elementprototype)
  - [Distorted Behavior](#distorted-behavior-37)
- [Element.prototype.setHTMLUnsafe](#elementprototypesethtmlunsafe)
  - [Distorted Behavior](#distorted-behavior-38)
- [Element.prototype.getInnerHTML](#elementprototypegetinnerhtml)
  - [Distorted Behavior](#distorted-behavior-39)
- [Element.prototype.innerHTML setter](#elementprototypeinnerhtml-setter)
  - [Distorted Behavior](#distorted-behavior-40)
- [Element.prototype.insertAdjacentElement](#elementprototypeinsertadjacentelement)
  - [Distorted Behavior](#distorted-behavior-41)
- [Element.prototype.insertAdjacentHTML](#elementprototypeinsertadjacenthtml)
  - [Distorted Behavior](#distorted-behavior-42)
- [Element.prototype.outerHTML setter](#elementprototypeouterhtml-setter)
  - [Distorted Behavior](#distorted-behavior-43)
- [Element.prototype.prepend](#elementprototypeprepend)
  - [Distorted Behavior](#distorted-behavior-44)
- [Element.prototype.remove](#elementprototyperemove)
  - [Distorted Behavior](#distorted-behavior-45)
- [Element.prototype.replaceChildren](#elementprototypereplacechildren)
  - [Distorted Behavior](#distorted-behavior-46)
- [Element.prototype.replaceWith](#elementprototypereplacewith)
  - [Distorted Behavior](#distorted-behavior-47)
- [Element.prototype.setAttribute*](#elementprototypesetattribute)
  - [Distorted Behavior](#distorted-behavior-48)
- [Element.prototype.setHTML](#elementprototypesethtml)
  - [Distorted Behavior](#distorted-behavior-49)
- [Element.prototype.shadowRoot getter](#elementprototypeshadowroot-getter)
  - [Distorted Behavior](#distorted-behavior-50)
- [Event.prototype.explicitOriginalTarget](#eventprototypeexplicitoriginaltarget)
  - [Distorted Behavior](#distorted-behavior-51)
- [Event.prototype.originalTarget](#eventprototypeoriginaltarget)
  - [Distorted Behavior](#distorted-behavior-52)
- [Event.prototype.composedPath](#eventprototypecomposedpath)
  - [Distorted Behavior](#distorted-behavior-53)
- [Function Constructor](#function-constructor)
  - [Distorted Behavior](#distorted-behavior-54)
- [HTMLBodyElement "rejectionhandled" event](#htmlbodyelement-rejectionhandled-event)
  - [Distorted Behavior](#distorted-behavior-55)
- [HTMLBodyElement "storage" event](#htmlbodyelement-storage-event)
  - [Distorted Behavior](#distorted-behavior-56)
- [HTMLBodyElement "unhandledrejection" event](#htmlbodyelement-unhandledrejection-event)
  - [Distorted Behavior](#distorted-behavior-57)
- [HTMLElement.prototype.nonce](#htmlelementprototypenonce)
  - [Distorted Behavior](#distorted-behavior-58)
- [HTMLElement.prototype.onrejectionhandled and HTMLElement.prototype.onunhandledrejection [Safari]](#htmlelementprototypeonrejectionhandled-and-htmlelementprototypeonunhandledrejection-safari)
  - [Distorted Behavior](#distorted-behavior-59)
- [HTMLElement.prototype.innerText setter](#htmlelementprototypeinnertext-setter)
  - [Distorted Behavior](#distorted-behavior-60)
- [HTMLElement.prototype.outerText setter](#htmlelementprototypeoutertext-setter)
  - [Distorted Behavior](#distorted-behavior-61)
- [HTMLEmbedElement.prototype.getSVGDocument](#htmlembedelementprototypegetsvgdocument)
  - [Distorted Behavior](#distorted-behavior-62)
- [HTMLFrameSetElement "rejectionhandled" event](#htmlframesetelement-rejectionhandled-event)
  - [Distorted Behavior](#distorted-behavior-63)
- [HTMLFrameSetElement "storage" event](#htmlframesetelement-storage-event)
  - [Distorted Behavior](#distorted-behavior-64)
- [HTMLFrameSetElement "unhandledrejection" event](#htmlframesetelement-unhandledrejection-event)
  - [Distorted Behavior](#distorted-behavior-65)
- [HTMLIFrameElement.prototype.getSVGDocument](#htmliframeelementprototypegetsvgdocument)
  - [Distorted Behavior](#distorted-behavior-66)
- [HTMLIFrameElement.prototype.srcdoc](#htmliframeelementprototypesrcdoc)
  - [Distorted Behavior](#distorted-behavior-67)
- [HTMLIFrameElement.prototype.src setter](#htmliframeelementprototypesrc-setter)
  - [Distorted Behavior](#distorted-behavior-68)
- [HTMLLinkElement.prototype.rel setter](#htmllinkelementprototyperel-setter)
  - [Distorted Behavior](#distorted-behavior-69)
- [HTMLLinkElement.prototype.relList setter](#htmllinkelementprototyperellist-setter)
  - [Distorted Behavior](#distorted-behavior-70)
- [HTMLObjectElement.prototype.getSVGDocument](#htmlobjectelementprototypegetsvgdocument)
  - [Distorted Behavior](#distorted-behavior-71)
- [HTMLObjectElement.prototype.data setter](#htmlobjectelementprototypedata-setter)
  - [Distorted Behavior](#distorted-behavior-72)
- [HTMLScriptElement.prototype.nonce](#htmlscriptelementprototypenonce)
  - [Distorted Behavior](#distorted-behavior-73)
- [HTMLScriptElement.prototype.src setter](#htmlscriptelementprototypesrc-setter)
  - [Distorted Behavior](#distorted-behavior-74)
- [HTMLScriptElement.prototype.text setter](#htmlscriptelementprototypetext-setter)
  - [Distorted Behavior](#distorted-behavior-75)
- [NamedNodeMap.prototype.setNamedItem](#namednodemapprototypesetnameditem)
  - [Distorted Behavior](#distorted-behavior-76)
- [NamedNodeMap.prototype.setNamedItemNS](#namednodemapprototypesetnameditemns)
  - [Distorted Behavior](#distorted-behavior-77)
- [Navigator.sendBeacon()](#navigatorsendbeacon)
  - [Distorted Behavior](#distorted-behavior-78)
- [Navigator.prototype.serviceWorker getter](#navigatorprototypeserviceworker-getter)
  - [Distorted Behavior](#distorted-behavior-79)
- [Node.prototype.appendChild](#nodeprototypeappendchild)
  - [Distorted Behavior](#distorted-behavior-80)
- [Node.prototype.insertBefore](#nodeprototypeinsertbefore)
  - [Distorted Behavior](#distorted-behavior-81)
- [Node.prototype.removeChild](#nodeprototyperemovechild)
  - [Distorted Behavior](#distorted-behavior-82)
- [Node.prototype.replaceChild](#nodeprototypereplacechild)
  - [Distorted Behavior](#distorted-behavior-83)
- [Node.prototype.textContent setter](#nodeprototypetextcontent-setter)
  - [Distorted Behavior](#distorted-behavior-84)
- [Range.prototype.createContextualFragment](#rangeprototypecreatecontextualfragment)
  - [Distorted Behavior](#distorted-behavior-85)
- [Range.prototype.deleteContents](#rangeprototypedeletecontents)
  - [Distorted Behavior](#distorted-behavior-86)
- [Range.prototype.extractContents](#rangeprototypeextractcontents)
  - [Distorted Behavior](#distorted-behavior-87)
- [Range.prototype.insertNode](#rangeprototypeinsertnode)
  - [Distorted Behavior](#distorted-behavior-88)
- [Range.prototype.*](#rangeprototype)
  - [Distorted Behavior](#distorted-behavior-89)
- [SVGAnimateElement: "attributeName" attribute](#svganimateelement-attributename-attribute)
  - [Distorted Behavior](#distorted-behavior-90)
- [SVGAnimateElement: "from" attribute](#svganimateelement-from-attribute)
  - [Distorted Behavior](#distorted-behavior-91)
- [SVGAnimateElement: "to" attribute](#svganimateelement-to-attribute)
  - [Distorted Behavior](#distorted-behavior-92)
- [SVGAnimateElement: "values" attribute](#svganimateelement-values-attribute)
  - [Distorted Behavior](#distorted-behavior-93)
- [SVGElement.prototype.nonce](#svgelementprototypenonce)
  - [Distorted Behavior](#distorted-behavior-94)
- [SVGScriptElement.prototype.href setter](#svgscriptelementprototypehref-setter)
  - [Distorted Behavior](#distorted-behavior-95)
- [SVGSetElement: "attributeName" attribute](#svgsetelement-attributename-attribute)
  - [Distorted Behavior](#distorted-behavior-96)
- [SVGSetElement: "to" attribute](#svgsetelement-to-attribute)
  - [Distorted Behavior](#distorted-behavior-97)
- [SVGUseElement: "href" attribute](#svguseelement-href-attribute)
  - [Distorted Behavior](#distorted-behavior-98)
  - [Distorted Behavior for setAttribute](#distorted-behavior-for-setattribute)
  - [Distorted Behavior for setAttributeNode](#distorted-behavior-for-setattributenode)
  - [Distorted Behavior for setAttributeNS](#distorted-behavior-for-setattributens)
- [Selection.prototype.collapse](#selectionprototypecollapse)
  - [Distorted Behavior](#distorted-behavior-99)
- [Selection.prototype.extend](#selectionprototypeextend)
  - [Distorted Behavior](#distorted-behavior-100)
- [Selection.prototype.selectAllChildren](#selectionprototypeselectallchildren)
  - [Distorted Behavior](#distorted-behavior-101)
- [Selection.prototype.setBaseAndExtent](#selectionprototypesetbaseandextent)
  - [Distorted Behavior](#distorted-behavior-102)
- [Selection.prototype.setPosition](#selectionprototypesetposition)
  - [Distorted Behavior](#distorted-behavior-103)
- [ServiceWorkerContainer.prototype](#serviceworkercontainerprototype)
  - [Distorted Behavior](#distorted-behavior-104)
- [ShadowRoot.prototype.innerHTML setter](#shadowrootprototypeinnerhtml-setter)
  - [Distorted Behavior](#distorted-behavior-105)
- [SharedWorker Constructor](#sharedworker-constructor)
  - [Distorted Behavior](#distorted-behavior-106)
- [Storage.prototype.clear](#storageprototypeclear)
  - [Distorted Behavior](#distorted-behavior-107)
- [Storage API: Storage.prototype](#storage-api-storageprototype)
  - [Distorted Behavior](#distorted-behavior-108)
- [Storage.prototype.getItem](#storageprototypegetitem)
  - [Distorted Behavior](#distorted-behavior-109)
- [Storage.prototype.key](#storageprototypekey)
  - [Distorted Behavior](#distorted-behavior-110)
- [Storage.prototype.length getter](#storageprototypelength-getter)
  - [Distorted Behavior](#distorted-behavior-111)
- [Storage.prototype.removeItem](#storageprototyperemoveitem)
  - [Distorted Behavior](#distorted-behavior-112)
- [Storage.prototype.setItem](#storageprototypesetitem)
  - [Distorted Behavior](#distorted-behavior-113)
- [TrustedTypePolicyFactory.createPolicy](#trustedtypepolicyfactorycreatepolicy)
  - [Distorted Behavior](#distorted-behavior-114)
- [UIEvent.prototype.rangeParent](#uieventprototyperangeparent)
  - [Distorted Behavior](#distorted-behavior-115)
- [URL.createObjectURL](#urlcreateobjecturl)
  - [Distorted Behavior](#distorted-behavior-116)
- [Window.find](#windowfind)
  - [Distorted Behavior](#distorted-behavior-117)
- [Window.requestFileSystem](#windowrequestfilesystem)
  - [Distorted Behavior](#distorted-behavior-118)
- [Window.fetch](#windowfetch)
  - [Distorted Behavior](#distorted-behavior-119)
- [window.frames getter](#windowframes-getter)
  - [Distorted Behavior](#distorted-behavior-120)
- [window.length getter](#windowlength-getter)
  - [Distorted Behavior](#distorted-behavior-121)
- [Window "rejectionhandled" event](#window-rejectionhandled-event)
  - [Distorted Behavior](#distorted-behavior-122)
- [Window "securitypolicyviolation" event](#window-securitypolicyviolation-event)
  - [Distorted Behavior](#distorted-behavior-123)
- [Window "storage" event](#window-storage-event)
  - [Distorted Behavior](#distorted-behavior-124)
- [Window "unhandledrejection" event](#window-unhandledrejection-event)
  - [Distorted Behavior](#distorted-behavior-125)
- [window.open](#windowopen)
  - [Distorted Behavior](#distorted-behavior-126)
- [window.setInterval](#windowsetinterval)
  - [Distorted Behavior](#distorted-behavior-127)
- [window.setTimeout](#windowsettimeout)
  - [Distorted Behavior](#distorted-behavior-128)
- [Worker Constructor](#worker-constructor)
  - [Distorted Behavior](#distorted-behavior-129)
- [XMLHttpRequest.prototype.open](#xmlhttprequestprototypeopen)
  - [Distorted Behavior](#distorted-behavior-130)
- [XMLHttpRequest.prototype.response getter](#xmlhttprequestprototyperesponse-getter)
  - [Distorted Behavior](#distorted-behavior-131)
- [XMLHttpRequest.prototype.responseXML getter](#xmlhttprequestprototyperesponsexml-getter)
  - [Distorted Behavior](#distorted-behavior-132)
- [XSLTProcessor.prototype.transformToDocument](#xsltprocessorprototypetransformtodocument)
  - [Distorted Behavior](#distorted-behavior-133)
- [XSLTProcessor.prototype.transformToFragment](#xsltprocessorprototypetransformtofragment)
  - [Distorted Behavior](#distorted-behavior-134)
- [eval](#eval)
  - [Distorted Behavior](#distorted-behavior-135)

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
document.head.append(el); // append to head
```
### Distorted Behavior

The behavior varies according to the invoked distortion. If no distortions are registered for an attribute, the behavior seems native.
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

Currently, Lightning Web Security doesn't support the `CookieStore.onchange` event, so setting the `onchange` property, or adding a `change` event listener is not allowed and throws an exception.
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

Lightning Web Security controls the definition of custom elements by virtualizing the registry per sandbox to prevent usage of custom elements defined by system mode or others namespaces.

### Distorted Behavior

Custom Elements defined by the sandbox will only conflict with custom elements of the same tag name defined by another sandbox or by the system if the definition has a differing value for the static class property `formAssociated`.
<hr>
<a name="customelementregistrydocsget-valuemd"></a>

## CustomElementRegistry.prototype.get

The [`get`](https://developer.mozilla.org/en-US/docs/Web/API/CustomElementRegistry/get) method of `CustomElementRegistry` interface returns the constructor for a previously-defined custom element.

Lightning Web Security controls the access to defined custom elements by virtualizing the registry per sandbox to prevent usage of custom elements defined by system mode or others namespaces.

### Distorted Behavior

The sandbox can only get Custom Elements defined by the sandbox itself for a given name. It will prevent access to conflict with custom elements with the same name defined by another sandbox or by the system.
<hr>
<a name="customelementregistrydocswhendefined-valuemd"></a>

## CustomElementRegistry.prototype.whenDefined

The [`whenDefined`](https://developer.mozilla.org/en-US/docs/Web/API/CustomElementRegistry/whenDefined) method of the `CustomElementRegistry` interface returns a promise that fulfills when a new custom element of a given name is defined. 

Lightning Web Security controls the definition of custom elements by virtualizing the registry per sandbox to prevent usage of custom elements defined by system mode or others namespaces.

### Distorted Behavior

The promise will only be resolved for Custom Elements defined by the sandbox itself, and will never resolve for name defined by another sandbox or by the system.
<hr>
<a name="domparserdocsparsefromstring-valuemd"></a>

## DOMParser.prototype.parseFromString

The [`DOMParser.parseFromString()`](https://developer.mozilla.org/en-US/docs/Web/API/DOMParser/parseFromString) method parses a string containing either HTML or XML, returning an `HTMLDocument` or an `XMLDocument`.

Documents created via `new DOMParser().parseFromString('', 'text/html')` are subject to the same rules that govern `Element.prototype.innerHTML`.

### Distorted Behavior

This distortion sanitizes HTML strings prior to parsing and document creation.
<hr>
<a name="datatransferdocsblocked-properties-mozmd"></a>

## DataTransfer.moz*

[`DataTransfer.moz*()`](https://developer.mozilla.org/en-US/docs/Web/API/DataTransfer).

### Distorted Behavior

This distortion currently blocks access to `DataTransfer.moz*` APIs. This is a Firefox only API.
<hr>
<a name="documentdocsblocked-properties-createprocessinginstruction-valuemd"></a>

## Document.prototype.createProcessingInstruction

The [`Document.prototype.createProcessingInstruction()`](https://developer.mozilla.org/en-US/docs/Web/API/Document/createProcessingInstruction) generates a new processing instruction node and returns it.

Malicious code can create a processing instruction from an external XSLT that contains code which can bypass Lightning Web Security distortions and access the raw window.

### Distorted Behavior

This distortion blocks access to `Document.prototype.createProcessingInstruction`.
<hr>
<a name="documentdocsblocked-properties-fullscreenmd"></a>

## Fullscreen API: Document.prototype

The [Fullscreen API](https://developer.mozilla.org/en-US/docs/Web/API/Fullscreen_API) adds methods to present a specific `Document` (and its descendants) in full-screen mode, and to exit full-screen mode when it is no longer needed. This API makes it possible to present desired content such as an online game, using the user's entire screen. Full-screen mode removes all browser user interface elements and other applications from the screen until full-screen mode is shut off.

It is supported by all major browsers, with varying implementations.

This API doesn't adjust the DOM in the element. Instead, the native fullscreen hooks onto the browser. Malicious code can use the fullscreen API for phishing attacks. For example, because the fullscreen API obscures the browser's address bar, malicious code can hide the fake URL of a phishing page. Malicious coders can also fake an address bar with their own DOM.

### Distorted Behavior

This distortion prevents code from requesting full screen by
blocking these properties from `Document.prototype` on specified browsers:

- `exitFullscreen` [Chrome, Edge, Firefox]
- `fullscreen` [Chrome, Edge, Firefox]
- `fullscreenElement` [Chrome, Edge, Firefox]
- `fullscreenEnabled` [Chrome, Edge, Firefox]
- `mozCancelFullScreen` [Firefox]
- `mozFullScreen` [Firefox]
- `mozFullScreenElement` [Firefox]
- `mozFullScreenEnabled` [Firefox]
- `mozRequestFullScreen` [Firefox]
- `onfullscreenchange` [Chrome, Edge, Firefox]
- `onfullscreenerror` [Chrome, Edge, Firefox]
- `onmozfullscreenchange` [Firefox]
- `onmozfullscreenerror` [Firefox]
- `requestFullscreen` [Chrome, Edge, Firefox]
- `webkitFullScreenKeyboardInputAllowed` [Safari]

<hr>
<a name="documentdocsblocked-properties-onrejectionhandledmd"></a>

## Document.prototype.onrejectionhandled and Document.prototype.onunhandledrejection [Safari]

The [`WindowEventHandlers`](https://html.spec.whatwg.org/#windoweventhandlers) mixin describes the event handlers common to several interfaces like `Window`, or `HTMLBodyElement` and `HTMLFrameSetElement`. Each of these interfaces can implement additional specific event handlers.

The [`WindowEventHandlers.onrejectionhandled`](https://developer.mozilla.org/en-US/docs/Web/API/WindowEventHandlers/onrejectionhandled) property is an event handler representing the code to be called when the `rejectionhandled` event is raised, indicating that a Promise was rejected and the rejection has been handled. The event is sent to the script's global scope.

The [`WindowEventHandlers.onunhandledrejection`](https://developer.mozilla.org/en-US/docs/Web/API/WindowEventHandlers/onunhandledrejection) property is an event handler representing the code to be called when the `unhandledrejection` event is raised, indicating that a Promise was rejected but the rejection was not handled. The code handles the event that's sent to the script's global scope when a Promise is rejected, and there is no handler for the rejection.

While most events are DOM related, these event handlers receive an event object containing information about the rejected promise, including the `type`, `promise`, and `reason` properties. Malicious code that accesses the event handler properties can look into the promise info.

### Distorted Behavior

This distortion blocks access to `Document.prototype.onrejectionhandled` and `Document.prototype.onunhandledrejection` in Safari.

<hr>
<a name="documentdocsblocked-properties-onsecuritypolicyviolationmd"></a>

## onsecuritypolicyviolation

The [`onsecuritypolicyviolation`](https://developer.mozilla.org/en-US/docs/Web/API/Element/securitypolicyviolation_event) event is fired when a Content Security Policy is violated.

### Distorted Behavior

This distortion blocks assignment to `onsecuritypolicyviolation`.
<hr>
<a name="documentdocsblocked-properties-parsehtmlunsafemd"></a>

## Document.prototype.parseHTMLUnsafe

The [`Document.prototype.parseHTMLUnsafe()`](https://developer.mozilla.org/en-US/docs/Web/API/Document/parseHTMLUnsafe_static) static method of the `Document` object is used to parse a string of HTML, which may contain declarative shadow roots, in order to create a new `Document` instance.

### Distorted Behavior

This distortion blocks access to `Document.prototype.parseHTMLUnsafe`.<hr>
<a name="documentdocsblocked-properties-releasecapture-valuemd"></a>

## Document.prototype.releaseCapture

The [`Document.prototype.releaseCapture()`](https://developer.mozilla.org/en-US/docs/Web/API/Document/releaseCapture) method releases mouse capture if it's currently enabled on an element within this document. When mouse capture is released, mouse events are no longer directed to the element on which capture is enabled.

Malicious code can use the `releaseCapture` API for phishing attacks.

### Distorted Behavior

This distortion blocks access to `Document.prototype.releaseCapture` in Firefox.
<hr>
<a name="documentdocsblocked-properties-releaseevents-valuemd"></a>

## Document.prototype.releaseEvents

The [`Document.prototype.releaseEvents()`](https://developer.mozilla.org/en-US/docs/Web/API/Window/releaseEvents) releases the window from trapping events of a specific type.

Malicious code can use the `releaseEvents` API for phishing attacks.

### Distorted Behavior

This distortion blocks access to `Document.prototype.releaseEvents` in Firefox.
<hr>
<a name="documentdocsblocked-properties-write-valuemd"></a>

## Document.prototype.write

The [`Document.prototype.write()`](https://developer.mozilla.org/en-US/docs/Web/API/Document/write) method writes a string of text to a document stream opened by `document.open()`.

Malicious code can use `document.write` to write arbitrary JavaScript code directly into the document, which can bypass Lightning Web Security distortions and access the raw window.

### Distorted Behavior

This distortion blocks access to `Document.prototype.write`.
<hr>
<a name="documentdocsblocked-properties-writeln-valuemd"></a>

## Document.prototype.writeln

The [`Document.prototype.writeln()`](https://developer.mozilla.org/en-US/docs/Web/API/Document/writeln) method writes a string of text followed by a newline character to a document.

Malicious code can use `document.writeln` to write arbitrary JavaScript code directly into the document, which can bypass Lightning Web Security distortions and access the raw window.

### Distorted Behavior

This distortion blocks access to `Document.prototype.writeln`.
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

On Firefox the distortion throws an exception instead of SecurityError.

On Chrome, Safari and Edge (Webkit) it throws an exception instead of allowing the setter to execute.
<hr>
<a name="documentdocsexeccommand-valuemd"></a>

## Document.prototype.execCommand

When an HTML document has been switched to `designMode`, its `document` object exposes an [`execCommand()`](https://developer.mozilla.org/en-US/docs/Web/API/Document/execCommand) method to run commands that manipulate the current editable region, such as form inputs or `contentEditable` elements.

The `insertHTML` command inserts new elements on the currently active editable element.

The `selectAll` command selects all of the content of the editable region.

Lightning Web Security runs in the main window, where the `<html>`, `<head>` and `<body>` elements are shared. If malicious code can insert any specified text as HTML into the DOM tree, even outside of the shared `<head>` and `<body>` elements, it can pollute the DOM. For this reason, any elements added to this shared DOM are sanitized to strip out malicious code.
### Distorted Behavior

- For `insertHTML` commands, this distortion sanitizes the inserted HTML string.
- For `selectAll` commands, this distortion blocks selecting all contents if the document is the top-level document.
<hr>
<a name="documentdocsonsecuritypolicyviolation-settermd"></a>

## Document "securitypolicyviolation" event

The [securitypolicyviolation](https://developer.mozilla.org/en-US/docs/Web/API/Element/securitypolicyviolation_event) event is fired when a Content Security Policy is violated.

The event is fired on the element that violates the policy and bubbles. It is normally handled by an event handler on the `Window` or `Document` object.

The handler can be assigned using the `onsecuritypolicyviolation` property or using `EventTarget.addEventListener()`.

The event object associated with the `securitypolicyviolation` event exposes a property called `originalPolicy` which contains the `nonce` value. Malicious code with access to the `nonce` value can use it to bypass the Content Security Policy that determines whether a given script is allowed to proceed, and then run inline scripts.

### Distorted Behavior

Currently, Lightning Web Security doesn't support the `securitypolicyviolation` event, so setting the `onsecuritypolicyviolation` property, or adding a `securitypolicyviolation` event listener is not allowed and throws an exception.
<hr>
<a name="documentdocsopen-valuemd"></a>

## Document.prototype.open

The [`document.open()`](https://developer.mozilla.org/en-US/docs/Web/API/Document/open) method opens a document for writing.

The `document.open()` method normally takes no arguments. However, there is a lesser-known variation: if you pass three arguments, `document.open()` acts as an alias for `window.open()`. This new window context is not sandboxed properly and malicious code can access system mode, so Lightning Web Security must apply a distortion to prevent such access.

### Distorted Behavior

When `document.open()` is invoked with zero arguments, the distortion throws an exception.

When `document.open()` is invoked with three arguments, the returned `window` object has the same distortions applied to it as the originating sandbox. `eval`, `Function`, `setInterval` and `setTimeout` are blocked.
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

This distortion restricts access to the element's `shadowRoot` property. Only code that's running in the same sandbox can access the property.
<hr>
<a name="elementdocsbefore-valuemd"></a>

## Element.prototype.before

The [`Element.prototype.before()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/before) method inserts a set of `Node` objects or `DOMString` objects before the `Element` in the child list of the parent of the `Element`. `DOMString` objects are inserted as equivalent `Text` nodes.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can add nodes or text before those shared elements, corrupting the DOM of the current rendered page.

### Distorted Behavior

This distortion allows only a `<script>` or `<link>` element to be added after `<html>`, `<head>`, and `<body>` elements. It throws an exception if any other element is specified.
<hr>
<a name="elementdocsblocked-properties-fullscreenmd"></a>

## Fullscreen API: Element.prototype

The [Fullscreen API](https://developer.mozilla.org/en-US/docs/Web/API/Fullscreen_API) adds methods to present a specific `Element` (and its descendants) in full-screen mode, and to exit full-screen mode when it is no longer needed. This API makes it possible to present desired content such as an online game, using the user's entire screen. Full-screen mode removes all browser user interface elements and other applications from the screen until full-screen mode is shut off.

It is supported by all major browsers, with varying implementations.

This API doesn't adjust the DOM in the element. Instead, the native fullscreen hooks onto the browser. Malicious code can use the fullscreen API for phishing attacks. For example, because the fullscreen API obscures the browser's address bar, malicious code can hide the fake URL of a phishing page. Malicious coders can also fake an address bar with their own DOM.

### Distorted Behavior

This distortion prevents code from requesting full screen by
blocking these properties from `Element.prototype` on specified browsers:

- `mozRequestFullScreen` [Firefox]
- `onfullscreenchange` [Chrome, Edge, Firefox]
- `onfullscreenerror` [Chrome, Edge, Firefox]
- `requestFullscreen` [Chrome, Edge, Firefox]
- `webkitRequestFullscreen` [Chrome, Edge, Safari]
- `webkitRequestFullScreen` [Chrome, Edge, Safari]
<hr>
<a name="elementdocsblocked-properties-sethtmlunsafemd"></a>

## Element.prototype.setHTMLUnsafe

The [`Element.prototype.setHTMLUnsafe()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/setHTMLUnsafe) method is used to parse a string of HTML into a `DocumentFragment`, which then replaces the element's subtree in the DOM. The input HTML may include declarative shadow roots. It should be used instead of `Element.innerHTML` for inserting untrusted strings of HTML into an element.

### Distorted Behavior

This distortion blocks the use of `Element.prototype.setHTMLUnsafe()`.
<hr>
<a name="elementdocsgetinnerhtml-valuemd"></a>

## Element.prototype.getInnerHTML

The `Element.prototype.getInnerHTML` property gets the HTML or XML markup contained within the element.

LWC's utilization of a synthetic shadow results in shadows that appear to be closed, but are actually open. To obtain the `innerHTML` of such open shadows, one can retrieve it by utilizing `getInnerHTML` on elements that are the parent of the shadow, with the `includeShadowRoots` option set to `true`.

### Distorted Behavior

This distortion sets the `includeShadowRoots` option from `true` to `false`.
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
<a name="elementdocssethtml-valuemd"></a>

## Element.prototype.setHTML

The [`Element.prototype.setHTML()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/setHTML) method is used to parse and sanitize a string of HTML and then insert it into the DOM as a subtree of the element. It should be used instead of `Element.innerHTML` for inserting untrusted strings of HTML into an element.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can prepend nodes or text directly to shared `<head>` and `<body>` elements, corrupting the DOM of the current rendered page.

### Distorted Behavior

This distortion sanitizes and prevents HTML from replacing the DOM within shared `<head>` and `<body>` elements.
<hr>
<a name="elementdocsshadowroot-gettermd"></a>

## Element.prototype.shadowRoot getter

The [`Element.prototype.shadowRoot`](https://developer.mozilla.org/en-US/docs/Web/API/Element/shadowRoot) read-only property represents the shadow root hosted by the element.

This property allows retrieving the shadow DOM of custom elements created with `attachShadow({mode: 'open'})`.


### Distorted Behavior

This distortion returns `null` when you try to access an element's `shadowRoot` property from outside of the sandbox that it was created in. Elements or `shadowRoot` objects that are passed as function arguments are not protected.
<hr>
<a name="eventdocsblocked-properties-explicitoriginaltarget-valuemd"></a>

## Event.prototype.explicitOriginalTarget

The read-only ['explicitOriginalTarget'](https://developer.mozilla.org/en-US/docs/Web/API/Event/explicitOriginalTarget) property of the `Event` interface returns the non-anonymous original target of the event.

The Firefox only `explicitOriginalTarget` property of an event object can be used by malicious code to gain cross-component access to elements.

### Distorted Behavior

This distortion blocks access to `Event.prototype.explicitOriginalTarget`.
<hr>
<a name="eventdocsblocked-properties-originaltarget-valuemd"></a>

## Event.prototype.originalTarget

The read-only [`originalTarget`](https://developer.mozilla.org/en-US/docs/Web/API/Event/originalTarget) property of the `Event` interface returns the original target of the event before any retargetings. Unlike `Event.prototype.explicitOriginalTarget` it can also be native anonymous content.

The Firefox only `originalTarget` property of an event object can be used by malicious code to gain cross-component access to elements.

### Distorted Behavior

This distortion blocks access to `Event.prototype.originalTarget`.
<hr>
<a name="eventdocscomposedpath-valuemd"></a>

## Event.prototype.composedPath

The [`Event.prototype.composedPath()`](https://developer.mozilla.org/en-US/docs/Web/API/Event/composedPath) method returns the event's path which is an array of objects on which listeners will be invoked. This does not include nodes in shadow trees if the shadow root was created with its `ShadowRoot.mode` closed.

### Distorted Behavior

This distortion returns an array of the objects on which listeners will be invoked, up to the closed custom element itself. The array doesn't include the shadow root, or nodes inside the shadow root.
<hr>
<a name="functiondocsfunction-valuemd"></a>

## Function Constructor

The [`Function()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function) constructor creates a new Function object that execute JavaScript code represented as a string in the global scope only.

### Distorted Behavior

This distortion ensures that code is evaluated in the executing sandbox's global object context.
<hr>
<a name="htmlbodyelementdocsonrejectionhandled-settermd"></a>

## HTMLBodyElement "rejectionhandled" event

The [rejectionhandled](https://developer.mozilla.org/en-US/docs/Web/API/Window/rejectionhandled_event) event is sent to the script's global scope (usually window but also Worker) whenever a rejected JavaScript Promise is handled late, such as when a handler is attached to the promise after its rejection had caused an `unhandledrejection` event.

This can be used in debugging and for general application resiliency, in tandem with the `unhandledrejection` event, which is sent when a promise is rejected but there is no handler for the rejection at the time.

The event object associated with the `rejectionhandled` event exposes a property called `reason`, which can contain sensitive information.

### Distorted Behavior

Currently, Lightning Web Security doesn't support setting the `onrejectionhandled` event handler or adding a `rejectionhandled` event listener; attempting to do so throws an exception.
<hr>
<a name="htmlbodyelementdocsonstorage-settermd"></a>

## HTMLBodyElement "storage" event

The [`storage`](https://developer.mozilla.org/en-US/docs/Web/API/Window/storage_event) event of the `Window` interface fires when a storage area (such as `localStorage`) has been modified in the context of another document.

The `storage` event object exposes `key`, `newValue`, `oldValue`, `storageArea` and `url` data, which can contain sensitive information.

### Distorted Behavior

Currently, Lightning Web Security doesn't support setting the `onstorage` event handler or adding a `storage` event listener; attempting to do so throws an exception.
<hr>
<a name="htmlbodyelementdocsonunhandledrejection-settermd"></a>

## HTMLBodyElement "unhandledrejection" event

The [unhandledrejection](https://developer.mozilla.org/en-US/docs/Web/API/Window/unhandledrejection_event) event is sent to the global scope of a script when a JavaScript Promise that has no rejection handler is rejected; typically, this is the window, but may also be a Worker.

This is useful for debugging and for providing fallback error handling for unexpected situations.

The event object associated with the `unhandledrejection` event exposes a property called `reason`, which can contain sensitive information.

### Distorted Behavior

Currently, Lightning Web Security doesn't support setting the `onunhandledrejection` event handler or adding a `unhandledrejection` event listener; attempting to do so throws an exception.
<hr>
<a name="htmlelementdocsblocked-properties-noncemd"></a>

## HTMLElement.prototype.nonce

The [`HTMLElement.prototype.nonce`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/nonce) property returns an element's cryptographic nonce (number used once) that is used by Content Security Policy to determine whether a given fetch will be allowed to proceed.

Lightning Web Security doesn't allow the use of inline scripts even when a nonce is used. Malicious code with access to the `nonce` value can use it to bypass the Content Security Policy that determines whether a given script is allowed to proceed, and then run inline scripts.

### Distorted Behavior

This distortion blocks access to `HTMLElement.prototype.nonce` in Chrome, Edge.<hr>
<a name="htmlelementdocsblocked-properties-onrejectionhandledmd"></a>

## HTMLElement.prototype.onrejectionhandled and HTMLElement.prototype.onunhandledrejection [Safari]

The [`WindowEventHandlers`](https://html.spec.whatwg.org/#windoweventhandlers) mixin describes the event handlers common to several interfaces like `Window`, or `HTMLBodyElement` and `HTMLFrameSetElement`. Each of these interfaces can implement additional specific event handlers.

The [`WindowEventHandlers.onrejectionhandled`](https://developer.mozilla.org/en-US/docs/Web/API/WindowEventHandlers/onrejectionhandled) property is an event handler representing the code to be called when the `rejectionhandled` event is raised, indicating that a Promise was rejected and the rejection has been handled. The event is sent to the script's global scope.

The [`WindowEventHandlers.onunhandledrejection`](https://developer.mozilla.org/en-US/docs/Web/API/WindowEventHandlers/onunhandledrejection) property is an event handler representing the code to be called when the `unhandledrejection` event is raised, indicating that a Promise was rejected but the rejection was not handled. The code handles the event that's sent to the script's global scope when a Promise is rejected, and there is no handler for the rejection.

While most events are DOM related, these event handlers receive an event object containing information about the rejected promise, including the `type`, `promise`, and `reason` properties. Malicious code that accesses the event handler properties can look into the promise info.

### Distorted Behavior

This distortion blocks access to `HTMLElement.prototype.onrejectionhandled` and `HTMLElement.prototype.onunhandledrejection` in Safari.

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
<a name="htmlembedelementdocsblocked-properties-getsvgdocument-valuemd"></a>

## HTMLEmbedElement.prototype.getSVGDocument

The [`HTMLEmbedElement.prototype.getSVGDocument()`](https://developer.mozilla.org/en-US/docs/Web/SVG/Scripting) method returns the XMLDocument representing the element's embedded SVG or null if the element doesn't represent an SVG document.

Malicious code can use `getSVGDocument` of an SVG element to bypass Lightning Web Security distortions and access the raw window.

### Distorted Behavior

This distortion blocks access to `HTMLEmbedElement.prototype.getSVGDocument`.
<hr>
<a name="htmlframesetelementdocsonrejectionhandled-settermd"></a>

## HTMLFrameSetElement "rejectionhandled" event

The [rejectionhandled](https://developer.mozilla.org/en-US/docs/Web/API/Window/rejectionhandled_event) event is sent to the script's global scope (usually window but also Worker) whenever a rejected JavaScript Promise is handled late, such as when a handler is attached to the promise after its rejection had caused an `unhandledrejection` event.

This can be used in debugging and for general application resiliency, in tandem with the `unhandledrejection` event, which is sent when a promise is rejected but there is no handler for the rejection at the time.

The event object associated with the `rejectionhandled` event exposes a property called `reason`, which can contain sensitive information.

### Distorted Behavior

Currently, Lightning Web Security doesn't support setting the `onrejectionhandled` event handler or adding a `rejectionhandled` event listener; attempting to do so throws an exception.
<hr>
<a name="htmlframesetelementdocsonstorage-settermd"></a>

## HTMLFrameSetElement "storage" event

The [`storage`](https://developer.mozilla.org/en-US/docs/Web/API/Window/storage_event) event of the `Window` interface fires when a storage area (such as `localStorage`) has been modified in the context of another document.

The event object associated with the `storage` event exposes `key`, `newValue`, `oldValue`, `storageArea` and `url` data, which can contain sensitive information.

### Distorted Behavior

Currently, Lightning Web Security doesn't support setting the `onstorage` event handler or adding a `storage` event listener; attempting to do so throws an exception.
<hr>
<a name="htmlframesetelementdocsonunhandledrejection-settermd"></a>

## HTMLFrameSetElement "unhandledrejection" event

The [unhandledrejection](https://developer.mozilla.org/en-US/docs/Web/API/Window/unhandledrejection_event) event is sent to the global scope of a script when a JavaScript Promise that has no rejection handler is rejected; typically, this is the window, but may also be a Worker.

This is useful for debugging and for providing fallback error handling for unexpected situations.

The event object associated with the `unhandledrejection` event exposes a property called `reason`, which can contain sensitive information.

### Distorted Behavior

Currently, Lightning Web Security doesn't support setting the `onunhandledrejection` event handler or adding a `unhandledrejection` event listener; attempting to do so throws an exception.
<hr>
<a name="htmliframeelementdocsblocked-properties-getsvgdocument-valuemd"></a>

## HTMLIFrameElement.prototype.getSVGDocument

The [`getSVGDocument()`](https://developer.mozilla.org/en-US/docs/Web/SVG/Scripting) method returns the XMLDocument representing the element's embedded SVG or null if the element doesn't represent an SVG document.

Malicious code can use `getSVGDocument` of an SVG element to bypass Lightning Web Security distortions and access the raw window.

### Distorted Behavior

This distortion blocks access to `HTMLIFrameElement.prototype.getSVGDocument`.
<hr>
<a name="htmliframeelementdocsblocked-properties-srcdocmd"></a>

## HTMLIFrameElement.prototype.srcdoc

The [`HTMLIFrameElement.prototype.srcdoc`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLIFrameElement/srcdoc) property of the HTMLIFrameElement specifies the content of the page.

Malicious code can set `srcdoc` to some string that contains arbitrary JavaScript code that can bypass Lightning Web Security distortions and access the raw window.

### Distorted Behavior

This distortion blocks access to `HTMLIFrameElement.prototype.srcdoc`.
<hr>
<a name="htmliframeelementdocssrc-settermd"></a>

## HTMLIFrameElement.prototype.src setter

The [`HTMLIFrameElement.prototype.src`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLIFrameElement/src) property reflects the HTML `referrerpolicy` attribute of the `<iframe>` element defining which referrer is sent when fetching the resource. The `src` value is a string that reflects the `src` HTML attribute, containing the address of the content to be embedded.

Lightning Web Security restricts the `src` attribute to values that use the `http://`, `https://`, and `about:blank` schemes, or relative urls. URL schemes like `javascript://` aren't allowed.

### Distorted Behavior

This distortion throws an exception for values that don't sanitize to `http://`, `https://`, and `about:blank` schemes, or relative urls.
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
<a name="htmlobjectelementdocsblocked-properties-getsvgdocument-valuemd"></a>

## HTMLObjectElement.prototype.getSVGDocument

The [`HTMLObjectElement.prototype.getSVGDocument()`](https://developer.mozilla.org/en-US/docs/Web/SVG/Scripting) method returns the XMLDocument representing the element's embedded SVG or null if the element doesn't represent an SVG document.

Malicious code can use `getSVGDocument` of an SVG element to bypass Lightning Web Security distortions and access the raw window.

### Distorted Behavior

This distortion blocks access to `HTMLObjectElement.prototype.getSVGDocument`.
<hr>
<a name="htmlobjectelementdocsdata-settermd"></a>

## HTMLObjectElement.prototype.data setter

The [`HTMLObjectElement.prototype.data`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLObjectElement/data) property of the `HTMLObjectElement` interface returns a string that reflects the `data` HTML attribute, specifying the address of a resource's data.

Lightning Web Security restricts the `data` attribute to values that use the `http://`, `https://`, and `about:blank` schemes, or relative urls. URL schemes like `javascript://` aren't allowed. LWS also prevents access to URL endpoints containing `"/aura"` and `"/webruntime"` because they are part of the Lightning Component framework.

### Distorted Behavior

This distortion throws an exception for values that don't sanitize to `http://`, `https://`, and `about:blank` schemes, or relative urls. It will also throw an exception for values that  contain the `"/aura"` and `"/webruntime"` endpoints.
<hr>
<a name="htmlscriptelementdocsblocked-properties-noncemd"></a>

## HTMLScriptElement.prototype.nonce

The [`HTMLScriptElement.prototype.nonce`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLScriptElement) property returns an element's cryptographic nonce (number used once) that is used by Content Security Policy to determine whether a given fetch will be allowed to proceed.

Lightning Web Security doesn't allow the use of inline scripts even when a nonce is used. Malicious code with access to the `nonce` value can use it to bypass the Content Security Policy that determines whether a given script is allowed to proceed, and then run inline scripts.

### Distorted Behavior

This distortion blocks access to `HTMLScriptElement.prototype.nonce` in Chrome, Edge.
<hr>
<a name="htmlscriptelementdocssrc-settermd"></a>

## HTMLScriptElement.prototype.src setter

[`HTMLScriptElement.prototype.src`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLScriptElement) property is a `DOMString` representing the URL of an external script. It reflects the `src` attribute of the `script` element specifying the URL to an external script.

To ensure that JavaScript code loaded through a `script` element runs in the sandbox, Lightning Web Security evaluates the source text in the same sandbox before the browser evaluates it. This prevents the native behavior of the `script` element from triggering.

### Distorted Behavior

This distortion prevents a script from running before LWS can evaluate it.
<hr>
<a name="htmlscriptelementdocstext-settermd"></a>

## HTMLScriptElement.prototype.text setter

The [`HTMLScriptElement.prototype.text`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLScriptElement) is a string that joins and returns the contents of all Text nodes inside the <script> element (ignoring other nodes like comments) in tree order. On setting, it acts the same way as the textContent IDL attribute.

You can set `HTMLScriptElement.prototype.text` to replace DOM inside the element with nodes parsed from the given specified text as HTML.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. Malicious code can replace the DOM of those shared elements, corrupting the DOM of the current rendered page.

### Distorted Behavior

When setting the value of this property on a script element, this distortion will force the script to be evaluated in the sandbox that created the element.

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
<a name="rangedocsprototype-valuemd"></a>

## Range.prototype.*

The `Range` interface represents a fragment of a document that can contain nodes and parts of text nodes.

- The [`Range.prototype.setEnd()`](https://developer.mozilla.org/en-US/docs/Web/API/Range/setEnd) method sets the end position of a `Range` to be located at the given offset into the specified node x. Setting the end point above (higher in the document) than the start point will result in a collapsed range with the start and end points both set to the specified end position.
- The [`Range.prototype.selectNode()`](https://developer.mozilla.org/en-US/docs/Web/API/Range/selectNode) method sets the `Range` to contain the `Node` and its contents. The parent `Node` of the start and end of the `Range` will be the same as the parent of the `referenceNode`.
- The [`Range.prototype.selectNodeContents()`]() method sets the `Range` to contain the contents of a `Node`.
- The [`Range.prototype.setEndAfter()`]() method sets the end position of a `Range` relative to another `Node`. The parent `Node` of end of the `Range` will be the same as that for the `referenceNode`.
- The [`Range.prototype.setEndBefore()`]() method sets the end position of a `Range` relative to another `Node`. The parent `Node` of end of the `Range` will be the same as that for the `referenceNode`.
- The [`Range.prototype.setStart()`]() method sets the start position of a `Range`.
- The [`Range.prototype.setStartAfter()`]() method sets the start position of a `Range` relative to a `Node`. The parent `Node` of the start of the `Range` will be the same as that for the `referenceNode`.
- The [`Range.prototype.setStartBefore()`]() method sets the start position of a `Range` relative to another `Node`. The parent `Node` of the start of the `Range` will be the same as that for the `referenceNode`.
- The [`Range.prototype.surroundContents()`]() method moves content of the `Range` into a new node, placing the new node at the start of the specified range.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. These methods would allow a shared element to be included in a range, which would in turn allow malicious code to access shared elements. LWS prevents these methods from including shared elements in a range.

### Distorted Behavior

This distortion prevents `setEnd()`, `selectNode()`, `selectNodeContents()`, `setEndAfter()`, `setEndBefore()`, `setStart()`, `setStartAfter()`, `setStartBefore()`, and `surroundContents()` from including any shared elements in a range.


<hr>
<a name="svganimateelementdocsattributename-attributemd"></a>

## SVGAnimateElement: "attributeName" attribute

The [`attributeName`](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/attributeName) attribute indicates the name of the CSS property or attribute of the target element that is going to be changed during an animation.

When you set the `attributeName` to `href`, the element accesses an SVG resource specified with the `from`, `to`, or `value` attribute. Malicious code can bypass Lightning Web Security with an `<iframe>` or `<script>` element inside the SVG resource and run code outside the sandbox. 

This distortion applies when the code sets `href` on the `attributeName` attribute after setting the `from`, `to`, or `value` attribute.

### Distorted Behavior

This distortion sanitizes SVG files that are passed with `from`, `to`, or `value` attributes of the `<animate>` element.

<hr>
<a name="svganimateelementdocsfrom-attributemd"></a>

## SVGAnimateElement: "from" attribute

The [`from`](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/From) attribute indicates the initial value of the attribute that will be modified during the animation.

When used with the `to` attribute, the animation will change the modified attribute from the `from` value to the `to` value. When used with the `by` attribute, the animation will change the attribute relatively from the `from` value by the value specified in `by`.

When you set the SVG resource dynamically with the `from` attribute, the SVG resource isn't sanitized. Malicious code can bypass Lightning Web Security with an `<iframe>` or `<script>` element inside the SVG resource and  run code outside the sandbox. 

### Distorted Behavior

This distortion sanitizes SVG files that are passed with the `from` attribute of the `<animate>` element.
<hr>
<a name="svganimateelementdocsto-attributemd"></a>

## SVGAnimateElement: "to" attribute

The [`to`](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/To) attribute indicates the final value of the attribute that will be modified during the animation.

The value of the attribute will change between the `from` attribute value and this value.

When you set the SVG resource dynamically with the `to` attribute, the SVG resource isn't sanitized. Malicious code can bypass Lightning Web Security with an `<iframe>` or `<script>` element inside the SVG resource and run code outside the sandbox. 

### Distorted Behavior

This distortion sanitizes SVG files that are passed with the `to` attribute of the `<animate>` element.

<hr>
<a name="svganimateelementdocsvalues-attributemd"></a>

## SVGAnimateElement: "values" attribute

The [`values`](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/values#animate_animatecolor_animatemotion_animatetransform) attribute provides a list of values defining the sequence of values over the course of the animation. If this attribute is specified, any `from`, `to`, and `by` attribute values set on the element are ignored.

When you set the SVG resource dynamically with the `values` attribute, the SVG resource isn't sanitized. Malicious code can bypass Lightning Web Security with an `<iframe>` or `<script>` element inside the SVG resource and run code outside the sandbox.

### Distorted Behavior

This distortion sanitizes SVG files that are passed with the `values` attribute of the `<animate>` element.
<hr>
<a name="svgelementdocsblocked-properties-noncemd"></a>

## SVGElement.prototype.nonce

The [`SVGElement.prototype.nonce`](https://developer.mozilla.org/en-US/docs/Web/API/SVGElement) property returns an element's cryptographic nonce (number used once) that is used by Content Security Policy to determine whether a given fetch will be allowed to proceed.

Lightning Web Security doesn't allow the use of inline scripts even when a nonce is used. Malicious code with access to the `nonce` value can use it to bypass the Content Security Policy that determines whether a given script is allowed to proceed, and then run inline scripts.

### Distorted Behavior

This distortion blocks access to `SVGElement.prototype.nonce` in Chrome, Edge.
<hr>
<a name="svgscriptelementdocshref-settermd"></a>

## SVGScriptElement.prototype.href setter

The [`SVGScriptElement.prototype.href`](https://developer.mozilla.org/en-US/docs/Web/API/SVGScriptElement) property is an `SVGAnimatedString` corresponding to the `href` or `xlink:href` attribute of the given `<script>` element.

The `SVGScriptElement.prototype.href` property reflects the `href` attribute of a `<script>` element inside an `<svg>` element, specifying the URL to an external script.

The default value for `href` is `undefined` in the `SVGScriptElement.prototype`. Access to the raw `window` object could be attained by running scripts using the SVG `<script>` element.

To ensure that JavaScript code loaded through an SVG `<script>` element runs in the sandbox, Lightning Web Security evaluates the script source in the same sandbox before the browser evaluates it. This preemptive evaluation prevents the native behavior of the SVG `<script>` element from triggering.

### Distorted Behavior

This distortion for the `href` or `xlink:href` getter provides a distorted version of the script to the browser.
<hr>
<a name="svgsetelementdocsattributename-attributemd"></a>

## SVGSetElement: "attributeName" attribute

The [`attributeName`](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/attributeName) attribute indicates the name of the CSS property or attribute of the target element that is going to be changed during an animation.

When you set the `attributeName` to `href`, the element accesses an SVG resource specified with the `to` attribute.  Malicious code can bypass Lightning Web Security with an `<iframe>` or `<script>` element inside the SVG resource and run code outside the sandbox. 

This distortion applies when the code sets `href` on the `attributeName` attribute after setting the `to` attribute.

### Distorted Behavior

This distortion sanitizes SVG files passed with the `to` attribute of the `<set>` element.

<hr>
<a name="svgsetelementdocsto-attributemd"></a>

## SVGSetElement: "to" attribute

The [`to`](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/To#set) attribute specifies the value for the attribute during the duration of the element.

When you set the SVG resource dynamically with the `to` attribute, the SVG resource isn't sanitized. Malicious code can bypass Lightning Web Security with an `<iframe>` or `<script>` element inside the SVG resource and run code outside of sandbox. 

### Distorted Behavior

This distortion sanitizes SVG files that are passed with the `to` attribute of the `<set>` element.

<hr>
<a name="svguseelementdocshref-attributemd"></a>

## SVGUseElement: "href" attribute

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
<a name="selectiondocscollapse-valuemd"></a>

## Selection.prototype.collapse

The [`collapse()`](https://developer.mozilla.org/en-US/docs/Web/API/Selection/collapse) method collapses the current selection to a single point. The document is not modified. If the content is focused and editable, the caret will blink there.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. The `collapse()` method allows setting the selection to a shared element which could be used to malaciously modify the document.

### Distorted Behavior

This distortion prevents `collapse()` from setting the selection to a shared element.
<hr>
<a name="selectiondocsextend-valuemd"></a>

## Selection.prototype.extend

The [`extend()`](https://developer.mozilla.org/en-US/docs/Web/API/Selection/extend) method moves the focus of the selection to a specified point. The anchor of the selection does not move. The selection will be from the anchor to the new focus, regardless of direction.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. The `extend()` method allows setting the selection to a shared element which could be used to malaciously modify the document.

### Distorted Behavior

This distortion prevents `extend()` from setting the selection to a shared element.
<hr>
<a name="selectiondocsselectallchildren-valuemd"></a>

## Selection.prototype.selectAllChildren

The [`selectAllChildren()`](https://developer.mozilla.org/en-US/docs/Web/API/Selection/selectAllChildren) method adds all the children of the specified node to the selection. Previous selection is lost.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. The `selectAllChildren()` method allows setting the selection to a shared element which could be used to malaciously modify the document.

### Distorted Behavior

This distortion prevents `selectAllChildren()` from setting the selection to a shared element.
<hr>
<a name="selectiondocssetbaseandextent-valuemd"></a>

## Selection.prototype.setBaseAndExtent

The [`setBaseAndExtent()`](https://developer.mozilla.org/en-US/docs/Web/API/Selection/setBaseAndExtent) method of the Selection interface sets the selection to be a range including all or parts of two specified DOM nodes, and any content located between them.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. The `setBaseAndExtent()` method allows setting the selection to a shared element which could be used to malaciously modify the document.

### Distorted Behavior

This distortion prevents `setBaseAndExtent()` from setting the selection to a shared element.
<hr>
<a name="selectiondocssetposition-valuemd"></a>

## Selection.prototype.setPosition

The [`setPosition()`](https://developer.mozilla.org/en-US/docs/Web/API/Selection/setPosition) method collapses the current selection to a single point. The document is not modified. If the content is focused and editable, the caret will blink there.

Lightning Web Security runs in the main window, where the `<html>`, `<head>`, and `<body>` elements are shared. The `setPosition()` method allows setting the selection to a shared element which could be used to malaciously modify the document.

### Distorted Behavior

This distortion prevents `setPosition()` from setting the selection to a shared element.
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
<a name="uieventdocsblocked-properties-rangeparent-valuemd"></a>

## UIEvent.prototype.rangeParent

There is no associated documentation page for UIEvent.prototype.rangeParent on [MDN](https://developer.mozilla.org/)

The Firefox only `rangeParent` property of an event object can be used by malicious code to gain cross-component access to elements.

### Distorted Behavior

This distortion blocks access to `UIEvent.prototype.rangeParent`.
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
document.body.append(iframe);
```

Without protection from Lightning Web Security, upon loading the content of the `iframe`, the browser runs the code in the `<script>` tag which bypasses the sandbox. If the code is running on the same domain, it gains access to all cookies and displays them in a popup window.

To guard against exploits, Lightning Web Security fetches the content of the URL and scans `Blob` and `File` objects that have their MIME type set to `text/html`, `image/svg+xml` or `text/xml`. If malicious content is detected, the code doesn't execute.

### Distorted Behavior

This distortion throws an exception when MIME types `text/html`, `text/xml`, `image/svg+xml` are used with `Blob` or `File` objects that try to load malicious content: `Lightning Web Security: Cannot 'createObjectURL' using an unsecure [object Blob]!`

If no malicious content is detected when these MIME types are used, the content is allowed to load but the distortion enforces `charset=utf-8` to prevent exploits where the browser auto-interprets charset and special characters that can lead to XSS.

For any unsupported MIME types, including `text/javascript`, the distortion throws an exception with the message `Lightning Web Security: Unsupported MIME type.`

Empty MIME types on `File` and `Blob` objects are treated as `text/plain` since browsers treat this differently.

All commonly used and non-malicious MIME types work as expected.
<hr>
<a name="windowdocsblocked-properties-findmd"></a>

## Window.find

The [`Window.find()`](https://developer.mozilla.org/en-US/docs/Web/API/Window/find) method finds a string in a window sequentially.

Malicious code can use `window.find()` to access content across namespaces.

### Distorted Behavior

This distortion blocks access to `window.find()`.<hr>
<a name="windowdocsblocked-properties-requestfilesystemmd"></a>

## Window.requestFileSystem

[`Window.requestFileSystem()`](hhttps://developer.mozilla.org/en-US/docs/Web/API/Window/requestFileSystem).

### Distorted Behavior

This distortion currently block access to `window.requestFileSystem` and all browser prefixed methods to the same API, such as `window.webkitRequestFileSystem`.<hr>
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
<a name="windowdocslength-gettermd"></a>

## window.length getter

The [`window.length`](https://developer.mozilla.org/en-US/docs/Web/API/Window/length) property returns the number of frames (either `<frame>` or `<iframe>` elements) attached to the `window` object's `document`.

### Distorted Behavior

The `window.length` property always returns `0`.

Instead of `window.length`, use the `window.frames.length` value and `window.frames` object to iterate over the list of frames (either `<frame>` or `<iframe>` elements) attached to the `document`.
<hr>
<a name="windowdocsonrejectionhandled-settermd"></a>

## Window "rejectionhandled" event

The [rejectionhandled](https://developer.mozilla.org/en-US/docs/Web/API/Window/rejectionhandled_event) event is sent to the script's global scope (usually window but also Worker) whenever a rejected JavaScript Promise is handled late, such as when a handler is attached to the promise after its rejection had caused an `unhandledrejection` event.

This can be used in debugging and for general application resiliency, in tandem with the `unhandledrejection` event, which is sent when a promise is rejected but there is no handler for the rejection at the time.

The event object associated with the `rejectionhandled` event exposes a property called `reason`, which can contain sensitive information.

### Distorted Behavior

Currently, Lightning Web Security doesn't support setting the `onrejectionhandled` event handler or adding a `rejectionhandled` event listener; attempting to do so throws an exception.
<hr>
<a name="windowdocsonsecuritypolicyviolation-settermd"></a>

## Window "securitypolicyviolation" event

The [securitypolicyviolation](https://developer.mozilla.org/en-US/docs/Web/API/Element/securitypolicyviolation_event) event is fired when a Content Security Policy is violated.

The event is fired on the element that violates the policy and bubbles. It is normally handled by an event handler on the `Window` or `Document` object.

The handler can be assigned using the `onsecuritypolicyviolation` property or using `EventTarget.addEventListener()`.

The event object associated with the `securitypolicyviolation` event exposes a property called `originalPolicy` which contains the `nonce` value. Malicious code with access to the `nonce` value can use it to bypass the Content Security Policy that determines whether a given script is allowed to proceed, and then run inline scripts.

### Distorted Behavior

Currently, Lightning Web Security doesn't support setting the `onsecuritypolicyviolation` event handler or adding a `securitypolicyviolation` event listener; attempting to do so throws an exception.
<hr>
<a name="windowdocsonstorage-settermd"></a>

## Window "storage" event

The [`storage`](https://developer.mozilla.org/en-US/docs/Web/API/Window/storage_event) event of the `Window` interface fires when a storage area (such as `localStorage`) has been modified in the context of another document.

The event object associated with the `storage` event exposes `key`, `newValue`, `oldValue`, `storageArea` and `url` data, which can contain sensitive information.

### Distorted Behavior

Currently, Lightning Web Security doesn't support setting the `onstorage` event handler or adding a `storage` event listener; attempting to do so throws an exception.
<hr>
<a name="windowdocsonunhandledrejection-settermd"></a>

## Window "unhandledrejection" event

The [unhandledrejection](https://developer.mozilla.org/en-US/docs/Web/API/Window/unhandledrejection_event)  event is sent to the global scope of a script when a JavaScript Promise that has no rejection handler is rejected; typically, this is the window, but may also be a Worker.

This is useful for debugging and for providing fallback error handling for unexpected situations.

The event object associated with the `unhandledrejection` event exposes a property called `reason`, which can contain sensitive information.

### Distorted Behavior

Currently, Lightning Web Security doesn't support setting the `onunhandledrejection` event handler or adding a `unhandledrejection` event listener; attempting to do so throws an exception.
<hr>
<a name="windowdocsopen-valuemd"></a>

## window.open

The [`window.open()`](https://developer.mozilla.org/en-US/docs/Web/API/Window/open) method loads the specified resource into a new or existing browsing context with the specified name. If the name doesn't exist, then a new browsing context is opened in a new tab or a new window, and the specified resource is loaded into it.

This new browsing context isn’t sandboxed properly and malicious code can access system mode, so Lightning Web Security distorts the `window` object returned.

### Distorted Behavior

The returned `window` object has the same distortions applied to it as the originating sandbox. `eval`, `Function`, `setInterval` and `setTimeout` are blocked.
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
<a name="xsltprocessordocsblocked-properties-transformtodocument-valuemd"></a>

## XSLTProcessor.prototype.transformToDocument

**Non-standard**: This feature is non-standard and is not on a standards track. Do not use it on production sites facing the Web: it will not work for every user. There may also be large incompatibilities between implementations and the behavior may change in the future.

`XSLTProcessor.prototype.transformToDocument(Node source, Document owner)` transforms the node source by applying the stylesheet imported using the `XSLTProcessor.prototype.importStylesheet()` function. The owner document of the resulting document fragment is the owner node.

This function can be used to parse and transform XML documents with XSLT into valid HTML documents, which can be inserted into the current DOM. By using XSLT, it is possible to create arbitrary HTML tags and therefore gain access to the raw window object.

### Distorted Behavior

This method is blocked by LWS, and an exception is thrown if code attempts to call it.
<hr>
<a name="xsltprocessordocsblocked-properties-transformtofragment-valuemd"></a>

## XSLTProcessor.prototype.transformToFragment

**Non-standard**: This feature is non-standard and is not on a standards track. Do not use it on production sites facing the Web: it will not work for every user. There may also be large incompatibilities between implementations and the behavior may change in the future.

`XSLTProcessor.prototype.transformToFragment(Node source, Document owner)` transforms the node source by applying the stylesheet imported using the `XSLTProcessor.prototype.importStylesheet()` function. The owner document of the resulting document fragment is the owner node.

This function can be used to parse and transform XML documents with XSLT into valid HTML documents, which can be inserted into the current DOM. By using XSLT, it is possible to create arbitrary HTML tags and therefore gain access to the raw window object.

### Distorted Behavior

This method is blocked by LWS, and an exception is thrown if code attempts to call it.
<hr>
<a name="evaldocseval-valuemd"></a>

## eval

The [`eval()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/eval) function evaluates JavaScript code represented as a string.

### Distorted Behavior

This distortion ensures code executes in the sandbox.
