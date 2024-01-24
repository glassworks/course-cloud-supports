# Database as a Service

Pour le stockage des données relationnelles, la plupart des fournisseurs proposent aujourd'hui des options de provisionnement de bases de données.

Le fournisseur se charge de l'installation, de la sécurisation, du stockage des données et des sauvegardes. Cela peut simplifier considérablement le temps et les coûts d'un déploiement, tout en améliorant la sécurité (la plupart des fournisseurs cryptent leurs données stockées).

Comment cela fonctionne-t-il ?

Vous créez une base de données sur le panneau de contrôle du fournisseur :

- vous choisissez le type de données que vous stockez (relationnel, NoSQL, cache)
- vous indiquez le nom de la base de données
- vous fournissez un mot de passe administrateur sécurisé
- vous créez éventuellement d'autres profils d'utilisateurs (limités) dans la base de données (pour utilisation par des API ou d'autres logiciels)

Le fournisseur installe et configure la base de données pour vous et vous fournit une adresse IP ou un FQDN pour accéder à la base de données. Vous copiez généralement ces détails et les utilisez dans le code de votre application, afin que celle-ci puisse se connecter à la base de données pour récupérer et écrire des données.

La plupart des fournisseurs proposent également une interface d'administration (telle que phpMyAdmin) qui vous permet de créer les schémas de la base de données et d'effectuer d'autres tâches administratives.

## Vocabulaire

| Fournisseur | Terme | Type |
|--|--|--|
| AWS | RDS | Relationnel |
| AWS | DocumentDB | NoSQL |
| AWS | DynamoDB | NoSQL |
| Azure | Cosmos DB | Relationnel |
| Azure | Azure SQL | Relationnel |
| GCP | Cloud SQL | Relationnel |
| GCP | Firestore | NoSQL |
| OVH | Hosted Databases (web cloud) | Relationnel |
| Scaleway | SQL Databases | Relationnel |