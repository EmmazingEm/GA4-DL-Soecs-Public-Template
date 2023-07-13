# [Add Payment Info](https://developers.google.com/analytics/devguides/collection/ga4/reference/events?client_type=gtm#add_payment_info)

This event signifies a user has submitted their payment information.

## Javascript Code

```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({
  event: "add_payment_info",
  ecommerce: {
    affiliation: "<affiliation>",
    coupon: "<coupon>",
    currency: "<currency>",
    items: "<items>",
    payment_type: "<payment_type>",
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
|items|array|required|Populate with item objects that represent the product added.|See the [items](/schemas/items.md) array for a detailed example.|
|payment_type|string|recommended|The chosen method of payment.|`credit card`|
|value|number|required|The monetary value of the items added to the cart in this event pre-tax and shipping.|`7.77`|
