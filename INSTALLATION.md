# GET OUT THERE — Correctif V1.3.1

Trois corrections :
1. La page `reserver.html` est incluse (à ajouter impérativement à la racine du dépôt, sur la branche `main`).
2. La section « Un lodge flottant, autonome et attentif à la nature » est désormais immédiatement après « La vie sur l’eau, tout simplement ».
3. Contraste des liens de pied de page corrigé sur l'ensemble des pages.

## Installation rapide
1. Décompresser l'archive.
2. Sur GitHub > dépôt `get-out-there` > branche `main`, mettre les fichiers `.html` **à la racine**, à côté de `index.html` et `admin-gestion.html`. Ne pas uploader le dossier parent lui-même.
3. Écraser les fichiers HTML homonymes. En particulier vérifier que **`reserver.html` existe à la racine**. Ne pas écraser `admin-gestion.html` ni le dossier `images`.
4. Cliquer sur **Commit changes**, puis attendre la réussite de GitHub Actions.
5. Tester `https://www.getoutthere.fr/reserver.html` directement, puis le bouton « Réserver » de la page principale. Tester aussi le calendrier sur Chrome mobile.

## Périmètre
Aucun changement au code métier de réservation, API Stripe, Cloudflare Worker, D1 ou Google Apps Script. Les erreurs de chargement du calendrier sur Chrome mobile ne sont **pas** garanties corrigées par ce patch de présentation.
