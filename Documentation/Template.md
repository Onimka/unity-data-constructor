# Templates

A **Template** describes the *shape* of your data — think of it as a class definition. Every **Data** document is built from one Template, and every entry in that document follows the Template's fields.

Open the **Templates** tab to create and edit them.

## Creating a Template

1. Click **+ Create** in the left panel.
2. Fill in the form (only the **Name** is required) and confirm.
3. Select the new Template in the left list to open its editor.

The left panel lists all Templates, grouped by **Type** (Documents / Components) and then by their optional **Group**. Use the right-click menu on an item to **Select**, **Copy UnnyId**, or **Delete**.

## Template properties

| Property | Meaning |
|----------|---------|
| **Class Name** | Technical name; also the name of the generated C# class. Must be unique. |
| **Group** | Optional grouping label used to organize the left list. |
| **Description** | Free-text note for your team. |
| **Type** | `Document` (a standalone data list) or `Component` (an embedded structure owned by another entry). |
| **Flags** | `Abstract` and `Partial` — affect the generated C# class declaration. |
| **Base Template** | Inherit fields from another Template (see *Inheritance*). |

## Fields

Click **+ Add Field** to add a field. Each field has a **Name**, a **Type**, and an optional **Description** (shown as a tooltip on the data table header).

Reorder fields with the **↑ / ↓** buttons. Click a field's name to edit it; **Delete** removes it (inherited fields are read-only).

### Field types

| Type | Stores |
|------|--------|
| **Int / Long / Float** | Numeric values. |
| **String** | Text. |
| **Bool** | Toggle. |
| **Color** | RGBA color (stored as a hex string). |
| **LocalizedString** | A reference to a key from the **Localization** tab. |
| **Object** | A direct `UnityEngine.Object` reference — `GameObject`, `Sprite`, `Texture2D`, `Material`, `AudioClip`, `VideoClip`, `AnimationClip`, `AnimatorController`, `ScriptableObject`, or any object. The asset is tracked in **Resources** so it ships with the build. |
| **Addressable** | A reference to an Addressable asset (by GUID/address). |
| **Document** | A reference to an entry in another **Document** (cross-data link). |
| **Component** | An embedded structure based on a Component Template, edited inline. |
| **List** | A list of any of the above (with optional numbering and reordering). |

## Display Format

For Templates used as **Document** references, the **Display Format** section lets you choose which fields are shown in the link cell. Toggle **Name** and/or **Value** per field so a referenced document is recognizable at a glance instead of showing a raw id.

## Inheritance

Set a **Base Template** to inherit its fields. Inherited fields appear in children as read-only links and stay in sync with the parent. The **Children** foldout lists every Template that inherits from the current one.

Use `Abstract` for base Templates that should never be instantiated directly, and `Partial` when you want to extend the generated class with your own hand-written code.

## Documents vs Components

- A **Document** Template produces standalone data lists you fill in the **Data** tab.
- A **Component** Template is meant to be embedded inside other entries via a **Component** field. Components are selected through a small menu (which respects inheritance) and edited inline within the owning entry.

## Saving

Edits are local until you press **💾 Save**. **Reset** reverts unsaved changes. Switching away from a Template with unsaved changes will ask for confirmation. Names are validated for uniqueness before saving.

---

See also: [Data](Data.md) · [Localization](Localization.md) · [Resources](Resources.md)
