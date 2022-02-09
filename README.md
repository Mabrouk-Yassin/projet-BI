# Conception d’un Dashboard Interactif pour l’analyse des Remboursements d’Assurance Maladie

## Résumé
Ce projet porte sur la création d’un outil décisionnel qui permet d’analyser les remboursements mensuels effectués par le régime général de l'Assurance Maladie. Le business intelligence (informatique décisionnelle) joue un rôle très important dans l’aide à la prise de décision au niveau des entreprises. Cette discipline est utilisée dans plusieurs domaines et secteurs d’activité dont le domaine des assurances est parmi l’un des utilisateurs. Ce projet consiste à développer un tableau de bord interactif qui permet d’aider les manager à prendre la bonne décision en analysant les données disponibles. Comme tout projet du BI la première étape est la planification du projet en analysant le besoin. La deuxième étape est le processus ETL (Extract Transform Load) qui signifie transformer, transformer et charger. Cette phase consiste à la collecte des données de différentes sources (fichier Excel, base de données …), appliquer des transformations pour nettoyer et organiser les données et le chargement de ces derniers dans une base de données. Après le stockage des données dans un Data Warehouse (entrepôt de données) en respectant un modèle précis (modèle en étoile, modèle en flocont de neige…). Ensuite dès que les données sont prêtes l’analyse commence en utilisant des techniques de statistique et autre afin d’extraire de la connaissance. Enfin une visualisation à travers des tableaux de bord interactif sous forme de jolies interfaces destinées aux différents utilisateurs selon leur droit d’accès.


## Introduction : 
### 1.	Contexte général :
Ce projet porte sur la création d’un tableau de bord interactif qui permet de visualiser les remboursements mensuels effectués par le régime général de l'Assurance Maladie en France. Les opérations liées au domaine d’assurance génèrent un nombre important de données depuis différentes sources. Ces dernières il faut les analyser à fin de prendre la bonne décision. Dans ce projet une base de données contient l'ensemble des remboursements mensuels effectués par le régime général de l'Assurance est proposée. Les dépenses sont indiquées en montants remboursés et présentées au remboursement. L’idée est de faire parler ces données en utilisant le Business intelligence ou l’informatique décisionnelle.

### 2.	Problématique :
Comme on a expliqué dans la partie précédente, notre problématique est la collecte de ces données et les nettoyer en appliquant le processus ETL, les stocker dans un entrepôt de données, les visualiser sous forme des tableaux de bord interactifs et tout ça dans le but faciliter l’analyse et la prise de décision par les responsables d’entreprises.

### 3.	Outils et technologies utilisés :
Dans ce projet on a utilisé les outils suivants :

Sql Server Management Studio pour la conception de notre Data Warehouse.

Sql Server Integration Services pour le processus ETL (Extract, Transform, Load). 

Tableau pour la visualisation des données sous forme des tableaux de bord interactif.

![11](https://user-images.githubusercontent.com/81876011/152695253-12d33b00-f62d-4ca6-9440-62259ac9014d.png)


## Conception :

### 1.	Data Warehouse :
La conception de notre Data Warehouse est composé d’une table des faits « remboursement ». Les tables de dimensions sont nature_assurance, mode_exercice_prescripteur, caisse_primaire, qualite_beneficiaire, specialite_executant, specialite_prescripteur, nature_prestation, regroupement_exercie_executant, regroupemet_specialite_prescripteur, regroupement_speciate_executant, annee, serie_statistique_mensuelle, mode_exercice_executant et top_section_locale_mutualiste.

![image](https://user-images.githubusercontent.com/81876011/152695363-4b0ba659-18a2-40cc-b961-17e87daf6d02.png)
![image](https://user-images.githubusercontent.com/81876011/152695371-f2d5638b-5002-4f7c-8a34-61fca60fba86.png)

### 2.	Processus ETL
Pour la phase ETL, on a commencé par initialiser et remplir les données des fichiers Excel dans une base de données source à l’aide d’une boucle. Ensuite on vide la table des faits, on initialise et on remplit les tables de dimensions depuis la base de données source tout en respectant les clés étrangères. Enfin on remplit la table des faits. Les figures suivantes illustrent les étapes d’ETL :

![image](https://user-images.githubusercontent.com/81876011/152695452-d3d3ccb1-3221-4fce-a616-6e9372f60b56.png)
![image](https://user-images.githubusercontent.com/81876011/152695463-b7b82a50-9580-4c02-bbf1-88914a85306c.png)
![image](https://user-images.githubusercontent.com/81876011/152695484-f8555766-4254-4138-ace9-b45bcd1594b3.png)
![image](https://user-images.githubusercontent.com/81876011/153166367-1e463ff1-9e62-40fc-bbe3-8632639f16e2.png)
![1](https://user-images.githubusercontent.com/81876011/153166707-1c6d7e02-a659-4a49-837d-324d316046ec.png)

## Visualisation :
![image](https://user-images.githubusercontent.com/81876011/153166974-b42c3233-ce32-4ffd-9646-fddb5e40127c.png)
![image](https://user-images.githubusercontent.com/81876011/153166996-050a2563-d9e4-46fb-a332-4de916fe5d3d.png)

Références
https://www.data.gouv.fr/fr/datasets/depenses-d-assurance-maladie-hors-prestations-hospitalieres-par-caisse-primaire-departement/





