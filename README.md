# Salesforce Marketing Cloud (salesforce-marketing-cloud)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Salesforce Marketing Cloud is a comprehensive digital marketing platform that enables businesses to manage customer journeys, email marketing, mobile messaging, social media marketing, advertising, and data analytics.

**APIs.json:** [https://www.salesforce.com/products/marketing-cloud/overview/](https://www.salesforce.com/products/marketing-cloud/overview/)

## Scope

- **Type:** Index

## Tags

- Automation
- Customer Journey
- Digital Marketing
- Email
- Marketing
- Personalization

## Timestamps

- **Created:** 2024-01-15
- **Modified:** 2026-05-19

## APIs

### Marketing Cloud REST API

Core REST API for interacting with Marketing Cloud features including email, SMS, push notifications, and data extensions. REST API uses JSON request and response bodies and resource endpoints to support multi-channel use.

- **Human URL:** [https://developer.salesforce.com/docs/marketing/marketing-cloud/overview](https://developer.salesforce.com/docs/marketing/marketing-cloud/overview)
- **Base URL:** `https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com`

#### Tags

- Email
- Push
- REST
- SMS

#### Properties

- [Documentation](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/rest-api-overview.html)
- [OpenAPI](openapi/salesforce-marketing-cloud-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/salesforce-marketing-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/salesforce-marketing-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Authentication](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/authentication.html)
- [API Reference](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/routes.html)
- [Getting Started](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/get-started-index.html)
- [Rate Limits](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/rate-limiting.html)
- [Best Practices](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/rate-limiting-best-practices.html)
- [Errors](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/rate-limiting-errors.html)

### SOAP API

Legacy SOAP-based API for Marketing Cloud operations, including email sends, subscriber management, and data extension operations.

- **Human URL:** [https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/web_service_guide.html](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/web_service_guide.html)
- **Base URL:** `https://YOUR_SUBDOMAIN.soap.marketingcloudapis.com`

#### Tags

- Legacy
- SOAP
- Subscriber

#### Properties

- [Documentation](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/web_service_guide.html)
- [API Reference](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/soap_web_service_objects.html)
- [Getting Started](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/getting_started_developers_and_the_exacttarget_api.html)
- [Best Practices](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/working_with_soap_web_service_api.html)
- [Postman Collection](collections/salesforce-marketing-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/salesforce-marketing-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Transactional Messaging API

Specialized API for sending triggered, transactional messages including order confirmations, password resets, and real-time notifications.

- **Human URL:** [https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/transactional-messaging-api.html](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/transactional-messaging-api.html)
- **Base URL:** `https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/messaging/v1`

#### Tags

- Messaging
- Transactional
- Triggered

#### Properties

- [Documentation](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/transactional-messaging-api.html)
- [Getting Started](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/getting-started-spec.html)
- [Best Practices](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/transactional-messaging-best-practices.html)
- [Postman Collection](collections/salesforce-marketing-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/salesforce-marketing-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Journey Builder API

API for creating, managing, and automating customer journeys across multiple channels and touchpoints.

- **Human URL:** [https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/journey-builder-api-overview.html](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/journey-builder-api-overview.html)
- **Base URL:** `https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/interaction/v1`

#### Tags

- Automation
- Journey
- Orchestration

#### Properties

- [Documentation](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/journey-builder-api-overview.html)
- [Getting Started](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/get-started-jb.html)
- [Postman Collection](collections/salesforce-marketing-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/salesforce-marketing-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Data Extensions API

API for managing data extensions, which are database tables used to store and segment customer data in Marketing Cloud.

- **Human URL:** [https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/data-extensions.html](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/data-extensions.html)
- **Base URL:** `https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/data/v1`

#### Tags

- Data
- Segmentation
- Storage

#### Properties

- [Documentation](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/working-with-data-extensions.html)
- [API Reference](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/data-extension-api.html)
- [Postman Collection](collections/salesforce-marketing-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/salesforce-marketing-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Email Send Definition API

API for creating and managing email send definitions, which define the configuration for sending emails to subscribers.

- **Human URL:** [https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/email-send-definition.html](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/email-send-definition.html)
- **Base URL:** `https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/messaging/v1`

#### Tags

- Campaigns
- Email
- Sending

#### Properties

- [Documentation](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/email-send-definition.html)
- [Code Examples](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/code-examples.html)
- [Postman Collection](collections/salesforce-marketing-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/salesforce-marketing-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Mobile Push API

API for sending push notifications to mobile devices, managing device registrations, and tracking push message engagement.

- **Human URL:** [https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/mobile-push.html](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/mobile-push.html)
- **Base URL:** `https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/push/v1`

#### Tags

- Mobile
- Notifications
- Push

#### Properties

- [Documentation](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/push-notifications.html)
- [SDK](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/mobile-sdk.html)
- [Postman Collection](collections/salesforce-marketing-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/salesforce-marketing-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SMS/MMS API

API for sending SMS and MMS messages, managing mobile numbers, and handling keyword-based subscriptions.

- **Human URL:** [https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/sms-api.html](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/sms-api.html)
- **Base URL:** `https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/sms/v1`

#### Tags

- MMS
- Mobile Messaging
- SMS

#### Properties

- [Documentation](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/sms-api.html)
- [Best Practices](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/sms-best-practices.html)
- [Postman Collection](collections/salesforce-marketing-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/salesforce-marketing-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Asset API

API for managing marketing assets including images, documents, content blocks, and templates across Marketing Cloud.

- **Human URL:** [https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/asset-api.html](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/asset-api.html)
- **Base URL:** `https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/asset/v1`

#### Tags

- Assets
- Content
- Templates

#### Properties

- [Documentation](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/asset-api.html)
- [Postman Collection](collections/salesforce-marketing-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/salesforce-marketing-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Einstein Recommendations API

API for leveraging AI-powered product and content recommendations to personalize customer experiences.

- **Human URL:** [https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/einstein-recommendations.html](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/einstein-recommendations.html)
- **Base URL:** `https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/einstein/v1`

#### Tags

- AI
- Personalization
- Recommendations

#### Properties

- [Documentation](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/einstein-recommendations.html)
- [Postman Collection](collections/salesforce-marketing-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/salesforce-marketing-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Content Builder API

REST API for creating and manipulating marketing content in Content Builder, a single cross-channel repository for emails, images, text, content blocks, and other documents.

- **Human URL:** [https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/content-api.html](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/content-api.html)
- **Base URL:** `https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/asset/v1`

#### Tags

- Assets
- Content
- Email
- Templates

#### Properties

- [Documentation](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/content-api.html)
- [Postman Collection](collections/salesforce-marketing-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/salesforce-marketing-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Contacts API

REST API for creating, reading, updating, and deleting contacts in Marketing Cloud.

- **Human URL:** [https://developer.salesforce.com/docs/marketing/marketing-cloud/references/mc_rest_contacts/createContacts.html](https://developer.salesforce.com/docs/marketing/marketing-cloud/references/mc_rest_contacts/createContacts.html)
- **Base URL:** `https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/contacts/v1`

#### Tags

- Contacts
- Data
- Subscribers

#### Properties

- [Documentation](https://developer.salesforce.com/docs/marketing/marketing-cloud/references/mc_rest_contacts/createContacts.html)
- [Postman Collection](collections/salesforce-marketing-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/salesforce-marketing-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Automation Studio API

API for initiating and managing marketing automations, including file upload, download, decryption, compression, and decompression operations within Automation Studio.

- **Human URL:** [https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/automation-studio-api.html](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/automation-studio-api.html)
- **Base URL:** `https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/automation/v1`

#### Tags

- Automation
- Scheduling
- Workflows

#### Properties

- [Documentation](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/automation-studio-api.html)
- [Postman Collection](collections/salesforce-marketing-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/salesforce-marketing-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Campaign API

API for managing and performing marketing campaigns within Marketing Cloud.

- **Human URL:** [https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/campaign.html](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/campaign.html)
- **Base URL:** `https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/hub/v1`

#### Tags

- Campaigns
- Execution
- Marketing

#### Properties

- [Documentation](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/campaign.html)
- [Postman Collection](collections/salesforce-marketing-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/salesforce-marketing-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Event Notification Service API

API for registering callbacks and subscriptions to receive real-time event notifications from Marketing Cloud.

- **Human URL:** [https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/ens.html](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/ens.html)
- **Base URL:** `https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/platform/v1`

#### Tags

- Events
- Notifications
- Real-Time
- Webhooks

#### Properties

- [Documentation](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/ens.html)
- [Getting Started](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/ens-get-started.html)
- [Postman Collection](collections/salesforce-marketing-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/salesforce-marketing-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/showcase/salesforce-marketing-cloud-)
- [Developer Portal](https://developer.salesforce.com/docs/marketing/marketing-cloud/overview)
- [Documentation](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/apis-overview.html)
- [Authentication](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/authentication.html)
- [API Reference](https://developer.salesforce.com/docs/marketing/marketing-cloud/references)
- [Support](https://help.salesforce.com/s/)
- [Status Page](https://status.salesforce.com/)
- [SDK](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/sdks.html)
- [Terms of Service](https://www.salesforce.com/company/legal/)
- [Pricing](https://www.salesforce.com/products/marketing-cloud/pricing/)
- [Changelog](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/release-notes.html)
- [Rate Limits](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/rate-limiting.html)
- [GitHub Repository](https://github.com/salesforce-marketingcloud/SFDC-MC-REST-Style-Guide)
- [Training](https://trailhead.salesforce.com/en/content/learn/trails/get-started-with-marketing-cloud)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)

## Maintainers

**Email:** kin@apievangelist.com
**URL:** https://apievangelist.com
