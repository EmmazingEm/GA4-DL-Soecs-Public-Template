# Form Error
This event fires whenever an error prevents a user from successfully submitting a form.
  
## Sample JS
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ eventModel: null });  // Clear the previous eventModel object.
dataLayer.push({
  event: "form_error",
  eventModel: {
    form_id: "form_id",
    form_name: "form_name",
    error_code: "error_code",
    error_message: "error_message"
  }
});
```

## Parameter Definitions

|Field|Type|Required?|Description|Example|
| --- | --- | --- | --- | --- |
|form_id|string|required|HTML id attribute of the `<form>` DOM element.|`ABC12434`|
|form_name|string|optional|HTML name attribute of the `<form>` DOM element.|`sign_up`|
|error_code|string|required|A machine or human-readable, unique code for the error type.|`Invalid email.`|
|error_message|string|optional|A human-readable description of the error. Alternatively, may provide the human-readable error_code if both a machine-readable and human-readable code exist for the same error.|`Please enter a valid email address.`|
