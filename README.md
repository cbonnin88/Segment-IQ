# 🛍️ Segment IQ Dashboard

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Streamlit](https://img.shields.io/badge/Streamlit-App-FF4B4B)
![Machine Learning](https://img.shields.io/badge/Machine_Learning-Scikit_Learn-orange)

A fully interactive web application designed for Product Analysts to explore customer demographics, discover distinct shopping segments using unsupervised machine learning, and predict future customer spending. 

This project was built to demonstrate end-to-end data processing, machine learning integration, and interactive visualization using a modern Python data stack.

## ✨ Key Features

* **📊 Dynamic Customer Segmentation:** Uses the **K-Means Clustering** algorithm to automatically group customers based on age and purchase behavior. Users can dynamically adjust the number of clusters ($k$) via the UI.
* **🔮 Spend Prediction AI:** Features a trained **Random Forest Regressor** that predicts a hypothetical customer's purchase amount based on their age, gender, and preferred product category.
* **⚡ Blazing Fast Data Processing:** Built with **Polars** for highly optimized, multi-threaded data ingestion and filtering, falling back to Pandas only when necessary for scikit-learn compatibility.
* **📈 Interactive Visualizations:** Utilizes **Plotly Express** to render beautiful, interactive scatter plots with rich hover-data (revealing gender, purchased items, and categories).
* **📥 Data Export:** Allows stakeholders to download the newly segmented and filtered dataset directly to a CSV file from the browser.
* **🎛️ Live Filtering:** Multi-select drop-down menus allow for instant isolation of specific customer demographics and product categories.

## 🛠️ Tech Stack

* **Frontend & Framework:** [Streamlit](https://streamlit.io/)
* **Data Manipulation:** [Polars](https://pola.rs/) & [Pandas](https://pandas.pydata.org/)
* **Machine Learning:** [Scikit-Learn](https://scikit-learn.org/) (KMeans, RandomForestRegressor, StandardScaler)
* **Data Visualization:** [Plotly Express](https://plotly.com/python/plotly-express/)

## 🚀 How to Run the Project

### Option 1: Running Locally
1. Clone this repository:
   ```bash
   git clone [https://github.com/](https://github.com/)[cbonnin88]/[Segment-iQ].git
   cd Segment-IQ
   ```

### Option 2: Running via Google Colab (Cloud)
```
!pip install streamlit polars pandas plotly scikit-learn
!npm install -g localtunnel
Write the app code to a file:

Retrieve your Colab machine IP (used as the localtunnel password):

import urllib
print(urllib.request.urlopen('[https://ipv4.icanhazip.com](https://ipv4.icanhazip.com)').read().decode('utf8').strip("\n"))
Start the server and tunnel:

import subprocess
subprocess.Popen(["nohup", "streamlit", "run", "app.py", "--server.port", "8501", "--server.headless", "true"])
!npx localtunnel --port 8501g via Google Colab (Cloud)
```


```
Project Structure
├── app.py                               # Main Streamlit application file
├── customer_shopping_behavior.csv       # Dataset used for segmentation and prediction
├── README.md                            # Project documentation
```
