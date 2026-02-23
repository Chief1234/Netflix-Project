.

📌 Netflix Movies & TV Shows Clustering Project

This project performs Exploratory Data Analysis (EDA) and unsupervised machine learning on the Netflix Movies & TV Shows dataset.
Using TF-IDF Vectorization, K-Means Clustering, PCA, and Silhouette Score, the project groups similar titles based on their descriptions to gain insights into content patterns on Netflix.


🚀 Project Objectives

Perform EDA to understand Netflix content distribution

Convert descriptions into vectors using TF-IDF

Apply K-Means Clustering

Use Silhouette Score to find best K

Visualize clusters using PCA

Extract insights from grouped titles



📂 Dataset Details

The dataset includes the following columns:

Title

Director

Cast

Country

Date Added

Release Year

Rating

Duration

Description


🧹 Data Preprocessing & EDA

Handling missing values

Removing duplicates

Text cleaning (lowercase, remove stopwords, punctuation)

Visualizations:

Ratings distribution

Country-wise content count

Movies vs TV Shows

Top genres

Word frequency


🧠 Machine Learning Workflow
1️⃣ TF-IDF Vectorization

Converted text descriptions into numerical vectors.

2️⃣ K-Means Clustering

Grouped similar movies and shows.

3️⃣ Silhouette Score

Used to determine optimal number of clusters.

4️⃣ PCA

Reduced dimensions for visualization in 2D plots.


📊 Results & Insights

Content is grouped into clusters such as:

Romance / Drama

Comedy / Family

Thriller / Action

Documentary

PCA visualization clearly separates several clusters

Silhouette score helps in selecting best K


🛠 Tech Stack

Python

Pandas

NumPy

Matplotlib

Scikit-learn

NLP (TF-IDF Vectorizer)


📌 Future Enhancements

Build a Netflix recommendation system

Deploy using Streamlit

Use advanced NLP models (BERT, Word2Vec)


✨ Conclusion

This project uses EDA and NLP-based machine learning to cluster Netflix titles.
By applying TF-IDF, K-Means, Silhouette Score, and PCA, it uncovers meaningful patterns in content descriptions and provides strong insights into Netflix’s catalog.





