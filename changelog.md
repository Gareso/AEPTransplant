## Changelog

---

### v1.1.5 - in progress

<h3 style="color:#EB6669">ADDED</h3>

* **Folder import:** folders tick like anything else. Checking one takes everything inside it, all the way down, which beats hunting through a long list of comps one row at a time. See [Folder Import](features.md#folder-import).
* **One destination for a whole folder:** give a folder a target and its entire branch travels there together, structure intact. Whether it merges into the folder you picked or arrives nested inside it depends on its own name, and the row tells you which before you import.

<h3 style="color:#EB6669">CHANGED</h3>

* **Duplicates are found wherever they live:** aiming something at a folder now checks the whole project for an item of that name, not just the folder it is headed for, so you are asked about a comp you already have somewhere else instead of quietly getting a second copy. The prompt names the folder that copy sits in, and whatever you choose, the incoming item stays where you aimed it.
* **Tidier rows:** the change dot moved to its own column down the left edge, so the marks line up instead of stepping in and out with each level, and rows no longer shift or grow when you select them.

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
