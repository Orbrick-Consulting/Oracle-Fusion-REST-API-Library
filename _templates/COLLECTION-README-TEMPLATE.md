# <Collection Name>

## Purpose

One or two sentences on what business scenario this collection helps a consultant execute.

## Details

| Item | Value |
|---|---|
| Module | e.g. Financials |
| Category | e.g. Accounts-Payable |
| Owner | Name, email |
| Fusion release tested on | e.g. 24D, 25A |
| Authentication used | e.g. Basic Auth, OAuth 2.0 (describe type only; never include credentials) |
| Oracle API reference | Link to official docs.oracle.com REST API reference |
| Status | Active / Deprecated / Archived |

## Variables to set before use

Configure these variables in your Postman environment:

| Variable | Description | Example value |
|---|---|---|
| `{{baseUrl}}` | Your Fusion host URL | `https://your-instance.oraclecloud.com` |
| `{{username}}` | Your integration test user | `integration.user` |
| `{{password}}` | Your password (never commit; set in Postman Current Value) | (leave empty in repository) |
| `{{jwt_token}}` | Bearer token if using OAuth 2.0 / JWT | (set dynamically via Auth collection) |

## Requests included

| Step | Method | Request | Endpoint / Description |
|:---:|:---:|---|---|
| 1 | `GET` | Query records | `/fscmRestApi/resources/11.13.18.05/...` |
| 2 | `POST` | Create record | `/fscmRestApi/resources/11.13.18.05/...` |

## How to use

1. Download the `<Collection-Name>.postman_collection.json` and environment template files.
2. In Postman, click **Import** and select the files.
3. Select the imported environment and populate the variables listed above for your target test instance.
4. Run the first query request to verify connectivity and authentication.

## Known issues

List anything a consultant should be aware of (e.g. required privileges, timing constraints, known Oracle bugs). Write "None known" if empty.

## Change log

| Date | Author | Change description |
|---|---|---|
| YYYY-MM-DD | Name | Initial upload |
