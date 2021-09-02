# Distorted MessageEvent#source Getter (distorted-message-event-source-getter)

For security the `MessageEvent#source` getter is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/MessageEvent/docs/source-getter.md -->
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
<!-- END generated embed please keep comment here to allow auto update -->
