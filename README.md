# FakeReviewGuard

# Détection Automatique de Fausses Critiques de Produits

## Description du projet
Ce projet implémente des techniques de Machine Learning pour détecter automatiquement les fausses critiques de produits. L'objectif est de distinguer les critiques frauduleuses (fake) des critiques authentiques (real) en analysant leur contenu textuel.

## Dataset
Le projet utilise le dataset "Fake-Reviews" de Kaggle qui contient des critiques de produits avec les colonnes suivantes:
- **category**: catégorie de produit
- **rating**: note du produit (1-5)
- **label**: classe de la critique (fake/real)
- **text**: contenu textuel de la critique

## Méthodologie

### 1. Prétraitement des données
- Chargement et nettoyage du dataset
- Traitement du texte: suppression de la ponctuation, conversion en minuscules, élimination des stopwords, lemmatisation
- Encodage des labels (fake = 0, real = 1)
- Analyse statistique initiale: longueur des critiques, distribution des classes, détection de doublons

### 2. Analyse exploratoire (EDA)
- Visualisation de la distribution des classes
- Analyse de la longueur des critiques par classe
- Création de nuages de mots (WordCloud) pour les critiques authentiques et frauduleuses
- Analyse des bigrammes fréquents par classe
- Matrices de corrélation

### 3. Vectorisation du texte
- Application de la méthode TF-IDF pour transformer le texte en vecteurs numériques
- Analyse des dimensions et du vocabulaire obtenu

### 4. Modélisation
- Implémentation de deux modèles de classification:
  - Régression logistique (baseline)
  - Réseau de neurones simple (MLP)

### 5. Évaluation des performances
- Métriques d'évaluation: accuracy, précision, rappel, F1-score, AUC
- Visualisation des courbes ROC
- Analyse des matrices de confusion
- Comparaison des performances des modèles

### 6. Interprétation des résultats
- Application de LIME pour expliquer les prédictions du modèle
- Analyse des mots clés influençant la classification

## Résultats principaux
- Les modèles parviennent à distinguer efficacement les critiques authentiques des fausses critiques
- Le modèle Logistic Regression obtient les meilleures performances avec un F1-score de 0.869293

## Perspectives
- Amélioration des performances avec d'autres algorithmes (SVM, BERT, etc.)
- Exploration de modèles plus complexes pour capturer la structure linguistique
- Adaptation du système pour gérer différentes langues ou catégories de produits

## Réflexions théoriques
Le projet aborde également plusieurs questions théoriques importantes:
1. L'importance du nettoyage des données textuelles avant vectorisation
2. La pertinence du F1-score par rapport à l'accuracy pour l'évaluation des modèles
3. La comparaison entre les approches TF-IDF et Word2Vec pour la représentation du texte
4. L'impact du déséquilibre des classes sur les performances des modèles
5. Les enjeux éthiques de la détection automatisée de contenus frauduleux

## Outils et bibliothèques utilisés
- Python 3.x
- Pandas, NumPy
- NLTK pour le traitement du texte
- Scikit-learn pour la modélisation
- Matplotlib et Seaborn pour la visualisation
- LIME pour l'interprétation des modèles

## Structure du projet
- `Détection automatique de fausses critiques de produits.ipynb`: Notebook Jupyter contenant l'ensemble du code et des analyses
- `fake reviews dataset.csv`: Dataset utilisé (non inclus dans le dépôt)
- `README.md`: Ce fichier de documentation

## Auteur
Rayen Ayadi Boukhchina
Classe: IIA4  
Année Universitaire: 2024/2025  
Cours: Machine Learning  
Enseignant: Wassim Arfa

