# FX Decision Recommendation System for Indian Businesses

## Course
23CSE452 – Business Analytics  
Capstone Project

## Project Overview
In today's globalized economy, Indian businesses (such as importers, exporters, IT service companies, and startups) face massive financial exposure to foreign exchange (FX) fluctuations. A sudden drop in the USD/INR or GBP/INR rate can wipe out a company's profit margins overnight. Knowing when to convert money or hedge is a critical, yet highly difficult mathematical challenge.

This project proposes a **Full-Stack FX Decision Recommendation System** that applies advanced business analytics, machine learning (time-series forecasting), and statistical risk engines to support data-driven foreign exchange decision-making. The system bridges the gap between raw exchange rate data and business-relevant insights by quantifying currency exposure, calculating real-time risk, and generating prescriptive recommendations via a modern web dashboard.

---

## Business Insights & BA Concepts Applied (Rubric Alignment)

### 1. Relevance of Topics and Justification
This project addresses a real-world, high-stakes financial problem. Instead of relying on human intuition, this system provides objective, mathematical answers. By building a fully automated prediction and risk identification engine, we justified the need to protect the business from unforeseen crashes. The module provides an automated "Black Swan Alert" and unified risk scoring, actively advising CEOs when it is too dangerous or highly profitable to convert their money.

### 2. Dataset Selection and BA Concepts Applied
We utilized a historical time-series dataset of major global currency pairs (USD, EUR, GBP, JPY vs INR) using Yahoo Finance and RBI data. Several core Business Analytics concepts were successfully engineered:
- **Descriptive & Predictive Analytics:** 30-day rolling standard deviations (`.std()`) and Facebook Prophet ML Models predict future movements and confidence intervals.
- **Anomaly Detection (Z-Score):** Implemented statistical limiters using Z-Scores `(Current - Mean) / StdDev` to statistically identify and flag rare outlier events.
- **Data Normalization:** Applied Min-Max scaling to compress massive monetary exposures and microscopic volatilities into a standardized 0-100 impact array.
- **Value-at-Risk (VaR):** Calculated the 5th percentile (`np.percentile`) of historical returns to statistically define the 95% Confidence VaR (worst-case scenario modeling).

### 3. Key Business Insights Generated
Through building this analytical engine, several critical business insights were realized:
- **Risk Standardization:** By normalizing vastly different metrics (market volatility vs. specific dollar exposure), we created highly intuitive **0-100 Speedometer Risk Gauges** that allow non-technical executives to assess complex mathematical dangers in seconds.
- **Emotional Independence (Z-Score Guardrails):** Automating Z-Score thresholds removes emotional trading. The system flawlessly and mathematically proves when standard pricing models are unreliable via automated warnings.
- **Concrete Financial Mapping:** Translating abstract percentages into concrete Rupee losses via VaR models forces rational, grounded financial decision-making, minimizing corporate losses during high-volatility events.
- **Quadrant Risk Mapping:** Visually plotting Volatility vs. USD Sensitivity allows finance managers to instantly categorize their corporate holdings into "High Danger" vs "Safe Haven" trading zones.

---

## Platform Methodology
Our methodology was implemented dynamically via a Python Flask backend serving a localized React dashboard, eliminating manual analysis.
1. **Data Ingestion & Stabilization (Srividya):** Fetches historical/live data and stabilizes the time-series using Augmented Dickey-Fuller (ADF) tests to enable accurate machine learning.
2. **Predictive Forecasting (Adwaitha):** Runs Facebook Prophet models trained on historic data. It projects 7-30 day rate forecasts alongside Upper/Lower statistical confidence bounds.
3. **Risk Scoring Engine (Kanishkhan):** Computes rolling variations, Z-Score anomaly triggers, and VaR percentiles. It normalizes exposure risk to output real-time "Black Swan Alerts" and 0-100 Danger classifications.
4. **Business Exposure Modeling (Aadhithya):** Calculates Profit-at-Risk by merging live rates with user-defined contract types (Import/Export) and deal sizes to produce prescriptive action triggers (Hedge vs Spot).
5. **Dashboard Integration (Adarsh):** Connects the JSON Python API securely to a dynamic React Front-End, providing live metrics, responsive quadrants, and real-time user notification systems.

---

## Tools & Technologies
- **Backend Analytics Engine:** Python, Flask API, Pandas, NumPy, Statsmodels.
- **Predictive Modelling:** Facebook Prophet (Time-Series ML), yfinance.
- **Frontend Dashboard:** React, Vite, Tailwind CSS, Recharts.
- **Version Control & Collaboration:** Git, GitHub.

---

## Note
All financial values, business scenarios, and assumptions used in this project are for academic and demonstration purposes only and do not represent any specific real-world organization.
