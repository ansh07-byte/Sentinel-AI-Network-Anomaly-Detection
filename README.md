# 🛡️ Sentinel AI: Network Anomaly Detection & Threat Classification

## 📌 Project Overview
This project, developed for the **Statistical Machine Learning (CSET-211)** course, implements a hybrid machine learning framework to detect network anomalies and classify cyberattacks in real-time. 

The system uses the modern **NIDS_Bench_2026** dataset and deploys a **Random Forest** classifier for multi-class attack attribution alongside an **Isolation Forest** for unsupervised anomaly detection. The final models are served via an interactive **Streamlit** dashboard.

## 🚀 Features
*   **Data Preprocessing:** Handles missing values, removes collinear features (Pearson correlation > 0.95), and applies Z-score normalization.
*   **Dual-Model Architecture:**
    *   *Random Forest:* Supervised multi-class classification (97.76% Accuracy).
    *   *Isolation Forest:* Unsupervised zero-day anomaly detection trained on benign traffic.
*   **Live Dashboard:** A dark-mode Security Operations Center (SOC) interface built with Streamlit and Plotly. It simulates live traffic, calculates threat severity (Critical, High, Suspicious, Benign), and visualizes confidence trends in real-time.
*   **Cloud Tunneling:** Uses Cloudflare Tunnels to expose the Google Colab-hosted Streamlit app to the public internet.

## 📊 Dataset
The project utilizes the **NIDS_Bench_2026** dataset (Zenodo). 
*   *Note: Due to GitHub file size limits, the dataset is not uploaded here. You can download it from the official Zenodo repository.*
*   The test dataset contains 120,000 flow records across 71 columns.

## 🛠️ How to Run the Project
1. Open the `Network_Anomaly_Detection.ipynb` file in **Google Colab**.
2. Run the cells sequentially to install dependencies, extract the dataset, preprocess the data, and train the models.
3. The notebook will save the trained `.pkl` models and generate `app.py`.
4. Run the final cell to launch the **Streamlit Dashboard** via Cloudflare Tunnel.

## 👨‍💻 Authors
*   Ansh Raj (S25CSEU1411)
*   Maulik Joshi (S25CSEU1510)
*   Siddhi Shekhar (S25CSEU1533)
