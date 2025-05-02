# Analyse des Trajets Vélo à Chicago (Divvy) – Projet Data Analyst
**🎯 Objectif**
Préparer et analyser un jeu de données issu du service de vélos en libre-service Divvy à Chicago afin de :
•	Comprendre les comportements d’usage selon le temps, le type d’utilisateur et le type de trajet
•	Construire des visualisations claires et dynamiques dans Power BI

**📁 Données sources**
•	Données mensuelles 2021, au format .zip, fournies publiquement par Divvy via AWS S3
•	Chaque fichier contient les trajets réalisés avec des variables comme : heure, station, durée, type d’usager, etc
**🛠️ Étapes de préparation (dans le Notebook avec Python) :**
1.	Importation & fusion des 12 fichiers
Téléchargement automatique depuis AWS S3 – Divvy , extraction et concaténation dans un seul DataFrame.
2.	Nettoyage & transformation des données
o	Conversion des dates
o	Calcul de la durée du trajet (en secondes et en minutes)
o	Suppression des valeurs nulles, trajets incohérents (durée négative, vitesse > 45 km/h, trajets tests)
o	Nettoyage des espaces dans les noms de stations
3.	Enrichissement
o	Calcul de la distance (formule de Haversine)
o	Création de nouvelles colonnes temporelles : jour, mois, heure, saison
o	Classification des trajets : round trip / one-way trip
o	Calcul de la vitesse moyenne en km/h
4.	Export final
o	Création d’un jeu de données propre (cyclistic_clean.csv)
o	Téléchargement pour intégration dans Power BI
Fichier notebook associé : Business_Case_Chicago_Velos_analyse_trajet_PYTHON.ipynb

**📊 Analyse et visualisation (dans Power BI)**
Création d’un tableau de bord interactif organisé en deux parties :

Profil des usagers et comportement : 
•	Répartition membres / occasionnels
•	Type de vélo utilisé
•	Distance et durée moyennes
•	Type de trajet (aller simple ou aller-retour)

Analyse temporelle :
•	Répartition par jour, semaine, mois, saison
•	Durée moyenne selon le jour
•	Volume d’usage semaine vs week-end
•	Saisonnalité des trajets

**Fichier Power BI associé :**
**📌 Outils utilisés :**
•	Python (Pandas, NumPy) sur Google Colab
•	Power BI pour la visualisation
•	Données publiques Divvy via AWS S3

