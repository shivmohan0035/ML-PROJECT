# 🎬 Movie Recommender System

A Content-Based Movie Recommendation System built using **Python, Pandas, Scikit-Learn, NLTK, and Streamlit**. The application recommends movies similar to a selected movie based on genres, keywords, cast members, directors, and movie overviews.

---

## 🚀 Features

* Recommend Top 5 similar movies
* Content-Based Filtering approach
* Cosine Similarity for recommendation generation
* Interactive Streamlit Web Interface
* Precomputed similarity matrix for faster recommendations
* Clean and modular implementation

---

## 🛠️ Tech Stack

### Languages & Libraries

* Python
* Pandas
* NumPy
* Scikit-Learn
* NLTK
* Streamlit
* Pickle

### Dataset

* TMDB 5000 Movies Dataset
* TMDB 5000 Credits Dataset

---

## 📂 Project Structure

```text
Movie-Recommender-System/
│
├── app.py                         # Streamlit Application
├── movie-recommender-system.ipynb # Data Processing & Model Building
├── movie_dict.pkl                 # Processed Movie Data
├── similarity.pkl                 # Cosine Similarity Matrix
├── tmdb_5000_movies.csv           # Movie Dataset
├── tmdb_5000_credits.csv          # Credits Dataset
│
├── .devcontainer/
└── .ipynb_checkpoints/
```

---

## ⚙️ How It Works

### 1. Data Collection

The movie and credits datasets are merged using the movie title.

### 2. Feature Engineering

The following features are extracted:

* Overview
* Genres
* Keywords
* Top 3 Cast Members
* Director

These features are combined into a single text representation called **tags**.

### 3. Text Processing

* Lowercasing
* Tokenization
* Stemming using NLTK PorterStemmer

### 4. Vectorization

CountVectorizer converts text into numerical feature vectors.

```python
cv = CountVectorizer(max_features=5000, stop_words='english')
```

### 5. Similarity Calculation

Cosine Similarity is used to calculate similarity between movie vectors.

```python
similarity = cosine_similarity(vectors)
```

### 6. Recommendation Generation

For a selected movie:

1. Find its index
2. Retrieve similarity scores
3. Sort scores in descending order
4. Return Top 5 similar movies

---

## 📊 Recommendation Example

Input:

```text
Avatar
```

Output:

```text
Aliens
Silent Running
Moonraker
Alien
Mission to Mars
```

---

## ▶️ Running the Project

### Clone Repository

```bash
git clone https://github.com/your-username/Movie-Recommender-System.git
cd Movie-Recommender-System
```

### Install Dependencies

```bash
pip install pandas numpy scikit-learn nltk streamlit
```

### Run Application

```bash
streamlit run app.py
```

The application will start on:

```text
http://localhost:8501
```

---

## 🧠 Machine Learning Concepts Used

* Content-Based Filtering
* Feature Engineering
* Natural Language Processing (NLP)
* Count Vectorization
* Cosine Similarity
* Data Preprocessing

---

## 🔮 Future Improvements

* Movie Poster Integration using TMDB API
* Movie Ratings and Release Dates
* Hybrid Recommendation System
* Collaborative Filtering
* User Authentication
* Watch History Tracking
* Cloud Deployment (AWS / Streamlit Cloud)
* Docker Containerization

---

## 📸 Application Screenshot

<img width="1048" height="652" alt="image" src="https://github.com/user-attachments/assets/f3d2f624-62ef-4f95-99f3-bf87136d38e4" />

<img width="1015" height="645" alt="image" src="https://github.com/user-attachments/assets/92485855-ddec-47b5-8eed-613a5f9e11a3" />



## 👨‍💻 Author

**Shivmohan Chaurasia**

* LinkedIn: https://www.linkedin.com/in/shivmohan0035/
* GitHub: https://github.com/shivmohan0035

---

## ⭐ Acknowledgements

* TMDB Dataset
* Scikit-Learn Documentation
* Streamlit Documentation
* NLTK Documentation
