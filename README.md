# 🎬 Drama Finder & Recommendation System

## 📌 Overview
The Drama Finder & Recommendation System is a content-based machine learning project designed to help users discover Chinese and Korean dramas. It provides personalized recommendations using drama metadata such as genres, cast, tags, and descriptions, along with search and filtering capabilities for better content exploration.

---

## 🚀 Features
- 🔍 Search dramas by genre, country, and rating  
- 🤖 Content-based recommendation system  
- 🎯 Personalized suggestions using similarity metrics  
- 📊 Handles large datasets (~5000+ dramas)  
- ⚡ Efficient filtering and fast results  

---

## 🧠 How It Works
- Data is collected from a MyDramaList dataset  
- Features like genres, tags, cast, and descriptions are combined  
- TF-IDF vectorization converts text into numerical features  
- Cosine similarity measures similarity between dramas  
- Top similar dramas are recommended based on input  

---

## 📈 Evaluation Metrics

The recommendation system is evaluated using ranking-based metrics. Since the dataset does not contain explicit user relevance labels, **genre overlap is used as a proxy for relevance**.

| Metric | Description |
|---|---|
| **Precision@5** | Fraction of the top 5 recommendations that share at least one genre with the input drama |
| **Recall@5** | Fraction of genre-relevant dramas retrieved in the top 5 |
| **NDCG@5** | Measures ranking quality, giving higher importance to relevant dramas appearing near the top |
| **Average Similarity@5** | Average cosine similarity of the top 5 recommendations |
| **Intra-list Diversity@5** | Measures how different the recommended dramas are from one another |
| **Catalog Coverage** | Percentage of the drama catalog that appears in recommendations |

The notebook calculates these metrics automatically and displays the resulting scores in a metrics table.

> **Note:** Precision@5, Recall@5, and NDCG@5 are proxy metrics based on genre overlap rather than actual user feedback. For a production recommendation system, user ratings, clicks, watch history, or manually labeled relevance should be used as ground truth.

---

## 🛠️ Tech Stack
- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- KaggleHub  

---

## 📂 Dataset
Dataset used:  
**complete-5000-dramas-from-mydramalist-review-info** (Kaggle)

---

## ⚙️ Installation

```bash
pip install pandas numpy scikit-learn kagglehub
```

---

## ▶️ Usage

### Load and Run the Recommendation System

```python
# Get recommendations for a drama
recommend("Goblin")
```

### Evaluate the Recommendation System

Run the evaluation section in the notebook to calculate:

```python
metrics = evaluate_recommendations(5)
metrics_df
```
The output reports Precision@5, Recall@5, NDCG@5, Average Similarity@5, Intra-list Diversity@5, and Catalog Coverage.

