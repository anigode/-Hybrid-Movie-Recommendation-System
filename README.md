### Hybrid Movie Recommendation System
This project implements a hybrid movie recommendation system, combining collaborative filtering and content-based filtering. It leverages user ratings and movie metadata (tags) to generate personalized recommendations. The dataset includes information about movies, ratings, and tags, enabling the recommendation system to suggest relevant movies based on user preferences and the movie's features.
## Table of Contents
- Introduction
- Installation
- Usage
- Data
- Models
- Evaluation
- Libraries

## Introduction
The goal of this project is to recommend movies to users by combining collaborative filtering and content-based filtering techniques. The system uses matrix factorization to predict user ratings and cosine similarity to compare movies based on their tags. The hybrid model integrates both approaches to provide more accurate and diverse recommendations.
## Installation
- Clone the repository.
- Install the required libraries
- Ensure you have Python (preferably version 3.6 or above) installed.
## Usage
- Place the datasets (genome-scores.csv, genome-tags.csv, links.csv, movies.csv, ratings.csv, tags.csv) in the project directory.
- Run the script hybrid_recommendation.py to execute the analysis and generate movie recommendations.
- You can modify the number of recommendations by changing the top_n parameter.
## Data
The project uses the MovieLens dataset, which contains user ratings, movie metadata, and tag relevance scores. Key data files include:
- ratings.csv: User ratings of movies
- movies.csv: Movie information (e.g., title, genres)
- genome-scores.csv: Tag relevance scores for each movie
- genome-tags.csv: Tags associated with movies
The data preprocessing steps include:
- Creating user-item and movie-tag matrices
- Normalizing tag relevance scores
- Applying Singular Value Decomposition (SVD) for matrix factorization
## Models
This project implements a hybrid recommendation system, combining:
- Collaborative Filtering: Predicts user ratings using matrix factorization with SVD.
- Content-Based Filtering: Computes cosine similarity between movies based on their tags.
The hybrid model blends the results from both approaches using a weighted combination.
## Evaluation
The performance of the recommendation system is evaluated based on the quality of the top 10 movie recommendations for a sample user. Key metrics include:
- Predicted Ratings: Accuracy of the predicted ratings for unseen movies.
- Cosine Similarity: Measures the similarity between movies based on their tags.
## Libraries
The project depends on the following Python libraries:
- pandas
- numpy
- scikit-learn
