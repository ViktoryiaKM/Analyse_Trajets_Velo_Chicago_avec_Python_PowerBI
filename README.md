# Optimiser l’offre de mobilité Divvy via la visualisation des usages vélo dans Power BI
*Projet réalisé dans le cadre de ma formation à la Wild Code School.*

## **🚩Problématique **  
La ville de Chicago dispose d’un service de vélos partagés (Divvy) qui générait un important volume de données non exploitées, sans vue consolidée. Impossible, dans ces conditions, d’analyser les 
  
## **🎯 Objectif **  
Fournir un tableau de bord interactif et consolidé pour offrir aux décideurs une vision claire des usages réels du service Divvy, et ainsi optimiser la gestion du parc, adapter l’offre aux profils et aux saisons, et mieux piloter la stratégie de mobilité urbaine.  
 
## **Données sources**  
  •  	Données mensuelles 2021, au format .zip, fournies publiquement par Divvy via AWS S3  
  •	  Chaque fichier contient les trajets réalisés avec des variables comme : heure, station, durée, type d’usager, etc  

##  **Solution mise en place :**   
  •  Collecte & fusion de 12 fichiers mensuels (2021) des données publiques de Divvy depuis AWS S3   
  •  Nettoyage, enrichissement et création de variables clés sous Python (durée, distance, saison, type d’usage...)   
  •  Export du dataset final vers Power BI    
  •  Conception d’un rapport interactif en deux volets :  
    → Profil des usagers (type de vélo, durée, fréquence)  
    → Analyse temporelle (jours, mois, saisons, pics d’usage)  

##  **Résultat:**  
✔️ Transformation de données brutes en un outil décisionnel pour piloter les services de mobilité partagée  
✔️ Visualisation consolidée des usages : identification des profils, pics d’usage et tendances saisonnières  
✔️ Meilleure compréhension des comportements d’usagers, permettant d’ajuster l’offre aux besoins réels  

**Fichier notebook associé :** 
[Preparation_Analyse_trajet_Velo_Chicago__PYTHON.ipynb](https://github.com/ViktoryiaKM/Analyse_Trajets_Velo_Chicago_avec_Python_PowerBI/blob/main/Preparation_Analyse_trajet_Velo_Chicago__PYTHON.ipynb)

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
•	Power BI pour la visualisation -  - Power Query, DAX  
•	Données publiques Divvy via AWS S3  

