# Selector Foundation Notes

KeyCHC V3.4.2 is the standalone reference implementation for future pump selectors.

## Common selector foundation to retain
1. **Required Duty input** — total system flow, head and units.
2. **Parallel pump quantity** — 1 to 6 identical pumps; per-pump selection flow = total flow ÷ quantity.
3. **Operating speed** — Hz/RPM handling.
4. **Selected Pump display** — model, quantity, motor, total duty, per-pump duty, efficiency and operating point.
5. **Curve workspace** — combined Pump Curve plus per-pump Efficiency, Power and NPSH.
6. **System Curve** — static head + quadratic resistance through required total duty, visually capped at pump shut-off head.
7. **Operating Point** — intersection between total system curve and combined parallel pump curve.
8. **Orifice** — after-orifice parallel pump curve using per-pump/orifice flow.
9. **Display Settings** — screen and PDF curve page share the same curve/point visibility settings.
10. **Alternative Models** — clickable alternate selection list.
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
