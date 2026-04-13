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


---

## ▶️ Usage

### Load and Run the Recommendation System

```python
# Get recommendations for a drama
recommend("Goblin")
