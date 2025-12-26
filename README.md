

Movie Recommendation System (Collaborative Filtering)

This project implements a **Movie Recommendation System** using **Collaborative Filtering** with **Matrix Factorization (SVD)** on the **MovieLens 100K dataset**.

The system learns user preferences from historical ratings and generates **personalized movie recommendations** for each user.

---

Project Overview

* **Type**: Recommendation System (Collaborative Filtering)
* **Algorithm**: Singular Value Decomposition (SVD)
* **Framework**: `scikit-surprise`
* **Dataset**: MovieLens 100K
* **Environment**: Google Colab / Python

The project focuses on:

* clean data handling
* reproducible experiments
* quantitative evaluation (RMSE)
* human-readable recommendation output

---

Dataset

**MovieLens 100K**

* 100,000 ratings
* 943 users
* 1,682 movies
* Rating scale: **1–5**

Files used:

* `u.data` → user–movie ratings
* `u.item` → movie titles

Dataset source:
[https://grouplens.org/datasets/movielens/100k/](https://grouplens.org/datasets/movielens/100k/)

---

Tech Stack

* **Python**
* **pandas** – data manipulation
* **NumPy** – numerical computations
* **scikit-surprise** – recommendation algorithms
* **Google Colab** – execution environment

---

 Methodology

1. Load and preprocess ratings and movie metadata
2. Convert ratings to Surprise dataset format
3. Split data into training and test sets (80/20)
4. Train an **SVD collaborative filtering model**
5. Evaluate performance using **RMSE**
6. Generate **Top-N personalized recommendations**

---

Model Evaluation

The model is evaluated on unseen test data using **Root Mean Squared Error (RMSE)**.

Typical performance on MovieLens 100K:

* **RMSE ≈ 0.93 – 0.95**

This is a standard and expected result for collaborative filtering on this dataset.

---

Example Output

The system can generate recommendations such as:

| Movie Title                    | Predicted Rating |
| ------------------------------ | ---------------- |
| Star Wars (1977)               | 4.78             |
| Raiders of the Lost Ark (1981) | 4.65             |
| Shawshank Redemption (1994)    | 4.62             |

Each recommendation is:

* unseen by the user
* ranked by predicted preference

---

 How to Run

1. Open the notebook in **Google Colab**
2. Run **Cell 0** to install dependencies
3. Execute cells sequentially
4. Call the recommendation function:

```python
recommend_movies(user_id=1, n=5)
```

---

Project Structure

```
Movie-Recommender/
│
├── Movie_Recommender_CV_Clean.ipynb
├── README.md
└── data/
    └── ml-100k/
```

---

Possible Extensions

* Precision@K / Recall@K metrics
* Cold-start handling
* Content-based or hybrid recommender
* Model persistence (save/load)
* Web or API interface

---

Author

Developed as a **portfolio project** to demonstrate practical knowledge of:

* recommendation systems
* collaborative filtering
* machine learning workflows

---


