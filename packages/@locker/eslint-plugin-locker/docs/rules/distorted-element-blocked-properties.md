# Prevent access to certain Element properties (distorted-element-blocked-properties)

The following `Element` properties are prohibited when Lightning Web Security is enabled:
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
