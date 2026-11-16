# ERP: Integration

This folder contains Postman collections for cross-functional integration processes that span multiple functional areas or interact directly with the Oracle Fusion Cloud ERP integration framework.

### Scope and Example Workflows:
* Enterprise Scheduler Service (ESS) job execution, monitoring, and output retrieval.
* Oracle ERP Integration Service (SOAP/REST bridging, data load triggers).
* Universal Content Management (UCM / WebCenter Content) document check-in and search.
* Business Event subscriptions and webhook callbacks.

When to use this folder:
Use `ERP/Integration/` only when a collection spans across multiple functional domains. If an integration is specific to a single domain (for example, importing only AP Invoices), place it under that specific module (such as `Financials/Accounts-Payable/`).
