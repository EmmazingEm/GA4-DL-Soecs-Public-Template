# [Login](https://developers.google.com/analytics/devguides/collection/ga4/reference/events?client_type=gtm#login)
This sets the user's login status to "true" whenever the user logs in.
## Sample JS
``` javascript
window.dataLayer = window.dataLayer || [];
dataLayer.push({ eventModel: null });  // Clear the previous eventModel object.
dataLayer.push({
  event: "login",
  eventModel: {
    method: "method"
  },
  userModel: {
    login_status: "login_status"
});
```
## Parameter Definitions

|Field|Type|Required?|Description|Example|
| --- | --- | --- | --- | --- |
|method|string|required|The method used to login.|`Google`|
|login_status|boolean|required|Is the user logged in?|`true`|
