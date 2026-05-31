# Projets en Data Science & IA 

---
### Prédire le rendement hebdomadaire des actions du DJIA.

Résumé : Modélisation Prédictive du DJIA🎯 Objectif

**Objectif :** Développer un pipeline d'apprentissage statistique pour prévoir les rendements hebdomadaires du Dow Jones Industrial Average (DJIA) et isoler les déciles supérieurs afin de générer de l'alpha (surperformance).

* **Données :**

Source : Base longitudinale de 6 400+ instruments depuis 1998 (agrégateur Sovai).
Variables : Passage de 88 à 65 descripteurs robustes après élimination des données instables ou colinéaires.
Intégrité : Neutralisation du biais de survie (incluant les entreprises radiées comme GE, Kodak) et prévention des fuites d'information (data leakage) par confrontation des données 2024/2026.

* **Méthodologie :** 

Prétraitement : Normalisation robuste (RobustScaler), réduction de dimension (ACP) et intégration de variables retardées (lags).
Validation : Partitionnement chronologique strict pour tester la robustesse face aux régimes de marché :

Apprentissage : 2000–2020 (crises tech, 2008, COVID).
Validation : 2021–2023 (inflation, choc bancaire).
Test : 2024–Mai 2026 (IA, géopolitique).

* **Modélisation & Résultats :** 

Approches comparées : Régressions linéaires (échec sur la non-stationnarité) vs. Ensembles arborescents (XGBoost, LightGBM, Random Forest).
Meilleure performance : Architecture de Stacking (combinaison des modèles) optimisée par recherche bayésienne.
Performance : Supériorité sur la métrique Lift Top 100 et génération d'un alpha robuste malgré la cyclicité économique.

* **Perspectives :** 

Généralisation : Confrontation avec d'autres fournisseurs de données pour éliminer les biais résiduels.
Extension : Test de la méthode sur d'autres marchés géographiques pour valider les invariants structurels.


---

### Prédire la durée des courses de taxi à New-York City

Résumé : https://github.com/FredericDlx/Prediction-de-la-dur-e-des-courses-de-taxi-NYC

Rapport complet : https://fredericdlx.github.io/Prediction-de-la-dur-e-des-courses-de-taxi-NYC/PredictionTaxisNY.html

**Objectif :** Prédire avec précision la durée des trajets de taxi à New York en combinant analyse spatio-temporelle et modèles de régression avancés.

* **Problématique :** Comment la congestion urbaine et la géométrie de la ville influencent-elles le temps de transport ?
* **Technologies :** `R`, `XGBoost`, `ElasticNet`, `K-Means`.
* **Points clés :** 
    * *Feature Engineering* complexe (Distances Haversine/Manhattan, encodage cyclique du temps).
    * Approche hybride **Clustering + Elastic Net** pour capturer les spécificités par quartier.
* **Résultat :** Réduction de l'erreur (RMSE) à **5,1 min** avec XGBoost, **5,8 min** avec Elastic Net + Kmeans et **6,4 min** avec de la régression simple.



---

### Classification d'articles de presse (NLP)

Résumé : https://fredericdlx.github.io/Projet-LLM---Classification-d-articles-de-presse-fran-ais

Rapport complet : https://fredericdlx.github.io/Projet-LLM---Classification-d-articles-de-presse-fran-ais/LLM-Classification-articles-de-presse.html

**Objectif :** Étude comparative de modèles de langage (Transformers) pour la catégorisation automatique d'articles de presse en langue française.

* **Problématique :** Un modèle spécialisé (français) est-il plus performant qu'un modèle massif multilingue ?
* **Technologies :** `Python`, `PyTorch`, `Hugging Face Transformers`, `CamemBERT`, `XLM-RoBERTa`.
* **Points clés :** * Classification multi-classe (13 catégories : Politique, Éco, Sciences, etc.).
    * Mise en place d'un système de labellisation automatique par mots-clés pondérés.
    * *Fine-tuning* sur GPU Tesla P100.
* **Résultat :** Benchmark détaillé démontrant l'efficacité de la spécialisation linguistique de **CamemBERT** sur les subtilités du français.



---

### Data Quality

Project : https://fredericdlx.github.io/Data-Quality/miniproject-DataQuality-ExecMaster.pdf

Rapport complet : https://fredericdlx.github.io/Data-Quality/Project_Data_Quality.html

**Objective of the Project**
* **Task 1 :**
   To develop a Python class (which we could name Prov) that can be used to infer the provenance of each of the operations just presented.
   
   Given the input data frame(s), output data frame, and the kind of operation (vertical reduction, horizontal reduction, etc.),
  construct a tensor that informs on the provenance of the data records of the output data frames
  and how they depend on the input data frames. We will be using binary sparse tensors.

* **Task 2:** Using the tensors that capture the provenance, develop operations on
   tensors that can be used to for querying provenance information. That is
   connect given output records with the corresponding input records, and vice
   versa.
---


