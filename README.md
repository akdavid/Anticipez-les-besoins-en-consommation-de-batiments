
# Prédiction des Émissions de CO2 et de la Consommation Énergétique des Bâtiments à Seattle

## Contexte

La ville de Seattle vise à devenir neutre en émissions de carbone d'ici 2050. Dans ce contexte, une analyse approfondie de la consommation énergétique et des émissions de CO2 des bâtiments non résidentiels est nécessaire. Ce projet se concentre sur l'analyse de données récoltées en 2016 pour prédire les émissions de CO2 et la consommation énergétique totale des bâtiments non résidentiels. Les prédictions sont basées sur les caractéristiques structurelles des bâtiments, telles que leur taille, usage, date de construction, et localisation géographique.

L'un des objectifs est également d'évaluer l'intérêt de l'ENERGY STAR Score pour prédire les émissions de CO2, un score qui est actuellement calculé de manière complexe.

## Structure du Répertoire

- `data/`
  - `cleaned/` : Contient les fichiers de données nettoyées pour les différentes étapes de la modélisation.
    - `df_cleaned.csv`
    - `df_SiteEnergyUseWN_0_no_log.csv`
    - `df_SiteEnergyUseWN_0.csv`
    - `df_SiteEnergyUseWN_1.csv`
    - `df_TotalGHGEmissions_0_no_log.csv`
    - `df_TotalGHGEmissions_0.csv`
    - `df_TotalGHGEmissions_1.csv`
  - `source/` : Contient les données brutes originales.
    - `2016_Building_Energy_Benchmarking.csv`
- `.gitignore` : Fichiers et dossiers à exclure du suivi Git.
- `01_EDA.ipynb` : Analyse exploratoire initiale des données (Exploratory Data Analysis).
- `02_modelisation_energy_0.ipynb` : Première phase de modélisation pour la prédiction de la consommation énergétique.
- `03_modelisation_gas_0.ipynb` : Première phase de modélisation pour la prédiction des émissions de gaz à effet de serre.
- `04_gradient_boosting_energy_v2.ipynb` : Optimisation de la modélisation énergétique par Gradient Boosting (version 2).
- `04_gradient_boosting_energy.ipynb` : Modélisation énergétique par Gradient Boosting.
- `05_gradient_boosting_gas.ipynb` : Modélisation des émissions de gaz à effet de serre par Gradient Boosting.
- `06_EDA_feature_engineering.ipynb` : Exploration des données avec ajout de nouvelles caractéristiques (feature engineering).
- `07_gradient_boosting_energy_feature_engineering.ipynb` : Modélisation énergétique avec de nouvelles caractéristiques.
- `08_gradient_boosting_gas_feature_engineering.ipynb` : Modélisation des émissions de gaz avec de nouvelles caractéristiques.
- `09_gradient_boosting_energy_stratification.ipynb` : Stratification des données pour la modélisation énergétique.
- `10_gradient_boosting_gas_stratification.ipynb` : Stratification des données pour la modélisation des émissions de gaz.
- `11_gradient_boosting_energy_feature_importance.ipynb` : Analyse de l'importance des caractéristiques pour la modélisation énergétique.
- `12_gradient_boosting_gas_feature_importance.ipynb` : Analyse de l'importance des caractéristiques pour la modélisation des émissions de gaz.
- `13_gradient_boosting_energy_final_energystarscore.ipynb` : Modélisation énergétique finale incluant l'ENERGY STAR Score.
- `14_gradient_boosting_gas_final_energystarscore.ipynb` : Modélisation des émissions de gaz finale incluant l'ENERGY STAR Score.
- `15_EDA_bonus_without_log.ipynb` : Analyse exploratoire sans transformation logarithmique des données.
- `16_modelisation_energy_0_no_log.ipynb` : Modélisation énergétique sans transformation logarithmique.
- `17_modelisation_gas_0_no_log.ipynb` : Modélisation des émissions de gaz sans transformation logarithmique.
- `local_feature_importance_energy.html` : Visualisation de l'importance locale des caractéristiques pour la modélisation énergétique.
- `local_feature_importance_gas.html` : Visualisation de l'importance locale des caractéristiques pour la modélisation des émissions de gaz.

## Mission et Objectifs

L'objectif principal de ce projet est de prédire :
- Les émissions de CO2 des bâtiments non résidentiels.
- La consommation totale d'énergie de ces bâtiments.

Les prédictions se baseront sur les données structurelles des bâtiments. L'analyse a également pour but d'évaluer la pertinence de l'ENERGY STAR Score pour la prédiction des émissions de CO2.

**Étapes principales :**
1. Réaliser une analyse exploratoire des données pour comprendre leur structure et identifier les variables pertinentes.
2. Tester et comparer différents modèles de machine learning pour effectuer les prédictions.
3. Évaluer les performances de chaque modèle grâce à une validation croisée et optimiser leurs hyperparamètres.
4. Explorer l'impact de l'utilisation de l'ENERGY STAR Score sur les performances des modèles.

## Avertissements et Conseils
- Attention à la fuite de données : ne pas utiliser les relevés de consommation annuels futurs dans les prédictions.
- Explorer et transformer les variables pour améliorer les performances des modèles.
- Mettre en place une évaluation rigoureuse des modèles, notamment via une validation croisée.

