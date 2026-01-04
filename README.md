# stMTMV (spatio-temporal Multi Task Multi View )-Urban-Water-Quality-Prediction
Project Overview
This project focuses on urban water quality toxicity prediction using a combination of statistical, machine learning, and deep learning models.
The goal is to assess whether water is Safe or Unsafe for human consumption based on environmental, chemical, and infrastructure-related parameters.
The system compares multiple models and highlights model-specific decision differences, toxicity thresholds, and feature-level explanations to support transparent and interpretable predictions.

Dataset: An IEEE reserch paper "Predicting Urban Water Quality With Ubiquitous Data - A Data-Driven Approach" by authors Ye Liu; Yuxuan Liang; Kun Ouyang; Shuming Liu (https://ieeexplore.ieee.org/document/8988208) 
Collected and merged data from various sources like:
1. India Open Government Data – Water Quality (https://www.data.gov.in/dataset-group-name/Water%20Quality?utm_source=chatgpt.com)
2. Indian Water Quality Datasets (Kaggle) (https://www.kaggle.com/datasets/anbarivan/indian-water-quality-data?utm_source=chatgpt.com)
3. JJM Water Source Water Quality Data (India AI Portal) (https://aikosh.indiaai.gov.in/home/datasets/details/jjm_water_source_water_quality_data.html?utm_source=chatgpt.com)
4. Global Freshwater Quality (GEMStat) (https://gemstat.org/?utm_source=chatgpt.com)
5. Surface Water Quality Dataset (Research-level) (https://www.nature.com/articles/s41597-025-04715-4?utm_source=chatgpt.com)


 Models Implemented
The following models were implemented and evaluated:
Logistic Regression
ARMA (AutoRegressive Moving Average)
RC Decay Neural Network
Kalman Filter
ANN (Single View)
stMTMV (Spatio-Temporal Multi-Task Multi-View Model)

The project includes an interactive interface where users can input real-world parameters such as:
Temperature
pH level
Turbidity
Lead concentration
Chlorine level
Pipe age, length, and diameter
Industrial waste percentage
Water pressure and capacity

Each model predicts:
Toxicity level (%)
Safety label (Safe / Unsafe)
Classification metrics (Accuracy, Precision, Recall, F1-score)

Observation:
Even at similar toxicity levels (~50%), different models produce different safety labels, highlighting threshold sensitivity and decision-boundary variability.

Toxicity Prediction Visualization:
A comparative visualization plots toxicity levels across models with a 50% unsafe threshold:
Models near the threshold show label ambiguity
stMTMV predicts lower toxicity and classifies water as Safe
RC Decay (NN) shows the highest toxicity
This comparison emphasizes why multi-model evaluation is crucial in real-world water quality assessment.

Interactive Prediction Interface
Clicking “Predict Water Quality” generates real-time predictions.
Prediction Results & Explainability
For a sample input, the system reports:
Water Quality: Safe/Unsafe
Toxicity Probability
Potability Status: Water is NOT potable/ Water is potable


Feature Importance Analysis
The model also provides ranked feature importance for transparencyi.e. most to least influential factors responsible for toxicity level.


Insight:
Infrastructure-related factors (pipes, humidity, chlorine) play a significant role in determining urban water safety.

Key Takeaways
Different models may disagree near safety thresholds
stMTMV shows more conservative and stable predictions

Feature-level explanations improve trust and interpretability

Suitable for decision support in urban water management
