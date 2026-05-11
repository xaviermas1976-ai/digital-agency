# CHALOUMI -- Specifications Landing Page E-commerce
## Document de reference developpeur -- APEX DIGITAL
### Version 1.0 | Mai 2026

---

## TABLE DES MATIERES

1. [Architecture de page](#1-architecture-de-page)
2. [Hero Section](#2-hero-section)
3. [Section Produit](#3-section-produit)
4. [Section Histoire](#4-section-histoire)
5. [Section Degustation](#5-section-degustation)
6. [Section Temoignages](#6-section-temoignages)
7. [Section FAQ](#7-section-faq)
8. [Section Commande](#8-section-commande)
9. [Footer](#9-footer)
10. [Conversion Optimization](#10-conversion-optimization)
11. [Specifications Techniques](#11-specifications-techniques)
12. [Checkout Flow](#12-checkout-flow)
13. [Design System](#13-design-system)
14. [Implementation Notes](#14-implementation-notes)

---

## 1. ARCHITECTURE DE PAGE

### Vue d'ensemble du flux de conversion

```
HERO (accroche + CTA)
  |
PRODUIT (decouverte sensorielle + prix)
  |
HISTOIRE (confiance + authenticite)
  |
DEGUSTATION (projection usage + desir)
  |
TEMOIGNAGES (preuve sociale)
  |
FAQ (lever les objections)
  |
COMMANDE (conversion finale)
  |
FOOTER (reassurance juridique)
```

### Barre de navigation fixe (sticky)

```
Position: fixed top, z-index 1000
Background: blanc 95% opacite, blur 8px
Hauteur: 56px mobile / 64px desktop
Contenu:
  - Logo CHALOUMI (gauche)
  - CTA "Commander" (droite, bouton primaire compact)
  - Apparait apres scroll 300px (animation slide-down)
```

**Objectif** : Le CTA est toujours accessible, meme en milieu de page.

### Bandeau de reassurance (au-dessus du header)

```
Position: top of page, sticky au-dessus de la nav
Background: var(--color-brand-dark)
Hauteur: 36px
Texte: blanc, 13px, defilement horizontal sur mobile
Contenu rotatif (3 messages, rotation 4s) :
  1. "Livraison chaine du froid 48h partout en France"
  2. "Fromage artisanal 100% lait de chevre de Chypre"
  3. "Satisfait ou rembourse - retour sous 14 jours"
```

---

## 2. HERO SECTION

### Layout

```
Mobile (< 768px):
  - Image plein ecran (100vw x 85vh)
  - Overlay gradient bas (rgba(0,0,0,0.4) -> transparent)
  - Texte en overlay bas
  - CTA pleine largeur en bas

Desktop (>= 768px):
  - Split layout 55% image / 45% contenu
  - Image a gauche, contenu a droite
  - Contenu centre verticalement
```

### Headlines (3 variations pour A/B test)

**Variation A (Authenticite):**
```
H1: "Le vrai fromage de Chypre, grille a la perfection"
```

**Variation B (Experience sensorielle):**
```
H1: "Croustillant dehors, fondant dedans : le Chaloumi artisanal"
```

**Variation C (Exclusivite):**
```
H1: "Le fromage que les Chypriotes gardaient pour eux"
```

### Sous-titre

```
"100% lait de chevre, fabrique a la main dans les montagnes
du Troodos. Livre chez vous en 48h, chaine du froid garantie."
```

### CTA Principal

```
Texte: "Decouvrir nos coffrets"
Style: bouton large, couleur accent (terracotta/orange chaud)
Taille: 48px hauteur mobile, 56px desktop
Largeur: 100% mobile, auto desktop (min 280px)
Micro-copy sous le CTA: "A partir de 24,90EUR - Livraison offerte des 49EUR"
```

### Hero Shot (brief photo/video)

```
Option 1 (photo statique):
  - Chaloumi grille sur planche en bois d'olivier
  - Filet de miel qui coule, feuilles de menthe fraiche
  - Arriere-plan flou: terrasse mediterraneenne ensoleilllee
  - Format: WebP, 1920x1080, quality 85

Option 2 (video courte, recommandee):
  - 6 secondes, autoplay, muted, loop
  - Sequence: bloc de chaloumi -> poele chaude -> grillade ->
    coupe au couteau montrant l'interieur fondant
  - Format: MP4 H.264, max 2MB
  - Poster image: frame du fromage grille
```

### Elements de reassurance Hero (badges horizontaux)

```
Disposition: flex row, gap 16px, scroll horizontal mobile
3 badges icone + texte:
  1. [icone flocon] "Chaine du froid 48h"
  2. [icone chevre] "100% lait de chevre"
  3. [icone medaille] "Artisanal depuis 1987"
```

---

## 3. SECTION PRODUIT

### Objectif
Presenter le produit de facon sensorielle, justifier le prix, declencher le desir.

### Layout

```
Desktop: grid 2 colonnes (60% galerie / 40% infos)
Mobile: stack vertical (galerie puis infos)
Padding: 80px vertical desktop, 48px mobile
Background: var(--bg-cream)
```

### Galerie produit

```
Composant: carousel swipeable, thumbnails en bas
Images (5 minimum):
  1. Chaloumi entier sur ardoise (pack shot principal)
  2. Chaloumi coupe en deux (texture visible)
  3. Chaloumi sur le grill (action shot)
  4. Coffret livraison ouvert (unboxing)
  5. Plat complet avec salade, miel, menthe (usage)

Format: WebP, ratio 1:1 pour carousel, 800x800px
Lazy loading: toutes sauf image 1
Zoom: pinch-to-zoom mobile, hover-zoom desktop
```

### Fiche produit

```html
<!-- Structure semantique -->
<div class="product-info" itemscope itemtype="https://schema.org/Product">
  <p class="product-origin">Fromage artisanal de Chypre</p>
  <h2 class="product-name" itemprop="name">Chaloumi Traditionnel</h2>

  <div class="product-tagline">
    100% lait de chevre | Sans presure animale | Fabrique a la main
  </div>

  <div class="product-rating">
    [5 etoiles] 4.8/5 (127 avis) -- lien vers section temoignages
  </div>

  <div class="product-description" itemprop="description">
    "Notre Chaloumi est fabrique chaque semaine dans un petit atelier
    familial des montagnes du Troodos, a Chypre. Contrairement au
    halloumi industriel, il est fait exclusivement au lait de chevre
    frais, ce qui lui donne cette texture unique : croustillant quand
    on le grille, delicieusement fondant a l'interieur."
  </div>

  <div class="product-highlights">
    <ul>
      <li>[icone feuille] Lait de chevre frais, jamais pasteurise a outrance</li>
      <li>[icone main] Moule et sale a la main</li>
      <li>[icone zero] Sans conservateurs, sans additifs</li>
      <li>[icone certification] Recette familiale depuis 3 generations</li>
    </ul>
  </div>
</div>
```

### Selecteur de format et prix

```
Options (radio buttons visuels, type carte):

[  DECOUVERTE  ]    [  BEST-SELLER  ]     [  GOURMAND  ]
   250g x 1            250g x 3              250g x 6
   24,90 EUR           59,90 EUR             99,90 EUR
                       (-20%)                (-33%)
                       [badge "Populaire"]

Prix affiche: taille 32px, font-weight 700
Prix barre si promo: affiche a cote, couleur grise, text-decoration line-through
Badge promo: position absolute top-right de la carte, rotation -3deg
```

### CTA Produit

```
Bouton principal: "Ajouter au panier -- [prix]"
Taille: pleine largeur section info
Style: identique au hero CTA
Animation: micro-animation au hover (scale 1.02, shadow increase)

Sous le bouton:
"Livraison gratuite des 49EUR | Expedition sous 24h"
[icone cadenas] "Paiement 100% securise"
```

### Informations nutritionnelles (accordeon)

```
Toggle "Valeurs nutritionnelles" (ferme par defaut)
Contenu: tableau standard pour 100g
  - Energie: ~310 kcal
  - Proteines: ~22g
  - Matieres grasses: ~24g
  - Glucides: ~2g
  - Sel: ~2.5g
  - Calcium: ~500mg
```

---

## 4. SECTION HISTOIRE

### Objectif
Creer une connexion emotionnelle, justifier le positionnement premium.

### Layout

```
Desktop: 2 colonnes alternees (texte/image puis image/texte)
Mobile: stack vertical avec images pleine largeur
Background: blanc
Padding: 80px vertical
```

### Contenu

```
Bloc 1 -- L'origine
  Image: Paysage montagnes du Troodos, chevrerie
  Titre: "Ne dans les montagnes du Troodos"
  Texte: "Au coeur de Chypre, a 1200m d'altitude, la famille [Nom]
          eleve ses chevres en liberte depuis 1987. Chaque matin,
          le lait frais est collecte a la main pour devenir
          votre Chaloumi."

Bloc 2 -- Le savoir-faire
  Image: Artisan travaillant le fromage, mains dans le caille
  Titre: "Un savoir-faire transmis de pere en fils"
  Texte: "Pas de machines, pas de raccourcis. Le caillage, le filage,
          le salage -- chaque etape est realisee a la main, comme
          il y a 40 ans. C'est cette patience qui donne au Chaloumi
          sa texture incomparable."

Bloc 3 -- La difference
  Image: Comparaison visuelle chaloumi artisanal vs halloumi industriel
  Titre: "Pourquoi c'est different du halloumi de supermarche"
  Texte: "Le halloumi industriel melange lait de vache et conservateurs.
          Notre Chaloumi est 100% chevre, sans additifs, avec un gout
          plus delicat et une texture qui grille parfaitement."
```

### Element interactif (optionnel)

```
Mini-timeline horizontale scrollable:
  1987 -> Premiere fabrication
  1995 -> Reconnaissance locale
  2010 -> Premiere exportation EU
  2024 -> Lancement D2C France
```

---

## 5. SECTION DEGUSTATION

### Objectif
Projeter le visiteur dans l'usage, donner envie de cuisiner avec.

### Layout

```
Titre centre: "Comment deguster votre Chaloumi"
Sous-titre: "3 facons de le savourer"
Grid: 3 colonnes desktop, carousel mobile
Background: var(--bg-cream)
Padding: 80px vertical
```

### 3 cartes recette

```
Carte 1 -- Grille (classique)
  Image: Chaloumi grille dore, traces de grillage
  Titre: "Grille a la poele"
  Description: "2 minutes de chaque cote a feu vif,
                sans matiere grasse. Le Chaloumi ne fond pas,
                il devient croustillant et dore."
  Temps: "5 min"
  Difficulte: "Facile"

Carte 2 -- En salade
  Image: Salade mediterraneenne coloree avec chaloumi
  Titre: "Salade mediterraneenne"
  Description: "Sur un lit de roquette, tomates cerises,
                concombre, olives noires. Un filet d'huile
                d'olive et du miel de thym."
  Temps: "10 min"
  Difficulte: "Facile"

Carte 3 -- Au barbecue
  Image: Brochettes chaloumi + legumes grilles
  Titre: "Brochettes au BBQ"
  Description: "Alternez Chaloumi, poivrons, courgettes
                et oignons rouges. Badigeonnez d'huile au
                romarin. L'incontournable de l'ete."
  Temps: "15 min"
  Difficulte: "Facile"
```

### CTA section

```
"Telecharger notre livret de 10 recettes (gratuit)"
-> Capture email (prenom + email) pour lead nurturing
Format: popup modale ou inline form
Lead magnet: PDF recettes Chaloumi
```

---

## 6. SECTION TEMOIGNAGES

### Objectif
Preuve sociale, lever les doutes, confirmer la decision.

### Layout

```
Background: blanc
Titre: "Ils ont goute, ils sont conquis"
Sous-titre: note globale "[etoiles] 4.8/5 sur 127 avis"
Carousel: 1 temoignage visible mobile, 3 desktop
Navigation: fleches + dots + swipe
Auto-scroll: 5s entre chaque, pause au hover/touch
Padding: 80px vertical
```

### Format des temoignages

```
Structure par carte:
  - 5 etoiles (toujours visibles en haut)
  - Texte du temoignage (max 120 caracteres, guillemets)
  - Photo (avatar 48px rond, ou initiales)
  - Prenom + ville
  - Badge "Achat verifie" [icone check vert]

Exemples:

  [5 etoiles]
  "J'ai enfin retrouve le gout du vrai halloumi
   que j'avais mange a Chypre. Rien a voir avec
   celui du supermarche !"
  -- Sophie M., Lyon
  [Achat verifie]

  [5 etoiles]
  "La qualite est dingue. On l'a grille au BBQ
   ce weekend, mes amis m'en redemandent deja."
  -- Thomas R., Bordeaux
  [Achat verifie]

  [5 etoiles]
  "Livraison rapide, emballage impeccable avec
   le pack froid. Le fromage etait parfait."
  -- Amira K., Paris
  [Achat verifie]

  [4 etoiles]
  "Tres bon, un peu sale pour mon gout mais
   la texture grille est incroyable."
  -- Marc D., Nantes
  [Achat verifie]

  [5 etoiles]
  "Vegetarienne depuis 10 ans, c'est mon
   nouveau produit prefere. Sans presure animale
   en plus !"
  -- Claire B., Toulouse
  [Achat verifie]
```

### Widget avis (integration)

```
Source recommandee: Judge.me (Shopify) ou Trustpilot widget
Afficher: note globale + nombre d'avis + lien "Voir tous les avis"
UGC: prevoir espace pour photos client (post-lancement)
```

---

## 7. SECTION FAQ

### Objectif
Lever les dernieres objections avant commande.

### Layout

```
Background: var(--bg-cream)
Titre: "Vos questions frequentes"
Format: accordeon (un seul ouvert a la fois)
Padding: 80px vertical
Schema: FAQPage JSON-LD (cf. section SEO)
```

### 10 Questions / Reponses

```
Q1: "Quelle est la difference entre le Chaloumi et le halloumi ?"
R1: "Le halloumi classique est un melange de lait de brebis, chevre
     et souvent vache. Notre Chaloumi est fait exclusivement au lait
     de chevre frais, ce qui lui donne un gout plus delicat et une
     texture plus fine. Il est aussi fabrique artisanalement, sans
     aucun additif ni conservateur."

Q2: "Comment conserver le Chaloumi ?"
R2: "Au refrigerateur entre 2 et 6 degres C, dans son emballage d'origine ou
     dans un recipient hermetique. Il se conserve 30 jours apres
     reception. Vous pouvez aussi le congeler jusqu'a 3 mois --
     decongelez-le au refrigerateur 24h avant degustation."

Q3: "Le Chaloumi convient-il aux vegetariens ?"
R3: "Oui. Notre Chaloumi est fabrique sans presure animale.
     Il utilise une presure microbienne vegetale, ce qui le rend
     adapte a un regime vegetarien."

Q4: "Contient-il du lactose ?"
R4: "Le Chaloumi contient du lactose, comme tous les fromages frais.
     Cependant, le lait de chevre est naturellement plus facile a
     digerer que le lait de vache. Si vous etes intolerant au lactose,
     consultez votre medecin."

Q5: "Comment est assuree la chaine du froid pendant la livraison ?"
R5: "Chaque commande est expediee dans un emballage isotherme avec
     des packs de gel refrigerant. La livraison est effectuee en 48h
     par Chronofresh (transporteur specialise alimentaire frais).
     La temperature reste entre 0 et 4 degres C pendant tout le trajet."

Q6: "Quels sont les delais de livraison ?"
R6: "Les commandes passees avant 14h (lundi au jeudi) sont expediees
     le jour meme. Comptez 48h pour la livraison en France
     metropolitaine. Les commandes du vendredi sont expediees le
     lundi suivant."

Q7: "Que faire si mon colis arrive endommage ou si le produit ne me convient pas ?"
R7: "Nous offrons une garantie satisfait ou rembourse sous 14 jours.
     Si votre produit arrive endommage ou ne correspond pas a vos
     attentes, contactez-nous avec une photo et nous vous renvoyons
     un colis ou vous remboursons integralement."

Q8: "Le Chaloumi est-il adapte aux enfants ?"
R8: "Oui, a partir de 3 ans le Chaloumi peut etre donne aux enfants.
     C'est une excellente source de proteines et de calcium. Pour
     les plus petits, coupez-le en petits morceaux et servez-le
     tiede (pas brulant apres grillage)."

Q9: "Peut-on le cuire au four ou au barbecue ?"
R9: "Absolument. Le Chaloumi a la particularite de ne pas fondre a
     la chaleur. Vous pouvez le griller a la poele, au four (200 degres C,
     8-10 min), au barbecue, ou meme le paner et le frire. C'est
     un fromage polyvalent pour la cuisine."

Q10: "Proposez-vous des abonnements ou des livraisons regulieres ?"
R10: "Oui. Apres votre premiere commande, vous pouvez souscrire a
      un abonnement mensuel avec 15% de reduction. Vous choisissez la
      frequence (toutes les 2, 3 ou 4 semaines) et pouvez suspendre
      ou annuler a tout moment."
```

---

## 8. SECTION COMMANDE

### Objectif
Conversion finale, recapitulatif offre, derniere reassurance.

### Layout

```
Background: var(--color-brand-dark), texte blanc
Padding: 100px vertical
Contenu centre, max-width 640px
```

### Contenu

```
Titre: "Pret a decouvrir le vrai gout de Chypre ?"
Sous-titre: "Commandez aujourd'hui, recevez dans 48h"

Selecteur rapide (3 options visuelles):
  [DECOUVERTE]  [BEST-SELLER]  [GOURMAND]
  Meme selecteur que section produit, etat synchronise

CTA: "Commander maintenant -- [prix]"
Taille: 56px hauteur, max-width 400px
Couleur: var(--color-accent) (terracotta)

Micro-copy:
"Paiement securise par Stripe | CB, Apple Pay, Google Pay"

Badges de reassurance (icones blanches):
  [camion] Livraison 48h     [flocon] Chaine du froid
  [cadenas] Paiement securise [fleche retour] Retour 14j
```

---

## 9. FOOTER

### Layout

```
Background: #1a1a1a
Texte: rgba(255,255,255,0.7)
Padding: 48px vertical
Grid: 4 colonnes desktop, 2 colonnes tablet, stack mobile
```

### Contenu

```
Colonne 1 -- Marque
  Logo CHALOUMI (blanc)
  "Fromage artisanal de Chypre"
  Liens reseaux sociaux: Instagram, Facebook, TikTok

Colonne 2 -- Boutique
  Nos produits
  Coffret decouverte
  Abonnement
  Carte cadeau

Colonne 3 -- Informations
  Notre histoire
  FAQ
  Blog / Recettes
  Contact

Colonne 4 -- Legal
  Conditions generales de vente
  Politique de confidentialite
  Mentions legales
  Politique de cookies

Barre basse:
  "(c) 2026 CHALOUMI - Tous droits reserves"
  "Fromage artisanal fabrique a Chypre"
  Moyens de paiement: [icones CB Visa MC Amex ApplePay GPay]
```

---

## 10. CONVERSION OPTIMIZATION

### 10.1 Social Proof

```
Placements:
  - Hero: "Deja 2000+ gourmands conquis" (compteur)
  - Produit: Note 4.8/5 (127 avis) avec lien
  - Temoignages: Section dediee
  - Pre-footer: Logos presse si disponibles (Le Fooding, etc.)
  - Notification toast (optionnel): "Sophie de Lyon vient de commander"
    -> Apparait toutes les 45s, affiche des prenoms/villes aleatoires
    -> Disparait apres 4s, position bottom-left
    -> Desactiver si CTR < 0.5% apres 2 semaines
```

### 10.2 Urgence et Rarete

```
Elements:
  1. Badge produit: "Production limitee -- [X] coffrets restants cette semaine"
     -> Stock reel ou timer de production (batch hebdomadaire)
     -> Couleur: rouge doux, icone flamme

  2. Bandeau saisonnier (ete):
     "Saison BBQ : -15% sur le coffret Gourmand avec le code ETE26"

  3. Compteur expedition:
     "Commandez avant 14h, expedition aujourd'hui"
     -> Timer en temps reel jusqu'a 14h00 (lun-jeu)
     -> Apres 14h: "Commandez maintenant, expedition demain matin"
```

### 10.3 Reassurance Logistique

```
Elements recurrents (au moins 3 occurrences sur la page):
  - Chaine du froid: icone flocon + "Chronofresh 0-4 degres C"
  - Delai: icone camion + "Livraison 48h France metro"
  - Emballage: icone boite + "Emballage isotherme premium"
  - Retour: icone fleche + "Satisfait ou rembourse 14 jours"
  - Paiement: icone cadenas + "Paiement securise Stripe"

Placement:
  - Sous chaque CTA principal
  - Bande de reassurance horizontale entre sections
  - Dans le checkout sidebar
```

### 10.4 Trust Badges

```
Badges a afficher:
  - "Paiement securise" (Stripe/SSL)
  - "Livraison refrigeree" (Chronofresh)
  - "Satisfait ou rembourse"
  - "Artisanal certifie"
  - Logos moyens de paiement (Visa, MC, Amex, Apple Pay, Google Pay)

Format: icones minimalistes, 24px, couleur grise, hover couleur primaire
Position: pied de page de chaque section avec CTA
```

### 10.5 Micro-copy Boutons

```
CTA primaire (Commander):
  Texte: "Commander maintenant -- [prix]"
  Sous-texte: "Livraison offerte des 49EUR"

CTA secondaire (Ajouter au panier):
  Texte: "Ajouter au panier"
  Sous-texte: "[icone cadenas] Paiement 100% securise"

CTA tertiaire (En savoir plus):
  Texte: "Decouvrir notre histoire"
  Style: lien underline, pas de bouton
```

---

## 11. SPECIFICATIONS TECHNIQUES

### 11.1 Performance -- Core Web Vitals

```
Cibles (mobile):
  LCP (Largest Contentful Paint): < 2.5s
  FID (First Input Delay): < 100ms
  CLS (Cumulative Layout Shift): < 0.1
  INP (Interaction to Next Paint): < 200ms
  TTFB (Time to First Byte): < 600ms

Strategies:
  - Images: WebP, srcset responsive, lazy loading sauf hero
  - Fonts: preload 2 polices max, font-display: swap
  - CSS: critical CSS inline dans <head>, reste async
  - JS: defer tout sauf theme manager, bundle < 50KB
  - Video hero: poster image immediate, video en lazy
  - CDN: Cloudflare ou Shopify CDN
  - Preconnect: fonts.googleapis.com, cdn.shopify.com, js.stripe.com
```

### 11.2 SEO On-Page

```html
<!-- Title -->
<title>Chaloumi Artisanal de Chypre | 100% Chevre | Livraison 48h France</title>

<!-- Meta Description -->
<meta name="description" content="Decouvrez le Chaloumi, fromage artisanal
100% lait de chevre fabrique a Chypre. Grille, il devient croustillant dehors
et fondant dedans. Livraison chaine du froid 48h en France. Des 24,90EUR.">

<!-- H1 (unique, dans le hero) -->
<h1>Le vrai fromage de Chypre, grille a la perfection</h1>

<!-- Open Graph -->
<meta property="og:title" content="Chaloumi - Le fromage de Chypre artisanal">
<meta property="og:description" content="100% chevre, fabrique a la main.
Croustillant grille, fondant dedans. Livraison 48h chaine du froid.">
<meta property="og:image" content="[URL image hero 1200x630]">
<meta property="og:type" content="product">

<!-- Schema.org Product -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "Chaloumi Traditionnel",
  "description": "Fromage artisanal 100% lait de chevre de Chypre",
  "image": "[URL images]",
  "brand": {
    "@type": "Brand",
    "name": "CHALOUMI"
  },
  "offers": {
    "@type": "AggregateOffer",
    "lowPrice": "24.90",
    "highPrice": "99.90",
    "priceCurrency": "EUR",
    "availability": "https://schema.org/InStock",
    "seller": {
      "@type": "Organization",
      "name": "CHALOUMI"
    }
  },
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.8",
    "reviewCount": "127"
  }
}
</script>

<!-- Schema.org FAQPage -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Quelle est la difference entre le Chaloumi et le halloumi ?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Le halloumi classique est un melange de lait de brebis,
                 chevre et souvent vache. Notre Chaloumi est fait
                 exclusivement au lait de chevre frais..."
      }
    }
    // ... 9 autres questions
  ]
}
</script>
```

### 11.3 Tracking et Analytics

```javascript
// --- META PIXEL ---
// Installer via <head> ou Google Tag Manager
// Events a configurer:

fbq('track', 'PageView');                    // Auto sur chaque page
fbq('track', 'ViewContent', {               // Section produit vue (scroll)
  content_name: 'Chaloumi Traditionnel',
  content_type: 'product',
  content_ids: ['CHAL-250'],
  value: 24.90,
  currency: 'EUR'
});
fbq('track', 'AddToCart', {                  // Clic "Ajouter au panier"
  content_name: 'Chaloumi Traditionnel',
  content_type: 'product',
  content_ids: ['CHAL-250'],
  value: 24.90,
  currency: 'EUR'
});
fbq('track', 'InitiateCheckout', {           // Debut checkout
  content_type: 'product',
  num_items: 1,
  value: 24.90,
  currency: 'EUR'
});
fbq('track', 'Purchase', {                   // Confirmation commande
  content_type: 'product',
  content_ids: ['CHAL-250'],
  value: 24.90,
  currency: 'EUR'
});
fbq('track', 'Lead');                        // Soumission email (recettes)


// --- TIKTOK PIXEL ---
ttq.track('ViewContent', { ... });
ttq.track('AddToCart', { ... });
ttq.track('PlaceAnOrder', { ... });
ttq.track('CompletePayment', { ... });


// --- GA4 (Google Analytics 4) ---
// Events recommandes e-commerce:
gtag('event', 'view_item', { ... });
gtag('event', 'add_to_cart', { ... });
gtag('event', 'begin_checkout', { ... });
gtag('event', 'purchase', { ... });

// Events custom:
gtag('event', 'scroll_to_section', {
  section_name: 'hero|product|story|recipes|testimonials|faq|order'
});
gtag('event', 'cta_click', {
  cta_location: 'hero|product|order|sticky_nav',
  cta_text: 'Commander maintenant'
});
gtag('event', 'faq_toggle', {
  question_index: 1-10,
  question_text: '...'
});
gtag('event', 'recipe_download', {
  method: 'email_capture'
});
gtag('event', 'variant_select', {
  variant: 'decouverte|bestseller|gourmand'
});
```

### 11.4 A/B Tests Recommandes (par priorite)

```
Test 1 -- HERO HEADLINE (priorite haute)
  Objectif: CTR sur CTA principal
  Variantes: A (authenticite) vs B (sensoriel) vs C (exclusivite)
  Trafic: 33/33/33
  Duree: 2 semaines ou 1000 visiteurs par variante
  Outil: Google Optimize ou Shopify native

Test 2 -- FORMAT CTA (priorite haute)
  Objectif: taux d'ajout au panier
  A: "Decouvrir nos coffrets" (actuel)
  B: "Commander mon Chaloumi"
  C: "Gouter le Chaloumi -- 24,90EUR"
  Duree: 2 semaines

Test 3 -- PRIX AFFICHE (priorite moyenne)
  Objectif: panier moyen
  A: Prix unitaire 24,90EUR mis en avant
  B: Prix pack 59,90EUR (-20%) mis en avant (pre-selectionne)

Test 4 -- SOCIAL PROOF TOAST (priorite moyenne)
  Objectif: taux de conversion global
  A: Avec notification "X vient de commander"
  B: Sans notification

Test 5 -- VIDEO vs PHOTO HERO (priorite basse)
  Objectif: LCP + taux de scroll + conversion
  A: Photo statique optimisee
  B: Video 6s autoplay
  Note: mesurer impact Core Web Vitals
```

---

## 12. CHECKOUT FLOW

### 12.1 Tunnel de Conversion

```
ETAPE 1 -- PANIER (slide-over panel, pas de page separee)
  - Recap produit: image thumb, nom, quantite, prix
  - Selecteur quantite (+/-)
  - Code promo: champ inline
  - Sous-total + estimation livraison
  - CTA: "Passer commande"
  - "Livraison offerte des 49EUR" si panier < 49EUR
    (afficher combien il manque: "Plus que X EUR pour la livraison offerte")

ETAPE 2 -- INFORMATIONS
  - Email (pre-rempli si cookie)
  - Prenom, Nom
  - Adresse complete (autocomplete Google Places)
  - Telephone (pour le livreur Chronofresh)
  - Case a cocher: "M'inscrire a la newsletter" (pre-cochee)
  - CTA: "Continuer vers le paiement"

ETAPE 3 -- PAIEMENT
  - Stripe Elements ou Shopify Payments
  - Methodes: CB (Visa, MC, Amex), Apple Pay, Google Pay
  - Recapitulatif commande visible en sidebar
  - CTA: "Payer [montant] EUR"
  - Reassurance sous le bouton:
    [icone cadenas] "Vos donnees sont protegees par chiffrement SSL 256 bits"

ETAPE 4 -- CONFIRMATION
  - Message: "Merci [prenom] ! Votre Chaloumi arrive dans 48h"
  - Recap commande + numero de suivi
  - CTA secondaire: "Parrainer un ami (-10%)"
  - Partage social: "Dites-le a vos amis" (boutons partage)
  - Pixel Purchase + GA4 purchase fires ici
```

### 12.2 Upsell / Cross-sell

```
Moment 1 -- Dans le panier (slide-over)
  "Completez votre commande :"
  - Huile d'olive extra vierge de Chypre (+8,90EUR)
  - Miel de thym du Troodos (+9,90EUR)
  - Menthe sechee artisanale (+4,90EUR)
  Format: mini-cartes horizontales avec bouton "Ajouter"

Moment 2 -- Pre-checkout (popup/modal)
  Si panier = 1x Decouverte:
  "Passez au coffret Best-Seller et economisez 20%"
  Comparaison: 3x24.90 = 74.70 vs 59.90EUR (-20%)
  CTA: "Oui, je prends le coffret" / "Non merci"

Moment 3 -- Post-purchase (page confirmation)
  "Abonnez-vous et economisez 15% chaque mois"
  Description: livraison automatique, modifiable, annulable
  CTA: "S'abonner a [prix reduit]/mois"

Moment 4 -- Email post-achat (J+5)
  "Votre Chaloumi vous a plu ? Revenez avec -10%"
  Code unique, valable 7 jours
```

### 12.3 Strategie Abandon de Panier

```
Couche 1 -- Exit Intent Popup (web)
  Declencheur: souris vers la barre d'adresse (desktop)
               ou back button (mobile)
  Contenu: "Attendez ! Votre Chaloumi va vous manquer"
  Offre: "-10% avec le code REVIENS10"
  CTA: "Appliquer ma reduction"
  Timer: code valable 30 minutes (creer urgence)
  Frequence: 1 seule fois par session

Couche 2 -- Email abandon panier (si email capture)
  Email 1 (H+1): "Vous avez oublie quelque chose..."
    Rappel produit, pas de reduction
  Email 2 (H+24): "Votre Chaloumi vous attend toujours"
    Ajout de 2 temoignages
  Email 3 (H+48): "Derniere chance : -10% sur votre panier"
    Code promo 48h

Couche 3 -- Retargeting Meta/TikTok
  Audience: visiteurs ayant ajoute au panier sans acheter
  Delai: J+1 a J+7
  Creative: video/photo produit + "Votre Chaloumi vous attend"
  Budget: 10-15% du budget media
```

---

## 13. DESIGN SYSTEM

### 13.1 Couleurs

```css
:root {
  /* Brand */
  --color-brand-primary: #2C5F2D;     /* Vert olive profond */
  --color-brand-secondary: #97BC62;   /* Vert feuille clair */
  --color-brand-dark: #1B3A1C;        /* Vert nuit */

  /* Accent */
  --color-accent: #C8553D;            /* Terracotta (CTAs) */
  --color-accent-hover: #A8432F;      /* Terracotta fonce */
  --color-accent-light: #F4E0DB;      /* Terracotta pastel */

  /* Neutrals */
  --color-white: #FFFFFF;
  --color-cream: #FBF7F0;             /* Fond sections alternees */
  --color-gray-100: #F5F5F5;
  --color-gray-300: #D4D4D4;
  --color-gray-500: #737373;
  --color-gray-700: #404040;
  --color-gray-900: #171717;

  /* Semantic */
  --color-success: #22C55E;
  --color-warning: #F59E0B;
  --color-error: #EF4444;
  --color-info: #3B82F6;

  /* Backgrounds */
  --bg-primary: var(--color-white);
  --bg-cream: var(--color-cream);
  --bg-dark: var(--color-brand-dark);

  /* Text */
  --text-primary: var(--color-gray-900);
  --text-secondary: var(--color-gray-500);
  --text-on-dark: rgba(255, 255, 255, 0.9);
  --text-on-accent: #FFFFFF;
}
```

### 13.2 Typographie

```css
:root {
  /* Font Families */
  --font-heading: 'DM Serif Display', Georgia, serif;
  --font-body: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
  --font-accent: 'DM Sans', sans-serif;

  /* Scale */
  --text-xs: 0.75rem;      /* 12px */
  --text-sm: 0.875rem;     /* 14px */
  --text-base: 1rem;       /* 16px */
  --text-lg: 1.125rem;     /* 18px */
  --text-xl: 1.25rem;      /* 20px */
  --text-2xl: 1.5rem;      /* 24px */
  --text-3xl: 2rem;        /* 32px */
  --text-4xl: 2.5rem;      /* 40px */
  --text-5xl: 3rem;        /* 48px - hero mobile */
  --text-6xl: 3.75rem;     /* 60px - hero desktop */

  /* Line Heights */
  --leading-tight: 1.15;
  --leading-snug: 1.3;
  --leading-normal: 1.6;
  --leading-relaxed: 1.75;
}

/* Usage */
h1 { font-family: var(--font-heading); font-size: var(--text-5xl); line-height: var(--leading-tight); }
h2 { font-family: var(--font-heading); font-size: var(--text-3xl); line-height: var(--leading-snug); }
h3 { font-family: var(--font-heading); font-size: var(--text-2xl); line-height: var(--leading-snug); }
body { font-family: var(--font-body); font-size: var(--text-base); line-height: var(--leading-normal); }
.btn { font-family: var(--font-accent); font-weight: 600; letter-spacing: 0.02em; }

@media (min-width: 768px) {
  h1 { font-size: var(--text-6xl); }
  h2 { font-size: var(--text-4xl); }
}
```

### 13.3 Spacing

```css
:root {
  --space-1: 0.25rem;    /* 4px */
  --space-2: 0.5rem;     /* 8px */
  --space-3: 0.75rem;    /* 12px */
  --space-4: 1rem;       /* 16px */
  --space-6: 1.5rem;     /* 24px */
  --space-8: 2rem;       /* 32px */
  --space-10: 2.5rem;    /* 40px */
  --space-12: 3rem;      /* 48px */
  --space-16: 4rem;      /* 64px */
  --space-20: 5rem;      /* 80px */
  --space-24: 6rem;      /* 96px */

  /* Section padding */
  --section-py-mobile: var(--space-12);   /* 48px */
  --section-py-desktop: var(--space-20);  /* 80px */

  /* Container */
  --container-px: var(--space-4);         /* 16px */
  --container-max: 1200px;

  /* Border radius */
  --radius-sm: 4px;
  --radius-md: 8px;
  --radius-lg: 12px;
  --radius-xl: 16px;
  --radius-full: 9999px;
}
```

### 13.4 Composants Cles

```css
/* --- CTA Button Primary --- */
.btn-primary {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: var(--space-2);
  padding: var(--space-3) var(--space-8);
  min-height: 48px;
  background: var(--color-accent);
  color: var(--text-on-accent);
  font-family: var(--font-accent);
  font-size: var(--text-lg);
  font-weight: 600;
  border: none;
  border-radius: var(--radius-lg);
  cursor: pointer;
  transition: all 0.2s ease;
  text-decoration: none;
}

.btn-primary:hover {
  background: var(--color-accent-hover);
  transform: translateY(-1px);
  box-shadow: 0 4px 12px rgba(200, 85, 61, 0.3);
}

.btn-primary:active {
  transform: translateY(0);
}

@media (max-width: 767px) {
  .btn-primary {
    width: 100%;
    min-height: 52px;
    font-size: var(--text-base);
  }
}

/* --- Product Card (format selector) --- */
.format-card {
  border: 2px solid var(--color-gray-300);
  border-radius: var(--radius-lg);
  padding: var(--space-6);
  text-align: center;
  cursor: pointer;
  transition: all 0.2s ease;
  position: relative;
}

.format-card.selected {
  border-color: var(--color-accent);
  background: var(--color-accent-light);
}

.format-card .badge {
  position: absolute;
  top: -12px;
  right: 12px;
  background: var(--color-accent);
  color: white;
  padding: 4px 12px;
  border-radius: var(--radius-full);
  font-size: var(--text-xs);
  font-weight: 700;
  text-transform: uppercase;
}

/* --- FAQ Accordion --- */
.faq-item {
  border-bottom: 1px solid var(--color-gray-300);
}

.faq-question {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: var(--space-6) 0;
  font-family: var(--font-accent);
  font-size: var(--text-lg);
  font-weight: 600;
  cursor: pointer;
  background: none;
  border: none;
  width: 100%;
  text-align: left;
}

.faq-answer {
  overflow: hidden;
  max-height: 0;
  transition: max-height 0.3s ease, padding 0.3s ease;
  padding: 0 0;
}

.faq-item.open .faq-answer {
  max-height: 300px;
  padding: 0 0 var(--space-6) 0;
}

/* --- Testimonial Card --- */
.testimonial-card {
  background: var(--bg-primary);
  border: 1px solid var(--color-gray-100);
  border-radius: var(--radius-lg);
  padding: var(--space-8);
  box-shadow: 0 1px 3px rgba(0,0,0,0.06);
}

/* --- Reassurance Badge --- */
.reassurance-badge {
  display: inline-flex;
  align-items: center;
  gap: var(--space-2);
  font-size: var(--text-sm);
  color: var(--text-secondary);
}

.reassurance-badge svg {
  width: 20px;
  height: 20px;
  color: var(--color-brand-primary);
}

/* --- Toast Notification (Social Proof) --- */
.social-toast {
  position: fixed;
  bottom: 24px;
  left: 24px;
  background: white;
  border: 1px solid var(--color-gray-100);
  border-radius: var(--radius-lg);
  padding: var(--space-3) var(--space-4);
  box-shadow: 0 8px 24px rgba(0,0,0,0.12);
  display: flex;
  align-items: center;
  gap: var(--space-3);
  z-index: 900;
  transform: translateY(120%);
  transition: transform 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}

.social-toast.visible {
  transform: translateY(0);
}
```

### 13.5 Theme Toggle (Light/Dark/System)

Pas pertinent pour ce projet e-commerce food. La palette de couleurs chaudes et les photos produit necessitent un fond clair pour maximiser l'appetence visuelle. Un mode sombre degraderait la perception du produit et la conversion.

Recommandation : pas de theme toggle sur cette landing page. Reserve pour les sites de contenu/SaaS.

---

## 14. IMPLEMENTATION NOTES

### 14.1 Stack Recommande

```
Option A -- Shopify (recommandee pour le MVP)
  Theme: Dawn (gratuit) ou Taste (premium)
  Avantages: checkout natif, gestion stock, Chronofresh integration
  Apps: Judge.me (avis), Klaviyo (email), ReConvert (upsell)
  Delai: 1-2 semaines
  Budget: ~30EUR/mois + apps

Option B -- Next.js + Stripe (si besoin de controle total)
  Framework: Next.js 14+ App Router
  Paiement: Stripe Checkout
  Hosting: Vercel
  CMS: Sanity ou Contentful (pour contenu editable)
  Email: Resend ou SendGrid
  Delai: 3-4 semaines
  Budget: ~0EUR hosting (Vercel free tier) + Stripe 1.4%+0.25EUR/tx
```

### 14.2 Structure de fichiers (si Next.js)

```
app/
  layout.tsx            # Root layout, fonts, metadata
  page.tsx              # Landing page (toutes les sections)
  checkout/
    page.tsx            # Flow de paiement
  confirmation/
    page.tsx            # Post-achat
  api/
    checkout/route.ts   # Stripe session creation
    webhook/route.ts    # Stripe webhook handler
components/
  Hero.tsx
  ProductSection.tsx
  StorySection.tsx
  RecipeCards.tsx
  Testimonials.tsx
  FAQ.tsx
  OrderSection.tsx
  Footer.tsx
  ui/
    Button.tsx
    Badge.tsx
    FormatSelector.tsx
    ReassuranceBadge.tsx
    SocialToast.tsx
    StickyNav.tsx
    ReassuranceBanner.tsx
lib/
  stripe.ts             # Stripe config
  tracking.ts           # GA4 + Meta + TikTok helpers
  constants.ts          # Product data, prices, FAQ content
styles/
  globals.css           # Design system variables + reset
  components.css        # Component styles
public/
  images/               # Optimized WebP product images
  fonts/                # Self-hosted fonts
```

### 14.3 Checklist Pre-Lancement

```
[ ] Core Web Vitals passes (LCP < 2.5s, CLS < 0.1)
[ ] Responsive OK: 375px, 414px, 768px, 1024px, 1440px
[ ] Meta Pixel fires: PageView, ViewContent, AddToCart, Purchase
[ ] TikTok Pixel fires: ViewContent, AddToCart, CompletePayment
[ ] GA4 e-commerce events operational
[ ] Schema Product + FAQPage valide (schema.org validator)
[ ] Open Graph preview correct (Facebook debugger)
[ ] Images toutes en WebP, lazy loaded sauf hero
[ ] Fonts preloaded, FOIT/FOUT gere
[ ] SSL actif (https)
[ ] CGV, mentions legales, politique confidentialite publiees
[ ] RGPD: banner cookies + consentement tracking
[ ] Checkout flow teste end-to-end (Stripe test mode)
[ ] Email abandon panier configure (Klaviyo ou custom)
[ ] Exit intent popup operationnel
[ ] 404 page custom
[ ] Redirections si besoin
[ ] Accessibilite: contraste, navigation clavier, alt text images
[ ] Vitesse mobile testee sur 3G (Lighthouse)
```

### 14.4 KPIs a Suivre

```
Semaine 1-2 (validation):
  - Taux de rebond hero < 60%
  - Scroll depth moyen > 50% page
  - CTR CTA hero > 5%
  - Taux d'ajout au panier > 8%

Mois 1 (optimisation):
  - Taux de conversion global > 2.5%
  - Panier moyen > 50EUR
  - Taux d'abandon panier < 70%
  - Taux de recuperation abandon > 10%
  - ROAS Meta Ads > 3x
  - CAC < 15EUR
```

---

**Document prepare par : ArchitectUX -- APEX DIGITAL**
**Version : 1.0**
**Date : Mai 2026**
**Statut : Pret pour implementation**

Ce document contient toutes les specifications necessaires pour qu'un
developpeur puisse implementer la landing page sans ambiguite. Chaque
section inclut le layout, le contenu, les interactions et les
specifications techniques associees.
