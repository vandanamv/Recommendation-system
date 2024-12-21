#Movie Recommender System
This project is a Movie Recommender System built using Streamlit for the user interface. It recommends movies similar to a selected movie based on their similarity scores, and it displays their posters fetched from The Movie Database (TMDb) API.

#Features
Interactive User Interface: Users can select a movie from a dropdown list and click a button to get movie recommendations.
Movie Recommendations: Displays 5 recommended movies based on similarity with the selected movie.
Movie Posters: Fetches and displays posters of the recommended movies using TMDb API.
##How It Works
#Data Preprocessing:

A preprocessed movie dataset (movies_dict.pkl) is loaded into a Pandas DataFrame. This file contains metadata for movies, such as titles and TMDb IDs.
A precomputed similarity matrix (similarity.pkl) is used to determine the similarity between movies.
Recommendation Logic:

When a user selects a movie, its index is retrieved from the dataset.
Using the similarity matrix, the top 5 most similar movies (excluding the selected movie itself) are identified.
For each recommended movie, its poster is fetched from the TMDb API.
Displaying Results:

The recommended movies' names and posters are displayed in a grid layout with 5 columns using Streamlit.
Installation
Clone the Repository:

bash
Copy code
git clone <repository_url>
cd <repository_folder>
Install Required Libraries: Use the following command to install the dependencies:

bash
Copy code
pip install streamlit pandas requests
Add Required Files: Ensure the following files are in the project directory:

movies_dict.pkl: Contains movie metadata.
similarity.pkl: Contains the similarity matrix.
TMDb API Key:

Replace a5e9e02f30c08c645f99e2714a6c3304 with your own TMDb API key in the fetch_poster function.
Usage
Run the Application:

bash
Copy code
streamlit run <script_name>.py
Select a Movie:

Use the dropdown menu to select a movie from the dataset.
Get Recommendations:

Click the "Recommend" button to get movie recommendations and view their posters.
Code Overview
Key Functions
fetch_poster(movie_id):

Fetches the poster URL for a movie using its TMDb ID.
Constructs the URL from the API response.
recommend(movie):

Retrieves the top 5 most similar movies for the selected movie.
Fetches their poster URLs using the fetch_poster function.# Recommendation-system
