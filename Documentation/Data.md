# Data

A **Data** document is a table of entries built from one **Template**. You can create as many documents as you like from the same Template (for example, several enemy lists that all share the `Enemy` Template).

Open the **Data** tab to manage them.

## Creating a document

1. Click **+ Create** in the left panel.
2. Choose the **Template** the document is based on, give it a **Name**, and an optional **Group**.
3. Select the document in the left list to open its table.

The left list groups documents by **Group**. A small icon may appear next to a document:

- 🔴 **error** — the document has broken cross-references (e.g. a Document/Object link points to something that no longer exists);
- 🟡 **warning** — validation warnings, or the document's Template is missing.

Right-click a document for **Select**, **Copy UnnyId**, or **Delete**.

## The table

Each **row** is an entry; each **column** is a Template field, plus a **#** index, an **Id** pill, and an **Updated** timestamp.

- **+ Add Entry** — append a new entry (new rows are marked **NEW** until saved).
- **Edit cells inline** — each cell uses the editor matching its field type (text box, number, color picker, asset box with preview, document link, inline component, list, etc.).
- **Checkboxes + Clone / Delete** — tick rows to duplicate or remove them in bulk.
- **Sort** — click a column header to sort by it; click again to reverse.
- **Resize** — drag the right edge of a column header; widths are remembered per Template.
- **Id pill** — click to copy the full `UnnyId`; right-click for short/long id copy.
- **Pagination** — large documents are paged (20 entries per page).

## Document settings

The title bar shows the document name and a **⚙** button that opens its settings (rename, group, template, etc.). The subtitle shows which **Template** the document uses.

## Saving

Changes are local until you press **💾 Save**. **Reset** reverts unsaved edits (you'll be asked to confirm if there's anything to lose). Switching to another document or tab with unsaved changes is blocked until you save or discard.

## CSV import / export

Use the **📤 / 📥 CSV** buttons to move data in and out as CSV:

- **Export** writes one row per entry. Columns are `UnnyId`, the Template's scalar fields, and `Updated`. Document / Component / Object / Addressable / LocalizedString values are written as their `UnnyId`. **List** fields are marked `(list)` and are not exported as editable values.
- **Import** matches rows by `UnnyId` and updates existing entries; unknown ids are skipped. A summary reports **Applied / Skipped / Warnings**.

## Using the data in code

After a **Deploy** (see the **Deploy** tab and [First Launch](First%20Launch.md)), each document is available through the generated `DataManager`:

```csharp
IReadOnlyList<EnemyTemplate> enemies = DataConstructor.DataManager.Enemies;
```

---

See also: [Templates](Template.md) · [Database](Database.md) · [Resources](Resources.md)
