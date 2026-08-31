## Changelog

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
