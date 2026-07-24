# KeySelector CHC v3.2.3a

Immediate test release based on v3.2.2.

## Changes
- Removed the duplicate page-break logic that caused a blank PDF page.
- Added the same B.G.Reich logo/model header to the Technical Data page.
- Added consistent page footers and page numbering.
- Kept the existing Page 1 chart layout and selection logic.
- Updated the Technical Data page to use the available A4 print area more efficiently.
- Increased the print delay to improve logo and chart rendering reliability.

## Test
1. Open `index.html` in Chrome or Edge.
2. Select a duty point and pump.
3. Click Export PDF.
4. Confirm the preview contains exactly 2 pages with no blank page.

This is an immediate framework test release, not the final v3.2.3 production release.
