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
- [ ] No network calls
- [ ] No access to documents / vault
- [ ] Works at desktop and phone-ish widths

## Next steps (after lab is stable)

- Move to `dist/` as the artifact
- Add manifest-driven install simulation
- Host integration checks in Skipi Seafarer

## Safety (never remove)

BNWAS / Time Anchor is a **personal watchkeeping reminder and training aid**.

It is **not**:
- Certified bridge equipment
- SOLAS-compliant
- Replacement for vessel BNWAS
- Replacement for lookout duties, SMS, or master's orders
