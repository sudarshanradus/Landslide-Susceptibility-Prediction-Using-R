# Landslide Susceptibility Prediction using Machine Learning

This project focuses on predicting landslide-prone regions in Iran using various geographical and environmental factors.  
A Random Forest Classifier is trained to classify **landslide risk** into two categories:

- TRUE → High Risk (Steep slope > 20°)
- FALSE → Low Risk

The results support decision-making for hazard monitoring and disaster management.

---

## Project Objectives

Predict landslide risk using environmental and terrain features  
Identify high-slope vulnerable areas  
Analyze model results with confusion matrix and bar plots  
Support proactive safety planning  

---

#Dataset Information

Dataset name: **Landslide_Factors_IRAN.csv**  
Records: 10,000+  
Attributes include:

| Feature | Description |
|--------|-------------|
| Elevation | Height above sea level |
| Slop.Percent | Slope percentage |
| Slop.Degrees | Slope angle |
| RiverDIST | Distance from river |
| FaultDIST | Distance from geological fault |
| Climate Type | Weather classification |
| GEO_UNIT | Geological formation |
| Landuse Type | Used for original classification |

Source: Research-based Iran landslide dataset (public domain)

---

#Machine Learning Model

| Property | Details |
|---------|---------|
| Algorithm | Random Forest Classifier |
| Target | Landslide Risk (Binary) |
| Train-Test Split | 80% training, 20% testing |
| Performance Metrics | Confusion Matrix, Classification metrics |

Works well on non-linear terrain features and mixed data types.

---

#Data Preprocessing

✔ Removed missing targets  
✔ Created binary risk label using slope threshold  
✔ Categorical columns dummy-encoded  
✔ Avoided data leakage by splitting after encoding  

---

#Technologies Used

| Tool | Purpose |
|------|--------|
| R | Model training, graphs |
| Python | Data analysis (optional) |
| caret, randomForest | ML libraries |
| ggplot2, seaborn | Visualization |

Google Colab used for execution.

---

#Results

### Confusion Matrix
Shows correct predictions for TRUE/ FALSE landslide risk categories.

### Bar Chart Output
Displays distribution comparison between predicted and actual risk labels.

Model successfully identifies high-risk areas  
Useful visualization for affected regions

---

#Key Insights

• Slope angle & terrain has highest relation to landslide events  
• Higher elevation & geologically weak areas show strong susceptibility  
• Water proximity increases risk in steep zones  

---

#How to Run

### Run in Google Colab (R Runtime)

1️⃣ Upload notebook and dataset  
2️⃣ Install required packages  
3️⃣ Run code cells from top to bottom  

Example command:

```r
randomForest(x = x_train, y = y_train, ntree = 300)
