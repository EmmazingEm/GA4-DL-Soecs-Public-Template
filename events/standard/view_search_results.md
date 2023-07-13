# View Search Results
Each time a user performs a site search, indicated by the presence of a URL query parameter

## Sample JS
``` javascript
window.dataLayer = window.dataLayer || [];
dataLayer.push({ eventModel: null });  // Clear the previous eventModel object.
dataLayer.push({
  event: "view_search_results",
  eventModel: {
    search_term: "search_term"
});
```
## Parameter Definitions

|Field|Type|Required?|Description|Example|
| --- | --- | --- | --- | --- |
|search_term|string|required|Either the term used in a traditional site search or the first selection the user made in the drop-down menu.|`interior`|
