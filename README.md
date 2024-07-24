# 📚 Book Recommendation System

This project aims to create a book recommendation system using both popularity-based and collaborative filtering approaches. The datasets used include information about books, users, and their ratings.

## 📁 Project Structure

The project is structured with three main datasets:
- `books.csv`: Contains detailed information about books, including their ISBN, title, author, year of publication, publisher, and image URLs.
- `users.csv`: Contains information about users, including user ID, location, and age.
- `ratings.csv`: Contains data about book ratings provided by users, including user IDs, ISBNs of the books, and the corresponding ratings.

## 🚀 Getting Started

### 📥 Prerequisites

To run this project, you will need to have Python installed along with the necessary libraries such as pandas, numpy, scikit-learn, and pickle.

### 📂 Data Loading

The project starts by loading the datasets into pandas DataFrames to facilitate data manipulation and analysis.

### 🔍 Data Overview

An initial overview of the data is performed to understand the structure and contents of the datasets. This includes displaying the first few rows of each dataset to get a sense of the data.

### 🔢 Data Cleaning

Data cleaning is a crucial step in preparing the data for analysis. This involves:
- Checking for and handling missing values in the datasets.
- Identifying and removing duplicate entries to ensure data integrity.

## 📈 Popularity-Based Recommender System

The popularity-based recommender system suggests books based on their overall popularity among users. The steps involved include:

1. **Merging Ratings with Book Titles**: Combining the ratings dataset with the books dataset to link ratings with book titles.
2. **Calculating Number of Ratings**: Counting the total number of ratings each book has received.
3. **Calculating Average Ratings**: Computing the average rating for each book.
4. **Creating Popularity DataFrame**: Merging the number of ratings and average ratings into a single DataFrame.
5. **Filtering and Sorting**: Filtering books that have received a significant number of ratings and sorting them by their average rating to identify the most popular books.

## 👫 Collaborative Filtering-Based Recommender System

The collaborative filtering-based recommender system suggests books based on user preferences and similar users' ratings. The steps involved include:

1. **Filtering Active Users and Popular Books**: Selecting users who have provided a significant number of ratings and books that have received a considerable number of ratings.
2. **Creating a Pivot Table**: Transforming the ratings data into a pivot table with books as rows and users as columns.
3. **Filling Missing Values**: Replacing missing values in the pivot table with zeros to prepare the data for similarity calculations.
4. **Calculating Similarity Scores**: Using cosine similarity to compute similarity scores between books.
5. **Making Recommendations**: For a given book, identifying and recommending books that have high similarity scores.

## 💾 Saving the Model

The final step involves saving the trained models and data structures using the pickle library. This allows for easy loading and use of the models for making recommendations without retraining.

---

This README provides a comprehensive overview of the project, explaining the data, processes, and methodologies used to build the book recommendation system.
