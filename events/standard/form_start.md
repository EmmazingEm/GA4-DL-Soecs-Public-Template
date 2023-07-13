# Form Start
The first time a user interacts with a form in a session. GA4 technically tracks this automatically, but there are two reasons to prefer a custom event pushed to the data layer:
  1. There is no way to distinguish between lead-generating forms (such as contact) vs. other forms (such as sign up).
  2. GA4 will not be able to detect forms inside iframes by default.
  
## Sample JS
```javascript
window.dataLayer = window.dataLayer || [];
dataLayer.push({ eventModel: null });  // Clear the previous eventModel object.
dataLayer.push({
  event: "form_start",
  eventModel: {
    form_id: "form_id",
    form_name: "form_name",
    form_destination: "form_destination",
    form_type: "form_type"
  }
});
```

## Parameter Definitions

|Field|Type|Required?|Description|Example|
| --- | --- | --- | --- | --- |
|form_id|string|required|HTML id attribute of the `<form>` DOM element.|`ABC12434`|
|form_name|string|optional|HTML name attribute of the `<form>` DOM element.|`sign_up`|
|form_destination|string|required|URL to which the form is being submitted.|`https://example.com`|
|form_type|string|required|This will always be either lead-generating or other.|`other`|
