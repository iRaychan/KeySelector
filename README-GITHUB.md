# KeyCHC V3.4.6 — Pure Standalone Selector

This is a **standalone CHC pump selector** and reusable selector foundation. It opens directly without KeySuite or a backend.

## Access / backend
- **No KeySuite login required.**
- **No Keylargo user approval required.**
- **No Supabase required.**
- **No `config.js` required.**
- **No customer, quotation, role, or user-access dependency.**
- The selector opens directly from `index.html`.

## Selector functions
- Existing CHC pump database and selection engine retained.
- Required Duty is direct **single-pump Flow + Head**. There is no number-of-pumps-running-at-D1 input and D1 is never divided by a pump quantity.
- Operating Speed / Hz is used to select the pump. After selection, changing Hz/RPM keeps the selected model fixed and recalculates that model's curves live; press **Select** again only when a new model selection is required at the new speed.
- Selected Pump Summary can collapse to only **Efficiency, Shaft Power and NPSHr**.
- Top controls are matching-size **Summary ▼ / ▶** and **PDF** buttons.
- Display Settings provide independent **1P, 2P, 3P, 4P, 5P and 6P** reference-curve choices.
- Enabled 1P–6P references apply to **Pump Curve, Efficiency, Power and NPSH** together.
  - Pump: combined flow = per-pump flow × pump count at the same head.
  - Efficiency: per-pump efficiency plotted against combined flow.
  - Power: total power of the enabled number of pumps plotted against combined flow.
  - NPSH: per-pump NPSHr plotted against combined flow.
- Parallel references are display/analysis curves only; they do **not** change the D1 selection model.
- **Multiple Duty Points D1–D6**: D1 controls pump selection; D2–D6 are reference/display points.
- System Curve uses static head + quadratic resistance through D1 and stops at whichever comes first: **selected pump shut-off head** or the maximum flow of the highest enabled 1P–6P reference curve.
- Operating Point remains the **1P pump/system intersection** because D1 selection is single-pump.
- Orifice / After-Orifice remains a 1P analysis curve using the selected CHC pump discharge DN.
- Clickable Alternative Models remain arranged **CHC model small → big**, with `-2` variants before the matching standard model.
- PDF curve output follows current Display Settings, duty points, enabled 1P–6P curves and the current live curve speed.
- PDF chart layout preserves SVG aspect ratios so curves are not squeezed into fixed-height boxes.
- Existing CHC technical and dimensional PDF content is retained.

## Display Settings applied to screen and PDF
- Parallel Curves: **1P / 2P / 3P / 4P / 5P / 6P**
- Duty Points D1–D6
- System Curve
- After-Orifice Curve
- Operating Point (1P)

## Foundation purpose
Use this package as a clean working selector base before connecting any selector to KeySuite. Product-specific data, selection rules and PDF content can later be replaced for another pump series while retaining the common selector workflow.

See `SELECTOR-FOUNDATION.md` for reusable areas.

## Deploy
Upload all files in this package to the root of a GitHub Pages repository. `index.html` is the application entry point. No environment variables or backend setup are required.

## V3.4.6 PDF Page 1 lock

- PDF Page 1 returns to the original **KeySelector V3.3.3** page layout.
- **Efficiency / Power / NPSHr** chart format, size, stacking, spacing and styling are locked to V3.3.3.
- Only the top **Pump / Head Curve** plotted content follows the current KeyCHC display settings (live curve speed, duty points, system/orifice/operating point and enabled parallel reference curves).
- Page 2 technical data and Page 3 dimensions remain unchanged.
