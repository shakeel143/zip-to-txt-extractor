<div align="center">

<br/>

```
███████╗██╗██████╗     →    ████████╗██╗  ██╗████████╗
╚══███╔╝██║██╔══██╗         ╚══██╔══╝╚██╗██╔╝╚══██╔══╝
  ███╔╝ ██║██████╔╝            ██║    ╚███╔╝    ██║   
 ███╔╝  ██║██╔═══╝             ██║    ██╔██╗    ██║   
███████╗██║██║                 ██║   ██╔╝ ██╗   ██║   
╚══════╝╚═╝╚═╝                 ╚═╝   ╚═╝  ╚═╝   ╚═╝   
```

# 📦 ZIP → TXT Code Extractor

**Turn any ZIP of source code into a single, clean, AI-ready `.txt` file — 100% in your browser.**

[![Live Demo](https://img.shields.io/badge/🚀_Live_Demo-Try_It_Now-00e5a0?style=for-the-badge)](https://shakeel143.github.io/zip-to-txt-extractor/)
[![No Backend](https://img.shields.io/badge/🔒_No_Backend-Client--Side_Only-0075ff?style=for-the-badge)](#)
[![MIT License](https://img.shields.io/badge/📄_License-MIT-gray?style=for-the-badge)](#license)
[![Made with JSZip](https://img.shields.io/badge/Powered_by-JSZip-orange?style=for-the-badge)](https://stuk.github.io/jszip/)

<br/>

> *"You can't paste a ZIP into ChatGPT. Now you don't have to."*

<br/>

</div>

---

## 🧩 The Problem

Every developer has been there:

```
"Can you debug my project?"
"Sure, send the code."
"Here's the zip."
...opens zip...
📁 47 folders · 200 files · 6 hours of copy-pasting...
```

Whether you're sharing code with an AI assistant, doing a code review, handing off to a client, or just trying to document a codebase — **ZIP files are painful to work with**.

- ❌ You can't paste a `.zip` into ChatGPT or Claude
- ❌ Copy-pasting 200 files is soul-crushing
- ❌ Most online tools upload your files to a server (privacy risk)
- ❌ No universal tool existed — until now.

---

## ✅ The Solution

**ZIP → TXT Code Extractor** reads your ZIP entirely in the browser and produces a single beautifully formatted `.txt` file — every source file, organised by its full folder path.

```
============================================================
api/admin/create_user.php
============================================================
<?php
// your code here...


============================================================
config/database.php
============================================================
<?php
// your code here...
```

**One file. Every path. All your code. Ready to paste anywhere.**

---

## ✨ Features

| Feature | Details |
|---|---|
| 🌐 **100% Browser-based** | No install, no server, no uploads — runs entirely locally |
| 🗜️ **Multi-ZIP support** | Drop multiple ZIPs at once, get one combined output |
| 📁 **Smart path stripping** | Auto-strips redundant root folders so paths stay clean |
| 🔍 **40+ file types** | PHP, JS, TS, CSS, Python, SQL, YAML, Go, Rust, and more |
| 🚫 **Auto-skips junk** | Ignores binaries, `.DS_Store`, `.keep`, oversized files |
| 📊 **Live progress log** | Watch each file get extracted in real-time |
| ⚙️ **Configurable output** | Set custom output filename, toggle prefix stripping |
| 🔒 **Privacy-first** | Your files never touch any server — ever |

---

## 🚀 Quick Start

### Option 1 — Use the Web App (Zero setup)

**👉 [Open the Live Tool](https://shakeel143.github.io/zip-to-txt-extractor/)**

1. Drag & drop your `.zip` file(s) onto the page
2. Configure options (strip prefix, output filename)
3. Click **Extract & Download**
4. Get your `.txt` file — done in seconds ✅

### Option 2 — Run Locally

Just download and open in any browser. No web server needed.

```bash
git clone https://github.com/shakeel143/zip-to-txt-extractor.git
cd zip-to-txt-extractor

# macOS
open index.html

# Windows
start index.html

# Linux
xdg-open index.html
```

---

## 🎯 Perfect For

```
🤖  AI Assistants    →  Paste your full project into ChatGPT, Claude, or Gemini in one shot
👥  Code Reviews     →  Send a single readable file instead of a messy zip
📖  Documentation    →  Create a readable snapshot of a codebase at any point in time
🧑‍💼  Client Handoffs  →  Share clean, readable source with non-technical stakeholders
🔍  Quick Audits     →  Search your entire project with Ctrl+F in any text editor
🎓  Learning         →  Study open-source projects without setting up a dev environment
```

---

## 📁 Supported File Types

```
Web & Frontend  →  .php  .js  .jsx  .ts  .tsx  .html  .css  .scss  .sass  .vue  .svelte
Data & Config   →  .json  .yaml  .yml  .xml  .toml  .ini  .env  .cfg  .conf  .sql  .csv
Scripts         →  .py  .sh  .bash  .zsh  .rb  .pl  .bat  .ps1
Systems         →  .java  .kt  .go  .rs  .c  .cpp  .h  .cs  .swift
Docs            →  .md  .txt  .rst  .log  .htaccess  .gitignore  .properties
```

> Binary files, images, archives, and anything over **2 MB** are automatically skipped.

---

## 🔐 Privacy First

```
Your ZIP file
    │
    ▼
JSZip (runs in YOUR browser)
    │
    ├── Filter: text files only
    ├── Sort: alphabetically by path
    ├── Strip: common root prefix (optional)
    │
    ▼
Formatted .txt file — downloaded directly to your device
```

**Your files never leave your computer.** All processing happens client-side using the browser's built-in JavaScript engine. No data is sent to any server — not even a single byte.

---

## 🛠 How It Works

Under the hood, the tool uses [JSZip](https://stuk.github.io/jszip/) to:

1. **Read** your `.zip` files in the browser using the `FileReader` API
2. **Filter** entries to text/code files only (based on extension)
3. **Sort** entries alphabetically by full path
4. **Strip** the common root prefix from all paths (optional, toggleable)
5. **Decode** file content (UTF-8 with Latin-1 fallback for safety)
6. **Combine** everything into one structured `.txt` file
7. **Trigger** an instant browser download — no server involved

For **multiple ZIP files**, each archive gets a clearly labelled section header:

```
############################################################
# Archive: frontend.zip
############################################################

...all frontend files...

############################################################
# Archive: backend.zip
############################################################

...all backend files...
```

---

## ⚠️ Limitations

| Constraint | Value |
|---|---|
| Max file size per entry | 2 MB |
| Supported file types | Text/code only (no images or binaries) |
| Large projects | May take a few seconds in the browser — totally normal |
| Archives | `.zip` only (`.tar.gz` not supported yet) |

---

## 🤝 Contributing

Contributions are very welcome! Open a PR or suggest an idea via Issues.

Some things on the wishlist:

- [ ] `.tar.gz` archive support
- [ ] File tree preview before extraction
- [ ] Syntax-highlighted preview panel
- [ ] Copy-to-clipboard per file block
- [ ] Dark / light theme toggle
- [ ] Export as Markdown (with fenced code blocks)

```bash
git clone https://github.com/shakeel143/zip-to-txt-extractor.git
cd zip-to-txt-extractor

# All logic lives in a single file — easy to hack on:
# → index.html
```

---

## 📄 License

**MIT License** — free to use, modify, and distribute. See [`LICENSE`](LICENSE) for details.

---

<div align="center">

### Built by [Shakeel Ahmed Sanjrani](https://github.com/shakeel143)
*Android Developer · React · Firebase*

<br/>

**If this saved you time — pay it forward with a ⭐**

It takes one click and helps other developers find the tool.

<br/>

[![Try Live Demo](https://img.shields.io/badge/🚀_Try_the_Live_Demo-00e5a0?style=for-the-badge)](https://shakeel143.github.io/zip-to-txt-extractor/)
[![Report a Bug](https://img.shields.io/badge/🐛_Report_a_Bug-ff4d6d?style=for-the-badge)](https://github.com/shakeel143/zip-to-txt-extractor/issues)
[![Request a Feature](https://img.shields.io/badge/💡_Request_a_Feature-0075ff?style=for-the-badge)](https://github.com/shakeel143/zip-to-txt-extractor/issues)

<br/>

*Built for developers who are tired of dealing with ZIP files.*

</div>
