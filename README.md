# hackaton1
The repository for the first part of the hackaton
# 🏡 Airbnb Availability Predictor

This project aims to predict whether an Airbnb listing will be **available on a specific date**, using machine learning techniques and three different datasets from Valencia.  
The work is divided into two main components:

1. **Data Preparation** – merging, cleaning, feature engineering.  
2. **Model Training** – building and evaluating ML models to classify availability.

---

## 🚀 Project Motivation

Understanding Airbnb availability patterns helps:
- Travelers find properties more efficiently.
- Hosts optimize their pricing and occupancy.
- Platforms improve search ranking and recommendations.

By combining property attributes, host characteristics, review information, and daily calendar availability, we build a model that predicts whether a listing will be available on a given date.

---

## 📂 Dataset Overview

We work with **three CSV datasets from Valencia**:

### **1. `listings.csv`**
Contains:
- Property attributes (room type, beds, bathrooms, etc.)
- Host characteristics (host status, verification, response rate…)
- Location information
- Review scores and overall listing metadata

### **2. `calendar.csv`**
Daily availability information:
- `date`
- `available` (target variable)
- `price`, `adjusted_price`
- `minimum_nights`, `maximum_nights`

### **3. `reviews.csv`**
Contains individual customer reviews:
- reviewer information
- comments (text)
- timestamps

Because reviews are extremely granular, we aggregate them at the **listing level** (e.g., number of reviews, average review length).

---

## 🔗 Data Preparation

Steps followed during preprocessing:

1. **Load all datasets**
2. **Merge them** 
3. **Drop irrelevant or redundant columns** (e.g., text-heavy fields, URLs, metadata)
4. **Feature engineering**, including:
   - numerical features from listings  
   - host characteristics  
   - calendar-based attributes  
   - aggregated review statistics  
5. **Final dataset structure**: one row per `(listing_id, date)` pair

### Features kept in the final dataset  
`TBD` — will be completed in the next part of the hackaton.

---

## 🧠 Machine Learning Objective

We frame the problem as a **binary classification task**:

> **Predict whether a listing will be available ("t") or not ("f") on a given date.**

### Models tested  
`TBD` — model list (e.g., Logistic Regression, Random Forest...)

---

## 📊 Results

Performance metrics such as:

- Accuracy  
- F1-score  
- Precision  
- Recall  
- Confusion Matrix  

will be reported here once the model is finalized.

**Current results:**  
`TBD`

---

## 📦 Environment Setup

To reproduce the environment, install micromamba or conda and run:

```bash
micromamba create -f environment.yml
micromamba activate hackathon-ai
