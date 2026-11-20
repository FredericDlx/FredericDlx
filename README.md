# Projets en Data Science & IA 

---
### Atteindre plus de 50% de précision au Go avec une IA miniature

Résumé : [Frederic_Delcroix_Rapport_Jeu_de_Go_Executive_Master_IA_Sciences_Des_donnees_2026.pdf](https://github.com/FredericDlx/Go/blob/main/Frederic_Delcroix_Rapport_Jeu_de_Go_Executive_Master_IA_Sciences_Des_donnees_2026.pdf)

Rapport complet : https://github.com/FredericDlx/Go/blob/main/Frederic_Delcroix_Rapport_Jeu_de_Go_Executive_Master_IA_Sciences_Des_donnees_2026.ipynb

**Objectif :** Concevoir un réseau de neurones capable d'évaluer le plateau de Go et de prédire le meilleur coup.
               Respecter une contrainte matérielle stricte en limitant la taille du modèle à environ 100 000 paramètres.

* **Données et Environnement :**
    Utilisation de la librairie golois pour encoder l'état du goban sous la forme de 31 plans spatiaux (19x19).

Intégration de caractéristiques expertes complexes (historique, décompte des libertés, ladders) pour guider l'apprentissage.

* **Méthodologie et Stack Technique :**
    Évaluation de plusieurs architectures convolutives économes en paramètres (ResNet, MobileNetV2, SE+Swish, MixNet).

    Application de stratégies de compression avancées via la Distillation de connaissances et l'Élagage (Pruning).

* **Modélisation et Résultats :**
    Parmi les modèles de 100k paramètres entraînés de zéro, l'architecture SE + Swish domine avec 47,2% de précision.

    La meilleure performance globale (49,0%) est atteinte par l'Élagage progressif d'un modèle Professeur réduit à une sparsité de 66,6%.

* **Perspectives :**
    Maximiser la technique de distillation en exploitant un modèle Professeur beaucoup plus large et puissant.

    Explorer de nouvelles méthodes d'élagage, telles que le Movement Pruning, pour repousser le plafond de précision actuel.

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
  
* **Technologies :** `Python`, `sparse binary tensor`

* **Conclusion**
      We implemented a row-level provenance capture system for the four core operations (filter, merge, concat, SMOTE), extended with two utility decorators (dropna and a 1-to-1 hook). All decorators share a uniform four-step pattern, which keeps       the Prov class small and the API consistent across operations.

    Three results stand out:

        Massive Compression: Compression up to ~900× versus dense storage, thanks to the sparse boolean CSR format.
        Low Execution Overhead: Low overhead on realistic workloads: +2% on Census (1.1 s pipeline), rising to +7-25% on the smaller pipelines where the per-step instrumentation cost weighs more relative to the few-millisecond baseline.
        High-Performance Tracking: Near-instantaneous queries, since looking up provenance reduces to a single sparse row or column slice.

    Taken together, these results show that the system imposes a marginal cost on realistic pipelines while keeping its memory footprint orders of magnitude below the data it tracks — making row-level provenance practical to enable by default.
---


