# [Share](https://developers.google.com/analytics/devguides/collection/ga4/reference/events?client_type=gtm#share)
Use this event when a user has shared content.
## Sample JS
``` javascript
window.dataLayer = window.dataLayer || [];
dataLayer.push({ eventModel: null });  // Clear the previous eventModel object.
dataLayer.push({
  event: "share",
  eventModel: {
    platform: "platform",
    content_type: "content_type",
    content_id: "content_id"
  }
});
```
## Parameter Definitions

|Field|Type|Required?|Description|Example|
| --- | --- | --- | --- | --- |
|platform|strint|required|The platform on which the content is shared.|`Reddit`|
|content_type|string|required|The type of content selected.|`image`|
|content_id|string|required|The content's unique identifier.|`C-1234`|
