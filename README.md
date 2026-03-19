# Universal Toaster

A lightweight, zero-dependency JavaScript library that turns standard HTML `title` attributes into **Rich Text** floating tooltips.Designed for modern websites, browser extensions, and single-page applications (SPAs).



## ✨ Key Features

- **Auto-Fetch Fonts:** Use `&fn=FontName;` and it automatically loads it from Google Fonts.
- **Smart Positioning:** Keeps tooltips on screen (flips edges).
- **Mobile Optimized:** A separate positioning engine for small screens centers the tooltip and clamps it to the viewport, ensuring it's always fully visible.
- **Auto-Contrast:** Detects Dark/Light backgrounds and adjusts colors automatically.
- **Safety:** Sanitizes HTML to prevent XSS while allowing styling.
- **Stability:** Auto-closes on Scroll, Click, or Tab Switch.
- **API-Driven:** Control the library with `init`, `destroy`, and `updateConfig` methods.
- **Web App Ready:** `MutationObserver` automatically detects dynamically added content.
- **Shadow DOM Support:** Works seamlessly inside web components and modern frameworks.
- **Rich Content Engine:** Style tooltips with lists, links, icons, images, custom fonts, and more.
- **Interactive Tooltips:** Links inside a tooltip make it "hoverable" so they can be clicked.


## 📦 Installation

1.  Download the [`src/toaster.js`](https://gitfolderdownloader.github.io/api/?=https://github.com/MegaMind-Solution/toaster/tree/main/src&name=Universal%20Toaster) Or Use js deliver version
2.  Add it to the bottom of your `<body>`.

```html
<script src="src/toaster.js"></script>
```

```html
<script src="https://cdn.jsdelivr.net/gh/MegaMind-Solution/toaster@main/src/toaster.js"></script>
```

## 🎨 Rich Text Syntax

You can use these codes inside any `title="..."` attribute.

| Feature            | Syntax                   | Example                        |
| :----------------- | :----------------------- | :----------------------------- |
| **List Item**      | `&li=symbol;Text&li;`    | `&li=$;First Point&li;`        |
| **Link**           | `&lnk=url;Text&lnk;`     | `&lnk=//google.com;Go&lnk;`    |
| **Icon**           | `&icon=name;`            | `&icon=warning; Warning!`      |
| **Image**          | `&img=url;`              | `&img=path/to/img.png;`        |
| **Divider**        | `&hr;`                   | `Line 1&hr;Line 2`             |
| **Width Override** | `&w=value;`              | `&w=300px;Wider content...`    |
| **Text Color**     | `&cl=color;Text&cl;`     | `&cl=red;Error&cl;`            |
| **Background**     | `&bgcl=color;Text&bgcl;` | `&bgcl=yellow;Highlight&bgcl;` |

### Examples

**1. Size, Colors & Highlights**

```html
<button title="This is &fz=12px;&cl=red;Important&cl; and this is &bgcl=yellow;Highlighted&bgcl;&fz;">Hover Me</button>
```

**2. Custom Fonts (Google Fonts)**
_The script automatically adds the `<link>` tag for the font._

```html
<button title="&fn=Pacifico;Start with a cool font&fn; and end normal.">Hover Me</button>
```

**3. Character Limit**
_Useful for previewing long database content._

```html
<span title="Preview: &chr=20;This is a very long description that will be cut off&chr;">Hover for preview</span>
```

## ⚙️ Global Configuration (Optional)

Place this **before** loading the script to set global defaults.

```html
<script>
  // Initialize with default settings
  UniversalToaster.init();

  // Or, initialize with custom options
  UniversalToaster.init({
    delay: 200, // Wait 200ms before showing
    fontSize: "14px",
    borderRadius: "8px",
    backgroundColor: null, // e.g. "#333"
    textColor: null, // e.g. "#fff"
    // TYPOGRAPHY
    fontFamily: "inherit", // Uses page font
    fontSize: "13px",
    fontWeight: "500",
    // SHAPE
    borderRadius: "6px",
    padding: "8px 12px",
    boxShadow: "0 4px 12px rgba(0,0,0,0.15)",
  });
</script>
```

### API Methods

- **`UniversalToaster.init(config)`**: Starts the library. `config` is an optional object.
- **`UniversalToaster.destroy()`**: Safely removes all listeners and elements. Essential for SPAs when components unmount.
- **`UniversalToaster.updateConfig(config)`**: Updates the global configuration on the fly.

## 🎨 Rich Text Syntax

Use these shortcodes inside any `title="..."` attribute.

## License

The Project is Creaate Under MIT License EveryOne Can Modify and Improve this
