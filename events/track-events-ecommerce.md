---
id: track-events-ecommerce
title: Track Events - Ecommerce
sidebar_label: Track Events - Ecommerce
description: Comprehensive documentation for UCP Clickstream track events including ecommerce and mobile application events
---

# Track Events - Ecommerce

This document provides comprehensive documentation for UCP Clickstream track events of generic ecommerce activity tracking. The payloads for all events are followed by the context data variations in web & mobile along with a complete event payload call

## Ecommerce Events

### Product Clicked

**Triggered when:** A user clicks on a product in PLP, Home Page or any other CTA where navigation to PDP happens.

**Type:** Core Event

```json
{
  "type": "track",
  "event": "Product Clicked",
  "properties": {
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
  }
}
```

### Product Viewed

**Triggered when:** A user views a product on a page, screen or preview mode.

**Type:** Core Event

```json
{
  "type": "track",
  "event": "Product Viewed",
  "properties": {
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
  }
}
```

### Product Added

**Triggered when:** A user adds a product to their cart.

**Type:** Core Event

```json
{
  "type": "track",
  "event": "Product Added",
  "properties": {
    "cart_id": "3j2h3j4gh-3472dbsjk",
    "position": 1,
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
    "quantity": 2,
    "price": 1299.00,
    "value": 2598.00,
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
  }
}
```

### Product Removed

**Triggered when:** A user removes an item from the cart.

**Type:** Core Event

```json
{
  "type": "track",
  "event": "Product Removed",
  "properties": {
    "cart_id": "3j2h3j4gh-3472dbsjk",
    "position": 1,
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
  }
}
```

### Order Completed

**Triggered when:** An order is completed by the user.

**Type:** Core Event

```json
{
  "type": "track",
  "event": "Order Completed",
  "properties": {
    "order_id": "3j2h3j4gh-2323b2b3",
    "cart_id": "3j2h3j4gh-3472dbsjk",
    "cart_total": 3897.00,
    "items": 3,
    "other_charges": 2.00,
    "discount": 50.00,
    "order_total": 3849.00,
    "order_payment_breakup": [
      {
        "payment_amount": 3800.0,
        "mop": "UPI"
      },
      {
        "payment_amount": 49.0,
        "mop": "Sodexo"
      }
    ],
    "products": [
      {
        "position": 1,
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
      },
      {
        "position": 2,
        "product_id": "52efg-7l",
        "sku": "SD-henleyyellowL",
        "product_name": "SuperDry Henley Full - Yellow",
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
        "quantity": 2,
        "price": 1299.00,
        "value": 2598.00,
        "url": "https://www.ajio.com/superdry-waffle-long-sleeve-henley-t-shirt/p/4103",
        "img_url": "https://assets.ajio.com/medias/sys_master/root/20231111/tJjY/654fa",
        "generic_article_id": "12345679",
        "EAN": "4006381333932",
        "variant_article_number": "12345678-011",
        "meta": {
          "sleeve_type": "full",
          "fabric": "cotton blend",
          "pattern_type": "solid",
          "colour": "yellow",
          "wash_type": "softner wash",
          "pack_type": "single",
          "size": "L"
        }
      }
    ]
  }
}
```

### Order Cancelled

**Triggered when:** An order is cancelled by the user.

**Type:** Core Event

```json
{
  "type": "track",
  "event": "Order Cancelled",
  "properties": {
    "order_id": "3j2h3j4gh-2323b2b3",
    "cart_id": "3j2h3j4gh-3472dbsjk",
    "cart_total": 3897.00,
    "items": 3,
    "other_charges": 2.00,
    "discount": 50.00,
    "order_total": 3849.00,
    "order_payment_breakup": [
      {
        "payment_amount": 3800.0,
        "mop": "UPI"
      },
      {
        "payment_amount": 49.0,
        "mop": "Sodexo"
      }
    ],
    "cancellation_reason": "Defective Product",
    "cancelled_amount": 3897.00,
    "products": [
      {
        "position": 1,
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
      },
      {
        "position": 2,
        "product_id": "52efg-7l",
        "sku": "SD-henleyyellowL",
        "product_name": "SuperDry Henley Full - Yellow",
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
        "quantity": 2,
        "price": 1299.00,
        "value": 2598.00,
        "url": "https://www.ajio.com/superdry-waffle-long-sleeve-henley-t-shirt/p/4103",
        "img_url": "https://assets.ajio.com/medias/sys_master/root/20231111/tJjY/654fa",
        "generic_article_id": "12345679",
        "EAN": "4006381333932",
        "variant_article_number": "12345678-011",
        "meta": {
          "sleeve_type": "full",
          "fabric": "cotton blend",
          "pattern_type": "solid",
          "colour": "yellow",
          "wash_type": "softner wash",
          "pack_type": "single",
          "size": "L"
        }
      }
    ]
  }
}
```

### Order Refunded

**Triggered when:** An order that has been cancelled by the user gets a refund.

**Type:** Core Event

```json
{
  "type": "track",
  "event": "Order Refunded",
  "properties": {
    "order_id": "3j2h3j4gh-2323b2b3",
    "cart_id": "3j2h3j4gh-3472dbsjk",
    "cart_total": 3897.00,
    "items": 3,
    "other_charges": 2.00,
    "discount": 50.00,
    "order_total": 3849.00,
    "order_payment_breakup": [
      {
        "payment_amount": 3800.0,
        "mop": "UPI"
      },
      {
        "payment_amount": 49.0,
        "mop": "Sodexo"
      }
    ],
    "cancellation_reason": "Defective Product",
    "refund_amount": 3847.00,
    "refund_payment_breakup": [
      {
        "payment_amount": 3800.0,
        "mop": "UPI"
      },
      {
        "payment_amount": 49.0,
        "mop": "Sodexo"
      }
    ],
    "products": [
      {
        "position": 1,
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
      },
      {
        "position": 2,
        "product_id": "52efg-7l",
        "sku": "SD-henleyyellowL",
        "product_name": "SuperDry Henley Full - Yellow",
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
        "quantity": 2,
        "price": 1299.00,
        "value": 2598.00,
        "url": "https://www.ajio.com/superdry-waffle-long-sleeve-henley-t-shirt/p/4103",
        "img_url": "https://assets.ajio.com/medias/sys_master/root/20231111/tJjY/654fa",
        "generic_article_id": "12345679",
        "EAN": "4006381333932",
        "variant_article_number": "12345678-011",
        "meta": {
          "sleeve_type": "full",
          "fabric": "cotton blend",
          "pattern_type": "solid",
          "colour": "yellow",
          "wash_type": "softner wash",
          "pack_type": "single",
          "size": "L"
        }
      }
    ]
  }
}
```

### Checkout Started

**Triggered when:** A user starts the checkout process for the items in their cart. This event can be fired when a user clicks on the "Proceed to buy" or any other variation of the option.

**Type:** Core Event

```json
{
  "type": "track",
  "event": "Checkout Started",
  "properties": {
    "order_id": "3j2h3j4gh-2323b2b3",
    "cart_id": "3j2h3j4gh-3472dbsjk",
    "cart_total": 3897.00,
    "items": 3,
    "other_charges": 2.00,
    "discount": 50.00,
    "order_total": 3849.00,
    "products": [
      {
        "position": 1,
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
      },
      {
        "position": 2,
        "product_id": "52efg-7l",
        "sku": "SD-henleyyellowL",
        "product_name": "SuperDry Henley Full - Yellow",
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
        "quantity": 2,
        "price": 1299.00,
        "value": 2598.00,
        "url": "https://www.ajio.com/superdry-waffle-long-sleeve-henley-t-shirt/p/4103",
        "img_url": "https://assets.ajio.com/medias/sys_master/root/20231111/tJjY/654fa",
        "generic_article_id": "12345679",
        "EAN": "4006381333932",
        "variant_article_number": "12345678-011",
        "meta": {
          "sleeve_type": "full",
          "fabric": "cotton blend",
          "pattern_type": "solid",
          "colour": "yellow",
          "wash_type": "softner wash",
          "pack_type": "single",
          "size": "L"
        }
      }
    ]
  }
}
```


## Context Data and Payload

The context data for apps and web will also vary as per the device being used. Below is an example for both the cases.

The standard structure is as follows:

1. **campaign** - Campaign information
2. **device** - Device information
3. **library** - Library information
4. **locale** - Locale information
5. **network** - Network information
6. **os** - Operating system information
7. **page** - Page information (for web)
8. **screen** - Screen information (for mobile)
9. **timezone** - Timezone information
10. **traits** - User traits
11. **userAgent** - User agent information

### Web Context Example

```json
{
  "context": {
    "campaign": {
      "name": "Summer Sale",
      "source": "email",
      "medium": "newsletter"
    },
    "device": {
      "type": "desktop",
      "manufacturer": "Apple",
      "model": "MacBook Pro"
    },
    "library": {
      "name": "analytics.js",
      "version": "2.0.0"
    },
    "locale": "en-US",
    "network": {
      "wifi": true,
      "carrier": "AT&T"
    },
    "os": {
      "name": "macOS",
      "version": "12.0"
    },
    "page": {
      "path": "/products/123",
      "referrer": "https://google.com",
      "search": "red shirt",
      "title": "Product Page",
      "url": "https://example.com/products/123"
    },
    "timezone": "America/New_York",
    "traits": {
      "email": "user@example.com",
      "name": "John Doe"
    },
    "userAgent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36"
  }
}
```

### Mobile Context Example

```json
{
  "context": {
    "campaign": {
      "name": "App Launch",
      "source": "app_store",
      "medium": "organic"
    },
    "device": {
      "type": "mobile",
      "manufacturer": "Apple",
      "model": "iPhone 13",
      "id": "device_id_123"
    },
    "library": {
      "name": "analytics-ios",
      "version": "4.0.0"
    },
    "locale": "en-US",
    "network": {
      "wifi": false,
      "carrier": "Verizon"
    },
    "os": {
      "name": "iOS",
      "version": "15.0"
    },
    "screen": {
      "width": 390,
      "height": 844,
      "density": 3
    },
    "timezone": "America/New_York",
    "traits": {
      "email": "user@example.com",
      "name": "John Doe"
    }
  }
}
```

## Complete Track Call Examples

### Behaviour Events (Web)

A complete example of a Track Call (behaviour) with context data and properties:

```json
{
  "type": "track",
  "event": "Product Clicked",
  "properties": {
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
  },
  "context": {
    "campaign": {
      "name": "Summer Sale",
      "source": "email",
      "medium": "newsletter"
    },
    "device": {
      "type": "desktop",
      "manufacturer": "Apple",
      "model": "MacBook Pro"
    },
    "library": {
      "name": "analytics.js",
      "version": "2.0.0"
    },
    "locale": "en-US",
    "network": {
      "wifi": true,
      "carrier": "AT&T"
    },
    "os": {
      "name": "macOS",
      "version": "12.0"
    },
    "page": {
      "path": "/products/123",
      "referrer": "https://google.com",
      "search": "red shirt",
      "title": "Product Page",
      "url": "https://example.com/products/123"
    },
    "timezone": "America/New_York",
    "traits": {
      "email": "user@example.com",
      "name": "John Doe"
    },
    "userAgent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36"
  }
}
```


## Field Descriptions

### Common Product Fields

- **product_id**: Unique identifier for the product
- **sku**: Stock Keeping Unit identifier
- **product_name**: Display name of the product
- **l1_category** to **l5_category**: Hierarchical category classification
- **brand**: Brand name of the product
- **quantity**: Number of items
- **price**: Unit price of the product
- **value**: Total value (price × quantity)
- **url**: Product page URL
- **img_url**: Product image URL
- **generic_article_id**: Generic article identifier
- **EAN**: European Article Number
- **variant_article_number**: Variant-specific article number
- **meta**: Additional product metadata (size, color, fabric, etc.)

### Order Fields

- **order_id**: Unique order identifier
- **cart_id**: Shopping cart identifier
- **cart_total**: Total cart value before discounts
- **items**: Number of items in the order
- **other_charges**: Additional charges (shipping, taxes, etc.)
- **discount**: Discount amount applied
- **order_total**: Final order total after discounts
- **order_payment_breakup**: Payment method breakdown
- **cancellation_reason**: Reason for order cancellation
- **refund_amount**: Amount refunded
- **refund_payment_breakup**: Refund payment method breakdown
