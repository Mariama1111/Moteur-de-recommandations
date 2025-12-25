# 🎬 Moteur de recommandations
Application de recommandation de films + analyse cinéma pour un cinéma local  
---

## 📌 Présentation du projet  
Ce projet a été réalisé dans le cadre d’une mission de Data Analyst pour un cinéma indépendant souhaitant :

1. Explorer et analyser une base volumineuse (+7M films) provenant d’IMDb  
2. Construire des **indicateurs et KPI** pour mieux orienter la programmation  
3. Mettre en place un **système de recommandation de films** performant  
4. Proposer une **application** testable par les internautes  

Le projet combine **Data Analysis, Machine Learning et Data Engineering léger** pour produire une solution complète et industrialisable.

---

## 🚀 Fonctionnalités principales  

### 🔍 Analyse & KPI
- Étude IMDb : évolution des films, genres, durées, acteurs récurrents  
- Visualisation des tendances (Matplotlib / Seaborn)  
- Extraction des films les mieux notés & leurs caractéristiques  

### 🤖 Machine Learning  
Le système de recommandation repose sur 2 approches :  

#### ✔️ **Modèle de similarité (Cosine Similarity)**  
- Basé sur TF-IDF appliqué aux descriptions, genres et tags  
- Similaire aux systèmes utilisés par Netflix / Amazon  

#### ✔️ **Clustering (K-Means)**  
- Segmentation des films par thématiques  
- Recommandations plus cohérentes & personnalisables  

---

## 🧱 Architecture du repository  
```bash
cinema-recommender/
│── README.md
│── requirements.txt
│
│── data/
│ ├── raw/
│ └── processed/ → movies_clean.csv
│ 
│── notebooks/
│ ├── 01_eda.ipynb
│ ├── 02_cleaning.ipynb
│ ├── 03_feature_engineering.ipynb
│ ├── 04_modeling.ipynb
│ └── 05_streamlit_prep.ipynb
│
│── src/
│ ├── data_prep.py
│ ├── features.py
│ ├── modeling.py
│ └── recommend.py
│
│── models/
│ ├── tfidf_vectorizer.pkl
│ ├── cosine_matrix.pkl
│ ├── kmeans_model.pkl
│
│── app/
│ ├── streamlit_app.py
│ ├── style.css
│ └── images/
│
└── tests/
```

---

## 📊 Méthodologie complète  

### 1️⃣ Étude de marché  
- Analyse des données CNC + INSEE  
- Tendances cinéma en Creuse  
- Identification des genres & formats les plus consommés  

### 2️⃣ Exploration & Nettoyage  
- Lecture des fichiers IMDb au format **TSV** (datasets massifs)  
- Nettoyage : gestion des valeurs manquantes, filtres pertinents  
- Export d’un dataset propre : `movies_clean.csv`

### 3️⃣ Feature Engineering  
- TF-IDF sur la description, genres et mots-clés  
- Normalisation des durées & notes  
- Construction d’un dataset optimisé pour le ML  

### 4️⃣ Machine Learning  
- Similarité Cosine pour recommander des films proches  
- Clustering KMeans pour regrouper les films par thèmes  
- Analyse qualitative des clusters  

### 5️⃣ Déploiement Streamlit  
- Interface simple et efficace  
- Zone de saisie du titre du film  
- Affichage d’affiches via TMDB  
- Recommandations instantanées  

---

## 🖥️ **Application Streamlit**  
👉 **Lien de l'application :** *(à ajouter)*

L’application permet de :  
- consulter les KPI cinéma  
- entrer un film et recevoir plusieurs recommandations  
- visualiser les posters des films recommandés  

---

## 📚 Technologies utilisées  

### 🔧 Data Analysis  
- Python (Pandas, NumPy)  
- Matplotlib, Seaborn  

### 🤖 Machine Learning  
- Scikit-learn  
- TF-IDF  
- K-Means  
- Cosine Similarity  

### 🌐 Application  
- Streamlit  
- TMDB API (affiches de films)  

---

## ▶️ Installation et exécution  

### 1️⃣ Cloner le projet  

git clone https://github.com/Mariama1111/cinema-reco.git
cd cinema-recommender

### 2️⃣ Installer les dépendances

pip install -r requirements.txt

### 3️⃣ Lancer l’application

streamlit run app/streamlit_app.py

📌 Auteure
Mariama Pasco — Data Analyst en spécialisation Data Engineering
Passionnée par l’optimisation, l’automatisation et la création de pipelines robustes.

---

📬 Contact
📧 mariadialp@hotmail.com
