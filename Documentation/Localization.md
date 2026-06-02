# Localization

The **Localization** tab manages localized strings — one **Key** per entry with a value for each enabled language. Template fields of type **LocalizedString** reference these keys, so your data stays language-agnostic and the actual text lives in one place.

## The table

The right side is a grid: a **#** index, a **Key** column, and one column per enabled language.

- **+ Add New** — add a localization entry.
- Type the **Key** and the value for each language directly in the cells.
- The **: / ✎** icon on each row opens a context menu to **add / edit a translator note** (a hint for whoever translates, e.g. "shown in the main menu, max 12 chars") or to **delete** the entry. A note turns the icon into **✎** and shows on hover.
- Press **💾 Save** to persist, **Reset** to discard unsaved edits.

The set of languages comes from the project settings (`Tools > Data Constructor > Settings`); if none are configured, a built-in default list is used.

## Auto-translation

The left panel configures automatic translation:

| Setting | Meaning |
|---------|---------|
| **Provider** | Translation backend (see below). |
| **Source Language** | The language to translate *from*. |
| **Target Language** | The language to translate *into* (the source is excluded from the list). |
| **Skip existing translations** | Leave already-filled target cells untouched. |
| **Provider Settings** | Per-provider options such as API URL and model. |

Press **Launch Auto-Translation** to translate every entry from the source to the target language. A progress bar shows status; the same button cancels a run in progress.

### Providers

| Provider | Notes |
|----------|-------|
| **Google Translate** | Uses default Google settings. |
| **DeepL** | Configurable API URL. |
| **Ollama** | Local LLM — set the API URL and model (e.g. `gemma3:4b`). |
| **LibreTranslate** | Self-hosted / public Libre instance. |
| **LM Studio** | Local OpenAI-compatible server — set API URL and model. |

A **translation memory** is built from your existing translations: identical source strings reuse a previous result instead of calling the provider again, which keeps output consistent and avoids redundant requests.

## At runtime

Use the generated localization manager to read the active-language value for a key, and switch languages as needed. LocalizedString fields on your data resolve to the same keys you edit here.

---

See also: [Templates](Template.md) · [Data](Data.md)
