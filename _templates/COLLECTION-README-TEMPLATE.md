# <Collection Name>

One-sentence description of the business scenario this collection covers.

| Field | Value |
|---|---|
| **Module / Category** | e.g., `Financials / Accounts-Payable` |
| **Owner** | Name (`email@orbrick.com`) |
| **Fusion Release** | e.g., `24D`, `25A` |
| **Auth Type** | e.g., `OAuth 2.0 Bearer` / `Basic Auth` |
| **Oracle Docs** | [REST API Reference](https://docs.oracle.com/en/cloud/saas/index.html) |
| **Status** | `Active` |

## Requests

| # | Method | Name | Endpoint |
|:---:|:---:|---|---|
| 1 | `GET` | Query records | `/fscmRestApi/resources/11.13.18.05/...` |
| 2 | `POST` | Create record | `/fscmRestApi/resources/11.13.18.05/...` |

## Environment Variables

Set these in Postman **Current Value** before running (never commit real values):

| Variable | Description | Example |
|---|---|---|
| `{{fusion_host}}` | Fusion pod base URL | `https://your-instance.oraclecloud.com` |
| `{{username}}` | Integration user (if Basic Auth) | `integration.user` |
| `{{password}}` | User password (if Basic Auth) | *(keep blank in repo)* |
| `{{jwt_token}}` | Bearer token (if OAuth / JWT) | *(generated via Auth collection)* |

## Quick Use

1. Import `<Collection-Name>.postman_collection.json` and `<Collection-Name>.postman_environment.template.json`.
2. Select the environment and populate your target pod variables.
3. Run Request `#1` to verify connectivity.

## Notes

* *None known* (list required roles, privileges, or Oracle quirks here).

## Change Log

| Date | Author | Summary |
|---|---|---|
| YYYY-MM-DD | Name | Initial upload |

