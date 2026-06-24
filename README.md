# BNWAS / Time Anchor — Plugin Lab

Standalone development + test environment for the BNWAS / Time Anchor plugin.

## Quick start (standalone)

```bash
cd test-host
python3 -m http.server 8765
# then open http://localhost:8765
```

Or simply open `test-host/index.html` directly in any browser.

## What it must do (Definition of Done for this lab)

- [x] Interval selection (presets + future custom)
- [x] Start watch
- [x] Accurate countdown
- [x] On expiry → alarm starts immediately
- [x] Alarm repeats until user presses Acknowledge
- [x] Acknowledge stops alarm and arms next cycle (+1 cycle count)
- [x] Visible cycle counter + total watch time
- [x] Day / Night mode (theming + flash behavior)
- [x] Strong visible safety disclaimer
- [x] No network calls (static grep + runtime monkeypatch: 0 calls)
- [x] No access to documents / vault
- [x] Works at desktop and phone-ish widths

## Bundled artifact (for Seafarer PR #4)

The host-consumable artifact lives at:

```text
dist/plugins/bnwas-time-anchor/
  plugin.json   index.js   index.css   assets/   checksums.json   CHANGELOG.md   REPORT.md
```

It registers `window.SkipiPlugins["bnwas-time-anchor"] = { manifest, mount, unmount }`.

Test the artifact in a mock host:

```bash
cd test-host
python3 -m http.server 8765
# mock host:      http://localhost:8765/mock-host.html
# contract test:  http://localhost:8765/contract-test.html  (prints PASS n/n)
```

## Next steps (after lab is stable)

- [x] Move artifact under `dist/plugins/bnwas-time-anchor/`
- [ ] Seafarer copies the artifact into its `dist/plugins/` and wires Install → Open (separate handoff)
- [ ] Host integration smoke in Skipi Seafarer

## Safety (never remove)

BNWAS / Time Anchor is a **personal watchkeeping reminder and training aid**.

It is **not**:
- Certified bridge equipment
- SOLAS-compliant
- Replacement for vessel BNWAS
- Replacement for lookout duties, SMS, or master's orders
