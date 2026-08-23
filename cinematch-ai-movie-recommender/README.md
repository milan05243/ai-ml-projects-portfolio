# 🎬 CineMatch — AI Movie Recommendation System

CineMatch is a full-stack **content-based movie recommendation system** that helps users discover movies similar to a selected title.

The recommendation engine uses **TF-IDF vectorization and Cosine Similarity** to analyze movie metadata such as plot overviews, genres, and keywords. The application also integrates the **TMDB API** to dynamically retrieve movie posters and provides a responsive web interface for searching and exploring recommendations.

## 🌐 Project Links

* **Live Demo:** https://cinematch-ai-tccm.onrender.com/
* **GitHub:** https://github.com/milan05243/ai-ml-projects-portfolio

> **Deployment Note:** The application is hosted on Render's free tier. After a period of inactivity, the first request may take a short time while the service restarts.

---

## ✨ Features

### 🤖 Content-Based Recommendation Engine

Recommends the top 5 movies most similar to the selected movie using:

* TF-IDF Vectorization
* Cosine Similarity
* Movie overview, genres, and keywords

### 🔎 Movie Search & Autocomplete

Provides real-time, case-insensitive autocomplete suggestions while users type a movie title.

### 🎞️ Dynamic Movie Posters

Movie posters are retrieved dynamically using the TMDB API through a backend proxy endpoint.

### 🏠 Featured Movie Feed

The home page provides curated sections for:

* Popular Movies
* Trending Movies
* Recently Released Movies

### 🎨 Responsive User Interface

A modern dark-themed interface featuring:

* Glassmorphism-inspired design
* Responsive layouts
* Hover animations
* Smooth transitions
* Interactive movie cards

### 🔌 REST API

The Flask backend provides structured API endpoints for:

* Health monitoring
* Movie autocomplete
* Featured movies
* Movie recommendations
* Movie poster retrieval

### 🚀 Cloud Deployment

The application is deployed as a web application using **Flask, Gunicorn, and Render**.

---

## 🧠 How CineMatch Works

The recommendation process follows these steps:

```text
User searches for a movie
          ↓
Movie title is matched with the dataset
          ↓
Movie metadata is processed
          ↓
TF-IDF converts textual information into numerical vectors
          ↓
Cosine Similarity compares movie vectors
          ↓
Top 5 most similar movies are selected
          ↓
Movie information is returned to the frontend
          ↓
TMDB API provides movie posters
          ↓
Recommendations are displayed to the user
```

---

## 🛠️ Tech Stack

### Machine Learning

* **Python 3.8+**
* **Pandas** — Data processing and manipulation
* **NumPy** — Numerical operations
* **Scikit-learn** — TF-IDF vectorization and cosine similarity

### Backend

* **Flask** — Web framework and REST API
* **Python-dotenv** — Environment variable management
* **Requests** — HTTP requests
* **Gunicorn** — Production WSGI server

### Frontend

* **HTML5**
* **CSS3**
* **Bootstrap 5**
* **JavaScript**
* **Font Awesome**

### External API & Deployment

* **TMDB API** — Movie poster retrieval
* **Render** — Application deployment

---

## 📊 Dataset

The recommendation engine is trained using the **TMDB 5000 Movies Dataset**.

The dataset provides movie information used to construct the recommendation features, including:

* Movie titles
* Plot overviews
* Genres
* Keywords

These features are combined and processed using TF-IDF before calculating movie-to-movie similarity.

---

## 📁 Project Structure

```text
cinematch-ai-movie-recommender/
│
├── app.py
├── recommender.py
├── train_model.py
├── requirements.txt
├── .env.example
├── .gitignore
│
├── movies.pkl
├── similarity.pkl
├── tfidf_vectorizer.pkl
│
├── static/
│   ├── css/
│   └── js/
│
├── templates/
│   └── index.html
│
└── README.md
```

---

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/milan05243/ai-ml-projects-portfolio.git
```

Navigate to the CineMatch project directory:

```bash
cd ai-ml-projects-portfolio/cinematch-ai-movie-recommender
```

### 2. Create a Virtual Environment

#### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

#### macOS / Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables

Create a `.env` file based on `.env.example`.

Example:

```env
FLASK_APP=app.py
FLASK_ENV=development
SECRET_KEY=your_development_secret_key
PORT=5000
TMDB_API_KEY=your_tmdb_api_key_here
```

The TMDB API key is used server-side for retrieving movie posters.

**Never commit your actual `.env` file or API key to GitHub.**

### 5. Train the Recommendation Model

Run:

```bash
python train_model.py
```

The training process preprocesses the movie dataset, generates TF-IDF vectors, calculates cosine similarity, and creates the required model files.

Expected generated files include:

```text
movies.pkl
similarity.pkl
tfidf_vectorizer.pkl
```

### 6. Run the Application

Start the Flask server:

```bash
python app.py
```

Open:

```text
http://127.0.0.1:5000
```

---

# 🔌 API Documentation

CineMatch provides REST API endpoints for communication between the frontend and Flask backend.

## 1. Health Check

### `GET /health`

Returns the application and model loading status.

Example response:

```json
{
  "status": "healthy",
  "models_loaded": true,
  "config": {
    "environment": "development",
    "top_n": 5,
    "tmdb_poster_api_enabled": true
  }
}
```

---

## 2. Movie Autocomplete

### `GET /autocomplete?q=av`

Returns movie titles matching the entered search query.

Example:

```json
[
  "Avatar",
  "Avengers: Age of Ultron",
  "The Avengers",
  "Avengers: Infinity War"
]
```

---

## 3. Featured Movies

### `GET /movies/featured`

Returns movie collections used by the application's home page.

The response can include:

* Popular movies
* Trending movies
* Recently released movies

---

## 4. Movie Recommendations

### `POST /recommend`

Generates recommendations based on a selected movie.

Request:

```json
{
  "movie_name": "Interstellar"
}
```

The API returns the searched movie along with its top recommended movies.

Example:

```json
{
  "searched_movie": {
    "id": 157336,
    "title": "Interstellar",
    "genres": [
      "Adventure",
      "Drama",
      "Science Fiction"
    ],
    "release_year": "2014",
    "rating": 8.1
  },
  "recommendations": [
    {
      "id": 264660,
      "title": "Ex Machina",
      "genres": [
        "Drama",
        "Science Fiction"
      ],
      "release_year": "2015",
      "rating": 7.6
    }
  ]
}
```

---

## 5. Movie Poster

### `GET /poster/<movie_id>`

Retrieves poster information through the TMDB API.

Example:

```text
GET /poster/157336
```

Response:

```json
{
  "poster_url": "https://image.tmdb.org/t/p/w500/gEU2QvEw1Fg7lsbq5v44R4m2Pjh.jpg"
}
```

The API key remains on the backend rather than being exposed to the client.

---

# 🚀 Deployment

CineMatch is deployed as a live web application using **Render**.

### Live Application

https://cinematch-ai-tccm.onrender.com/

The deployed application provides the complete CineMatch experience, including:

* Movie search
* Autocomplete
* Recommendations
* Movie posters
* Featured movie sections
* REST API endpoints

---

# 📸 Screenshots

## Home Page

![CineMatch Home Page](https://github.com/user-attachments/assets/698f1e7b-bbba-41cd-ab70-3b27f6cc5c0e)

## Movie Recommendations

![CineMatch Movie Recommendations](https://github.com/user-attachments/assets/354d8a82-6d40-4834-8d21-4ddee0736705)

## Featured Movies

![CineMatch Featured Movies](https://github.com/user-attachments/assets/c5354bf5-c7d9-42db-aab7-9e4da376b9e6)

---

# 🔮 Future Improvements

Potential improvements for future versions include:

1. **User Authentication**
   Allow users to create accounts and maintain personalized profiles.

2. **Personalized Recommendations**
   Incorporate user preferences and watch history into recommendations.

3. **Collaborative Filtering**
   Combine content-based recommendations with user-rating data.

4. **Hybrid Recommendation Engine**
   Combine content-based and collaborative filtering approaches.

5. **Watchlists & Ratings**
   Allow users to save movies, rate them, and maintain personal watchlists.

6. **Personalized Dashboard**
   Provide users with recommendations based on their viewing preferences.

7. **Database Integration**
   Replace file-based pickle storage with a scalable database such as PostgreSQL or MongoDB.

---

# 📚 Key Learning Outcomes

This project provided practical experience in:

* Building a content-based recommendation system
* TF-IDF feature extraction
* Cosine similarity
* Machine learning data preprocessing
* Flask REST API development
* Frontend and backend integration
* Third-party API integration
* Environment variable management
* Git and GitHub
* Cloud deployment
* Debugging production applications

---

# 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## 👨‍💻 Author

**Milan Choudhary**

Computer Science & Engineering — Artificial Intelligence


---

⭐ If you find this project interesting, feel free to explore the repository and try the live application.


### Project Links

- Live Demo: https://cinematch-ai-tccm.onrender.com/
- GitHub Repository: https://github.com/milan05243/internsMilan_INBT019545_iNeuBytes/tree/main/Major%20Project

