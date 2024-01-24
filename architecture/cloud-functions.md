# Serverless functions

Vous avez une application que vous avez codée en utilisant PHP, NodeJS, Python, Ruby ... ?

De nombreux fournisseurs offrent désormais la possibilité de déployer votre application en téléchargeant simplement la base de code sur leurs serveurs. 

Ils fournissent de manière transparente le CPU, la RAM, le réseau nécessaire à l'exécution de votre code. Cela signifie qu'en tant que développeur ou entreprise, vous avez une abstraction totale de l'architecture de déploiement sous-jacente.

Comment cela fonctionne-t-il ? En général, les étapes suivantes sont nécessaires :

- Vous fournissez les détails de connexion à votre dépôt GIT
- Lorsque vous poussez un tag ou une branche spécifique, une opération CI/CD est lancée.
- Les procédures qui détaillent comment construire et déployer votre code sont automatiquement exécutées.
- La version finale est copiée, conteneurisée et démarrée sur une infrastructure de production.
- Votre application est prête à être utilisée !


Avantages :

- Vous pouvez vous concentrer sur votre application et non sur tous les détails du déploiement, de la mise à l'échelle, etc. qui peuvent être longs et coûteux.
- Contrôle de version : il est facile de déployer et de revenir en arrière, puisqu'il est basé sur GIT.

Inconvénients :
- les fonctions serverless vraiment performantes peuvent rapidement devenir coûteuses.
- coûts cachés : parfois les fournisseurs facturent au nombre de données transférées, ou au nombre total d'heures de traitement effectuées. Cela peut parfois donner lieu à des factures surprenantes.
- dépendance : vous êtes totalement dépendant de leur architecture. Tout ralentissement ou interruption de service est totalement hors de votre contrôle.


## Containers

Un niveau en dessous des fonctions sans serveur est l'option de déploiement de conteneurs.

Un conteneur est une collection de fichiers qui inclut tout votre code ainsi que les dépendances du système d'exploitation afin de s'exécuter. Cela rend le déploiement beaucoup plus facile, car il simplifie les problèmes de dépendance lors du déploiement de notre code.

Docker est un exemple de système de conteneurisation très populaire.

De nombreux fournisseurs de cloud ont l'option de spécifier simplement l'**Image** à exécuter (typiquement précompilée dans le registre Docker, ou dans notre propre registre privé), et provisionneront automatiquement un ou plusieurs conteneurs en notre nom.


## Vocabulaire

| Fournisseur | Terme |
|--|--|
| AWS | Lambda |
| Azure | Application de fonction |
| GCP | Cloud Run / Firebase functions |
| OVH |  |
| Scaleway | Serverless Functions / Containers |