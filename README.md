# Universal Toaster

A lightweight, zero-dependency JavaScript solution that converts standard HTML `title` attributes into modern, floating, single-line "toast" style tooltips.

## Features

- **Universal Compatibility:** Works on any website, instantly converting all native tooltips.
- **Smart Positioning:** Keeps tooltips on screen. If near the right edge, it flips left. If near the bottom, it flips up.
- **Auto-Contrast:** Automatically detects if the page background is Light or Dark and adjusts the tooltip color for perfect readability.
- **Single Line:** Enforces a clean, single-line design (no text wrapping).
- **Customizable:** Configure fonts, radius, and colors via a simple setup object.

## Installation

1. Download the `src/toaster.js` file.
2. Include it at the bottom of your HTML body.

```html
<script src="path/to/src/toaster.js"></script>
```

## Configuration

You can customize the appearance by defining the `window.UniversalToasterConfig` object **before** loading the script.

```html
<script>
    window.UniversalToasterConfig = {
        // COLORS
        // Set to null to use Auto-Contrast (Recommended)
        backgroundColor: null,   // e.g., "#333333"
        textColor:       null,   // e.g., "#ffffff"
        
        // FONTS & SIZE
        fontFamily:      "inherit", // Uses your website's font
        fontSize:        "13px",
        fontWeight:      "500",
        
        // VISUALS
        borderRadius:    "6px",
        padding:         "8px 12px"
    };
</script>

<script src="src/toaster.js"></script>
```

## How it works

The script listens for `mouseover` events. When you hover over an element with a `title` attribute:

1. It saves the title text.
2. It removes the `title` attribute (preventing the ugly browser default tooltip).
3. It displays the text in a fixed `div` that follows your mouse cursor.
4. It calculates viewport collisions to ensure the tooltip never goes off-screen.

## License

MIT
```
