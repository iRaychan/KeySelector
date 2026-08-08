# KeyCHC Changelog

## V3.4.2 Standalone — 2026-08-08
- Added **1 to 6 identical pumps in parallel**. Required Flow is treated as total system flow; pump selection uses Total Flow ÷ Pump Quantity at the same head.
- Main pump curve now becomes the combined parallel-pump curve while Efficiency, Power and NPSH remain per-pump charts.
- System Curve and Operating Point now calculate against total parallel flow.
- Limited System Curve display to the selected pump **shut-off head at zero flow** so it no longer extends excessively above the useful pump range.
- Orifice / After-Orifice calculation now uses the flow through each individual pump/orifice when multiple pumps are selected.
- Added Pump Curve ON/OFF to Display Settings.
- PDF curve page now follows the active Pump Curve, Required Duty, System Curve, After-Orifice and Operating Point display settings.
- PDF front page shows total system duty and pump quantity; CHC technical data Capacity is shown **per pump** for parallel selections.
- Retained the original CHC database, model data and standalone/no-login deployment mode.

## V3.4.1 Standalone — 2026-08-08
- Defined KeyCHC as a **pure standalone selector** foundation.
- Explicitly removed any KeySuite/Supabase/login requirement from the deployment specification.
- No KeySuite user or Keylargo approval is required to open the selector.
- No `config.js` or backend is required.
- Retained all KeyCHC V3.4.0 selector functions and CHC data.
- Added selector-foundation notes for branching future pump selectors.

## V3.4.0 — 2026-08-08
- Renamed the CHC selector interface from KeySelector to KeyCHC.
- Retained the complete KeySelector V3.3.3 CHC database and selection engine.
- Reorganized the selector screen to follow the KeyES result style.
- Added prominent Selected Pump display.
- Added primary Pump Curve with auxiliary Efficiency, Power and NPSH charts.
- Added System Curve based on Static Head plus calculated quadratic friction resistance through Required Duty.
- Added CHC discharge-DN-aware Orifice calculation and After-Orifice curve.
- Added calculated Operating Point intersection.
- Kept Alternative Models clickable.
- Retained the existing CHC PDF generator/report format.
