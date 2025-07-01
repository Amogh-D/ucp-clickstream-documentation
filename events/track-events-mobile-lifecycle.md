---
id: track-events-mobile-lifecycle
title: Track Events - Mobile Lifecycle
sidebar_label: Track Events - Mobile Lifecycle
description: Documentation for UCP Clickstream mobile application lifecycle events and their payloads
---

# Track Events - Mobile Lifecycle

This document provides comprehensive documentation for UCP Clickstream mobile application lifecycle events. Each event includes a description, trigger, and example payload.

## Mobile Lifecycle Events


### Application Opened

**Triggered when:** The app is opened or brought to the foreground after first open. Fired with login track events.

**Type:** Core Event

```json
{
    "type": "track",
    "event": "Application Opened",
    "properties": {
        "application": "Jiomart",
        "from_background": false,
        "not_running": true,
        "version": "18.0.1",
        "build": "23",
        "platform": "iOS"
    }
}
```

### Application Backgrounded

**Triggered when:** The app is moved to background from the foreground after first open.

**Type:** Core Event

```json
{
    "type": "track",
    "event": "Application Backgrounded",
    "properties": {
        "application": "Jiomart",
        "platform": "iOS"
    }
}
```

### Application Updated

**Triggered when:** The app is updated and opened for the first time after update.

**Type:** Core Event

```json
{
    "type": "track",
    "event": "Application Updated",
    "properties": {
        "application": "Jiomart"
        "previous_version": "18.1.0"
        "previous_build": "24",
        "version": "19.0.0",
        "build": "10",
        "platform": "iOS"
    }
}
```

### Application Uninstalled

**Triggered when:** The app is uninstalled by the user.

**Type:** Core Event

```json
{
    "type": "track",
    "event": "Application Uninstalled",
    "properties": {
        "application": "Jiomart",
        "platform": "iOS"
        }
}
```

### Application Crashed

**Triggered when:** A crash notification is fired from the app.

**Type:** Core Event

```json
{
    "type": "track",
    "event": "Application Crashed",
    "properties": {
        "application": "Jiomart",
        "platform": "iOS"
    }
}
``` 

### Push Notification Received

**Triggered when:** A push notification is received at the customer end

**Type:** Core Event

```json
{
  "type": "track",
  "event": "Push Notification Received",
  "writeKey": "a70e4d4ad88fb90f53df0fa63250edbf161692e4b33edb9f8c1db5e0d1853007",
    "external_ids": [
        {
            "type": "rr_id",
            "id": "77d42965-2c30-4007-b7c4-fd5340163d3d"
        }
    ],
    "application_ids": [
        {
            "type": "jiomart_id",
            "id": "851"
        }
    ],
  "properties": {
    "campaign": {
      "medium": "Push",
      "source": "Vendor Name",
      "name": "Referral Flow",
      "content": "Your friend invited you to play a match."
    }
  }
}
```

### Push Notification Tapped

**Triggered when:** A push notification is tapped by the customer

**Type:** Core Event

```json
{
  "type": "track",
  "event": "Push Notification Tapped",
  "properties": {
    "action": "Accept",
    "campaign": {
      "medium": "Push",
      "source": "Vendor Name",
      "name": "Referral Flow",
      "content": "Your friend invited you to play a match."
    }
  }
}
```

### Push Nofitication Bounced

**Triggered when:** A push notification is bounced off the by customer

**Type:** Core Event

```json
{
  "type": "track",
  "event":"Push Notification Bounced",
  "properties": {
    "action": "Accept",
    "campaign": {
      "medium": "Push",
      "source": "Vendor Name",
      "name": "Referral Flow",
      "content": "Your friend invited you to play a match."
    }
  }
}
```

## Complete Track Call Examples

## Application Lifecycle Events (Mobile)

A complete example of a Track call (application lifecycle) with context data and properties:

```json
{
  "writeKey": "859f596fec469fae9a5644877d8a5840e53afbaa415833d402a67f2f5ff29f9d",
  "messageId": "ajs-next-8a1f5afd38d23123d171bc94777e88b6",
  "request_id": "68443ea7-41bb-4cf9-bc6c-7467afbce5b6",
  "sent_at": "2024-04-26T09:45:13.695Z",
  "external_ids": [
    {
      "type": "rr_id",
      "id": "802e83d0-27bc-4d68-b403-3da6d3fa223a"
    }
  ],
  "application_ids": [
    {
      "type": "ajio_id",
      "id": "f225edcf-0fc9-4053-ba48-756813baa6fa"
    }
  ],
  "context": {
    "campaign": {
      "name": "Ajio Big Bold Sale",
      "source": "Sale banner",
      "medium": "push notifications",
      "content": "image link"
    },
    "device": {
      "adTrackingEnabled": true,
      "advertisingId": "0EE0AC3D-F204-4807-92CE-972CD19E3462",
      "id": "9DEE4E8E-ED3D-4C2F-BCF1-9A51149C773F",
      "manufacturer": "Apple",
      "model": "iPhone14,5",
      "name": "iPhone",
      "token": "f468984aa58aef5dfbfd6943dda709454cdea1b45a1f522a89c3809d236c8810",
      "type": "ios"
    },
    "screen": {
      "width": 1125,
      "height": 2436,
      "density": 3
    },
    "location": {
      "city": "Mumbai",
      "country": "India",
      "latitude": 19.116625,
      "longitude": 72.862358
    },
    "os": {
      "name": "iOS",
      "version": "17.2"
    },
    "channel": "mobile"
  },
  "type": "track",
  "event": "Application Opened",
  "properties": {
      "application": "Jiomart",
      "from_background": false,
      "not_running": true,
      "version": "18.0.1",
      "build": "23",
      "platform": "iOS"
  }
}
```