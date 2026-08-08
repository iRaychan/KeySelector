# KeyCHC V3.4.1 — Pure Standalone Selector

This is a **standalone pump selector** build intended to be used directly and as a foundation for future selector products.

## Access / backend
- **No KeySuite login required.**
- **No Keylargo user approval required.**
- **No Supabase required.**
- **No `config.js` required.**
- **No customer, quotation, role, or user-access dependency.**
- The selector opens directly from `index.html`.

## Selector functions retained
- CHC pump database and CHC selection engine.
- Required Duty input.
- Selected Pump display.
- Pump Curve, Efficiency, Power and NPSH charts.
- System Curve and calculated Operating Point.
- Orifice / After-Orifice curve using selected CHC discharge DN.
- Clickable Alternative Models.
- Existing CHC PDF output.

## Foundation purpose
Use this package as the clean working selector base before connecting any selector to KeySuite. Product-specific data, selection rules and PDF content can later be changed for a new pump series while retaining the common selector workflow.

See `SELECTOR-FOUNDATION.md` for the reusable areas.

## Deploy
Upload all files in this package to the root of a GitHub Pages repository. `index.html` is the application entry point. No environment variables or backend setup are required.
