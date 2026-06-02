# Resources

When a field of type **Object** points to a Unity asset (a sprite, prefab, audio clip, material, …), the data file can't store the asset itself — it stores a small **id**. The mapping from that id to the real asset is kept in a system **ScriptableObject** (`ResourceLinks`) so the asset is referenced by the project and **included in your build**.

The **Resources** tab is where you inspect and maintain those links.

## What you can do

- **See every tracked asset** referenced by your data, with a preview.
- **Usage** — find which documents/entries reference a given asset, so you know what depends on it before changing or removing it.
- **Weight** — get a sense of how heavy the referenced assets are.
- **Clean up** — remove links whose asset is missing/forbidden, and prune entries no longer used by any data.

## How references are created

In a **Data** cell of an Object field you can:

- **drag & drop** an asset onto the field, or
- click the field to open Unity's **object picker**.

Either way the editor registers the asset in `ResourceLinks` and stores its id in the entry. A red outline on a cell means the referenced asset is **missing** (the link no longer resolves).

**Addressable** fields work similarly but reference the asset through the Addressables system (by address/GUID) instead of the `ResourceLinks` container.

## At runtime

The generated loader resolves ids back to assets:

```csharp
Sprite icon = DataConstructor.DataLoaderService.GetResource<Sprite>(link);
```

Because the references live in a ScriptableObject that is part of the project, the assets are pulled into the build automatically — no manual "preload" list to maintain.

## Tips

- Run a clean-up pass before shipping to drop links to assets you removed.
- Prefer **Addressable** fields for large or on-demand content you don't want loaded up front; use **Object** fields for small assets that should always be available.

---

See also: [Templates](Template.md) · [Data](Data.md) · [Database](Database.md)
