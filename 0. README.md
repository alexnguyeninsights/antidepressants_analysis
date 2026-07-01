# ⚡ Machine Learning for Antidepressant Adverse Event Classification

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
* Merged DEMO, DRUG, INDI, REAC, OUTC, and RPSR tables based on primary IDs.
* Focused on suspected antidepressant drugs and patients aged 12+.
* Mapped adverse event (AE) symptoms to MedDRA System Organ Class categories.

### 4.2 Exploratory Data Analysis (EDA)
* Visualized distributions of AE categories, antidepressant types, age, and gender groups.
* Decomposed trends over time to observe pre-, during-, and post-COVID patterns.

### 4.3 Feature Engineering
* Built TF-IDF vectors from AE textual data.
* Created COVID-period labels (pre, during, post) for additional context.
* Applied PCA (optional) for feature reduction if required for modelling efficiency.

### 4.4 Modelling
* Logistic Regression and Support Vector Classifier (SVC) models with TF-IDF features.
* Clinical-BERT fine-tuned on AE descriptions for advanced classification.
* LDA Topic Modelling to extract hidden patterns and emerging AE risks.

### 4.5 Model Evaluation
* Metrics: Accuracy, F1-score, Area Under the Curve (AUC).
* Results:

| Model                 | Accuracy | F1-score | AUC         |
|------------------------|----------|----------|-------------|
| Logistic Regression    | Moderate | Moderate | Good        |
| Support Vector Machine | High     | High     | Very Good   |
| Clinical-BERT          | Very High (~100%) | Very High | Excellent (~1.0) |

=> Clinical-BERT achieved the best performance but required significant computing resources.

---

### 4.6 Key Takeaways
* Clinical-BERT significantly improved AE classification but is resource-intensive.
* Logistic Regression and SVC are strong, lightweight alternatives for AE categorization.
* SSRIs (Selective Serotonin Reuptake Inhibitors) exhibited higher AE rates during COVID.
* Topic Modelling revealed emerging concerns like "haemorrhage" and "serotonin syndrome".

---

### 4.7 Future Improvements
* Extend analysis to other mental health indications and drug classes.
* Deploy resource-optimized BERT variants (e.g., DistilBERT) for faster classification.
* Expand disproportionality analysis across a broader medication set.
* Integrate multi-label classification to handle complex AE symptoms across categories.

---

### 4.8 How to Run
* Clone this repository.
* Install required libraries: pip install pandas numpy seaborn matplotlib scikit-learn pmdarima gensim tensorflow transformers wordcloud pyldavis
* Run the notebooks sequentially to: Preprocess and clean FAERS data, Train models (Logistic Regression, SVC, and Clinical-BERT), Perform Topic Modelling and Disproportionality Analysis, Visualise insights

---

### 4.9 Author
📧 alexnguyen.insights@gmail.com
🔗 LinkedIn: AlexNguyenInsights

