# The End of the Grand Compromise — Education in the Age of AI

A Prezi-style (impress.js) zoomable presentation. **`index.html` is the deck** — single
self-contained file (fonts, logos, impress.js embedded), works offline from a double-click.

## Presenting
`→`/`SPACE` next · `←` back · `B` blackout · `F` jump to discussion view · `F5` fullscreen.
PgUp/PgDn clicker keys work.

Speaker script: `docs/speaker-script-lt.md` (LT) — the only source of speaker notes; the deck
itself contains none. Before the talk, run the agent once on the real coursework and record a
fallback — see the script's checklist.

## Files
- `index.html` — the built deck (final deliverable)
- `src/deck.template.html` — deck source (edit this, then rebuild)
- `build/instrument-embedded.css`, `build/plexmono-embedded.css` — base64-embedded fonts
- `vendor/impress.js` — impress.js 1.1.0 (presenter-console plugin stripped)
- `assets/` — Visma wordmark SVG, VilniusTech logo PNG
- `mockups/E-visma-canvas.html` — the approved overview design (static reference)
- `docs/specs/…design.md` — full design doc: thesis, fact-check record, demo plan
- `prezi/` — alternative Prezi.com route (brief + structure map); unused by the HTML deck
- `build/screens/deck/` — current verification screenshots

## Rebuild after editing the template
```bash
python3 - <<'EOF'
import pathlib, base64
tpl = pathlib.Path("src/deck.template.html").read_text()
fonts = pathlib.Path("build/instrument-embedded.css").read_text() + pathlib.Path("build/plexmono-embedded.css").read_text()
impress = pathlib.Path("vendor/impress.js").read_text()
svg = pathlib.Path("assets/visma-logo.svg").read_text().strip().replace('<svg width="235" height="64"', '<svg width="92" height="25"', 1)
vt = base64.b64encode(pathlib.Path("assets/vilniustech.png").read_bytes()).decode()
out = (tpl.replace("/*__FONTS__*/", fonts).replace("/*__IMPRESS__*/", impress)
          .replace("__VISMA_SVG__", svg).replace("__VT_B64__", vt))
pathlib.Path("index.html").write_text(out)
EOF
```
