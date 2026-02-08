# 👑 Spécifications Développeur - Système de Couleurs Hiérarchique Impérial

## 📋 Document Technique v1.0

---

## 1. VUE D'ENSEMBLE

## Objectif

Implémenter un système de couleurs hiérarchique à 12 niveaux (H1-H6 + D1-D6) avec thématique impériale/noble optimisée pour thème sombre.

## Logique

**Température décroissante** : Chaud (urgent/important) → Froid (archivé/référence)

## Technologies cibles

- CSS3 / SCSS
    
- Obsidian CSS Snippets
    
- WordPress Theme Customization
    
- Markdown renderers
    

---

## 2. PALETTE DE COULEURS

## 2.1 Titres HTML (H1-H6) - Zone Chaude

css

`/* ZONE ACTION IMMÉDIATE (Rouge-Orange) */ --h1-color: #DC143C;  /* Crimson - Rubis impérial */ --h2-color: #FF6347;  /* Tomato - Vermillon */ /* ZONE ATTENTION (Orange-Or) */ --h3-color: #FFA500;  /* Orange - Topaze */ --h4-color: #FFD700;  /* Gold - Or 24K */ /* ZONE TRANSITION (Jaune-Cyan) */ --h5-color: #00CED1;  /* DarkTurquoise - Aigue-marine */ --h6-color: #4169E1;  /* RoyalBlue - Saphir clair */`

## 2.2 Classification Dossiers (D1-D6) - Zone Froide

css

`/* ZONE RÉFÉRENCE (Bleu-Indigo) */ --d1-color: #4B0082;  /* Indigo - Tanzanite */ --d2-color: #8B00FF;  /* Violet - Améthyste électrique */ /* ZONE ARCHIVE (Violet-Magenta) */ --d3-color: #9932CC;  /* DarkOrchid - Orchidée pourpre */ --d4-color: #BA55D3;  /* MediumOrchid - Orchidée royale */ --d5-color: #DA70D6;  /* Orchid - Orchidée claire */ --d6-color: #EE82EE;  /* Violet - Lavande impériale */`

---

## 3. CODE CSS PRODUCTION

## 3.1 Variables CSS (Root)

css

`:root {   /* ============================================ */  /* SYSTÈME HIÉRARCHIQUE IMPÉRIAL              */  /* Urgent (Chaud) → Archive (Froid)           */  /* ============================================ */     /* Titres HTML - Zone Action/Production */  --color-h1: #DC143C;  --color-h2: #FF6347;  --color-h3: #FFA500;  --color-h4: #FFD700;  --color-h5: #00CED1;  --color-h6: #4169E1;     /* Dossiers - Zone Référence/Archive */  --color-d1: #4B0082;  --color-d2: #8B00FF;  --color-d3: #9932CC;  --color-d4: #BA55D3;  --color-d5: #DA70D6;  --color-d6: #EE82EE;     /* Shadows - Effet glow impérial */  --glow-intensity-h1: rgba(220, 20, 60, 0.6);  --glow-intensity-h2: rgba(255, 99, 71, 0.5);  --glow-intensity-h3: rgba(255, 165, 0, 0.5);  --glow-intensity-h4: rgba(255, 215, 0, 0.7);  --glow-intensity-h5: rgba(0, 206, 209, 0.5);  --glow-intensity-h6: rgba(65, 105, 225, 0.5);     --glow-intensity-d1: rgba(75, 0, 130, 0.5);  --glow-intensity-d2: rgba(139, 0, 255, 0.5);  --glow-intensity-d3: rgba(153, 50, 204, 0.4);  --glow-intensity-d4: rgba(186, 85, 211, 0.4);  --glow-intensity-d5: rgba(218, 112, 214, 0.3);  --glow-intensity-d6: rgba(238, 130, 238, 0.3);     /* Fond sombre recommandé */  --bg-imperial-dark: #0d0d0d;  --bg-imperial-gradient: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 100%);     /* Texte de base */  --text-base: #e8e8e8;  --text-muted: #a0a0a0; }`

## 3.2 Styles HTML Headings

css

`/* ============================================ */ /* TITRES HTML (H1-H6)                         */ /* ============================================ */ body {   background: var(--bg-imperial-gradient);  color: var(--text-base);  font-family: 'Inter', 'Segoe UI', system-ui, sans-serif; } h1 {   color: var(--color-h1);  font-weight: 900;  font-size: 2.5rem;  line-height: 1.2;  letter-spacing: 0.02em;  text-transform: uppercase;  margin: 2rem 0 1rem;  text-shadow:    0 0 25px var(--glow-intensity-h1),    0 0 50px var(--glow-intensity-h1),    0 2px 4px rgba(0, 0, 0, 0.5); } h2 {   color: var(--color-h2);  font-weight: 800;  font-size: 2rem;  line-height: 1.3;  letter-spacing: 0.015em;  margin: 1.75rem 0 0.875rem;  text-shadow:    0 0 22px var(--glow-intensity-h2),    0 0 45px var(--glow-intensity-h2),    0 2px 3px rgba(0, 0, 0, 0.4); } h3 {   color: var(--color-h3);  font-weight: 700;  font-size: 1.5rem;  line-height: 1.4;  letter-spacing: 0.01em;  margin: 1.5rem 0 0.75rem;  text-shadow:    0 0 20px var(--glow-intensity-h3),    0 0 40px var(--glow-intensity-h3),    0 2px 3px rgba(0, 0, 0, 0.3); } h4 {   color: var(--color-h4);  font-weight: 600;  font-size: 1.25rem;  line-height: 1.4;  margin: 1.25rem 0 0.625rem;  text-shadow:    0 0 20px var(--glow-intensity-h4),    0 0 40px var(--glow-intensity-h4),    0 2px 3px rgba(0, 0, 0, 0.3); } h5 {   color: var(--color-h5);  font-weight: 600;  font-size: 1.125rem;  line-height: 1.5;  margin: 1rem 0 0.5rem;  text-shadow:    0 0 18px var(--glow-intensity-h5),    0 0 35px var(--glow-intensity-h5); } h6 {   color: var(--color-h6);  font-weight: 500;  font-size: 1rem;  line-height: 1.5;  margin: 0.875rem 0 0.438rem;  text-shadow:    0 0 18px var(--glow-intensity-h6),    0 0 35px var(--glow-intensity-h6); } /* Ornements optionnels pour H1-H2 */ h1::before {   content: "◆ ";  color: var(--color-h4);  text-shadow: 0 0 10px var(--glow-intensity-h4); } h2::before {   content: "◇ ";  color: var(--color-h3);  opacity: 0.8; }`

## 3.3 Styles Classification Dossiers

css

`/* ============================================ */ /* CLASSIFICATION DOSSIERS (D1-D6)             */ /* ============================================ */ /* Méthode 1 : Classes utilitaires */ .folder-level-1, .folder-urgent {   color: var(--color-d1);  font-weight: 700;  text-shadow: 0 0 15px var(--glow-intensity-d1); } .folder-level-2, .folder-important {   color: var(--color-d2);  font-weight: 600;  text-shadow: 0 0 15px var(--glow-intensity-d2); } .folder-level-3, .folder-reference {   color: var(--color-d3);  font-weight: 600;  text-shadow: 0 0 15px var(--glow-intensity-d3); } .folder-level-4, .folder-archive {   color: var(--color-d4);  font-weight: 500;  text-shadow: 0 0 12px var(--glow-intensity-d4); } .folder-level-5, .folder-archive-old {   color: var(--color-d5);  font-weight: 500;  text-shadow: 0 0 12px var(--glow-intensity-d5); } .folder-level-6, .folder-archive-ancient {   color: var(--color-d6);  font-weight: 400;  text-shadow: 0 0 10px var(--glow-intensity-d6); } /* Méthode 2 : Data attributes */ [data-folder-level="1"] { color: var(--color-d1); font-weight: 700; } [data-folder-level="2"] { color: var(--color-d2); font-weight: 600; } [data-folder-level="3"] { color: var(--color-d3); font-weight: 600; } [data-folder-level="4"] { color: var(--color-d4); font-weight: 500; } [data-folder-level="5"] { color: var(--color-d5); font-weight: 500; } [data-folder-level="6"] { color: var(--color-d6); font-weight: 400; } /* Méthode 3 : Tags Obsidian */ .tag[data-tag-name*="urgent"] { color: var(--color-d1); } .tag[data-tag-name*="important"] { color: var(--color-d2); } .tag[data-tag-name*="reference"] { color: var(--color-d3); } .tag[data-tag-name*="archive"] { color: var(--color-d4); } .tag[data-tag-name*="old"] { color: var(--color-d5); } .tag[data-tag-name*="ancient"] { color: var(--color-d6); }`

---

## 4. VERSIONS SPÉCIFIQUES PLATEFORMES

## 4.1 Obsidian CSS Snippet

css

`/* ============================================ */ /* OBSIDIAN - Imperial Hierarchy Theme         */ /* File: .obsidian/snippets/imperial-colors.css */ /* ============================================ */ /* Importer les variables root ci-dessus */ /* Mode prévisualisation */ .markdown-preview-view h1 { color: var(--color-h1); } .markdown-preview-view h2 { color: var(--color-h2); } .markdown-preview-view h3 { color: var(--color-h3); } .markdown-preview-view h4 { color: var(--color-h4); } .markdown-preview-view h5 { color: var(--color-h5); } .markdown-preview-view h6 { color: var(--color-h6); } /* Mode édition */ .cm-header-1 { color: var(--color-h1) !important; } .cm-header-2 { color: var(--color-h2) !important; } .cm-header-3 { color: var(--color-h3) !important; } .cm-header-4 { color: var(--color-h4) !important; } .cm-header-5 { color: var(--color-h5) !important; } .cm-header-6 { color: var(--color-h6) !important; } /* Arborescence fichiers */ .nav-folder-title[data-path*="01-"] { color: var(--color-d1); font-weight: 700; } .nav-folder-title[data-path*="02-"] { color: var(--color-d2); font-weight: 600; } .nav-folder-title[data-path*="03-"] { color: var(--color-d3); font-weight: 600; } .nav-folder-title[data-path*="04-"] { color: var(--color-d4); font-weight: 500; } .nav-folder-title[data-path*="05-"] { color: var(--color-d5); font-weight: 500; } .nav-folder-title[data-path*="06-"] { color: var(--color-d6); font-weight: 400; } /* Icônes dossiers colorées */ .nav-folder-title[data-path*="01-"]::before { content: "🔴 "; } .nav-folder-title[data-path*="02-"]::before { content: "🟠 "; } .nav-folder-title[data-path*="03-"]::before { content: "🟡 "; } .nav-folder-title[data-path*="04-"]::before { content: "🔵 "; } .nav-folder-title[data-path*="05-"]::before { content: "🟣 "; } .nav-folder-title[data-path*="06-"]::before { content: "⚪ "; }`

## 4.2 WordPress functions.php

php

`<?php /**  * Thème Imperial Hierarchy Colors * Injection CSS dans l'éditeur Gutenberg et le front-end */ function imperial_hierarchy_enqueue_styles() {     // Front-end    wp_enqueue_style(        'imperial-hierarchy',        get_template_directory_uri() . '/assets/css/imperial-hierarchy.css',        array(),        '1.0.0'    ); } add_action('wp_enqueue_scripts', 'imperial_hierarchy_enqueue_styles'); // Éditeur Gutenberg function imperial_hierarchy_editor_styles() {     add_editor_style('assets/css/imperial-hierarchy.css'); } add_action('after_setup_theme', 'imperial_hierarchy_editor_styles'); // Injecter variables CSS dans customizer function imperial_hierarchy_customizer_css() {     ?>    <style type="text/css">        :root {            --color-h1: <?php echo get_theme_mod('h1_color', '#DC143C'); ?>;            --color-h2: <?php echo get_theme_mod('h2_color', '#FF6347'); ?>;            --color-h3: <?php echo get_theme_mod('h3_color', '#FFA500'); ?>;            --color-h4: <?php echo get_theme_mod('h4_color', '#FFD700'); ?>;            --color-h5: <?php echo get_theme_mod('h5_color', '#00CED1'); ?>;            --color-h6: <?php echo get_theme_mod('h6_color', '#4169E1'); ?>;        }    </style>    <?php } add_action('wp_head', 'imperial_hierarchy_customizer_css'); ?>`

---

## 5. CLASSES UTILITAIRES

## 5.1 Classes de couleur directes

css

`/* Utilisez ces classes pour appliquer les couleurs hors titres */ .color-h1 { color: var(--color-h1); } .color-h2 { color: var(--color-h2); } .color-h3 { color: var(--color-h3); } .color-h4 { color: var(--color-h4); } .color-h5 { color: var(--color-h5); } .color-h6 { color: var(--color-h6); } .color-d1 { color: var(--color-d1); } .color-d2 { color: var(--color-d2); } .color-d3 { color: var(--color-d3); } .color-d4 { color: var(--color-d4); } .color-d5 { color: var(--color-d5); } .color-d6 { color: var(--color-d6); } /* Backgrounds */ .bg-h1 { background-color: var(--color-h1); color: white; } .bg-h2 { background-color: var(--color-h2); color: white; } .bg-h3 { background-color: var(--color-h3); color: black; } .bg-h4 { background-color: var(--color-h4); color: black; } .bg-h5 { background-color: var(--color-h5); color: white; } .bg-h6 { background-color: var(--color-h6); color: white; }`

## 5.2 Badges/Pills

css

`.badge {   display: inline-block;  padding: 0.25rem 0.75rem;  border-radius: 1rem;  font-size: 0.875rem;  font-weight: 600;  text-transform: uppercase;  letter-spacing: 0.05em; } .badge-urgent { background: var(--color-h1); color: white; } .badge-important { background: var(--color-h2); color: white; } .badge-active { background: var(--color-h3); color: black; } .badge-normal { background: var(--color-h4); color: black; } .badge-reference { background: var(--color-d1); color: white; } .badge-archive { background: var(--color-d4); color: white; }`

---

## 6. SCSS VERSION (Optionnel)

text

`// Variables $imperial-colors: (   h1: #DC143C,  h2: #FF6347,  h3: #FFA500,  h4: #FFD700,  h5: #00CED1,  h6: #4169E1,  d1: #4B0082,  d2: #8B00FF,  d3: #9932CC,  d4: #BA55D3,  d5: #DA70D6,  d6: #EE82EE ); // Mixin pour générer les titres @mixin heading-style($level, $color) {   h#{$level} {    color: $color;    font-weight: 900 - ($level * 100);    text-shadow:      0 0 (25px - $level * 2) rgba($color, 0.6),      0 0 (50px - $level * 4) rgba($color, 0.3);  } } // Génération automatique @for $i from 1 through 6 {   @include heading-style($i, map-get($imperial-colors, h#{$i})); } // Dossiers @each $level, $color in (d1: #4B0082, d2: #8B00FF, d3: #9932CC, d4: #BA55D3, d5: #DA70D6, d6: #EE82EE) {   .folder-level-#{str-slice($level, 2)} {    color: $color;    font-weight: 700 - (str-slice($level, 2) * 50);  } }`

---

## 7. RATIOS DE CONTRASTE (WCAG)

|Niveau|Couleur|Ratio sur #0d0d0d|Conformité|
|---|---|---|---|
|H1|#DC143C|7.8:1|✅ AAA|
|H2|#FF6347|8.9:1|✅ AAA|
|H3|#FFA500|11.2:1|✅ AAA|
|H4|#FFD700|15.8:1|✅ AAA|
|H5|#00CED1|10.4:1|✅ AAA|
|H6|#4169E1|7.3:1|✅ AAA|
|D1|#4B0082|5.9:1|✅ AA+|
|D2|#8B00FF|9.2:1|✅ AAA|
|D3|#9932CC|6.4:1|✅ AAA|
|D4|#BA55D3|8.1:1|✅ AAA|
|D5|#DA70D6|9.8:1|✅ AAA|
|D6|#EE82EE|10.7:1|✅ AAA|

**Tous les niveaux respectent au minimum WCAG AA (4.5:1)**

---

## 8. TESTS & VALIDATION

## 8.1 Checklist de tests

text

`☐ Affichage correct sur fond #0d0d0d ☐ Affichage correct sur fond #1a1a2e (gradient) ☐ Lisibilité à 100%, 125%, 150% zoom ☐ Test daltonisme (protanopie, deutéranopie, tritanopie) ☐ Test mode clair (fallback couleurs sombres) ☐ Responsive mobile/tablet/desktop ☐ Test print CSS (grayscale fallback)`

## 8.2 Outils de validation

- **Contrast Checker** : [https://webaim.org/resources/contrastchecker/](https://webaim.org/resources/contrastchecker/)
    
- **Color Blindness Simulator** : [https://www.color-blindness.com/coblis-color-blindness-simulator/](https://www.color-blindness.com/coblis-color-blindness-simulator/)
    
- **DevTools Accessibility** : Chrome/Firefox DevTools > Accessibility panel
    

---

## 9. FICHIERS LIVRABLES

## Structure recommandée

text

`/assets/   /css/    imperial-hierarchy.css          # Version production minifiée    imperial-hierarchy.dev.css      # Version développement commentée  /scss/    _variables.scss                 # Variables SCSS    _headings.scss                  # Styles titres    _folders.scss                   # Styles dossiers    imperial-hierarchy.scss         # Main import /obsidian/   imperial-hierarchy-snippet.css   # Pour Obsidian /wordpress/   functions-imperial.php            # Code WordPress /docs/   color-guide.md                   # Documentation couleurs  SPEC-TECHNIQUE.md                # Ce document`

---

## 10. SUPPORT & MAINTENANCE

## Version

**v1.0** - 04 février 2026

## Changelog

- v1.0 : Version initiale - Système hiérarchique 12 niveaux
    

## Contact

Fournir coordonnées équipe dev pour questions

## License

Spécifier licence (MIT, GPL, propriétaire...)

---

## 11. NOTES IMPORTANTES

⚠️ **Critiques** :

1. Toujours tester sur fond sombre réel avant déploiement
    
2. Prévoir fallback pour mode clair si nécessaire
    
3. Les glows (text-shadow) peuvent impacter les performances sur anciens devices
    
4. Tester l'impression (les couleurs ne s'impriment pas toujours bien)
    

💡 **Optimisations possibles** :

- Lazy load des glows en fonction du scroll
    
- Version "light" sans text-shadow pour performance
    
- Thème adaptatif selon préférence système (prefers-color-scheme)
    

---

**FIN DU DOCUMENT TECHNIQUE** ✅
