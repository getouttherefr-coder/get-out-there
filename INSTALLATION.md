# GET OUT THERE — V1.4.2 consolidée

Ce paquet **remplace** les paquets V1.4 et V1.4.1. Il contient l’ensemble des 12 pages HTML et intègre les règles de séjour corrigées.

## Navigation commune vérifiée
1. Le concept → index.html
2. Description d’un séjour → sejour.html
3. Les alentours → alentours.html
4. Réserver → reserver.html
5. FAQ → faq.html

Les pages `acces.html`, `arrivee-depart.html`, `equipements.html`, `reglement-interieur.html` restent accessibles par des liens contextuels / FAQ.

## Installation
1. Décompresser le ZIP.
2. Aller sur GitHub, dépôt getouttherefr-coder/get-out-there, branche `main`.
3. Envoyer **les 12 fichiers .html à la racine**, en remplaçant ceux de même nom. NE PAS envoyer le dossier parent.
4. Ne pas modifier `admin-gestion.html`, `images/`, Cloudflare, Stripe ou Apps Script.
5. Commit changes et vérifier le déploiement dans GitHub Actions.
6. Vérifier `index.html`, `sejour.html`, `alentours.html`, `reserver.html`, `faq.html` sur ordinateur ET téléphone.
7. Vérifier le chargement des disponibilités, le devis et le checkout jusqu’à la page Stripe SANS procéder à un paiement non voulu.
8. Le plan du site `plandusite.png` doit être ajouté à la racine si souhaité.

## Points à finaliser
- Médiation de la consommation obligatoire mais non encore renseignée.
- Vérifier en réel le calendrier sur Chrome mobile et le retour Stripe après paiement.
- Ne pas afficher le séjour comme accessible aux chiens ; les chiens d'assistance peuvent relever d'obligations particulières.
- Les conditions exceptionnelles ne sont pas détaillées commercialement, mais les droits légaux restent applicables.
- Les fichiers n'ont pas été testés sur la version déployée en ligne.
