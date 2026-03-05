# Universal Toaster 🍞

A lightweight, zero-dependency JavaScript library that instantly modernizes your website's tooltips. It converts standard HTML `title` attributes into sleek, floating, single-line toast notifications that follow the mouse.

## 🚀 Features

*   **Universal:** Works on `div`, `span`, `a`, `button`, `input`—anything with a `title` attribute.
*   **Smart Positioning:** Viewport collision detection ensures tooltips never fly off-screen. (Flips Left/Up near edges).
*   **Auto-Theme:** Automatically detects the page background brightness and adjusts tooltip colors for high contrast (Dark on Light / Light on Dark).
*   **Single Line:** Enforces a clean `white-space: nowrap` UI.
*   **Zero Config:** Works out of the box, or fully customizable via JS.

## 📦 Installation

1.  Download the `src/toaster.js` file.
2.  Or use hosted file
3.  Link it at the end of your HTML `<body>`.

```html
<script src="src/toaster.js"></script>
```
```html
<script src="https://megamind-solution.github.io/toaster/src/toaster.js"></script>
```

## ⚙️ Configuration (Optional)

You can customize the appearance by defining a global config object **before** loading the script.

```html
<script>
    window.UniversalToasterConfig = {
        // COLORS
        // Set to null to allow Auto-Contrast (Recommended)
        backgroundColor: null,   // e.g. "#333"
        textColor:       null,   // e.g. "#fff"
        
        // TYPOGRAPHY
        fontFamily:      "inherit", // Uses page font
        fontSize:        "13px",
        fontWeight:      "500",
        
        // SHAPE
        borderRadius:    "6px",
        padding:         "8px 12px",
        boxShadow:       "0 4px 12px rgba(0,0,0,0.15)"
    };
</script>
```

## 🛠 Usage

Just add a standard `title` attribute to any HTML element.

```html
<button title="Save changes to database">Save</button>
<a href="#" title="Go to Home Page">Home</a>
```

## 📄 License

MIT License. Feel free to use in personal and commercial projects.
