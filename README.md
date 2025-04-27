# Machine Learning for Antidepressant Adverse Event Classification

## 1. Project Overview
This project applies machine learning techniques to classify adverse events (AEs) associated with antidepressants using the FDA’s FAERS database (2018–2023). It evaluates Logistic Regression, Support Vector Machines, and Clinical-BERT models to categorize AEs into standard MedDRA System Organ Classes, and investigates emerging risks via topic modelling and disproportionality analysis.

The project demonstrates end-to-end skills in clinical data cleaning, natural language processing (NLP), machine learning model development, and post-COVID impact analysis.

---

## 2. Dataset
* Source: FDA Adverse Event Reporting System (FAERS)
* Description: Reports of patient demographics, medications, adverse events, and outcomes.
* Period Covered: January 2018 – December 2023
* Records: ~1.9M raw case reports reduced to 118,577 cleaned records

---

## 3. Tools and Libraries
* Python 3: Pandas, NumPy, Seaborn, Matplotlib
* Machine Learning: Scikit-learn (Logistic Regression, SVC, TF-IDF), TensorFlow/Keras (Clinical-BERT)
* NLP: Gensim (LDA Topic Modelling), WordCloud, pyLDAvis
* Statistical Analysis: PMDARIMA, Disproportionality Analysis (PRR, ROR)

---

## 4. Methodology

### 4.1 Data Preprocessing
* Downloaded FAERS quarterly datasets from 2018–2023.
* Merged DEMO, DRUG, INDI, REAC, OUTC, and R*
