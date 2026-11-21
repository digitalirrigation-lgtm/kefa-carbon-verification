# kefa-carbon-verification
# Carbon Stock Estimation for Kefa Zone, Ethiopia

## 1. Objective
This project estimates the aboveground carbon stock for Kefa Zone (formerly Kafa) in South West Ethiopia, using Google Earth Engine. It is a screening-level analysis intended to identify high-carbon forest areas for potential conservation or carbon project development.

## 2. Study Area
- **Country:** Ethiopia
- **Region:** South West Ethiopia
- **Zone:** Kefa
- **Area:** Approximately 10,000 km²

## 3. Data & Methods
- **Carbon Data:** NASA/ORNL Global Biomass Carbon Density (2010, 300 m resolution). Band used: `agb` (aboveground carbon density, in Mg C/ha).
- **Boundary:** FAO GAUL 2025 administrative boundaries (Level 2, `Kefa`).
- **Tool:** Google Earth Engine Python API, executed in Google Colab.

### Workflow
1.  Boundary acquisition from GAUL 2025.
2.  Loading and filtering the NASA carbon dataset.
3.  Unit conversion: converting carbon density (Mg C/ha) to total tonnes of carbon (tC) by multiplying by pixel area and summing across the zone.
4.  Uncertainty calculation using the dataset's provided `agb_uncertainty` band.
5.  Visualisation and export of a classified carbon map.

## 4. Key Results
- **Estimated Total Aboveground Carbon:** 44.4 million tonnes of carbon (tC).
- **Uncertainty (1σ):** ±53% (plausible range: 20.8 – 68.1 million tC).
- **CO₂-Equivalent:** Approximately 162.9 million tonnes of CO₂e.

## 5. Interpretation & Limitations
The estimate is a **screening-level tool**, not a verified carbon credit. The wide uncertainty (±53%) is typical for global datasets applied without local field calibration. The result identifies Kefa as a high-carbon landscape and provides a spatial prioritisation map for where field sampling should be conducted to narrow the uncertainty. The carbon baseline is from 2010; it is not a current measurement.

## 6. How to Run This Code
1.  Open the `.ipynb` notebook in Google Colab.
2.  Ensure you have a Google Cloud project registered for Earth Engine.
3.  Run the notebook cells in order. The notebook is self-contained.

## 7. Repository Contents
- `kefa_carbon_analysis.ipynb` — The complete, documented Colab notebook.
- `README.md` — This file.

## 8. Author
[Your Name]
[Your Email / LinkedIn]
