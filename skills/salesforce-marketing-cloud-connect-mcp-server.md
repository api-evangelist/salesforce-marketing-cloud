---
name: Connect to the Marketing Cloud Engagement MCP server
description: >-
  Connect an MCP client to Salesforce's first-party hosted MCP server for Marketing Cloud
  Engagement, and understand what its 142 tools can and cannot reach.
api: mcp/salesforce-marketing-cloud-mcp.yml
operations: [sfmc_get_journeys, sfmc_get_data_extensions, sfmc_get_content_assets, sfmc_send_transactional_email, sfmc_stop_journey]
generated: '2026-08-13'
method: generated
---

# Connect to the Marketing Cloud Engagement MCP server

Salesforce operates a **remote hosted** MCP server for Marketing Cloud Engagement, GA since
2026-06-02. There is nothing to install — an MCP client POSTs to a URL.

## Endpoint

The path is templated per tenant:

- US: `https://mai-mce-mcp-cdp1.sfdc-yfeipo.svc.sfdcfc.net/t/{tenantID}/c/{clientID}/api/mcp`
- EU: `https://mai-mce-mcp-cdp1.sfdc-yzvdd4.svc.sfdcfc.net/t/{tenantID}/c/{clientID}/api/mcp`

`{tenantID}` and `{clientID}` come from an Installed Package created in Marketing Cloud
Engagement Setup. **Both are required** — POSTing to the un-tenanted `/api/mcp` root returns
HTTP 405. If you do not have them, stop and ask a Marketing Cloud administrator; there is
nothing to guess.

Salesforce's published registration line for Claude Code:

```
claude mcp add -s user --transport http CONFIG_NAME https://mai-mce-mcp-cdp1.sfdc-yfeipo.svc.sfdcfc.net/t/{tenantID}/c/{clientID}/api/mcp
```

## Authorization

OAuth 2.0 authorization code with PKCE. The server publishes RFC 8414 and RFC 9728 metadata
at its root (both saved in `well-known/`):

- issuer `https://mai-mce-mcp-cdp1.sfdc-yfeipo.svc.sfdcfc.net/api/mcp`
- authorization `.../authorize`, token `.../token`, dynamic registration `.../register`
- `code_challenge_methods_supported: [S256]`, grants `authorization_code` + `refresh_token`

Salesforce is explicit about the permission model: *"An agent's permissions are a combination
of the scopes in a dedicated, installed package and your own user permissions."* Review the
Installed Package scopes **before** connecting an agent — the tool set includes destructive
operations.

## What the tools cover

142 tools, all prefixed `sfmc_`, across 11 categories: Automations (35), Journeys (36), Data
Extensions (19), Content (13), Contacts (11), Campaigns (8), SMS (8), Email (5), Utilities
(5), Push (1), Tracking (1).

Reach for read tools first to orient: `sfmc_get_journeys`, `sfmc_get_data_extensions`,
`sfmc_get_content_assets`, `sfmc_get_automations`, `sfmc_describe_object`.

## Rules

- **Confirm before every destructive tool.** `sfmc_stop_journey` is documented as
  "Permanently stop a running journey." `sfmc_clear_data_extension_data`,
  `sfmc_delete_data_extension`, `sfmc_delete_contacts`, `sfmc_delete_journey` and
  `sfmc_delete_campaign` are all irreversible against production marketing data.
- **`sfmc_send_transactional_email`, `sfmc_send_outbound_sms_message` and
  `sfmc_send_push_notification` send real messages to real people.** There is no test mode:
  Marketing Cloud Engagement publishes no sandbox, no test key prefix and no magic test
  recipient. Never call a send tool speculatively.
- **The activity-construction tools hold state in the server, not in Marketing Cloud.**
  `sfmc_email_activity`, `sfmc_wait_activity`, `sfmc_decision_split_activity`,
  `sfmc_random_split_activity`, `sfmc_sms_activity`, `sfmc_einstein_sto_activity` and
  `sfmc_engagement_decision_activity` are all documented as "construct ... and hold it in
  memory". Nothing is persisted until you call a journey create/update tool. Do not report
  success after constructing an activity.
- **Asynchronous tools need polling.** `sfmc_publish_journey`,
  `sfmc_insert_contacts_into_journey_async`, `sfmc_bulk_upsert_data_extension_rows` and the
  `*_field_async` tools all return a handle; use the matching `*_status` /
  `sfmc_get_bulk_job_status` / `sfmc_get_bulk_job_results` tool before claiming completion.
- **Marketing Cloud API limits apply to MCP calls.** Salesforce states plainly: "Marketing
  Cloud API limits and guidelines apply." Expect `429` behaviour to propagate.

## Where MCP and REST diverge

They are not the same surface. `mcp/salesforce-marketing-cloud-tool-crosswalk.yml` records
the mapping: 26 tools bind to captured OpenAPI operationIds, 116 reach product areas with no
captured contract, and one REST operation (`deleteAsset`) has no MCP tool at all — an agent
on MCP alone cannot delete a Content Builder asset.

## References

- MCP manifest: `mcp/salesforce-marketing-cloud-mcp.yml`
- Tool crosswalk: `mcp/salesforce-marketing-cloud-tool-crosswalk.yml`
- OAuth metadata: `well-known/salesforce-marketing-cloud-oauth-authorization-server.json`
- Scopes: `scopes/salesforce-marketing-cloud-scopes.yml`
