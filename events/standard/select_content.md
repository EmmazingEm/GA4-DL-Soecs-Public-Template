# [Select Content](https://developers.google.com/analytics/devguides/collection/ga4/reference/events?client_type=gtm#select_content)
This event signifies that a user has selected some content of a certain type from search results.
## Sample JS
``` javascript
window.dataLayer = window.dataLayer || [];
dataLayer.push({ eventModel: null });  // Clear the previous eventModel object.
dataLayer.push({
  event: "select_content",
  eventModel: {
    content_type: "content_type",
    content_id: "content_id"
  }
});
```
## Parameter Definitions

|Field|Type|Required?|Description|Example|
| --- | --- | --- | --- | --- |
|content_type|string|required|The type of content selected.|`Blog post`|
|content_id|string|required|The content's unique identifier.|`C-1234`|
