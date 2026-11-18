# Programme Été 2027

Application web (PWA) de suivi d'un programme de 30 semaines : musculation à la maison (Smith, poulie, haltères), course et vélo, jusqu'à l'été 2027.

## Fonctionnalités

- **Séance du jour** avec bande de la semaine, stats de régularité et progression du programme.
- **4 séances par semaine** les 4 premières semaines, puis **5**. Quatre phases : Fondations, Hypertrophie, Force & densité, Sèche.
- **Mode séance** : charges conseillées (départ estimé, puis progression automatique de 2,5 kg), saisie des séries, minuteur de repos avec bips, effort ressenti (RPE) en fin de séance.
- **Coach adaptatif** : check du matin (sommeil, courbatures, énergie) et douleurs par zone qui adaptent automatiquement les exercices et le cardio.
- **Course et vélo** : cardio prévu chaque jour et journal des sorties.
- **Nutrition** : cibles par phase et compteur de protéines.
- **Progrès** : poids et trajectoire visée, tests de référence, volume, endurance, records, historique.
- **Bibliothèque** de 31 exercices avec carte des muscles, exécution, erreurs fréquentes et lien vers une démo.
- **Hors ligne** grâce au service worker, et installation sur l'écran d'accueil.

## Synchronisation (optionnelle)

Les données sont enregistrées sur l'appareil. Pour les retrouver sur plusieurs appareils, l'app se connecte à un projet Supabase (même principe que Climbing-Coach) :

1. Dans Supabase › SQL Editor, lancer le script affiché dans l'app (Progrès › Synchronisation). Il crée la table `ete_state` avec Row Level Security : chaque compte ne voit que sa ligne.
2. Dans l'app, renseigner l'URL du projet et la clé publique (anon), puis se connecter.

Sur `anakfgr.github.io`, la configuration de Climbing-Coach est reprise automatiquement.

## Fichiers

- `index.html` : toute l'application (HTML, CSS, JS).
- `sw.js` : cache hors ligne.
- `manifest.webmanifest` et icônes : installation sur l'écran d'accueil.

Cette application ne remplace pas l'avis d'un professionnel de santé.
