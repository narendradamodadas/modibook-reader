LIVE READER: https://narendradamodadas.github.io/modibook-reader/

Use the GitHub Pages URL above to read the book as a website. The repo page only shows source files.

# Modibook static reader

This folder contains a static website generated from `modibook.pdf`.

Contents:
- `index.html` — table of contents / page list
- `pages/` — one HTML page per scanned book page
- `images/` — rendered scan images
- `data/` — OCR + English translation JSON per page
- `styles.css` — site styling
- `book.json` — combined metadata

Local preview:

```bash
cd modibook-site
python3 -m http.server 8765
```

Then open:
- `http://127.0.0.1:8765/`

GitHub Pages deployment:
1. Create a GitHub repo.
2. Upload the contents of this folder to the repo root.
3. Add the empty file `.nojekyll`.
4. In GitHub repo settings, enable Pages from the `main` branch `/ (root)`.

Notes:
- The book is scanned Gujarati OCRed with Tesseract.
- English text is machine-translated and may contain OCR/translation errors.
- Each page keeps the original scan side-by-side with OCR and English text for traceability.
