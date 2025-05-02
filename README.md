# Analyse des Trajets Vélo à Chicago (Divvy) – Projet Data Analyst
## **🎯 Objectif**  
Préparer et analyser un jeu de données issu du service de vélos en libre-service Divvy à Chicago afin de :  
•	Comprendre les comportements d’usage selon le temps, le type d’utilisateur et le type de trajet  
•	Construire des visualisations claires et dynamiques dans Power BI  

## **Données sources**  
  •  	Données mensuelles 2021, au format .zip, fournies publiquement par Divvy via AWS S3  
  •	  Chaque fichier contient les trajets réalisés avec des variables comme : heure, station, durée, type d’usager, etc  
  
## **I. Étapes de préparation (dans le Notebook avec Python) :**  
1.	Importation & fusion des 12 fichiers  
Téléchargement automatique depuis AWS S3 – Divvy , extraction et concaténation dans un seul DataFrame.

3.	Nettoyage & transformation des données  
  •	Conversion des dates  
  •	Calcul de la durée du trajet (en secondes et en minutes)  
  •	Suppression des valeurs nulles, trajets incohérents (durée négative, vitesse > 45 km/h, trajets tests)  
  •	Nettoyage des espaces dans les noms de stations  

3.	Enrichissement  
•	Calcul de la distance (formule de Haversine)  
•	Création de nouvelles colonnes temporelles : jour, mois, heure, saison  
•	Classification des trajets : round trip / one-way trip  
•	Calcul de la vitesse moyenne en km/h  
4.	Export final  
•	Création d’un jeu de données propre (cyclistic_clean.csv)  
•	Téléchargement pour intégration dans Power BI

**Fichier notebook associé :** 

## **II. Analyse et visualisation (dans Power BI)**  
Création d’un tableau de bord interactif organisé en deux parties :  

**1. Profil des usagers et comportement**:  
•	Répartition membres / occasionnels  
•	Type de vélo utilisé  
•	Distance et durée moyennes  
•	Type de trajet (aller simple ou aller-retour)  

**2. Analyse temporelle** :  
•	Répartition par jour, semaine, mois, saison  
•	Durée moyenne selon le jour  
•	Volume d’usage semaine vs week-end  
•	Saisonnalité des trajets  

**Fichier Power BI associé :**
[Dashboard_Analyse_Trajets_Velo_Chicago_PowerBI.gif](https://github.com/ViktoryiaKM/Analyse_Trajets_Velo_Chicago_avec_Python_PowerBI/blob/main/Dashboard_Analyse_Trajets_Velo_Chicago_PowerBI.gif)


## **Outils utilisés :**  
•	Python (Pandas, NumPy) sur Google Colab  
•	Power BI pour la visualisation  
•	Données publiques Divvy via AWS S3  

