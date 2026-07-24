# Features

---

<h2 id="browse-import">Browse & Import</h2>

> 📸 *[Image needed: GIF or sequence showing: choose file → tree appears → check items → Import]*

The core workflow:

1. Click **→ Choose AEP, PSD or AI…** and pick a source file.
2. The panel reads the file and displays its full folder/asset structure — no need to open it in After Effects.
3. Check the items you want to import.
4. Click **Import Selected**.

AEP Transplant extracts only the checked items and their real dependencies. Everything else in the source project stays behind. Footage that isn't reachable from your selection is never imported.

**Supported file types:**

| Type | What you browse | What gets imported |
| ---- | --------------- | ------------------ |
| `.aep` | Full project tree — comps, folders, all footage | Selected items + their real comp/footage dependencies |
| `.psd` / `.psb` | Layers of the document | Selected layers as individual footage items |
| `.ai` | Layers / artboards of the document | Selected layers as individual footage items |

> The import itself is not undoable via Cmd+Z. To fully remove an import, undo the merge step (Cmd+Z/Ctrl+Z once) — this parks everything into a labeled folder at the project root — then manually delete that folder.

---

<h2 id="smart-merge">Smart Merge</h2>

> 📸 *[Image needed: GIF showing imported content folding into existing folders instead of creating a new root folder]*

Enable **Try to merge with current project** before importing to fold the incoming content into your existing folder structure.

With merge on, AEP Transplant matches each imported folder by name against your current project and combines them rather than creating a new top-level import folder. If a same-named item already exists in your project, you'll be prompted:

| Option | What it does |
| ------ | ------------ |
| **Replace** | Swaps the existing item with the incoming one. Layers and expressions that reference it automatically point to the new version. |
| **Use Current** | Keeps your existing item and discards the incoming duplicate. |
| **Keep Both** | Imports the incoming item alongside the existing one (name is suffixed). |

The merge step collapses into a **single Undo** (Cmd+Z/Ctrl+Z once restores everything to a labeled folder at the project root). The import that preceded it is separate and not undoable.

> Merge preference (on/off) is remembered between sessions.

---

<h2 id="swap-source">Swap Source</h2>

> 📸 *[Image needed: screenshot of a SWAP SOURCE row in the tree panel, and/or GIF showing the replace-all-layers flow]*

When you load a PSD or AI file, a **SWAP SOURCE** row appears above the file's individual layer items, marked with a blue badge.

**Swap Source** lets you replace every layer of a source file across your entire current project in one action — instead of updating each layer one by one. This is perfect for re-skinning a character rig or updating artwork across a complex project.

**How it works:**

1. Check the **SWAP SOURCE** row (and/or its individual layer rows).
2. Click the **crosshair icon** that appears next to the checked row to open the Target Picker.
3. In the picker, select the existing footage item in your current project that you want to replace.
4. Click **Import Selected**.

AEP Transplant matches the source file's layers to the targeted item's layers by name, replaces each one, and handles any layers that don't find a match by parking them in a "no match" folder.

> OPT/ALT + click the crosshair icon to clear a target assignment.

---

<h2 id="target-picker">Target Picker</h2>

> 📸 *[Image needed: screenshot of the Target Picker modal overlaid on the panel]*

When an item is checked, a **crosshair icon** appears next to it. Click it to open the Target Picker — a modal that lets you manually point that imported item at a specific existing item or folder in your current project, overriding the automatic name-based merge matching.

| Target type | What happens at import |
| ----------- | ---------------------- |
| **Comp or footage item** | Replaces the targeted item. Layers and expressions referencing it update automatically. |
| **Folder** | Places the imported item into that folder instead of wherever the merge logic would put it. |

Use the search bar and filter checkboxes inside the picker to quickly find the right target in a large project. OPT/ALT + click any folder arrow to collapse or expand all folders at once.

Once a target is set, the crosshair icon turns **blue**. OPT/ALT + click it to clear the assignment.

---

<h2 id="search-filter">Search & Filter</h2>

> 📸 *[Image needed: screenshot of search and filter bar]*

**Search** filters the asset tree by name (case-insensitive substring). Results update live as you type.

**Filter checkboxes** show or hide items by category:

| Filter | Covers |
| ------ | ------ |
| Comps | After Effects compositions |
| Media | Video and audio files |
| Graphics | Image files (PNG, JPG, EXR, TGA, SVG…) |
| Design | Layered design files (PSD, AI, PDF, EPS…) |
| 3D | 3D asset files (C4D, OBJ, FBX, GLTF…) |

**OPT/ALT + click** a filter checkbox to solo it — showing only that category and hiding the rest. OPT/ALT + click again to restore the previous state.

Filter preferences are saved between sessions.

---

<h2 id="update-watcher">Update Watcher</h2>

> 📸 *[Image needed: screenshot showing the blue dot on the Recent Projects button and next to the file name]*

AEP Transplant watches the files you've worked with and tells you when they change:

- A **blue dot on the clock button** means one or more projects in your recent list have been saved since you last loaded them here.
- A **blue dot next to the loaded file name** means the currently open source file has changed on disk since you loaded it.
- Blue dots **inside the Recent Projects list** appear on individual entries that have updated.

Click **↺ Reload** to re-read the current file from disk and pick up any changes.

This is especially useful on shared projects — if a teammate updates an `.aep` you're sourcing from, the dot lets you know before you import stale content.

---

<h2 id="undo">Undo Behavior</h2>

AEP Transplant separates the import into two phases, each with different undo behavior:

| Phase | Undoable? | Notes |
| ----- | :-------: | ----- |
| **Import** | No | Brings the reduced project into AE. Cannot be reversed via Cmd+Z. |
| **Merge** | Yes | Every move, replace, and rename collapses into a single Undo step. |

**To fully discard an import:**
1. Undo the merge: Cmd+Z/Ctrl+Z **once**. This parks everything back into a single labeled folder at the project root (named after the source file, suffixed `(not merged)` if anything was left unmatched).
2. Manually delete that folder from the Project panel.

Nothing is ever silently lost — it's one manual deletion instead of a full automatic undo.
