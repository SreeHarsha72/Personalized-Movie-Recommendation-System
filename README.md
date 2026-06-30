# Personalized-Movie-Recommendation-System

## About This Project

I built this project to understand how recommendation systems work in real-world streaming platforms like Netflix, Amazon Prime Video etc.

Instead of implementing only one recommendation algorithm, I wanted to compare multiple recommendation strategies and understand:
- Why different recommendation techniques exist
- When each technique performs well
- How companies combine them into a hybrid recommendation engine
- How recommendation quality can be evaluated
- How recommendations can be explained to business stakeholders


## Project Objectives

The primary goals of this project are to:
- Explore streaming platform user behavior
- Analyze movie ratings and viewing patterns
- Build multiple recommendation models
- Compare recommendation approaches
- Predict user ratings
- Generate personalized movie recommendations
- Explain why recommendations are made
- Interpret the business value of recommendation systems



## Tech Stack

Python, Pandas, NumPy. Matplotlib, Scikit-learn, Jupyter Notebook, TF-IDF Vectorizer, Cosine Similarity



## Dataset

For this project I used a synthetic streaming platform dataset that mimics a real-world movie recommendation environment.

The dataset contains: Users, Movies, Ratings



## Project Workflow

### 1. Data Loading

I begin by loading the datasets and validating the overall structure before starting any analysis.

Tasks include:

- Loading CSV files
- Inspecting schemas
- Understanding relationships between datasets



### 2. Exploratory Data Analysis (EDA)

Before building recommendation models, I explore user behavior and movie characteristics.

Key analyses include:
- Number of users
- Number of movies
- Rating distribution
- Most watched genres
- Movie popularity
- Average movie ratings

This helps to understand user engagement before building recommendation algorithms.



## Recommendation Models

This project includes multiple recommendation approaches to illustrate how recommendation systems evolve from simple methods to more intelligent models.


### 1. Popularity-Based Recommendation

This is the simplest recommendation strategy.

It recommends movies that:
- Receive many ratings
- Have high average ratings
- Are generally popular among all users

This serves as a strong baseline recommendation model.

While this method is easy to implement and performs well, however the recommendations are not personalized.



### 2. Content-Based Recommendation

This recommender suggests movies that are similar to movies a user already likes.

Movie similarity is calculated using:
- TF-IDF Vectorization
- Cosine Similarity

The recommendation engine compares movie features and recommends movies with similar characteristics.

This approach is useful because it focuses on a user's preferences without needing data from other users. However, it has limited variety in its recommendations.



### 3. User-Based Collaborative Filtering

This approach identifies users with similar rating behavior.

The workflow:
1. Build a User-Movie Matrix
2. Compute User Similarity
3. Find similar users
4. Recommend movies liked by similar users

This approach improves recommendation quality by learning from users with similar preferences. However, it works best when there is enough user rating data and can struggle with new users or limited interactions.



### 4. Item-Based Collaborative Filtering

Instead of comparing users, this approach compares movies. If users frequently rate two movies similarly, they are considered related. Recommendations are generated based on movies the user already enjoyed.

This approach is a reliable recommendation approach, but it depends on having enough user interactions to identify similar movies.


### 5. Hybrid Recommendation System

Finally, I combine multiple recommendation signals into a hybrid model.

The hybrid recommender integrates:
- Popularity Score
- Content Similarity
- Collaborative Filtering

This approach balances personalization with overall popularity, making recommendations more robust.


## Rating Prediction

Beyond recommending movies, I also predict how a user might rate an unseen movie.

The workflow includes:
- Train/Test Split
- User similarity calculation
- Rating prediction
- Evaluation

This demonstrates how recommendation systems estimate future user preferences.



## Model Evaluation

The recommendation system is evaluated using predicted ratings.

Evaluation focuses on:
- Prediction accuracy
- User similarity
- Recommendation relevance
