# ⚡ EV Infrastructure Analysis

## 📌 Project Overview
This project explores **Electric Vehicle (EV) adoption** and **charging infrastructure** in Canadian cities using open datasets from the Government of Canada and Statistics Canada.  
The analysis focuses on six major CMAs (**Ottawa, Toronto, Québec, Montréal, Vancouver, Victoria**) with detailed charging station data for **Montréal**.  

The study combines **time-series forecasting, demographic analysis, and geospatial insights** to answer critical policy and planning questions:

- **How has EV adoption trended over time in major Canadian cities?**  
- **What will EV demand look like in the next 5 years?**  
- **How do EV registrations relate to population size and income levels**  
- **Which cities are leading (or lagging) in EV penetration?**  
- **What is the current charging landscape in Montréal?**  

---

## 📂 Data Sources
This project uses open government datasets:

- 🔋 **EV Charging Stations in Canada**  
  [Natural Resources Canada – NRCan](https://open.canada.ca/data/en/dataset/c999d1a9-8333-4871-9226-7d3a53f490a6)  

- 🚗 **EV Registration Statistics**  
  [StatsCan](https://open.canada.ca/data/dataset/a9e40f30-3229-4fb7-8105-83e751c848d4)  

- 👥 **2021 Census Profile**  
  [Statistics Canada](https://www12.statcan.gc.ca/census-recensement/2021/dp-pd/prof/index.cfm?Lang=E)  

---

## 🔑 Key Questions & Insights  

### Q1: EV Registrations Trend Over Time by City
- 📈 Line charts show EV adoption trends (quarterly) across the six cities.  
- 👉 **Montréal leads** in registrations, followed by Vancouver and Toronto.  
- Québec and Ottawa show moderate growth, while Victoria records the lowest adoption among the six.  

### Q2: Forecasted EV Demand (Next 5 Years)
- 🔮 Prophet forecasting (quarterly) indicates a strong upward trend across all cities.  
- 👉 The projected order mirrors current adoption: Montréal, Vancouver, Toronto, Québec, Ottawa, and Victoria.  
- Montréal is expected to **maintain its lead** in total EV demand.  

### Q3: EV Ownership vs. Population & Income
📊 Regression analysis reveals:  
- A **strong positive relationship** between population size and EV registrations — larger cities tend to have more EVs.  
- A **negative association with average income**, suggesting that higher income alone does not guarantee higher EV adoption.  

### Q4: EV Penetration (EVs per 1,000 Residents)
🚦 EV penetration calculated as:  
\[
EV\ Penetration = \frac{Total\ EV\ Registrations}{Population\ 2021} \times 1000
\]  
- 👉 **Victoria and Vancouver lead** in EV penetration, demonstrating high adoption relative to their populations.  

### Q5: High vs. Low Adopter Cities
📊 Diverging bar chart compares adoption relative to the group average:  
- 👉 Victoria and Vancouver are **well above average**.  
- 👉 Toronto and Ottawa fall **below average**, signaling lagging adoption despite their size.  

### Q6 + Q7: Montréal Charger Accessibility
🗺️ Montréal stands out as the only city with detailed public charging station data, hosting **813 chargers**.  
- The network is dominated by **Level 2 chargers**, supplemented by faster **BRCC stations**.  
- Accessibility is strong:  
  - **Average distance to nearest charger (unique sites)** = 0.33 km  
  - **Median distance** = 0.26 km  
- 👉 This indicates **dense coverage in central Montréal**, though accessibility decreases in suburban zones.  

---

## 🛠️ Tech Stack
- Python (**Pandas, NumPy, Matplotlib, Seaborn**)  
- **Prophet** (time-series forecasting)  
- **Geopy** (geospatial distance analysis)  
- **Power BI** (dashboard visualization)  
- **Jupyter Notebook**  

---

## 🚀 How to Run This Project

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/ev-infrastructure-analysis.git
cd ev-infrastructure-analysis
```
### 2. Create Virtual Environment & Install Dependencies
```bash
python -m venv venv
source venv/bin/activate    # On Mac/Linux
venv\Scripts\activate       # On Windows
pip install -r requirements.txt
```
### 3. Add Data
- Download datasets from the links in the Data Sources section.
- Place them inside a folder called data/ in the project root.

### 4. Run Analysis
- Open Jupyter Notebook:
- jupyter notebook
- Run ev_analysis.ipynb to reproduce results.

### 5. Open Power BI Dashboard
- Open ev_dashboard.pbix in Power BI Desktop to explore the interactive dashboard.

---

## 📊 Future Work

- Expand charger datasets beyond Montréal by implementing standardized reporting requirements across Canadian cities.
- Incorporate utilization metrics (charging sessions, demand peaks) when released, to capture real-world usage.
- Develop scenario-based simulations (e.g., policy targets, incentive programs, charger deployment strategies) to evaluate infrastructure readiness in other cities.

---

## 🙌 Acknowledgements

- Government of Canada Open Data Portal for datasets.
- Statistics Canada for Census insights.
- Facebook Prophet team for forecasting library.

