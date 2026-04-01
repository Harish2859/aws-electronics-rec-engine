# AWS Electronics Recommendation Engine (NCF)

An end-to-end Machine Learning pipeline that predicts user ratings for Amazon Electronics products. This project was developed as a technical showcase for the **AWS Internship 2026**.

## 🚀 Project Overview
This project moves from a statistical baseline to a Deep Learning architecture to solve the "Sparsity Problem" in large-scale e-commerce datasets.

### Key Features:
* **Dataset:** 1 Million+ records from the Amazon Reviews (Electronics) 5-core dataset.
* **Architecture:** Neural Collaborative Filtering (NCF) using Embedding layers and a Multi-Layer Perceptron (MLP).
* **Optimization:** Specifically tuned for **NVIDIA Blackwell (RTX 5050)** using PyTorch Nightly & CUDA 12.8.
* **Baseline Comparison:** Successfully outperformed a Global Mean + Bias baseline, achieving a **test RMSE of 1.1334**.

## 🏗️ Technical Stack
* **Language:** Python 3.12
* **Frameworks:** PyTorch, Scikit-Learn, Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Hardware:** Lenovo LOQ (RTX 5050 Laptop GPU)

## 📊 Exploratory Data Analysis (EDA)
* **Sparsity:** The user-item interaction matrix was **99.9885% sparse**, justifying the use of Deep Learning Embeddings over traditional Matrix Factorization.
* **Distribution:** Observed a strong "Positivity Bias" with a global mean rating of **4.28/5.0**.



## ☁️ AWS Deployment Architecture (Conceptual)
Designed with AWS scalability in mind:
1.  **Data Storage:** Raw JSON files stored in **Amazon S3**.
2.  **Preprocessing:** Data cleaning handled via **AWS Glue** or SageMaker Processing jobs.
3.  **Inference:** Model deployed via **AWS Lambda** and **Amazon API Gateway** for serverless, low-latency recommendations.
4.  **Cold Start:** Implemented a fallback logic to Global Mean and Popularity-based recommendations for new users.

## 📈 Results
| Model | RMSE |
| :--- | :--- |
| **Statistical Baseline** | 1.1391 |
| **NCF (Deep Learning)** | **1.1334** |

## 🛠️ How to Run
1. Clone the repo: `git clone https://github.com/Harish2859/aws-electronics-rec-engine.git`
2. Install dependencies: `pip install -r requirements.txt`
3. Run the notebook: `jupyter notebook notebooks/01_Data_Cleaning.ipynb`

---
**Contact:** [harishm.aids2023@citchennai.net](mailto:harishm.aids2023@citchennai.net)