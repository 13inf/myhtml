# MyHtml Editor

A lightweight, single-file HTML visual editor for quick text and color edits on presentations, resumes, infographics, and other single-page or multi-page HTML files.

## Background

MyHtml is a second-stage development based on the open-source project [htmltool2](https://github.com/caoxianqi/htmltool2) by [caoxianqi](https://github.com/caoxianqi). The entire development process was completed with AI assistance. The original project provided the core iframe preview, text editing, and color panel features. MyHtml builds on this foundation with added undo/redo, image insertion and manipulation, page scroll navigation, and smart color swatch toggling.

## Features

### Core Editing
- **Single-file app**: open `MyHtml.html` and start editing — no installation needed
- **Fully local**: all operations run in the browser, no file uploads
- **Scripts enabled by default**: JavaScript runs automatically, supporting animated and interactive pages
- **Text editing**: enable edit mode and click any text to modify it; pasted content is auto-stripped to plain text
- **Color editing**: click empty space inside an element to open the color panel with background/text color, HEX input, and preset swatches
- **Smart swatch toggle**: presets apply to background or text color depending on which input was last focused

### Undo / Redo
- `Ctrl+Z` to undo, `Ctrl+Shift+Z` or `Ctrl+Y` to redo
- Up to 50 history steps
- Works for both text edits and color changes
- Preserves edit mode and scroll position across undo/redo

### Page Scrolling
- **Mouse wheel**: scroll anywhere to navigate pages
- **Arrow keys**: `↑` `↓` `←` `→` to scroll
- **Page Up / Page Down**: fast page navigation
- **Ctrl+Home / Ctrl+End**: jump to top / bottom
- In edit mode, arrow keys auto-detect: move cursor when inside text, scroll when in empty space

### Image Insertion
- Click the image button in the toolbar to insert a local image
- Images are automatically converted to embedded data URLs
- **Free drag**: hold and drag to reposition
- **Corner resize**: drag corner handles to adjust size
- **Slide-aware**: images insert into the active slide; hidden when switching pages, shown when switching back
- Press `Delete` or `Backspace` to remove the selected image
- Press `Esc` to deselect

### File Operations
- Drag and drop `.html` / `.htm` files into the window to open
- Images are automatically inlined as data URLs when saving
- Real-time modification status indicator

## Quick Start

Open in a browser:

```
MyHtml.html
```

Click the "Open" button or drag an HTML file into the window.

If the HTML depends on relative-path resources, start a local server:

```bash
python -m http.server 8765
```

Then visit `http://127.0.0.1:8765/MyHtml.html`

## Keyboard Shortcuts

| Shortcut | Action |
| --- | --- |
| `Ctrl` + `S` | Save |
| `Ctrl` + `Z` | Undo |
| `Ctrl` + `Shift+Z` / `Ctrl+Y` | Redo |
| `↑` `↓` `←` `→` | Scroll page |
| `Page Up` / `Page Down` | Fast scroll |
| `Ctrl` + `Home` / `End` | Jump to top / bottom |
| `Delete` / `Backspace` | Delete selected image |
| `Esc` | Close panel / deselect |

## Relationship with htmltool2

The core editing architecture of MyHtml (iframe preview, contentEditable text editing, color panel, overlay highlight system) originated from [htmltool2](https://github.com/caoxianqi/htmltool2). Built on top of this foundation with AI-assisted development, MyHtml adds:

- Undo / redo (50 history steps)
- Image insertion, drag-to-move, corner resize, and deletion
- Mouse wheel page scrolling, arrow key navigation, Page Up/Down
- Smart color swatch toggling
- Slide-aware page detection
- Dark theme UI

## Project Structure

```
MYhtml/
├── MyHtml.html             # Main editor file
├── test.html               # Example test page
├── README.md               # Chinese documentation
├── README_EN.md            # English documentation
├── LICENSE                 # MIT License (Copyright (c) 2026 Bin)
└── THIRD_PARTY_NOTICES.md  # Third-party notices
```

## Browser Compatibility

Latest Chrome or Edge is recommended. Safari and Firefox are supported, but editing behavior may vary.

## Acknowledgments

- [htmltool2](https://github.com/caoxianqi/htmltool2) by [caoxianqi](https://github.com/caoxianqi) — the foundational architecture that MyHtml is built upon, MIT License
- AI-assisted development — code implementation and feature development were completed with AI assistance

## License

MIT License — see [LICENSE](LICENSE)

Third-party notices: [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)
