# retail-marketing-analytics-framework
An integrated retail analytics framework combining Market Basket Analysis, RFM Segmentation, and Sales-Driver Machine Learning
# Integrated Marketing Analytics for Retail Growth

## 📌 Business Challenge
Retail organizations sit on massive volumes of transaction data, but often struggle to convert these historical records into actionable marketing intelligence. The business required an evidence-based framework to identify optimal product bundling, understand internal sales drivers, and execute targeted customer retention strategies without relying on external advertising spend data.

## 🎯 Project Objective
To architect a comprehensive, Python-based decision-support system analyzing 478,000+ UK retail transactions across three complementary analytical lenses: Market Basket Analysis (WHAT to sell together), RFM Segmentation (WHO to target), and Internal Sales-Driver Modeling (UNDER WHAT CONDITIONS sales occur).

## ⚙️ Analytical Pipeline & Tech Stack
* **Data Engineering:** Cleaned 551K+ raw transaction rows, removing cancellations and administrative codes to isolate 478,941 valid UK transactions generating £8.73M in revenue.
* **Market Basket Analysis (Apriori):** Mined 14,763 baskets across the top 120 products to generate frequent itemsets and high-confidence association rules.
* **Sales-Driver Machine Learning:** Engineered 54 sequential weekly bins and evaluated Linear Regression, Ridge, Lasso, and Random Forest models using `TimeSeriesSplit` to identify internal variables (e.g., product breadth, cancellation rates) driving weekly sales.
* **RFM Segmentation:** Scored 3,916 identifiable customers across Recency, Frequency, and Monetary dimensions to build 6 distinct behavioral archetypes.

## 📊 Key Findings & Impact
* **Cross-Selling Opportunities:** Discovered 154 actionable association rules. The strongest rule (PINK REGENCY TEACUP -> GREEN/ROSES REGENCY) achieved a massive **14.78x Lift** with 70% confidence, providing a data-backed blueprint for product bundling.
* **Predictive Sales Drivers:** The expanded Marketing Mix Linear Regression outperformed baseline models on the chronological test set (RMSE: £49,997). Driver analysis revealed product assortment breadth as the strongest positive indicator for weekly sales volume.
* **Customer Value Concentration:** The 'Champions' segment, despite representing only 21.9% of the customer base, generated an aggregate monetary value of **£4.56 Million**—over 50% of the total measured revenue.

## 💡 Strategic Recommendations
1. **Evidence-Based Bundling:** Deploy "frequently bought together" algorithms focused on the high-lift REGENCY product family to drive attachment rates.
2. **Segment-Specific Interventions:** Pivot from mass-marketing to targeted action: deploy loyalty cross-sells for Champions and targeted win-back experiments for the 972 customers identified in the 'Hibernating' segment.
3. **Assortment Management:** Protect product breadth and availability during the 11 identified peak-season weeks, as breadth mathematically correlates with peak weekly sales performance.

## 📁 Repository Contents
* `CIA_4_MA_25121007 (1).pdf`: Comprehensive executive report containing exploratory data analysis, ML model evaluation, and the Business Impact Framework.
* `Online_Retail_Combined_Continued (1).xlsx`: Raw transactional dataset containing 551,012 invoices.
* `marketing_analytics_dashboard.ipynb`: Python code for Apriori, RFM, ML modeling, and KPI dashboard generation.
