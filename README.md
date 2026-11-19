<!-- Generated from the SocQ API catalog and docs. Do not edit by hand. -->
# Instagram API

[![SocQ Instagram API](https://img.shields.io/badge/API-SocQ%20Instagram%20API-F64C31)](https://socq.ai/apis/instagram?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)
[![API documentation](https://img.shields.io/badge/Docs-docs.socq.ai-111827)](https://docs.socq.ai/api-manual/instagram/overview)
[![License: MIT](https://img.shields.io/badge/License-MIT-2563EB)](LICENSE)
[![Check examples](https://github.com/SocQAPI/instagram-api/actions/workflows/check.yml/badge.svg)](https://github.com/SocQAPI/instagram-api/actions/workflows/check.yml)

25 endpoints for public Instagram data through one SocQ API key, with runnable cURL, Node.js and Python examples and a valid request body for every endpoint.

[Browse Instagram APIs](https://socq.ai/apis/instagram?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api) · [Get an API key](https://socq.ai/dashboard/api-key?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api) · [Documentation](https://docs.socq.ai/api-manual/instagram/overview) · [All SocQ examples](https://github.com/SocQAPI/socq-examples)

## Endpoints

Prices are in SocQ credits; 1 credit = $0.005.

| Endpoint | publicId | What it returns | Price | Launched |
| --- | --- | --- | --- | --- |
| [Instagram Followers Count API](#instagram-followers-count-api) | `instagram/followers-count` | Collect public Instagram profile details and visible follower, following, and post counts for usernames or profile URLs. | 0.52 credits ($0.0026) per result | 2026-07-11 |
| [Instagram Posts API](#instagram-posts-api) | `instagram/posts` | Collect public Instagram posts for one or more usernames, including captions, author data, media references, hashtags, mentions, and visible engagement metrics. | 0.34 credits ($0.0017) per result | 2026-07-11 |
| [Instagram Reels API](#instagram-reels-api) | `instagram/reels` | Collect public Instagram Reels for one or more usernames, including captions, media references, visible engagement metrics, duration, and audio details. | 0.52 credits ($0.0026) per result | 2026-07-11 |
| [Instagram Search API](#instagram-search-api) | `instagram/search` | Search public Instagram profiles by keyword or handle and return normalized profile identity, biography, verification, privacy, and visible count fields. | 0.54 credits ($0.0027) per result | 2026-07-11 |
| [Instagram Comments API](#instagram-comments-api) | `instagram/comments` | Collect normalized public Instagram comments from public post URLs, including text, author fields, timestamps, post references, and visible engagement metrics. | 0.3 credits ($0.0015) per result | 2026-07-15 |
| [Instagram Profiles API](#instagram-profiles-api) | `instagram/profiles` | Retrieve public Instagram profiles for one or more usernames, returning normalized identity, biographies, links, account flags, and visible follower, following, and post counts. | 0.6 credits ($0.003) per result | 2026-07-23 |
| [Instagram Followers List API](#instagram-followers-list-api) | `instagram/followers-list` | Collect public profile records visible in the follower lists of one or more Instagram usernames, with normalized identity and relationship context. | 0.3 credits ($0.0015) per result | 2026-07-23 |
| [Instagram Following List API](#instagram-following-list-api) | `instagram/following-list` | Collect public profiles followed by one or more Instagram accounts, including profile identity, relationship context, and visible account metrics. | 0.3 credits ($0.0015) per result | 2026-07-23 |
| [Instagram Hashtag Posts API](#instagram-hashtag-posts-api) | `instagram/hashtag-posts` | Collect public Instagram posts for one or more hashtags, with author details, captions, media, source hashtags, timestamps, and visible engagement metrics. | 0.5 credits ($0.0025) per result | 2026-07-22 |
| [Instagram Tagged Posts API](#instagram-tagged-posts-api) | `instagram/tagged-posts` | Collect public Instagram posts that tag one or more profiles, including captions, authors, media, tagged-user context, mentions, and visible engagement. | 0.5 credits ($0.0025) per result | 2026-07-23 |
| [Instagram Transcript API](#instagram-transcript-api) | `instagram/transcript` | Extract transcript records from public Instagram post and Reel URLs, returning text, language, format, source URLs, and shortcodes in a normalized structure. | 0.7 credits ($0.0035) per result | 2026-07-22 |
| [Instagram Audio Reels API](#instagram-audio-reels-api) | `instagram/audio-reels` | Collect public Instagram Reels associated with known numeric audio IDs, returning normalized captions, creator identity, media, timestamps, visible engagement, and source audio context. | 0.5 credits ($0.0025) per result | 2026-07-25 |
| [Instagram Highlight Items API](#instagram-highlight-items-api) | `instagram/highlight-items` | Retrieve public Story items from known Instagram highlight IDs as normalized records with text, author identity, visible metrics, media details, and source context. | 0.5 credits ($0.0025) per result | 2026-07-25 |
| [Instagram Post Info API](#instagram-post-info-api) | `instagram/post-info` | Retrieve details for known public Instagram post, Reel, or legacy IGTV URLs, including captions, author identity, media, timestamps, visible engagement, and input context. | 0.5 credits ($0.0025) per result | 2026-07-25 |
| [Instagram Reels Search API](#instagram-reels-search-api) | `instagram/reels-search` | Search public Instagram Reels with a text query, returning captions, creators, media, timestamps, visible engagement, and query context in normalized records. | 0.5 credits ($0.0025) per result | 2026-07-25 |
| [Instagram Story Highlights API](#instagram-story-highlights-api) | `instagram/story-highlights` | Collect public Instagram Story Highlight containers from one or more usernames, returning normalized titles, owner identity, media, counts, and reusable highlight IDs. | 0.5 credits ($0.0025) per result | 2026-07-25 |
| [Instagram Trending Reels API](#instagram-trending-reels-api) | `instagram/trending-reels` | Collect the current Reel set exposed by the trending feed without selectors, returning captions, authors, media, timestamps, and visible engagement. | 0.5 credits ($0.0025) per result | 2026-07-25 |
| [Instagram Stories API](#instagram-stories-api) | `instagram/stories` | Collect the stories a public Instagram account is showing right now from its username, returning each story's image or video, posting and expiry times, and link stickers. | 0.5 credits ($0.0025) per result | 2026-11-09 |
| [Instagram Similar Accounts API](#instagram-similar-accounts-api) | `instagram/similar-users` | Find the accounts Instagram recommends alongside a public profile from its username, returning each suggestion's username, display name, avatar, and verified status. | 0.5 credits ($0.0025) per result | 2026-11-09 |
| [Instagram Comment Replies API](#instagram-comment-replies-api) | `instagram/comment-replies` | Collect the replies under a public Instagram comment from the post URL and comment ID, returning reply text, authors, like counts, timestamps, and mentioned accounts. | 0.3 credits ($0.0015) per result | 2026-11-09 |
| [Instagram Post Likers API](#instagram-post-likers-api) | `instagram/post-likers` | Collect the accounts in a public Instagram post's likers list from its URL, returning each liker's username, display name, avatar, and verified and private status. | 0.3 credits ($0.0015) per result | 2026-11-09 |
| [Instagram Location Info API](#instagram-location-info-api) | `instagram/location-info` | Look up an Instagram location by ID or location page URL and get its name, category, phone, city, coordinates, and how many posts are tagged there. | 0.5 credits ($0.0025) per call | 2026-11-09 |
| [Instagram Location Posts API](#instagram-location-posts-api) | `instagram/location-posts` | Collect public posts and reels tagged at an Instagram location by ID or URL, returning captions, authors, likes, comments, media, and timestamps, ordered by top or recent. | 0.5 credits ($0.0025) per result | 2026-11-09 |
| [Instagram Location Search API](#instagram-location-search-api) | `instagram/location-search` | Search Instagram locations by place name or by latitude and longitude, returning location IDs with names, addresses, cities, and coordinates for follow-up lookups. | 0.5 credits ($0.0025) per call | 2026-11-09 |
| [Instagram Hashtag Search API](#instagram-hashtag-search-api) | `instagram/search-hashtags` | Search Instagram hashtags by keyword and get the matching tags with their IDs, tag page links, and the number of posts using each one. | 0.5 credits ($0.0025) per result | 2026-11-09 |

## Quick start

1. Create an API key at [socq.ai/dashboard/api-key](https://socq.ai/dashboard/api-key?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api).
2. Export it. The examples read only `SOCQ_API_KEY`.

```bash
git clone https://github.com/SocQAPI/instagram-api.git
cd instagram-api
export SOCQ_API_KEY="your-api-key"
```

3. Run any endpoint by its publicId. Without a second argument the script sends `payloads/<slug>.json`; pass a JSON file or an inline JSON object to change the input.

```bash
# Node.js 20+
node examples/node/socq.mjs instagram/followers-count

# Python 3.8+ (standard library only)
python3 examples/python/socq.py instagram/followers-count payloads/followers-count.json

# cURL + jq
bash examples/curl/socq.sh instagram/followers-count '{"usernames":["instagram"]}'
```

Each script submits the task, polls it until it succeeds or fails, follows every result page, and writes the records to `output/<slug>-<task_id>.json`. Run `npm run check` to validate the payloads and scripts offline.

Never expose `SOCQ_API_KEY` in browser code, mobile apps, public repositories, screenshots, fixtures or logs.

## How the API works

Base URL `https://api.socq.ai`. Every request sends the API key as a bearer token:

```http
Authorization: Bearer <SOCQ_API_KEY>
Content-Type: application/json
```

All endpoints are asynchronous:

```text
POST /v1/<publicId>  ->  data.task_id  ->  GET /v1/tasks/{task_id}  ->  queued | running | succeeded | failed
```

1. **Submit** the JSON body to `POST https://api.socq.ai/v1/<publicId>`. The response returns `data.task_id` immediately; it means the task was created, not that data is ready.
2. **Poll** `GET https://api.socq.ai/v1/tasks/{task_id}` until `data.status` is `succeeded` or `failed` (a failed task carries `data.error_message`).
3. **Read results.** A succeeded task returns normalized records in `data.results.items`. Use `limit` (default 50, max 500) and pass `data.results.next_cursor` as `cursor` while `data.results.has_more` is true. `fields` selects up to 50 comma-separated fields or dot paths.
4. **Raw files (optional).** `GET https://api.socq.ai/v1/tasks/{task_id}/files` lists raw JSONL exports.

```bash
curl "https://api.socq.ai/v1/tasks/$TASK_ID?limit=100" \
  -H "Authorization: Bearer $SOCQ_API_KEY"

curl "https://api.socq.ai/v1/tasks/$TASK_ID?limit=100&cursor=$NEXT_CURSOR" \
  -H "Authorization: Bearer $SOCQ_API_KEY"
```

`callback_url` (where an endpoint accepts it) makes SocQ POST to your URL when the task reaches a terminal state; keep polling as a fallback.

**Billing.** A submit may reserve credits from `results_limit` or the number of submitted inputs; when the task finishes SocQ settles the charge from the actual result count and returns unused reserved credits. `402` means insufficient credits.

**Errors.** `400` invalid body or unsupported field, `401` missing or invalid key, `402` insufficient credits, `403` IP allowlist or task owned by another account, `404` endpoint or task not found, `422` input validation failed, `429` rate or credit-window limit (respect `Retry-After`), `500` submission failed. A client-side timeout does not cancel a task: resume polling the same `task_id` instead of submitting again.

Reference: [Authentication](https://docs.socq.ai/api-manual/agent-api/authentication) · [Task status and results](https://docs.socq.ai/api-manual/agent-api/status) · [Task files](https://docs.socq.ai/api-manual/agent-api/files) · [Callbacks](https://docs.socq.ai/api-manual/agent-api/callbacks) · [Errors](https://docs.socq.ai/api-manual/agent-api/errors)

## Endpoint reference

### Instagram Followers Count API

Collect public Instagram profile details and visible follower, following, and post counts for usernames or profile URLs.

- **Request:** `POST https://api.socq.ai/v1/instagram/followers-count`
- **publicId:** `instagram/followers-count`
- **Price:** 0.52 credits ($0.0026) per result
- **Launched:** 2026-07-11
- **Example body:** [`payloads/followers-count.json`](payloads/followers-count.json)

Collect public follower and following counts for Instagram profiles.

Provide usernames or public Instagram profile URLs. query is ignored and cannot be used as the only input.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `query` | string | No | Deprecated and ignored. Provide usernames or public profile URLs; use Instagram Search for keyword searches. (deprecated) |
| `results_limit` | integer | No | (value 1 to 2000) |
| `urls` | array of string | One of* | Public profile or content URLs. (items at least 1) |
| `usernames` | array of string | One of* | Public account usernames. (items at least 1) |

*Required rule: send at least one of `urls`, `usernames`.

```bash
curl -X POST "https://api.socq.ai/v1/instagram/followers-count" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "usernames": [
    "instagram"
  ]
}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/followers-count](https://docs.socq.ai/api-manual/instagram/followers-count) · Landing page: [socq.ai/apis/instagram/followers-count](https://socq.ai/apis/instagram/followers-count?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

### Instagram Posts API

Collect public Instagram posts for one or more usernames, including captions, author data, media references, hashtags, mentions, and visible engagement metrics.

- **Request:** `POST https://api.socq.ai/v1/instagram/posts`
- **publicId:** `instagram/posts`
- **Price:** 0.34 credits ($0.0017) per result
- **Launched:** 2026-07-11
- **Example body:** [`payloads/posts.json`](payloads/posts.json)

Collect public Instagram post data, including caption text, engagement metrics, media URLs, author fields, and raw JSONL output.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `query` | string | No | Deprecated for Instagram Posts and does not select posts. Use usernames or profile URLs, or call Instagram Search. (deprecated) |
| `results_limit` | integer | No | (value 1 to 2000) |
| `urls` | array of string | One of* | Public profile or content URLs. (items at least 1) |
| `usernames` | array of string | One of* | Public account usernames. (items at least 1) |

*Required rule: send at least one of `urls`, `usernames`.

```bash
curl -X POST "https://api.socq.ai/v1/instagram/posts" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "usernames": [
    "instagram"
  ],
  "results_limit": 10
}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/posts](https://docs.socq.ai/api-manual/instagram/posts) · Landing page: [socq.ai/apis/instagram/posts](https://socq.ai/apis/instagram/posts?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

### Instagram Reels API

Collect public Instagram Reels for one or more usernames, including captions, media references, visible engagement metrics, duration, and audio details.

- **Request:** `POST https://api.socq.ai/v1/instagram/reels`
- **publicId:** `instagram/reels`
- **Price:** 0.52 credits ($0.0026) per result
- **Launched:** 2026-07-11
- **Example body:** [`payloads/reels.json`](payloads/reels.json)

Collect public Instagram reel data, including caption text, view counts, engagement metrics, media fields, and raw JSONL output.

Provide usernames or public Instagram profile URLs. query is ignored and cannot be used as the only input.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `query` | string | No | Deprecated and ignored. Provide usernames or public profile URLs; use Instagram Search for keyword searches. (deprecated) |
| `results_limit` | integer | No | (value 1 to 2000) |
| `urls` | array of string | One of* | Public profile or content URLs. (items at least 1) |
| `usernames` | array of string | One of* | Public account usernames. (items at least 1) |

*Required rule: send at least one of `urls`, `usernames`.

```bash
curl -X POST "https://api.socq.ai/v1/instagram/reels" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "usernames": [
    "instagram"
  ],
  "results_limit": 10
}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/reels](https://docs.socq.ai/api-manual/instagram/reels) · Landing page: [socq.ai/apis/instagram/reels](https://socq.ai/apis/instagram/reels?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

### Instagram Search API

Search public Instagram profiles by keyword or handle and return normalized profile identity, biography, verification, privacy, and visible count fields.

- **Request:** `POST https://api.socq.ai/v1/instagram/search`
- **publicId:** `instagram/search`
- **Price:** 0.54 credits ($0.0027) per result
- **Launched:** 2026-07-11
- **Example body:** [`payloads/search.json`](payloads/search.json)

Search public Instagram profiles for username and creator discovery workflows.

query is required and accepts keywords, not task instructions. Separate multiple terms with commas; punctuation such as @, #, quotes, periods, slashes and hyphens is unsupported. results_limit is 1 to 250. urls and usernames are deprecated and ignored.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `query` | string | Yes | One or more search keywords. Separate multiple terms with commas. Punctuation such as @, #, quotes, periods, slashes and hyphens is not supported; do not send natural-language task instructions. (pattern `^[^!?.,:;\\-+=*&%$#@/\\\\~^\|<>()[\\]{}"'`]+(?:,[^!?.,:;\\-+=*&%$#@/\\\\~^\|<>()[\\]{}"'`]+)*$`) |
| `results_limit` | integer | No | (value 1 to 250) |
| `urls` | array of string | No | Deprecated and ignored for search. Provide query instead. (items at least 1; deprecated) |
| `usernames` | array of string | No | Deprecated and ignored for search. Provide query instead. (items at least 1; deprecated) |

```bash
curl -X POST "https://api.socq.ai/v1/instagram/search" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "query": "instagram",
  "results_limit": 20
}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/search](https://docs.socq.ai/api-manual/instagram/search) · Landing page: [socq.ai/apis/instagram/search](https://socq.ai/apis/instagram/search?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

### Instagram Comments API

Collect normalized public Instagram comments from public post URLs, including text, author fields, timestamps, post references, and visible engagement metrics.

- **Request:** `POST https://api.socq.ai/v1/instagram/comments`
- **publicId:** `instagram/comments`
- **Price:** 0.3 credits ($0.0015) per result
- **Launched:** 2026-07-15
- **Example body:** [`payloads/comments.json`](payloads/comments.json)

Collect public Instagram comment data for public post URLs, including comment text, author fields, engagement metrics, and raw JSONL output.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `urls` | array of string | Yes | Public profile or content URLs. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/instagram/comments" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "urls": [
    "https://www.instagram.com/reel/DBZMUClOJjZ/"
  ]
}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/comments](https://docs.socq.ai/api-manual/instagram/comments) · Landing page: [socq.ai/apis/instagram/comments](https://socq.ai/apis/instagram/comments?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

### Instagram Profiles API

Retrieve public Instagram profiles for one or more usernames, returning normalized identity, biographies, links, account flags, and visible follower, following, and post counts.

- **Request:** `POST https://api.socq.ai/v1/instagram/profiles`
- **publicId:** `instagram/profiles`
- **Price:** 0.6 credits ($0.003) per result
- **Launched:** 2026-07-23
- **Example body:** [`payloads/profiles.json`](payloads/profiles.json)

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `usernames` | array of string | Yes | Public Instagram usernames, with an optional leading @. (items 1 to 100; pattern `^@?[A-Za-z0-9._]{1,30}$`) |

```bash
curl -X POST "https://api.socq.ai/v1/instagram/profiles" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "usernames": [
    "instagram",
    "natgeo"
  ]
}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/profiles](https://docs.socq.ai/api-manual/instagram/profiles) · Landing page: [socq.ai/apis/instagram/profiles](https://socq.ai/apis/instagram/profiles?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

### Instagram Followers List API

Collect public profile records visible in the follower lists of one or more Instagram usernames, with normalized identity and relationship context.

- **Request:** `POST https://api.socq.ai/v1/instagram/followers-list`
- **publicId:** `instagram/followers-list`
- **Price:** 0.3 credits ($0.0015) per result
- **Launched:** 2026-07-23
- **Example body:** [`payloads/followers-list.json`](payloads/followers-list.json)

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `results_limit` | integer | No | (value 1 to 2000) |
| `usernames` | array of string | Yes | Public account usernames. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/instagram/followers-list" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "usernames": [
    "instagram"
  ],
  "results_limit": 100
}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/followers-list](https://docs.socq.ai/api-manual/instagram/followers-list) · Landing page: [socq.ai/apis/instagram/followers-list](https://socq.ai/apis/instagram/followers-list?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

### Instagram Following List API

Collect public profiles followed by one or more Instagram accounts, including profile identity, relationship context, and visible account metrics.

- **Request:** `POST https://api.socq.ai/v1/instagram/following-list`
- **publicId:** `instagram/following-list`
- **Price:** 0.3 credits ($0.0015) per result
- **Launched:** 2026-07-23
- **Example body:** [`payloads/following-list.json`](payloads/following-list.json)

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `results_limit` | integer | No | (value 1 to 2000) |
| `usernames` | array of string | Yes | Public account usernames. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/instagram/following-list" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "usernames": [
    "instagram"
  ],
  "results_limit": 100
}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/following-list](https://docs.socq.ai/api-manual/instagram/following-list) · Landing page: [socq.ai/apis/instagram/following-list](https://socq.ai/apis/instagram/following-list?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

### Instagram Hashtag Posts API

Collect public Instagram posts for one or more hashtags, with author details, captions, media, source hashtags, timestamps, and visible engagement metrics.

- **Request:** `POST https://api.socq.ai/v1/instagram/hashtag-posts`
- **publicId:** `instagram/hashtag-posts`
- **Price:** 0.5 credits ($0.0025) per result
- **Launched:** 2026-07-22
- **Example body:** [`payloads/hashtag-posts.json`](payloads/hashtag-posts.json)

Search hashtags, not account usernames. An explicit no-posts response completes successfully with an empty results.items list. Other access or service errors remain failures. Empty collections follow the normal empty-result billing policy.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `hashtags` | array of string | Yes | Hashtags with or without the # prefix. (items at least 1) |
| `media_type` | string | No | - |
| `published_within` | string | No | - |
| `results_limit` | integer | No | (value 10 to 2000) |

```bash
curl -X POST "https://api.socq.ai/v1/instagram/hashtag-posts" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "hashtags": [
    "#travel"
  ],
  "results_limit": 20,
  "published_within": "week",
  "media_type": "all"
}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/hashtag-posts](https://docs.socq.ai/api-manual/instagram/hashtag-posts) · Landing page: [socq.ai/apis/instagram/hashtag-posts](https://socq.ai/apis/instagram/hashtag-posts?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

### Instagram Tagged Posts API

Collect public Instagram posts that tag one or more profiles, including captions, authors, media, tagged-user context, mentions, and visible engagement.

- **Request:** `POST https://api.socq.ai/v1/instagram/tagged-posts`
- **publicId:** `instagram/tagged-posts`
- **Price:** 0.5 credits ($0.0025) per result
- **Launched:** 2026-07-23
- **Example body:** [`payloads/tagged-posts.json`](payloads/tagged-posts.json)

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `results_limit` | integer | No | (value 1 to 2000) |
| `usernames` | array of string | Yes | Public account usernames. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/instagram/tagged-posts" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "usernames": [
    "instagram"
  ],
  "results_limit": 20
}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/tagged-posts](https://docs.socq.ai/api-manual/instagram/tagged-posts) · Landing page: [socq.ai/apis/instagram/tagged-posts](https://socq.ai/apis/instagram/tagged-posts?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

### Instagram Transcript API

Extract transcript records from public Instagram post and Reel URLs, returning text, language, format, source URLs, and shortcodes in a normalized structure.

- **Request:** `POST https://api.socq.ai/v1/instagram/transcript`
- **publicId:** `instagram/transcript`
- **Price:** 0.7 credits ($0.0035) per result
- **Launched:** 2026-07-22
- **Example body:** [`payloads/transcript.json`](payloads/transcript.json)

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `urls` | array of string | Yes | Public profile or content URLs. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/instagram/transcript" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "urls": [
    "https://www.instagram.com/reel/SHORTCODE/"
  ]
}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/transcript](https://docs.socq.ai/api-manual/instagram/transcript) · Landing page: [socq.ai/apis/instagram/transcript](https://socq.ai/apis/instagram/transcript?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

### Instagram Audio Reels API

Collect public Instagram Reels associated with known numeric audio IDs, returning normalized captions, creator identity, media, timestamps, visible engagement, and source audio context.

- **Request:** `POST https://api.socq.ai/v1/instagram/audio-reels`
- **publicId:** `instagram/audio-reels`
- **Price:** 0.5 credits ($0.0025) per result
- **Launched:** 2026-07-25
- **Example body:** [`payloads/audio-reels.json`](payloads/audio-reels.json)

Collect public Instagram Reels for audio IDs. Results are normalized and billed by the actual saved record count.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `audio_ids` | array of string | Yes | Public Instagram audio identifiers. (items at least 1) |
| `callback_url` | string (uri) | No | - |
| `results_limit` | integer | No | (value 20 to 2000; default `100`) |

```bash
curl -X POST "https://api.socq.ai/v1/instagram/audio-reels" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "audio_ids": [
    "1383262936846577"
  ],
  "results_limit": 20
}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/audio-reels](https://docs.socq.ai/api-manual/instagram/audio-reels) · Landing page: [socq.ai/apis/instagram/audio-reels](https://socq.ai/apis/instagram/audio-reels?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

### Instagram Highlight Items API

Retrieve public Story items from known Instagram highlight IDs as normalized records with text, author identity, visible metrics, media details, and source context.

- **Request:** `POST https://api.socq.ai/v1/instagram/highlight-items`
- **publicId:** `instagram/highlight-items`
- **Price:** 0.5 credits ($0.0025) per result
- **Launched:** 2026-07-25
- **Example body:** [`payloads/highlight-items.json`](payloads/highlight-items.json)

Collect items from public Instagram highlights. Results are normalized and billed by the actual saved record count.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `highlight_ids` | array of string | Yes | Public Instagram highlight identifiers. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/instagram/highlight-items" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "highlight_ids": [
    "18067016518767507"
  ]
}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/highlight-items](https://docs.socq.ai/api-manual/instagram/highlight-items) · Landing page: [socq.ai/apis/instagram/highlight-items](https://socq.ai/apis/instagram/highlight-items?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

### Instagram Post Info API

Retrieve details for known public Instagram post, Reel, or legacy IGTV URLs, including captions, author identity, media, timestamps, visible engagement, and input context.

- **Request:** `POST https://api.socq.ai/v1/instagram/post-info`
- **publicId:** `instagram/post-info`
- **Price:** 0.5 credits ($0.0025) per result
- **Launched:** 2026-07-25
- **Example body:** [`payloads/post-info.json`](payloads/post-info.json)

Collect detailed public Instagram post data. Results are normalized and billed by the actual saved record count.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `urls` | array of string | Yes | Public profile or content URLs. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/instagram/post-info" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "urls": [
    "https://www.instagram.com/p/DbbY9pdm6Q2/"
  ]
}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/post-info](https://docs.socq.ai/api-manual/instagram/post-info) · Landing page: [socq.ai/apis/instagram/post-info](https://socq.ai/apis/instagram/post-info?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

### Instagram Reels Search API

Search public Instagram Reels with a text query, returning captions, creators, media, timestamps, visible engagement, and query context in normalized records.

- **Request:** `POST https://api.socq.ai/v1/instagram/reels-search`
- **publicId:** `instagram/reels-search`
- **Price:** 0.5 credits ($0.0025) per result
- **Launched:** 2026-07-25
- **Example body:** [`payloads/reels-search.json`](payloads/reels-search.json)

Search public Instagram Reels. Results are normalized and billed by the actual saved record count.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `published_within` | string | No | - |
| `query` | string | Yes | Search query. |
| `results_limit` | integer | No | (value 20 to 2000; default `100`) |

```bash
curl -X POST "https://api.socq.ai/v1/instagram/reels-search" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "query": "street photography",
  "results_limit": 20
}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/reels-search](https://docs.socq.ai/api-manual/instagram/reels-search) · Landing page: [socq.ai/apis/instagram/reels-search](https://socq.ai/apis/instagram/reels-search?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

### Instagram Story Highlights API

Collect public Instagram Story Highlight containers from one or more usernames, returning normalized titles, owner identity, media, counts, and reusable highlight IDs.

- **Request:** `POST https://api.socq.ai/v1/instagram/story-highlights`
- **publicId:** `instagram/story-highlights`
- **Price:** 0.5 credits ($0.0025) per result
- **Launched:** 2026-07-25
- **Example body:** [`payloads/story-highlights.json`](payloads/story-highlights.json)

Collect public Instagram story highlights. Results are normalized and billed by the actual saved record count.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `usernames` | array of string | Yes | Public account usernames. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/instagram/story-highlights" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "usernames": [
    "instagram"
  ]
}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/story-highlights](https://docs.socq.ai/api-manual/instagram/story-highlights) · Landing page: [socq.ai/apis/instagram/story-highlights](https://socq.ai/apis/instagram/story-highlights?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

### Instagram Trending Reels API

Collect the current Reel set exposed by the trending feed without selectors, returning captions, authors, media, timestamps, and visible engagement.

- **Request:** `POST https://api.socq.ai/v1/instagram/trending-reels`
- **publicId:** `instagram/trending-reels`
- **Price:** 0.5 credits ($0.0025) per result
- **Launched:** 2026-07-25
- **Example body:** [`payloads/trending-reels.json`](payloads/trending-reels.json)

Collect currently trending public Instagram Reels. Results are normalized and billed by the actual saved record count.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |

```bash
curl -X POST "https://api.socq.ai/v1/instagram/trending-reels" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/trending-reels](https://docs.socq.ai/api-manual/instagram/trending-reels) · Landing page: [socq.ai/apis/instagram/trending-reels](https://socq.ai/apis/instagram/trending-reels?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

### Instagram Stories API

Collect the stories a public Instagram account is showing right now from its username, returning each story's image or video, posting and expiry times, and link stickers.

- **Request:** `POST https://api.socq.ai/v1/instagram/stories`
- **publicId:** `instagram/stories`
- **Price:** 0.5 credits ($0.0025) per result
- **Launched:** 2026-11-09
- **Example body:** [`payloads/stories.json`](payloads/stories.json)

Collect the stories a public Instagram account currently has live, with media URLs, the author and posting times. Submit an asynchronous task, then read its standard results.

Provide a public Instagram username. Returns the stories the account currently has live; each story stays available for 24 hours after posting.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `username` | string | Yes | Public Instagram username, with an optional leading @. (pattern `^@?[A-Za-z0-9._]{1,30}$`) |

```bash
curl -X POST "https://api.socq.ai/v1/instagram/stories" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "username": "natgeo"
}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/stories](https://docs.socq.ai/api-manual/instagram/stories) · Landing page: [socq.ai/apis/instagram/stories](https://socq.ai/apis/instagram/stories?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

### Instagram Similar Accounts API

Find the accounts Instagram recommends alongside a public profile from its username, returning each suggestion's username, display name, avatar, and verified status.

- **Request:** `POST https://api.socq.ai/v1/instagram/similar-users`
- **publicId:** `instagram/similar-users`
- **Price:** 0.5 credits ($0.0025) per result
- **Launched:** 2026-11-09
- **Example body:** [`payloads/similar-users.json`](payloads/similar-users.json)

Look up the accounts Instagram suggests as similar to a public account, with usernames, display names, avatars and verification status. Submit an asynchronous task, then read its standard results.

Provide a public Instagram username. Returns the accounts Instagram suggests as similar to it; results_limit sets how many to return (default 50, up to 100).

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `results_limit` | integer | No | (value 1 to 100; default `50`) |
| `username` | string | Yes | Public Instagram username, with an optional leading @. (pattern `^@?[A-Za-z0-9._]{1,30}$`) |

```bash
curl -X POST "https://api.socq.ai/v1/instagram/similar-users" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "username": "instagram",
  "results_limit": 50
}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/similar-users](https://docs.socq.ai/api-manual/instagram/similar-users) · Landing page: [socq.ai/apis/instagram/similar-users](https://socq.ai/apis/instagram/similar-users?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

### Instagram Comment Replies API

Collect the replies under a public Instagram comment from the post URL and comment ID, returning reply text, authors, like counts, timestamps, and mentioned accounts.

- **Request:** `POST https://api.socq.ai/v1/instagram/comment-replies`
- **publicId:** `instagram/comment-replies`
- **Price:** 0.3 credits ($0.0015) per result
- **Launched:** 2026-11-09
- **Example body:** [`payloads/comment-replies.json`](payloads/comment-replies.json)

Collect the replies under one comment on a public Instagram post, reel or IGTV video, with reply text, authors, like counts and posting times. Submit an asynchronous task, then read its standard results.

Provide the post, reel or IGTV url and the comment_id of the comment whose replies you want; results_limit sets how many replies to return (default 100, up to 1000).

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `comment_id` | string | Yes | Numeric ID of the parent comment, such as the id returned by Instagram Comments. (pattern `^[0-9]{5,32}$`) |
| `results_limit` | integer | No | (value 1 to 1000; default `100`) |
| `url` | string | Yes | Public Instagram post, reel or IGTV URL. |

```bash
curl -X POST "https://api.socq.ai/v1/instagram/comment-replies" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "url": "https://www.instagram.com/p/DRhvwVLAHAG/",
  "comment_id": "18117277147949901",
  "results_limit": 100
}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/comment-replies](https://docs.socq.ai/api-manual/instagram/comment-replies) · Landing page: [socq.ai/apis/instagram/comment-replies](https://socq.ai/apis/instagram/comment-replies?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

### Instagram Post Likers API

Collect the accounts in a public Instagram post's likers list from its URL, returning each liker's username, display name, avatar, and verified and private status.

- **Request:** `POST https://api.socq.ai/v1/instagram/post-likers`
- **publicId:** `instagram/post-likers`
- **Price:** 0.3 credits ($0.0015) per result
- **Launched:** 2026-11-09
- **Example body:** [`payloads/post-likers.json`](payloads/post-likers.json)

Collect the accounts shown in the likers list of a public Instagram post, with usernames, display names, avatars and verification status. Submit an asynchronous task, then read its standard results.

Provide a public post, reel or IGTV url. Returns the accounts shown in the post's likers list; results_limit sets how many to return (default 100, up to 1000).

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `results_limit` | integer | No | (value 1 to 1000; default `100`) |
| `url` | string | Yes | Public Instagram post, reel or IGTV URL. |

```bash
curl -X POST "https://api.socq.ai/v1/instagram/post-likers" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "url": "https://www.instagram.com/p/DRhvwVLAHAG/",
  "results_limit": 100
}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/post-likers](https://docs.socq.ai/api-manual/instagram/post-likers) · Landing page: [socq.ai/apis/instagram/post-likers](https://socq.ai/apis/instagram/post-likers?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

### Instagram Location Info API

Look up an Instagram location by ID or location page URL and get its name, category, phone, city, coordinates, and how many posts are tagged there.

- **Request:** `POST https://api.socq.ai/v1/instagram/location-info`
- **publicId:** `instagram/location-info`
- **Price:** 0.5 credits ($0.0025) per call
- **Launched:** 2026-11-09
- **Example body:** [`payloads/location-info.json`](payloads/location-info.json)

Look up an Instagram location by ID or location page URL and return its name, category, phone number, city and coordinates. Submit an asynchronous task, then read its standard results.

Identify the location with either location_id or its location page url.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `location_id` | string | One of* | Numeric Instagram location ID, as returned by Instagram Location Search. (pattern `^[0-9]{1,32}$`) |
| `url` | string | One of* | Instagram location page URL, such as https://www.instagram.com/explore/locations/212988663/. |

*Required rule: send at least one of `location_id`, `url`; do not send `location_id` and `url` together.

```bash
curl -X POST "https://api.socq.ai/v1/instagram/location-info" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "location_id": "384695225271379"
}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/location-info](https://docs.socq.ai/api-manual/instagram/location-info) · Landing page: [socq.ai/apis/instagram/location-info](https://socq.ai/apis/instagram/location-info?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

### Instagram Location Posts API

Collect public posts and reels tagged at an Instagram location by ID or URL, returning captions, authors, likes, comments, media, and timestamps, ordered by top or recent.

- **Request:** `POST https://api.socq.ai/v1/instagram/location-posts`
- **publicId:** `instagram/location-posts`
- **Price:** 0.5 credits ($0.0025) per result
- **Launched:** 2026-11-09
- **Example body:** [`payloads/location-posts.json`](payloads/location-posts.json)

Collect public posts tagged at an Instagram location, either the top posts or the newest ones, with captions, authors, like and comment counts and media. Submit an asynchronous task, then read its standard results.

Identify the location with either location_id or its location page url. Set sort_by to top (default) for the location's top posts or recent for the newest posts; results_limit sets how many posts to return (default 20, up to 100).

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `location_id` | string | One of* | Numeric Instagram location ID, as returned by Instagram Location Search. (pattern `^[0-9]{1,32}$`) |
| `results_limit` | integer | No | (value 1 to 100; default `20`) |
| `sort_by` | string | No | (one of `recent`, `top`; default `"top"`) |
| `url` | string | One of* | Instagram location page URL, such as https://www.instagram.com/explore/locations/212988663/. |

*Required rule: send at least one of `location_id`, `url`; do not send `location_id` and `url` together.

```bash
curl -X POST "https://api.socq.ai/v1/instagram/location-posts" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "location_id": "384695225271379",
  "sort_by": "top",
  "results_limit": 20
}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/location-posts](https://docs.socq.ai/api-manual/instagram/location-posts) · Landing page: [socq.ai/apis/instagram/location-posts](https://socq.ai/apis/instagram/location-posts?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

### Instagram Location Search API

Search Instagram locations by place name or by latitude and longitude, returning location IDs with names, addresses, cities, and coordinates for follow-up lookups.

- **Request:** `POST https://api.socq.ai/v1/instagram/location-search`
- **publicId:** `instagram/location-search`
- **Price:** 0.5 credits ($0.0025) per call
- **Launched:** 2026-11-09
- **Example body:** [`payloads/location-search.json`](payloads/location-search.json)

Search Instagram locations by a place name or by latitude and longitude, and get location IDs with names, addresses, cities and coordinates. Submit an asynchronous task, then read its standard results.

Search by place name with query, or by a point on the map with latitude and longitude. Coordinate search returns the places around that point.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `latitude` | number | One of* | (value -90 to 90) |
| `longitude` | number | One of* | (value -180 to 180) |
| `query` | string | One of* | Place name, landmark or city to search for. (length 1 to 100) |

*Required rule: send at least one of these field sets: `query`, `latitude` + `longitude`.

```bash
curl -X POST "https://api.socq.ai/v1/instagram/location-search" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "query": "Times Square"
}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/location-search](https://docs.socq.ai/api-manual/instagram/location-search) · Landing page: [socq.ai/apis/instagram/location-search](https://socq.ai/apis/instagram/location-search?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

### Instagram Hashtag Search API

Search Instagram hashtags by keyword and get the matching tags with their IDs, tag page links, and the number of posts using each one.

- **Request:** `POST https://api.socq.ai/v1/instagram/search-hashtags`
- **publicId:** `instagram/search-hashtags`
- **Price:** 0.5 credits ($0.0025) per result
- **Launched:** 2026-11-09
- **Example body:** [`payloads/search-hashtags.json`](payloads/search-hashtags.json)

Search Instagram hashtags by keyword and get the matching hashtag names, IDs and post counts. Submit an asynchronous task, then read its standard results.

Provide one keyword in query; a leading # is optional. results_limit sets how many hashtags to return (default 50, up to 100).

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `query` | string | Yes | Keyword to match against hashtag names, with or without a leading #. (length 1 to 100) |
| `results_limit` | integer | No | (value 1 to 100; default `50`) |

```bash
curl -X POST "https://api.socq.ai/v1/instagram/search-hashtags" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "query": "travel",
  "results_limit": 50
}'
```

Full docs: [https://docs.socq.ai/api-manual/instagram/search-hashtags](https://docs.socq.ai/api-manual/instagram/search-hashtags) · Landing page: [socq.ai/apis/instagram/search-hashtags](https://socq.ai/apis/instagram/search-hashtags?utm_source=github&utm_medium=readme&utm_campaign=socq-instagram-api)

## Repository contents

| Path | Purpose |
| --- | --- |
| [`examples/curl/socq.sh`](examples/curl/socq.sh) | Submit, poll and paginate with cURL and jq |
| [`examples/node/socq.mjs`](examples/node/socq.mjs) | Same workflow in Node.js 20+ (no dependencies) |
| [`examples/python/socq.py`](examples/python/socq.py) | Same workflow in Python 3.8+ (standard library) |
| [`payloads/`](payloads) | One documented request body per endpoint |
| [`endpoints.json`](endpoints.json) | Endpoint list, prices and request schemas used by the scripts and checks |
| [`fixtures/`](fixtures) | Synthetic submit and task response shapes |
| [`docs/production-notes.md`](docs/production-notes.md) | Retries, timeouts, pagination and data handling |
| [`scripts/check.mjs`](scripts/check.mjs) | Offline check: payloads, syntax and secrets |

## Responsible use and platform scope

- Use only publicly accessible Instagram data and the fields supported by each endpoint.
- Do not use the examples to access restricted content, login-only surfaces, authentication controls or non-public personal information.
- SocQ is not an official API of the represented platform and is not affiliated with or endorsed by it. Platform names and trademarks belong to their respective owners.
- Before production use, assess the laws, platform terms, privacy obligations and retention requirements that apply to your organization and use case.
- Collect only the fields needed for a defined purpose, restrict access, set retention periods, and support correction or deletion workflows where required.

This section describes the public-data boundary; it is not legal advice.

## License

[MIT](LICENSE)
