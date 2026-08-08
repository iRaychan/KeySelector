# KeyCHC V3.4.3 — Pure Standalone Selector

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
- Required Duty input uses **Total System Flow** and Head.
- **1–6 identical pumps in parallel**; selection flow per pump = Total Flow ÷ Pump Quantity.
- Selected Pump display shows quantity, total system duty and duty per pump.
- Selected Pump Summary can collapse to only **Efficiency, Shaft Power and NPSHr**.
- Selected parallel Pump Curve plus optional **1–6 pump parallel reference curves**; per-pump Efficiency, Power and NPSH charts.
- System Curve based on static head + quadratic resistance through Required Duty.
- System Curve display stops at whichever comes first: **selected pump shut-off head** or **selected parallel-pump maximum flow**.
- Operating Point is calculated from the combined parallel pump curve and total System Curve.
- Orifice / After-Orifice curve uses each pump's discharge DN and per-pump flow.
- Clickable Alternative Models, with the qualified shortlist arranged **CHC model small → big** and `-2` variants before the matching standard model.
- PDF curve page follows current Display Settings, including parallel reference curves.
- Existing CHC technical/dimensional PDF format retained; parallel selections show total duty on the curve page and per-pump capacity on the technical page.

## Display Settings applied to PDF
- Selected Pump Curve
- Parallel Curves 1–6
- Required Duty
- System Curve
- After-Orifice Curve
- Operating Point

## Foundation purpose
Use this package as a clean working selector base before connecting any selector to KeySuite. Product-specific data, selection rules and PDF content can later be replaced for another pump series while retaining the common selector workflow.

See `SELECTOR-FOUNDATION.md` for reusable areas.

## Deploy
Upload all files in this package to the root of a GitHub Pages repository. `index.html` is the application entry point. No environment variables or backend setup are required.
