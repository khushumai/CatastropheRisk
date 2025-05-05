# 🌪️ Catastrophe Risk Simulation (Hurricane Loss Estimator)
Estimate insured losses from synthetic hurricane events using Monte Carlo simulation techniques. This model demonstrates basic catastrophe modeling logic, suitable for reinsurance risk analysis.

This project models the **insured losses from hurricanes** across a synthetic coastal property portfolio using **NOAA HURDAT2 storm data** and **Monte Carlo simulation**. It includes **Exceedance Probability (EP) curves**, **100-year and 10-year Probable Maximum Loss (PML)** estimates, and **forecasting of hurricane impacts over the next 10 years**.

---

## 📌 Objectives

- Estimate financial risk from hurricanes in the U.S. Gulf Coast
- Use probabilistic modeling to simulate storm impacts on exposed properties
- Generate annual loss distributions and key insurance risk metrics

---

## 📁 Data Components

### 1. 🏠 Synthetic Property Exposure Dataset
- 50,000 properties randomly distributed across Gulf Coast latitudes & longitudes
- Attributes include:
  - Location (Latitude/Longitude)
  - Insured Value (log-normal distribution between $100K and $5M)
  - Construction Type: Wood, Steel, or Concrete

### 2. 🌀 Historical Storm Data from NOAA HURDAT2
- Parsed data for the last 25 years of Atlantic hurricanes
- Includes storm name, year, and coordinates of landfall positions

---

## 🔁 Simulation Workflow

1. **Generate Synthetic Properties**
2. **Parse Historical Storm Paths from NOAA**
3. **Run 10-Year Monte Carlo Simulations**
   - Random selection of historical storm paths
   - Identify properties within 50-mile radius of storm center
   - Calculate loss as 10% of insured value with multipliers:
     - Wood: ×2
     - Steel: ×1.5
     - Concrete: ×1.2
4. **Aggregate Yearly Losses**
5. **Generate EP Curve & Compute PML Metrics**
6. **Output Summary & CSV Exports**

---
