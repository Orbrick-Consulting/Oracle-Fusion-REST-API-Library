# Contribution Guidelines

Thank you for contributing to the Oracle Fusion REST API Library. By sharing verified Postman collections, you help fellow consultants save hours of repetitive setup across projects.

Every team member follows the same set of contribution rules to keep the library organized, up-to-date, and secure.

---

## The Six Core Rules

1. **Private Repository Access**: Access is granted through your GitHub team. Never duplicate this repository into a public repository.
2. **Never Commit to `main` Directly**: The `main` branch is protected. All additions and updates must be submitted through a branch and a Pull Request.
3. **One Maintainer Approval**: Every Pull Request must be reviewed and approved by a maintainer before it is merged.
4. **Dedicated Collection Folder**: Each collection lives in its own folder containing a `.postman_collection.json` file, an environment template, and a completed `README.md` naming the owner.
5. **Zero Credentials or Confidential Data**: Sanitize every file before uploading. The contributor checks first, and the maintainer checks during review.
6. **Choice of Tools**: You may contribute via the GitHub website (browser) or GitHub Desktop. Both produce the same Pull Request.

---

## Directory Hierarchy and Naming Conventions

### Three-Level Hierarchy
Collections must be placed in:
`[Module] / [Category] / [Collection-Folder]`

Example:
`Financials/Accounts-Payable/AP-Invoices-Create-and-Query/`

### Naming Standards
* **Casing**: Use `Title-Case-With-Hyphens` for category folders and collection folders.
* **No Spaces or Special Characters**: Do not use spaces, parentheses, brackets, underscores, or ampersands.
* **No Version Numbers or Dates in Names**: Git tracks versions and timestamps automatically. Avoid `_v2`, `_final`, `_new`, or date tags like `202611`.
* **No Personal Names in File or Folder Names**: Record your name inside the collection `README.md`, not in the path.

### Required Files in Each Collection Folder
1. `<Collection-Name>.postman_collection.json`: Exported from Postman using the **Collection v2.1** format.
2. `<Collection-Name>.postman_environment.template.json`: Environment file containing only variable names with blank default/initial values.
3. `README.md`: Copied from `_templates/COLLECTION-README-TEMPLATE.md` and filled out.

---

## Pre-Upload Sanitization Checklist

Before exporting any collection from Postman, check these six hotspot locations for sensitive data:

1. **Authorization Tab**: Clear all Basic Auth usernames, passwords, Bearer tokens, and OAuth client secrets from the collection, folder, and request levels. Set the authorization type to inherit from parent where possible.
2. **Request Headers**: Remove explicit `Authorization` headers with pasted tokens, and remove custom tenant/client headers.
3. **Variables**: In the collection variable table, clear all values under both **Initial Value** and **Current Value**. Leave only the variable keys (for example, `fusion_host`, `jwt_token`, `invoice_id`).
4. **Pre-request and Test Scripts**: Check JavaScript code for hardcoded tokens, passwords, or client URLs.
5. **Saved Response Examples**: Review saved response examples. Remove real client employee records, supplier tax IDs, real invoice totals, and banking numbers. Replace them with standard Oracle sample data (such as Vision Corporation or ABC Supplies).
6. **Request URLs**: Ensure all URLs start with `{{fusion_host}}` rather than a specific customer pod URL (such as `https://fa-xxxx-test.fa.ocs.oraclecloud.com`).

---

## Contributing via GitHub Website (Browser Method)

1. **Check for Duplicates**: Use the GitHub search bar or navigate to the relevant category to confirm a similar collection does not already exist.
2. **Prepare Files Locally**: Create a local folder matching your collection name (for example, `AP-Invoices-Create-and-Query`). Place the sanitized JSON collection, environment template, and completed `README.md` inside it.
3. **Navigate to the Category Folder**: On GitHub, click into the module and category (for example, `Financials/Accounts-Payable/`).
4. **Upload Files**: Click **Add file** > **Upload files**. Drag the entire local folder into the upload drop zone.
5. **Write Commit Message**:
   * *Summary*: Short imperative phrase (for example: `Add AP Invoices create and query collection`).
   * *Description*: Mention Fusion release tested on (for example: `Tested on 24D and 25A`).
6. **Create Branch and Propose Changes**:
   * Select **Create a new branch for this commit and start a pull request**.
   * Give the branch a clear name (for example, `add-ap-invoices-collection`).
   * Click **Propose changes**.
7. **Submit the Pull Request**: Fill in the PR template, verify the checklist boxes, and click **Create pull request**.

---

## Contributing via GitHub Desktop

1. **Update Local Copy (Step 0)**: Open GitHub Desktop, set Current Branch to `main`, click **Fetch origin**, and click **Pull origin** if updates are available.
2. **Create a New Branch**: Go to **Branch** > **New branch...**, name it descriptively (for example, `add-ap-invoices-collection`), and create it from `main`.
3. **Place Files in Local Repository**: Choose **Repository** > **Show in Explorer** (or **Show in Finder** on macOS). Navigate to the right module and category folder, create your collection folder, and paste your files inside.
4. **Review Changes**: Return to GitHub Desktop. In the **Changes** tab on the left, verify that only your intended files appear with green plus icons. Check the contents in the diff viewer.
5. **Commit**: Enter a descriptive summary (for example, `Add AP Invoices create and query collection`) and click **Commit to [branch]**.
6. **Publish and Open PR**: Click **Publish branch** at the top. Once published, click the **Create Pull Request** button that appears. This opens GitHub in your browser.
7. **Complete the PR**: Review the checklist, check the boxes, and submit the Pull Request.

---

## Commit Message Guidelines

Write clear, informative commit messages so your colleagues know what changed when reading the repository history:

* **Good Examples**:
  * `Add Purchase Orders creation and lifecycle collection`
  * `Update AP Invoices: add cancel invoice and line query endpoints`
  * `Fix missing Content-Type header in Supplier Sites POST request`
* **Weak Examples to Avoid**:
  * `Upload files`
  * `Updates`
  * `Changes for project`
  * `fixed`

---

## Updating an Existing Collection

When you need to enhance or fix an existing collection:
1. Always start from the latest file on `main`. Do not use an outdated local copy from months ago.
2. Create a new branch (for example, `update-ap-invoices-cancel-endpoint`).
3. Make your updates in Postman, re-export, and verify that credentials remain clean.
4. Replace the existing `.postman_collection.json` file in the collection folder using the exact same file name.
5. Add a row to the **Change Log** table in the collection's `README.md`.
6. Submit a Pull Request and verify in the **Files changed** tab that only the expected lines are added or modified.

---

## Review and Merge Process

* **Turnaround Time**: Maintainers review Pull Requests within two working days.
* **If Changes Are Requested**: Make the adjustments on the same branch and push the new commit. The Pull Request will automatically refresh.
* **Merge**: Once approved, the maintainer merges the branch into `main`. You can then safely delete your working branch.
