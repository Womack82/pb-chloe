# Règles du projet « P&B Chloé »

## Le projet

- **À compléter** : ce que fait l'app, pour qui (Chloé, papa, maman ?),
  sur quel appareil elle sert surtout (iPhone ?).
- Petite web app installable (PWA), interface en français, au tutoiement.
- Publication prévue sur GitHub Pages (compte Womack82, adresse à fixer
  quand le dépôt sera créé).
- Les améliorations à faire et déjà faites sont suivies dans `TODO.md`.

## Façon de travailler

- L'utilisateur débute en programmation : explique brièvement ce que tu fais
  et pourquoi, avec des mots simples.
- Avant de coder, signale tout point qui pose problème (limite technique,
  risque, effet secondaire) et attends sa réponse.
- Fais un commit Git par étape, avec un message clair qui dit ce qui change.
- Après chaque commit, fais `git push` automatiquement, sans demander
  l'accord de l'utilisateur. Le site GitHub Pages se met alors à jour tout seul.
- Ne mets jamais une clé API dans un fichier suivi par Git sans le dire
  clairement à l'utilisateur.

## Version et cache

- À chaque modification, change la version du cache (`NOM_CACHE`) dans
  `service-worker.js`. Sinon, le téléphone continue d'utiliser l'ancienne copie.
- Change en même temps `VERSION` en haut de `app.js` : c'est le numéro affiché
  dans les Réglages, et il doit rester identique à celui du cache.
- Numérotation : première version **v1.0**. Chaque changement, quel qu'il
  soit (nouvelle demande ou retouche), ajoute 1 au second numéro :
  v1.0 → v1.1 → v1.2…
- D'autres apps sont publiées sur le même site (womack82.github.io) : tous
  les noms techniques (mémoire localStorage, cache, sauvegardes) commencent
  par « pb-chloe », et le nettoyage du cache n'efface que les caches
  « pb-chloe-… ».

## Apparence

- Mobile d'abord : boutons et zones à toucher d'au moins 44 px, texte lisible
  sans zoomer.
- Palette de couleurs : **à définir**.
- Animations légères, de 150 à 280 ms, et désactivées quand l'option
  « réduire les animations » est activée sur l'appareil
  (`@media (prefers-reduced-motion: reduce)`).
- Quand l'utilisateur demande un changement d'apparence, ne modifie que
  l'apparence (CSS, présentation) : ne touche à aucune fonction.
