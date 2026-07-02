# AkabiLife — Clarity for better decisions

A private, in-browser financial health check and document redactor.

- **Financial Health Check** — answer ~30 quick questions and get a benchmarked report (52 US metros with cost-of-living adjustment, age-band peer benchmarks, KPIs, comparison bars, scorecard, and a ranked action plan).
- **Document Redactor** — strip PII (SSN, phone, email, account & card numbers) from financial PDFs before sharing them. True redaction: pages are rasterized and rebuilt so the original text bytes are removed.

Everything runs entirely in the visitor's browser. No account, no uploads, nothing stored.

## Tech

A single self-contained `index.html` (no build step). External dependencies are loaded over HTTPS:

- [Playfair Display](https://fonts.google.com/specimen/Playfair+Display) + [Hanken Grotesk](https://fonts.google.com/specimen/Hanken+Grotesk) via Google Fonts
- [pdf.js](https://mozilla.github.io/pdf.js/) and [pdf-lib](https://pdflib.js.org/) (lazy-loaded only when the redactor is opened)

## Deploy to GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** = *Deploy from a branch*.
4. Choose branch **`main`** and folder **`/ (root)`**, then **Save**.
5. Wait ~1 minute; the site publishes at `https://<username>.github.io/akabilife/`.

`.nojekyll` is included so GitHub serves the files as-is (no Jekyll processing). `404.html` provides a branded not-found page.

## Local preview

Any static server works, e.g.:

```bash
python -m http.server 8000
# then open http://localhost:8000
```

## Disclaimer

AkabiLife is an educational tool and does not provide financial, investment, tax, or legal advice. All outputs are estimates. Use is at your own risk and sole responsibility. See the in-app disclaimer for full terms; have it reviewed by a licensed attorney before production use.
