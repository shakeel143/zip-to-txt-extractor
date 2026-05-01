<div align="center">

# 📦 ZIP → TXT Code Extractor

### *Instantly turn any ZIP of source code into a single, readable text file — right in your browser.*

[![Live Demo](https://img.shields.io/badge/🚀_Live_Demo-Try_it_Now-00e5a0?style=for-the-badge)](https://YOUR-USERNAME.github.io/zip-to-txt)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](LICENSE)
[![No Install](https://img.shields.io/badge/No_Install-100%25_Browser-ff6b6b?style=for-the-badge)]()
[![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-brightgreen?style=for-the-badge)](CONTRIBUTING.md)

<br/>

![ZIP to TXT Demo](https://raw.githubusercontent.com/YOUR-USERNAME/zip-to-txt/main/assets/demo.gif)

</div>

---

## 🧩 The Problem

Every developer has been here:

> *"Can you review my project?"*
> *"Sure, send it over."*
> *"Here's the zip."*
> *...opens zip... 47 folders... 200 files... 3 hours later...*

Whether you're sharing code with **AI assistants** (like ChatGPT or Claude), doing a **code review**, sending your project to a **freelancer**, or just trying to **document a codebase** — working with ZIP files is painful.

You can't paste a ZIP into an AI chat. You can't email a folder structure. You can't quickly search across 200 files scattered across nested directories.

**There was no simple, universal tool to solve this.** Until now.

---

## ✅ The Solution

**ZIP → TXT Code Extractor** reads your ZIP file entirely in the browser and produces a single, beautifully formatted `.txt` file containing every source file — organised by its full folder path.

```
============================================================
api/admin/create_user.php
============================================================
<?php
// your code here...


============================================================
config/db.php
============================================================
<?php
// your code here...
```

One file. Every path. All your code. Ready to paste anywhere.

---

## ✨ Features

| Feature | Details |
|---|---|
| 🌐 **100% Browser-based** | No install, no server, no uploads — everything runs locally |
| 🗜️ **Multi-ZIP support** | Drop multiple ZIPs and get one combined output |
| 📁 **Smart path display** | Auto-strips redundant root folders so paths stay clean |
| 🔍 **Smart file filtering** | Includes PHP, JS, JSX, TS, CSS, SQL, Python, and 40+ text formats |
| 🚫 **Auto-skips junk** | Ignores binaries, `.DS_Store`, `.keep`, files over 2MB |
| ⚙️ **Configurable** | Toggle prefix stripping, set custom output filename |
| 📋 **Live processing log** | See every file as it's extracted in real-time |
| 🐍 **Python CLI too** | Power users get a command-line version for automation |

---

## 🚀 Quick Start

### Option 1 — Use the Web App (Recommended)

👉 **[Open the Live Tool](https://YOUR-USERNAME.github.io/zip-to-txt)**

1. Drag & drop your `.zip` file(s) onto the page
2. Click **Extract & Download**
3. Get your `.txt` file — done in seconds

### Option 2 — Run Locally

Just download `index.html` and open it in any browser. No web server needed.

```bash
git clone https://github.com/YOUR-USERNAME/zip-to-txt.git
cd zip-to-txt
open index.html   # macOS
# or double-click index.html on Windows/Linux
```

### Option 3 — Python CLI

For automation, CI pipelines, or large codebases:

```bash
# Single zip
python zip_to_txt.py myproject.zip

# Multiple zips → one combined output
python zip_to_txt.py frontend.zip backend.zip -o full_project.txt

# Keep the root folder name in paths
python zip_to_txt.py archive.zip --no-strip-prefix
```

**Requirements:** Python 3.10+ · No external packages needed

---

## 🎯 Perfect For

- 🤖 **Sharing code with AI** — Paste your entire project into ChatGPT, Claude, Gemini or any LLM in one shot
- 👥 **Code reviews** — Send a single readable file to a reviewer instead of a zip
- 📖 **Documentation** — Create a readable snapshot of a codebase at a point in time
- 🧑‍💼 **Client handoffs** — Share readable source with non-technical stakeholders
- 🔍 **Quick audits** — Search across an entire project with Ctrl+F in any text editor
- 🎓 **Learning** — Study open-source projects without setting up a dev environment

---

## 📁 Supported File Types

The tool extracts all common source and config file types:

```
Web       → .php .js .jsx .ts .tsx .html .css .scss .vue .svelte
Data      → .json .yaml .yml .xml .toml .env .sql .csv
Scripts   → .py .sh .bash .rb .pl .bat .ps1
Systems   → .java .kt .go .rs .c .cpp .h .cs .swift
Docs      → .md .txt .rst .log .gitignore .htaccess
```

Binary files, images, archives, and anything over **2 MB** are automatically skipped.

---

## 🔐 Privacy First

> **Your files never leave your computer.**

The web app uses the browser's built-in [JSZip](https://stuk.github.io/jszip/) library. All processing happens entirely client-side. No data is sent to any server.

---

## 🛠️ How It Works

```
Your ZIP file
     │
     ▼
JSZip (browser) / zipfile (Python)
     │
     ├── Filter: text files only
     ├── Sort: alphabetically by path  
     ├── Strip: common root prefix (optional)
     │
     ▼
Formatted .txt output

  ════════════════════
  api/admin/login.php
  ════════════════════
  <?php ...
```

---

## 🤝 Contributing

Contributions are very welcome! Here are some ideas:

- [ ] Add syntax highlighting in the preview
- [ ] Support `.tar.gz` archives
- [ ] Add a file tree preview before extraction
- [ ] Dark/light theme toggle
- [ ] Copy-to-clipboard button per file

**To contribute:**

```bash
git clone https://github.com/YOUR-USERNAME/zip-to-txt.git
cd zip-to-txt
# make your changes to index.html or zip_to_txt.py
# open a pull request!
```

---

## 📄 License

MIT License — free to use, modify, and distribute. See [LICENSE](LICENSE) for details.

---

<div align="center">

**Built for developers, by a developer who was tired of dealing with ZIP files.**

⭐ If this saved you time, consider starring the repo — it helps others find it!

[🚀 Try the Live Demo](https://YOUR-USERNAME.github.io/zip-to-txt) · [🐛 Report a Bug](https://github.com/YOUR-USERNAME/zip-to-txt/issues) · [💡 Request a Feature](https://github.com/YOUR-USERNAME/zip-to-txt/issues)

</div>
