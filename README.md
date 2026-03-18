# Universal Toaster

A lightweight, zero-dependency JavaScript library that turns standard HTML `title` attributes into **Rich Text** floating tooltips. 

**New in v3.0:** Support for Colors, Backgrounds, Custom Fonts (Google Fonts), Font Weights, and Text Truncation inside the tooltip!

## ✨ Features

- **Rich Text Engine:** Use simple shortcodes to style specific parts of the text.
- **Auto-Fetch Fonts:** Use `&fn=FontName;` and it automatically loads it from Google Fonts.
- **Smart Positioning:** Keeps tooltips on screen (flips edges).
- **Mobile Optimized:** A separate positioning engine for small screens centers the tooltip and clamps it to the viewport, ensuring it's always fully visible.
- **Auto-Contrast:** Detects Dark/Light backgrounds and adjusts colors automatically.
- **Safety:** Sanitizes HTML to prevent XSS while allowing styling.
- **Stability:** Auto-closes on Scroll, Click, or Tab Switch.

## 📦 Installation

1.  Download the [`src/toaster.js`](https://gitfolderdownloader.github.io/api/?=https://github.com/MegaMind-Solution/toaster/tree/main/src&name=Universal%20Toaster) Or Use hosted script
2.  Add it to the bottom of your `<body>`.

```html
<script src="src/toaster.js"></script>
```

```html
<script src="https://cdn.jsdelivr.net/gh/MegaMind-Solution/toaster@main/src/toaster.js"></script>
```

## 🎨 Rich Text Syntax

You can use these codes inside any `title="..."` attribute.

| Feature | Syntax | Example |
| :--- | :--- | :--- |
| **Text Color** | `&fz=Value; ... &fz;` | `&fz=12px;Error&fz;` |
| **Text Color** | `&cl=Value; ... &cl;` | `&cl=red;Error&cl;` |
| **Background** | `&bgcl=Value; ... &bgcl;` | `&bgcl=yellow;Highlight&bgcl;` |
| **Font Family** | `&fn=Name; ... &fn;` | `&fn=Roboto;Hello&fn;` |
| **Font Weight** | `&fw=Weight; ... &fw;` | `&fw=bold;Bold&fw;` |
| **Truncate** | `&chr=Limit; ... &chr;` | `&chr=10;VeryLongText&chr;` |

### Examples

**1. Size, Colors & Highlights**
```html
<button title="This is &fz=12px;&cl=red;Important&cl; and this is &bgcl=yellow;Highlighted&bgcl;&fz;">Hover Me</button>
```

**2. Custom Fonts (Google Fonts)**
*The script automatically adds the `<link>` tag for the font.*
```html
<button title="&fn=Pacifico;Start with a cool font&fn; and end normal.">Hover Me</button>
```

**3. Character Limit**
*Useful for previewing long database content.*
```html
<span title="Preview: &chr=20;This is a very long description that will be cut off&chr;">Hover for preview</span>
```

## ⚙️ Global Configuration (Optional)

Place this **before** loading the script to set global defaults.

```html
<script>
    window.UniversalToasterConfig = {
        // COLORS (Set to null for Auto-Contrast)
        backgroundColor: null, 
        textColor:       null,
        
        // VISUALS
        borderRadius:    "6px",
        fontSize:        "13px",
        fontFamily:      "inherit", // Default font
        padding:         "8px 12px",
        boxShadow:       "0 4px 12px rgba(0,0,0,0.2)"
    };
</script>
```

## 🛡 Security Note

The script includes an HTML sanitizer. It escapes raw HTML tags (like `<script>`) to prevent XSS attacks, while properly parsing the custom `&cmd=val;` syntax.

## License

The Project is Creaate Under MIT License EveryOne Can Modify and Improve this
