# WagnerPlot — XPS Chemical State Analysis Tool

A self-contained, browser-based application for constructing and exporting Wagner plots (chemical state plots) from X-ray photoelectron spectroscopy (XPS) data. No installation, no server, no dependencies to manage — open the single HTML file in any modern browser and it works immediately.

### What it does

Wagner plots display core-level binding energy (x-axis, in the negative direction) against Auger kinetic energy (y-axis) for a given element across a range of chemical states. Diagonal lines of constant modified Auger parameter α′ = BE + KE allow rapid identification of chemical state, and the slope of trends through data points distinguishes initial-state effects (slope 1) from final-state relaxation effects (slope 3).

### Features
•	Built-in XPS reference database covering 20 elements (Cu, Zn, Ag, Ni, Fe, Co, Mn, Cr, Ti, Si, Al, Mg, Na, C, O, S, Pd, Sn, In, Cd, Pb) with ~140 reference compounds drawn from the NIST XPS Database and Biesinger et al., with BE and Auger KE values pre-populated on element/compound selection

•	Live α′ calculation — the modified Auger parameter updates as values are entered

•	Correct Wagner plot convention — BE axis runs in the negative direction (high→low left to right); Auger KE increases upward; constant-α′ diagonals appear at +45° in screen coordinates

•	Orthogonal axis scaling — enforces equal eV/pixel on both axes so α′ lines are geometrically true 45° diagonals, matching published plot standards

•	Overlay of reference ghost points for the active element, showing all database states as faded markers for visual comparison

•	Toggleable display options — α′ lines, data labels, grid, reference overlay, and orthogonal scaling

•	Three export formats: 
  - JPG — high-resolution (3× pixel density) raster image
  - PDF (A4 landscape) — publication-ready output with the plot, element metadata, and a formatted data table; Unicode-safe text rendering throughout
  - CSV — label, element, core level, Auger transition, BE, KE, and α′ for import into Excel, OriginLab, or any plotting package

•	Horizontal data strip — all plotted points displayed as colour-coded cards below the plot for at-a-glance review and one-click removal

### Usage

Download wagner_plot.html and open it in Chrome, Firefox, Edge, or Safari. No internet connection is required after the initial load of two Google Fonts.

### Technical notes

The application is a single-file HTML/CSS/JavaScript document (~56 KB). The SVG plot engine is written from scratch with no charting library dependency. PDF generation uses jsPDF loaded from the Cloudflare CDN. The HarwellXPS logo is embedded as a base64 data URI.

