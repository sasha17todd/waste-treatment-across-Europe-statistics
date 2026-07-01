# Buried or Reborn? Europe's Waste-Management Divide and Romania's Position in the Recycling Transition (2004–2022)

Big Data Visualization course project — Polytechnic University of Timișoara.
**Author:** Alexandrina Tudosiev Palincas · **Coordinator:** Alexandru Topîrceanu

## Overview

This project analyzes how European countries treat their waste and locates Romania
within that landscape. Starting from a large Eurostat dataset (~527,000 observations),
it computes recycling rates and waste-management mixes, applies descriptive statistics
and correlation analysis, and builds a country-similarity **network** with community
detection.

**Main findings:** Europe splits into four distinct recycling tiers rather than a
smooth gradient. Romania recycles ~31.6% of its non-mineral treated waste (EU-27
average: 50.9%), ranks 23rd of 27, and landfills close to 90% of its total waste.
Landfill and recycling shares are strongly anti-correlated (r = −0.82). An unsupervised
similarity network groups Romania with Bulgaria, Estonia, Greece, Hungary and Malta —
the landfill-reliant periphery — with modularity Q = 0.62.

## Data

- **Source:** Eurostat — *Treatment of waste by waste category, hazardousness and waste
  management operations* (`env_wastrt`), unit: tonnes.
- **Link:** https://ec.europa.eu/eurostat/databrowser/view/env_wastrt/
- **Complementary source (for comparison):** European Environment Agency — *Waste
  recycling in Europe*: https://www.eea.europa.eu/en/analysis/indicators/waste-recycling-in-europe
- The raw export file `env_wastrt__custom_21660473_spreadsheet.xlsx` is included in
  this repository so the notebook can be run end to end.

## How to run

1. Clone or download this repository.
2. Make sure the Excel file `env_wastrt__custom_21660473_spreadsheet.xlsx` is in the
   same folder as the notebook.
3. Install dependencies:
   ```
   pip install pandas numpy matplotlib networkx scipy openpyxl
   ```
4. Open `waste_analysis.ipynb` in Jupyter (or Google Colab) and run all cells top to
   bottom. Figures are saved as `fig1_*.png` … `fig6_*.png`, and the network is
   exported to `country_waste_network.graphml` (openable in Gephi).

## Contents

- `waste_analysis.ipynb` — full analysis pipeline (parsing → indicators → figures → network)
- `env_wastrt__custom_21660473_spreadsheet.xlsx` — raw Eurostat data
- `figures/` — generated figures
- `country_waste_network.graphml` — network export for Gephi

## Tools

Python (pandas, NumPy, Matplotlib, NetworkX, SciPy, openpyxl), Jupyter, and Gephi for
interactive network visualization.
