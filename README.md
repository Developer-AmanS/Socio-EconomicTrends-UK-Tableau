📊 **Socio-Economic Trends in England & Wales: Visual Analytics & Bayesian Insights**

🚀 **Project Overview**

Welcome to a deep dive into the socio-economic landscape of England and Wales!
This project explores how housing tenure, occupation, accommodation type, and economic activity evolved between the 2011 and 2021 censuses.
Key highlights:

🧹 Data cleaning, transformation, and merging of complex census datasets

🧠 Bayesian imputation to handle merged districts and boundary changes

📈 Interactive Tableau dashboards for visual exploration

🧬 Dimensionality reduction (t-SNE, PCA) to reveal hidden clusters and trends

🗂️ Data Sources
2011 Census: Area Code, Local Authority, Year, Economic Activity, Ethnic Group, Observation

2021 Census: Area Code, Local Authority, Economic Activity, Ethnic Group, Observation, Year

Lookup Table: Maps 2011 area codes to 2021 merged codes

Derived Files: Bayesian-imputed splits, PCA/t-SNE projections

🧹 **Data Preparation & Processing**
Standardization: Consistent labels for tenure, accommodation, economic activity, etc.

Cleaning: Remove irrelevant or missing entries.

Geographic Alignment:

🔄 Use lookup table to map 2011 districts to 2021 merged districts.

🧠 Bayesian Ridge Regression predicts splits for merged districts using 2011 patterns.

Aggregation & Pivoting: Prepare data for both visualization and projection (PCA/t-SNE).

🧠 **Bayesian Disaggregation/Imputation**
Problem: Some 2021 districts are aggregates of multiple 2011 districts.
Solution:

Use 2011 distributions as a Dirichlet prior.

Model 2021 total as a multinomial over sub-districts.

Sample posterior splits with PyMC.

Output: Posterior mean & credible intervals for each sub-district’s 2021 count.

🔬 **Dimensionality Reduction**
PCA: Reveals main axes of variation in accommodation data.
t-SNE: Visualizes clusters in occupation data.

📊 **Visualization (Tableau Dashboards)**
Choropleth Maps: Spatial patterns & changes

Bar Charts & Dot Plots: Category comparisons

Heatmaps: Quick identification of high/low values

Scatter Plots: PCA/t-SNE projections

🏆 **Key Results & Insights**
📉 Owned properties fell from 64.33% to 62.30% (2011–2021)

🏠 Flats are mostly rented; detached houses are mostly owned

👩‍💼 Professionals saw the highest increase in representation

🌍 Regional disparities: North-south differences in population & tenure shifts

📝 **Dashboard Navigation Guide**
**Dashboard 1-2:** Occupation, Tenure & Population Density
🗺️ Choropleth: Population density change by occupation & tenure

🧬 t-SNE: Occupation distribution clusters

📋 Table: Majority tenancy by occupation

📊 Bar: Ownership by occupation

**Dashboard 3-4:** Accommodation Type & Tenure Trends
🗺️ Choropleth: Accommodation & tenure change

📊 Bar: Owned vs Rented over time

🔥 Heatmap: Accommodation by tenure

🧬 PCA: Accommodation clusters

**Dashboard 5:** Economic Activity & Tenure
🗺️ Choropleth: Density change by economic activity & tenure

📈 Dot Plot: Economic activity trends by tenure

🔥 Heatmap: Economic status by tenure

📊 Bar: Economic activity trends by tenure

🧑‍🔬 **Evaluation**
Peer review: High marks for visual appeal, interactivity, and insightfulness

Feedback:

👍 Color & layout praised

⚠️ Some performance issues noted

🏷️ Legends and tooltips improved for clarity
