# 🎬 Movies Recommender System

This project is a **Content-Based Movies Recommender System** that suggests similar movies to users based on their preferences.  
It leverages movie metadata such as genres, cast, crew, and keywords to provide intelligent and personalized recommendations.

---

## 📊 Overview

The system analyzes textual and categorical data from the TMDB dataset to find movies that are most similar to a given movie using **cosine similarity**.  
It demonstrates the use of **Natural Language Processing (NLP)** and **feature vectorization** for content-based recommendation systems.

---

## 📁 Dataset

The project uses the **TMDB 5000 Movies Dataset**, containing rich metadata for thousands of movies.

**Files used:**
- `tmdb_5000_movies.csv`
- `tmdb_5000_credits.csv`

**Key columns:**
- `title`
- `overview`
- `genres`
- `keywords`
- `cast`
- `crew`

---

## 🧠 Methodology

1. **Data Loading and Exploration**
   - Loaded movie and credits datasets using `pandas`.
   - Explored data to understand relationships and missing values.

2. **Data Cleaning & Preprocessing**
   - Merged datasets on the movie title.
   - Selected relevant features: `movie_id`, `title`, `overview`, `genres`, `keywords`, `cast`, and `crew`.
   - Parsed JSON-like columns using `ast.literal_eval`.
   - Extracted meaningful data such as actor names, director, and genre names.
   - Combined key textual features into a single column called **“tags”**.
   - Cleaned and normalized text (lowercasing, removing spaces, etc.).

3. **Feature Engineering**
   - Used **CountVectorizer** to convert text data into numerical vectors.
   - Removed stopwords and limited the vocabulary to top 5000 frequent terms.

4. **Similarity Computation**
   - Computed **cosine similarity** between all movie vectors to measure closeness.

5. **Recommendation Function**
   - Implemented `recommend(movie_name)` that:
     - Finds the input movie in the dataset.
     - Retrieves the most similar movies based on cosine similarity scores.

---

## 💻 Technologies Used

- **Python**
- **pandas**, **numpy**
- **scikit-learn**
- **ast**
- **pickle**

---


---

## ⚙️ How to Run the Code

1. **Install dependencies**
   ```bash
   pip install pandas numpy scikit-learn
recommend('Avatar')
1. Guardians of the Galaxy
2. Star Trek Beyond
3. John Carter
4. The Fifth Element
5. Star Wars: The Force Awakens
