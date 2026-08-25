[MINTLIFY-20260810-002] status: active | hits: 1 | promoted: no
Signature: Mintlify Index rate-limits repeated context queries
Note: A second focused query returned HTTP 429. Consolidate related questions into one context query, then use the cited official docs and local evidence if a follow-up query is rate-limited.

[MINTLIFY-20260821-003] status: active | hits: 1 | promoted: no
Signature: Mintlify subpath root loops between slash variants
Note: Test both the proxied URL and the direct `.mintlify.site` upstream with and without a trailing slash. If the direct upstream loops too, treat it as a Mintlify deployment issue before you change the customer proxy.

[MINTLIFY-20260821-004] status: active | hits: 1 | promoted: no
Signature: Mintlify preview webhook does not create a deployment
Note: If a PR receives no preview after ready, synchronize, and reopen events, test the predicted preview host before waiting longer. Use the dashboard or Admin API instead of merging a diagnostic change into production.
