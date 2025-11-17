#  Hybrid Movie Recommendation System (TF-IDF + KNN + SVD)

This project is a **Hybrid Movie Recommendation Engine** that combines both  
**content-based filtering** (using TF-IDF + cosine similarity) and  
**collaborative filtering** (KNN, KNNWithMeans, and SVD from Surprise).  

The goal was to build a recommender system that feels much closer to real-world apps like **Netflix**,  
while keeping the project easy to understand, experiment with, and extend.

Everything runs smoothly in **Google Colab**, includes an **interactive movie picker UI**,  
and lets you **download your recommendations as a CSV file**.

---

##  What This Project Does

### 🔹 Content-Based Filtering
Looks at movie titles and genres, converts them to TF-IDF vectors,  
and finds similar movies based on cosine similarity.

### 🔹 Collaborative Filtering
Uses actual user ratings to predict how much a typical user might like a movie.  
Several algorithms are tested and the one with the best RMSE is automatically selected:
- KNNBasic  
- KNNWithMeans  
- SVD  

### 🔹 Hybrid Model (Best of Both Worlds)
The final score is a mix of:
- **70%** content similarity  
- **30%** collaborative score  

This gives recommendations that are more realistic and personalized.

### 🔹 Interactive UI (Colab Widgets)
You get:
- A dropdown of all movie titles  
- A “Recommend Movies” button  
- A “Download CSV” button   

---

##  Dataset Used

The project uses the **MovieLens 100k dataset**, which includes:  
- 9,742 movies  
- 100,836 ratings  
- 700+ users  

It’s one of the most widely used datasets for recommender systems.

---

##  Tools and Libraries

This project uses:

- Python  
- NumPy 1.26 (important due to Surprise library)  
- Pandas  
- Scikit-Learn  
- Scikit-Surprise  
- Matplotlib / Seaborn  
- ipywidgets (for the UI)  
- Google Colab  

Everything is lightweight and runs in a single notebook.

---

##  Methodology (CRISP-ML(Q))

I followed the CRISP-ML(Q) framework to keep the project structured:

### 1. **Business Understanding**
Build a simple, understandable movie recommendation system.

### 2. **Data Understanding**
Explored movie titles, genres, rating distribution, duplicates, missing data, etc.

### 3. **Data Preparation**
- Clean titles and genres  
- Build “tags” feature  
- Validate ratings  
- Format types  

### 4. **Modeling**
- TF-IDF content model  
- Collaborative models (multiple)  
- Hybrid scoring method  

### 5. **Evaluation**
Compared RMSE + MAE for CF models.  
Hybrid model evaluated qualitatively.

### 6. **Deployment**
Interactive UI + CSV download.

### 7. **Quality Assurance**
Code tested with multiple movie titles for stability.

---

##  How to Use the Notebook

1. Upload `movies.csv` and `ratings.csv` to Colab.  
2. Run all cells until the UI appears.  
3. Pick any movie from the dropdown.  
4. Click **Recommend Movies**.  
5. (Optional) Download the results as a CSV.

---

##  Example Output

###  Movie picker with dropdown list
<img width="1054" height="729" alt="image" src="https://github.com/user-attachments/assets/a6637f19-4069-4ca2-8188-9e34c10eb081" />

<img width="1237" height="613" alt="image" src="https://github.com/user-attachments/assets/b01e795a-9024-4131-9d69-cc1a74f10496" />




