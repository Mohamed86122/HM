DOSSIER

Représente l’objet principal du système.

Attributs possibles :
	•	id_dossier (identifiant technique)
	•	reference_dossier
	•	date_depot (si disponible plus tard)
	•	montant_investissement_mdh
	•	nombre_emplois
	•	observation
	•	statut_dossier

INVESTISSEUR
	•	id_investisseur
	•	nom_investisseur
	•	type_investisseur (optionnel)
	•	nationalite (optionnel)
	•	contact (optionnel)

SECTEUR
	•	id_secteur
	•	libelle_secteur
	•	code_secteur (optionnel)

PROVINCE_PREFECTURE
	•	id_province
	•	nom_province
	•	type_territoire (province / préfecture)

ACTE_DEMANDE
	•	id_acte
	•	libelle_acte
	•	description_acte (optionnel)

DECISION
	•	id_decision
	•	libelle_decision
	•	categorie_decision
	•	description_decision (optionnel)

SEANCE_CRUI
	•	id_seance
	•	date_seance
	•	numero_seance
	•	annee_seance
	•	observation_seance

ETAT_DOSSIER
	•	id_etat
	•	libelle_etat
	•	description_etat

REGION
	•	id_region
	•	nom_region

FAMILLE_SECTEUR
	•	id_famille_secteur
	•	libelle_famille

HISTORIQUE_DOSSIER

Entité associative ou historique.
	•	id_historique
	•	date_evenement
	•	commentaire
	•	type_evenement