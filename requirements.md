# Data Quality Agent — requirements

## Runtime requirements

- A modern browser with JavaScript modules and React 18 support.
- Internet access while the page is open. The current prototype loads its UI libraries and fonts from CDNs.
- Serve `index.html` over HTTP rather than opening it with `file://`, because UI5 Web Components are ES modules.

## Browser libraries loaded by `index.html`

- React 18 production UMD: `https://unpkg.com/react@18/umd/react.production.min.js`
- ReactDOM 18 production UMD: `https://unpkg.com/react-dom@18/umd/react-dom.production.min.js`
- Babel Standalone: `https://unpkg.com/@babel/standalone/babel.min.js`
- UI5 Web Components modules: `https://cdn.jsdelivr.net/npm/@ui5/webcomponents/dist/Assets.js` and `Button.js`
- Fonts: DM Sans and Manrope from Google Fonts

The page is a static HTML prototype. It does not currently require npm, Python packages, a database, or an API key. The agent configuration stays in browser memory; connecting AI or processing uploaded data requires a backend.

## Supported upload

- CSV files only (`.csv`, `text/csv`)
- The page advertises a 100 MB limit. Server-side validation and CSV parsing are not implemented in this prototype.

