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

#### Product Clicked

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
  "click_source": "Category List",
  "product_id": "52efg-7f",
  "sku": "SD-henleyredL",
  "product_name": "SuperDry Henley Full - Red",
  "l1_category": "Fashion & Lifestyle",
  "l1_category_id": "16578",
  "l2_category": "Men",
  "l2_category_id": "10890",
  "l3_category": "Westernwear",
  "l3_category_id": "10189",
  "l4_category": "T-shirts",
  "l4_category_id": "97878",
  "l5_category": "Henley",
  "l5_category_id": "7896",
  "brand": "SuperDry",
  "brand_id": "90876",
  "quantity": 1,
  "price": 1299.00,
  "value": 1299.00,
  "url": "https://www.ajio.com/superdry-waffle-long-sleeve-henley-t-shirt/p/4103",
  "img_url": "https://assets.ajio.com/medias/sys_master/root/20231111/tJjY/654fa",
  "generic_article_id": "12345678",
  "EAN": "4006381333931",
  "variant_article_number": "12345678-001",
  "meta": {
        "sleeve_type": "full",
        "fabric": "cotton blend",
        "pattern_type": "solid",
        "colour": "red",
        "wash_type": "softner wash",
        "pack_type": "single",
        "size": "L"
   }
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