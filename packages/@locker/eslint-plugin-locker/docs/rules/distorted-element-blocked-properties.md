# Distorted Element Blocked Properties (distorted-element-blocked-properties)

For security the following `Element` properties are prohibited in Lightning Locker:
-   mozRequestFullScreen
-   onfullscreenchange
-   onfullscreenerror
-   requestFullscreen
-   webkitRequestFullScreen
-   webkitRequestFullscreen

## Rule Details

Example of **incorrect** code:

```js
video.onfullscreenchange;
```
