<div align="center">

# LinkVault

**Votre catalogue de liens personnel, élégant et hors-ligne.**

[![Statut](https://img.shields.io/badge/statut-fonctionnel-success?style=flat-square)]()
[![Licence](https://img.shields.io/badge/licence-MIT-blue?style=flat-square)]()
[![Navigateur](https://img.shields.io/badge/navigateur-tous-orange?style=flat-square)]()
[![Stockage](https://img.shields.io/badge/stockage-localStorage-9cf?style=flat-square)]()
[![Tailwind](https://img.shields.io/badge/Tailwind_CSS-3.x-38bdf8?style=flat-square&logo=tailwindcss)]()

<img src="https://img.shields.io/badge/0_API-0_serveur-22c55e?style=for-the-badge" alt="Zéro API, Zéro serveur">

<br><br>

<img width="720" alt="LinkVault Preview" src="https://placehold.co/720x400/111111/e8a849?text=LinkVault+Preview">

<br>

*Tout est stocké dans votre navigateur. Aucune donnée ne quitte votre machine.*

</div>

---

## Pourquoi LinkVault ?

On a tous des dizaines de liens éparpillés : des onglets ouverts depuis des semaines, des favoris en désordre, des messages Slack avec des URLs qu'on ne retrouve plus.

LinkVault résout ça avec une interface propre où chaque lien est **catégorisé, recherchable et identifiable en un coup d'oeil** grâce à la détection automatique des plateformes.

---

## Fonctionnalités

### Gestion des liens
- **Ajout / modification / suppression** via un formulaire simple
- **Détection automatique** de plus de 30 plateformes (Facebook, YouTube, TikTok, GitHub, Spotify, Discord, Reddit, Figma, etc.) avec icônes et couleurs officielles
- **Favicon personnalisé** possible pour les sites non détectés
- **Recherche instantanée** par titre, URL ou description

### Organisation
- **Catégories personnalisables** avec icône et couleur au choix
- **Filtrage par catégorie** depuis la sidebar
- **Stats en temps réel** affichant les catégories les plus remplies
- **Vue grille ou liste** selon vos préférences

### Données
- **Stockage 100% local** via `localStorage` — aucune donnée envoyée nulle part
- **Export JSON** pour sauvegarder vos liens sur disque
- **Import JSON** pour restaurer ou fusionner des données
- **12 liens d'exemple** pré-chargés pour voir le résultat immédiatement

### Technique
- **Aucune dépendance serveur** — un seul fichier HTML
- **Aucune API externe** — tout fonctionne hors-ligne après le premier chargement CDN
- **Responsive** — fonctionne sur mobile, tablette et desktop avec sidebar adaptative
- **Accessible** — navigation clavier (Escape pour fermer), aria-labels, respect de `prefers-reduced-motion`
- **PWA** — installable sur mobile et desktop, fonctionne hors-ligne

---

## Installation

### Option 1 — Utiliser directement
Téléchargez `index.html` et ouvrez-le dans votre navigateur.

```bash
# Ou avec curl
curl -O https://votre-url/index.html
open index.html
```

### Option 2 — Héberger en ligne gratuitement

**Netlify Drop** (le plus rapide)
1. Allez sur [app.netlify.com/drop](https://app.netlify.com/drop)
2. Glissez `index.html` et `sw.js` dans la page
3. C'est en ligne.

**GitHub Pages**
1. Créez un repo
2. Poussez `index.html` et `sw.js` à la racine
3. Settings → Pages → Source: main branch
4. Votre site est accessible à `https://votre-pseudo.github.io/nom-du-repo/`

**Surge.sh**
```bash
npm i -g surge
surge index.html sw.js
```

---

## Structure du projet

```
linkvault/
├── index.html      # App complète (HTML + CSS + JS)
├── sw.js           # Service Worker pour le mode hors-ligne (PWA)
└── README.md       # Ce fichier
```

Pas de build, pas de `node_modules`, pas de configuration.

---

## Technologies

| Technologie | Rôle |
|---|---|
| **Tailwind CSS** | Utilitaire CSS via CDN |
| **Font Awesome 6** | Icônes de plateformes et interface |
| **Google Fonts** | Space Grotesk (texte) + Syne (titres) |
| **localStorage** | Persistance des données |
| **Service Worker** | Cache hors-ligne (PWA) |

---

## Détection des plateformes

LinkVault reconnaît automatiquement ces services :

<div align="center">

Facebook · Instagram · X (Twitter) · LinkedIn · TikTok · YouTube · Twitch · Reddit · Discord · Telegram · WhatsApp · Pinterest · Snapchat · Spotify · SoundCloud · Netflix · GitHub · GitLab · Stack Overflow · CodePen · npm · Figma · Dribbble · Behance · Medium · Slack · Notion · Google · Apple · Microsoft · Amazon

</div>

Pour tout autre site, une icône globe générique est affichée. Vous pouvez aussi fournir manuellement une URL de favicon.

---

## Personnalisation

Les couleurs sont définies via des variables CSS en haut du `<style>` :

```css
:root {
    --bg: #080808;           /* Fond principal */
    --bg-raised: #111111;    /* Fond sidebar */
    --bg-card: #151515;      /* Fond des cartes */
    --fg: #f0ece4;           /* Texte principal */
    --accent: #e8a849;       /* Accent doré */
    --danger: #ef4444;       /* Suppressions */
    --success: #22c55e;      /* Confirmations */
    --border: #1e1c1a;       /* Bordures */
}
```

Changez `--accent` pour transformer tout le thème en un clic (`#ef4444` pour du rouge, `#22c55e` pour du vert, etc.).

---

## Hébergement gratuit comparé

| Service | Limite | Custom domaine | SSL |
|---|---|---|---|
| **Netlify** | 100 Go/mois | Oui | Oui |
| **GitHub Pages** | 1 Go repos | Oui | Oui |
| **Surge.sh** | Illimité (usage personnel) | Oui | Oui |
| **Tiiny.host** | 1 fichier, 5 Mo | Non | Oui |
| **Cloudflare Pages** | Illimité | Oui | Oui |

Pour un fichier HTML statique, n'importe lequel suffit largement.

---

## Licence

MIT — faites ce que vous voulez avec.

---

<div align="center">

**Fait avec soin. Aucune donnée collectée. Aucun tracker.**

</div>