# term_project_32190
# Environmental and Socioeconomic Factors Affecting Lung Cancer: A Comparative Study of India and Canada
# Introduction #
Lung cancer remains one of the leading causes of cancer-related deaths worldwide, with environmental and socioeconomic factors playing a significant role in its prevalence. This study aims to compare lung cancer incidence in India and Canada, analyzing how various environmental, occupational, and socioeconomic factors contribute to the disease. The goal is to identify patterns, risk factors, and potential areas for intervention to reduce lung cancer rates in both countries

# Motivation #
Understanding the factors influencing lung cancer can help policymakers and healthcare professionals develop better prevention strategies. India and Canada have stark differences in air quality, smoking rates, healthcare access, and economic conditions, making them ideal for a comparative study. This project will provide valuable insights into how these differences impact lung cancer trends.

# Project Goals #
- Analyze historical air and water pollution levels,smoking data and the other factors in India and Canada
- Identify correlations between datas and lung cancer incidence rates
- Comparing the data between India and Canada, which are very different from each other, in order to ensure that the level of pollution might affect lung cancer.
- Use statistical techniques to evaluate the significance of these correlations
- Visualize trends and findings effectively
- Provide insights into possible policy recommendations
-  # In general:
      - This project aims to highlight the far-reaching consequences of environmental pollution. Comparing India, a country struggling with high pollution levels, to Canada, which has significantly cleaner          air and water, allows for a deeper understanding of how different environmental conditions impact public health. Through this research, we hope to shed light on the need for comprehensive pollution          control measures that address both air and water quality. This study will provide insights into how different living conditions contribute to lung cancer prevalence. Through this research, we hope 
        to emphasize the importance of targeted public health policies, pollution control measures, and improved healthcare accessibility in mitigating lung cancer risks.
# Hyphotesis  #
# - H0 (Null Hypothesis):
-There is no significant relationship between environmental/socioeconomic factors and lung cancer incidence.

# -HA (Alternative Hypothesis - senin main hipotezin):
-Environmental and socioeconomic factors significantly affect lung cancer incidence rates.
    
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

**My final and combined CSV file:** [Click here to view](./final_clean_combined_dataset.csv)

### 🔍 Data Analysis

**1. Data Preprocessing**
-Datasets from multiple sources — including air pollution, water pollution, smoking rates, healthcare access, population, and lung cancer incidence — were collected and compiled.
-First we determine the effect of each attribute to outcome within each country
-All datasets were filtered to include only India and Canada, allowing for a focused comparative analysis.
-The data were aligned by year and country, and merged into a single unified dataset for analysis.
-Missing data were cleaned and handled appropriately using techniques such as interpolation or mean imputation.

**2. Exploratory Data Analysis (EDA)**
-The distributions of all independent variables were examined (e.g., PM2.5, PM10, NO2, water pollution index, smoking rates, healthcare spending).
-Separate time-series plots were created for India and Canada to visualize environmental and socioeconomic trends.
-Preliminary observations showed that India has generally higher levels of air and water pollution, along with elevated smoking rates, compared to Canada.

**3. Correlation Analysis**
-The relationships between each independent variable and lung cancer incidence were measured using Pearson and Spearman correlation coefficients.
-Correlation matrices were generated to assess the strength and direction of associations.
-Notably, PM2.5(I named it "Air Pollution" based on the information) and smoking rates exhibited a positive correlation with lung cancer rates, suggesting that these factors may be significant contributors.

**4. Regression Modeling**
-A Multiple Linear Regression model was constructed to determine which factors most significantly impact lung cancer incidence.
-Dependent variable: Lung Cancer Incidence Rate
-Independent variables: Air Pollution, water pollution index, smoking rate, healthcare access, population over age 65
The model was evaluated using:
  - correlation value is calculated
  - p-values to test the statistical significance of each factor.

**5. Visualization**
-Heatmaps were used to visually represent correlations between all variables.
-Scatter plots were created to illustrate the relationships between individual variables and lung cancer incidence.
-Box plots compared average values of key variables between India and Canada.

## 🔍 Findings and Hyphotesis
## **The Comparision of India**

 **🔵Testing: Tobacco Use vs Lung Cancer Mortality**
 
H0 (Null Hypothesis): There is no significant relationship between Tobacco Use and Lung Cancer Mortality.

HA (Alternative Hypothesis): There is a significant relationship between Tobacco Use and Lung Cancer Mortality.

Spearman Correlation (ρ) = -0.990

p-value = 0.0000

✅ Result: Null Hypothesis rejected (significant relationship detected)

![image](https://github.com/user-attachments/assets/e0f86a84-577c-4a20-bc86-53cba932ded7)

 **🔵 Testing: Air Pollution vs Lung Cancer Mortality**
 
H0 (Null Hypothesis): There is no significant relationship between Air Pollution and Lung Cancer Mortality.

HA (Alternative Hypothesis): There is a significant relationship between Air Pollution and Lung Cancer Mortality.

Spearman Correlation (ρ) = -0.875

p-value = 0.0000

✅ Result: Null Hypothesis rejected (significant relationship detected)

![image](https://github.com/user-attachments/assets/92203778-738d-476a-b2b0-257eaa99a5f9)


 **🔵 Testing: Water Pollution vs Lung Cancer Mortality**
 
H0 (Null Hypothesis): There is no significant relationship between Water Pollution and Lung Cancer Mortality.

HA (Alternative Hypothesis): There is a significant relationship between Water Pollution and Lung Cancer Mortality.

Spearman Correlation (ρ) = -0.700

p-value = 0.0000

✅ Result: Null Hypothesis rejected (significant relationship detected)

![image](https://github.com/user-attachments/assets/6395c324-c32b-4f87-b492-82aa74869339)


 **🔵 Testing: Health Expenditure vs Lung Cancer Mortality**
 
H0 (Null Hypothesis): There is no significant relationship between Health Expenditure and Lung Cancer Mortality.

HA (Alternative Hypothesis): There is a significant relationship between Health Expenditure and Lung Cancer Mortality.

Spearman Correlation (ρ) = 0.975

p-value = 0.0000

✅ Result: Null Hypothesis rejected (significant relationship detected)

![image](https://github.com/user-attachments/assets/1ead638a-fab4-4627-b51c-ac8279045c2c)


 **🔵 Testing: Doctors per 1,000 vs Lung Cancer Mortality**
 
H0 (Null Hypothesis): There is no significant relationship between Doctors per 1,000 and Lung Cancer Mortality.

HA (Alternative Hypothesis): There is a significant relationship between Doctors per 1,000 and Lung Cancer Mortality.

Spearman Correlation (ρ) = 0.969

p-value = 0.0000

✅ Result: Null Hypothesis rejected (significant relationship detected)

![image](https://github.com/user-attachments/assets/be973d9d-0b8e-4520-ba93-38d6c07e1741)


**Comparision Table**


![image](https://github.com/user-attachments/assets/88ac205d-9057-4605-ad69-253768d5051d)

-📌 Interpretation 

  -All five variables show statistically significant relationships with lung cancer mortality in India (p < 0.05).

  -Tobacco Use and Air Pollution have strong negative correlations, suggesting that as these factors increase, lung cancer mortality tends to rise.

  -Health Expenditure and Doctors per 1,000 exhibit strong positive correlations, implying that as healthcare access improves, mortality rates also increase — which may seem counterintuitive. This could reflect a lag effect or improved diagnosis/reporting in better-funded systems.

  -Water Pollution also shows a significant negative relationship.


## **The Comparision of Canada**

 **🔎 Testing: Tobacco Use**

H0: There is no relationship between Tobacco Use and Lung Cancer Mortality.

H1: There is a relationship between Tobacco Use and Lung Cancer Mortality.

Spearman ρ = 0.835, p-value = 0.00000001

✅ Reject H0 (Significant relationship detected)

![image](https://github.com/user-attachments/assets/f79aa3c8-8841-4bc7-afc3-e7ae92e54480)


 **🔎 Testing: Air Pollution**
 
H0: There is no relationship between Air Pollution and Lung Cancer Mortality.

H1: There is a relationship between Air Pollution and Lung Cancer Mortality.

Spearman ρ = 0.659, p-value = 0.00005560

✅ Reject H0 (Significant relationship detected)

![image](https://github.com/user-attachments/assets/14c80bb1-8cdd-4fe0-8624-2877d6426e14)


 **🔎 Testing: Water Pollution**
 
H0: There is no relationship between Water Pollution and Lung Cancer Mortality.

H1: There is a relationship between Water Pollution and Lung Cancer Mortality.

Spearman ρ = 0.587, p-value = 0.00052195

✅ Reject H0 (Significant relationship detected)

![image](https://github.com/user-attachments/assets/6bb16bc9-c8ac-43b3-b8e7-599b7d91b133)


 **🔎 Testing: Health Expenditure**
 
H0: There is no relationship between Health Expenditure and Lung Cancer Mortality.

H1: There is a relationship between Health Expenditure and Lung Cancer Mortality.

Spearman ρ = -0.811, p-value = 0.00000003

✅ Reject H0 (Significant relationship detected)


![image](https://github.com/user-attachments/assets/049eb6ed-8bea-4bb1-a90d-9a69544a7549)



 **🔎 Testing: Doctors per 1,000**
 
H0: There is no relationship between Doctors per 1,000 and Lung Cancer Mortality.

H1: There is a relationship between Doctors per 1,000 and Lung Cancer Mortality.

Spearman ρ = -0.841, p-value = 0.00000000

✅ Reject H0 (Significant relationship detected)


![image](https://github.com/user-attachments/assets/4e779536-39c5-486c-b368-f643e7c563ff)


**Comparision Table**

![image](https://github.com/user-attachments/assets/b6ea0d0a-2d21-478e-ae12-8c5c477ced29)

-📌 Key Observations:

  -Tobacco Use:
A very strong positive correlation (ρ = 0.835) suggests that increased tobacco use is strongly associated with higher lung cancer rates. This is one of the most critical factors influencing the disease.


  -Air Pollution:
Shows a moderately strong positive correlation (ρ = 0.659), supporting the idea that poor air quality significantly contributes to lung cancer incidence.


  -Water Pollution:
Displays a weaker but still meaningful positive correlation (ρ = 0.587), indicating environmental pollution in general is a relevant factor.


  -Health Expenditure:
Strong negative correlation (ρ = -0.811) suggests that higher investment in healthcare is associated with lower lung cancer rates, possibly due to better prevention and early diagnosis.


  -Doctors per 1,000:
The most negative correlation (ρ = -0.841), indicating that greater healthcare accessibility (measured by medical staff availability) is strongly linked to lower incidence rates.


## **After examining each country individually, we conducted a comparative analysis of all variables between India and Canada to look at the difference.**##

![image](https://github.com/user-attachments/assets/95a2d7aa-a99f-451c-b1ed-683a2264d13e)

![image](https://github.com/user-attachments/assets/a5e0388a-d127-4d9b-9ddc-5fce40131d78)

# T-test Results:
> T-statistic: 34.783227715563314

> P-value: 2.352888101332243e-32

> Result: Reject the null hypothesis. PM2.5 levels in India and Canada are significantly different.

![image](https://github.com/user-attachments/assets/31fb9aad-b67f-4f43-99e6-a8351fd51fa4)

![image](https://github.com/user-attachments/assets/6fa44bad-7d53-4277-84aa-979fd6ae243d)

# -T-test Results:
> T-statistic: -57.41459263384998

> P-value: 2.156445105185347e-32

> Result: Reject the null hypothesis. Health Expenditure Per Capita (USD PPP) levels in India and Canada are significantly different.

![image](https://github.com/user-attachments/assets/a15687db-cdd7-4eac-8549-656861be4b6b)

![image](https://github.com/user-attachments/assets/313d5697-776d-4c6d-a3fe-c152332efd75)

 # T-test Results:
> T-statistic: 11.60051334193618

> P-value: 2.681344669739041e-16

> Result: Reject the null hypothesis. Water Pollution levels in India and Canada are significantly different.

## Canada vs India: Lung Cancer Mortality

![image](https://github.com/user-attachments/assets/82f2bd63-873c-4860-af9f-94fe7c928bd7)

**Summary**
> The chart shows a contrasting trend in lung cancer mortality between Canada and India over time.  
> While Canada demonstrates a steady **decline**—likely due to effective tobacco control policies, early diagnosis, and better healthcare—India exhibits a **consistent increase**, suggesting a growing environmental and public health burden.  
> By 2020, India surpasses Canada in lung cancer mortality, highlighting the urgent need for policy intervention, especially around pollution and tobacco control.

**📌As a result** :Based on the correlation analysis results where p-values were consistently below 0.05, we reject the null hypothesis (H₀).  
Thus, we accept the alternative hypothesis (H₁), concluding that environmental and socioeconomic factors significantly affect lung cancer incidence rates.


## You can reach my code: [Dosyaya Gitmek İçin Tıklayın](./main.ipynb)


## 🧠 Machine Learning Analysis: Country-Specific Modeling of Lung Cancer Mortality

To explore the relationship between environmental and socioeconomic factors and lung cancer mortality, we developed supervised machine learning models using country-separated datasets for **India** and **Canada**. Instead of combining the two countries, we trained models individually, aiming to capture regional patterns more effectively and avoid misleading generalizations.

We utilized four regression models:
- Linear Regression
- K-Nearest Neighbors (KNN)
- Decision Tree Regressor
- Random Forest Regressor

Each model was evaluated using **5-Fold Cross-Validation** to ensure robustness and avoid overfitting.

---

### 🔍 Features Used (Independent Variables)

- Tobacco Use (combined)
- Tobacco Smoking (combined)
- Cigarette Smoking (combined)
- Air Pollution (PM2.5)
- Water Pollution
- Health Expenditure Per Capita (USD, PPP)
- Doctors per 1,000 population
- Hospital Beds per 1,000 population
- Population Density

---

### Target Variable
- **Lung Cancer Mortality** (per population)

---

## 📈 Model Performance by Country

### 🇮🇳 India

| Model              | R² Score | RMSE  |
|--------------------|----------|-------|
| Linear Regression  | 0.993    | 0.020 |
| KNN                | 0.961    | 0.047 |
| Decision Tree      | 0.934    | 0.061 |
| Random Forest      | 0.980    | 0.034 |

#### 🔬 India: Prediction vs Actual Graphs

**Linear Regression**  
![image](https://github.com/user-attachments/assets/1ca6fb97-c8fe-4ae4-8029-67f0558b4837)
➡️ Almost perfect fit. Predicted values align extremely well with actual mortality rates.

**KNN**  
 ![image](https://github.com/user-attachments/assets/9b00afe7-7179-45bb-9344-354b6dcb0841)

➡️ Strong fit, slightly less precise than linear regression at extremes.

**Decision Tree**  
![image](https://github.com/user-attachments/assets/b2d7e526-dff0-49b6-a2d5-277881baed27)
➡️ Captures non-linearity, but minor overfitting causes slight scatter.

**Random Forest**  
![image](https://github.com/user-attachments/assets/751c8363-9e17-4c9c-9528-735ab30cc839)
➡️ Balanced and powerful, provides strong generalization with low error.

---

### 🇨🇦 Canada

| Model              | R² Score | RMSE  |
|--------------------|----------|-------|
| Linear Regression  | 0.598    | 0.138 |
| KNN                | 0.635    | 0.132 |
| Decision Tree      | 0.238    | 0.190 |
| Random Forest      | 0.571    | 0.143 |

#### 🔬 Canada: Prediction vs Actual Graphs

**Linear Regression**  
 ![image](https://github.com/user-attachments/assets/c06e6b35-3138-40c6-b1b6-3744f1999a81)
➡️ Moderate fit. The model captures the main trend but shows more residual scatter.

**KNN**  
![image](https://github.com/user-attachments/assets/c9ce0b04-bd2e-4775-9289-2e368bae69fa)
➡️ Slightly better than linear regression, with localized prediction strength.

**Decision Tree**  
![image](https://github.com/user-attachments/assets/0fa780c6-abad-4567-bbf8-a7c04050b0ee)
➡️ Weakest model for Canada. Predictions fluctuate with no clear pattern.

**Random Forest**  
![image](https://github.com/user-attachments/assets/d5ad6a28-05a9-444f-bf3c-02229a0df076)
➡️ Generalizes slightly better than the tree, but struggles with data noise and variance.

---

## Interpretation & Insights

- **India models outperformed Canada’s across all algorithms**, likely due to stronger correlations or less variance in India’s data.
- **Linear Regression and Random Forest** yielded near-perfect results for India, confirming strong linear patterns and interaction effects.
- For Canada, **KNN performed best**, suggesting localized trends that simple linear models missed.
- **Healthcare infrastructure variables** (doctors per 1,000, health expenditure) contributed meaningfully alongside pollution and smoking-related variables.
- **Decision Trees struggled with Canadian data**, possibly due to smaller sample size or noisier relationships.

---

## Limitations & Future Work

- Data is limited to two countries; broader international data could improve generalizability.
- Non-linear models like **XGBoost** or **Neural Networks** could further capture hidden patterns.
- **Feature importance analysis** and **SHAP values** would provide deeper insights into variable influence.
- Temporal patterns were not analyzed. A panel or time-series approach could identify lag effects from pollution or public health interventions.

---

## ✅ Conclusion

By splitting modeling tasks across countries and applying rigorous cross-validation, we’ve shown that **context-aware models** yield more accurate, interpretable results. The approach highlights the importance of both environmental and healthcare-related factors in predicting lung cancer mortality — and sets the stage for broader, global modeling in future work.
