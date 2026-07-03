# The Korea Hub

English-language guides and data-driven stories on Korean local businesses, neighborhoods, and city life.

- **Stack**: Hugo + GitHub Pages (Actions deploy). No heavy JS, semantic HTML (GEO-first).
- **Publishing**: content under `content/posts/` is written exclusively by the
  [Syndicator](https://github.com/This-HW/syndicator) pipeline (single-writer invariant —
  see `PUBLISHING_CONTRACT.md` §6 in the syndicator repo).
- **Registry**: `data/publish_registry.json` maps `content_id ↔ canonical URL` for published posts.
- **JSON-LD**: `layouts/partials/jsonld.html` renders exactly one schema object per page,
  branched on front matter `media_type` (`article`→BlogPosting, `news`→NewsArticle,
  `local_business`→LocalBusiness).

Manual edits to `content/posts/` are not allowed; site chrome (layouts/css) is maintained here.
