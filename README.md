# Oracle Fusion REST API Library

Welcome to the shared Oracle Fusion Cloud REST API Postman Collection Library for Orbrick consultants.

This private repository is the central home for all verified, reusable Postman collections across Oracle Fusion Cloud applications. Instead of keeping Postman collections isolated on individual laptops or sharing outdated JSON files over chat, this library maintains versioned, reviewed, and secure collections accessible to the entire consulting team.

---

## Repository Structure

Collections are organized in a three-tier hierarchy: **Module / Category / Collection Folder**.

* **ERP/**: Platform integrations, cross-module setups, and foundational workflows that span multiple functional domains.
* **Financials/**: General Ledger, Accounts Payable, Accounts Receivable, Cash Management, Fixed Assets, Expenses, and Tax.
* **Procurement/**: Purchase Orders, Requisitions, Suppliers, Sourcing, and Purchasing Agreements.
* **SCM/**: Inventory Management, Order Management, Manufacturing, and Logistics.
* **HCM/**: Core HR, Absence Management, Payroll, Talent Management, and Recruiting.
* **Common/**: Shared utility patterns, including OAuth/JWT token retrieval, UCM attachments, ESS jobs, and bulk data import/export.

Each collection resides in its own folder with a collection JSON file, an environment template, and a `README.md` identifying the collection owner and usage guide.

---

## How to Download and Use a Collection

### Download One Collection
1. Navigate to the relevant module and category folder above.
2. Open the collection folder (for example, `Financials/Accounts-Payable/AP-Invoices-Create-and-Query`).
3. Click on the `.postman_collection.json` file.
4. Click the **Download raw file** button (downward arrow icon) in the top-right corner of the file viewer.
5. In Postman, click **Import** (top left), select or drag the downloaded file, and confirm import.
6. If the collection folder includes a `.postman_environment.template.json` file, download and import it as well, then fill in your project-specific host and credentials in Postman.

### Download the Entire Library
1. On the repository home page, click the green **Code** button.
2. Select **Download ZIP**.
3. Extract the ZIP file locally and import whichever collections you need into Postman.

---

## How to Contribute

All contributions must follow our contribution policy:
1. **Never commit directly to `main`**: Always work on a separate branch and open a Pull Request.
2. **Sanitize thoroughly**: Every exported file must be checked for passwords, tokens, client URLs, and sensitive customer data.
3. **Include the collection standard files**: Each collection requires a dedicated folder containing the `.postman_collection.json`, a blank `.postman_environment.template.json`, and a completed `README.md`.
4. **Peer Review**: At least one maintainer review is required before merging.

You can contribute using either:
* **Method 1 (Browser)**: Ideal for quick updates and occasional uploads without local Git setup.
* **Method 2 (GitHub Desktop)**: Recommended for regular contributors, large collections, and multi-file changes.

For step-by-step instructions and pre-upload checklists, read [CONTRIBUTING.md](CONTRIBUTING.md).

---

## Security and Credentials Policy

This repository is private to authorized Orbrick team members. However, private access is not a substitute for data sanitization.

* **Never upload real passwords, Bearer tokens, or API keys.**
* **Never upload real customer data, employee records, or supplier bank details in saved examples.**
* **Never upload client-specific hostnames.** Use generic variable placeholders such as `{{fusion_host}}`.

If a secret is accidentally committed to any branch:
1. Revoke and change the credential at the source immediately.
2. Notify the repository maintainers.
3. Close the Pull Request so the commit can be permanently removed from Git history.

---

## Maintainers

* Repository Owner: [Your Name / Orbrick Lead]
* Lead Maintainers: [Maintainer Team]
* Response SLA: Pull Requests are reviewed within two working days.
