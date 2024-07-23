# Prevent access to certain Document properties (distorted-document-blocked-properties)

The following `Document` properties are prohibited when Lightning Web Security is enabled:
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
-   onunhandledrejection
-   parseHTMLUnsafe
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
