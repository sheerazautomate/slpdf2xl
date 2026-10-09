# EMIS Student List → Excel

Single-file, browser-only web app (`index.html`). The PDF never leaves the device.

## Deploy (GitHub Pages)
1. Create a repo, add `index.html` at the root.
2. Settings → Pages → Deploy from branch → `main` / root.

## Notes
- Libraries load from cdnjs (pinned): pdf.js 3.11.174, ExcelJS 4.4.0. Needs internet on first load.
- Parser logic: `parsePdf()` between the `//--CORE--` and `//--UI--` markers.
- New class names (e.g. KG, PREP): add to the `KNOWN` array.
- Output: Students sheet + Summary sheet (COUNTIFS formulas), same as the Claude skill.

## Next steps
- Wrap with Capacitor for an APK (same GitHub Actions flow as your other apps); bundle the two libraries locally for offline use.
