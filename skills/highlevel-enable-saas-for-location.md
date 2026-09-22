---
name: highlevel-enable-saas-for-location
description: Enable SaaS for a specific location and verify its subscription details.
api: openapi/saas-api.json
operations:
- locations
- enable-saas-location
- get-location-subscription
generated: '2026-09-22'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/saas-api.json ; every operationId checked against the contract
---

# highlevel-enable-saas-for-location

Enable SaaS for a specific location and verify its subscription details.

## Steps

1. 1. Retrieve the location information using `locations` (requires query parameters `stripeId` and `companyId`).
2. 2. Enable SaaS for the location with `enable-saas-location` (path parameter `locationId`).
3. 3. Get the subscription details for the location using `get-location-subscription` (path parameter `locationId`).

## Rules

- Auth header: use one of the supported schemes (Agency-Access, Location-Access, or bearer) by providing the appropriate Authorization or token-id header.
- All requests are made to the server https://services.leadconnectorhq.com.
