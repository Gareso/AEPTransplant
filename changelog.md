## Changelog

---

### v1.4.1 - Unreleased

<h3 style="color:#EB6669">FIXED</h3>

* **Consistent comp previews:** comp previews now look the same whatever your After Effects render defaults are.

---

### v1.4.0 - October 8, 2026

<h3 style="color:#EB6669">ADDED</h3>

* **Comp previews:** see the first seconds of any comp, or a still frame, without leaving your project. See [Previews](features.md#previews).
* **Footage previews:** images, videos, Photoshop, Illustrator, PDF and 3D files preview too.
* **Preview Settings:** choose animated or still previews, clear saved ones, or turn previews off. See [Preview Settings](features.md#preview-settings).

<h3 style="color:#EB6669">FIXED</h3>

* **Image sequences:** sequences now show their real name, like `render_[0001-0100].png`, instead of their folder's.

---

### v1.3.1 - October 7, 2026

<h3 style="color:#EB6669">ADDED</h3>

* **Templates:** .AET files are now supported.
* **Choose where copies go:** pick the folder for external assets before they're copied, with or without a subfolder. See [External Assets](features.md#external-assets).
* **Cancel an import:** back out from the External Assets dialog before anything is copied or imported.

<h3 style="color:#EB6669">CHANGED</h3>

* **Better default folder:** default external assets folder is the folder of your project that holds the most media.
* **Windows file dialogs:** choosing a file or folder now opens the current Explorer dialog, with Quick Access and the address bar.
* **Clearer errors:** a file that won't open now says why, with a way out.
* **Empty folders:** the Target Picker now shows empty folders by default.

<h3 style="color:#EB6669">FIXED</h3>

* **Renamed item icons:** items renamed in After Effects now show the right file type icon.

---

### v1.3.0 - September 28, 2026

<h3 style="color:#EB6669">CHANGED</h3>

* **Faster imports:** AEP Transplant is much faster now.
* **Minor UI changes:** the project panel's change dots now sit next to the item name, plus other small changes. See [Update Watcher](features.md#update-watcher).

<h3 style="color:#EB6669">FIXED</h3>

* **PSD and AI file targets:** layer targets now work as intended, and single-layer PSDs open without issues. See [Target Picker](features.md#target-picker).

---

### v1.2.0 - September 16, 2026

<h3 style="color:#EB6669">ADDED</h3>

* **Folder import:** check a folder to take everything inside it. See [Folder Import](features.md#folder-import).
* **Folder targets:** send a whole folder to one place, merging into it or nesting inside it depending on the name.
* **New folders from the Target Picker:** build the destination you want without leaving the panel, then rename, move or delete it before importing. See [Target Picker](features.md#target-picker).
* **Intel Mac support:** imports now run on Intel Macs.

<h3 style="color:#EB6669">CHANGED</h3>

* **Duplicates are checked project-wide:** aiming at a folder now finds a copy you already have anywhere, not just at the destination.
* **Folder names show as they are:** the tree no longer forces them to capitals, so `PreRenders` stays `PreRenders`.

---

### v1.1.4 - September 10, 2026

<h3 style="color:#EB6669">ADDED</h3>

* **Proxy support:** proxies now come across with the items that use them, copied into your project and relinked along with everything else, and the Use Proxy setting arrives exactly as you left it. Items with a proxy are marked in the tree the way After Effects marks them in its Project panel. See [External Assets](features.md#external-assets).
* **Smarter external file copy:** you're only asked about assets your project doesn't already have, so importing from the same source again reuses what's there instead of asking every time. When an incoming file shares a name with a different file already in your asset folder, you choose **Overwrite**, **Use Current** or **Keep Both**, with **Apply to all** for the rest of the import.

<h3 style="color:#EB6669">CHANGED</h3>

* **Long names now show both ends:** an item name too long for the panel is shortened in the middle rather than cut off at the end, the way Finder does it, so the version or extension you were looking for stays readable.

---

### v1.1.3 - September 1, 2026

<h3 style="color:#EB6669">FIXED</h3>

* **Maintenance:** internal improvements and minor fixes.

---

### v1.1.2 - August 30, 2026

<h3 style="color:#EB6669">ADDED</h3>

* **Blue dots now track changes within the project:** reloading a source file now marks the comps, footage and layers that changed or were added, not just the file itself. See [Update Watcher](features.md#update-watcher).
* **Expressions are followed for whole comps:** importing a comp now brings the comps and footage its expressions point to, with the same confirmation you get for layers. See [What comes with a layer](features.md#what-comes-with-a-layer).

<h3 style="color:#EB6669">CHANGED</h3>

* **Expressions that name their own comp:** these are now converted to `thisComp`, so they keep working after import, and any layer they depend on comes along.

---

### v1.1.1 - August 27, 2026

<h3 style="color:#EB6669">FIXED</h3>

* **macOS security warning:** imports on macOS could stop with a system warning about an unverified file.
* **[Target Picker](features.md#target-picker) for layers:** hides the items a layer cannot go into, instead of listing them greyed out.
* **Target Picker labels:** the title names the layer you clicked, and the top row names your open project.

---

### v1.1.0 - August 22, 2026

<h3 style="color:#EB6669">ADDED</h3>

* **Layer import:** open any comp from the asset tree and pick individual layers out of it instead of taking the whole comp. See [Layer Import](features.md#layer-import).
* **Layer targets:** point a comp's imported layers at a comp that already exists in your project, and they are copied into it instead of arriving in the comp they came from.
* **Dependency confirmation:** before importing layers, the panel lists what else has to come with them (parent chains, track mattes, layers used by effects and expressions) and offers **Include Dependencies** or **Selected Layers Only**.
* **Drag and drop:** drop an `.aep`, `.psd`, `.psb` or `.ai` straight onto the panel to load it.

---

### v1.0.0 - August 19, 2026

<h3 style="color:#EB6669">ADDED</h3>

* Initial release.

---
