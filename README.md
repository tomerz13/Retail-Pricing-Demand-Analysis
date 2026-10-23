# Retail Pricing Strategy & Demand Elasticity Analysis 🛒📊

## 1. Executive Summary
This end-to-end data analytics and econometrics project analyzes over 100,000 retail transaction records from Dominick's Finer Foods to explore demand elasticity, price optimization, and demographic impacts on sales. Designed from the perspective of a Retail Pricing Analyst, the project utilizes Python (Pandas, Statsmodels) for advanced statistical modeling (OLS, IV Regressions, Wald Tests) and Matplotlib for data visualization.

## 2. Business Problem
**The Context:** In the highly competitive supermarket industry, profit margins are razor-thin. Retailers must constantly balance pricing strategies to maximize revenue without losing market share to competitors.

**The Problem:** Without a clear mathematical understanding of Price Elasticity of Demand (PED) and how local store demographics impact purchasing behavior, retailers often rely on "gut feeling" or uniform pricing, leading to missed revenue opportunities or lost sales volume. Furthermore, simple pricing models often suffer from endogeneity (price is influenced by unobserved local demand shocks).

**The Objective:** This project provides a robust econometric framework tailored for Pricing Strategists and Category Managers to solve two main challenges:
1. **Optimize Price Elasticity:** Measure exact demand elasticity to determine if products are price-sensitive (elastic) or price-insensitive (inelastic).
2. **Demographic-Driven Pricing:** Identify how local factors (e.g., education, income, age) drive sales volume, allowing for localized, dynamic pricing strategies rather than a one-size-fits-all approach.

## 3. Methodology
* **Data Processing (Python/Pandas):** Cleaned and merged multiple datasets (transactions, product metadata, store demographics). Filtered out outliers (e.g., prices > 3 standard deviations) and handled missing values to create a robust analytical dataset.
* **Econometric Modeling (Statsmodels):** 
  * Built Level-Level and Log-Log OLS regression models to isolate the impact of price on sales volume while controlling for store and product fixed effects (using Dummy Variables).
  * Conducted **Wald Tests (F-tests)** to validate the joint significance of categorical variables.
  * Implemented **Instrumental Variable (IV) Regression** (using average regional prices as an instrument) to correct for endogeneity and uncover the true causal effect of price on demand.
* **Data Visualization (Matplotlib):** Generated dynamic scatter plots with regression trendlines and multi-grid histograms to visualize pricing distribution and demographic variance across 90+ stores.

## 4. Results & Business Recommendations
* **Highly Elastic Demand Discovered:** The Log-Log regression model revealed a price elasticity of **-2.58**. 
  * *Recommendation:* Since demand is highly elastic (absolute value > 1), a 1% decrease in price leads to a ~2.58% increase in sales volume. The retailer should consider strategic price drops or promotions on these specific items, as the increased volume will likely offset the lower profit margin per unit, driving higher total revenue.
* **Uniform Pricing Misses Local Opportunities:** The Instrumental Variable (IV) analysis showed that the chain applies nearly uniform pricing across most stores, regardless of local demographics. 
  * *Recommendation:* Demographic analysis indicates significant variance in store environments (e.g., education levels, income, and vehicle ownership). The retailer should transition from uniform pricing to localized, zone-based pricing to capture the consumer surplus in wealthier or less price-sensitive neighborhoods.

## 5. Visual Insights
*(Note: Visualizing demand curves and demographic distributions)*

<p align="center">
  <img <img width="720" height="432" alt="Question 19 Plot" src="https://github.com/user-attachments/assets/aeea38a9-d68b-42e0-b8e5-adc07ec8a98c" />
" alt="Log-Log Demand Curve">
  <br>
  <i>Figure 1: Log-Log Regression demonstrating the inverse relationship between price and sales volume.</i>
</p>

<br>

<p align="center">
  <img src="outputs/Question_29_Plot.png" alt="Demographic Distributions">
  <br>
  <i>Figure 2: Multi-grid histograms showing the variance in local demographics across different store zones.</i>
</p>

<img width="864" height="720" alt="Question 29 Plot" src="https://github.com/user-attachments/assets/72658b9c-740d-4896-a489-f111f63c9943" />

*Figure 2: Multi-grid histograms showing the variance in local demographics across different store zones.*
