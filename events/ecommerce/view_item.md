# [View Item](https://developers.google.com/analytics/devguides/collection/ga4/reference/events?client_type=gtm#view_item)

This event signifies that a user viewed a product detail page.

## Javascript Code

```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({
  event: "view_item",
  ecommerce: {
    currency: "<currency>",
    items: "<items>",
    value: "<value>"
  }
});
```

## Variable Definitions

|Field|Type|Required|Description|Example|
| --- | --- | --- | --- | --- |
|currency|string|required|Currency of the items associated with the event, in 3-letter ISO 4217 format.|`USD`|
|items|array|required|Populate with item objects that represent the viewed product.|See the [items](/schemas/items.md) array for a detailed example.|
|value|number|required|The monetary value of the viewed item pre-tax and shipping.|`7.77`|
