# Contributing

Short guide for adding or updating Postman collections in this library.

---

## Core Rules

1. **Never push to `main`** — Work on a feature branch and open a Pull Request.
2. **One maintainer approval** — Every PR requires review before merge.
3. **Dedicated folder** — Every collection lives in `<Module>/<Category>/<Collection-Name>/` with 3 files:
   * `<Collection-Name>.postman_collection.json` *(Collection v2.1)*
   * `<Collection-Name>.postman_environment.template.json` *(blank values only)*
   * `README.md` *(copied from [_templates/COLLECTION-README-TEMPLATE.md](./_templates/COLLECTION-README-TEMPLATE.md))*
4. **Sanitize everything** — Zero credentials, tokens, client pod URLs, or real customer data.
5. **Update the category index** — Add a row for your collection in the parent category `README.md`.

---

## Naming Rules

* Use **`Title-Case-With-Hyphens`** and the category's prefix (for example, `AP-Invoices-Create-and-Query`).
* **Avoid** spaces, underscores, version tags (`_v2`, `_final`), dates, or personal names in file/folder paths.

---

## Pre-Upload Sanitization Checklist

Check these six areas in Postman before exporting:

| Area | What to clean |
|---|---|
| **Authorization** | Remove usernames, passwords, Bearer tokens, and client secrets. Use `Inherit auth from parent`. |
| **Headers** | Remove hardcoded `Authorization` headers or tenant-specific headers. |
| **Variables** | Clear all **Initial** and **Current** values. Keep only variable keys (`fusion_host`, `jwt_token`, etc.). |
| **Scripts** | Check Pre-request and Test scripts for hardcoded secrets or client URLs. |
| **Examples** | Replace real employee/supplier/invoice records with generic Vision or ABC sample data. |
| **URLs** | Start every request URL with `{{fusion_host}}` (never a client pod URL). |

---

## How to Submit

### Option A: GitHub Website (Quick Uploads)

1. Navigate to `<Module>/<Category>/` on GitHub and confirm no duplicate exists.
2. Prepare your `<Collection-Name>/` folder locally with the 3 required files.
3. Click **Add file → Upload files** and drag the folder into the upload box.
4. Select **Create a new branch for this commit and start a pull request** (e.g. `add-ap-invoices-collection`).
5. Complete the PR checklist and click **Create pull request**.

### Option B: GitHub Desktop (Recommended for Regular Updates)

1. Switch to `main` and click **Fetch origin / Pull origin**.
2. Create a new branch (**Branch → New branch...**).
3. Add or update your collection folder in `<Module>/<Category>/` and update the category `README.md`.
4. Review changes in the **Changes** tab to ensure no secrets are present.
5. Commit with a clear message (e.g. `Add AP Invoices create and query collection`), click **Publish branch**, and open the PR.

---

## Updating an Existing Collection

1. Always branch from the latest `main`.
2. Replace `<Collection-Name>.postman_collection.json` using the **same filename**.
3. Add a row to the **Change Log** table in the collection's `README.md`.
4. Open a PR and verify the diff in **Files changed**.

> **Accidental secret committed?** Revoke the credential at the source immediately, notify a maintainer, and close the PR so the commit can be purged from history.

