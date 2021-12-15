# Distorted HTML{IFrame|Script}Element#src Setter (distorted-html-iframe-script-element-src-setter)

For security the `HTML{IFrame|Script}Element#src` setter is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/HTMLIFrameElement/docs/src-setter.md -->
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
<!-- END generated embed please keep comment here to allow auto update -->

<!-- START generated embed: @locker/distortion/src/HTMLScriptElement/docs/src-setter.md -->
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
<!-- END generated embed please keep comment here to allow auto update -->
