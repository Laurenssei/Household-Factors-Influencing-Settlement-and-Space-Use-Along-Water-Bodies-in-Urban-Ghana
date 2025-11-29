# Household Factors Influencing Settlement and Space Use Along Water Bodies in Urban Ghana


A data analysis project examining why low-income households settle near water bodies in Ghanaian cities, the socio-economic drivers behind these locational decisions, regulatory compliance, environmental risks, and implications for urban planning and flood-risk policy.

---

## Project Description

This project analyzes survey data from **323 households** living along water bodies in informal settlements in Ghana (primarily the Kumasi Metropolitan Area). The study integrates demographic, economic, environmental, and regulatory variables to understand settlement motivations, waste disposal practices, flood exposure, and relocation willingness.

Key themes include:  
**urban informality**, **environmental justice**, **flood-risk vulnerability**, **migration and settlement patterns**, and **policy-relevant household segmentation**.

---

## Research Objectives

- Identify the primary reasons households settle near water bodies  
- Examine how demographic and economic factors relate to settlement motivations  
- Derive household typologies using clustering and MCA  
- Identify predictors of regulatory compliance (planning permits)  
- Analyze environmentally risky practices (e.g., river waste disposal)  
- Assess willingness to relocate and barriers to relocation  

---

## Dataset

- **Source:** Primary household survey (2025)  
- **Sample:** 323 households across water-adjacent informal communities  
- **Variables:**  
  - Demographics (age, sex, education, religion, ethnicity)  
  - Socioeconomic indicators (income, expenditure, occupation)  
  - Settlement history (years lived, reason for settling)  
  - Regulatory status (planning permit)  
  - Environmental practices (waste disposal, flood exposure)  
  - Perceived benefits and challenges  
  - Relocation willingness  


---

## Methods Used

- **Descriptive statistics** (`dplyr`, `kableExtra`)  
- **Association testing:**  
  - Fisher’s Exact Test (categorical variables)  
  - Kruskal-Wallis tests (continuous variables by settlement reason)  
- **Predictive modeling:**  
  - Binary/Multinomial logistic regression (`nnet`, `broom`)  
- **Unsupervised learning:**  
  - K-means clustering  
  - Hierarchical clustering  
  - Multiple Correspondence Analysis (MCA)  
- **Visualization:**  
  - `ggplot2` (stacked bars, boxplots, MCA plots, cluster plots)  
- Fully reproducible via an **R Markdown workflow**

---

## Key Findings

- **Proximity to workplace (31.4%)** is the leading motivator for settling near rivers, outweighing safety concerns  
- Households choosing workplace proximity have **lower planning permit ownership** and **shorter residency durations**  
- Four distinct **ethnic–occupational household clusters** were identified, reflecting informal labor niches  
- Logistic regression revealed **weak demographic predictors** (pseudo-R² ≈ 0.01), suggesting context-specific drivers dominate  
- Significant differences in income, expenditure, and residency length across settlement reasons  
- Households face high environmental-health risks (flooding, malaria exposure, waste accumulation) yet remain due to livelihood benefits  

---

## Folder Structure

```plaintext
├── data/                # Not included: cleaned datasets (confidential)
├── scripts/             # Supporting R scripts
├── figures/             # Auto-generated plots and visualizations
├── analysis.Rmd         # Main reproducible R Markdown report
└── README.md            # This file

How to Reproduce the Analysis
Clone the repository
git clone https://github.com/laurenssei/urban-waterbody-settlement-analysis.git
Ensure R and RStudio are installed.
Install the required R packages:
install.packages(c(
  "dplyr", "tidyr", "ggplot2", "kableExtra", "broom",
  "nnet", "cluster", "FactoMineR", "factoextra"
))
Place the cleaned dataset
data_cleaned.csv
inside the data/ folder (dataset not included in the repository).
Open:
analysis.Rmd
and click Knit, or run:
rmarkdown::render("analysis.Rmd")
A complete, fully formatted HTML/PDF report will be generated automatically.
Author
Lawrence Ankomah Sei
BSc Statistics (KNUST)
Email: seiankomhalawrence@gmail.com
