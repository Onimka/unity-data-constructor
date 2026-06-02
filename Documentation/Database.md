# Database & Branches

The **Database** controls *where* your Templates, Data and Localization are stored. The top toolbar exposes the active **Branch** and **Database** mode, each with its own **⚙** settings button and a **↻** refresh button.

## Storage modes

| Mode | Where data lives | Use for |
|------|------------------|---------|
| **Local** | `Assets/Data Constructor` inside your project | Solo work, version control via your own repo. |
| **Firebase** | Firebase Realtime Database | Teams — shared cloud storage so everyone edits the same data. |

Switch modes from the **Database** dropdown in the top bar. Selecting a mode reloads the data for that backend.

The asset references used by Object/Addressable fields are always stored locally in a system ScriptableObject (see [Resources](Resources.md)) so they're included in the build regardless of the database mode.

### Firebase setup

Open the **⚙** next to the Database dropdown to enter your Firebase **URL** and **secret**. The secret is entered through a masked field. Once configured, switching to **Firebase** loads and saves data in the cloud.

## Branches

Branches work like lightweight version branches for your data (for example `Development`, `Release`). They let you stage changes without touching the data another part of the team relies on.

- Switch branches from the **Branch** dropdown.
- Open the **⚙** next to it to **create**, **delete**, and **merge** branches.
- **Merge** compares a source and target branch (added / deleted / modified Templates and Data) and shows a preview before applying. Newer entries win on conflicts.

## Refresh

Press **↻** to force a full reload from the active database. This is rarely needed — the editor refreshes after saves and branch/mode switches — but it's handy after external changes (e.g. someone else pushed to Firebase).

## How data is stored

Within a branch, the editor keeps separate folders for **Templates** and **Data**, plus a single **Localization** file and a change **Log**. On **Deploy**, the data is published into `Resources/Data` as clean JSON and the C# classes are generated, which is what the game loads at runtime.

The on-disk JSON format is stable; upgrading the plugin does not change how your existing data is serialized.

---

See also: [Data](Data.md) · [Templates](Template.md) · [First Launch](First%20Launch.md)
