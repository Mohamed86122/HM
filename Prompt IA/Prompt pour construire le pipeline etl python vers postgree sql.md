Agis comme un data engineer senior.

Contexte :
Je dispose d’un fichier Excel nettoyé contenant des données sur des dossiers d’investissement. Je veux charger ces données dans PostgreSQL selon une structure relationnelle normalisée.

Je veux que tu me proposes un pipeline ETL Python complet.

Je veux exactement :
1. la stratégie ETL générale,
2. l’ordre de chargement des tables,
3. les transformations à appliquer pour chaque colonne,
4. la gestion des doublons,
5. la création des tables de dimension/référence,
6. l’affectation des identifiants techniques,
7. la gestion des jointures entre le DataFrame Excel et les identifiants PostgreSQL,
8. un script Python complet utilisant pandas + sqlalchemy + psycopg2,
9. des exemples d’insertion dans PostgreSQL,
10. des contrôles qualité après chargement.

Mon besoin :
- lire Excel avec pandas,
- nettoyer les colonnes,
- créer les tables de référence comme secteur, province, décision, acte, investisseur,
- créer ensuite la table dossier avec les clés étrangères,
- garantir la cohérence des données.

Je veux du code clair, modulaire et directement réutilisable.