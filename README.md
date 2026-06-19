# Clavie Events — Site web

Site vitrine (une seule page) pour **Clavie Events**, organisatrice d'événements sur mesure
en **Hérault, Gard & Occitanie** — mariages, baptêmes, baby showers, anniversaires,
gender reveal et événements privés. Basée à **Boisseron (34)**.

Site **100 % statique** (HTML/CSS/JS), prêt à héberger sur **GitHub Pages**.

---

## 📁 Contenu

```
.
├── index.html          # Le site complet (structure + styles + scripts)
├── assets/
│   ├── logo.svg        # Logo Clavie Events (vectoriel, réutilisable)
│   └── favicon.svg     # Icône d'onglet
└── README.md
```

> Le logo a été **recréé en SVG** d'après la carte Instagram (monogramme CE, couronne
> botanique, « CLAVIE EVENTS », script « Créatrice d'émotions »).

---

## ✅ Ce qui est déjà branché (vraies infos)

- **Téléphone / WhatsApp** : 06 23 28 69 39 (liens `tel:` et `wa.me/33623286939` actifs).
- **Zone** : Boisseron (34) — Hérault, Gard & Occitanie.
- **Instagram** : lien vers https://www.instagram.com/clavieevents (affiché « @clavie.events »).
- **Facebook** : https://www.facebook.com/share/18KqxPGpEL/
- **Domaine prévu** : clavie-events.fr (déjà mis dans les balises `og:` / `canonical`).
- **6 prestations**, **6 types d'événements** et le **parcours** repris de tes visuels.

## ✏️ À compléter / vérifier

### 1. Email
Le contact email est **younes.nait.b@gmail.com** (temporaire). Quand Clavie a un email pro,
fais un rechercher/remplacer dans `index.html`.

### 2. Pseudo Instagram
Tes visuels affichent **@clavie.events** mais l'URL fournie est `instagram.com/clavieevents`
(sans point). Le lien pointe vers l'URL vérifiée ; si le vrai compte est bien `clavie.events`
(avec point), remplace l'URL dans `index.html` (3 occurrences) + le README.

### 3. Formulaire de contact (Formspree)
Le formulaire marche **sans configuration** : tant que Formspree n'est pas réglé, l'envoi
ouvre l'application mail du visiteur (repli `mailto`).
Pour recevoir les demandes directement :
1. Compte gratuit sur [formspree.io](https://formspree.io) (50 envois/mois gratuits).
2. Crée un formulaire → copie son ID (ex. `xrgvabcd`).
3. Dans `index.html`, remplace `VOTRE_ID_FORMSPREE` :
   ```html
   <form id="contactForm" action="https://formspree.io/f/xrgvabcd" method="POST">
   ```
4. Valide l'email de confirmation Formspree au premier envoi. ✅

### 4. Galerie photo
**3 photos de baptême sont déjà intégrées** (Baptême, Cérémonie, Bouquet & fleurs) dans `assets/gallery/`.
Les autres cases (Mariage, Décoration de table, Anniversaire, Baby shower, Lieu de réception) sont des
placeholders en attendant d'autres photos.

Pour **ajouter** une photo à une case : place l'image dans `assets/gallery/`, puis sur la case voulue
(section `id="galerie"`) ajoute `data-img` et retire le `style="--c1…"` :
`<button class="g-item" data-cat="Mariage" data-img="assets/gallery/mariage.jpg"></button>`
(ajoute la classe `tall` pour une photo portrait qui occupe 2 rangées).

Pour **supprimer** une case vide : retire sa ligne `<button …></button>`.
> Photos ~1200–1500 px, `.jpg`/`.webp` compressé pour un site rapide.

### 5. Photo de Clavie (À propos)
La section « Mon parcours » affiche un médaillon « CE ». Pour mettre le vrai portrait
(celui de la carte « Mon parcours, ma passion »), dépose-le dans `assets/` et remplace
le bloc `<div class="ph">…</div>` par `<img src="assets/portrait.jpg" alt="Clavie">`.

---

## 🚀 Mise en ligne (GitHub Pages)

1. Crée un dépôt (ex. `clavie-events`) et dépose `index.html`, le dossier `assets/`, `README.md`.
   ```bash
   git init
   git add .
   git commit -m "Site Clavie Events"
   git branch -M main
   git remote add origin https://github.com/TON_PSEUDO/clavie-events.git
   git push -u origin main
   ```
2. **Settings → Pages** → Source : *Deploy from a branch* → branche **main** / dossier **/(root)** → **Save**.
3. Le site sera dispo sur `https://TON_PSEUDO.github.io/clavie-events/` (~1 min).
4. Domaine perso : Settings → Pages → *Custom domain* → `clavie-events.fr`, puis configure les DNS.

---

## 🎨 Charte graphique

| Élément          | Valeur |
|------------------|--------|
| Ivoire (fond)    | `#f6f0e7` |
| Crème            | `#efe7da` |
| Cuivre (accent)  | `#a9784f` |
| Cuivre foncé     | `#8a5d36` |
| Or clair         | `#c8a275` |
| Anthracite       | `#2a2521` |

**Polices** (Google Fonts) : Cinzel, Cormorant Garamond, Great Vibes, Jost.

---

*Aperçu : ouvre simplement `index.html` dans un navigateur.*
