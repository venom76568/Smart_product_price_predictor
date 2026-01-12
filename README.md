# Amazon ML Challenge: Smart Product Price Predictor

This project is a smart implementation to predict product prices using images and catalog content. It combines deep learning embeddings with custom feature engineering like extracting units from catalog content and standardizing them and using KNN to turn messy data into accurate price tags.

---

### 🚀 Project Overview

Predicting prices from 150,000+ entries is a challenge of scale and noise. My solution uses a multimodal approach, meaning it "sees" the product via images and "reads" the description via text to find the best price.

### 🛠️ How it Works

* **Vision & Text:** Uses **OpenAI’s CLIP** for images and **SBERT** for text to create deep mathematical representations of products.
* **Smart Features:** Includes a **KNN "Lookalike" engine** that finds similar products to see how they are priced, acting like a comparison shopper and also included a logic to extract numeric values from the catalog content and **standardize** them to avoid false learning.
* **Data Cleanup:** Uses Regex to extract and standardize weights and volumes (like converting lbs and oz to grams) to avoid false learning from inconsistent units.
* **Advanced Training:** Uses **XGBoost** with 32-bit precision tuning to handle large data within limited GPU memory.

### 📈 Results

* **SMAPE Score:** Improved from **65% to 46%** through smart feature stacking and precision optimization.
* **Efficiency:** Processes 150k+ items within 3 days under strict memory limitations.

---

### 📂 Repository Structure

* `Amazon_ML_Challenge_Solution.ipynb`: The complete end-to-end code.
* `requirements.txt`: Necessary libraries to run the project.
* `submission_sample.csv`: Example output file.

### ⚙️ Installation

```bash
pip install -r requirements.txt

```

---

