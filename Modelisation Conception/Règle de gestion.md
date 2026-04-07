RG1. Un dossier d’investissement est identifié de manière unique par une référence dossier.

RG2. Un dossier est déposé par un investisseur principal.
Dans une première version, on suppose un seul investisseur principal par dossier.

RG3. Un dossier concerne un acte demandé principal.
Exemple : autorisation, avis, étude, régularisation, etc.

RG4. Un dossier est rattaché à un secteur d’activité principal.

RG5. Un dossier est localisé dans une province ou préfecture.

RG6. Un dossier peut donner lieu à une décision CRUI à une date donnée.

RG7. Une décision appartient à une catégorie normalisée : avis favorable, avis favorable sous réserve, avis défavorable, à reprogrammer, clôturé, etc.

RG8. Un dossier peut comporter des indicateurs quantitatifs, notamment :
	•	montant d’investissement
	•	nombre d’emplois prévus

RG9. Le montant d’investissement est exprimé en MDHs.

RG10. Les données doivent être normalisées afin d’éviter les doublons, les incohérences d’écriture et les valeurs aberrantes. Cette logique est cohérente avec le nettoyage déjà réalisé en Python.  
RG11. Un dossier peut passer par plusieurs états de traitement au cours de son cycle de vie.

RG12. Un dossier peut être examiné dans une séance CRUI.

RG13. Une séance CRUI examine plusieurs dossiers.

RG14. Un dossier peut être reprogrammé et donc repassé dans plusieurs séances.

RG15. Une décision est prise dans le cadre d’une séance CRUI.

RG16. Un dossier peut avoir un historique de décisions si on veut tracer l’évolution.

RG17. Une province/préfecture appartient à une région.
Dans ton cas, on peut garder la région comme entité secondaire ou attribut fixe.

RG18. Un secteur peut être regroupé dans une famille de secteurs pour faciliter l’analyse.

RG19. Un investisseur peut déposer plusieurs dossiers.

RG20. Un dossier peut être associé à un statut administratif : en cours, traité, reprogrammé, clos.