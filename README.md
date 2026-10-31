# Salesforce Marketing Cloud

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Salesforce Marketing Cloud Engagement is an enterprise digital marketing platform for customer journeys, email marketing, mobile messaging (SMS/MMS and push), advertising, content management and marketing data. Its API surface is tenant-scoped: every REST call goes to https://{subdomain}.rest.marketingcloudapis.com and every SOAP call to https://{subdomain}.soap.marketingcloudapis.com, with OAuth 2.0 tokens issued per tenant from https://{subdomain}.auth.marketingcloudapis.com/v2/token and scopes granted to an Installed Package rather than requested at authorization time. Product areas are versioned independently at v1 behind route prefixes (/asset, /contacts, /interaction, /data, /messaging, /push, /sms, /automation, /hub, /platform). Salesforce also operates a first-party hosted MCP server for Marketing Cloud Engagement, generally available since June 2026, exposing 142 tools across eleven product areas, and an outbound webhook product, the Event Notification Service, with HMAC-SHA256 signed callbacks.

**Areas:** Automation · Content Management · Customer Journey · Digital Marketing · Email · Marketing · Marketing Automation · MCP · Mobile Messaging · Personalization · SMS · Webhook

## Salesforce Marketing Cloud on APIs.io

Everything profiled for Salesforce Marketing Cloud is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/salesforce-marketing-cloud/](https://apis.io/providers/salesforce-marketing-cloud/)** — or go straight to one of the APIs or properties below.

### APIs (17)

- [SOAP API](https://apis.io/apis/salesforce-marketing-cloud/soap-api/) — Legacy SOAP-based API for Marketing Cloud operations, including email sends, subscriber management, and data extension operations.
- [Transactional Messaging API](https://apis.io/apis/salesforce-marketing-cloud/transactional-messaging-api/) — Specialized API for sending triggered, transactional messages including order confirmations, password resets, and real-time notifications.
- [Journey Builder API](https://apis.io/apis/salesforce-marketing-cloud/journey-builder-api/) — API for creating, managing, and automating customer journeys across multiple channels and touchpoints.
- [Data Extensions API](https://apis.io/apis/salesforce-marketing-cloud/data-extensions-api/) — API for managing data extensions, which are database tables used to store and segment customer data in Marketing Cloud.
- [Email Send Definition API](https://apis.io/apis/salesforce-marketing-cloud/email-send-definition-api/) — API for creating and managing email send definitions, which define the configuration for sending emails to subscribers.
- [Mobile Push API](https://apis.io/apis/salesforce-marketing-cloud/mobile-push-api/) — API for sending push notifications to mobile devices, managing device registrations, and tracking push message engagement.
- [SMS/MMS API](https://apis.io/apis/salesforce-marketing-cloud/sms-mms-api/) — API for sending SMS and MMS messages, managing mobile numbers, and handling keyword-based subscriptions.
- [Asset API](https://apis.io/apis/salesforce-marketing-cloud/asset-api/) — API for managing marketing assets including images, documents, content blocks, and templates across Marketing Cloud.
- [Einstein Recommendations API](https://apis.io/apis/salesforce-marketing-cloud/einstein-recommendations-api/) — API for leveraging AI-powered product and content recommendations to personalize customer experiences.
- [Content Builder API](https://apis.io/apis/salesforce-marketing-cloud/content-builder-api/) — REST API for creating and manipulating marketing content in Content Builder, a single cross-channel repository for emails, images, text, content blocks, and…
- [Contacts API](https://apis.io/apis/salesforce-marketing-cloud/contacts-api/) — REST API for creating, reading, updating, and deleting contacts in Marketing Cloud.
- [Automation Studio API](https://apis.io/apis/salesforce-marketing-cloud/automation-studio-api/) — API for initiating and managing marketing automations, including file upload, download, decryption, compression, and decompression operations within…
- [Campaign API](https://apis.io/apis/salesforce-marketing-cloud/campaign-api/) — API for managing and performing marketing campaigns within Marketing Cloud.
- [Event Notification Service API](https://apis.io/apis/salesforce-marketing-cloud/event-notification-service-api/) — API for registering callbacks and subscriptions to receive real-time event notifications from Marketing Cloud.
- [Salesforce Marketing Cloud Assets API](https://apis.io/apis/salesforce-marketing-cloud/salesforce-marketing-cloud-assets-api/) — Manage marketing assets including images, documents, content blocks, and templates. The Asset API provides CRUD operations for all content types stored in…
- [Salesforce Marketing Cloud Contacts API](https://apis.io/apis/salesforce-marketing-cloud/salesforce-marketing-cloud-contacts-api/) — Create, retrieve, update, and delete contacts in Marketing Cloud. Contacts represent individuals who interact with your marketing campaigns across channels.
- [Salesforce Marketing Cloud Journeys API](https://apis.io/apis/salesforce-marketing-cloud/salesforce-marketing-cloud-journeys-api/) — Create, manage, and automate customer journeys across multiple channels and touchpoints. Journeys define the automated workflows that guide customers…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Salesforce Marketing Cloud Webhooks](https://apis.io/asyncapis/salesforce-marketing-cloud/salesforce-marketing-cloud-webhooks/)

#### GraphQL (1)

GraphQL schemas.

- [Moved to /providers/salesforce-marketing-cloud/](https://apis.io/graphqls/salesforce-marketing-cloud/salesforce-marketing-cloud-graphql/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [MCP Server for Marketing Cloud Engagement](https://apis.io/servers/salesforce-marketing-cloud/mcp-server-for-marketing-cloud-engagement/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Salesforce Marketing Cloud Agentic Access](https://apis.io/agentic-access/salesforce-marketing-cloud/salesforce-marketing-cloud-agentic-access/)

#### JSON Schema (51)

The data models the API reads and writes.

- [Asset](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-asset/)
- [AssetCollection](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-asset-collection/)
- [AssetDefinition](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-asset-definition/)
- [AssetQuery](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-asset-query/)
- [AssetType](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-asset-type/)
- [AssetCollection](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-assetcollection/)
- [AssetDefinition](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-assetdefinition/)
- [AssetQuery](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-assetquery/)
- [AssetType](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-assettype/)
- [AttributeSet](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-attribute-set/)
- [AttributeSetsResponse](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-attribute-sets-response/)
- [AttributeValue](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-attribute-value/)
- [AttributeSet](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-attributeset/)
- [AttributeSetsResponse](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-attributesetsresponse/)
- [AttributeValue](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-attributevalue/)
- [CategoryCollection](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-category-collection/)
- [CategoryCollection](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-categorycollection/)
- [Contact](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-contact/)
- [ContactResponse](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-contact-response/)
- [ContactSearchRequest](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-contact-search-request/)
- [ContactSearchResponse](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-contact-search-response/)
- [ContactResponse](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-contactresponse/)
- [ContactSearchRequest](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-contactsearchrequest/)
- [ContactSearchResponse](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-contactsearchresponse/)
- [CreateContactsRequest](https://apis.io/schemas/salesforce-marketing-cloud/salesforce-marketing-cloud-create-contacts-request/)
- …and 26 more published on APIs.io

#### JSON Structure (28)

Data models expressed in JSON Structure.

- [Salesforce Marketing Cloud Asset Collection Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-asset-collection-structure/)
- [Salesforce Marketing Cloud Asset Definition Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-asset-definition-structure/)
- [Salesforce Marketing Cloud Asset Query Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-asset-query-structure/)
- [Salesforce Marketing Cloud Asset Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-asset-structure/)
- [Salesforce Marketing Cloud Asset Type Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-asset-type-structure/)
- [Salesforce Marketing Cloud Attribute Set Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-attribute-set-structure/)
- [Salesforce Marketing Cloud Attribute Sets Response Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-attribute-sets-response-structure/)
- [Salesforce Marketing Cloud Attribute Value Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-attribute-value-structure/)
- [Salesforce Marketing Cloud Category Collection Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-category-collection-structure/)
- [Salesforce Marketing Cloud Contact Response Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-contact-response-structure/)
- [Salesforce Marketing Cloud Contact Search Request Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-contact-search-request-structure/)
- [Salesforce Marketing Cloud Contact Search Response Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-contact-search-response-structure/)
- [Salesforce Marketing Cloud Contact Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-contact-structure/)
- [Salesforce Marketing Cloud Create Contacts Request Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-create-contacts-request-structure/)
- [Salesforce Marketing Cloud Delete Contact Response Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-delete-contact-response-structure/)
- [Salesforce Marketing Cloud Entry Event Response Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-entry-event-response-structure/)
- [Salesforce Marketing Cloud Entry Event Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-entry-event-structure/)
- [Salesforce Marketing Cloud Error Response Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-error-response-structure/)
- [Salesforce Marketing Cloud Journey Activity Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-journey-activity-structure/)
- [Salesforce Marketing Cloud Journey Collection Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-journey-collection-structure/)
- [Salesforce Marketing Cloud Journey Definition Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-journey-definition-structure/)
- [Salesforce Marketing Cloud Journey Exit Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-journey-exit-structure/)
- [Salesforce Marketing Cloud Journey Goal Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-journey-goal-structure/)
- [Salesforce Marketing Cloud Journey Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-journey-structure/)
- [Salesforce Marketing Cloud Journey Trigger Structure](https://apis.io/json-structure/salesforce-marketing-cloud/salesforce-marketing-cloud-journey-trigger-structure/)
- …and 3 more published on APIs.io

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Salesforce Marketing Cloud Context](https://apis.io/jsonld/salesforce-marketing-cloud/salesforce-marketing-cloud-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Salesforce Marketing Cloud Domain Vocabulary](https://apis.io/vocabularies/salesforce-marketing-cloud/salesforce-marketing-cloud-vocabulary/)

#### Examples (33)

Example requests and responses.

- [Salesforce Marketing Cloud Asset Collection Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-asset-collection-example/)
- [Salesforce Marketing Cloud Asset Definition Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-asset-definition-example/)
- [Salesforce Marketing Cloud Asset Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-asset-example/)
- [Salesforce Marketing Cloud Asset Query Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-asset-query-example/)
- [Salesforce Marketing Cloud Asset Type Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-asset-type-example/)
- [Salesforce Marketing Cloud Attribute Set Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-attribute-set-example/)
- [Salesforce Marketing Cloud Attribute Sets Response Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-attribute-sets-response-example/)
- [Salesforce Marketing Cloud Attribute Value Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-attribute-value-example/)
- [Salesforce Marketing Cloud Category Collection Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-category-collection-example/)
- [Salesforce Marketing Cloud Contact Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-contact-example/)
- [Salesforce Marketing Cloud Contact Response Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-contact-response-example/)
- [Salesforce Marketing Cloud Contact Search Request Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-contact-search-request-example/)
- [Salesforce Marketing Cloud Contact Search Response Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-contact-search-response-example/)
- [Salesforce Marketing Cloud Create Contacts Request Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-create-contacts-request-example/)
- [Salesforce Marketing Cloud Createasset Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-createasset-example/)
- [Salesforce Marketing Cloud Createcontacts Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-createcontacts-example/)
- [Salesforce Marketing Cloud Createjourney Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-createjourney-example/)
- [Salesforce Marketing Cloud Delete Contact Response Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-delete-contact-response-example/)
- [Salesforce Marketing Cloud Entry Event Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-entry-event-example/)
- [Salesforce Marketing Cloud Entry Event Response Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-entry-event-response-example/)
- [Salesforce Marketing Cloud Error Response Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-error-response-example/)
- [Salesforce Marketing Cloud Fireentryevent Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-fireentryevent-example/)
- [Salesforce Marketing Cloud Journey Activity Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-journey-activity-example/)
- [Salesforce Marketing Cloud Journey Collection Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-journey-collection-example/)
- [Salesforce Marketing Cloud Journey Definition Example](https://apis.io/examples/salesforce-marketing-cloud/salesforce-marketing-cloud-journey-definition-example/)
- …and 8 more published on APIs.io

#### Collections (7)

Postman and Open Collection request collections.

- [Salesforce Marketing Cloud REST API](https://apis.io/collections/salesforce-marketing-cloud/open-salesforce-marketing-cloud/)
- [Salesforce Marketing Cloud REST Assets API](https://apis.io/collections/salesforce-marketing-cloud/open-salesforce-marketing-cloud-assets-api/)
- [Salesforce Marketing Cloud REST Assets Contacts API](https://apis.io/collections/salesforce-marketing-cloud/open-salesforce-marketing-cloud-contacts-api/)
- [Salesforce Marketing Cloud REST Assets Journeys API](https://apis.io/collections/salesforce-marketing-cloud/open-salesforce-marketing-cloud-journeys-api/)
- [Salesforce Marketing Cloud REST Assets API](https://apis.io/collections/salesforce-marketing-cloud/postman-salesforce-marketing-cloud-assets-api/)
- [Salesforce Marketing Cloud REST Assets Contacts API](https://apis.io/collections/salesforce-marketing-cloud/postman-salesforce-marketing-cloud-contacts-api/)
- [Salesforce Marketing Cloud REST Assets Journeys API](https://apis.io/collections/salesforce-marketing-cloud/postman-salesforce-marketing-cloud-journeys-api/)

#### Overlays (6)

OpenAPI overlays, including conversational phrasing for each operation.

- [Salesforce Marketing Cloud Assets Api Overlay](https://apis.io/overlays/salesforce-marketing-cloud/salesforce-marketing-cloud-assets-api-overlay/)
- [Salesforce Marketing Cloud Assets Api Phrasing Overlay](https://apis.io/overlays/salesforce-marketing-cloud/salesforce-marketing-cloud-assets-api-phrasing-overlay/)
- [Salesforce Marketing Cloud Contacts Api Overlay](https://apis.io/overlays/salesforce-marketing-cloud/salesforce-marketing-cloud-contacts-api-overlay/)
- [Salesforce Marketing Cloud Contacts Api Phrasing Overlay](https://apis.io/overlays/salesforce-marketing-cloud/salesforce-marketing-cloud-contacts-api-phrasing-overlay/)
- [Salesforce Marketing Cloud Journeys Api Overlay](https://apis.io/overlays/salesforce-marketing-cloud/salesforce-marketing-cloud-journeys-api-overlay/)
- [Salesforce Marketing Cloud Journeys Api Phrasing Overlay](https://apis.io/overlays/salesforce-marketing-cloud/salesforce-marketing-cloud-journeys-api-phrasing-overlay/)

#### Governance rules (3)

Spectral rulesets for the provider's contracts.

- [Salesforce Marketing Cloud — jsonschema rules](https://apis.io/rules/salesforce-marketing-cloud/salesforce-marketing-cloud-jsonschema-spectral-rules/)
- [Salesforce Marketing Cloud API Rules](https://apis.io/rules/salesforce-marketing-cloud/salesforce-marketing-cloud-rules/)
- [Salesforce Marketing Cloud API Rules](https://apis.io/rules/salesforce-marketing-cloud/salesforce-marketing-cloud-spectral-rules/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Salesforce Marketing Cloud Authentication](https://apis.io/security/salesforce-marketing-cloud/salesforce-marketing-cloud-authentication/)
- [Salesforce Marketing Cloud Domain Security](https://apis.io/security/salesforce-marketing-cloud/salesforce-marketing-cloud-domain-security/)
- [Salesforce Marketing Cloud Trust Center](https://apis.io/security/salesforce-marketing-cloud/salesforce-marketing-cloud-trust-center/)
- [Salesforce Marketing Cloud Vulnerability Disclosure](https://apis.io/security/salesforce-marketing-cloud/salesforce-marketing-cloud-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Salesforce Marketing Cloud Scopes](https://apis.io/scopes/salesforce-marketing-cloud/salesforce-marketing-cloud-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Salesforce Marketing Cloud Plans Pricing](https://apis.io/plans/salesforce-marketing-cloud/salesforce-marketing-cloud-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Salesforce Marketing Cloud Rate Limits](https://apis.io/rate-limits/salesforce-marketing-cloud/salesforce-marketing-cloud-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Salesforce Marketing Cloud Finops](https://apis.io/finops/salesforce-marketing-cloud/salesforce-marketing-cloud-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.salesforce.com/)
- [Documentation](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/apis-overview.html)
- [Getting started](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/get-started-index.html)
- [API reference](https://developer.salesforce.com/docs/marketing/marketing-cloud/references)
- [Pricing](https://www.salesforce.com/products/marketing-cloud/pricing/)
- [Sign up](https://www.salesforce.com/form/signup/freetrial-marketing-cloud/)
- [Support](https://help.salesforce.com/s/)
- [Changelog](https://help.salesforce.com/s/articleView?id=sf.mc_rn_release_notes.htm&type=5)
- [Blog](https://developer.salesforce.com/blogs/feed)
- [Security](https://www.salesforce.com/company/disclosure/)
- [Compliance](https://compliance.salesforce.com/)
- [Trust centre](https://trust.salesforce.com/)
- [Terms of service](https://www.salesforce.com/company/legal/)
- [Privacy policy](https://www.salesforce.com/company/legal/privacy/)
- [GitHub](https://github.com/salesforce-marketingcloud)
- [Status](https://status.salesforce.com/)

## API Evangelist rating

**Kin Score 79.1** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 75.0 |
| Contract quality | 74.3 |
| Contract governance | 45.5 |
| Operational transparency | 84.2 |
| Developer ergonomics | 76.8 |
| Access clarity | 92.1 |

**Agent readiness 56.8** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | templated |
| Auth Clarity | served (partial credit) |
| Idempotency | documented (partial credit) |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 44.2** — Telecommunications

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/salesforce-marketing-cloud/](https://apis.io/providers/salesforce-marketing-cloud/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Salesforce Marketing Cloud: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/salesforce-marketing-cloud/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
