---
title: "RSS Web Scraper — Go-Based Backend Aggregation Service"
date: 2025-09-05
description: "A Go-based RSS aggregation backend with REST APIs, API key authentication, background scraping workers, and postgreSQL persistence."
isStarred: true
---

**RSS Web Scraper** is a **backend service built in Go** that aggregates RSS feeds, manages user subscriptions, and continuously scrapes content in the background.  
It exposes a **RESTful API** with **API key–based authentication**, enabling users to create accounts, add feeds, follow sources, and retrieve aggregated posts.

🔗 **GitHub:** https://github.com/AryanManojKumar/RSS-Web-Scraper

---

### Key Features

- **RESTful API Design**
  - Create users and issue API keys
  - Add RSS feed sources
  - Follow and unfollow feeds
  - Retrieve aggregated posts per user

- **Authentication**
  - API key–based authorization for all protected endpoints
  - User-scoped access to feeds and posts

- **Background Scraping Engine**
  - Concurrent feed scraping using Go routines
  - Configurable worker pool (default: 10 workers)
  - Scheduled scraping at fixed intervals (default: every 1 minute)
  - Duplicate detection to prevent repeated posts
  - Fault-tolerant execution (individual feed failures don’t stop the system)

- **Persistent Storage**
  - postgreSQL-backed data model
  - Normalized schema for users, feeds, subscriptions, and posts
  - Type-safe database access using SQLC
  - Versioned schema migrations with Goose

---

### API Capabilities (Example)

```bash
# Create a user
post /v1/users

# Add an RSS feed (authenticated)
post /v1/feed

# Follow a feed
post /v1/feed_follow

# Get user-specific posts
GET /v1/upost
---
```

### Architecture Overview
- HTTP Layer: REST API built with Go’s net/http
- Auth Layer: API key validation middleware
- Worker Layer: Concurrent background scraping jobs
- Data Layer: postgreSQL with SQLC-generated queries
- Migrations: Goose for schema versioning