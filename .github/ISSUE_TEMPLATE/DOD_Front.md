---
name: "DOD Front"
about: "Checklist Definition of Done pour le front"
labels: []
assignees: []
---

# DoD – Développeurs HTML / CSS / JavaScript (Frontend)

## Fonctionnel

-   [ ] L’UI/UX respecte les maquettes (Figma) le cas écheant\~
-   [ ] ~~Le site est responsive (mobile / tablette / desktop)~~
-   [ ] ~~Le rendu est cohérent entre les navigateurs majeurs (Chrome, Firefox, Edge, Safari)~~

## Qualité du code

-   [ ] ~~Le code HTML est valide (W3C validator)~~ Approfondir le sujet - A demander à l'ATIH
-   [ ] ~~Le CSS suit une méthodologie (BEM, ITCSS, Tailwind conventions…)~~ A regarder en interne
-   [ ] La convention de nommage ATOL est respectée +
-   [ ] Les docstrings sont à jour -
-   [ ] Le JS est découpé en modules/fonctions cohérentes ~~( limite de lignes 150 ? )~~
-   [ ] Aucun code nouvellement créé est dupliqué (DRY) \~
-   [ ] Aucun console.log, code mort ou variable globale non maîtrisée +

## Tests

-   [ ] ~~Tests unitaires créés ou mis à jour (Jest, Vitest…)~~
-   [ ] ~~Tests E2E mis à jour si nécessaire (Cypress, Playwright)~~
-   [ ] ~~Tous les tests passent~~

## Sécurité

-   [ ] ~~Aucun contenu dangereux injecté (XSS, innerHTML non contrôlé) cross forgery token~~
-   [ ] Les entrées utilisateurs sont validées côté client -

## Performances

-   [ ] ~~Les images sont optimisées (WebP, compression)~~
-   [ ] ~~Le bundling/minification fonctionne (Vite, Webpack, …)~~
-   [ ] Aucun blocage du main thread (éviter longues boucles, DOM lourd) \~

## Intégration & documentation

-   [ ] Le ~~README~~ wiki du projet est mis à jour si la fonctionnalité le nécessite
-   [ ] La Pull Request redirige vers l'issue concernée

## Git & collaboration

-   [ ] ~~Les commits respectent la convention de nommage interne (ex : Conventional Commits)~~
-   [ ] ~~Les fichiers générés (dist/, .cache, node_modules/ ou fichiers temporaires) ne sont pas ajoutés à la PR~~
-   [ ] J'ai pull la branche main / dev et je l'ai mergé dans ma branche avant de la push sur le repo distant - A debattre
-   [ ] La branche est à jour avec main / dev avant merge sur le repo distant- A debattre

## Structure générale du projet

-   [ ] Une arborescence de projet clair contenant uniquement des fichiers nécessaires, particulierment en fin de projet (pas de fichiers temporaires, pas de data locales non versionnées).
-   [ ] Le projet contient un ~~README~~ wiki expliquant la structure des dossiers.

