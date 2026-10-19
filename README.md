# Zenith 2026 — Live Scoring Console

Plain HTML/CSS/JS project — no framework, no build step, no backend.

## Structure
```
zenith-2026/
├── index.html      # markup, links css/style.css and js/app.js
├── css/
│   └── style.css   # all styling (pastel red + black theme, Times New Roman)
└── js/
    └── app.js      # all app logic (leaderboard, faceoff, reveal, upload parsing)
```

## Run locally in VS Code
1. Open this folder in VS Code (`File > Open Folder`).
2. Install the **Live Server** extension (if you don't have it).
3. Right-click `index.html` → **Open with Live Server**.
   (Or just double-click `index.html` to open it directly in a browser — it works either way.)

## External dependencies
Two libraries are loaded via CDN `<script>` tags in `index.html` (no install needed, just needs internet at runtime):
- [SheetJS / xlsx](https://cdnjs.com/libraries/xlsx) — parses uploaded Excel/CSV files
- [pdf.js](https://cdnjs.com/libraries/pdf.js) — extracts text from uploaded PDFs

## Deploying
Since it's fully static, you can drop this folder as-is onto any static host:
- **GitHub Pages**: push this folder to a repo, enable Pages on the `main` branch.
- **Netlify / Vercel**: drag-and-drop the folder, or connect the repo — no build command needed.
- **Any plain web server / shared hosting**: just upload the three files/folders.

## Where to make changes
- Colors, fonts, spacing → `css/style.css` (all custom properties are at the top under `:root`)
- Seed/sample teams, round labels, upload-parsing logic, faceoff/reveal behaviour → `js/app.js`
- Page structure/text (tab labels, section headings) → `index.html`
