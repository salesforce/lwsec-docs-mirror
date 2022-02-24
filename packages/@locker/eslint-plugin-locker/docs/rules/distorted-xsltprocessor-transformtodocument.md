# Distorted XSLTProcessor.prototype.transformToDocument (distorted-xsltprocessor-transformtodocument)

For security `XSLTProcessor.prototype.transformToDocument` is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/XSLTProcessor/docs/transformToDocument-value.md -->
## XSLTProcessor.prototype.transformToDocument

**Non-standard**: This feature is non-standard and is not on a standards track. Do not use it on production sites facing the Web: it will not work for every user. There may also be large incompatibilities between implementations and the behavior may change in the future.

`XSLTProcessor.prototype.transformToDocument(Node source, Document owner)` transforms the node source by applying the stylesheet imported using the `XSLTProcessor.prototype.importStylesheet()` function. The owner document of the resulting document fragment is the owner node.

This function can be used to parse and transform XML documents with XSLT into valid HTML documents, which can be inserted into the current DOM. By using XSLT, it is possible to create arbitrary HTML tags and therefore gain access to the raw window object.

### Distorted Behavior

This method is blocked by LWS, and an exception is thrown if code attempts to call it.
<!-- END generated embed, please keep comment -->
