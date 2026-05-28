# Distorted formAction Setter (distorted-formaction-setter)

For security the `HTMLButtonElement#formAction` and `HTMLInputElement#formAction` setters are distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/HTMLButtonElement/docs/formAction-setter.md -->
## HTMLButtonElement.prototype.formAction setter

The [`HTMLButtonElement.formAction`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLButtonElement/formAction) property represents the URL that processes the form submission when the button is clicked. It overrides the form's `action` attribute at submission time.

Malicious code can use the `formAction` property on submit buttons to bypass endpoint restrictions enforced on `HTMLFormElement.action`, making unauthorized requests to internal Salesforce endpoints.

### Distorted Behavior

This distortion validates the `formAction` URL before allowing it to be set. If the URL points to a disallowed endpoint, it throws a `LockerSecurityError`.
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/HTMLInputElement/docs/formAction-setter.md -->
## HTMLInputElement.prototype.formAction setter

The [`HTMLInputElement.formAction`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement/formAction) property represents the URL that processes the form submission when an `input[type="submit"]` or `input[type="image"]` element is activated. It overrides the form's `action` attribute at submission time.

Malicious code can use the `formAction` property on submit/image inputs to bypass endpoint restrictions enforced on `HTMLFormElement.action`, making unauthorized requests to internal Salesforce endpoints.

### Distorted Behavior

This distortion validates the `formAction` URL before allowing it to be set. If the URL points to a disallowed endpoint, it throws a `LockerSecurityError`.
<!-- END generated embed, please keep comment -->
