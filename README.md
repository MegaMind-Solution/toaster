# Toaster Tooltip 🍞

A lightweight, zero-dependency JavaScript solution that converts standard HTML `title` attributes into modern, floating toast-style tooltips.

## Features
- 🚀 **Zero Dependencies**: Pure Vanilla JS.
- 🌓 **Auto-Contrast**: Detects your page background and automatically applies High Contrast colors (Dark tooltip on Light pages, and vice versa).
- 📐 **Smart Positioning**: Stays on screen. Flips to the left or top if the cursor is near the edge.
- 🎨 **Fully Configurable**: Set your own fonts, radius, and colors via a simple setup object.
- ⚡ **Single Line**: Enforces single-line display for a clean UI look.

## Installation

1. Download `universal-tooltip.js` and `setup.js`.
2. Add them to your HTML file (place them at the bottom of `<body>` or in `<head>` with `defer`).

```html
<script src="path/to/setup.js"></script>
<script src="path/to/universal-tooltip.js"></script>
```

## Usage

Simply add a standard `title` attribute to any HTML element. The script handles the rest.

```html
<button title="This will become a floating toast!">Hover Me</button>
```

## Configuration (`setup.js`)

Edit `src/setup.js` to match your brand. Set values to `null` to use automatic defaults.

```javascript
window.UniversalTooltipConfig = {
    backgroundColor: null,      // Let script decide (Auto-Contrast)
    textColor:       null,      // Let script decide
    fontFamily:      "Arial",   // Custom Font
    fontSize:        "13px",
    borderRadius:    "4px"
};
```

## License
MIT License. Free to use in personal and commercial projects.
```

---

### 5. `.gitignore`
**Description:** Tells Git what not to upload.

```text
.DS_Store
node_modules/
.vscode/
dist/
```

---

### How to Upload to GitHub

1.  **Create a folder** on your PC named `universal-tooltip`.
2.  **Create the files** listed above inside that folder.
3.  Open your terminal/command prompt in that folder.
4.  Run these commands:

```bash
git init
git add .
git commit -m "Initial commit: Universal Tooltip Setup"
git branch -M main
# Replace URL below with your actual GitHub repository URL
git remote add origin https://github.com/YOUR_USERNAME/universal-tooltip.git
git push -u origin main
```
