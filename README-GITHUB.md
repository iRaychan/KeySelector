# KeySelector CHC v3.2.3g

Test build for the two-page Pump Selection and Technical Data report.

Changes in this build:
- Underlined Motor Efficiency, Power Factor, and Pumpset Dimension headings.
- Fixed the missing Technical Data logo by waiting for images and fonts before printing.
- Removed the duplicate print page break that could create a blank second page on PC.

Open `index.html` in Chrome or Edge, select a pump, and use Export PDF.


## v3.2.3g
- Replaced B.G.Reich logo with the supplied high-definition PNG.
- Lowered the Page 2 TECHNICAL DATA title by 3 px.
- Moved the modification notice one row below the approximate dimension note.

- Reduced the Page 2 header-to-table gap by about half.
- Increased and balanced Page 2 row heights and section spacing to use the printable page more evenly.
- Kept the approved table structure, borders, logo, and footer wording unchanged.


## v3.2.3g
- TECHNICAL DATA title: 13 px
- Technical table content: 10 px
- Approximate dimension note: 10 px
- B.G.Reich reservation notice: 11 px

## v3.2.3h motor data update
- Added motor efficiency selection: IE5, IE4, IE3 (default), IE2 and IE.
- Added motor phase selection: 3 Phase (default) and 1 Phase.
- Voltage range changes automatically: 380–415 V for 3 Phase; 220–240 V for 1 Phase.
- Page 2 motor specifications now match motor HP, phase and efficiency class using Motor - 260726.xlsx.
- IE4 and IE5 remain selectable and display Data Not Available until their specification tables are added.
