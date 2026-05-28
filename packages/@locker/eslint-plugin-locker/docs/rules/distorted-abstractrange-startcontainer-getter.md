# Access to abstractRange.startContainer (distorted-abstractrange-startcontainer-getter)

Lightning Web Security limits `abstractRange.startContainer` access to the sandbox that the element was created in.

<!-- START generated embed: @locker/distortion/src/AbstractRange/docs/startContainer-getter.md -->
## AbstractRange.prototype.startContainer getter

The read-only [`AbstractRange.prototype.startContainer`](https://developer.mozilla.org/en-US/docs/Web/API/AbstractRange/startContainer) property of the `AbstractRange` interface returns the Node in which the end of the range is located.

This property may reference an element that is within a `ShadowRoot` that belongs to another sandbox.

### Distorted Behavior

Returns `null` if the element is within a `ShadowRoot` that belongs to another sandbox.
<!-- END generated embed, please keep comment -->
