# term_project_32190
# Environmental and Socioeconomic Factors Affecting Lung Cancer: A Comparative Study of India and Canada
# 1. Introduction #
Lung cancer remains one of the leading causes of cancer-related deaths worldwide, with environmental and socioeconomic factors playing a significant role in its prevalence. This study aims to compare lung cancer incidence in India and Canada, analyzing how various environmental, occupational, and socioeconomic factors contribute to the disease. The goal is to identify patterns, risk factors, and potential areas for intervention to reduce lung cancer rates in both countries

# 2. Motivation #
Understanding the factors influencing lung cancer can help policymakers and healthcare professionals develop better prevention strategies. India and Canada have stark differences in air quality, smoking rates, healthcare access, and economic conditions, making them ideal for a comparative study. This project will provide valuable insights into how these differences impact lung cancer trends.

# 3. Project Goals #
- Analyze historical air and water pollution levels,smoking data and the other factors in India and Canada
- Identify correlations between datas and lung cancer incidence rates
- Comparing the data between India and Canada, which are very different from each other, in order to ensure that the level of pollution might affect lung cancer.
- Use statistical techniques to evaluate the significance of these correlations
- Visualize trends and findings effectively
- Provide insights into possible policy recommendations
-  # In general:
      - This project aims to highlight the far-reaching consequences of environmental pollution. Comparing India, a country struggling with high pollution levels, to Canada, which has significantly cleaner          air and water, allows for a deeper understanding of how different environmental conditions impact public health. Through this research, we hope to shed light on the need for comprehensive pollution          control measures that address both air and water quality. This study will provide insights into how different living conditions contribute to lung cancer prevalence. Through this research, we hope 
        to emphasize the importance of targeted public health policies, pollution control measures, and improved healthcare accessibility in mitigating lung cancer risks.
        
# Data Source #
The data for this study will be collected from multiple publicly available sources:

#### **Environmental Factors**
- **Air Pollution:**
  - **Global Air Pollution Dataset:**  WHO, AQI datasets, government pollution monitoring agencies (PM2.5, PM10, NO2, CO2 levels). In this data we have 12 column in this data I will just use India 
  and Canada rows. Link: https://www.kaggle.com/datasets/hasibalmuzdadid/global-air-pollution-dataset(Kaggle)
  - **India:** In this data there are 16 columns which shows the air quality by looking at each month information sets. In this dateset I will just use for India in order to show further the pollution. 
  Link: https://www.kaggle.com/datasets/shruthiiiee/asia-2023-air-report-2000-cities (Kaggle)
  - **Canada:** (https://www.canada.ca/en/environment-climate-change/services/air-quality-health-index.html) [Air Quality Health Index (AQHI)] 

- **Water Pollution:**
  -- **World's Air Quality and Water Pollution Dataset:** UN water quality reports and air quality levels. In this data there are 5 colums. I will just use India and Canada rows in this dataset.
- Link: https://www.kaggle.com/datasets/victorahaji/worlds-air-quality-and-water-pollution-dataset (Kaggle)

- 
   
#### **Socioeconomic Factors**
- **Smoking and Tobacco Use:**  
  - **India:** (https://ntcp.nhp.gov.in/)  [Global Adult Tobacco Survey (GATS)]
  - **Canada:** (https://www.canada.ca/en/health-canada/services/canadian-tobacco-nicotine-survey.html)  [Canadian Tobacco and Nicotine Survey (CTNS)]

- **Healthcare Accessibility:**  
  - **India:** (https://www.cbhidghs.nic.in/)  [National Health Profile]
  - **Canada:** (https://www.cihi.ca/)  [Canadian Institute for Health Information (CIHI)]

- **World Population Dataset:**
   - **India and Canada:** https://www.kaggle.com/datasets/iamsouravbanerjee/world-population-dataset (Kaggle)


#### **Outcome**
   - **Lung Cancer Rates :** National health statistics, research papers (cancer incidence by region). In this data there are 6 columns. I will just use India and Canada rows. https://www.who.int/data/gho/data/indicators/indicator-details/GHO/ambient-air-pollution-attributable-deaths (World Health Organization)
## 🔍 Data Analysis

## 1. Data Preprocessing
-Datasets from multiple sources — including air pollution, water pollution, smoking rates, healthcare access, population, and lung cancer incidence — were collected and compiled.
-First we determine the effect of each attribute to outcome within each country
-All datasets were filtered to include only India and Canada, allowing for a focused comparative analysis.
-The data were aligned by year and country, and merged into a single unified dataset for analysis.
-Missing data were cleaned and handled appropriately using techniques such as interpolation or mean imputation.

## 2. Exploratory Data Analysis (EDA)
-The distributions of all independent variables were examined (e.g., PM2.5, PM10, NO2, water pollution index, smoking rates, healthcare spending).
-Separate time-series plots were created for India and Canada to visualize environmental and socioeconomic trends.
-Preliminary observations showed that India has generally higher levels of air and water pollution, along with elevated smoking rates, compared to Canada.

## 3. Correlation Analysis
-The relationships between each independent variable and lung cancer incidence were measured using Pearson and Spearman correlation coefficients.
-Correlation matrices were generated to assess the strength and direction of associations.
-Notably, PM2.5(I named it "Air Pollution" based on the information) and smoking rates exhibited a positive correlation with lung cancer rates, suggesting that these factors may be significant contributors.

## 4. Regression Modeling
-A Multiple Linear Regression model was constructed to determine which factors most significantly impact lung cancer incidence.
-Dependent variable: Lung Cancer Incidence Rate
-Independent variables: Air Pollution, water pollution index, smoking rate, healthcare access, population over age 65
The model was evaluated using:
  - correlation value is calculated
  - p-values to test the statistical significance of each factor.

## 5. Visualization
-Heatmaps were used to visually represent correlations between all variables.
-Scatter plots were created to illustrate the relationships between individual variables and lung cancer incidence.
-Box plots compared average values of key variables between India and Canada.

## 🔍 Findings
## The Comparision of India
-🔵Testing: Tobacco Use vs Lung Cancer Mortality
H0 (Null Hypothesis): There is no significant relationship between Tobacco Use and Lung Cancer Mortality.
HA (Alternative Hypothesis): There is a significant relationship between Tobacco Use and Lung Cancer Mortality.

Spearman Correlation (ρ) = -0.990
p-value = 0.0000
✅ Result: Null Hypothesis rejected (significant relationship detected)

![image](https://github.com/user-attachments/assets/e0f86a84-577c-4a20-bc86-53cba932ded7)

-🔵 Testing: Air Pollution vs Lung Cancer Mortality
H0 (Null Hypothesis): There is no significant relationship between Air Pollution and Lung Cancer Mortality.
HA (Alternative Hypothesis): There is a significant relationship between Air Pollution and Lung Cancer Mortality.

Spearman Correlation (ρ) = -0.875
p-value = 0.0000
✅ Result: Null Hypothesis rejected (significant relationship detected)
![image](https://github.com/user-attachments/assets/92203778-738d-476a-b2b0-257eaa99a5f9)


🔵 Testing: Water Pollution vs Lung Cancer Mortality
H0 (Null Hypothesis): There is no significant relationship between Water Pollution and Lung Cancer Mortality.
HA (Alternative Hypothesis): There is a significant relationship between Water Pollution and Lung Cancer Mortality.

Spearman Correlation (ρ) = -0.700
p-value = 0.0000
✅ Result: Null Hypothesis rejected (significant relationship detected)
![image](https://github.com/user-attachments/assets/6395c324-c32b-4f87-b492-82aa74869339)


🔵 Testing: Health Expenditure vs Lung Cancer Mortality
H0 (Null Hypothesis): There is no significant relationship between Health Expenditure and Lung Cancer Mortality.
HA (Alternative Hypothesis): There is a significant relationship between Health Expenditure and Lung Cancer Mortality.

Spearman Correlation (ρ) = 0.975
p-value = 0.0000
✅ Result: Null Hypothesis rejected (significant relationship detected)
![image](https://github.com/user-attachments/assets/1ead638a-fab4-4627-b51c-ac8279045c2c)


🔵 Testing: Doctors per 1,000 vs Lung Cancer Mortality
H0 (Null Hypothesis): There is no significant relationship between Doctors per 1,000 and Lung Cancer Mortality.
HA (Alternative Hypothesis): There is a significant relationship between Doctors per 1,000 and Lung Cancer Mortality.

Spearman Correlation (ρ) = 0.969
p-value = 0.0000
✅ Result: Null Hypothesis rejected (significant relationship detected)
![image](https://github.com/user-attachments/assets/be973d9d-0b8e-4520-ba93-38d6c07e1741)

## The Comparision of Canada
🔎 Testing: Tobacco Use
H0: There is no relationship between Tobacco Use and Lung Cancer Mortality.
H1: There is a relationship between Tobacco Use and Lung Cancer Mortality.
Spearman ρ = 0.835, p-value = 0.00000001
✅ Reject H0 (Significant relationship detected)
![image](https://github.com/user-attachments/assets/f79aa3c8-8841-4bc7-afc3-e7ae92e54480)


🔎 Testing: Air Pollution
H0: There is no relationship between Air Pollution and Lung Cancer Mortality.
H1: There is a relationship between Air Pollution and Lung Cancer Mortality.
Spearman ρ = 0.659, p-value = 0.00005560
✅ Reject H0 (Significant relationship detected)
![image](https://github.com/user-attachments/assets/14c80bb1-8cdd-4fe0-8624-2877d6426e14)


🔎 Testing: Water Pollution
H0: There is no relationship between Water Pollution and Lung Cancer Mortality.
H1: There is a relationship between Water Pollution and Lung Cancer Mortality.
Spearman ρ = 0.587, p-value = 0.00052195
✅ Reject H0 (Significant relationship detected)
![image](https://github.com/user-attachments/assets/6bb16bc9-c8ac-43b3-b8e7-599b7d91b133)


🔎 Testing: Health Expenditure
H0: There is no relationship between Health Expenditure and Lung Cancer Mortality.
H1: There is a relationship between Health Expenditure and Lung Cancer Mortality.
Spearman ρ = -0.811, p-value = 0.00000003
✅ Reject H0 (Significant relationship detected)
![image](https://github.com/user-attachments/assets/049eb6ed-8bea-4bb1-a90d-9a69544a7549)


🔎 Testing: Doctors per 1,000
H0: There is no relationship between Doctors per 1,000 and Lung Cancer Mortality.
H1: There is a relationship between Doctors per 1,000 and Lung Cancer Mortality.
Spearman ρ = -0.841, p-value = 0.00000000
✅ Reject H0 (Significant relationship detected)
![image](https://github.com/user-attachments/assets/4e779536-39c5-486c-b368-f643e7c563ff)

## After lloking each country individually we look at the difference of their 
