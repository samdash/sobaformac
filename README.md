# SOBA Static Website

A dependency-free static landing/download site for SOBA.

## Files

```text
index.html
styles.css
script.js
assets/
  soba-brand.png
downloads/
  Soba.dmg             <-- put your release DMG here
```

## Add your SOBA DMG

Copy your **Developer ID signed + notarized** release DMG to:

```text
downloads/Soba-1.2.dmg
```

The Download button in `index.html` already points to that file.

If you want a versioned filename such as:

```text
Soba-1.2.0.dmg
```

change this line in `index.html`:

```html
href="downloads/Soba-1.0.dmg"
```

to:

```html
href="downloads/Soba-1.2.0.dmg"
```

## Customize before publishing

Search `index.html` for:

- `support@example.com`
- `Version 1.2`
- `Apple silicon`
- Privacy wording
- Download filename

You may also want to add:

- A real privacy-policy page
- A support page
- Release notes
- Minimum macOS version
- Intel/Universal build information if applicable
- SHA-256 checksum for the DMG

## Local preview

From this directory:

```bash
python3 -m http.server 8080
```

Then open:

```text
http://localhost:8080
```

## Hosting

This is plain static HTML/CSS/JS and can be hosted on:

- GitHub Pages
- Cloudflare Pages
- Netlify
- Vercel static hosting
- Amazon S3 / CloudFront
- Any ordinary web server

## Recommended production download

For direct distribution, use a final DMG that is:

- Signed with Developer ID Application
- Hardened Runtime enabled
- Notarized by Apple
- Stapled
- Tested with Gatekeeper on a separate Mac

## Public-site FAQ

The public FAQ in `index.html` is intentionally customer-facing and explains how to use SOBA. Deployment, notarization, DMG placement, and hosting instructions belong only in this README.

## Quick Capture examples

The website includes customer-facing SOBA examples for JSON, Image, PDF, and Address contextual actions using the supplied SOBA screenshots.

## Quick Capture showcase

The website now showcases six contextual SOBA workflows in a 2-column grid:

1. JSON
2. Image
3. PDF
4. Address
5. Unix timestamp
6. Terminal command

## Smart Actions and drag-to-edge

The site now includes customer-facing examples for Image, PDF, and Folder/Project contextual Actions, plus a drag-to-edge section explaining configurable right/left/top/bottom activation and dynamic actions based on item type.


## Newly reflected product features

The public site now documents:

- Keyboard-only navigation
- First-run onboarding / guided tour
- Undo for reversible destructive actions
- Optional iCloud sync for preferences and pins
- Focus Mode awareness
- Fuzzy shelf search

The Privacy and Terms pages were also updated to disclose the optional iCloud feature.

## Navbar and product mockups update

- Header now matches the requested layout: SOBA identity at left, navigation centered, and labeled Light/Dark control fixed at the top-right.
- Removed the header Download button to keep the top bar clean.
- The six Quick Capture examples are no longer raw screenshots. They are reconstructed, polished HTML/CSS representations based on the actual SOBA UI and preserve the real button/action names, including dropdown indicators.
- The reconstructed SOBA windows remain dark in both website themes so the product UI remains visually consistent.
