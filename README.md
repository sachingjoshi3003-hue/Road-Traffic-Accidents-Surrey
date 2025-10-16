### Exploring Road Traffic Accidents in Surrey  
**Module:** Data Mining and Text Analytics  
**Tools Used:** SAS Viya | Data Mining | Text Analytics | Sentiment Analysis  

---

###  Project Overview
Road traffic accidents are a major concern for public safety, transport efficiency, and the economy.  
This project analyses **road accident data from Surrey, UK (2021)** using **data mining and text analytics** techniques within **SAS Viya**.  

The study integrates **structured accident data** with **unstructured tweet data** to:
- Identify patterns and causes of accidents.  
- Predict accident severity using machine learning.  
- Analyse public sentiment towards road safety.  
- Propose actionable recommendations to reduce accident risks.  

![Project Overview](images/project_overview_banner.png)

---

###  Datasets
1. **RoadAcci_2021Surrey Dataset**
   -  **Rows:** 2,480 | **Columns:** 35  
   - **Includes:** Accident severity, weather, road type, speed limit, time, and vehicle/casualty info.  

2. **Tweets Dataset**
   -  598 text entries related to road accidents in Surrey.  
   - Used for **sentiment and topic extraction** to capture public opinions on road safety.  

---

###  Data Preparation
- Missing and invalid values filtered and imputed (median/mode).  
- Outliers examined through box plots and distribution analysis.  
- Dataset balanced to ensure fair representation of all accident severity levels (slight, serious, fatal).  
- Final cleaned dataset: **3,510 rows × 48 variables.**

![Data Cleaning Workflow](images/data_cleaning_workflow.png)

---

###  Exploratory Data Analysis (EDA)
Key findings from visualisations and summary statistics:
- **Severity:** 75% slight, 24% serious, 1% fatal.  
- **High-risk roads:** Category 6 roads recorded the most incidents.  
- **Lighting:** Most accidents occur in daylight, but night-time crashes are more severe.  
- **Time:** Accidents peak in **afternoon and evening hours** during **summer months**.  
- **Location:** Urban hotspots show higher accident density.  

![Accident Severity Distribution](images/accident_severity_chart.png)
![Road Type Distribution](images/road_type_chart.png)
![Geo Map of Accidents](images/accident_map.png)

---

###  Predictive Modelling
Four supervised machine learning models were implemented in SAS Viya:

| Model | Key Strengths | Accuracy (Test) | AUC | KS |
|--------|----------------|----------------|-----|----|
| Neural Network | Captures non-linear relationships | 90.6% | 0.9414 | 0.80 |
| Gradient Boosting (Champion Model) | High accuracy, interpretable | **96.2%** | **0.9621** | **0.83** |
| Decision Tree | Simple, fast baseline | — | — | — |
| Forest | Handles noise & variance | — | — | — |

![Model Comparison](images/model_comparison.png)
![ROC Curve](images/roc_curve.png)
![Feature Importance](images/feature_importance.png)

---

###  Text Analytics & Sentiment Analysis
- 598 accident-related tweets analysed using SAS Text Analytics.  
- Custom **concept nodes** created for:
  - Accident Severity *(fatal, serious, minor)*  
  - Sentiments *(stuck, delayed, blocked)*  
  - Contextual themes *(weather, road, location)*  
- Helped uncover negative sentiment spikes during bad weather and peak traffic hours.  

![Text Analysis Workflow](images/text_analysis_pipeline.png)
![Sentiment Word Cloud](images/sentiment_wordcloud.png)

---

###  Key Insights & Recommendations
1. **Infrastructure Improvements** in accident-prone urban zones.  
2. **Speed Control Enforcement** — install cameras in high-risk areas.  
3. **Enhanced Lighting** in poorly lit rural and suburban roads.  
4. **Weather Preparedness** — awareness campaigns for drivers in rainy/foggy conditions.  
5. **Time-Based Measures** — increase patrols and awareness in afternoon/evening peaks.  
6. **Public Education Campaigns** promoting safe driving behaviour.  

---

###  Tools & Technologies
- **SAS Viya** — Data cleaning, EDA, and predictive modelling.  
- **SAS Visual Analytics** — Graphical visualisation and dashboards.  
- **SAS Text Analytics** — Sentiment extraction and topic grouping.  
- **MS Word & Excel** — Report documentation and data summary.  

---

###  Conclusion
The integration of structured accident data and social media sentiment offers a deeper understanding of road safety in Surrey.  
Machine learning models—especially **Gradient Boosting**—proved highly effective in predicting accident severity and identifying critical risk factors.  
These insights can support **data-driven road safety strategies** and **targeted interventions** by local authorities.
