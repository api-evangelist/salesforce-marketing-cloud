---
name: Manage Content Builder assets
description: >-
  Find, create, update and delete Content Builder assets (emails, templates, images, content
  blocks) through the Marketing Cloud Engagement Assets API.
api: openapi/salesforce-marketing-cloud-assets-api-openapi.yml
operations: [listAssets, queryAssets, getAsset, createAsset, updateAsset, deleteAsset, listCategories]
generated: '2026-08-13'
method: generated
---

# Manage Content Builder assets

## Before you start

- Host `https://{subdomain}.rest.marketingcloudapis.com`, route prefix `/asset/v1`.
  OAuth bearer token from `https://{subdomain}.auth.marketingcloudapis.com/v2/token`.
- **One operation creates every content type.** `createAsset` makes an HTML email, a
  template, an image or a content block — the numeric `assetType.id` is the only
  discriminator. Resolve the correct asset type before writing anything; do not guess the id.

## Steps

1. **Find the folder.** Call `listCategories`
   (`GET /asset/v1/content/categories`) with `$page`, `$pageSize`, `$filter`. Categories are
   Content Builder folders; `Asset.category` points at one.

2. **Search existing assets.** Two paths, and they are not equivalent:
   - `listAssets` (`GET /asset/v1/content/assets`) with `$page`, `$pageSize`, `$orderBy`,
     `$filter` — simple string filtering.
   - `queryAssets` (`POST /asset/v1/content/assets/query`) with an `AssetQuery` body
     (`page`, `query`, `sort`, `fields`) — compound conditions the `$filter` string cannot
     express. Use this for anything beyond a single predicate.

   The `$`-prefixed parameter names are OData-flavoured but this is **not** OData; do not send
   OData operators the docs do not list.

3. **Read one asset.** `getAsset` (`GET /asset/v1/content/assets/{id}`). Note `{id}` is the
   **integer** system id, not `customerKey`. If you only hold a `customerKey`, resolve it via
   `listAssets`/`queryAssets` first.

4. **Create.** `createAsset` (`POST /asset/v1/content/assets`) with an `AssetDefinition`:
   `name`, `assetType`, `content`/`views`/`data`, `category`, and — always — `customerKey`.
   `customerKey` is the customer-defined external key and the only handle that is stable
   across business units and environments. Setting it yourself also makes your create
   re-runnable, which matters because this API has **no idempotency header**: a retried
   `createAsset` after a timeout will produce a duplicate asset. Check with `queryAssets` on
   your `customerKey` before retrying.
   Success is `201` returning the full `Asset` with its assigned integer `id`.

5. **Update.** `updateAsset` (`PUT /asset/v1/content/assets/{id}`) with an `AssetDefinition`.
   This is a PUT — send the complete definition, not a partial patch.

6. **Delete.** `deleteAsset` (`DELETE /asset/v1/content/assets/{id}`) returns `200` with no
   body.
   Worth knowing when an agent is choosing a surface: **the Marketing Cloud MCP server has no
   asset-delete tool.** It can create and update assets and delete folders, but asset removal
   exists only on REST. See `mcp/salesforce-marketing-cloud-tool-crosswalk.yml`.

## Rules

- `400` is a validation error (`errorcode` 10000–10005) — fix the payload, do not retry.
- `404` on `getAsset`/`updateAsset`/`deleteAsset` means the integer id is wrong, most often
  because a `customerKey` was passed where an `id` belongs.
- `429`: honour `Retry-After`. `errorcode` `50100` retryable, `50200` not.
- Never send `Content-Type` other than `application/json` — `415` is documented.

## References

- Conventions: `conventions/salesforce-marketing-cloud-conventions.yml`
- Errors: `errors/salesforce-marketing-cloud-problem-types.yml`
- Tool crosswalk: `mcp/salesforce-marketing-cloud-tool-crosswalk.yml`
