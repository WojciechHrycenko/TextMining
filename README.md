# Text Mining - Bigfoot Sightings Analysis

![Project Status](https://img.shields.io/badge/Status-Completed-green)
![Course](https://img.shields.io/badge/Course-Text%20Mining-blue)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?logo=jupyter&logoColor=white)
![BERTopic](https://img.shields.io/badge/Library-BERTopic-FF0000)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit_Learn-F7931E?logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Library-Pandas-150458?logo=pandas&logoColor=white)

## Project Overview

This repository contains the coursework and analysis for a **Text Mining** project. The primary objective was to apply **BERTopic** and other text mining techniques to analyze the unstructured narratives of Bigfoot sighting reports collected by the Bigfoot Field Researchers Organization (BFRO). The project aims to uncover latent narrative themes, environmental contexts, and emotional patterns within the corpus.

## Author
* **Wojciech Hrycenko**

---

## Repository Contents

### 1. Text Mining: Bigfoot Sightings
**File:** `Text_Mining_Hrycenko.ipynb`

**Objective**
The goal of this project was to analyze the semantic and emotional structure of BFRO reports to:
1.  **Identify latent narrative themes** (e.g., distinguishing between auditory encounters vs. visual sightings).
2.  **Analyze emotional variance** by quantifying sentiment (fear vs. neutral observation) within reports.
3.  **Separate environmental contexts** and discover geospatial or temporal patterns in the sightings.

**Dataset**
The project utilizes the `bfro_reports.csv` dataset, specifically focusing on the `OBSERVED` column which contains detailed text narratives. The analysis was performed on **4,982 unique documents** after cleaning and deduplication.

**Methodology**
* **Data Analysis & Preprocessing:**
    * **Text Normalization:** Lowercasing and whitespace removal.
    * **Cleaning:** Removal of empty rows and exact duplicates to prevent model bias.
    * **EDA:** Distribution analysis of document lengths and word frequency analysis to identify domain-specific terms.
* **Feature Engineering:**
    * **Sentiment Analysis:** Utilized `TextBlob` to calculate sentiment polarity, allowing for the correlation of emotional tone with specific sighting types.
* **Modeling:**
    * **Algorithm:** **BERTopic** (a density-based clustering algorithm using transformers).
    * **Embeddings:** Generated using `SentenceTransformer`.
    * **Dimensionality Reduction:** Implemented using **UMAP**.
    * **Clustering:** Applied **HDBSCAN** to identify dense clusters of semantically similar reports.
    * **Representation:** Utilized `ClassTfidfTransformer` and `KeyBERTInspired` for extracting coherent topic representations.
* **Evaluation & Visualization:**
    * Interactive visualizations exported as HTML (e.g., `view1a_time_evolution.html`, `view4_map_no_topic0.html`).
    * Semantic landscape visualization using Word Clouds.

---

## Technologies and Libraries

The project was developed in **Python**, utilizing the following key libraries:

* **BERTopic:** For advanced topic modeling using transformer embeddings.
* **Sentence-Transformers:** For generating state-of-the-art text embeddings.
* **TextBlob:** For sentiment analysis and polarity calculation.
* **UMAP & HDBSCAN:** For dimensionality reduction and density-based clustering.
* **Pandas & NumPy:** For efficient data manipulation and numerical analysis.
* **Scikit-learn:** For text vectorization (`CountVectorizer`, `TfidfVectorizer`) and preprocessing.
* **Plotly & Matplotlib/Seaborn:** For generating interactive and static visualizations.
* **Gensim:** For coherence models and dictionary management.
* **Jupyter Notebook:** Used as the interactive development environment.

## Usage Instructions

1.  Clone this repository to your local machine.
2.  Ensure all required dependencies are installed (refer to the library list above).
3.  The dataset `bfro_reports.csv` is included in the repository.
4.  Navigate to the directory and execute the `Text_Mining_Hrycenko.ipynb` notebook to view the analysis, preprocessing steps, and interactive topic models.
5.  Open the included HTML files (e.g., `view1a_time_evolution.html`) in a web browser to interact with the exported BERTopic visualizations.
