# Consent Status
This event should fire with every page load and any time the user updates their consent preferences.
## Sample JS
``` javascript
window.dataLayer = window.dataLayer || [];
dataLayer.push({ eventModel: null });  // Clear the previous eventModel object.
dataLayer.push({
  event: "consent_status",
  eventModel: {
    status: "<decline>",
    categories: {
        necessary: "<necessary>",
        analytics: "<analytics>",
        marketing: "<marketing>",
        functionality: "<functionality>"
      }
  }
});
```
## Parameter Definitions

|Field|Type|Required?|Description|Example|
| --- | --- | --- | --- | --- |
|categories|array|required|An array that containes a json object of the types of permissions and their current statuses.|`[{<permission types and statuses>}]`|
|necessary|boolean|required|Did the user give permission for necessary cookies? Should always be true.|`true`|
|analytics|boolean|required|Did the user give permission for analytics cookies? Should default to false until user says otherwise.|`false`|
|marketing|boolean|required|Did the user give permission for marketing cookies? Should default to false until user says otherwise.|`false`|
|functionality|boolean|required|Did the user give permission for functionality cookies? Should default to false until user says otherwise.|`false`|
