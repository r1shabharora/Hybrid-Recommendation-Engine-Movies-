# Hybrid-Recommendation-Engine-Movies-

Movie Recommendation System

This project implements a complete end-to-end Movie Recommender System using the TMDB dataset. It covers data exploration, preprocessing, feature engineering, and development of multiple recommendation models—Content-Based, Collaborative Filtering, and Hybrid techniques.

📂 Project Structure

Data Loading & Cleaning
Loads TMDB metadata, credits, keywords, and ratings datasets. Handles missing values, merges metadata, and filters movies present across datasets.

Exploratory Data Analysis (EDA)
Includes distribution of ratings, count of ratings per movie, metadata review (genres, cast, keywords, overview, tagline, etc.).

Preprocessing

Converts IDs

Cleans text fields

Creates a combined "description" field using overview + tagline

Content-Based Recommender

TF-IDF Vectorizer on descriptions → cosine similarity

CountVectorizer on cast/crew/keywords/genres → cosine similarity

Functions to get top similar movies via content similarity.

Collaborative Filtering (Surprise Library)

User–movie matrix

SVD model to predict ratings

Generates personalized recommendations using predicted scores.

Hybrid Recommender
Combines:

User preference (via SVD predictions)

Movie similarity (via cosine similarity)
The hybrid model finds movies similar to a given title and ranks them by predicted user rating.

🛠 Tech Stack

Python

Pandas, NumPy

Scikit-learn

Surprise (SVD)

Matplotlib / Seaborn

TMDB Movie Metadata

🚀 Features

Movie similarity search using storyline, cast, and keywords

Recommendations based on user behavior

Hybrid model merging both worlds

Fully interpretable and modular design

Suitable for deploying as an API or integrating into ML pipelines

🔮 Future Enhancements

Deep-learning–based embeddings (BERT, SentenceTransformers)

Multi-criteria recommendation (genre diversity, popularity, recency)

Real-time recommendation API

UI dashboard (Streamlit / React)
