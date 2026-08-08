# Selector Foundation Notes

KeyCHC V3.4.3 is the standalone reference implementation for future pump selectors.

## Common selector foundation to retain
1. **Required Duty input** — total system flow, head and units.
2. **Parallel pump quantity** — 1 to 6 identical pumps; per-pump selection flow = total flow ÷ quantity.
3. **Operating speed** — Hz/RPM handling.
4. **Selected Pump display** — model, quantity, motor, total duty, per-pump duty, efficiency and operating point; summary collapse keeps Efficiency, Shaft Power and NPSHr visible.
5. **Curve workspace** — selected parallel Pump Curve, optional 1–6 pump reference curves, plus per-pump Efficiency, Power and NPSH.
6. **System Curve** — static head + quadratic resistance through required total duty, stopped at the first boundary reached: shut-off head or selected parallel-pump maximum flow.
7. **Operating Point** — intersection between total system curve and combined parallel pump curve.
8. **Orifice** — after-orifice parallel pump curve using per-pump/orifice flow.
9. **Display Settings** — screen and PDF curve page share the same curve/point visibility settings.
10. **Alternative Models** — clickable qualified shortlist sorted by CHC model small → big, with `-2` before the corresponding standard model.
11. **Motor display/data hook** — motor efficiency class and sizing information.
12. **PDF hook** — total system duty on the curve page and product-specific per-pump technical data.

## Product-specific parts to replace for another selector
- Pump model database.
- Pump curve data/equations.
- Valid operating range.
- Selection ranking rules.
- Motor sizing rules if product-specific.
- Suction/discharge dimensions and product dimensions.
- Product description text.
- PDF technical/dimensional content.

## Integration rule
Keep the selector standalone while developing and validating a pump series. KeySuite integration, authentication, customer selection, quotation transfer and Supabase should be added only as a separate integration layer later.
