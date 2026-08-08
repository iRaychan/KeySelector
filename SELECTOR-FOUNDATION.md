# Selector Foundation Notes

KeyCHC V3.4.7 is the standalone reference implementation for future pump selectors.

## Common selector foundation to retain
1. **Required Duty input** — direct single-pump flow, head and units. D1 is not divided by a pump quantity.
2. **Operating speed** — Hz/RPM input used for selection plus live post-selection curve simulation while retaining the selected model.
3. **Selected Pump display** — model, motor, D1 performance, selected-at speed and current curve speed; collapsed Summary keeps Efficiency, Shaft Power and NPSHr visible.
4. **Parallel reference layer** — independent 1P–6P display choices applied to Pump, Efficiency, Power and NPSH charts without changing D1 selection logic.
5. **Curve workspace** — Pump Curve plus Efficiency, Power and NPSH using the same enabled 1P–6P reference set.
6. **System Curve** — static head + quadratic resistance through D1; display stops at the first boundary reached: shut-off head or maximum flow of the highest enabled parallel reference curve.
7. **Operating Point** — 1P pump/system intersection. Parallel references remain analysis overlays rather than selection-state inputs.
8. **Orifice** — 1P after-orifice analysis using selected pump discharge DN.
9. **Display Settings** — screen and PDF share 1P–6P, duty-point, system, orifice and operating-point visibility settings.
10. **Multiple Duty Points** — D1 is primary selection duty; D2–D6 are optional reference points.
11. **Alternative Models** — clickable qualified shortlist sorted by CHC model small → big, with `-2` before the corresponding standard model.
12. **PDF hook** — retain the locked V3.3.3 Page 1 chart-box layout while letting Pump, Efficiency, Power and NPSHr plotted content follow enabled 1P–6P references and current live Curve Hz.

## Product-specific parts to replace for another selector
- Pump model database.
- Pump curve data/equations.
- Valid operating range.
- Selection ranking rules.
- Speed/affinity-law implementation where product-specific.
- Motor sizing rules if product-specific.
- Suction/discharge dimensions and product dimensions.
- Product description text.
- PDF technical/dimensional content.

## Integration rule
Keep the selector standalone while developing and validating a pump series. KeySuite integration, authentication, customer selection, quotation transfer and Supabase should be added only as a separate integration layer later.
