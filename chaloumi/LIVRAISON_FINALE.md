# CHALOUMI — Livraison Finale Projet Complet
## APEX DIGITAL | Mai 2026

---

## RESUME EXECUTIF

Projet D2C fromage artisanal de Chypre vers la France.
Budget : 10 000 EUR. Objectif : 200 clients en 6 mois.

**Tout est livre. Pret a deployer.**

---

## 1. SITE WEB (Next.js 16 — pret production)

### Dossier : `chaloumi-site/`

**Pages**
| Route | Description | Status |
|-------|-------------|--------|
| `/` | Landing page — 10 composants, 18 images reelles | OK |
| `/recettes` | 6 recettes completes (ingredients + etapes) | OK |
| `/liens` | Link-in-bio natif (remplace Linktree) | OK |
| `/cgv` | Conditions generales de vente | OK |
| `/confidentialite` | Politique de confidentialite RGPD | OK |
| `/mentions-legales` | Mentions legales | OK |
| `/commande/confirmation` | Page post-achat Stripe | OK |
| `/api/checkout` | API Stripe Checkout (5 produits) | OK |
| `/api/webhook` | Webhook Stripe (payment events) | OK |

**Composants (12)**
- ReassuranceBanner, Navbar, Hero, ProductSection, StorySection
- TastingSection, TestimonialsSection, FaqSection, OrderSection
- Footer, TrackingPixels, CookieBanner

**Integration**
- Stripe Checkout (5 produits : 14.90 / 26.90 / 39.90 / 59.90 / 99.90 EUR)
- Livraison auto (gratuite des 49 EUR, sinon 5.90 EUR Chronofresh)
- Meta Pixel + TikTok Pixel + Pinterest Tag + GA4 (env variables)
- Cookie banner RGPD
- Schema.org JSON-LD (Product + FAQPage)
- SEO meta tags + Open Graph
- Liens sociaux reels dans le footer (IG, FB, TikTok, Pinterest)

**Assets**
- 18 images Unsplash (hero, produits, recettes, ferme, paysages)
- 3 logos SVG (couleur, blanc, favicon)
- 5 highlight covers SVG (Instagram Stories)

**Pour deployer :**
```bash
# 1. Remplir .env.local avec les vrais IDs
# 2. Deploy sur Vercel
cd chaloumi-site
vercel --prod
```

---

## 2. STRATEGIE (8 documents)

### Dossier : `chaloumi/`

| # | Fichier | Contenu |
|---|---------|---------|
| 00 | `00_MASTER_PLAN.md` | Plan strategique 6 mois complet |
| 02 | `02_brand_identity.md` | Identite visuelle, ton, palette, typo |
| 03 | `03_paid_social_strategy.md` | Strategie ads Meta + TikTok |
| 04 | `04_ad_creatives.md` | Specs creatives publicitaires |
| 05 | `05_social_content_strategy.md` | Strategie contenu 4 plateformes |
| 06 | `06_landing_page_specs.md` | Specs fonctionnelles site |
| 07 | `07_email_growth_strategy.md` | Sequences email + growth loops |
| 08 | `08_financial_model.md` | Modele financier + projections |
| — | `COMPTE_RENDU_COMPLET.md` | Rapport executif consolide |

---

## 3. EMAIL MARKETING (16 templates Brevo)

### Dossier : `chaloumi/email-templates/`

| Template | Usage |
|----------|-------|
| 00 | Base template HTML |
| 01-03 | Sequence bienvenue (J0, J1, J3) |
| 04-06 | Post-achat (J1 confirmation, J3 recettes, J7 avis) |
| 07-09 | Abandon panier (J1, J3, J7) |
| 10-11 | Pre-lancement (teaser, invitation) |
| 12-13 | Fidelisation (points, exclusivite) |
| 14 | Reactivation J90 |
| 15 | Newsletter bimensuelle (template Brevo) |
| 16 | Exemple newsletter Juin 2026 |

---

## 4. CONTENU SOCIAL (package complet)

### Dossier : `chaloumi/social-content/`

| Type | Quantite | Details |
|------|----------|---------|
| Posts Instagram | 30 | Scripts reels, slides carrousels, briefs photos |
| Scripts TikTok | 15 | Tables timecodes (Sec/Visuel/Son/Texte) |
| Pins Pinterest | 16 | Descriptions SEO 250+ chars, alt text |
| Stories Instagram | 3 semaines | Prompts quotidiens |
| Calendrier editorial | 12 semaines | Jour/plateforme/format/fichier |
| Sets hashtags | 8 | Pre-configures par theme |
| Kit influenceurs | 1 | 3 templates outreach + 9 cibles + brief |

---

## 5. PUBLICITE (Meta + TikTok)

### Dossier : `chaloumi/meta-ads/`

| Fichier | Contenu |
|---------|---------|
| `00_META_ADS_SETUP.md` | 4 campagnes (Awareness/Consideration/Conversion/Retention) |
| `01_ad_copies.md` | 5 textes principaux × 2 versions + 5 titres + matrices A/B |
| `02_tiktok_ads_setup.md` | 3 campagnes TikTok (Discovery/Conversion/Spark) |
| `03_retargeting_sequences.md` | 4 etapes Meta + 2 etapes TikTok |
| `04_growth_loops.md` | 5 programmes (referral, lead magnet, UGC, abo, SEO) |

**Budget total ads : 4 500 EUR / 6 mois**

---

## 6. SETUP RESEAUX SOCIAUX (pret copier-coller)

### Dossier : `chaloumi/social-setup/`

| # | Fichier | Plateforme |
|---|---------|-----------|
| 00 | `LAUNCH_CHECKLIST.md` | Checklist master 4 plateformes |
| 01 | `instagram_setup.md` | Instagram (@chaloumi.fr) |
| 02 | `tiktok_setup.md` | TikTok (@chaloumi.fr) |
| 03 | `pinterest_setup.md` | Pinterest (Chaloumi France) |
| 04 | `facebook_setup.md` | Facebook Page + Messenger + Commerce |
| 05 | `utm_tracking.md` | Tous les liens UTM prets |
| 06 | `analytics_dashboard.md` | Pixels + GA4 + KPIs + Metricool |
| 07 | `linktree_content.md` | Link-in-bio (Linktree ou natif) |

---

## 7. ASSETS VISUELS

### Dossier : `chaloumi-site/public/`

**Images (18)**
- hero-halloumi.jpg
- product-halloumi.jpg, product-halloumi-2.jpg
- recipe-grilled.jpg, recipe-salad.jpg, recipe-bbq.jpg
- story-artisan.jpg, goats-field.jpg, cheese-market.jpg
- village-mediterranean.jpg, village-greek.jpg, village-coast.jpg
- goats-herd.jpg, goats-rocky.jpg
- (+ 4 autres paysages/ferme)

**Logos (3)**
- logo.svg (vert sur transparent)
- logo-white.svg (blanc sur transparent)
- favicon.svg

**Highlight Covers (5)**
- highlight-recettes.svg (poele)
- highlight-ferme.svg (chevre)
- highlight-comment.svg (colis)
- highlight-avis.svg (etoile)
- highlight-ugc.svg (coeur)

---

## CHECKLIST DEPLOIEMENT

### Immediat (Jour 1)
- [ ] Deployer le site sur Vercel (`vercel --prod`)
- [ ] Configurer le domaine chaloumi.fr → Vercel
- [ ] Remplir `.env.local` avec les vrais IDs (Stripe, Pixels, GA4)
- [ ] Tester un achat Stripe en mode test
- [ ] Configurer le webhook Stripe

### Semaine 1
- [ ] Creer les comptes sociaux (IG, TikTok, Pinterest, FB)
- [ ] Copier-coller les bios/descriptions depuis les setup docs
- [ ] Publier les 9 premiers posts Instagram
- [ ] Publier les 3 premiers TikTok
- [ ] Creer les 5 boards Pinterest + 15 pins
- [ ] Installer Metricool et connecter les comptes
- [ ] Configurer Brevo et importer les templates email

### Semaine 2
- [ ] Lancer la campagne Awareness Meta (CBO)
- [ ] Publier TikTok 4 et 5
- [ ] Commencer le calendrier editorial S2
- [ ] Envoyer les premiers DMs influenceurs
- [ ] Activer les Rich Pins Pinterest

### Mois 1
- [ ] Analyser les premieres metriques (Metricool)
- [ ] Identifier les Spark Ads candidats sur TikTok
- [ ] Lancer la campagne Consideration Meta
- [ ] Premier rapport hebdomadaire

---

## BUDGET TOTAL PROJET

| Poste | Budget |
|-------|--------|
| Site web (dev + hebergement) | ~0 EUR (Vercel free tier) |
| Meta Ads (6 mois) | 4 500 EUR |
| TikTok Ads (6 mois) | 1 500 EUR |
| Influenceurs | 2 000 EUR |
| Email marketing (Brevo) | ~0 EUR (free tier 300 emails/jour) |
| Pinterest Ads (optionnel) | 500 EUR |
| Outils (Metricool, Canva) | 500 EUR |
| Reserve / imprevu | 1 000 EUR |
| **TOTAL** | **10 000 EUR** |

---

## CONTACTS

- Site : chaloumi.fr
- Email : contact@chaloumi.fr
- Instagram : @chaloumi.fr
- TikTok : @chaloumi.fr
- Pinterest : @chaloumifrance
- Facebook : Chaloumi - Fromage artisanal de Chypre

---

*Projet execute par APEX DIGITAL — Mai 2026*
