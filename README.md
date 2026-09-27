# 🎬 Movie Recommendation Engine

A **content-based movie recommendation engine** built with Python and Streamlit that recommends similar movies based on their plot, cast, director, keywords, and spoken language.

The project demonstrates an end-to-end recommendation workflow, from **data preprocessing and feature engineering to text vectorization, similarity calculation, and an interactive web application**.

---

## 🌐 Demo

<p align="center">
  <img src="assets/Movie-Recommender-Demo.gif" alt="Movie Recommendation Engine Demo" width="700">
</p>

---

## 📌 Project Overview

The system uses movie metadata to identify similarities between movies and generate personalised recommendations based on the selected movie.

Information such as the movie overview, cast, director, keywords, and spoken language is combined into a single feature representation. These features are transformed into numerical vectors using **CountVectorizer**, and movie similarity is calculated to identify the most relevant recommendations.

The recommendation engine is integrated into an interactive **Streamlit web application**.

### 🎯 Objective

Given a movie selected by the user:

**Input:** Movie title

**Output:** A list of similar movie recommendations

---

## 🔄 Recommendation Pipeline

```text
Movie Dataset
     │
     ▼
Data Cleaning & Preprocessing
     │
     ▼
Feature Engineering
     │
     ▼
Combine Movie Metadata
     │
     ▼
Create Feature Tags
     │
     ▼
CountVectorizer
     │
     ▼
Movie Feature Vectors
     │
     ▼
Similarity Calculation
     │
     ▼
Similar Movie Retrieval
     │
     ▼
Streamlit Web Application
```

---

## 🧠 Recommendation Approach

### Content-Based Filtering

The system uses **content-based filtering** to recommend movies that are similar to a movie selected by the user.

Movie attributes are combined to create a `tags` feature containing information such as:

* Movie overview
* Cast
* Director
* Keywords
* Spoken language

These textual features are converted into numerical representations using **Bag of Words (CountVectorizer)**.

The similarity between movies is then calculated based on their feature vectors. Movies with higher similarity scores are returned as recommendations.

---

## ✨ Features

* 🎬 Select a movie and receive similar movie recommendations
* 🔎 Content-based movie similarity
* 📝 Uses plot, cast, director, keywords, and language information
* 🤖 Bag of Words text representation
* 📊 Vector-based similarity calculation
* 🌐 Interactive Streamlit web application
* ⚡ Fast recommendation generation after preprocessing

---

## 🛠️ Technologies Used

| Technology           | Purpose                                       |
| -------------------- | --------------------------------------------- |
| **Python**           | Core programming language                     |
| **Pandas**           | Data manipulation and preprocessing           |
| **NumPy**            | Numerical computation                         |
| **Scikit-learn**     | Text vectorization and similarity calculation |
| **Streamlit**        | Interactive web application                   |
| **Jupyter Notebook** | Experimentation and model development         |

---

## 📊 Dataset

The project uses the **TMDB Movies Daily Updates** dataset provided by **Alan Vourch** on Kaggle.

[TMDB Movies Daily Updates Dataset — Kaggle](https://www.kaggle.com/datasets/alanvourch/tmdb-movies-daily-updates?utm_source=chatgpt.com)

The dataset provides movie metadata that can be used to analyse relationships between movies and build content-based recommendations.

---

## ▶️ Running the Project

### 1. Clone the repository

```bash
git clone https://github.com/simran2104/movie-recommendation-engine.git
cd movie-recommendation-engine
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the Streamlit application

```bash
streamlit run app.py
```

The application will open in your browser, where you can select a movie and generate recommendations.
