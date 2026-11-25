# Instagram Profile Scraper: Exact Followers, Reels Views

Get public Instagram profile data from a list of usernames: **exact follower and following counts**, full name, bio, every bio link, verified and private flags, profile picture and the account ID, plus optional **Reels stats: the views of the latest Reels, the account's median and how many times each Reel beat it**, the number creators and agencies use to spot a hit and to judge an account by views instead of followers. Paste usernames, @handles or profile URLs.

**[Run it on Apify](https://apify.com/pomlabs/instagram-profile-data?utm_source=github&utm_medium=readme&utm_campaign=instagram-profile-data)**: no install, no login, free credit on a new Apify account.

## What you get

- **Exact numbers**: followers (e.g. 267,638,613, not "267M") and following
- **Identity**: username, account ID, full name, verified, private
- **Bio and links**: the biography text plus every link in the bio (title and URL)
- **Reels stats (optional)**: views of the latest ~15 Reels, median, average, max and each Reel's multiple of the median
- **Profile picture URL**
- **Clear status per profile**: `ok`, `not_found_or_restricted`, `invalid_username` or `blocked`

## Pricing

**No login, no cookies, no account at risk. You pay only for profiles delivered: $0.0025 per profile.** Profiles that don't exist, invalid usernames and failed requests are listed with the reason and never charged.

That is the free-plan price; Apify paid plans (Bronze, Silver, Gold) pay less per item.

## Call it by API

```bash
curl -X POST "https://api.apify.com/v2/acts/pomlabs~instagram-profile-data/run-sync-get-dataset-items?token=YOUR_APIFY_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"usernames": ["nasa", "https://www.instagram.com/natgeo/"]}'
```

Python:

```python
from apify_client import ApifyClient

client = ApifyClient("YOUR_APIFY_TOKEN")
run = client.actor("pomlabs/instagram-profile-data").call(run_input={"usernames": ["nasa", "https://www.instagram.com/natgeo/"]})
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)
```

## Use it from Claude, Cursor or any MCP client

```bash
claude mcp add instagram-profile "https://mcp.apify.com?tools=pomlabs/instagram-profile-data" -t http
```

## Ready-made examples

- [Get the exact follower count of Instagram profiles](https://apify.com/pomlabs/instagram-profile-data/examples/instagram-exact-follower-count)
- [Average Reels views of an Instagram creator](https://apify.com/pomlabs/instagram-profile-data/examples/instagram-reels-average-views)
- [Compare several Instagram influencers](https://apify.com/pomlabs/instagram-profile-data/examples/compare-instagram-influencers)

## More Actors by Pom Labs

- [YouTube Transcript Scraper: Translate, No Login · $3/1K](https://apify.com/pomlabs/youtube-transcript-scraper?utm_source=github&utm_medium=readme&utm_campaign=instagram-profile-data)
- [Instagram Transcript Scraper: Reels, TikTok, Facebook, Hook](https://apify.com/pomlabs/social-video-transcript?utm_source=github&utm_medium=readme&utm_campaign=instagram-profile-data)
- [Reddit Scraper: Deleted & Removed, Mods, Hidden Profiles](https://apify.com/pomlabs/reddit-posts-comments-scraper?utm_source=github&utm_medium=readme&utm_campaign=instagram-profile-data)
- [LinkedIn Company Scraper (No Cookies): Posts, Similar Companies](https://apify.com/pomlabs/linkedin-company-scraper?utm_source=github&utm_medium=readme&utm_campaign=instagram-profile-data)
- [YouTube Comments Scraper + Replies, Shorts · No API Key · $1/1K](https://apify.com/pomlabs/youtube-comments-scraper?utm_source=github&utm_medium=readme&utm_campaign=instagram-profile-data)
- [LinkedIn Profile Scraper (No Cookies) + Similar Profiles](https://apify.com/pomlabs/linkedin-profile-scraper?utm_source=github&utm_medium=readme&utm_campaign=instagram-profile-data)
- [Threads Scraper: Keyword Search, Posts & Profiles · No Login](https://apify.com/pomlabs/threads-scraper?utm_source=github&utm_medium=readme&utm_campaign=instagram-profile-data)
- [AliExpress Scraper: Exact Units Sold, Prices, Search · $1/1K](https://apify.com/pomlabs/aliexpress-scraper?utm_source=github&utm_medium=readme&utm_campaign=instagram-profile-data)
- [AI Brand Visibility Tracker - ChatGPT, Claude & Perplexity](https://apify.com/pomlabs/ai-brand-visibility?utm_source=github&utm_medium=readme&utm_campaign=instagram-profile-data)
- [Mercado Livre & Amazon BR Coupon Code Checker](https://apify.com/pomlabs/mercadolivre-coupon-checker?utm_source=github&utm_medium=readme&utm_campaign=instagram-profile-data)
- [Page Time Machine · Wayback Diff + AI · No Login · $2.5/1K](https://apify.com/pomlabs/page-time-machine?utm_source=github&utm_medium=readme&utm_campaign=instagram-profile-data)
- [Video Downloader: TikTok No Watermark, Instagram, YouTube, X](https://apify.com/pomlabs/video-downloader?utm_source=github&utm_medium=readme&utm_campaign=instagram-profile-data)
- [NSFW Image Detector & Image Tagger - Moderation + Categories](https://apify.com/pomlabs/image-moderation-tagger?utm_source=github&utm_medium=readme&utm_campaign=instagram-profile-data)
- [Google Trends Scraper: Related Queries, No 429 · $2/1K](https://apify.com/pomlabs/google-trends-scraper?utm_source=github&utm_medium=readme&utm_campaign=instagram-profile-data)

Full documentation, input fields and output format: [Instagram Profile Scraper: Exact Followers, Reels Views on Apify](https://apify.com/pomlabs/instagram-profile-data?utm_source=github&utm_medium=readme&utm_campaign=instagram-profile-data).
