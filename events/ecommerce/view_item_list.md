# [View Item List](https://developers.google.com/analytics/devguides/collection/ga4/reference/events?client_type=gtm#view_item_list)

Log this event when the user has been presented with a list of items of a certain category.

## Javascript Code

```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({
  event: "view_item_list",
  ecommerce: {
    item_list_id: "<item_list_id>",
    item_list_name: "<item_list_name>",
    items: "<items>"
  }
});
```

## Variable Definitions

|Field|Type|Required|Description|Example|
| --- | --- | --- | --- | --- |
|item_list_id|string|recommended|The ID of the list in which the item was presented to the user.|`related_products`|
|item_list_name|string|recommended|The name of the list in which the item was presented to the user.|`related products`|
|items|array|required|Populate with item objects that represent the products in the list.|See the [items](/schemas/items.md) array for a detailed example.|
