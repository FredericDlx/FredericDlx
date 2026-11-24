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




