# Richard · Endurance 2027

Application statique : séances détaillées Half et ultra, suivi local, renforcement lundi/mercredi/vendredi, exports calendrier et vélo. Aucune dépendance de compilation ou police distante.

## Tester

Avec Node.js 22 ou supérieur :

```sh
node --check dist/app.js
node --test tests/plan.test.cjs
```

Pour voir l’application localement : `python3 -m http.server 8000 --directory dist`, puis ouvrir http://localhost:8000.

## Publier sur GitHub Pages

1. Créer un dépôt nommé par exemple `endurance-2027`, sans modifier le dépôt de l’application trains.
2. Ajouter à la racine les dossiers `dist`, `tests` et `.github` de cette archive ainsi que ce fichier README. Le dossier `.github` peut être masqué dans le Finder : utiliser Cmd+Maj+point pour l’afficher. En ligne de commande, effectuer un commit puis un push sur `main`.
3. Dans GitHub : Settings → Pages → Build and deployment → Source : GitHub Actions.
4. Dans Actions, lancer « Test and deploy GitHub Pages » via Run workflow si aucun lancement n’est en cours.
5. Le lien du déploiement réussi apparaît dans Actions et Settings → Pages. Les futurs push sur `main` testent puis republient automatiquement le site.

Les liens CSS/JavaScript sont relatifs : le site fonctionne aussi dans un sous-chemin de dépôt. `dist/.nojekyll` est fourni. L’archive n’inclut aucune configuration Sites ou clé d’accès.

## Données et limites

Le code contient les objectifs et repères sportifs utilisés comme valeurs initiales. GitHub Pages est généralement public : ces valeurs seront lisibles par les visiteurs. Le journal personnel, les notes et les déplacements restent dans le navigateur et ne sont jamais envoyés au dépôt. Les données du site ChatGPT ne se transfèrent pas automatiquement sur le domaine GitHub : exporter la sauvegarde depuis l’ancien site, puis la restaurer dans Réglages du nouveau site.

La connexion Garmin n’est pas automatisée. Les séances course sont à reproduire dans Garmin Connect. Les exports `.zwo` sont réservés aux plateformes compatibles et nécessitent la même FTP que l’application.

Renforcement réduit les semaines allégées, suspendu pendant l’affûtage et la récupération. Premier volume : 8 h 30 ; pic du plan par défaut : 15 h hors épreuves. Les notes et séances réalisées sont conservées lors des modifications de FTP. Un déplacement manuel peut augmenter le volume d’une semaine : il ne rééquilibre pas le plan.

Le Half est réglé au 6 juin 2027 selon le programme officiel. Le départ ultra du 15 septembre est provisoire ; le lieu et le règlement de la Race Across restent à confirmer.

## Bloc PMA hiver

Du 1 décembre 2026 au 26 janvier 2027 : sept séances PMA de 60 min le mardi, en remplacement du tempo, et deux mardis faciles (22 décembre, 19 janvier). Départ 2 × 6 × 30 s/30 s, progression vers 2 × 10 répétitions, puis 4 × 2, 5 × 2, 4 × 3 et 5 × 3 min. Les puissances sont des cibles provisoires depuis la FTP, pas une mesure de PMA. Le jeudi reste facile sur home trainer ; le dimanche reste en endurance dehors. Toutes les séances vélo de semaine sont marquées Home trainer. Les blocs ultra exceptionnels du samedi sont conservés hors hiver.

Chaque séance PMA possède échauffement, récupérations, retour au calme, couleurs d’intensité et export .zwo. Huit tests vérifient le plan et les exports, dont les durées des intervalles de 30 secondes.
