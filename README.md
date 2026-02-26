# digital-asset-macro-econometrics
An econometric analysis of the Animal Crossing: New Horizons secondary market. This project implements a Hedonic Pricing Model in Python to quantify how idiosyncratic traits (including species, personality, and gender) drive the market valuation of digital assets.

This project conducts a formal econometric investigation into the secondary market of Animal Crossing: New Horizons (ACNH). By treating in-game characters as digital assets, I implemented a Hedonic Pricing Model to decompose their market value into specific idiosyncratic traits (Species, Personality, and Gender). 
This study demonstrates how aesthetic branding and behavioral utility drive price discovery in virtual economies.

**Key Professional Insights of the Project**
* Statistical Significance: The model successfully rejected the Null Hypothesis ($H_0$), confirming that traits like "Octopus" species or "Normal" personality provide a statistically significant premium ($p < 0.05$).
* Market Inefficiencies: Identified "Residual Outliers" - villagers with high-value personalities that remain in low popularity tiers. This quantifies the "Visual Tax," where aesthetic branding (Species) can override functional utility (Personality).
* Predictive Power: Achieved an R-squared of 0.394, indicating that nearly 40% of an asset's market value is driven by observable structural traits rather than random preference.

**Econometric Career Applications:**
This project demonstrates my readiness for the following industry tasks:
* Pricing Analytics: Using Hedonic models to value complex goods (e.g., real estate or insurance products) by their individual features.
* Market Research: Applying API-driven data collection and regression analysis to identify consumer sentiment and brand premiums.
* Causal Inference: Isolating the impact of specific variables while holding others constant (Ceteris Paribus) to inform business strategy.
* Reproducible Reporting: Building end-to-end Python pipelines that transform raw, disparate data sources into actionable statistical evidence.

**Technical Stack & Data Engineering:**
* Language: Python.
* Econometrics: Multivariate OLS Regression, Hedonic Pricing, Hypothesis Testing.
* Data Pipeline: Developed a relational mapping system to join community-sourced popularity data with real-time trait data via the Nookipedia REST API.
* Libraries: Pandas (Data Wrangling), Statsmodels (Inference), Seaborn/Matplotlib (Visualization), Requests (API Integration).

**Project Report and Documentation:** For a deep dive into the methodology and statistical results, please see: [Digital_Asset_Project.pdf](https://github.com/user-attachments/files/25581726/Digital_Asset_Project.pdf)

**Econometric Methodology:**
To quantify the marginal effect of each character trait on market desirability, I specified the following cross-sectional multiple regression model:
$$Y_{i} = \beta_{0} + \beta_{1}X_{1i} + \beta_{2}X_{2i} + \beta_{3}X_{3i} + \epsilon_{i}$$
* Dependent Variable ($Y$): Popularity Tier (1=Elite, 6=Common), serving as a proxy for market valuation.
* Independent Variables ($X$): 8 unique Personality types (Behavioral Utility) and 35 Species classifications (Aesthetic Branding).
* Control Variable: Gender binary to test for valuation bias.

