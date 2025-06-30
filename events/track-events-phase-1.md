---
id: track-events-phase-1
title: Track Events - Phase 1 Integration
sidebar_label: Track Events Phase 1
description: Comprehensive documentation for UCP Clickstream track events including ecommerce and mobile application events
---

# Track Events - Phase 1 Integration

This document provides comprehensive documentation for UCP Clickstream track events, including both ecommerce and mobile application events. These events are generic activity events - clickstream and orderstream and not dependent on medium.

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

## Mobile Events

These events are specific to mobile application activity.

### Application Installed

**Triggered when:** An application is opened for the first time after installation. It is a one time event. Should be fired on first open.

**Type:** Core Event

| Key name | Data type | Possible Values | Example/Description |
|----------|-----------|-----------------|-------------------|
| app_name | String | - | Name of the application |
| app_version | String | - | Version of the application |
| build_number | String | - | Build number of the application |

### Application Opened

**Triggered when:** An application is opened or brought to the foreground after first open. It is fired along with any other Login Track events. (This event should be fired in all instances of application being opened/ brought to the foreground except first open).

**Type:** Core Event

| Key name | Data type | Possible Values | Example/Description |
|----------|-----------|-----------------|-------------------|
| app_name | String | - | Name of the application |
| app_state | String | "foreground", "background" | Value for when app is in foreground, Value for when app is in background |
| app_version | String | - | Version of the application |
| build_number | String | - | Build number of the application |

### Application Backgrounded

**Triggered when:** The application is moved to background from the foreground after first open.

**Type:** Core Event

| Key name | Data type | Possible Values | Example/Description |
|----------|-----------|-----------------|-------------------|
| app_name | String | - | Name of the application |

### Application Updated

**Triggered when:** A user updates the application and opens it for the first time after an update.

**Type:** Core Event

| Key name | Data type | Possible Values | Example/Description |
|----------|-----------|-----------------|-------------------|
| app_name | String | - | Name of the application |
| app_version | String | - | Version of the application |
| build_number | String | - | Build number of the application |
| previous_app_version | String | - | Version of the previous application |
| previous_build_number | String | - | Build number of the previous application |

### Application Uninstalled

**Triggered when:** A user uninstalls the application.

**Type:** Core Event

| Key name | Data type | Possible Values | Example/Description |
|----------|-----------|-----------------|-------------------|
| app_name | String | - | Name of the application |

### Application Crashed

**Triggered when:** A crash notification is fired from app. It is only meant supplant information for crashed users.

**Type:** Core Event

| Key name | Data type | Possible Values | Example/Description |
|----------|-----------|-----------------|-------------------|
| app_name | String | - | Name of the application |

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

### Mobile Events

A complete example of a Track Call (mobile) with context data and properties:

```json
{
  "type": "track",
  "event": "Application Opened",
  "properties": {
    "app_name": "Jiomart",
    "app_state": "foreground",
    "app_version": "4.2.1",
    "build_number": "421"
  },
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

## SDK Implementation

### Analytics.js (Web)

```javascript
// Initialize analytics
analytics.identify('user_123', {
  email: 'user@example.com',
  name: 'John Doe'
});

// Track product clicked
analytics.track('Product Clicked', {
  click_source: 'Category List',
  product_id: '52efg-7f',
  sku: 'SD-henleyredL',
  product_name: 'SuperDry Henley Full - Red',
  // ... other properties
});
```

### Analytics-iOS

```swift
// Initialize analytics
Analytics.shared().identify("user_123", traits: [
    "email": "user@example.com",
    "name": "John Doe"
])

// Track application opened
Analytics.shared().track("Application Opened", properties: [
    "app_name": "Jiomart",
    "app_state": "foreground",
    "app_version": "4.2.1",
    "build_number": "421"
])
```

### Analytics-Android

```java
// Initialize analytics
Analytics.with(context).identify("user_123", new Traits()
    .putEmail("user@example.com")
    .putName("John Doe"), null);

// Track application opened
Analytics.with(context).track("Application Opened", new Properties()
    .putValue("app_name", "Jiomart")
    .putValue("app_state", "foreground")
    .putValue("app_version", "4.2.1")
    .putValue("build_number", "421"));
```

## Phase 1 Events Summary

| Method | Name | Triggered by Jiomart Web | Triggered by Jiomart Mobile App |
|--------|------|-------------------------|--------------------------------|
| Track | Order Completed | Yes | Yes |
| Track | Order Cancelled | Yes | Yes |
| Track | Order Refunded | Yes | Yes |
| Track | Product Viewed | Yes | Yes |
| Track | Product Added | Yes | Yes |
| Track | Product Removed | Yes | Yes |
| Track | Checkout Started | Yes | Yes |
| Page | Page Viewed | Yes | No |
| Screen | Screen Viewed | No | Yes |
| Track | Application Installed | No | Yes |
| Track | Application Opened | No | Yes |
| Track | Application Backgrounded | No | Yes |
| Track | Application Updated | Yes | No |

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

### Mobile App Fields

- **app_name**: Application name
- **app_version**: Application version
- **build_number**: Build number
- **app_state**: Application state (foreground/background)
- **previous_app_version**: Previous application version
- **previous_build_number**: Previous build number
