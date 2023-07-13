# Logout
This sets the user's login status to "false" whenever the user logs out.
## Sample JS
``` javascript
window.dataLayer = window.dataLayer || [];
dataLayer.push({ eventModel: null });  // Clear the previous eventModel object.
dataLayer.push({
  event: "logout",
  userModel: {
    login_status: "login_status"
});
```
## Parameter Definitions

|Field|Type|Required?|Description|Example|
| --- | --- | --- | --- | --- |
|login_status|boolean|required|Is the user logged in?|`false`|
