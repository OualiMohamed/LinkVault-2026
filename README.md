LinkVault

Votre catalogue de liens personnel, élégant et hors-ligne.

StatutLicenceNavigateurStockageTailwind
Zéro API, Zéro serveur



LinkVault Preview

Tout est stocké dans votre navigateur. Aucune donnée ne quitte votre machine.
Pourquoi LinkVault ?

On a tous des dizaines de liens éparpillés : des onglets ouverts depuis des semaines, des favoris en désordre, des messages Slack avec des URLs qu'on ne retrouve plus.

LinkVault résout ça avec une interface propre où chaque lien est catégorisé, recherchable et identifiable en un coup d'oeil grâce à la détection automatique des plateformes.
Fonctionnalités
Gestion des liens

    Ajout / modification / suppression via un formulaire simple
    Détection automatique de plus de 30 plateformes (Facebook, YouTube, TikTok, GitHub, Spotify, Discord, Reddit, Figma, etc.) avec icônes et couleurs officielles
    Favicon personnalisé possible pour les sites non détectés
    Recherche instantanée par titre, URL ou description

Organisation

    Catégories personnalisables avec icône et couleur au choix
    Filtrage par catégorie depuis la sidebar
    Stats en temps réel affichant les catégories les plus remplies
    Vue grille ou liste selon vos préférences

Données

    Stockage 100% local via localStorage — aucune donnée envoyée nulle part
    Export JSON pour sauvegarder vos liens sur disque
    Import JSON pour restaurer ou fusionner des données
    12 liens d'exemple pré-chargés pour voir le résultat immédiatement

Technique

    Aucune dépendance serveur — un seul fichier HTML
    Aucune API externe — tout fonctionne hors-ligne après le premier chargement CDN
    Responsive — fonctionne sur mobile, tablette et desktop avec sidebar adaptative
    Accessible — navigation clavier (Escape pour fermer), aria-labels, respect de prefers-reduced-motion

Installation
Option 1 — Utiliser directement

Téléchargez index.html et ouvrez-le dans votre navigateur.

# Ou avec curlcurl -O https://votre-url/index.htmlopen index.html

 
Option 2 — Héberger en ligne gratuitement 

Netlify Drop (le plus rapide) 

    Allez sur app.netlify.com/drop  
    Glissez index.html dans la page 
    C'est en ligne. 

GitHub Pages 

    Créez un repo 
    Poussez index.html à la racine 
    Settings → Pages → Source: main branch 
    Votre site est accessible à https://votre-pseudo.github.io/nom-du-repo/ 

Surge.sh 
bash
 
  
 
npm i -g surge
surge index.html
 
 
 
Structure du projet 
text
 
  
 
linkvault/
└── index.html          # Tout est ici
    ├── <style>         # CSS personnalisé (variables, layout, composants)
    ├── <body>          # HTML sémantique (sidebar, grille, modals, toasts)
    └── <script>        # Logique JS (CRUD, stockage, détection, rendu)
 
 
 

Pas de build, pas de node_modules, pas de configuration. 
Technologies 
Technologie
 
	
Rôle
 
 
Tailwind CSS	Utilitaire CSS via CDN 
Font Awesome 6	Icônes de plateformes et interface 
Google Fonts	Space Grotesk (texte) + Syne (titres) 
localStorage	Persistance des données 
   
Détection des plateformes 

LinkVault reconnaît automatiquement ces services : 


Facebook · Instagram · X (Twitter) · LinkedIn · TikTok · YouTube · Twitch · Reddit · Discord · Telegram · WhatsApp · Pinterest · Snapchat · Spotify · SoundCloud · Netflix · GitHub · GitLab · Stack Overflow · CodePen · npm · Figma · Dribbble · Behance · Medium · Slack · Notion · Google · Apple · Microsoft · Amazon 


Pour tout autre site, une icône globe générique est affichée. Vous pouvez aussi fournir manuellement une URL de favicon. 
Personnalisation 

Les couleurs sont définies via des variables CSS en haut du <style> : 
css
 
  
 
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
 
 
 

Changez --accent pour transformer tout le thème en un clic (#ef4444 pour du rouge, #22c55e pour du vert, etc.). 
Hébergement gratuit comparé 
Service
 
	
Limite
 
	
Custom domaine
 
	
SSL
 
 
Netlify	100 Go/mois	Oui	Oui 
GitHub Pages	1 Go repos	Oui	Oui 
Surge.sh	Illimité (usage personnel)	Oui	Oui 
Tiiny.host	1 fichier, 5 Mo	Non	Oui 
Cloudflare Pages	Illimité	Oui	Oui 
   

Pour un fichier HTML statique, n'importe lequel suffit largement. 
Licence 

MIT — faites ce que vous voulez avec. 


Fait avec soin. Aucune donnée collectée. Aucun tracker. 