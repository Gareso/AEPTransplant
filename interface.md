# Interface

The panel is divided into five zones, from top to bottom:

<img src="assets/interface-panel-overview.svg" alt="The five zones of the AEP Transplant panel" class="doc-illustration bare xl" />

---

## File Picker

<div class="illustration-row">
  <div>
    <p class="illustration-caption">Before selecting a file</p>
    <img src="assets/interface-file-picker-empty.svg" alt="File picker before a file is loaded" class="doc-illustration panel lg" />
  </div>
  <div>
    <p class="illustration-caption">After loading a file</p>
    <img src="assets/interface-file-picker-loaded.svg" alt="File picker after a file is loaded" class="doc-illustration panel lg" />
  </div>
</div>

Loads a source file. Dragging one onto the panel from Finder or Explorer does the same thing.

| Control | Description |
| ------- | ----------- |
| **Clock button** | Opens the [Recent Projects](interface.md#recent-projects) list. A blue dot on this button means one or more recent projects have been updated since you last loaded them. |
| **→ Choose AEP, PSD or AI…** | Opens a file dialog. Takes `.aep`, `.psd`, `.psb` and `.ai`. |
| **✕** | The same button once a file is loaded. Clears it, along with whatever you had checked and any destinations you had set. |
| **File name** | Displays the name of the currently loaded file. Hover over it when it's truncated to see the full path. A blue dot next to the name means the loaded file has changed on disk since you opened it. |
| **Reload button** | Appears next to the **✕** once a file is loaded. Re-reads the file from disk, picking up any changes since you opened it. |

---

## Search & Filters

<img src="assets/interface-search-filters.svg" alt="Search bar and filter checkboxes" class="doc-illustration panel" />

- **Search bar**: filters the tree by name. Clear with the × button.
- **Filter checkboxes**: show or hide **Comps**, **Media**, **Graphics**, **Design**, **3D**. OPT/ALT + click one to solo it; OPT/ALT + click again to restore all.

Filter preferences are saved between sessions.

---

## Asset Tree

<img src="assets/interface-asset-tree.svg" alt="The asset tree with folders, comps, and a swap source group" class="doc-illustration panel" />

The full folder and asset structure of the loaded file, laid out like After Effects' Project panel.

- **Folders** expand and collapse on click; OPT/ALT + click an arrow for all of them at once. They tick like anything else, taking everything inside, and carry their own crosshair that sends the whole branch to one place. See [Folder Import](features.md#folder-import).
- **Comps** show a tooltip on hover with dimensions, duration, frame rate and usage count.
- **Label colors** appear as small swatches, matching After Effects' palette.
- **Solids, Nulls and Adjustment Layers** are excluded, being scaffolding rather than reusable assets.
- **↺ Reload** re-reads the file from disk without clearing your selection.

**Checking an item** selects it for import, and a **crosshair** appears for opening the [Target Picker](features.md#target-picker). A row inside a folder that already has a destination shows that one instead, dimmed, since the folder speaks for everything under it.

**Comps** also carry a **`>`** button that opens their layers for importing individually. See [Layer Import](features.md#layer-import).

Any PSD or AI file gets a **SWAP SOURCE** row above its layer items, whether loaded directly or nested inside an `.aep`. See [Swap Source](features.md#swap-source).

---

## Merge Option

<img src="assets/interface-merge-option.svg" alt="The merge checkbox and Folder Merge Settings button" class="doc-illustration bare compact" />

**Try to merge with current project** folds imported content into your existing folder structure, combining matching folders rather than creating a new top-level import folder. See [Smart Merge](features.md#smart-merge).

The folder icon beside it opens [Folder Merge Settings](features.md#folder-merge-settings), for the matching strategy and the word lists behind similar-name matching.

Saved between sessions.

---

## Import Button & Status

<img src="assets/interface-import-status.svg" alt="The Import Selected button and status line" class="doc-illustration panel" />

**Import Selected (N)** imports all checked items, showing the count and disabled when nothing is checked. The status line below shows progress, then a summary.

---

## Recent Projects

<img src="assets/interface-recent-projects.svg" alt="The Recent Projects dropdown" class="doc-illustration panel" />

The last 10 files you loaded, each with a blue dot if it has been saved since you last loaded it here.

- Click an entry to load it immediately.
- Click **×** next to an entry to remove it from the list.
- Click **Clear Recent File List…** to wipe all entries.
