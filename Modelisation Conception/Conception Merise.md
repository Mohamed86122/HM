Pourquoi DOSSIER est l’entité centrale

Parce que tout tourne autour de lui :
	•	investisseur
	•	secteur
	•	province
	•	acte
	•	décision
	•	séance
	•	montant
	•	emplois

C’est le cœur métier évident.

Pourquoi séparer INVESTISSEUR, SECTEUR, PROVINCE, ACTE, DECISION

Parce qu’en Excel, ces informations sont souvent répétées en texte brut, ce qui provoque :
	•	incohérences d’écriture
	•	redondances
	•	erreurs de saisie
	•	difficulté de maintenance

La normalisation permet :
	•	cohérence
	•	intégrité
	•	réutilisation
	•	évolutivité

Ton nettoyage Python montrait déjà ce besoin avec l’harmonisation des libellés de secteurs, provinces et décisions. Donc ce choix est totalement justifié.

Pourquoi introduire SEANCE_CRUI

Parce que, métier parlant, une décision n’apparaît pas “dans le vide”.
Elle est généralement liée à une instance d’examen.

Donc la vraie logique métier est :
dossier → examiné en séance → décision

C’est plus robuste qu’un simple champ texte “décision” dans DOSSIER.

⸻

Pourquoi introduire EXAMEN_DOSSIER

Parce que la relation entre dossier et séance est n,n :
	•	une séance examine plusieurs dossiers
	•	un dossier peut revenir dans plusieurs séances

Il faut donc une entité associative.

⸻

Pourquoi introduire HISTORIQUE_DOSSIER

Parce qu’un système de suivi crédible ne stocke pas seulement l’état final.
Il doit pouvoir expliquer :
	•	quand le dossier a été déposé
	•	quand il a été examiné
	•	quand il a été reprogrammé
	•	quand il a été clôturé

Même si tu ne l’implémentes pas complètement, le mettre dans la conception montre de la maturité.

8. Limites du modèle relationnel pour l’analyse décisionnelle

C’est un point très important pour ton PFE.

Le modèle relationnel Merise est bon pour :
	•	structurer les données métier
	•	éviter la redondance
	•	garantir l’intégrité
	•	gérer les opérations courantes

Mais il a des limites pour la BI.

Limite 1 : trop normalisé pour l’analyse

Pour faire un tableau de bord, il faut souvent joindre plusieurs tables :
	•	dossier
	•	secteur
	•	province
	•	décision
	•	acte
	•	séance
	•	date

Cela ralentit l’analyse et complique les requêtes.

Limite 2 : pas optimisé pour les agrégations

Les besoins BI demandent :
	•	total des investissements par province
	•	nombre de dossiers par secteur
	•	taux d’avis favorable par année
	•	emplois créés par territoire

Le modèle relationnel n’est pas pensé en priorité pour ce type d’agrégations massives.

Limite 3 : difficulté d’analyse historique simplifiée

L’analyse décisionnelle aime répondre vite à :
	•	évolution annuelle
	•	comparaison trimestrielle
	•	cumul par année
	•	tendance par secteur

D’où le besoin d’une dimension temps structurée.

Limite 4 : moins lisible pour les outils BI

Power BI ou tout autre outil décisionnel travaille mieux avec :
	•	une table de faits
	•	des dimensions claires
	•	des relations simples