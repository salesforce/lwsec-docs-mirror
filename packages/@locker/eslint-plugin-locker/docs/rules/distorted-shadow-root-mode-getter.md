# Distorted ShadowRoot#mode Getter (distorted-shadow-root-mode-getter)

For security the `ShadowRoot#mode` getter is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/ShadowRoot/docs/mode-getter.md -->
## ShadowRoot.prototype.mode getter

### Goal

 - To force a reported mode of 'closed'.

### Design

- Patch getter on `ShadowRoot.prototype.mode` descriptor to return `'closed'`.

### Distorted Behavior

- Each time code accesses `mode` property on any element with an attached shadow
  DOM this distortion will return `'closed'`.
<!-- END generated embed, please keep comment -->
