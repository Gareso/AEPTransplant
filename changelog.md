## Changelog

---

### v1.1.0 - 2026

<h3 style="color:#EB6669">ADDED</h3>

* **Layer import.** Open any comp from the asset tree and pick individual layers out of it instead of taking the whole comp. See [Layer Import](features.md#layer-import).
* **Layer targets.** Point a comp's imported layers at a comp that already exists in your project, and they are copied into it instead of arriving in the comp they came from.
* **Dependency confirmation.** Before importing layers, the panel lists what else has to come with them (parent chains, track mattes, layers used by effects and expressions) and offers **Include Dependencies** or **Selected Layers Only**.
* **Drag and drop.** Drop an `.aep`, `.psd`, `.psb` or `.ai` straight onto the panel to load it.

<h3 style="color:#EB6669">FIXED</h3>

* The **Copy to Project** prompt for external assets no longer stays silent for projects saved directly to the Desktop or another everyday folder, where the whole home folder was being treated as "inside the project".
* Illustrator and Photoshop files imported as individual layers are now included in that same external-asset check, and copying one relinks the imported layers to the copy.

---

### v1.0.0 - 2026

<h3 style="color:#EB6669">ADDED</h3>

* Initial release.

---
