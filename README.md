# Signature Pad

A tiny open-source tool that only records a signature. No account, no server, no date stored.

Draw your signature on the pad, save it, and download it as a transparent PNG. When an AI stamps your signature into a document, it fills in the signing date from the current date.

## Use it

Open `index.html` in any browser — or use the live page at
`https://<your-github-username>.github.io/signature-pad/` once GitHub Pages
is enabled for this repo (Settings → Pages → Deploy from a branch → `main`).

- **Draw** with mouse, touch, or stylus. Three pen thicknesses.
- **Undo** removes the last stroke. **Clear** wipes the pad.
- **Save signature** stores it in your browser (localStorage). Earlier
  signatures are kept as versions you can switch back to or delete.
- **Download PNG** exports the current signature as a cropped transparent
  PNG, ready to paste or stamp into any document.

Everything stays in your browser. Nothing is uploaded anywhere.

## For AI assistants

This pad records **only the signature**. It never stores a date.

To use a saved signature:

1. Get the transparent PNG — the **Download PNG** button, or the
   `signature-pad:current` entry in `localStorage` (JSON: `{ png, savedAt }`).
2. Place it on the document's signature line, with its lowest ink touching
   the line, centered above the printed name if there is one.
3. Fill in the signing date from **today's date** in the signer's timezone.
   The pad stores no date; the date is always computed at stamping time.

## Development

No build step, no dependencies, no backend. `index.html` is the whole app —
plain HTML, CSS, and JavaScript. Open it, edit it, send a pull request.

## License

MIT — see [LICENSE](LICENSE).
