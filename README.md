# **Movie Recommender System**

This project is a **Movie Recommender System** built using **Streamlit** for the user interface. It recommends movies similar to a selected movie based on their similarity scores, and it displays their posters fetched from **The Movie Database (TMDb) API**.

---

## **Features**

- **Interactive User Interface**: Users can select a movie from a dropdown list and click a button to get movie recommendations.  
- **Movie Recommendations**: Displays 5 recommended movies based on similarity with the selected movie.  
- **Movie Posters**: Fetches and displays posters of the recommended movies using **TMDb API**.

---

## **How It Works**

### **1. Data Preprocessing**
- A preprocessed movie dataset (`movies_dict.pkl`) is loaded into a Pandas DataFrame. This file contains metadata for movies, such as titles and TMDb IDs.  
- A precomputed similarity matrix (`similarity.pkl`) is used to determine the similarity between movies.

### **2. Recommendation Logic**
- When a user selects a movie, its index is retrieved from the dataset.  
- Using the similarity matrix, the top 5 most similar movies (excluding the selected movie itself) are identified.  
- For each recommended movie, its poster is fetched from the **TMDb API**.

### **3. Displaying Results**
- The recommended movies' names and posters are displayed in a grid layout with 5 columns using **Streamlit**.

---

## **Installation**

### **1. Clone the Repository**
```bash
git clone <repository_url>
cd <repository_folder>
