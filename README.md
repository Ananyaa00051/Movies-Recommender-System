
#  Movie Recommendation System (Content-Based Filtering)

A content-based movie recommendation system built using Python, NLP techniques, and cosine similarity.
This project analyzes movie metadata (genres, keywords, cast, and crew) to recommend movies similar to a given input title.

---

## 🚀 Project Overview

This project uses machine learning & Natural Language Processing (NLP) to recommend similar movies based on textual metadata from the TMDB 5000 dataset.

### ✅ Key Features

* Content-based movie recommendation system
* Text preprocessing and metadata extraction
* Feature engineering using **Bag-of-Words (BoW)**
* Cosine similarity for recommendation calculation
* Supports **case-insensitive movie search**
* Exported models using `pickle` for deployment

---

## 📂 Dataset

Dataset used: **TMDB 5000 Movies & Credits**
Available on Kaggle: *(user must download & place in working directory)*

Files used:

* `tmdb_5000_movies.csv`
* `tmdb_5000_credits.csv`

---

## 🧠 Tech Stack

| Category             | Libraries / Tools                                     |
| -------------------- | ----------------------------------------------------- |
| Language             | Python                                                |
| Data Handling        | Pandas, NumPy                                         |
| NLP                  | `ast`, tokenization, text preprocessing               |
| ML / Vectorization   | scikit-learn (`CountVectorizer`, `cosine_similarity`) |
| Storage & Deployment | Pickle                                                |

---

## 🔧 Methodology

### 1️⃣ Data Loading & Merging

* Loaded movie and credits CSVs
* Merged datasets on `title`

### 2️⃣ Feature Selection

Selected relevant columns:

```
movie_id, title, overview, genres, keywords, cast, crew
```

### 3️⃣ Data Cleaning & Parsing

* Removed null values
* Extracted names from nested lists using `ast.literal_eval()`
* Extracted **top 3 cast members**
* Extracted **director** from crew

### 4️⃣ NLP & Feature Engineering

* Removed spaces in tokens (`Tom Cruise → TomCruise`)
* Combined metadata into a single `tags` column
* Converted text to numerical vectors using **CountVectorizer**

### 5️⃣ Similarity Computation

Computed similarity matrix using **Cosine Similarity**

### 6️⃣ Recommendation Logic

Returns top 5 similar movies based on similarity scores.

---

## 📦 Output Files

The following files are saved for deployment:

```
movie_list.pkl
similarity.pkl
```

---

## ▶️ Usage

### Run the recommender function

```python
recommend("The Dark Knight Rises")
```

### Example Output

```
The Dark Knight
Batman Begins
Batman
Man of Steel
Iron Man 2
```

---

## 🧪 Sample Code to Test

```python
movie = "Pirates of the Caribbean: At World's End"
recommend(movie)
```

---

## 📊 Improvement Ideas (Future Scope)

| Feature               | Description                                     |
| --------------------- | ----------------------------------------------- |
| Add TF-IDF vectorizer | Better text representation                      |
| Web app               | Build UI using Streamlit / Flask                |
| Hybrid system         | Combine content-based + collaborative filtering |
| Model deployment      | Host using Streamlit Cloud / Render             |

---

## 📁 Project Structure

```
│── tmdb_5000_movies.csv
│── tmdb_5000_credits.csv
│── movie_recommender.ipynb / .py
│── movie_list.pkl
│── similarity.pkl
└── README.md
```

---

## 🙌 Acknowledgements

Dataset courtesy:
**The Movie Database (TMDB)**
Kaggle Dataset Source

---

## ⭐ Author

**Annanyaa Sharma**
AI & Data Science



