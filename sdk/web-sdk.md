---
id: web-sdk
title: Web SDK Documentation
sidebar_label: Web SDK
description: Complete guide for implementing UCP Clickstream Web SDK
---

# Web SDK Documentation

## Overview

The UCP Clickstream Web SDK enables you to track user interactions and events on your web applications. This guide provides comprehensive documentation for implementing and configuring the Web SDK.

## Installation

### Prerequisites

- Modern web browser with JavaScript enabled
- UCP Clickstream account and write key

### Setup

1. **Inject the SDK Script**

Add the following script to your HTML page:

```html
<script>
!function(){var e=window.stelios=window.stelios||[];if(!e.initialize){if(e.invoked)return;e.invoked=!0,e.methods=["track","identify","alias","group","page","once","off","on"],e.factory=function(t){return function(){var e=Array.prototype.slice.call(arguments);return e.unshift(t),e.push(e),e}};for(var t=0;t<e.methods.length;t++){var r=e.methods[t];e[r]=e.factory(r)}e.load=function(t){var r=document.createElement("script");r.type="text/javascript",r.async=!0,r.src="https://cdn.segment.com/analytics.js/v1/"+t+"/analytics.min.js";var n=document.getElementsByTagName("script")[0];n.parentNode.insertBefore(r,n)},e.SNIPPET_VERSION="4.1.0",e.load("YOUR_WRITE_KEY")}}();
</script>
```

2. **Configure Variables**

Replace the following variables in the script above:

- `WRITE_KEY`: Your UCP Clickstream write key (contact UCP team)
- `URL`: `https://api.cctz0.de/service/application/ccp-ingest/stream/v1.0`

## Configuration

### Basic Configuration

[Content will be added from PDF]

### Advanced Configuration

[Content will be added from PDF]

## API Reference

### Core Methods

#### Track Event

```javascript
window.stelios.track(eventName, eventPayload)
```

**Parameters:**
- `eventName` (string): The name of the event to track
- `eventPayload` (object): The event data payload

## Event Examples

### Basic Event Structure

All events follow this basic structure:

```javascript
{
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  // ... event-specific properties
}
```

### Complete Event Reference

#### 1. Coupon Applied

```javascript
window.stelios.track("Coupon Applied", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "order_id": "",
  "cart_id": "",
  "coupon_id": "",
  "coupon_code": "",
  "discount": 0
});
```

#### 2. Coupon Denied

```javascript
window.stelios.track("Coupon Denied", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "order_id": "",
  "cart_id": "",
  "coupon_id": "",
  "coupon_code": "",
  "reason": ""
});
```

#### 3. Coupon Removed

```javascript
window.stelios.track("Coupon Removed", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "coupon_id": "",
  "coupon_code": "",
  "discount": 0,
  "order_id": "",
  "cart_id": ""
});
```

#### 4. Coupon Entered

```javascript
window.stelios.track("Coupon Entered", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "order_id": "",
  "cart_id": "",
  "coupon_id": "",
  "coupon_code": ""
});
```

#### 5. Checkout Step Viewed

```javascript
window.stelios.track("Checkout Step Viewed", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "order_id": "",
  "cart_id": "",
  "step": 0,
  "address_selected": "",
  "shipping_method": ""
});
```

#### 6. Checkout Initiated

```javascript
window.stelios.track("Checkout Initiated", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "cart_total": 0,
  "items": 0,
  "shipping": 0,
  "tax": 0,
  "order_total": 0,
  "product_id": "",
  "sku": "",
  "product_name": "",
  "l1_category": "",
  "l2_category": "",
  "l3_category": "",
  "l4_category": "",
  "l5_category": "",
  "brand": "",
  "variant": "",
  "price": 0,
  "value": 0,
  "currency": "",
  "quantity": 0,
  "position": 0,
  "url": "",
  "img_url": ""
});
```

#### 7. Checkout Step Completed

```javascript
window.stelios.track("Checkout Step Completed", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "step": 0,
  "address_selected": "",
  "shipping_method": "",
  "order_id": "",
  "cart_id": ""
});
```

#### 8. Cart Abandoned

```javascript
window.stelios.track("Cart Abandoned", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "cart_id": "",
  "products": []
});
```

#### 9. Cart Viewed

```javascript
window.stelios.track("Cart Viewed", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "cart_id": "",
  "products": []
});
```

#### 10. Cart Shared

```javascript
window.stelios.track("Cart Shared", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "share_via": "",
  "share_message": "",
  "share_to": "",
  "cart_id": "",
  "product_id": ""
});
```

#### 11. Gift Selected

```javascript
window.stelios.track("Gift Selected", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "order_id": "",
  "product_id": "",
  "gift": true
});
```

#### 12. Navigation Viewed

```javascript
window.stelios.track("Navigation Viewed", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "menu1_name": "",
  "menu2_name": "",
  "menu3_name": "",
  "order_id": "",
  "cart_id": ""
});
```

#### 13. Order Completed

```javascript
window.stelios.track("Order Completed", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "order_id": "",
  "cart_id": "",
  "cart_total": 0,
  "cart_type": "",
  "items": 0,
  "shipping": 0,
  "tax": 0,
  "order_total": 0,
  "currency": "",
  "products": []
});
```

#### 14. Order Refund

```javascript
window.stelios.track("Order Refund", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "order_id": "",
  "cart_total": 0,
  "items": 0,
  "shipping": 0,
  "tax": 0,
  "order_total": 0,
  "cancellation_reason": "",
  "refund_amount": 0,
  "refund_to": "",
  "refund_status": "",
  "products": []
});
```

#### 15. Order Updated

```javascript
window.stelios.track("Order Updated", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "order_id": "",
  "cart_total": 0,
  "items": 0,
  "shipping": 0,
  "tax": 0,
  "order_total": 0,
  "products": []
});
```

#### 16. Order Cancelled

```javascript
window.stelios.track("Order Cancelled", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "order_id": "",
  "cart_total": 0.0,
  "items": 0,
  "shipping": 0.0,
  "tax": 0.0,
  "order_total": 0.0,
  "cancellation_reason": "",
  "products": []
});
```

#### 17. Product Shared

```javascript
window.stelios.track("Product Shared", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "share_via": "",
  "share_message": "",
  "share_to": "",
  "product_id": "",
  "sku": "",
  "product_name": "",
  "l1_category": "",
  "l2_category": "",
  "l3_category": "",
  "l4_category": "",
  "l5_category": "",
  "brand": "",
  "variant": "",
  "price": 0,
  "value": 0,
  "currency": "",
  "quantity": 1,
  "position": 0,
  "url": "",
  "img_url": ""
});
```

#### 18. Product Added

```javascript
window.stelios.track("Product Added", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "cart_id": "",
  "product_id": "",
  "sku": "",
  "product_name": "",
  "l1_category": "",
  "l2_category": "",
  "l3_category": "",
  "l4_category": "",
  "l5_category": "",
  "brand": "",
  "variant": "",
  "price": 0,
  "value": 0,
  "currency": "",
  "quantity": 0,
  "url": "",
  "img_url": ""
});
```

#### 19. Product Clicked

```javascript
window.stelios.track("Product Clicked", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "product_id": "",
  "sku": "",
  "product_name": "",
  "l1_category": "",
  "l2_category": "",
  "l3_category": "",
  "l4_category": "",
  "l5_category": "",
  "brand": "",
  "variant": "",
  "price": 0,
  "value": 0,
  "currency": "",
  "quantity": 0,
  "url": "",
  "img_url": ""
});
```

#### 20. Product List Filtered

```javascript
window.stelios.track("Product List Filtered", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "products": [],
  "filters": [],
  "sorts": []
});
```

#### 21. Product Searched

```javascript
window.stelios.track("Product Searched", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "query": ""
});
```

#### 22. Product Wishlisted

```javascript
window.stelios.track("Product Wishlisted", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "wishlist_id": "",
  "wishlist_name": "",
  "product_id": "",
  "sku": "",
  "product_name": "",
  "l1_category": "",
  "l2_category": "",
  "l3_category": "",
  "l4_category": "",
  "l5_category": "",
  "brand": "",
  "variant": "",
  "price": 0,
  "value": 0,
  "currency": "",
  "quantity": 0,
  "url": "",
  "img_url": ""
});
```

#### 23. Product Wishlist Removed

```javascript
window.stelios.track("Product Wishlist Removed", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "wishlist_id": "",
  "wishlist_name": "",
  "product_id": "",
  "sku": "",
  "product_name": "",
  "l1_category": "",
  "l2_category": "",
  "l3_category": "",
  "l4_category": "",
  "l5_category": "",
  "brand": "",
  "variant": "",
  "price": 0,
  "value": 0,
  "currency": "",
  "quantity": 0,
  "position": 0,
  "url": "",
  "img_url": ""
});
```

#### 24. Product Reviewed

```javascript
window.stelios.track("Product Reviewed", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "product_id": "",
  "review_id": "",
  "review_body": "",
  "rating": 0
});
```

#### 25. Payment Details Added

```javascript
window.stelios.track("Payment Details Added", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "order_id": "",
  "cart_id": "",
  "payment_method": "",
  "pay_amount": 0,
  "upi_id": "",
  "netbanking_id": "",
  "card_number": "",
  "name_on_card": "",
  "expiry": ""
});
```

#### 26. Product Notify

```javascript
window.stelios.track("Product Notify", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "notify": true,
  "reason": "",
  "product_id": "",
  "sku": "",
  "product_name": "",
  "l1_category": "",
  "l2_category": "",
  "l3_category": "",
  "l4_category": "",
  "l5_category": "",
  "brand": "",
  "variant": "",
  "price": 0,
  "value": 0,
  "currency": "",
  "quantity": 0,
  "url": "",
  "img_url": ""
});
```

#### 27. Product Removed

```javascript
window.stelios.track("Product Removed", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "cart_id": "",
  "product_id": "",
  "sku": "",
  "product_name": "",
  "l1_category": "",
  "l2_category": "",
  "l3_category": "",
  "l4_category": "",
  "l5_category": "",
  "brand": "",
  "variant": "",
  "price": 0,
  "value": 0,
  "currency": "",
  "quantity": 0,
  "url": "",
  "img_url": ""
});
```

#### 28. Product Wishlist To Cart

```javascript
window.stelios.track("Product Wishlist To Cart", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "wishlist_id": "",
  "wishlist_name": "",
  "cart_id": "",
  "product_id": "",
  "sku": "",
  "product_name": "",
  "l1_category": "",
  "l2_category": "",
  "l3_category": "",
  "l4_category": "",
  "l5_category": "",
  "brand": "",
  "variant": "",
  "price": 0.0,
  "value": 0.0,
  "currency": "",
  "quantity": 0,
  "position": 0,
  "url": "",
  "img_url": ""
});
```

#### 29. Product List Viewed

```javascript
window.stelios.track("Product List Viewed", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "products": []
});
```

#### 30. Product Viewed

```javascript
window.stelios.track("Product Viewed", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "product_id": "",
  "sku": "",
  "product_name": "",
  "l1_category": "",
  "l2_category": "",
  "l3_category": "",
  "l4_category": "",
  "l5_category": "",
  "brand": "",
  "variant": "",
  "price": 0.0,
  "value": 0.0,
  "currency": "",
  "quantity": 0,
  "position": 0,
  "url": "",
  "img_url": ""
});
```

#### 31. Promotion Clicked

```javascript
window.stelios.track("Promotion Clicked", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "id": "",
  "name": "",
  "position": ""
});
```

#### 32. Promotion Viewed

```javascript
window.stelios.track("Promotion Viewed", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "id": "",
  "name": "",
  "position": ""
});
```

#### 33. Payment Details Removed

```javascript
window.stelios.track("Payment Details Removed", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "order_id": "",
  "cart_id": "",
  "payment_method": "",
  "pay_amount": 0,
  "upi_id": "",
  "netbanking_id": "",
  "card_number": "",
  "name_on_card": "",
  "expiry": ""
});
```

#### 34. Payment Details Failed

```javascript
window.stelios.track("Payment Details Failed", {
  "external_ids": [
    {
      "type": "rr_id",
      "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
    }
  ],
  "application_ids": [
    {
      "type": "jiomart_id",
      "id": "1615343"
    }
  ],
  "payment_method": "",
  "failure_reason": "",
  "product_id": ""
});
```

## Implementation Examples

### Basic Setup Example

```html
<!DOCTYPE html>
<html>
<head>
    <title>UCP Clickstream Integration</title>
</head>
<body>
    <!-- UCP Clickstream SDK -->
    <script>
    !function(){var e=window.stelios=window.stelios||[];if(!e.initialize){if(e.invoked)return;e.invoked=!0,e.methods=["track","identify","alias","group","page","once","off","on"],e.factory=function(t){return function(){var e=Array.prototype.slice.call(arguments);return e.unshift(t),e.push(e),e}};for(var t=0;t<e.methods.length;t++){var r=e.methods[t];e[r]=e.factory(r)}e.load=function(t){var r=document.createElement("script");r.type="text/javascript",r.async=!0,r.src="https://cdn.segment.com/analytics.js/v1/"+t+"/analytics.min.js";var n=document.getElementsByTagName("script")[0];n.parentNode.insertBefore(r,n)},e.SNIPPET_VERSION="4.1.0",e.load("YOUR_WRITE_KEY")}}();
    </script>
    
    <script>
        // Example: Track product view
        window.stelios.track("Product Viewed", {
            "external_ids": [
                {
                    "type": "rr_id",
                    "id": "9aee539a-c22b-48b3-a069-f573e5c0ae2e"
                }
            ],
            "application_ids": [
                {
                    "type": "jiomart_id",
                    "id": "1615343"
                }
            ],
            "product_id": "52efg-7f",
            "sku": "AMM-500g",
            "product_name": "Amul Mithai Mate 500 gm",
            "l1_category": "Groceries",
            "l2_category": "Dairy & Bakery",
            "l3_category": "Dairy",
            "brand": "Amul",
            "variant": "500 gm",
            "price": 116,
            "value": 116,
            "currency": "INR",
            "url": "https://www.jiomart.com/p/groceries/amul-mithai-mate",
            "img_url": "https://www.jiomart.com/images/product/original/490010311/amul-taaza-homogenised-toned-milk-1-l.jpg"
        });
    </script>
</body>
</html>
```

## Best Practices

1. **Always include external_ids and application_ids** in every event
2. **Use consistent data types** for fields (strings, numbers, booleans)
3. **Validate payload structure** before sending events
4. **Handle errors gracefully** when tracking fails
5. **Test events in development** before deploying to production

## Troubleshooting

### Common Issues

1. **Script not loading**: Check if the write key is correct
2. **Events not firing**: Verify the script is loaded before calling track
3. **Invalid payload**: Ensure all required fields are present

### Debug Mode

Enable debug mode by adding console logging:

```javascript
// Add this before tracking events
window.stelios.debug = true;
```

## Field Descriptions

### Common Fields

- **external_ids**: Array of external user identifiers
- **application_ids**: Array of application-specific user identifiers
- **product_id**: Unique product identifier
- **sku**: Stock keeping unit
- **product_name**: Human-readable product name
- **l1_category** to **l5_category**: Product category hierarchy
- **brand**: Product brand name
- **variant**: Product variant (size, color, etc.)
- **price**: Product price
- **value**: Total value (price × quantity)
- **currency**: Currency code (e.g., "INR")
- **quantity**: Number of items
- **url**: Product page URL
- **img_url**: Product image URL 