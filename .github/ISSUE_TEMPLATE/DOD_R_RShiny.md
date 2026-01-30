
---
name: "DOD R"
about: "Checklist Definition of Done pour le front"
labels: []
assignees: []
---

# DoD – Développeurs R (Backend / Data / Scripts)

## Qualité du code

-   [ ] Les docstrings / commentaires sont créés ou mis à jour pour toutes les fonctions impactées +
-   [ ] ~~Le code est formaté avec formatR et/ou styler ( AIR utilisé à l'ATIH ) Audit à faire sur les formateurs~~
-   [ ] Le code est découpé en fonctions simples, testables (TUs) et cohérentes (1 fonction = 1 tâche) \~
-   [ ] ~~Aucune fonction ne dépasse 150 lignes (limite à définir)~~
-   [ ] Aucun code nouvellement créé est dupliqué (DRY), sinon il faut faire une fonction dédiée +
-   [ ] N’utilise pas de grepl dans un filter() pour filtrer une dataframe (préférer str_detect(), les méthodes tidyverse ou équivalent) \~+
-   [ ] ~~Les conventions de nommage du projet sont respectées recheche biblio à faire~~
-   [ ] ~~Le package lintr ne renvoi pas d'erreur~~

## Tests

-   [ ] ~~Les tests unitaires (testthat) sont créés pour les nouvelles fonctions~~
-   [ ] ~~Les tests unitaires existants sont mis à jour si nécessaire~~
-   [ ] ~~Tous les tests unitaires passent (Status : PASSED)~~
-   [ ] ~~Les tests fonctionnels (TF) sont créés pour les nouvelles fonctionnalités~~
-   [ ] ~~Les tests fonctionnels modifiés sont mis à jour~~
-   [ ] ~~Tous les tests fonctionnels passent (Status : PASSED)~~
-   [ ] ~~Le coverage des tests atteint le seuil attendu (seuil à définir, 80 % par défault)~~

## Documentation

-   [ ] ~~Le README, wiki ou manuel utilisateur est mis à jour~~
-   [ ] Les scripts R ou packages s’exécutent sans warnings inattendus ( packaging ifaq et TDBESMS, non prioritaire ) \~

## Git & collaboration

-   [ ] ~~Les commits respectent la convention de nommage interne (ex : Conventional Commits)~~
-   [ ] La Pull Request ne contient pas de fichiers inutiles (data temporaire, caches, .Rhistory…), le git ignore est à jour +
-   [ ] ~~Le changelog est mis à jour~~
-   [ ] J'ai pull la branche main / dev et je l'ai mergé dans ma branche avant de la push sur le repo distant \~
-   [ ] ~~La branche est à jour avec main / dev avant merge~~

# Definition of Done – R Shiny

## Réactivité & logique serveur

-   [ ] ~~Utilisation appropriée de `reactive()`, `eventReactive()`, ``` observeEvent(),``observe() ```~~ ( à detailler )

## Performance

-   [ ] ~~Ressources statiques optimisées (images, scripts, CSS)~~ -
-   [ ] Les gros tableaux/objets sont gérés efficacement (pagination, filtrage local) \~

## Validation des entrées & gestion des erreurs

-   [ ] Validation des inputs (via `validate` / `need`) selon le contexte et cohérence des inputs \~
-   [ ] Messages d’erreurs clairs et adaptés à l’utilisateur \~
-   [ ] ~~Gestion propre des erreurs côté serveur (try/catch, logs, sans fuite d’information sensible)~~

## Sécurité

-   [ ] Utilisation de `req()` pour éviter les erreurs liées aux inputs incomplets +
-   [ ] Pas d’exécution dynamique dangereuse (éviter `eval(parse())` sur des inputs) \~

## Données & I/O ( bathir )

-   [ ] Connexions optimisées si BDD (pooling, timeout, retry)
-   [ ] Gestion correcte des erreurs réseau / API

## Tests Shiny

-   [ ] ~~Tests unitaires présents pour les fonctions métier (hors UI)~~
-   [ ] ~~Tests Shiny via `testServer` ou `{shinytest2}` pour les modules critiques~~
-   [ ] ~~Les snapshots UI sont stables et mis à jour si nécessaire~~
-   [ ] ~~Tous les tests passent et la couverture est acceptable pour le projet~~

## Observabilité & logs

-   [ ] ~~Journalisation des actions importantes~~
-   [ ] ~~Logs structurés (niveau, message, contexte)~~
-   [ ] ~~Suivi des erreurs lors de l’exécution~~
-   [ ] ~~Indicateurs de santé si l’app est déployée (sessions, temps de réponse)~~

## ~~Ressources web (www/) (Interet à définir)~~

-   [ ] ~~Les ressources statiques sont regroupées dans `www/`~~
-   [ ] ~~Les scripts, styles et images sont versionnés et organisés~~
-   [ ] ~~Minification/compression activée si nécessaire~~

## Structure générale du projet

-   [ ] ~~Les fichiers sont organisés dans des répertoires dédiés (R/, data/, tests/, www/, etc.)~~

# Pour un Nouveau projet

## UI/UX & accessibilité

-   [ ] Interface cohérente, lisible et compréhensible
-   [ ] États de chargement et retours visuels durant les traitements (`withProgress`, `shinybusy`)
-   [ ] ~~Utilisation éventuelle d’un thème via ``` {bslib} ( confrontez bslib et bs``4``dash ) ```~~

## Déploiement

-   [ ] Vérifier qu'il y a "devel" par defaut dans le script dev/run_dev.R pour la commande golem::run_dev()
-   [ ] ~~La procédure de déploiement est documentée (Shiny Server, Posit Connect, Docker, etc.)~~
-   [ ] Les configurations sont séparées du code (config files, variables d’env.)

## Structure générale du projet

-   [ ] ~~Le projet contient un README expliquant la structure des dossiers~~
-   [ ] Faire un état des lieux des librairies necessaires pour le projet ( à faire valider par le client/metier )

