# Selector Foundation Notes

KeyCHC V3.4.1 is the standalone reference implementation for future pump selectors.

## Common selector foundation to retain
1. **Required Duty input** — flow, head and units.
2. **Operating speed** — Hz/RPM handling.
3. **Selected Pump display** — model, motor, duty, efficiency and operating point.
4. **Curve workspace** — Pump Curve, Efficiency, Power and NPSH.
5. **System Curve** — static head + quadratic resistance through required duty.
6. **Operating Point** — pump/system curve intersection.
7. **Orifice** — after-orifice pump curve and new intersection.
8. **Alternative Models** — clickable alternate selection list.
9. **Motor display/data hook** — motor efficiency class and sizing information.
10. **PDF hook** — product-specific PDF/report output.

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
