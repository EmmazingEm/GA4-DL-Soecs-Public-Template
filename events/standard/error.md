# Error
This event fires whenever the user encounters a non-form error.
  
## Sample JS
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ eventModel: null });  // Clear the previous eventModel object.
dataLayer.push({
  event: "error",
  eventModel: {
    error_code: "error_code",
    error_message: "error_message"
  }
});
```

## Parameter Definitions

|Field|Type|Required?|Description|Example|
| --- | --- | --- | --- | --- |
|error_code|string|required|A machine or human-readable, unique code for the error type.|`404`|
|error_message|string|optional|A human-readable description of the error. Alternatively, may provide the human-readable error_code if both a machine-readable and human-readable code exist for the same error.|`Page doesn't exist.`|
