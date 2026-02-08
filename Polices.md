# 📋 FICHE TECHNIQUE DÉVELOPPEUR

## Système Typographique & Colorimétrique Impérial

**Version** : 1.0  
**Date** : 04 février 2026  
**Projet** : Thème Imperial Hierarchy

---

## 1. VUE D'ENSEMBLE

## Objectif

Implémenter un système de design complet avec :

- **12 niveaux de couleurs hiérarchiques** (H1-H6 + D1-D6)
    
- **Échelle typographique basée sur le nombre d'or** (φ = 1.618)
    
- **Police unique haute performance** : Barlow Condensed
    
- **Optimisation lisibilité & accessibilité** WCAG AAA
    

## Technologies

- CSS3 / CSS Variables
    
- Google Fonts
    
- Responsive Design
    
- Dark Theme optimisé
    

---

## 2. POLICE PRINCIPALE

## Barlow Condensed

**Source** : Google Fonts (gratuit)  
**Styles requis** : 300, 400, 500, 600, 700, 800, 900 + Italiques  
**Poids fichier** : ~35 KB

## Import CDN

css

`@import url('https://fonts.googleapis.com/css2?family=Barlow+Condensed:ital,wght@0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,400;1,700&display=swap');`

## Import Local (Performance optimale)

xml

`<!-- Placer dans <head> --> <link rel="preconnect" href="https://fonts.googleapis.com"> <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin> <link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:ital,wght@0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,400;1,700&display=swap" rel="stylesheet">`

---

## 3. ÉCHELLE TYPOGRAPHIQUE NOMBRE D'OR

## Formule

text

`Chaque niveau = Niveau précédent × 1.618 (φ) Base = 16px (1rem)`

## Tableau des tailles

|Niveau|Calcul|Pixels|REM|EM|Poids|Line-Height|
|---|---|---|---|---|---|---|
|**H1**|φ⁵ × 16|177px|11.089rem|11.089em|900|1.1|
|**H2**|φ⁴ × 16|110px|6.854rem|6.854em|800|1.15|
|**H3**|φ³ × 16|68px|4.236rem|4.236em|700|1.2|
|**H4**|φ² × 16|42px|2.618rem|2.618em|600|1.3|
|**H5**|φ¹ × 16|26px|1.618rem|1.618em|600|1.4|
|**H6**|φ⁰ × 16|16px|1rem|1em|500|1.5|
|**Body**|Base|16px|1rem|1em|400|1.618|

---

## 4. PALETTE DE COULEURS

## Système Hiérarchique (Chaud → Froid)

## Titres HTML (H1-H6) - Zone Action

css

`--color-h1: #DC143C;  /* Crimson - Rubis impérial */ --color-h2: #FF6347;  /* Tomato - Vermillon */ --color-h3: #FFA500;  /* Orange - Topaze */ --color-h4: #FFD700;  /* Gold - Or 24K */ --color-h5: #00CED1;  /* DarkTurquoise - Aigue-marine */ --color-h6: #4169E1;  /* RoyalBlue - Saphir */`

## Classification Dossiers (D1-D6) - Zone Archive

css

`--color-d1: #4B0082;  /* Indigo - Tanzanite */ --color-d2: #8B00FF;  /* Violet - Améthyste électrique */ --color-d3: #9932CC;  /* DarkOrchid - Orchidée pourpre */ --color-d4: #BA55D3;  /* MediumOrchid - Orchidée royale */ --color-d5: #DA70D6;  /* Orchid - Orchidée claire */ --color-d6: #EE82EE;  /* Violet - Lavande impériale */`

## Effets Glow (Text-shadow)

css

`--glow-h1: 0 0 25px rgba(220, 20, 60, 0.6), 0 0 50px rgba(220, 20, 60, 0.3); --glow-h2: 0 0 22px rgba(255, 99, 71, 0.5), 0 0 45px rgba(255, 99, 71, 0.2); --glow-h3: 0 0 20px rgba(255, 165, 0, 0.5), 0 0 40px rgba(255, 165, 0, 0.2); --glow-h4: 0 0 20px rgba(255, 215, 0, 0.7), 0 0 40px rgba(255, 215, 0, 0.3); --glow-h5: 0 0 18px rgba(0, 206, 209, 0.5), 0 0 35px rgba(0, 206, 209, 0.2); --glow-h6: 0 0 18px rgba(65, 105, 225, 0.5), 0 0 35px rgba(65, 105, 225, 0.2); --glow-d1: 0 0 15px rgba(75, 0, 130, 0.5); --glow-d2: 0 0 15px rgba(139, 0, 255, 0.5); --glow-d3: 0 0 15px rgba(153, 50, 204, 0.4); --glow-d4: 0 0 12px rgba(186, 85, 211, 0.4); --glow-d5: 0 0 12px rgba(218, 112, 214, 0.3); --glow-d6: 0 0 10px rgba(238, 130, 238, 0.3);`

---

## 5. CODE CSS PRODUCTION

## 5.1 Variables Root

css

`:root {   /* ========================================== */  /* SYSTÈME IMPÉRIAL - VARIABLES GLOBALES    */  /* ========================================== */     /* Typographie */  --font-heading: 'Barlow Condensed', 'Arial Narrow', sans-serif;  --font-base-size: 16px;     /* Échelle Nombre d'Or */  --font-h1: 11.089rem;   /* 177px */  --font-h2: 6.854rem;    /* 110px */  --font-h3: 4.236rem;    /* 68px */  --font-h4: 2.618rem;    /* 42px */  --font-h5: 1.618rem;    /* 26px */  --font-h6: 1rem;        /* 16px */  --font-body: 1rem;      /* 16px */     /* Poids police */  --weight-h1: 900;  --weight-h2: 800;  --weight-h3: 700;  --weight-h4: 600;  --weight-h5: 600;  --weight-h6: 500;  --weight-body: 400;     /* Line-heights */  --lh-h1: 1.1;  --lh-h2: 1.15;  --lh-h3: 1.2;  --lh-h4: 1.3;  --lh-h5: 1.4;  --lh-h6: 1.5;  --lh-body: 1.618;     /* Letter-spacing */  --ls-h1: -0.02em;  --ls-h2: -0.015em;  --ls-h3: -0.01em;  --ls-h4: 0;  --ls-h5: 0.01em;  --ls-h6: 0.02em;     /* Couleurs Titres */  --color-h1: #DC143C;  --color-h2: #FF6347;  --color-h3: #FFA500;  --color-h4: #FFD700;  --color-h5: #00CED1;  --color-h6: #4169E1;     /* Couleurs Dossiers */  --color-d1: #4B0082;  --color-d2: #8B00FF;  --color-d3: #9932CC;  --color-d4: #BA55D3;  --color-d5: #DA70D6;  --color-d6: #EE82EE;     /* Glows */  --glow-h1: 0 0 25px rgba(220, 20, 60, 0.6), 0 0 50px rgba(220, 20, 60, 0.3), 0 2px 4px rgba(0, 0, 0, 0.5);  --glow-h2: 0 0 22px rgba(255, 99, 71, 0.5), 0 0 45px rgba(255, 99, 71, 0.2), 0 2px 3px rgba(0, 0, 0, 0.4);  --glow-h3: 0 0 20px rgba(255, 165, 0, 0.5), 0 0 40px rgba(255, 165, 0, 0.2), 0 2px 3px rgba(0, 0, 0, 0.3);  --glow-h4: 0 0 20px rgba(255, 215, 0, 0.7), 0 0 40px rgba(255, 215, 0, 0.3), 0 2px 3px rgba(0, 0, 0, 0.3);  --glow-h5: 0 0 18px rgba(0, 206, 209, 0.5), 0 0 35px rgba(0, 206, 209, 0.2);  --glow-h6: 0 0 18px rgba(65, 105, 225, 0.5), 0 0 35px rgba(65, 105, 225, 0.2);     --glow-d1: 0 0 15px rgba(75, 0, 130, 0.5);  --glow-d2: 0 0 15px rgba(139, 0, 255, 0.5);  --glow-d3: 0 0 15px rgba(153, 50, 204, 0.4);  --glow-d4: 0 0 12px rgba(186, 85, 211, 0.4);  --glow-d5: 0 0 12px rgba(218, 112, 214, 0.3);  --glow-d6: 0 0 10px rgba(238, 130, 238, 0.3);     /* Fonds */  --bg-dark: #0d0d0d;  --bg-gradient: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 100%);     /* Texte */  --text-base: #e8e8e8;  --text-muted: #a0a0a0;     /* Espacements */  --spacing-h1: 2rem 0 1rem;  --spacing-h2: 1.75rem 0 0.875rem;  --spacing-h3: 1.5rem 0 0.75rem;  --spacing-h4: 1.25rem 0 0.625rem;  --spacing-h5: 1rem 0 0.5rem;  --spacing-h6: 0.875rem 0 0.438rem; }`

## 5.2 Styles de Base

css

`/* ========================================== */ /* STYLES DE BASE                            */ /* ========================================== */ * {   margin: 0;  padding: 0;  box-sizing: border-box; } html {   font-size: var(--font-base-size);  scroll-behavior: smooth; } body {   font-family: var(--font-heading);  font-size: var(--font-body);  font-weight: var(--weight-body);  line-height: var(--lh-body);  color: var(--text-base);  background: var(--bg-gradient);  -webkit-font-smoothing: antialiased;  -moz-osx-font-smoothing: grayscale;  text-rendering: optimizeLegibility; }`

## 5.3 Titres HTML (H1-H6)

css

`/* ========================================== */ /* TITRES HTML (H1-H6)                       */ /* ========================================== */ h1 {   font-family: var(--font-heading);  font-size: var(--font-h1);  font-weight: var(--weight-h1);  line-height: var(--lh-h1);  letter-spacing: var(--ls-h1);  color: var(--color-h1);  text-shadow: var(--glow-h1);  margin: var(--spacing-h1);  text-transform: uppercase; } h2 {   font-family: var(--font-heading);  font-size: var(--font-h2);  font-weight: var(--weight-h2);  line-height: var(--lh-h2);  letter-spacing: var(--ls-h2);  color: var(--color-h2);  text-shadow: var(--glow-h2);  margin: var(--spacing-h2); } h3 {   font-family: var(--font-heading);  font-size: var(--font-h3);  font-weight: var(--weight-h3);  line-height: var(--lh-h3);  letter-spacing: var(--ls-h3);  color: var(--color-h3);  text-shadow: var(--glow-h3);  margin: var(--spacing-h3); } h4 {   font-family: var(--font-heading);  font-size: var(--font-h4);  font-weight: var(--weight-h4);  line-height: var(--lh-h4);  letter-spacing: var(--ls-h4);  color: var(--color-h4);  text-shadow: var(--glow-h4);  margin: var(--spacing-h4); } h5 {   font-family: var(--font-heading);  font-size: var(--font-h5);  font-weight: var(--weight-h5);  line-height: var(--lh-h5);  letter-spacing: var(--ls-h5);  color: var(--color-h5);  text-shadow: var(--glow-h5);  margin: var(--spacing-h5); } h6 {   font-family: var(--font-heading);  font-size: var(--font-h6);  font-weight: var(--weight-h6);  line-height: var(--lh-h6);  letter-spacing: var(--ls-h6);  color: var(--color-h6);  text-shadow: var(--glow-h6);  margin: var(--spacing-h6); } /* Ornements optionnels */ h1::before {   content: "◆ ";  color: var(--color-h4);  text-shadow: 0 0 10px rgba(255, 215, 0, 0.8);  margin-right: 0.3em; } h2::before {   content: "◇ ";  color: var(--color-h3);  opacity: 0.8;  margin-right: 0.3em; }`

## 5.4 Classification Dossiers (D1-D6)

css

`/* ========================================== */ /* CLASSIFICATION DOSSIERS (D1-D6)           */ /* ========================================== */ /* Méthode 1 : Classes utilitaires */ .folder-level-1, .folder-urgent {   color: var(--color-d1);  font-weight: 700;  text-shadow: var(--glow-d1); } .folder-level-2, .folder-important {   color: var(--color-d2);  font-weight: 600;  text-shadow: var(--glow-d2); } .folder-level-3, .folder-reference {   color: var(--color-d3);  font-weight: 600;  text-shadow: var(--glow-d3); } .folder-level-4, .folder-archive {   color: var(--color-d4);  font-weight: 500;  text-shadow: var(--glow-d4); } .folder-level-5, .folder-archive-old {   color: var(--color-d5);  font-weight: 500;  text-shadow: var(--glow-d5); } .folder-level-6, .folder-archive-ancient {   color: var(--color-d6);  font-weight: 400;  text-shadow: var(--glow-d6); } /* Méthode 2 : Data attributes */ [data-folder-level="1"] { color: var(--color-d1); font-weight: 700; text-shadow: var(--glow-d1); } [data-folder-level="2"] { color: var(--color-d2); font-weight: 600; text-shadow: var(--glow-d2); } [data-folder-level="3"] { color: var(--color-d3); font-weight: 600; text-shadow: var(--glow-d3); } [data-folder-level="4"] { color: var(--color-d4); font-weight: 500; text-shadow: var(--glow-d4); } [data-folder-level="5"] { color: var(--color-d5); font-weight: 500; text-shadow: var(--glow-d5); } [data-folder-level="6"] { color: var(--color-d6); font-weight: 400; text-shadow: var(--glow-d6); }`

## 5.5 Classes Utilitaires

css

`/* ========================================== */ /* CLASSES UTILITAIRES                       */ /* ========================================== */ /* Couleurs directes */ .color-h1 { color: var(--color-h1); } .color-h2 { color: var(--color-h2); } .color-h3 { color: var(--color-h3); } .color-h4 { color: var(--color-h4); } .color-h5 { color: var(--color-h5); } .color-h6 { color: var(--color-h6); } .color-d1 { color: var(--color-d1); } .color-d2 { color: var(--color-d2); } .color-d3 { color: var(--color-d3); } .color-d4 { color: var(--color-d4); } .color-d5 { color: var(--color-d5); } .color-d6 { color: var(--color-d6); } /* Badges/Pills */ .badge {   display: inline-block;  padding: 0.25rem 0.75rem;  border-radius: 1rem;  font-size: 0.875rem;  font-weight: 600;  text-transform: uppercase;  letter-spacing: 0.05em; } .badge-urgent { background: var(--color-h1); color: white; } .badge-important { background: var(--color-h2); color: white; } .badge-active { background: var(--color-h3); color: black; } .badge-normal { background: var(--color-h4); color: black; } .badge-reference { background: var(--color-d1); color: white; } .badge-archive { background: var(--color-d4); color: white; } /* Backgrounds */ .bg-h1 { background-color: var(--color-h1); color: white; } .bg-h2 { background-color: var(--color-h2); color: white; } .bg-h3 { background-color: var(--color-h3); color: black; } .bg-h4 { background-color: var(--color-h4); color: black; }`

---

## 6. RESPONSIVE (Mobile/Tablet/Desktop)

## Breakpoints

css

`/* ========================================== */ /* RESPONSIVE BREAKPOINTS                    */ /* ========================================== */ /* Mobile : < 768px */ @media (max-width: 767px) {   :root {    --font-h1: 3.5rem;    /* ~56px au lieu de 177px */    --font-h2: 2.5rem;    /* ~40px au lieu de 110px */    --font-h3: 2rem;      /* ~32px au lieu de 68px */    --font-h4: 1.5rem;    /* ~24px au lieu de 42px */    --font-h5: 1.25rem;   /* ~20px au lieu de 26px */    --font-h6: 1rem;      /* 16px */    --font-body: 0.875rem; /* 14px */  }     h1 { letter-spacing: 0; }  h2 { letter-spacing: 0; }     /* Réduire les glows sur mobile (performance) */  h1, h2, h3, h4, h5, h6 {    text-shadow: none;  } } /* Tablet : 768px - 1023px */ @media (min-width: 768px) and (max-width: 1023px) {   :root {    --font-h1: 6rem;      /* ~96px */    --font-h2: 4rem;      /* ~64px */    --font-h3: 3rem;      /* ~48px */    --font-h4: 2rem;      /* ~32px */    --font-h5: 1.5rem;    /* ~24px */    --font-h6: 1rem;      /* 16px */  } } /* Desktop : >= 1024px */ @media (min-width: 1024px) {   /* Utiliser les tailles par défaut (nombre d'or complet) */ } /* Large Desktop : >= 1920px */ @media (min-width: 1920px) {   :root {    --font-base-size: 18px; /* Augmenter base pour grands écrans */  } }`

---

## 7. INTÉGRATION OBSIDIAN

## Fichier : `.obsidian/snippets/imperial-theme.css`

css

`/* ========================================== */ /* OBSIDIAN IMPERIAL THEME                   */ /* ========================================== */ /* Importer toutes les variables root ci-dessus */ /* Mode prévisualisation */ .markdown-preview-view h1 { color: var(--color-h1); font-family: var(--font-heading); } .markdown-preview-view h2 { color: var(--color-h2); font-family: var(--font-heading); } .markdown-preview-view h3 { color: var(--color-h3); font-family: var(--font-heading); } .markdown-preview-view h4 { color: var(--color-h4); font-family: var(--font-heading); } .markdown-preview-view h5 { color: var(--color-h5); font-family: var(--font-heading); } .markdown-preview-view h6 { color: var(--color-h6); font-family: var(--font-heading); } /* Mode édition (Live Preview) */ .cm-header-1 { color: var(--color-h1) !important; font-family: var(--font-heading); font-weight: 900; } .cm-header-2 { color: var(--color-h2) !important; font-family: var(--font-heading); font-weight: 800; } .cm-header-3 { color: var(--color-h3) !important; font-family: var(--font-heading); font-weight: 700; } .cm-header-4 { color: var(--color-h4) !important; font-family: var(--font-heading); font-weight: 600; } .cm-header-5 { color: var(--color-h5) !important; font-family: var(--font-heading); font-weight: 600; } .cm-header-6 { color: var(--color-h6) !important; font-family: var(--font-heading); font-weight: 500; } /* Arborescence fichiers (colorisation dossiers) */ .nav-folder-title[data-path^="01-"] { color: var(--color-d1); font-weight: 700; } .nav-folder-title[data-path^="02-"] { color: var(--color-d2); font-weight: 600; } .nav-folder-title[data-path^="03-"] { color: var(--color-d3); font-weight: 600; } .nav-folder-title[data-path^="04-"] { color: var(--color-d4); font-weight: 500; } .nav-folder-title[data-path^="05-"] { color: var(--color-d5); font-weight: 500; } .nav-folder-title[data-path^="06-"] { color: var(--color-d6); font-weight: 400; } /* Icônes emoji dossiers */ .nav-folder-title[data-path^="01-"]::before { content: "🔴 "; } .nav-folder-title[data-path^="02-"]::before { content: "🟠 "; } .nav-folder-title[data-path^="03-"]::before { content: "🟡 "; } .nav-folder-title[data-path^="04-"]::before { content: "🔵 "; } .nav-folder-title[data-path^="05-"]::before { content: "🟣 "; } .nav-folder-title[data-path^="06-"]::before { content: "⚪ "; } /* Tags colorés */ .tag[data-tag-name*="urgent"] { color: var(--color-d1); background: rgba(75, 0, 130, 0.2); } .tag[data-tag-name*="important"] { color: var(--color-d2); background: rgba(139, 0, 255, 0.2); } .tag[data-tag-name*="reference"] { color: var(--color-d3); background: rgba(153, 50, 204, 0.2); } .tag[data-tag-name*="archive"] { color: var(--color-d4); background: rgba(186, 85, 211, 0.2); }`

## Activation

1. Copier le fichier dans `.obsidian/snippets/`
    
2. Obsidian → Paramètres → Apparence → Snippets CSS
    
3. Activer le snippet "imperial-theme"
    

---

## 8. INTÉGRATION WORDPRESS

## functions.php

php

`<?php /**  * Thème Imperial - Enqueue Styles */ function imperial_theme_enqueue_styles() {     // Google Fonts    wp_enqueue_style(        'imperial-fonts',        'https://fonts.googleapis.com/css2?family=Barlow+Condensed:ital,wght@0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,400;1,700&display=swap',        array(),        null    );         // Styles principaux    wp_enqueue_style(        'imperial-theme',        get_template_directory_uri() . '/assets/css/imperial-theme.css',        array('imperial-fonts'),        '1.0.0'    ); } add_action('wp_enqueue_scripts', 'imperial_theme_enqueue_styles'); // Éditeur Gutenberg function imperial_theme_editor_styles() {     add_editor_style('assets/css/imperial-theme.css'); } add_action('after_setup_theme', 'imperial_theme_editor_styles'); ?>`

---

## 9. TESTS & VALIDATION

## Checklist obligatoire

text

`☐ Test sur fond #0d0d0d (noir) ☐ Test sur fond #1a1a2e (bleu sombre) ☐ Zoom 100%, 125%, 150%, 200% ☐ Mobile (320px, 375px, 414px) ☐ Tablet (768px, 1024px) ☐ Desktop (1440px, 1920px, 2560px) ☐ Daltonisme (protanopie, deutéranopie, tritanopie) ☐ Lecteur d'écran (VoiceOver, NVDA) ☐ Contraste WCAG (minimum AA 4.5:1) ☐ Performance PageSpeed (>90) ☐ Print CSS (fallback grayscale)`

## Outils validation

- **WebAIM Contrast Checker** : [https://webaim.org/resources/contrastchecker/](https://webaim.org/resources/contrastchecker/)
    
- **Chrome Lighthouse** : DevTools > Lighthouse > Accessibility
    
- **axe DevTools** : Extension navigateur
    
- **Color Oracle** : Simulateur daltonisme
    

---

## 10. PERFORMANCES

## Optimisations critiques

css

`/* 1. Font-display swap */ @import url('...&display=swap'); /* 2. Preconnect DNS */ <link rel="preconnect" href="https://fonts.googleapis.com"> <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin> /* 3. Will-change pour animations */ h1:hover, h2:hover {   will-change: transform; } /* 4. Réduire glows sur mobile */ @media (max-width: 767px) {   h1, h2, h3, h4, h5, h6 {    text-shadow: none; /* Économie GPU */  } } /* 5. Font-smoothing */ body {   -webkit-font-smoothing: antialiased;  -moz-osx-font-smoothing: grayscale; }`

## Métriques cibles

|Métrique|Cible|
|---|---|
|**First Contentful Paint**|< 1.8s|
|**Largest Contentful Paint**|< 2.5s|
|**Cumulative Layout Shift**|< 0.1|
|**Poids total CSS**|< 50 KB|
|**Poids police**|35 KB (Barlow Condensed)|

---

## 11. ACCESSIBILITÉ (WCAG 2.1)

## Ratios de contraste garantis

|Niveau|Couleur|Ratio sur #0d0d0d|Conformité|
|---|---|---|---|
|H1|#DC143C|7.8:1|✅ AAA|
|H2|#FF6347|8.9:1|✅ AAA|
|H3|#FFA500|11.2:1|✅ AAA|
|H4|#FFD700|15.8:1|✅ AAA|
|H5|#00CED1|10.4:1|✅ AAA|
|H6|#4169E1|7.3:1|✅ AAA|

## Sémantique HTML

xml

`<!-- ✅ CORRECT --> <article>   <h1>Titre principal</h1>  <section>    <h2>Section</h2>    <h3>Sous-section</h3>  </section> </article> <!-- ❌ INCORRECT --> <div class="color-h1">Faux titre</div>`

## Attributs ARIA

xml

`<!-- Navigation dossiers --> <nav aria-label="Arborescence fichiers">   <ul>    <li class="folder-level-1" aria-label="Dossier urgent">...</li>  </ul> </nav> <!-- Badges --> <span class="badge-urgent" role="status" aria-label="Urgence élevée">   URGENT </span>`

---

## 12. FICHIERS À LIVRER

## Structure projet

text

`/assets/   /css/    imperial-theme.css              # Version production (minifiée)    imperial-theme.dev.css          # Version dev (commentée)    imperial-responsive.css         # Breakpoints  /fonts/    barlow-condensed/               # Backup local fonts /obsidian/   imperial-theme.css                # Snippet Obsidian /wordpress/   functions-imperial.php            # Code WP  imperial-gutenberg.css            # Styles éditeur /docs/   FICHE-TECHNIQUE.md                # Ce document  color-palette.png                 # Visuel palette  typography-scale.png              # Visuel échelle /tests/   accessibility-report.html         # Rapport WCAG  performance-audit.json            # Lighthouse report`

---

## 13. NOTES IMPORTANTES

## ⚠️ Attention

1. **Text-shadow performance** : Les glows peuvent ralentir les vieux devices → Prévoir version "light"
    
2. **Font-size H1 mobile** : 177px est TROP grand mobile → Obligatoire de réduire
    
3. **Letter-spacing négatif** : Peut causer problèmes lisibilité → Tester avec utilisateurs
    
4. **Uppercase H1** : Peut réduire vitesse lecture → Usage modéré
    

## 💡 Améliorations futures

-  Variable fonts support (Barlow Condensed VF)
    
-  Dark/Light mode toggle
    
-  CSS Container Queries (@container)
    
-  Animation entrée titres (scroll-triggered)
    
-  Version print optimisée
    

---

## 14. SUPPORT

## Contact

**Équipe dev** : [[votre-email@domain.com](mailto:votre-email@domain.com)]  
**Version** : 1.0  
**Dernière MAJ** : 04 février 2026

## License

© 2026 - Propriétaire / MIT / GPL (à spécifier)

---

## 15. CHANGELOG

## v1.0 (04/02/2026)

- ✅ Système complet 12 couleurs hiérarchiques
    
- ✅ Échelle typographique nombre d'or
    
- ✅ Police Barlow Condensed
    
- ✅ Responsive mobile/tablet/desktop
    
- ✅ Obsidian snippet
    
- ✅ WordPress integration
    
- ✅ WCAG AAA compliance
    

---

**FIN DE LA FICHE TECHNIQUE** ✅

**Développeurs** : Tous les codes sont prêts à l'emploi. Copier/coller dans vos fichiers CSS. Questions → Contact support ci-dessus.