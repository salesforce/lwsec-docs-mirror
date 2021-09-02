# Distorted Document Blocked Properties (distorted-document-blocked-properties)

For security the following `Document` properties are prohibited in Lightning Locker:
-   exitFullscreen
-   fullscreen
-   fullscreenElement
-   fullscreenEnabled
-   mozCancelFullScreen
-   mozFullScreen
-   mozFullScreenElement
-   mozFullScreenEnabled
-   onfullscreenchange
-   onfullscreenerror
-   onmozfullscreenchange
-   onmozfullscreenerror
-   onrejectionhandled
-   onsecuritypolicyviolation
-   onunhandledrejection
-   releaseCapture
-   releaseEvents
-   webkitFullScreenKeyboardInputAllowed
-   write
-   writeln

## Rule Details

Example of **incorrect** code:

```js
document.exitFullscreen();
```
