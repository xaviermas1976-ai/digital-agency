# CHALOUMI -- Meta Ads Setup Guide Complet
## APEX DIGITAL | Budget 4 500 EUR / 6 mois

---

## 1. PRE-REQUIS TECHNIQUES

### Pixel & Tracking
- [ ] Installer Meta Pixel sur la landing page (GTM recommande)
- [ ] Configurer les evenements standards : PageView, ViewContent, AddToCart, InitiateCheckout, Purchase
- [ ] Implementer la Conversions API (CAPI) via le plugin e-commerce ou GTM server-side
- [ ] Passer la valeur du panier dans l'evenement Purchase
- [ ] Tester avec Meta Pixel Helper (extension Chrome)
- [ ] Configurer le domaine verifie dans Business Manager

### Comptes
- [ ] Business Manager cree et verifie
- [ ] Page Facebook "Chaloumi France" creee
- [ ] Compte Instagram @chaloumi.fr connecte
- [ ] Catalogue produits cree (optionnel pour Collection Ads)
- [ ] Moyen de paiement configure

### UTM
Format standard pour tous les liens :
```
?utm_source=meta&utm_medium=paid&utm_campaign={campaign_name}&utm_content={ad_name}
```

---

## 2. STRUCTURE DU COMPTE

```
COMPTE : Chaloumi France
|
+-- [CBO] AWARENESS (M1-M2) -- 550-400 EUR/mois
|   +-- Foodies Interet Large
|   +-- BBQ & Grillades
|   +-- Consom'acteurs Bio/Local
|
+-- [CBO] CONSIDERATION (M2-M4) -- 150-300 EUR/mois
|   +-- Video Viewers 50%+ (Custom)
|   +-- Page/Insta Engagers 30j
|   +-- LP Visitors non-acheteurs
|
+-- [ABO] CONVERSION (M3-M6) -- 50-350 EUR/mois
|   +-- Retargeting LP Visitors 7j
|   +-- Retargeting ATC 14j
|   +-- Retargeting Video Viewers 75%+ 14j
|   +-- Lookalike 1% Acheteurs
|
+-- [ABO] RETENTION (M4+) -- 50-150 EUR/mois
    +-- Acheteurs existants (cross-sell/reorder)
```

---

## 3. AUDIENCES DETAILLEES

### Phase 1 -- Prospecting (froides)

**Ad Set : Foodies Interet Large**
- Age : 25-45
- Geo : France metropolitaine
- Interets : gastronomie, cuisine maison, fromage, degustation, Marmiton, 750g
- Taille estimee : 3-5M
- Exclusion : acheteurs, LP visitors 7j

**Ad Set : BBQ & Grillades**
- Age : 25-50
- Geo : France
- Interets : barbecue, plancha, Weber, grillades, cuisine exterieure
- Taille : 1.5-2.5M

**Ad Set : Consom'acteurs Bio/Local**
- Age : 25-45
- Geo : France
- Interets : bio, circuit court, artisanat alimentaire, AMAP, La Ruche qui dit Oui
- Taille : 1-2M

### Phase 2 -- Tiedes

**Video Viewers 50%+** : Custom Audience, 30 jours
**Engagers Insta/FB** : Page + profil, 30 jours
**LP Visitors** : Pixel PageView, 30 jours, excl. acheteurs

### Phase 3 -- Chaudes

**LP Visitors recents** : Pixel page produit, 7 jours
**Add-to-Cart** : Pixel ATC sans achat, 14 jours
**Video Viewers 75%+** : Custom Audience, 14 jours
**LAL Acheteurs** : Lookalike 1% Purchase (des M3+)

---

## 4. BUDGET MENSUEL

| Mois | Awareness | Consideration | Conversion | Retention | TOTAL |
|------|----------:|-------------:|----------:|---------:|------:|
| M1 | 550 | 150 | 50 | 0 | **750** |
| M2 | 400 | 250 | 100 | 0 | **750** |
| M3 | 250 | 300 | 200 | 0 | **750** |
| M4 | 200 | 250 | 250 | 50 | **750** |
| M5 | 150 | 200 | 300 | 100 | **750** |
| M6 | 100 | 150 | 350 | 150 | **750** |
| **TOTAL** | **1 650** | **1 300** | **1 250** | **300** | **4 500** |

---

## 5. REGLES D'OPTIMISATION

| Condition | Action |
|-----------|--------|
| CTR < 0.8% apres 1000 impressions | Couper l'ad |
| CPA > 20 EUR apres 50 EUR depenses | Couper l'ad set |
| CPA < 10 EUR sur 3 jours consecutifs | +20% budget (max +20%/3j) |
| Frequence > 2.5 sur audience froide | Refresh creative |
| ROAS retargeting > 2x awareness | +15% vers retargeting |
| CPM +30% sem/sem meme audience | Elargir ou pause 7j |
| M3 si 50+ purchases | Lancer campagne Advantage+ |

---

## 6. FORMATS PAR PHASE

| Phase | Format principal | Secondaire |
|-------|-----------------|------------|
| Awareness | Reels 9:16 (15-30s) | Carrousel 3-5 images |
| Consideration | Reels UGC degustation | Stories + CTA |
| Conversion | Carrousel produit + prix | Collection Ad |
| Retention | Stories offre fidelite | Reels recette |

---

## 7. KPIs CIBLES

| KPI | Awareness | Consideration | Conversion | Retention |
|-----|----------|--------------|-----------|----------|
| CPM | 6-9 EUR | 8-12 EUR | 12-18 EUR | 10-15 EUR |
| CPC | 0.30-0.50 | 0.40-0.70 | 0.80-1.50 | 0.50-1.00 |
| CTR | 1.5-2.5% | 1.8-3.0% | 2.0-4.0% | 2.5-4.0% |
| CPA | N/A | N/A | 10-15 EUR | 8-12 EUR |
| ROAS | N/A | N/A | 1.5-2.2x | 2.0-3.0x |
