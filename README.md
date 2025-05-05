# LLM-Generated Text Detection

This repository contains the code and data for our project on distinguishing human-written from LLM-generated text using a lightweight, parameter-efficient adaptation of XLM-RoBERTa (LoRA) plus a simple classifier.

## Overview

We conducted four experimental phases:

1. **Phase 1 – Representation Comparison**  
   – TF-IDF (1–2 grams) + Logistic Regression  
   – Frozen XLM-RoBERTa CLS embeddings + Logistic Regression  

2. **Phase 2 – LoRA Adaptation**  
   a) End-to-end LoRA fine-tuning (softmax head) on 10 % subset  
   b) Extract fused LoRA CLS embeddings → train Logistic Regression on large hold-out  

3. **Phase 3 – Classifier Selection**  
   – Compare Logistic Regression, XGBoost, Linear SVM, Random Forest on LoRA embeddings  

4. **Phase 4 – Final Evaluation**  
   – Stratified 5-fold CV of the chosen pipeline (LoRA + Logistic Regression)  
   – Report Accuracy, F1-score, ROC-AUC stability and calibration  
