# LINKTREE / LINK IN BIO — Contenu

---

## OPTION 1 : Linktree (gratuit)

### URL
```
linktr.ee/chaloumifrance
```

### Theme
- Fond : #FBF7F0 (creme)
- Boutons : #2C5F2D (olive) avec texte blanc
- Police : Inter
- Avatar : Logo Chaloumi

### Liens (dans cet ordre)

#### 1. Commander
```
Texte : Commander le Chaloumi
Emoji : (aucun)
URL : https://chaloumi.fr/boutique?utm_source=linktree&utm_medium=social&utm_campaign=bio_link&utm_content=commander
Icone : panier
```

#### 2. Offre decouverte
```
Texte : Pack Decouverte — 14.90 EUR
URL : https://chaloumi.fr/boutique?product=decouverte&utm_source=linktree&utm_medium=social&utm_campaign=bio_link&utm_content=pack_decouverte
Icone : cadeau
Priorite : highlight (activer le badge "popular")
```

#### 3. Recettes
```
Texte : Nos recettes au Chaloumi
URL : https://chaloumi.fr/recettes?utm_source=linktree&utm_medium=social&utm_campaign=bio_link&utm_content=recettes
Icone : livre de recettes
```

#### 4. Lead magnet
```
Texte : 5 recettes gratuites (PDF)
URL : https://chaloumi.fr/?utm_source=linktree&utm_medium=social&utm_campaign=lead_magnet_pdf#newsletter
Icone : telechargement
Priorite : highlight
```

#### 5. Notre histoire
```
Texte : Notre ferme familiale a Chypre
URL : https://chaloumi.fr/?utm_source=linktree&utm_medium=social&utm_campaign=bio_link&utm_content=histoire#histoire
Icone : coeur
```

#### 6. TikTok
```
Texte : Suivez-nous sur TikTok
URL : https://tiktok.com/@chaloumi.fr
Icone : TikTok
```

---

## OPTION 2 : Page native /liens sur chaloumi.fr

Si on prefere garder tout le trafic sur le domaine :

### URL
```
https://chaloumi.fr/liens?utm_source=[plateforme]&utm_medium=social&utm_campaign=bio_link
```

### Avantages
- Pixel tracking natif (pas de redirection)
- SEO juice reste sur le domaine
- Design 100% brand
- Pas de dependance outil tiers

### Implementation
Creer une page `/liens` dans le site Next.js avec :
- Logo en haut
- Liste de boutons olive #2C5F2D sur fond creme
- Memes liens que le Linktree ci-dessus
- Footer avec icones sociales

---

## CONFIGURATION PAR PLATEFORME

### Instagram
```
Bio link : linktr.ee/chaloumifrance
```
OU
```
Bio link : https://chaloumi.fr/liens?utm_source=instagram&utm_medium=social&utm_campaign=bio_link
```

### TikTok
```
Bio link : https://chaloumi.fr/?utm_source=tiktok&utm_medium=social&utm_campaign=bio_link
```
(TikTok n'a qu'un seul lien — pointer direct vers le site, pas Linktree)

### Pinterest
```
Website : https://chaloumi.fr/?utm_source=pinterest&utm_medium=social&utm_campaign=profile
```
(Pinterest a le lien site web natif — pas besoin de Linktree)

### Facebook
```
Website : https://chaloumi.fr/?utm_source=facebook&utm_medium=social&utm_campaign=page
CTA button : https://chaloumi.fr/boutique?utm_source=facebook&utm_medium=social&utm_campaign=cta_button
```
