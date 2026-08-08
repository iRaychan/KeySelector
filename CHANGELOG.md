# KeyCHC Changelog

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
