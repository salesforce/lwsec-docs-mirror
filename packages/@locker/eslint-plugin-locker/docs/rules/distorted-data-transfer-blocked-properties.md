The following `DataTransfer` properties are prohibited when Lightning Web Security is enabled:
-   mozCursor
-   mozSourceNode
-   mozUserCancelled

## Rule Details

Example of **incorrect** code:

```js
window.ondrag=function(evt) { 
    const text = evt.dataTransfer.mozSourceNode; 
    text.textContent = text.textContent.replace(/☀️/, '🌑');  
} 
```
