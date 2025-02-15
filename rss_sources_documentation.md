# RSS Sources JSON Documentation

This document provides detailed information about the `rss_sources.json` file, which is used by our system to configure and manage RSS feed sources for various languages. The file is written in JSON and contains metadata for each feed, including URL, category, update timestamps, and status information.

---

## Overview

- **Purpose:**  
  The `rss_sources.json` file stores configuration data for RSS feeds grouped by language. Each language object contains information about the language (such as language code, country code, locale, and language name) as well as a list of RSS feed sources.

- **Usage:**  
  The system reads this file to know which RSS feeds to fetch, how to categorize them, and whether they are active. This file is also used for maintenance and update operations.

- **Maintenance:**  
  - **URL Consistency:** All feed URLs must include a valid protocol (`http://` or `https://`).  
  - **Timestamps:** Timestamps use the ISO 8601 format (e.g., `2025-02-15T00:00:00Z`). Update the `last_updated` fields as necessary when the feed or its configuration is changed.
  - **Categorization:** Each source has a `category` object with a machine-readable `slug` and a human-readable `display` value. This helps in grouping and filtering feeds.
  - **Source Types:** Currently, the system supports a single source type (`standard`), but additional types can be added in the future if needed.
  - **Active Flag:** The `is_active` Boolean indicates if a feed is currently in use. Setting it to `false` will disable the feed without removing it from the configuration.

---

## File Structure

The JSON file is structured as an array containing one or more language objects. Each language object has the following keys:

- **language_code** (string):  
  A two-letter ISO code representing the language (e.g., `"tr"`).

- **country_code** (string):  
  A two-letter ISO country code (e.g., `"TR"`).

- **locale** (string):  
  The locale identifier (e.g., `"tr-TR"`).

- **language_name** (string):  
  The full name of the language (e.g., `"Türkçe"`).

- **last_updated** (string):  
  A timestamp in ISO 8601 format representing the last update for the language block.

- **sources** (array):  
  An array of source objects. Each object represents an individual RSS feed and has the following structure:

  - **url** (string):  
    The full URL of the RSS feed. **_Note:_** All URLs must include the protocol (e.g., `https://`).

  - **category** (object):  
    Contains:
    - **slug** (string): A machine-friendly category identifier (e.g., `"gundem"`).
    - **display** (string): A human-friendly label for the category (e.g., `"Gündem"`).

  - **is_active** (boolean):  
    Indicates whether the feed is currently active (`true` or `false`).

  - **source_type** (string):  
    Indicates the type of source. Currently, the only supported value is `"standard"`.

  - **last_updated** (string):  
    A timestamp in ISO 8601 format indicating when this source was last updated.

---

## Example

Below is an abbreviated example of the JSON structure:

```json
[
  {
    "language_code": "tr",
    "country_code": "TR",
    "locale": "tr-TR",
    "language_name": "Türkçe",
    "last_updated": "2025-02-15T00:00:00Z",
    "sources": [
      {
        "url": "https://www.ntv.com.tr/gundem.rss",
        "category": {
          "slug": "gundem",
          "display": "Gündem"
        },
        "is_active": true,
        "source_type": "standard",
        "last_updated": "2025-02-15T00:00:00Z"
      },
      {
        "url": "https://www.ntv.com.tr/dunya-kupasi-2018.rss",
        "category": {
          "slug": "spor",
          "display": "Spor"
        },
        "is_active": true,
        "source_type": "standard",
        "last_updated": "2025-02-15T00:00:00Z"
      }
      // ... Additional source objects
    ]
  }
]
