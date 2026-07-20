Week 7 — Issue selection

Issue Number : #86

Issue title: Add an API rate limiting header (X-RateLimit-Remaining) to responses

Issue link: https://github.com/ascherj/pathreview/issues/86

Tier: 2

Branch: feat/86-rate-limit-headers

Problem summary:

The API currently enforces request limits, but clients have no way to know how many requests they have remaining before reaching the limit. Instead, they only find out after receiving a 429 Too Many Requests response. The existing rate limiter already calculates the remaining number of requests, but that information is not exposed in API responses. A successful fix will add the standard X-RateLimit-Limit and X-RateLimit-Remaining headers so clients can monitor their usage before exceeding the limit.

Why I Chose This Issue

I selected this issue because it has a clearly defined objective and focuses on improving an existing feature rather than building a completely new one. The issue description identifies the relevant parts of the codebase, giving me a good starting point while allowing me to learn more about how middleware and request handling work in a FastAPI application. Since the required behavior is well documented, I felt this would be a manageable issue that would help me better understand the project's architecture.