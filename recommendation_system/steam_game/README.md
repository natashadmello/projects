# **Steam Game Recommender System**

## **Project Overview**
This project implements a content-based recommendation system for Steam games. The system suggests games based on on text data like name, description, tags, genres, and categories.

## **Features**
- Content-based filtering using game metadata  
- Uses TF-IDF and cosine similarity for similarity calculation  
- Simple and easy-to-use interface for game recommendations  
- Data cleaning and preprocessing included

## **Dataset**
The dataset is from Kaggle's Steam Games Dataset, which includes:
- Game name  
- Release year  
- Tags, genres, and categories  
- Game description (*About the Game*)  
- Other metadata

## **Implementation Details**

### **Data Preprocessing**
- Fixed column misalignment  
- Removed missing and duplicate values  
- Applied text preprocessing (lemmatisation, lowercasing, and normalisation)  
- Combined multiple features (Name, Tags, Genres, Categories, and Description) for similarity calculation

### **Feature Extraction & Similarity**
- Used `TfidfVectorizer` to convert text data into numerical vectors  
- Computed pairwise cosine similarity between games based on these vectors

### **Recommendation Function**
The recommender function retrieves the top N most similar games based on cosine similarity scores, excluding the input game.