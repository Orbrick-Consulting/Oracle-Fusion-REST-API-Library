# Common: Authentication

This folder contains Postman collections for authenticating against Oracle Fusion Cloud environments and obtaining tokens for downstream API calls.

### Scope and Example Workflows:
* Oracle Identity Cloud Service (IDCS) / OCI IAM OAuth 2.0 client credentials token flow.
* User JWT token generation and session token caching.
* Pre-request script patterns to automatically renew tokens across requests.

Use this collection as a prerequisite before running API collections that rely on Bearer token authentication rather than Basic Auth.
