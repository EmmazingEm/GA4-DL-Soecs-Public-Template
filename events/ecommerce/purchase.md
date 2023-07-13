# [Purchase](https://developers.google.com/analytics/devguides/collection/ga4/reference/events?client_type=gtm#purchase)

Fire whenever a user purchases one or more items.

## Javascript Code

```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({
  event: "purchase",
  ecommerce: {
    affiliation: "<affiliation>",
    coupon: "<coupon>",
    currency: "<currency>",
    items: "<items>",
    shipping: "<shipping>",
    tax: "<tax>",
    transaction_id: "<transaction_id>",
    value: "<value>"
  }
});
```

## Variable Definitions

|Field|Type|Required|Description|Example|
| --- | --- | --- | --- | --- |
|affiliation|string|recommended|A product affiliation to designate a supplying company or brick and mortar store location. Event-level and item-level affiliation parameters are independent.|`first street`|
|coupon|string|recommended|The coupon name/code associated with the event. Event-level and item-level coupon parameters are independent.|`15OFF`|
|currency|string|required|Currency of the items associated with the event, in 3-letter ISO 4217 format.|`USD`|
|items|array|required|Populate with item objects that represent the products purchased.|See the [items](/schemas/items.md) array for a detailed example.|
|shipping|number|recommended|Shipping cost associated with a transaction.|`3.33`|
|tax|number|recommended|Tax cost associated with a transaction.|`1.11`|
|transaction_id|string|required|The unique identifier of a transaction.|`T12345`|
|value|number|required|The monetary value of all purchased items before tax and shipping.|`7.77`|
