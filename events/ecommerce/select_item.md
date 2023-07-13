# [Select Item](https://developers.google.com/analytics/devguides/collection/ga4/reference/events?client_type=gtm#select_item)

This event signifies an item was selected from a list. This should fire in conjunction with [select_content](/events/standard/select_content.md), as appropriate.

## Javascript Code

```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({
  event: "select_item",
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
|items|array|required|Populate with item objects that represent the product selected.|See the [items](/schemas/items.md) array for a detailed example.|
