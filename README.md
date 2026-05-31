# Projets en Data Science & IA 

### Prédire la durée des courses de taxi à New-York City

Résumé : https://fredericdlx.github.io/Pr-diction-de-la-dur-e-des-courses-de-taxi-NYC

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


