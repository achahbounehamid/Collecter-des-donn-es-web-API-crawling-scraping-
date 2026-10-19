# 🚀 Projet de Classification Automatique de Textes et Optimisation de Modèle

Ce projet s'inscrit dans le cadre d'un travail pratique complet en Machine Learning, allant de la collecte automatisée de données web jusqu'à l'optimisation, la régularisation et la quantification d'un réseau de neurones (TFLite) destiné à être déployé sur des systèmes embarqués.

---

## 📁 Structure du Dépôt

Le projet est divisé en trois parties principales, complétées par un rapport de synthèse et le jeu de données :

- **`1_collecte.ipynb`** : Constitution du corpus textuel via l'API MediaWiki et du scraping HTML (Wikipédia en anglais), nettoyage des doublons, et équilibrage des classes.
- **`2_premier_reseau.ipynb`** : Construction, entraînement et évaluation du premier réseau de neurones dense (baseline) comparé à une méthode de référence, avec analyse du bruit statistique.
- **`3_optimisation.ipynb`** : Exploration des hyperparamètres (taux d'apprentissage, taille du réseau), application de la régularisation (Dropout, Arrêt précoce) et quantification du modèle au format TensorFlow Lite (TFLite).
- **`corpus.csv`** : Le jeu de données final collecté, nettoyé et équilibré (239 textes répartis sur 4 catégories : astronomie, cuisine, football, peinture).
- **`compte_rendu.pdf`** : Le rapport de synthèse détaillé du projet.

---

## 📊 Synthèse des Résultats Clés

- **Taille du corpus :** 239 textes (classes équilibrées, longueur médiane de 65 mots).
- **Modèle initial :** Réseau dense (64 et 32 neurones) avec une précision de référence (~0,944 - 0,950).
- **Quantification (TFLite) :** 
  - **Taille initiale :** ~509 Ko
  - **Taille finale quantifiée :** 131 Ko (réduction drastique d'environ 74 %)
  - **Précision conservée :** **0,950** (aucune perte de performance malgré la compression).

---

## 🛠️ Technologies et Bibliothèques Utilisées

- **Python**
- **Requêtes & Web Scraping :** `requests`, `BeautifulSoup`
- **Manipulation de données :** `pandas`, `numpy`
- **Deep Learning :** `TensorFlow` / `Keras`, `TensorFlow Lite` (TFLite)

---

## 🚀 Utilisation

1. Clonez le dépôt sur votre machine :
   ```bash
   git clone https://github.com/achahbounehamid/Collecter-des-donn-es-web-API-crawling-scraping-.git
