# KnowDrug Doctor Edition (English)

An English copy of the KnowDrug doctor app. The original Chinese project remains separate. This copy preserves the video files and video sources, patient insights, video browsing, and the Q&A workflow.

## Run locally

```bash
python3 -m http.server 8080 --directory dist
```

Open `http://127.0.0.1:8080/` on a computer or phone on the same network.

## Implementation

- `dist/` is the deployable site. GitHub Pages serves this directory from the `gh-pages` branch.
- `dist/i18n-en.js` translates interface text in place without changing the underlying interaction logic or video media.
- The Q&A client requests English responses from the existing server using `locale: "en"`. The server keeps its default Chinese behavior for the original apps.
- Browser storage uses the `medlink-en-` prefix, separate from the Chinese doctor app.

## Check

```bash
npm ci
npm test
```
