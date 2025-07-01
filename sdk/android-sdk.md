---
id: android-sdk
title: Android SDK Documentation
sidebar_label: Android SDK
description: Complete guide for implementing UCP Clickstream Android SDK
---

# Android SDK Documentation

## Overview

The UCP Clickstream Android SDK enables you to track user interactions and events in your Android applications. This guide provides comprehensive documentation for implementing and configuring the Android SDK.

## Installation

### Prerequisites
- Android Studio
- UCP Clickstream .aar and .jar files
- UCP Clickstream account and write key

### Step 1: Create `libs` Directory
- Navigate to your app's main directory.
- Create a new directory named `libs` within the app directory.

### Step 2: Download SDK Files
- [android-release.aar](https://cdn.pixelbin.io/v2/autumn-band-3b0a0b/original/ucp-sdk/android/android-release.aar)
- [core-1.16.4-SNAPSHOT.jar](https://cdn.pixelbin.io/v2/autumn-band-3b0a0b/original/ucp-sdk/android/core-1.16.4-SNAPSHOT.jar)

### Step 3: Add SDK Files
- Place the downloaded `.aar` and `.jar` files into the `libs` directory you just created.

### Step 4: Update `build.gradle`
Add the following lines to your app-level `build.gradle` dependencies section:

```gradle
dependencies {
    implementation fileTree(dir: "libs", include: ["*.aar"])
    implementation files('libs/core-1.16.4-SNAPSHOT.jar')
    api 'com.segment:sovran-kotlin:1.2.2'
    api "org.jetbrains.kotlinx:kotlinx-serialization-json:1.5.1"
    implementation 'org.jetbrains.kotlinx:kotlinx-coroutines-core:1.7.1'
}
```

> **Note:** This setup includes all files in the `libs` directory as dependencies for your project.

## SDK Initialization

To use the SDK's functionalities, you must initialize it with appropriate configurations. Example:

```kotlin
class MainActivity : ComponentActivity() {
    companion object {
        lateinit var analytics: Analytics
    }
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        analytics = Analytics("YOUR_WRITE_KEY")
        analytics.collectDeviceId = true
        analytics.trackApplicationLifecycleEvents = true
        analytics.trackDeepLinks = true
        analytics.apiHost = "YOUR_API_HOST"
        analytics.cdnHost = "YOUR_CDN_HOST"
        // ...
    }
}
```

> **Reach out to the UCP Team for your unique `apiHost` & `cdnHost` values.**

## Tracking Events

> ⚠️ **Do not call tracking methods on the main/UI thread to avoid UI blocking.**

The SDK allows you to track events throughout your application. Example for tracking a "Product Viewed" event:

```kotlin
class MainActivity : ComponentActivity() {
    companion object {
        lateinit var analytics: Analytics
    }
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        analytics = Analytics("YOUR_WRITE_KEY")
        analytics.collectDeviceId = true
        analytics.trackApplicationLifecycleEvents = true
        analytics.trackDeepLinks = true
        analytics.apiHost = "YOUR_API_HOST"
        analytics.cdnHost = "YOUR_CDN_HOST"
        setContentView(R.layout.activity_main)
        val simpleButton: Button = findViewById(R.id.simpleButton)
        simpleButton.setOnClickListener {
            val event = "Product Viewed"
            val externalIds = listOf(
                mapOf("type" to "rr_id", "id" to "9aee539a-c22b-48b3-a069-f573e5c0ae2e")
            )
            val applicationIds = listOf(
                mapOf("type" to "jiomart_id", "id" to "1615343")
            )
            analytics.track(
                event,
                buildJsonObject {
                    put("externalIds", buildJsonArray {
                        externalIds.forEach { externalId ->
                            add(buildJsonObject {
                                put("type", externalId["type"])
                                put("id", externalId["id"])
                            })
                        }
                    })
                    put("applicationIds", buildJsonArray {
                        applicationIds.forEach { applicationId ->
                            add(buildJsonObject {
                                put("type", applicationId["type"])
                                put("id", applicationId["id"])
                            })
                        }
                    })
                    put("product_id", "123")
                    put("sku", "AMM-500g")
                    put("product_name", "Amul Mithai Mate 500 gm")
                    put("l1_category", "Groceries")
                    put("l2_category", "Dairy & Bakery")
                    put("l3_category", "Dairy")
                    put("brand", "Amul")
                    put("variant", "500 gm")
                    put("quantity", 1)
                    put("price", 116)
                    put("value", 116)
                    put("currency", "INR")
                    put("url", "https://www.jiomart.com/p/groceries/nestle-milkmaid-sweetened-condensed-mi")
                    put("img_url", "https://www.jiomart.com/images/product/original/490010311/amul-taaza-homogenised-toned-milk-1-l.jpg")
                }
            )
            Toast.makeText(this, "Button Clicked!", Toast.LENGTH_SHORT).show()
        }
    }
}
```

## Best Practices
- Always initialize the SDK before tracking events.
- Never call tracking methods on the main/UI thread.
- Validate event payloads before sending.
- Use unique identifiers for users and applications.

## Troubleshooting
- Ensure all dependencies are included in your `build.gradle`.
- Check for correct API and CDN host values.
- Contact UCP support for integration issues. 