# Innov Innovation

Site vitrine statique (page unique) pour Innov Innovation — startup/agence tech basée à Kinshasa.

## Description

Ce dépôt contient une page HTML autonome (index.html) et un dossier d'images (img/) pour présenter les services, le portfolio, l'équipe et les informations de contact d'Innov Innovation. Le site est conçu pour être déployé comme site statique (GitHub Pages, Netlify, Vercel, ou tout hébergement de fichiers statiques).

## Points forts

- Page unique (single-page) responsive avec sections : Accueil, Services, À propos, Portfolio, Témoignages, Contact, Équipe, Footer.
- Utilise Tailwind CSS et Font Awesome via CDN pour le style et les icônes.
- Animations et interactions légères implémentées en JavaScript côté client (menu mobile, animations au scroll, bouton "back to top").
- Formulaire de contact géré côté client (alert de confirmation). Pour recevoir réellement les messages, il faut connecter le formulaire à un service ou back-end.

## Stack

- Langage : HTML
- Librairies (CDN) : Tailwind CSS, Font Awesome
- Assets : images locales (dossier `img/`) et images externes (Unsplash)

## Arborescence importante

```
index.html        # Page principale (HTML + CSS inline + JS inline)
README.md         # Ce fichier
img/              # Images et logos utilisés par le site
```

## Installation / Aperçu local

Le site ne nécessite pas de compilation — il fonctionne en ouvrant `index.html` dans un navigateur. Pour un aperçu via un serveur local (recommandé) :

- Avec Python 3 :

```bash
python -m http.server 8000
# Ouvrir http://localhost:8000
```

- Avec Node (http-server) :

```bash
npx http-server -p 8000
# Ouvrir http://localhost:8000
```

- Avec VS Code : utilisez l'extension Live Server et ouvrez `index.html`.

## Déploiement

Vous pouvez déployer le site facilement sur n'importe quel hébergement statique.

- GitHub Pages
  - Dans les paramètres du dépôt, activez GitHub Pages depuis la branche `main` (root) pour servir `index.html`.

- Netlify
  - Drag & drop du dossier racine sur app.netlify.com ou connectez le repo GitHub et configurez le build comme "Static Site" (pas de build command nécessaire).

- Vercel
  - Importez le repo et déployez comme projet statique. Aucune commande de build requise.

## Rendre le formulaire de contact fonctionnel

Actuellement, le formulaire affiche une alerte côté client. Options pour recevoir les messages :

1. Utiliser un service de formulaire (sans back-end) :
   - Formspree, Getform, Netlify Forms
   - Avantage : configuration rapide, pas de serveur

2. Ajouter un petit back-end (ex. Node.js/Express) qui reçoit POST `/contact` et envoie un email (Nodemailer) ou stocke le message.

3. Intégrer une fonction serverless (Netlify Functions, Vercel Serverless) pour traiter les envois.

Si vous voulez, je peux ajouter un exemple minimal pour l'une de ces options.

## Personnalisation

- Couleurs et styles : configurés dans la balise `<script>` Tailwind et dans les styles inline du fichier `index.html`.
- Images : remplacez celles du dossier `img/` par vos visuels (respectez les noms ou mettez à jour les références dans `index.html`).
- Texte : modifiez directement les sections dans `index.html` (sections identifiées par des ids : `#accueil`, `#services`, `#apropos`, `#portfolio`, `#contact`, `#equipe`).

## Contribution

Toute contribution est bienvenue : corrections de texte, nouvelles images, optimisation des performances ou ajout d'un back-end pour le formulaire.

- Forkez le dépôt
- Créez une branche feature/nom
- Proposez une pull request avec une description claire des changements

## Licence

Ajoutez une licence si vous souhaitez en définir une (ex. MIT). Si vous voulez, je peux ajouter un fichier `LICENSE` avec la licence MIT.

## Crédits & Contacts

- Auteur / Contact principal : Ndombe Elie (présent dans la page) — innovinnovationtech@gmail.com
- Images : certaines images proviennent d'Unsplash (liens inclus dans `index.html`).

---

Si tu veux, je peux :
- 1) mettre à jour automatiquement `README.md` dans le dépôt (je viens de préparer ce contenu),
- 2) créer un guide de contribution plus détaillé, ou
- 3) ajouter un exemple d'implémentation du formulaire (Formspree ou un petit back-end Node).

Dis-moi quelle option tu veux que j'exécute ensuite.