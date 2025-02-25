# Movie Recommendation System using K-Nearest Neighbors (KNN)

## 🎬 Overview
This project builds a **movie recommendation system** using collaborative filtering based on user ratings. It utilizes the **k-Nearest Neighbors (KNN)** algorithm to find similar movies based on rating patterns. The system is implemented using Python with libraries such as **Pandas, NumPy, Matplotlib, SciPy, and Scikit-learn**.

---

## 📂 Dataset
The project uses two datasets:
- **movies.csv** 🎥 - Contains movie details (movieId, title, genres).
- **ratings.csv** ⭐ - Contains user ratings for movies (userId, movieId, rating, timestamp).

---

## 🚀 Implementation Steps

### 1️⃣ Data Loading
📌 The datasets are loaded using **Pandas**.
📌 A preview of the data is displayed using `head()`.

### 2️⃣ Data Preprocessing
✅ A pivot table is created where:
   - Rows = **Movie IDs**
   - Columns = **User IDs**
   - Values = **Ratings given by users**
✅ Missing values (NaN) are replaced with `0`.

### 3️⃣ Filtering the Data
📌 Movies rated by **fewer than 10 users** are removed.
📌 Users who rated **fewer than 50 movies** are removed.
📌 This ensures that only meaningful and well-rated movies/users are considered.

### 4️⃣ Data Sparsity Calculation
📌 A small sample matrix is created to illustrate sparsity.
📌 **Sparsity** is computed as the ratio of zero values to total elements in the dataset.
📌 The dataset is converted into a **Compressed Sparse Row (CSR) matrix** for efficient computation.

### 5️⃣ KNN Model Training
📌 A **K-Nearest Neighbors (KNN)** model is trained using:
   - **Cosine similarity metric** 📊
   - **Brute-force algorithm** 🏎️
📌 The model is fit using the CSR matrix representation of the dataset.

### 6️⃣ Movie Recommendation Function
The function **`get_movie_recommendation(movie_name)`** performs the following:
1. 🎯 Searches for the given movie in the dataset.
2. 🔍 Retrieves its **movieId** and index.
3. 🔗 Finds the **10 most similar movies** using KNN.
4. 📋 Returns a **DataFrame** with recommended movies and their similarity distances.
5. ❌ If the movie is not found, an appropriate message is displayed.

### 7️⃣ Testing the Recommendation System
- 🔥 The function is tested by recommending movies similar to:
   - **Iron Man** 🦾
   - **Memento** 🧠

---

## 📦 Dependencies
Ensure you have the following Python libraries installed:
```sh
pip install pandas numpy matplotlib scipy scikit-learn
```

---

## 💡 Usage
1. 📂 Place `movies.csv` and `ratings.csv` in the working directory.
2. ▶️ Run the script to train the model.
3. 🎥 Call `get_movie_recommendation('<movie_name>')` to get recommendations.

---

## 🔥 Potential Improvements
✅ Use a more **advanced recommendation approach** (e.g., deep learning-based recommendation systems).
✅ Improve **data preprocessing and filtering** to handle sparse data more effectively.
✅ Implement a **web-based interface** for users to get recommendations interactively.

---

## 🎯 Conclusion
This project demonstrates a **simple but effective** way to build a **movie recommendation system** using collaborative filtering and KNN. It provides users with similar movie recommendations based on their rating patterns.

🚀 **Happy Coding & Movie Watching!** 🍿🎬
