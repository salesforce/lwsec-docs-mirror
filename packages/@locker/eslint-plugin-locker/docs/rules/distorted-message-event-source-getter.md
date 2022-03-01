# Distorted MessageEvent#source Getter (distorted-message-event-source-getter)

For security the `MessageEvent#source` getter is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/MessageEvent/docs/source-getter.md -->
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
<!-- END generated embed, please keep comment -->
