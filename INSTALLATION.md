# GET OUT THERE — V1.2 multipages (site vitrine)

## Installation directe sur `main`
1. Télécharger et décompresser l'archive.
2. Ouvrir https://github.com/getouttherefr-coder/get-out-there, branche **main**.
3. Importer les **10 fichiers HTML à la racine**, en remplaçant `index.html` et les 3 fichiers juridiques existants. Conserver leurs noms exacts. Aucun sous-dossier supplémentaire.
4. **Ne pas modifier `admin-gestion.html`, le Worker Cloudflare, D1, Stripe, Google Apps Script, ni le dossier `images/`**. Les photos du site sont réutilisées par leurs chemins existants.
5. Attendre la coche verte du déploiement GitHub Pages dans **Actions**.
6. Ouvrir `https://www.getoutthere.fr/`, puis cliquer sur chaque onglet, sur ordinateur et mobile. Vérifier que les 7 pages sont accessibles depuis le menu.
7. Tester `/index.html#reservation` et le chargement du calendrier sur Chrome mobile. **Ne pas réaliser de paiement de test sans procédure prévue.** Le code fonctionnel de réservation/Stripe est inchangé.
8. Tester `/acces.html`, `/arrivee-depart.html`, `/equipements.html`, `/faq.html`, `/alentours.html`, `/reglement-interieur.html` et les liens du pied de page.

## Pages et URLs pour messages automatiques
- Arrivée / itinéraire : `https://www.getoutthere.fr/acces.html`
- Horaires et organisation : `https://www.getoutthere.fr/arrivee-depart.html`
- Équipements : `https://www.getoutthere.fr/equipements.html`
- Règlement intérieur : `https://www.getoutthere.fr/reglement-interieur.html`
- FAQ : `https://www.getoutthere.fr/faq.html`
- Autour du lodge : `https://www.getoutthere.fr/alentours.html`
- Réservation : `https://www.getoutthere.fr/#reservation`

## Principes
- Page d'accueil : lodge, concept et images réelles du domaine, prestations, photos, moteur de réservation, puis avis voyageurs tout en bas.
- Rubriques d'assistance isolées sur des pages avec URLs pérennes et navigation horizontale défilable sur téléphone.
- Données de sécurité inchangées : ne pas afficher publiquement les coordonnées personnelles d'accueil de Maud.
- Autonomie et écologie : descriptions factuelles, sans certification environnementale non établie. Les trois visuels actuels sont des **photos réelles du lodge/étang**, réutilisées temporairement. Remplaçables par des fichiers `images/` au même emplacement ou en modifiant leur chemin HTML.
- La photo `IMG_20261026_112313_957.jpg` (579×1032 pixels) n'est pas appelée dans la page d'accueil fournie. Si elle s'affiche mal sur le site actuel, vérifier quelle page la référence et éviter un affichage pleine largeur non adapté à sa faible définition.

## Contrôles / limites
- Vérifier physiquement la publication : aucune validation de déploiement LIVE n'est possible à partir de cette archive seule.
- Le chemin `images/poele.jpg` qui déclenchait une erreur 404 a été remplacé dans la vitrine par `images/6C8A7677.jpg`, déjà présent sur le dépôt.
- Le calendrier conserve l'intégration du site V1.1 révisé : le souci Chrome mobile n'est pas considéré comme résolu sans test.
- Les pages juridiques réutilisent la version précédente, **sans médiateur identifié et avec des points RGPD/contrat restant à finaliser**. Les pages publiques ne deviennent pas automatiquement conformes du fait de cette refonte.
- Les images de certains lieux alentour sont chargées depuis des sites externes ; leurs URLs peuvent changer. En cas de 404, remplacer par des images locales disposant des autorisations de réutilisation.
- Aucun tarif, paramètre Stripe, route API ou statut de réservation n'est modifié ici.
