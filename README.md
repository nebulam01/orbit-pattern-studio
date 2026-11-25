# 🛰️ Communications Satellite Orbit & Pattern Analysis Studio

An interactive orbital analysis and pattern discovery tool I built in Google Colab using Gradio, `sgp4`, and Pandas to parse CelesTrak Two-Line Element (TLE) data across Communications Satellites categories, compute key orbital elements, and surface surprising orbital patterns in a clean dark-mode dashboard.

## ✨ Key Features
- **Communications Satellites Focus:** Curated category selector covering Communications Satellites groups (including Active Geosynchronous, Movers, GEO Protected Zone, GEO Protected Zone Plus, Intelsat, SES, Eutelsat, Telesat, Starlink, OneWeb, Qianfan, Hulianwang Digui, Kuiper, Iridium NEXT, Orbcomm, Globalstar, Amateur Radio, SatNOGS, Experimental Comm, and Other Comm).
- **Custom TLE Input & Satellite Picker:** Paste your own 2-line or 3-line CelesTrak TLE text directly into the interface and pick any parsed satellite from the dropdown.
- **Orbital Element Calculation:** Uses `sgp4` and Keplerian/orbital relations to compute mean altitude, inclination, eccentricity, orbital period, perigee/apogee altitudes, and `BSTAR` atmospheric drag.
- **Surprising Pattern & Astrodynamics Commentary:** Flags orbital regimes (LEO, MEO, GEO/HEO) and highlights notable patterns—such as geostationary belt alignment, eccentric/transfer orbits, sun-synchronous bands, or LEO constellation shells—alongside group comparisons.

## 🛠️ Tech Stack
- **Environment:** Google Colab (browser-based workflow, no local desktop orbit tools required)
- **Parsing, Propagation & UI:** Python, `sgp4`, Pandas, Gradio

## ⚙️ How to Run the Project
1. **Open in Google Colab:**
   - Upload the notebook or script to Google Colab (`colab.research.google.com`).
2. **Run & Launch the UI:**
   - Run the cell to install `sgp4`, `gradio`, and `pandas` and launch the interactive dashboard directly inside the notebook.
3. **Paste & Explore:**
   - Select a Communications Satellites category, paste your TLE data from CelesTrak, choose a satellite, and click **Run Orbit & Pattern Analysis** to inspect the metric cards and pattern interpretation.

## 📌 Scope & Assumptions
- Built for exploratory orbital analysis and educational/engineering pattern discovery from public TLE sets, not operational conjunction screening or high-precision mission navigation.
- Derives orbital altitude and period from Kozai mean motion (`no_kozai`), inclination, and eccentricity via standard Earth gravitational parameter ($\mu = 398600.4418\text{ km}^3/\text{s}^2$) and equatorial radius ($R_e = 6378.137\text{ km}$) approximations.
