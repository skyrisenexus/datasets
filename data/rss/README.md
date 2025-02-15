# RSS Data Sources

This directory contains the `rss_sources.json` file, which lists various Turkish news sources and their RSS feeds, organized by categories. The configuration file is located at [`rss_sources.json`](https://github.com/skyrisenexus/datasets/blob/main/data/rss/rss_sources.json).

## 📊 Data Structure

### File: `rss_sources.json`

The configuration file follows a hierarchical structure organized by language and news sources:

```json
[
  {
    "language_code": "tr",            // Language code (e.g., "tr" for Turkish)
    "country_code": "TR",             // Country code
    "locale": "tr-TR",                // Language-country locale
    "language_name": "Türkçe",        // Language name
    "sources": [
      {
        "url": "https://www.example.com/feed.rss",
        "category": {
          "slug": "category-slug",           // URL-friendly category name
          "display": "Category Name"         // Display name of category
        },
        "is_active": true,            // Whether the feed is active
        "source_type": "standard"     // Type of RSS feed
      }
    ]
  }
]
```

### Property Descriptions

#### Language Level Properties
- `language_code`: Two-letter ISO 639-1 language code (e.g., "tr" for Turkish)
- `country_code`: Two-letter ISO 3166-1 alpha-2 country code (e.g., "TR" for Turkey)
- `locale`: Combined language-country code (e.g., "tr-TR")
- `language_name`: Full name of the language in its native form

#### Source Level Properties
- `url`: Complete URL to the RSS feed
- `category`: Object containing categorization information
  - `slug`: URL-friendly version of the category name
  - `display`: Human-readable category name
- `is_active`: Boolean indicating if the feed is currently active
- `source_type`: Type of RSS feed (e.g., "standard", "custom", etc.)

### News Sources

The configuration includes RSS feeds from major Turkish news outlets:

1. **NTV**
   - Gündem (News)
   - Türkiye
   - Dünya (World)
   - Ekonomi (Economy)
   - Spor (Sports)
   - Teknoloji (Technology)
   - Yaşam (Life)
   - Seyahat (Travel)
   - Sağlık (Health)
   - Sanat (Art)
   - Otomobil (Automotive)
   - Eğitim (Education)

2. **Anadolu Ajansı (AA)**
   - Güncel (Current News)

3. **Cumhuriyet**
   - Son Dakika (Breaking News)
   - Genel (General News)

### Categories

Available news categories include:
- Gündem/Güncel (Current News)
- Son Dakika (Breaking News)
- Türkiye (Turkey News)
- Dünya (World News)
- Ekonomi (Economy)
- Spor (Sports)
- Teknoloji (Technology)
- Yaşam (Lifestyle)
- Seyahat (Travel)
- Sağlık (Health)
- Sanat (Art)
- Otomobil (Automotive)
- Eğitim (Education)

## 🚀 Usage

### Accessing RSS Feeds

1. RSS feeds can be accessed directly through their URLs
2. Most feeds return content in Turkish
3. Updates frequency varies by source and category

### Feed Format

Most feeds follow standard RSS 2.0 format with:
- Title
- Publication Date
- Description
- Link to full article
- Category information

## 🔒 Security & Privacy

- Respect each source's terms of service
- Follow rate limiting guidelines
- Handle content according to source policies
- Store data securely

## 📝 Notes

- Feed availability may change
- Some sources may require authentication
- Content is primarily in Turkish
- Update frequencies vary by source

## ⚠️ Limitations

- Subject to source API limitations
- Some feeds may become inactive
- Content may be removed or archived
- Feed structures may change

---

For questions or issues, please create a GitHub issue or contact the maintainers.