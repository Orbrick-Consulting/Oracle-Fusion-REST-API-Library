# Oracle Fusion REST API Library

Shared, sanitized Postman collections for Orbrick Oracle Fusion Cloud consultants.

---

## Directory

Browse collections by **Module** and **Category**:

| Module | Category | Naming Prefix | Focus |
|---|---|---|---|
| **Financials** | [General Ledger](./Financials/General-Ledger/) | `GL-` | Journals, COA, periods, daily rates |
| **Financials** | [Accounts Payable](./Financials/Accounts-Payable/) | `AP-` | Payables invoices, holds, payments |
| **Financials** | [Accounts Receivable](./Financials/Accounts-Receivable/) | `AR-` | Receivables invoices, receipts |
| **Financials** | [Cash Management](./Financials/Cash-Management/) | `CE-` | Bank accounts, statements, reconciliation |
| **Financials** | [Fixed Assets](./Financials/Fixed-Assets/) | `FA-` | Additions, adjustments, retirements |
| **Procurement** | [Purchase Orders](./Procurement/Purchase-Orders/) | `PO-` | Purchase orders, change orders |
| **Procurement** | [Requisitions](./Procurement/Requisitions/) | `POR-` | Self-service requisitions, approvals |
| **Procurement** | [Suppliers](./Procurement/Suppliers/) | `PO-Suppliers-` | Supplier profiles, sites, contacts |
| **SCM** | [Inventory](./SCM/Inventory/) | `INV-` | On-hand balances, transfers, counts |
| **SCM** | [Order Management](./SCM/Order-Management/) | `OM-` | Sales orders, fulfillment, holds |
| **HCM** | [Core HR](./HCM/Core-HR/) | `HCM-CoreHR-` | Workers, assignments, org structures |
| **HCM** | [Absence](./HCM/Absence/) | `HCM-Absence-` | Leave requests, accrual balances |
| **ERP** | [Integration](./ERP/Integration/) | `ERP-` | Cross-module FBDI, ERP Integration Service, events |
| **Common** | [Authentication](./Common/Authentication/) | `Auth-` | IDCS / OCI IAM OAuth 2.0 & JWT tokens |
| **Common** | [Attachments](./Common/Attachments/) | `Common-Attachments-` | Reusable `/child/attachments` patterns |
| **Common** | [Utilities](./Common/Utilities/) | `Common-Utilities-` | Lookups, flexfields, BU/Ledger IDs, health checks |

### Collection Layout

Every collection lives in its own folder under `Module/Category/`:

```text
<Module>/<Category>/<Collection-Name>/
├── <Collection-Name>.postman_collection.json
├── <Collection-Name>.postman_environment.template.json
└── README.md
```

---

## Quick Start

1. **Download** — Open a collection folder and click **Download raw file** on the `.json` files (or use **Code → Download ZIP** for the full library).
2. **Import** — In Postman, click **Import** and select both the collection and environment template files.
3. **Configure** — Select the imported environment, set `{{fusion_host}}` and your credentials in **Current Value**, and run your first request.

---

## Contributing

1. **Branch & PR only** — Never push directly to `main`. All changes require a Pull Request and one maintainer approval.
2. **Use the templates** — Copy [_templates/COLLECTION-README-TEMPLATE.md](./_templates/COLLECTION-README-TEMPLATE.md) and [_templates/COLLECTION-ENVIRONMENT-TEMPLATE.json](./_templates/COLLECTION-ENVIRONMENT-TEMPLATE.json) into your collection folder.
3. **Zero secrets** — Strip all passwords, tokens, client hostnames (`{{fusion_host}}` only), and real customer data before uploading.

See [CONTRIBUTING.md](./CONTRIBUTING.md) for the step-by-step guide, or open the [Training Manual](./docs/Oracle-Fusion-REST-API-Library-Training-Manual.docx).

