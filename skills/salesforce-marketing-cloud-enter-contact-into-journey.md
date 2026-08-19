---
name: Enter a contact into a running journey
description: >-
  Resolve or create a contact in the Marketing Cloud contact model, then fire a Journey
  Builder entry event to put that contact into a published journey.
api: openapi/salesforce-marketing-cloud-contacts-api-openapi.yml
operations: [searchContacts, getContact, createContacts, listAttributeSets, fireEntryEvent]
generated: '2026-08-13'
method: generated
---

# Enter a contact into a running journey

This is the join between the contact model (`/contacts/v1`) and Journey Builder
(`/interaction/v1`). Both live on the same tenant host.

## Before you start

- Host: `https://{subdomain}.rest.marketingcloudapis.com`. Token from
  `https://{subdomain}.auth.marketingcloudapis.com/v2/token`, sent as `Authorization: Bearer`.
- The journey must already be **published** and must have an API entry event whose
  `eventDefinitionKey` you know. `fireEntryEvent` against an unpublished journey does nothing
  useful.

## Steps

1. **Understand the contact shape first.** Call `listAttributeSets`
   (`GET /contacts/v1/attributeSets`). Marketing Cloud has no fixed contact schema — a
   `Contact` carries an array of named `attributeSets`, each holding name/value items. You
   cannot construct a valid contact payload without reading the tenant's attribute sets.
   Note this response has `count` and `items` but **no `page`/`pageSize`** — it is
   unpaginated, unlike every other collection in this API.

2. **Look the contact up.** Call `searchContacts`
   (`POST /contacts/v1/contacts/actions/search`) with a `conditionSet` and the
   `returnAttributes` you need. There is no GET-based contact list operation — search is a
   POST. The response is `{count, page, pageSize, items}`.
   If you already hold a `contactKey`, use `getContact`
   (`GET /contacts/v1/contacts/{contactKey}`) instead.

3. **Create the contact only if absent.** Call `createContacts`
   (`POST /contacts/v1/contacts`) with `contactKey` plus `attributeSets`.
   `contactKey` is the customer-defined natural key; `contactID` is the system integer and is
   assigned by Marketing Cloud. **Always set `contactKey` yourself** so the operation is
   re-runnable — this API has no idempotency header, and a retried create without a stable
   key produces duplicate contacts.
   Note `createContacts` returns `200` with a `ContactResponse`
   (`operationStatus`, `requestServiceMessageID`, `responseDateTime`, `resultMessages`) — an
   operation envelope, not the created contact. Read `operationStatus` and `resultMessages`;
   a `200` alone does not mean the contact was written.
   `createContacts` is the one operation in the captured Contacts spec that declares `403`,
   so a missing Installed Package scope shows up here first.

4. **Fire the entry event.** Call `fireEntryEvent`
   (`POST /interaction/v1/events`) with `ContactKey`, `EventDefinitionKey` and `Data`.
   **Watch the casing** — this body is PascalCase while every other payload in this API is
   camelCase. It is the only place in the captured specs that does this, and it is a common
   silent failure.
   A `201` returns `EntryEventResponse` with `requestId` and `eventInstanceId`. The contact
   has been accepted for entry, not necessarily entered — entry is evaluated asynchronously
   against the journey's entry criteria and re-entry rules.

## Rules

- **Do not blind-retry step 3 or step 4.** Neither is idempotent. The only client-supplied
  dedup key Salesforce documents anywhere in Marketing Cloud Engagement is `messageKey` on
  Transactional Messaging sends, which does not apply here. Guard retries with a
  `searchContacts` / `getContact` read.
- `deleteContact` returns `operationInitiated: true` — contact deletion is queued, not
  immediate. Do not assert the contact is gone on the response.
- On `429`: honour `Retry-After`. `errorcode` `50100` is retryable, `50200` is not.

## References

- Conventions: `conventions/salesforce-marketing-cloud-conventions.yml`
- Errors: `errors/salesforce-marketing-cloud-problem-types.yml`
- Data model: `data-model/salesforce-marketing-cloud-data-model.yml`
