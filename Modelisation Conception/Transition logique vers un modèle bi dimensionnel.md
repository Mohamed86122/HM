Étape 1 : modèle Merise

On modélise d’abord le métier de manière normalisée :
	•	dossier
	•	investisseur
	•	acte
	•	secteur
	•	province
	•	séance
	•	décision

Étape 2 : alimentation depuis l’Excel

Les données nettoyées avec Python sont intégrées dans PostgreSQL.
Le modèle relationnel sert de socle de stockage structuré.

Étape 3 : création d’un datamart décisionnel

À partir du modèle relationnel, on construit un schéma dimensionnel pour la BI.

⸻

Proposition de modèle BI

Table de faits : FAIT_DOSSIER_INVESTISSEMENT

Grain conseillé :
une ligne = un dossier examiné à une date donnée / dans une séance donnée

Mesures :
	•	montant_investissement_mdh
	•	nombre_emplois
	•	nombre_dossiers = 1
	•	delai_traitement si calculable

Clés :
	•	id_date
	•	id_province
	•	id_secteur
	•	id_decision
	•	id_acte
	•	id_investisseur
	•	id_seance éventuellement

⸻

Dimensions

DIM_DATE
	•	id_date
	•	date_complete
	•	jour
	•	mois
	•	trimestre
	•	annee

DIM_PROVINCE
	•	id_province
	•	nom_province
	•	type_territoire
	•	region

DIM_SECTEUR
	•	id_secteur
	•	libelle_secteur
	•	famille_secteur

DIM_DECISION
	•	id_decision
	•	libelle_decision
	•	categorie_decision

DIM_ACTE
	•	id_acte
	•	libelle_acte

DIM_INVESTISSEUR
	•	id_investisseur
	•	nom_investisseur
	•	type_investisseur

DIM_SEANCE
	•	id_seance
	•	numero_seance
	•	date_seance
	•	annee_seance

⸻

Pourquoi ce passage est logique

Parce que :
	•	le Merise sert à modéliser le métier
	•	le relationnel sert à stocker proprement
	•	le dimensionnel sert à analyser efficacement

C’est exactement la chaîne logique attendue dans un PFE BI sérieux.