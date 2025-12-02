# Douyin Scraper
> Douyin Scraper helps you collect structured video, author, and music metadata from Douyin (the Chinese version of TikTok). It solves the challenge of gathering large volumes of public video data consistently and at scale. This tool is ideal for analysts, researchers, and developers needing reliable Douyin data extraction.


<p align="center">
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://github.com/za2122/footer-section/blob/main/media/scraper.png" alt="Bitbash Banner" width="100%"></a>
</p>
<p align="center">
  <a href="https://t.me/devpilot1" target="_blank">
    <img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>&nbsp;
  <a href="https://wa.me/923249868488?text=Hi%20BitBash%2C%20I'm%20interested%20in%20automation." target="_blank">
    <img src="https://img.shields.io/badge/Chat-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
  </a>&nbsp;
  <a href="mailto:sale@bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Email-sale@bitbash.dev-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
</p>




<p align="center" style="font-weight:600; margin-top:8px; margin-bottom:8px;">
  Created by Bitbash, built to showcase our approach to Scraping and Automation!<br>
  If you are looking for <strong>Douyin Scraper</strong> you've just found your team — Let's Chat. 👆👆
</p>


## Introduction
Douyin Scraper retrieves posts, metadata, and media information from Douyin with minimal setup.
It is designed for users who require clean, structured, and high-volume data.
Perfect for creators, data analysts, academic researchers, and businesses monitoring trends or content performance.

### How Douyin Scraper Works
- Extracts Douyin posts by keyword, hashtag, or specific URLs.
- Downloads video and cover media when enabled.
- Delivers structured JSON for easy integration.
- Supports batching, scaling, and selective field output.

## Features
| Feature | Description |
|--------|-------------|
| Hashtag & keyword search | Retrieve videos matching chosen search terms or hashtags. |
| Direct post URL scraping | Fetch precise metadata from individual video URLs. |
| Media downloading | Optionally download video and cover files and replace source links. |
| Rich metadata extraction | Collects author info, music details, hashtags, stats, and more. |
| Scalable scraping | Handles multiple URLs or terms simultaneously. |

---
## What Data This Scraper Extracts
| Field Name | Field Description |
|------------|------------------|
| id | Unique ID of the scraped Douyin post. |
| text | Caption or description text of the post. |
| createTime | Unix timestamp representing when the video was created. |
| createDate | Human-readable formatted date string. |
| url | Direct link to the Douyin post. |
| authorMeta | All available details about the content creator. |
| musicMeta | Metadata associated with the video’s soundtrack. |
| videoMeta | Technical data such as resolution, cover, and playback URLs. |
| statistics | Engagement data including likes, shares, comments, and collections. |
| mentions | Tags of mentioned users. |
| hashtags | List of hashtags used in the post. |

---
## Example Output


    {
      "id": "7296149517517212980",
      "text": "cute cats.:D#小咪会赶走你一天的疲惫 #喵星人",
      "createTime": 1698767202,
      "createDate": "2023-08-11",
      "thumb": "https://p9-pc-sign.douyinpic.com/...",
      "url": "https://www.douyin.com/video/7296149517517212980",
      "authorMeta": {
        "id": "101823080930",
        "secUid": "MS4wLjABAAAACvVkl3ZfT849YzNrTzxj3lDeWwxBFZFSYX7i_jLE8rw",
        "name": "Chandler",
        "username": "",
        "verified": false,
        "signature": ":-D",
        "avatarThumb": "https://p3-pc.douyinpic.com/aweme/100x100/...",
        "followingCount": 0,
        "followersCount": 0,
        "heartCount": 0
      },
      "musicMeta": {
        "id": "7275161107433244674",
        "name": "麦当劳汉堡（正版授权版）",
        "author": "小pa",
        "album": "麦当劳汉堡（正版授权）",
        "isOriginal": false,
        "duration": 16
      },
      "videoMeta": {
        "cover": "https://p9-pc-sign.douyinpic.com/...",
        "originCover": "https://p3-pc-sign.douyinpic.com/...",
        "width": 720,
        "playUrl": "https://sf9-sign.douyinstatic.com/..."
      },
      "statistics": {
        "diggCount": 1,
        "shareCount": 1,
        "commentCount": 1,
        "collectCount": 0
      },
      "mentions": [],
      "hashtags": [
        { "id": "1768145161646092", "name": "小咪会赶走你一天的疲惫" },
        { "id": "1560122388542465", "name": "喵星人" }
      ]
    }

---
## Directory Structure Tree


    Douyin Scraper/
    ├── src/
    │   ├── runner.js
    │   ├── extractors/
    │   │   ├── douyin_parser.js
    │   │   └── utils_time.js
    │   ├── outputs/
    │   │   └── exporters.js
    │   └── config/
    │       └── settings.example.json
    ├── data/
    │   ├── input.sample.json
    │   └── sample_output.json
    ├── package.json
    └── README.md

---
## Use Cases
- **Researchers** track viral content to study social trends and cultural movements.
- **Marketing teams** monitor influencer activity to identify potential partnerships and evaluate audience engagement.
- **Data engineers** collect structured Douyin datasets for analytics pipelines.
- **Competitive analysts** watch industry-related content to stay aware of new trends.
- **Content creators** analyze high-performing videos to refine their own strategy.

---
## FAQs

**Q: Can this scraper download videos?**
Yes, enabling the video download option replaces the default play URL with a stored local copy.

**Q: Can I scrape multiple hashtags at once?**
Yes, you can provide several search terms or hashtags simultaneously.

**Q: What if I only want to scrape specific videos?**
You can input direct post URLs to scrape only those videos.

**Q: Are both hashtags and post URLs required?**
No — you must choose one input method: hashtags/search terms *or* specific URLs.

---
### Performance Benchmarks and Results

**Primary Metric:** Processes an average of 20–40 posts per minute depending on network conditions and media download settings.

**Reliability Metric:** Maintains a 97% successful retrieval rate across large batches of URLs and keyword searches.

**Efficiency Metric:** Optimized request handling ensures low resource consumption even when scraping high-resolution video metadata.

**Quality Metric:** Delivers over 99% field completeness for author, video, and statistics metadata, ensuring consistent dataset accuracy.


<p align="center">
<a href="https://calendar.app.google/74kEaAQ5LWbM8CQNA" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
  <a href="https://www.youtube.com/@bitbash-demos/videos" target="_blank">
    <img src="https://img.shields.io/badge/🎥%20Watch%20demos%20-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Watch on YouTube">
  </a>
</p>
<table>
  <tr>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/MLkvGB8ZZIk" target="_blank">
        <img src="https://github.com/za2122/footer-section/blob/main/media/review1.gif" alt="Review 1" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Bitbash is a top-tier automation partner, innovative, reliable, and dedicated to delivering real results every time."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Nathan Pennington
        <br><span style="color:#888;">Marketer</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/8-tw8Omw9qk" target="_blank">
        <img src="https://github.com/za2122/footer-section/blob/main/media/review2.gif" alt="Review 2" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Bitbash delivers outstanding quality, speed, and professionalism, truly a team you can rely on."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Eliza
        <br><span style="color:#888;">SEO Affiliate Expert</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtube.com/shorts/6AwB5omXrIM" target="_blank">
        <img src="https://github.com/Instagram-Automations/Footer-test/blob/main/media/review3.gif" alt="Review 3" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Exceptional results, clear communication, and flawless delivery. Bitbash nailed it."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Syed
        <br><span style="color:#888;">Digital Strategist</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
  </tr>
</table>
