# Early Prediction of Cognitive Decline in Older Adults

## Abstract
Alzheimer’s disease and related dementias are often detected only after significant cognitive deterioration, making early identification of high-risk individuals a critical public-health challenge.  
In this project, I built an explainable AI model to predict whether an older adult is likely to experience worsening cognitive decline based on lifestyle, medical, and mental-health indicators.

After handling extreme class imbalance using SMOTE, I trained Logistic Regression and Random Forest classifiers and evaluated them using F1-score and ROC-AUC metrics. To move beyond black-box predictions, I applied SHAP explainability to identify which factors contribute most to increased cognitive-decline risk for each individual.

The model highlights the potential role of sleep, mental distress, functional limitations, and chronic health conditions as key predictors. This work demonstrates the value of interpretable AI for supporting early screening and preventive care in aging populations.

---

## Research Motivation
Early cognitive decline is often recognized only after memory loss becomes severe, limiting treatment options. Although large population datasets contain valuable information about lifestyle and health risk factors linked to Alzheimer’s, these patterns are too complex to analyze manually.

Using explainable AI bridges this gap by:
- Modeling risk indicators at population scale
- Providing transparent, individualized prediction
- Supporting prevention and targeted screening

Scientifically, identifying cognitive decline earlier enables preventive interventions and improves long-term outcomes for aging adults.

---

## Dataset Details

| Attribute | Description |
|----------|-------------|
| Dataset Name & Source | Population-level Alzheimer’s & Cognitive Decline Indicators (derived from U.S. national and state public health surveys — Kaggle / CDC BRFSS) |
| Dataset Size | ≈ 48,000+ rows × ~50 features (after preprocessing and feature selection) |
| Population | Older adults aged 65+ across the United States |
| Data Collected | Lifestyle behaviors, mental health, cognitive function, chronic illness history, preventive healthcare |

---

## Methodology

### Data Cleaning
- Removed irrelevant and duplicate stratification columns  
- Standardized column formatting and handled missing values  

### Feature Engineering
- Selected meaningful behavioral, cognitive, and health indicators  
- Target variable: "SCD worsening in the past year"  
- Scaled and balanced dataset using SMOTE to address class imbalance  

### Models Used
- Logistic Regression (baseline interpretability)
- Random Forest Classifier (nonlinear model with stronger predictive power)

### Evaluation Approach
Evaluated on an unseen test set using:
- Precision, Recall, F1-score
- Confusion Matrix
- ROC–AUC score

### Explainable AI
- Applied SHAP to identify the most influential risk factors contributing to worsening subjective cognitive decline

---

## My Contributions

### Conceptual Contribution
- Framed the research question: Can lifestyle and health risk factors predict worsening subjective cognitive decline in older adults?
- Linked public-health statistics to early risk prediction for Alzheimer’s with a focus on prevention rather than diagnosis.

### Technical Contribution
- Built an end-to-end machine learning pipeline (data cleaning → feature engineering → resampling → model training → evaluation)
- Benchmarked Logistic Regression and Random Forest to avoid model dependence
- Implemented SMOTE to overcome extreme class imbalance
- Applied SHAP explainable AI to interpret model predictions and uncover clinically meaningful insights

---

## Insights Discovered
- Cognitive decline risk is strongly associated with modifiable lifestyle and mental-health indicators  
- Low physical activity, insufficient sleep, depression history, and caregiving-related stress emerged as top predictors  
- Results show that AI can highlight early behavioral signals before severe cognitive deterioration occurs, supporting preventive health interventions

---

## Conclusion
This project demonstrates the potential of interpretable machine learning for early prediction of cognitive decline. By combining performance metrics with SHAP-based interpretability, the system offers both reliable predictions and clinically meaningful insights that could support early screening and preventive care in aging populations.

