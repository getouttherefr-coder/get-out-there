# GET OUT THERE — V1.3 : vitrine + réservation + FAQ partageable

## Changements

- `index.html` : page vitrine sans calendrier ni bloc « Organiser votre séjour » ; garde présentation, concept, services, photos et avis en dernier, avec appels à réserver.
- `reserver.html` (nouveau) : calendrier, simulateur, formulaire, CGV et paiement Stripe. Le script de réservation provient sans modification de `index.html` V1.2.
- `faq.html` : toutes les questions et réponses, chacune avec un identifiant stable et un lien direct ; chargement d'un lien `#...` ouvre automatiquement sa réponse.
- Les autres pages pratiques et juridiques sont conservées, accessibles via la FAQ et leurs URL historiques, mais le menu simplifié devient : Le lodge / Réserver / FAQ / Aux alentours.

## Liens à communiquer
- https://www.getoutthere.fr/faq.html#comment-se-rendre-au-lodge
- https://www.getoutthere.fr/faq.html#comment-acceder-au-lodge
- https://www.getoutthere.fr/faq.html#horaires-arrivee-depart
- https://www.getoutthere.fr/faq.html#linge-fourni
- https://www.getoutthere.fr/faq.html#chiens-autorises
- https://www.getoutthere.fr/faq.html#peche-autorisee
- https://www.getoutthere.fr/faq.html#services-additionnels
- https://www.getoutthere.fr/reserver.html

## Installation sur GitHub Pages (main)
1. Sauvegarder le commit actuel en relevant son hash.
2. Sur la branche `main` à la racine du dépôt `getouttherefr-coder/get-out-there`, importer les 11 HTML du ZIP en remplaçant ceux portant le même nom. **Ne pas supprimer `admin-gestion.html` ni le répertoire `images`.**
3. Commit, puis attendre que GitHub Actions indique un déploiement terminé.
4. Tester `/`, `/reserver.html`, `/faq.html#comment-acceder-au-lodge`, `/alentours.html`, puis sur Chrome mobile.
5. Dans Réserver, charger le calendrier, sélectionner un séjour libre, contrôler le devis serveur, remplir le formulaire et aller jusqu'à l'écran Stripe. Ne pas payer un second test sans intention explicite.
6. Vérifier le parcours d'annulation Stripe (retour `?payment=cancel`) qui doit montrer l'avis sur `/reserver.html`.
7. Vérifier les boutons de la console admin ; elle et le Worker ne sont pas modifiés.

## Points à valider
- **Chiens et pêche** : aucune règle explicite confirmée ; FAQ conseille de demander l'accord de GET OUT THERE. Ne pas présenter comme autorisé sans validation.
- **Calendrier mobile** : la séparation des pages ne garantit pas la correction d'une éventuelle panne réseau/Google Apps Script. Contrôler sur le téléphone réel.
- **Paiement Stripe** : le code client est identique, mais les URL de retour côté Worker peuvent encore viser `/` (à vérifier sans changer le Worker). Le retour annulé depuis `/` est redirigé vers `/reserver.html`.
- **Avis** : vérifier la permission de publication et l'exactitude des citations.
- **Mentions légales** : médiateur encore à renseigner.
- **Photographie IMG_20261026_112313_957** : vérifier l'asset image réel, non joint dans ce package.
