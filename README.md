# Netflix Recommendation System

This project implements a **content-based recommendation engine** for Netflix titles using **Apache Spark (PySpark)**.  
The system applies text preprocessing (tokenization, stopword removal) and computes **Jaccard similarity** between shows to suggest similar titles.  
The solution is designed to run on **Databricks** for scalability on large datasets.

---

## Project Overview
- **Goal:** Recommend Netflix titles similar to a given show based on content.  
- **Dataset:** [Netflix Shows Dataset (Kaggle)](https://www.kaggle.com/datasets/shivamb/netflix-shows)  
- **Techniques Used:**
  - Text preprocessing: tokenization, stopword removal
  - Custom User-Defined Function (UDF) for Jaccard similarity
  - PySpark DataFrame operations and Spark SQL queries
- **Example:** Given the title *Kota Factory*, the system suggests the top 10 most similar titles.

---

## Tech Stack
- **Platform:** Databricks, Google Colab  
- **Frameworks/Libraries:** PySpark, Spark SQL, UDFs  
- **Language:** Python  

---

## How It Works
1. Load Netflix dataset into Spark DataFrame.  
2. Combine relevant fields (title, director, cast, genre, description).  
3. Apply preprocessing:
   - Convert to lowercase
   - Tokenize text
   - Remove stopwords  
4. Compute pairwise similarity using Jaccard coefficient.  
5. Return top-N most similar shows for a given title.

---

## Sample Results
For the input title **"Kota Factory"**, the system outputs:  
- TVF Pitchers  
- Engineering Girls  
- Aspirants  
- Flames  
- BroCourt  

*(Top recommendations vary based on dataset preprocessing.)*

---

## Repository Structure
```
├── Netflix_Recommendation_System.ipynb      # Jupyter/Colab notebook
├── docs/
│   └── Netflix_Recommendation_System.pdf    # Exported notebook as PDF
└── README.md
```

---

## Reports
- [Notebook Export (PDF)](docs/Netflix_Recommendation_System.pdf)

---

## Future Work
- Extend to **hybrid recommendation** (combine content-based + collaborative filtering).  
- Deploy as a **REST API** for real-time recommendations.  
- Add **evaluation metrics** (Precision@K, Recall@K).  

---

## Author
**Quhura Fathima**  
[LinkedIn](https://www.linkedin.com/in/quhurafathima/) | [GitHub](https://github.com/qfath001)
