# Disallow Blocked Element Properties (blocked-element-properties)

For security the following Element properties are prohibited in Lightning Locker:
  * mozRequestFullScreen
  * onfullscreenchange
  * onfullscreenerror
  * requestFullscreen
  * webkitRequestFullScreen
  * webkitRequestFullscreen

## Rule Details

Example of **incorrect** code:

<!-- eslint-disable-next-line no-undef, no-unused-expressions -->
```js
video.onfullscreenchange;
```
