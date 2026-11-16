## What does this Pull Request do?

- [ ] Adds a new collection
- [ ] Updates an existing collection
- [ ] Fixes a bug or endpoint error
- [ ] Documentation update only

* **Module**: [ERP / Financials / Procurement / SCM / HCM / Common]
* **Category**: [e.g. Accounts-Payable]
* **Collection Name**: [e.g. AP-Invoices-Create-and-Query]

## Summary of changes

Provide a concise 1-3 sentence summary of the business process and API operations covered.

## Contributor checklist

Please verify and check every item before opening the Pull Request:

- [ ] I searched the repository and confirmed this is not a duplicate collection.
- [ ] The module and category folders follow repository conventions.
- [ ] Folder and file names follow the `Title-Case-With-Hyphens` pattern.
- [ ] The collection was exported from Postman as **Collection v2.1**.
- [ ] The collection folder contains a filled-in `README.md` naming the owner.
- [ ] An environment template (`.postman_environment.template.json`) is included with blank values.
- [ ] I searched the JSON file for `password`, `token`, `Bearer`, `secret`, `Basic `, and client identifiers and found none.
- [ ] All request URLs use `{{baseUrl}}` rather than client-specific pod URLs.
- [ ] Response examples are sanitized and do not contain real client data.
- [ ] If updating an existing collection, I added a new row to the Change Log in `README.md`.

## Maintainer review checklist

- [ ] Folder hierarchy and naming conventions are verified.
- [ ] JSON inspected for secrets and confidential client data.
- [ ] README is complete and explains business context and owner.
- [ ] Environment template contains blank values only.
- [ ] Diff in "Files changed" shows only intended modifications.
