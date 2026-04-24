# 🎬 Netflix Content EDA & Clustering

> An unsupervised machine learning project that explores Netflix's content library using Exploratory Data Analysis and NLP-based K-Means Clustering to discover hidden content groups.

---

## 📌 Overview

This project analyzes the **Netflix Movies and TV Shows** dataset to uncover patterns in content type, ratings, and release trends. Using **TF-IDF vectorization** on content metadata (genres, descriptions, cast, director) and **K-Means clustering**, it segments Netflix titles into meaningful content groups — enabling insights useful for recommendation systems and content strategy.

---

## 🚀 Quick Start (Google Colab)

Click the badge below to open this notebook directly in Google Colab — no local setup needed:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/<YOUR_USERNAME>/<YOUR_REPO>/blob/main/Netflix_EDA_Clustering_ipynb.ipynb)

> ⚠️ **Replace** `<YOUR_USERNAME>` and `<YOUR_REPO>` with your actual GitHub username and repository name after uploading.

### Steps to run in Colab:
1. Click the **Open in Colab** badge above
2. Upload `NETFLIX MOVIES AND TV SHOWS CLUSTERING.csv` when prompted (or mount Google Drive)
3. Run all cells: `Runtime → Run all`

---

## 📁 Project Structure

```
📦 netflix-eda-clustering/
├── Netflix_EDA_Clustering_ipynb.ipynb              # Main analysis notebook
├── NETFLIX MOVIES AND TV SHOWS CLUSTERING.csv      # Dataset (add manually)
└── README.md                                        # Project documentation
```

> **Note:** The dataset CSV is not included in this repo. Download it from [Kaggle – Netflix Movies and TV Shows](https://www.kaggle.com/datasets/shivamb/netflix-shows) and upload it to `/content/` in Colab.

---

## 🔍 Project Pipeline

```
Load Data → EDA → Preprocessing → TF-IDF → Elbow Method → K-Means → PCA Visualization
```

| Step | Description |
|------|-------------|
| **1. Import Libraries** | pandas, numpy, matplotlib, seaborn, scikit-learn |
| **2. Load Data** | Read CSV, inspect shape, columns, missing values, data types |
| **3. Data Cleaning** | Fill nulls in director, cast, country, rating, duration; parse duration to minutes |
| **4. EDA Visualizations** | Movies vs TV Shows count, content ratings distribution, release year histogram |
| **5. Feature Engineering** | Combine `listed_in`, `description`, `cast`, `director` into a single text field |
| **6. TF-IDF Vectorization** | Convert combined text to a 5000-feature numeric matrix (stop words removed) |
| **7. Elbow Method** | Test K = 2–10; plot WCSS inertia to identify the optimal cluster count |
| **8. Silhouette Scores** | Validate cluster separation quality for each value of K |
| **9. K-Means (K=4)** | Fit final model; assign cluster labels to every title |
| **10. PCA Visualization** | Reduce TF-IDF matrix to 2D; plot clusters in a scatter plot |

---

## 📊 Key Techniques

- **Exploratory Data Analysis (EDA)** — distribution of type, rating, and release year
- **Missing Value Imputation** — mode for ratings, mean for duration, "Unknown" for text fields
- **Duration Parsing** — converting `"90 min"` / `"2 Seasons"` strings to numeric minutes
- **TF-IDF Vectorization** — NLP-based feature extraction from content metadata
- **Elbow Method + Silhouette Score** — data-driven optimal K selection
- **K-Means Clustering (K=4)** — grouping Netflix titles into 4 content clusters
- **PCA (2D)** — visualizing high-dimensional TF-IDF clusters in 2D space

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3.x | Core language |
| pandas | Data loading & manipulation |
| numpy | Numerical operations |
| matplotlib / seaborn | EDA & cluster visualizations |
| scikit-learn | TF-IDF, PCA, K-Means, Silhouette Score |
| Google Colab | Cloud notebook environment |

---

## 📦 Installation (Local Setup)

To run locally instead of Colab:

```bash
# Clone the repository
git clone https://github.com/<YOUR_USERNAME>/<YOUR_REPO>.git
cd <YOUR_REPO>

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn jupyter

# Launch Jupyter
jupyter notebook Netflix_EDA_Clustering_ipynb.ipynb
```

> Update the file path in Cell 1 from `/content/NETFLIX MOVIES AND TV SHOWS CLUSTERING.csv` to `./NETFLIX MOVIES AND TV SHOWS CLUSTERING.csv` before running locally.

---

## 📈 Results

The final model groups all Netflix titles into **4 clusters** based on genre tags, descriptions, cast, and director information. Each cluster represents a distinct content theme — for example, action movies, international dramas, children's content, or stand-up specials. Cluster labels are assigned back to the original dataframe for further profiling.

---

## 📄 Dataset

- **Source:** [Kaggle – Netflix Movies and TV Shows](https://www.kaggle.com/datasets/shivamb/netflix-shows)
- **Records:** ~8,800 titles
- **Features:** `show_id`, `type`, `title`, `director`, `cast`, `country`, `date_added`, `release_year`, `rating`, `duration`, `listed_in`, `description`

---

## 🙌 Acknowledgements

- [Kaggle](https://www.kaggle.com) for providing the Netflix dataset
- The open-source Python, scikit-learn, and NLP communities

---

## 📬 Contact

Feel free to open an issue or reach out with questions, feedback, or suggestions!

---





