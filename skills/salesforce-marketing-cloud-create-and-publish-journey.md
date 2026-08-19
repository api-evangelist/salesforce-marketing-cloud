---
name: Create and publish a Marketing Cloud journey
description: >-
  Create a Journey Builder journey, publish it asynchronously, and poll for the result,
  against Salesforce Marketing Cloud Engagement's tenant-scoped REST API.
api: openapi/salesforce-marketing-cloud-journeys-api-openapi.yml
operations: [createJourney, getJourney, publishJourney, listJourneys]
generated: '2026-08-13'
method: generated
---

# Create and publish a Marketing Cloud journey

## Before you start

- Resolve the tenant subdomain. Every host is `https://{subdomain}.rest.marketingcloudapis.com`.
  There is no shared host. The subdomain comes from the customer's Marketing Cloud
  Setup > Apps > Installed Packages. If you do not have it, stop and ask — do not guess.
- Get a token from `https://{subdomain}.auth.marketingcloudapis.com/v2/token` using the
  Installed Package's client credentials. Send it as `Authorization: Bearer <token>`.
  Cache it until expiry; requesting a token per call counts against account API activity.
- Scopes are fixed on the Installed Package by an administrator, not requested at
  authorization time. A `403` with an `errorcode` in the 20000 class means the package is
  missing a scope and only an admin can fix it. Do not retry.

## Steps

1. **Check what already exists.** Call `listJourneys`
   (`GET /interaction/v1/interactions`). Use `$page`, `$pageSize`, `$orderBy` and the
   `status` / `nameOrDescription` filters. The response envelope is
   `{count, page, pageSize, items}` — page until `page * pageSize >= count`.

2. **Create the journey.** Call `createJourney`
   (`POST /interaction/v1/interactions`) with a `JourneyDefinition` body: `key`, `name`,
   `description`, `workflowApiVersion`, and the `triggers`, `activities`, `goals` and `exits`
   arrays. Set `key` yourself — it is the customer-defined external key and the only stable
   handle across business units. A `201` returns the `Journey` including its `id` and
   `version`.
   **This operation is not idempotent.** Marketing Cloud Engagement has no
   `Idempotency-Key` header. If the call times out, do NOT blind-retry — call `listJourneys`
   filtered on your `key` first and only create if it is absent.

3. **Publish it.** Call `publishJourney`
   (`POST /interaction/v1/interactions/publishAsync/{id}`). This returns **202** with a
   `PublishResponse` carrying a `statusId`. **202 is not success** — the journey is queued,
   not live.

4. **Poll for the outcome.** Re-read the journey with `getJourney`
   (`GET /interaction/v1/interactions/{id}`, optional `versionNumber` query parameter) and
   check `status`. Back off between polls.

## Rules

- **Published versions are immutable.** `updateJourney`, `deleteJourney` and `stopJourney`
  all declare `409` for exactly this reason. On a `409`, do not retry the same call — either
  create a new version or stop the running journey first, and say which you are doing.
- **`stopJourney` is irreversible.** Salesforce describes the equivalent MCP tool as
  "Permanently stop a running journey." Treat it as a destructive, confirm-first action.
- **Branch on `errorcode`, not the HTTP status.** The envelope is
  `{message, errorcode, documentation}`. Two different `429`s exist: `50100` ("Rate limit
  exceeded") is retryable after the advertised `Retry-After`; `50200` ("Your requests are
  temporarily blocked.") is an account-level throttle that retrying will not clear.
- Honour `Retry-After` on every `429`. Salesforce publishes no numeric quota, so you cannot
  precompute a safe rate — you must react to the signal.

## References

- Conventions: `conventions/salesforce-marketing-cloud-conventions.yml`
- Errors: `errors/salesforce-marketing-cloud-problem-types.yml`
- Data model: `data-model/salesforce-marketing-cloud-data-model.yml`
