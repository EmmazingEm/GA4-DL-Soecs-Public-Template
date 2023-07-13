# [Sign Up](https://developers.google.com/analytics/devguides/collection/ga4/reference/events?client_type=gtm#sign_up)
This event indicates that a user has signed up for an account.

If the user is automatically logged in as a result of signing up, also fire a login event.
## Sample JS
``` javascript
window.dataLayer = window.dataLayer || [];
dataLayer.push({ eventModel: null });  // Clear the previous eventModel object.
dataLayer.push({
  event: "sign_up",
  eventModel: {
    method: "method"
  }
});
```
## Parameter Definitions

|Field|Type|Required?|Description|Example|
| --- | --- | --- | --- | --- |
|method|string|required|The method used to sign up.|`google`|
