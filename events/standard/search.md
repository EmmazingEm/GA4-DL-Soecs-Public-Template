# [Search](https://developers.google.com/analytics/devguides/collection/ga4/reference/events?client_type=gtm#search)
Log this event to indicate when the user has performed a search.

## Sample JS
``` javascript
window.dataLayer = window.dataLayer || [];
dataLayer.push({ eventModel: null });  // Clear the previous eventModel object.
dataLayer.push({
  event: "search",
  eventModel: {
    search_term: "search_term"
});
```
## Parameter Definitions

|Field|Type|Required?|Description|Example|
| --- | --- | --- | --- | --- |
|search_term|string|required|The term used in the site search.|`interior`|
