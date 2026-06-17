# DevicePreview Studio

A frontend-only viewport preview tool designed to run on a phone while previewing how a URL renders in desktop, tablet, or phone viewport dimensions.

## Usage

Open `index.html` directly in a browser, or serve the directory with any static server.

```bash
python3 -m http.server 8080
```

Then open `http://localhost:8080`.

## Notes

- The default preset is `Full HD Monitor`, so mobile users can paste a URL and immediately inspect the desktop layout.
- Some websites block iframe embedding with `X-Frame-Options` or CSP `frame-ancestors`. DevicePreview Studio shows a warning and an open-in-new-tab action when this is likely.
- Static browser pages cannot truly spoof `devicePixelRatio` or the iframe user agent. Presets display those values as QA metadata while the iframe uses the selected CSS viewport size.
- Shareable links support `?url=...&device=...`, plus custom `w` and `h` values.
