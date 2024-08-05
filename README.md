#LGBMRanker
This repository contains the code for an anime recommendation system using LightGBM, a powerful gradient boosting framework. The model is designed to predict and recommend anime titles to users based on their past interactions and the characteristics of the anime.

Overview The goal of this project is to develop a machine learning model that can generate personalized anime recommendations for users. The system leverages LightGBM for ranking and uses a dataset comprising user interactions, anime metadata, and user information.

Dataset The dataset consists of three main components:

Anime Info (anime_info.csv): Contains metadata about the anime, such as genres, year aired, and ratings.
Relevance Scores (relavence_scores.csv): Contains the relevance scores of various anime for different users, indicating how much a user liked an anime.
User Info (user_info.csv): Contains information about the users, such as the number of reviews they have written and their average scores.
Main Steps

Data Preparation:
Load and preprocess the anime, relevance scores, and user information datasets. Create binary flags for popular anime genres. Merge datasets to create a unified training dataset.

2)Model Training:

Limit the number of entries per user to manage the dataset size. Define features and target variables. Train a LightGBM ranking model using user interactions and anime metadata.

3)Recommendation Generation:

Generate a list of anime candidates for each user. Predict relevance scores for these candidates using the trained model. Sort and select the top-N recommendations for each user.

4)Saving and Loading the Model:

Save the trained model to a file for later use. Load the model and generate predictions for new users based on their past interactions and available anime metadata.

Usage

1)Install Dependencies:

Ensure you have the necessary libraries installed (e.g., pandas, scikit-learn, lightgbm).

2)Prepare the Data:

Unzip the anime-recommendation-ltr-dataset.zip file and place the CSV files in the appropriate directory.

3)Train the Model:

Run the training script to preprocess the data and train the LightGBM model.
