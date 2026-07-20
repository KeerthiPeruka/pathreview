Week 7 — Issue selection

Issue link: https://github.com/ascherj/pathreview/issues/86

Issue title: Add an API rate limiting header (X-RateLimit-Remaining) to responses

Tier: [ ] Tier 1 [x] Tier 2 [ ] Tier 3

Problem summary:

The API currently enforces request limits, but clients have no way to know how many requests they have remaining before reaching the limit. Instead, they only find out after receiving a 429 Too Many Requests response. The existing rate limiter already calculates the remaining number of requests, but that information is not exposed in API responses. A successful fix would add the standard X-RateLimit-Limit and X-RateLimit-Remaining headers so clients can monitor their usage before exceeding the limit.

I selected this Tier 2 issue because it is challenging enough to help me learn more about middleware and request handling without requiring me to design an entirely new system. I am still becoming familiar with the PathReview codebase, but the issue has a focused scope and identifies the relevant areas of the project. The existing rate limiter already calculates the values needed for the headers, so the main task is understanding how that information moves through the middleware and response flow. This makes the issue a good match for my current comfort level because it requires codebase exploration and testing while still building on functionality that already exists.

Branch name: feat/86-rate-limit-headers

Setup confirmation: [ ] App runs locally at localhost:5173

Cohort ledger: [x] Issue added to cohort ledger