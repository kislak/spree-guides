---
title: Receiving Data
---

## Overview

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut at leo a mi vehicula viverra. Nulla adipiscing mauris lorem, vitae tempus quam lacinia eu. Cras blandit aliquet turpis sed hendrerit. Etiam volutpat auctor varius. Nulla ullamcorper ut est eu suscipit. Ut porttitor, nisi non feugiat fringilla, nisi purus vehicula dui, vel semper nisi ligula at odio.

Maecenas sit amet metus arcu. Donec adipiscing leo nisl, vel convallis odio porta nec. Duis placerat lacus eget magna imperdiet, nec vehicula lorem bibendum. In dignissim sagittis ligula nec auctor. Fusce vel velit id velit rhoncus posuere. Etiam adipiscing mollis enim vel condimentum. Vestibulum quis nulla aliquet, lobortis quam quis, tempus metus. Nam nisl velit, tempus eu dapibus sed, malesuada nec lectus. Maecenas tincidunt urna a ipsum accumsan aliquam. Suspendisse fermentum libero a nisl sollicitudin, tristique mattis nibh dictum.

## Authentication

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut at leo a mi vehicula viverra. Nulla adipiscing mauris lorem, vitae tempus quam lacinia eu. Cras blandit aliquet turpis sed hendrerit. Etiam volutpat auctor varius. Nulla ullamcorper ut est eu suscipit. Ut porttitor, nisi non feugiat fringilla, nisi purus vehicula dui, vel semper nisi ligula at odio.

Maecenas sit amet metus arcu. Donec adipiscing leo nisl, vel convallis odio porta nec. Duis placerat lacus eget magna imperdiet, nec vehicula lorem bibendum. In dignissim sagittis ligula nec auctor. Fusce vel velit id velit rhoncus posuere. Etiam adipiscing mollis enim vel condimentum. Vestibulum quis nulla aliquet, lobortis quam quis, tempus metus. Nam nisl velit, tempus eu dapibus sed, malesuada nec lectus. Maecenas tincidunt urna a ipsum accumsan aliquam. Suspendisse fermentum libero a nisl sollicitudin, tristique mattis nibh dictum.

## Receive Hooks

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut at leo a mi vehicula viverra. Nulla adipiscing mauris lorem, vitae tempus quam lacinia eu. Cras blandit aliquet turpis sed hendrerit. Etiam volutpat auctor varius. Nulla ullamcorper ut est eu suscipit. Ut porttitor, nisi non feugiat fringilla, nisi purus vehicula dui, vel semper nisi ligula at odio.

### New Order

---POST /order_new---
```json
{
  "message": "order:new",
  "payload": {
    "order": {
      "number": "100-EXAMPLE-1000000",
      "channel": "Amazon.com",
      "currency": "USD",
      "status": "Unshipped",
      "placed_on": "2013-08-16T01:25:00Z",
      "updated_at": "2013-08-16T01:30:00Z",
      "email": "ceth5ni9mo4whyc@marketplace.amazon.com",
      "totals": {
        "item": 64.0,
        "adjustment": 0.0,
        "tax": 0.0,
        "shipping": 0.0,
        "order": 64.0,
        "payment": 64.0
      },
      "adjustments": [
        { "name": "Shipping Discount", "value": 0.0 },
        { "name": "Promotion Discount", "value": 0.0 },
        { "name": "Amazon Tax", "value": 0.0 },
        { "name": "Gift Wrap Price", "value": 0.0 },
        { "name": "Gift Wrap Tax", "value": 0.0 }
      ],
      "line_items": [
        {
          "name": "T-Shirt, Black, XX-Large",
          "price": 29.0,
          "sku": "100TSBXXL",
          "quantity": 1,
          "variant_id": null,
          "external_ref": null,
          "options": {}
        },
        {
          "name": "T-Shirt, White, XX-Large",
          "price": 35.0,
          "sku": "100TSWXXL",
          "quantity": 1,
          "variant_id": null,
          "external_ref": null,
          "options": {}
        }
      ],
      "payments": [
        {
          "amount": 64.0,
          "payment_method": "Amazon",
          "status": "complete"
        }
      ],
      "shipments": [
        {
          "cost": 0.0,
          "status": "Unshipped",
          "shipping_method": "Standard",
          "items": [
            {
              "name": "T-Shirt, Black, XX-Large",
              "price": 29.0,
              "sku": "100TSBXXL",
              "quantity": 1,
              "variant_id": null,
              "external_ref": null,
              "options": {}
            },
            {
              "name": "T-Shirt, White, XX-Large",
              "price": 35.0,
              "sku": "100TSWXXL",
              "quantity": 1,
              "variant_id": null,
              "external_ref": null,
              "options": {}
            }
          ],
          "stock_location": "",
          "tracking": "",
          "number": ""
        }
      ],
      "shipping_address": {
        "firstname": "Patrick",
        "lastname": "Cook",
        "address1": "7159 edwards rd",
        "address2": "Apartment A-12",
        "city": "Seymour",
        "zipcode": "37284",
        "phone": "471-543-4073",
        "country": "US",
        "state": "Pennsylvania"
      },
      "billing_address": {
        "firstname": "Patrick",
        "lastname": "Cook",
        "address1": "7159 edwards rd",
        "address2": "Apartment A-12",
        "city": "Seymour",
        "zipcode": "37284",
        "phone": "471-543-4073",
        "country": "US",
        "state": "Pennsylvania"
      }
    }
  }
}
```

### order_update

---POST /order_update---
```json
{
  "message": "order:update",
  "payload": {
    "order": {

    }
  }
}
```

### shipment_confirm

---POST /shipment_confirm---
```json
{
  "message": "shipment:confirm",
  "payload": {
    "order": {

    }
  }
}
```

### inventory_update

---POST /inventory_upate---
```json
{
  "message": "inventory:update",
  "payload": {
    "order": {

    }
  }
}
```
