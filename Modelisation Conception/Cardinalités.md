INVESTISSEUR — DEPOSER — DOSSIER
	•	Un investisseur dépose : (0,n) dossiers
	•	Un dossier est déposé par : (1,1) investisseur

Hypothèse simple et défendable.
Si plus tard tu veux plusieurs investisseurs par dossier, on changera.

⸻

DOSSIER — CONCERNER — SECTEUR
	•	Un secteur concerne : (0,n) dossiers
	•	Un dossier concerne : (1,1) secteur

⸻

DOSSIER — LOCALISER — PROVINCE_PREFECTURE
	•	Une province/préfecture localise : (0,n) dossiers
	•	Un dossier est localisé dans : (1,1) province/préfecture

⸻

DOSSIER — PORTER_SUR — ACTE_DEMANDE
	•	Un acte demandé est lié à : (0,n) dossiers
	•	Un dossier porte sur : (1,1) acte demandé

⸻

DOSSIER — ABOUTIR_A — DECISION

Deux options :

Option 1 — simple
	•	Une décision concerne : (0,n) dossiers
	•	Un dossier aboutit à : (0,1) décision

Pourquoi 0,1 ?
Parce qu’un dossier peut être encore en cours.

Option 2 — historique

Si tu veux gérer plusieurs décisions dans le temps :
	•	un dossier peut avoir (0,n) décisions
	•	une décision-type peut être appliquée à (0,n) dossiers

Dans ce cas il faut une association historique avec date.

⸻

SEANCE_CRUI — EXAMINER — DOSSIER
	•	Une séance examine : (1,n) dossiers
	•	Un dossier est examiné dans : (0,n) séances

Le 0,n côté dossier est pertinent si reprogrammation.

⸻

DOSSIER — AVOIR_ETAT — ETAT_DOSSIER

Version courante
	•	Un état concerne : (0,n) dossiers
	•	Un dossier a : (1,1) état courant

Version historique
	•	Un dossier peut avoir (0,n) changements d’état

⸻

PROVINCE_PREFECTURE — APPARTENIR — REGION
	•	Une région contient : (1,n) provinces/préfectures
	•	Une province/préfecture appartient à : (1,1) région

⸻

SECTEUR — CLASSER — FAMILLE_SECTEUR
	•	Une famille regroupe : (1,n) secteurs
	•	Un secteur appartient à : (1,1) famille