# GrapeSite — Local Studio

A fully local visual website builder powered by [GrapesJS](https://grapesjs.com). No server, no account, no cloud — everything runs in your browser and saves to localStorage.

Written entirely by **OpenCode** (AI coding agent) during a single session.

## Features

### Multi-page editing

Create, rename, reorder, and delete pages from the left panel. Each page has its own independent HTML, CSS, and JavaScript. Switch between pages instantly without losing any work.

- **Home**, **About**, and **Contact** pages are created by default
- Unlimited pages
- Each page renders as a standalone file on export

### Symbols

Turn any component into a reusable symbol. Edit the symbol once and every instance updates automatically across all pages.

- Create from any selected component
- Rename and delete symbols from the Symbols panel
- Instances remain editable individually while staying linked to the source
- Symbols persist in the project file

### Blocks & components

Drag pre-built blocks onto the canvas or create your own. The built-in blocks library includes layout, basic, and text components.

### Styling

Full CSS editing through the Styles panel — selectors, layout, typography, spacing, borders, backgrounds, and more. Styles are scoped per page by default.

### Page Settings

Click the gear icon on any page to configure per-page metadata:

| Field | Purpose |
|---|---|
| **Name** | Page name shown in the editor and used for the exported filename |
| **Title** | Browser tab title (`<title>` tag) |
| **Description** | Meta description for SEO |
| **Favicon** | URL to a favicon file |
| **Keywords** | Comma-separated meta keywords |
| **Social title** | Open Graph title for social sharing |
| **Social image** | Open Graph image URL |
| **Social description** | Open Graph description |
| **Custom HTML head** | Raw HTML injected before `</head>` (analytics, fonts, etc.) |
| **Custom HTML body** | Raw HTML injected before `</body>` (scripts, widgets, etc.) |

### Project import & export

Save the entire project — every page, symbol, asset, style, and data source — as a single `.json` file. Load it back anytime to continue editing.

- **Export**: `Project (.json)` button in the Export dialog
- **Import**: drag in a `.json` or `.gjs` file through the Import dialog

### Website export

Export the site as a self-contained `.zip` archive:

- `index.html` for the first page
- `{page-name}.html` for every other page
- Each file includes all HTML, CSS, and JavaScript inline — no external dependencies
- Page Settings metadata (title, description, OG tags, custom head/body) is injected into every exported file

### Preview

Click the eye icon to enter preview mode and interact with the site as a visitor would. Use **Publish** to see a standalone preview of the current page in an iframe.

### Undo / redo

Full undo and redo history via the toolbar buttons or `Ctrl+Z` / `Ctrl+Shift+Z`.

### Autosave

Your project is saved to the browser's localStorage automatically on every change. Press `Ctrl+S` to force a save at any time.

### Device preview

Switch between Desktop, Tablet, and Mobile views from the top bar to check responsive layouts.

## Getting started

### Prerequisites

- [Node.js](https://nodejs.org) (for the dev server, any recent version)
- A modern browser (Chrome, Firefox, Edge, Safari)

### Install & run

```bash
git clone https://github.com/Mehran-user/grapesjs-studio-local.git
cd grapesjs-studio-local
npm install
npm start
```

Then open **http://localhost:8099** in your browser.

### What you need to know

- **No backend** — the app is a single `index.html` file plus `styles.css`. Everything else is loaded from `node_modules` at runtime.
- **No database** — all data lives in the browser's localStorage under the key `gjsProject`. Clearing browser data will erase your project (so export regularly).
- **No network** — once loaded, the app works fully offline.

## Project structure

```
.
├── index.html          Main app — editor init, panels, import/export, page settings
├── styles.css          Dark theme, custom panels, modal, rail, tooltip styles
├── package.json        Dependencies (grapesjs, jszip)
├── LICENSE             GPL-3.0
└── README.md
```

## Keyboard shortcuts

| Shortcut | Action |
|---|---|
| `Ctrl+S` | Save project |
| `Ctrl+Z` | Undo |
| `Ctrl+Shift+Z` | Redo |
| `Tab` | Switch between Plan and Build mode |
| `Escape` | Close modal / cancel |

## Tech stack

- **[GrapesJS](https://grapesjs.com)** v0.22.16 — open-source visual editor framework
- **[JSZip](https://stuk.github.io/jszip/)** — in-browser ZIP creation for website export
- **Vanilla JS** — no framework, no build step, no bundler

## License

[GPL-3.0](LICENSE)

## Credits

Built by **OpenCode** — an open-source AI coding agent by [Anomaly](https://anoma.ly). The entire application (HTML, CSS, JavaScript, symbols system, multi-page architecture, project import/export, page settings, and this README) was generated through natural language conversation in a single session.
