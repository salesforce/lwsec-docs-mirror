# Access to abstractRange.endContainer (distorted-abstractrange-endcontainer-getter)

Lightning Web Security limits `abstractRange.endContainer` access to the sandbox that the element was created in.

<!-- START generated embed: @locker/distortion/src/AbstractRange/docs/endContainer-getter.md -->
## AbstractRange.prototype.endContainer getter

The read-only [`AbstractRange.prototype.endContainer`](https://developer.mozilla.org/en-US/docs/Web/API/AbstractRange/endContainer) property of the `AbstractRange` interface returns the Node in which the end of the range is located.

This property may reference an element that is within a `ShadowRoot` that belongs to another sandbox.

### Distorted Behavior

Returns `null` if the element is within a `ShadowRoot` that belongs to another sandbox.
<!-- END generated embed, please keep comment -->
