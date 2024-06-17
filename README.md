# Personalized Cancer Diagnosis

## Overview
This project classifies genetic variations/mutations based on text-based clinical literature to aid personalized cancer treatment. The data is sourced from Memorial Sloan Kettering Cancer Center (MSKCC) via a Kaggle competition.

## Table of Contents
1. [Business Problem](#business-problem)
2. [Machine Learning Problem Formulation](#machine-learning-problem-formulation)
3. [Performance Table of Models](#performance-table-of-models)
4. [Conclusion and Future Work](#conclusion-and-future-work)
5. [References](#references)

## Business Problem
Classify genetic variations/mutations based on evidence from clinical literature to enhance the personalization of cancer treatment.

## Machine Learning Problem Formulation
- **Data Files:**
  - `training_variants`: Contains `ID`, `Gene`, `Variation`, `Class`
  - `training_text`: Contains `ID`, `Text`
- **Type of Problem:** Multi-class classification
- **Performance Metric:** Multi-class log-loss
- **Dataset Split:** Train (64%), Cross Validation (16%), Test (20%)

## Performance Table of Models

| Models                               | Train   | CV      | Test    | Misclassified (%) |
|--------------------------------------|---------|---------|---------|-------------------|
| LR (Class balanced) BOW (bi-grams)   | 0.7335  | 1.041   | 1.0984  | 0.3477            |
| LR (Class unbalanced) BOW (bi-grams) | 0.7272  | 1.0412  | 1.0895  | 0.3533            |
| NB TFIDF                             | 0.7804  | 1.1437  | 1.179   | 0.3665            |
| KNN TFIDF                            | 0.6616  | 1.0031  | 1.0897  | 0.35528           |
| LR (Class balanced) TFIDF            | 0.5479  | 0.9628  | 0.98    | 0.3383            |
| LR (Class Unbalanced) TFIDF          | 0.5371  | 1.004   | 1.0059  | 0.3402            |
| Linear SVM TFIDF                     | 0.7966  | 1.0795  | 1.1097  | 0.3345            |
| Random forest TFIDF                  | 0.8395  | 1.1834  | 1.1822  | 0.4097            |
| Random forest Response coding        | 0.066   | 1.2127  | 1.3088  | 0.4436            |
| LR (Class balanced) feature eng.     | 1.1457  | 1.3441  | 1.3973  | 0.4807            |
| LR (Class Unbalanced) feature eng.   | 1.1908  | 1.3475  | 1.4088  | 0.468             |

## Conclusion and Future Work
This project successfully classifies genetic mutations to aid personalized cancer treatment. Future work includes:
- Implementing advanced feature engineering techniques.
- Exploring deep learning models for improved accuracy.
- Developing real-time prediction systems for clinical use.

## References
- [Kaggle Competition](https://www.kaggle.com/c/msk-redefining-cancer-treatment/)
- [Forbes Article](https://www.forbes.com/sites/matthewherper/2017/06/03/a-new-cancer-drug-helpedalmost-everyone-who-took-it-almost-heres-what-it-teaches-us/#2a44ee2f6b25)
- [YouTube Video 1](https://www.youtube.com/watch?v=UwbuW7oK8rk)
- [YouTube Video 2](https://www.youtube.com/watch?v=qxXRKVompI8)
