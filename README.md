# 📊 Segmentation Client Premium - Mall Customer Analytics

[![Python](https://img.shields.io/badge/Python-3.8+-2F80ED.svg?style=flat&logo=python&logoColor=white)](https://www.python.org)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Latest-F2994A.svg?style=flat&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Plotly](https://img.shields.io/badge/Plotly-Interactive-9B51E0.svg?style=flat&logo=plotly&logoColor=white)](https://plotly.com/)

## 1. Executive Summary & Objectifs Business

Ce projet répond à une problématique classique de **Customer Analytics** : transformer une base client brute en segments homogènes, compréhensibles et activables par les équipes marketing afin d'optimiser le ROI des campagnes publicitaires.

L'objectif principal est de segmenter les clients d'un centre commercial en fonction de leurs caractéristiques démographiques et de leurs habitudes d'achat. L'approche adoptée suit une logique de conseil en analytics, mettant l'accent sur la recherche d'un modèle qui ne maximise pas seulement les indicateurs mathématiques (métriques de clustering), mais qui produit avant tout des groupes stables, interprétables et actionnables d'un point de vue business.

### ❓ Questions business cibles :
1. Existe-t-il des groupes naturels de clients selon leur âge, revenu annuel et score de dépense ?
2. Quels segments présentent le plus fort potentiel commercial ?
3. Quels segments nécessitent une stratégie de fidélisation, d'upsell ou de réactivation ?
4. Comment transformer un résultat de clustering en recommandations concrètes pour une équipe marketing ?

---

## 📂 Structure du Dataset

Le projet s'appuie sur le dataset **Mall Customer Segmentation**. Il comprend 200 profils clients uniques sans valeurs manquantes, découpés selon les variables suivantes :
* `CustomerID` : Identifiant unique du client.
* `Gender` : Sexe (Male / Female).
* `Age` : Âge du client (de 18 à 70 ans).
* `Annual Income (k$)` : Revenu annuel exprimé en milliers de dollars.
* `Spending Score (1-100)` : Score attribué par le centre commercial selon le comportement d'achat.

---

## 🛠️ Approche Méthodologique

La démarche analytique est structurée en 5 grandes étapes au sein du notebook :

1.  **Analyse Exploratoire des Données (EDA) :** Étude des distributions des variables (âge, revenus, scores), détection des corrélations et premières visualisations des patterns de dépenses.
2.  **Préparation des Données :** Encodage des variables catégorielles, standardisation des caractéristiques numériques (`StandardScaler`) pour éviter les biais d'échelle.
3.  **Analyse Comparative des Modèles :** Entraînement et comparaison de 3 architectures d'apprentissage non supervisé :
    * **K-Means** (Recherche du $K$ optimal via la méthode du coude et le score de Silhouette).
    * **Clustering Hiérarchique (CAH)** (Analyse du dendrogramme avec lien de Ward).
    * **DBSCAN** (Modèle basé sur la densité avec recherche de l'Epsilon optimal via les plus proches voisins).
4.  **Évaluation Quantitative :** Calcul des métriques de référence : Score de Silhouette, Index de Calinski-Harabasz et Index de Davies-Bouldin.
5.  **Profilage Business (Personas) :** Traduction des clusters mathématiques en Personas Marketing avec recommandations stratégiques dédiées.

---

## 💻 Technologies & Librairies Utilisées

* **Manipulation de données :** `pandas`, `numpy`
* **Visualisations graphiques :** `matplotlib`, `seaborn`, `plotly` (visualisations interactives 2D et 3D)
* **Machine Learning (Clustering) :** `scikit-learn` (`KMeans`, `AgglomerativeClustering`, `DBSCAN`, `StandardScaler`, `PCA`)
* **Analyse Statistique :** `scipy` (`linkage`, `dendrogram`)

---

## 🚀 Installation et Utilisation

### Prérequis
Assurez-vous d'avoir Python 3.8+ installé.

### 1. Cloner le repository
```bash
git clone [https://github.com/votre-username/customer-segmentation.git](https://github.com/votre-username/customer-segmentation.git)
cd customer-segmentation
