# KeyCHC Changelog

## V3.4.7 Standalone — 2026-08-08
- Kept the **V3.3.3 PDF Page 1 layout fully locked**: same A4 chart order, chart-box dimensions, vertical stacking, spacing, borders and typography.
- Updated PDF **Efficiency / Power / NPSHr plotted content** to follow the same enabled **1P–6P** reference-curve selections as the Pump / Head chart.
- PDF Efficiency keeps per-pump efficiency values while plotting each enabled pump count against combined flow.
- PDF Power shows total absorbed power for each enabled pump count (per-pump power × number of pumps) against combined flow.
- PDF NPSHr keeps per-pump NPSHr values while plotting each enabled pump count against combined flow.
- All four PDF Page 1 charts use the current live **Curve Hz**. D1 remains a direct single-pump selection duty; parallel curves remain display/reference only.
- Page 2 technical data, Page 3 dimensions, selector logic and CHC database are unchanged.

## V3.4.6 Standalone — 2026-08-08
- Restored **PDF Page 1** to the original KeySelector V3.3.3 stacked chart layout and dimensions.
- Locked **Efficiency / Power / NPSHr** PDF charts to the V3.3.3 format: same chart sizes, vertical arrangement, spacing, border treatment and typography.
- Only the top **Pump / Head Curve** uses the current KeyCHC display content (live Curve Hz, D1–D6, System Curve, After-Orifice/Operating Point and enabled 1P–6P reference curves).
- Reduced the dynamic Pump / Head Curve SVG back to the original V3.3.3 Page 1 chart height while retaining current display content.
- Restored the original V3.3.3 Page 1 print scaling so the four stacked charts fit the A4 page exactly as before.
- No selector calculation, CHC database, Page 2 technical data or Page 3 dimension layout changes.

## V3.4.5 Standalone — 2026-08-08
- Removed the **number of pumps running at D1** feature completely. D1 is once again a direct single-pump Flow + Head selection duty.
- Replaced the old parallel-pump quantity logic with independent **1P / 2P / 3P / 4P / 5P / 6P** reference-curve checkboxes under Display Settings.
- The enabled 1P–6P choices now apply consistently to **Pump Curve, Efficiency, Power and NPSH**. Power reference curves show total power for the enabled number of identical pumps; Efficiency and NPSHr remain per-pump performance plotted against combined flow.
- Added **live post-selection speed adjustment**. The current Operating Speed is used during selection; after a model is selected, changing Hz/RPM keeps that model selected and recalculates its curves immediately. Pressing Select again performs a new model selection at the new speed.
- Selected Pump header now shows both **Selected @ Hz** and the current **Curve Hz** when speed simulation is changed.
- Changed the top actions to matching-size **Summary ▼ / ▶** and **PDF** buttons. Expanded Summary uses ▼; collapsed Summary uses ▶.
- Collapsed Summary continues to show only **Efficiency, Shaft Power and NPSHr**.
- PDF curve output now follows the current live curve speed and enabled 1P–6P references across all four charts.
- Reworked the PDF curve-page layout so SVGs preserve their own aspect ratio instead of being forced into fixed-height boxes; the main Pump Curve uses the full page width and the three auxiliary charts use a dedicated row without curve squeezing.
- System Curve remains capped by **shut-off head or the highest enabled parallel-reference maximum flow**, whichever is reached first. Operating Point remains a 1P/system intersection because D1 selection is single-pump.
- Multiple Duty Points D1–D6, Orifice, alternative model sorting and standalone/no-login deployment are retained.

## V3.4.4 Standalone — 2026-08-08
- Removed the **Pumps in Parallel** KPI card from the Selected Pump Summary.
- Added an explicit **Parallel pump curves 1–6** checkbox in Display Settings; the screen and PDF curve page follow this toggle.
- Added **Multiple Duty Points D1–D6**. D1 remains the primary pump-selection duty; D2–D6 are reference/display points only.
- Added **+ Duty Point** and remove controls for D2–D6. Extra duty points follow the current Flow and Head units.
- Pump Curve and PDF curve page label active duty points as **D1, D2, D3…** and expand the chart range when needed.
- Renamed the Required Duty display toggle to **Duty points D1–D6** so one setting controls all duty markers on screen and PDF.
- Retained the V3.4.3 System Curve stop rule: whichever comes first — selected pump shut-off head or selected parallel-pump maximum flow.
- Retained alternative-model small → big sorting and the standalone/no-login architecture.

## V3.4.3 Standalone — 2026-08-08
- Added **Selected Pump Summary collapse**; collapsed mode keeps only Efficiency, Shaft Power and NPSHr visible.
- Added **parallel reference pump curves from 1P to 6P** on the main pump chart; the currently selected pump quantity remains the highlighted curve.
- Added Parallel Curves 1–6 to Display Settings; the PDF curve page follows this setting.
- Removed the legacy **“Pump running at D1”** wording/annotation from the selector output.
- Alternative Selection qualified shortlist is now arranged by **CHC model small → big**; for the same base model, `-2` is listed before the standard model. Main recommendation logic remains unchanged.
- Refined System Curve plotting: it stops at whichever comes first — **selected pump shut-off head (Q=0 maximum head)** or **selected parallel-pump maximum flow**.

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
