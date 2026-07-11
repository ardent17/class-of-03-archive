# CCHS Class of 2003 — Digital Archive

A retro, single-page web archive for browsing and reading class yearbooks and ephemera right in the browser. No backend, no build step — just vanilla JS, static HTML, and pure Y2K nostalgia.

## ✨ Features

- 📖 In-browser PDF reader — Click any cover to flip through the full document via [PDF.js](https://mozilla.github.io/pdf.js/). No downloads required.
- 💾 Remembers your page — Saves the last page you were on for each document, so you can pick up where you left off.
- 🖼️ Auto-generated covers — Renders the PDF's first page as its shelf cover automatically. Optional manual `cover_url` override per item.
- 📚 Organized shelves — Items grouped into customizable categories (`Yearbooks`, `Other Media`, etc.) with descriptions and “empty shelf” states.
- 🔍 Full reader toolbar:
  - Page navigation (`Prev` / `Next`), direct page jump, live page count, and “From Back” start option
  - Zoom in / out + Fit to Screen
  - 90° rotation for sideways scans
  - One-click Save PDF download link
- 🎨 Retro aesthetic — VT323 + Comic Sans, dashed borders, drop shadows, scrolling `<marquee>`, checkerboard background, and a glitter mouse trail.
- 🪧 Interactive shelf — Covers sit at random tilt angles and zoom up on hover for a tactile, browsable feel.
- 💬 Community guestbook — Embedded Chattable live chat ("Sign the Yearbook") for classmates to reconnect and share memories.
- 🔒 Privacy-conscious — `noindex, nofollow` meta tag, plus a built-in contact button (copies email to clipboard) for redaction/removal requests.
- ⚡ Zero dependencies to host — Static HTML; drop it on Neocities, GitHub Pages, or any static host. Just edit the `BOOKS` array to add content.

## 🚀 Quick Start

Drop your PDFs into a `files/` folder next to the HTML file.

Edit the `BOOKS` array:

```js
const BOOKS = [
  { title: "2003 Yearbook", author: "CCHS", category: "Yearbooks", pdf_url: "files/2003.pdf" },
];
```

(Optional) Adjust categories to add/rename shelves.

Open or upload — done.

Each entry supports: `title`, `author`, `category`, `pdf_url`, optional `color` (loading fallback), and optional `cover_url` (custom cover).

## 📝 TODO / Future Updates

- Additional yearbooks — Add more class years and editions as scans become available.
- More artifacts & ephemera — Prom programs, playbills, newspapers, sports programs, flyers, and other memorabilia.
- Deep links — Shareable URLs that open a specific artifact/page.
- Tagging & filtering — Filter book content by tags (`sports`, `clubs`, `seniors`, etc.).
- Full-text search inside PDFs — Leverage PDF.js text layers for in-document searching.
- Mobile reader polish — Improved touch gestures (swipe to turn pages, pinch-to-zoom).
- Accessibility pass — Keyboard navigation, ARIA labels, reduced-motion option for the glitter trail.

## 🙏 Credits

Built for the CCHS Class of 2003 as a community archive project. Engine adapted from the [Little Free Zine Library](https://littlefreezinelibrary.neocities.org/local).

This is a shared archive of class memories and ephemera. If you're pictured and want something removed or redacted, reach out via the contact button on the page.