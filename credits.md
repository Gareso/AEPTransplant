## Credits & Licenses

---

AEP Transplant is built on some excellent open-source work. Thank you to everyone behind these projects.

| Project | What it does in AEP Transplant | License |
| ------- | ------------------------------ | ------- |
| [pdf.js](https://github.com/mozilla/pdf.js) by Mozilla | Draws [previews](features.md#previews) of PDF and Illustrator files | Apache 2.0 |
| [three.js](https://github.com/mrdoob/three.js) | Draws [previews](features.md#previews) of 3D models | MIT |
| [py-aep](https://github.com/forticheprod/py-aep) by Fortiche Production | Reads and writes After Effects project files | MIT |
| [attrs](https://github.com/python-attrs/attrs), [fontTools](https://github.com/fonttools/fonttools), [PyYAML](https://github.com/yaml/pyyaml) | Used by py-aep | MIT |
| [Python](https://www.python.org) | Runs the project reader | PSF License |
| [PyInstaller](https://pyinstaller.org) | Packages the project reader | GPL 2.0 with bootloader exception |

pdf.js also includes Adobe's character maps (BSD 3-Clause), Foxit fonts (BSD 3-Clause) and Liberation fonts (SIL Open Font License 1.1), used to display text in PDFs that don't embed their own fonts.

> The full license texts ship inside the extension, in `client/lib/THIRD_PARTY_NOTICES.txt`, with the pdf.js and three.js licenses beside their libraries in `client/lib/pdfjs/` and `client/lib/three/`.
