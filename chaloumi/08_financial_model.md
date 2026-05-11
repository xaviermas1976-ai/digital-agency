# CHALOUMI D2C France --- Modele Financier Complet

**Version** : 1.0 | **Auteur** : Morgan, Financial Analyst -- APEX DIGITAL | **Date** : 2026-05-08
**Objet** : Modelisation financiere pour le lancement D2C du Chaloumi artisanal (Chypre vers France)
**Budget** : 10 000 EUR sur 6 mois | **Objectif** : 200 clients pour declencher levee de fonds

---

## 0. HYPOTHESES CLES

> Toute projection repose sur ces hypotheses. Les remettre en question avant de valider les chiffres.

| # | Hypothese | Valeur retenue | Source / Justification |
|---|-----------|---------------|----------------------|
| H1 | Prix unitaire moyen | 21.50 EUR (250g) | Milieu de fourchette 18-25 EUR, positionnement premium artisanal |
| H2 | Panier moyen | 37.50 EUR | 2 unites (43 EUR) + livraison (8 EUR) = 51 EUR brut, mais mix 1 unite/2 unites donne ~37.50 EUR net |
| H3 | COGS unitaire | 8.00 EUR/unite | Production + emballage Chypre |
| H4 | Logistique/commande | 12.00 EUR | Expedition froid Chypre-France (DHL/Chronopost) |
| H5 | COGS total/commande | 28.00 EUR | 2 x 8 EUR (produit) + 12 EUR (logistique) pour panier moyen 2 unites |
| H6 | Marge brute/commande | 9.50 EUR | 37.50 - 28.00 = 9.50 EUR (25.3%) |
| H7 | CPM Meta Ads (France, food) | 8-15 EUR | Benchmark Meta France food/beverage 2025-2026 |
| H8 | CTR landing page | 1.5-3.0% | Benchmark D2C food premium |
| H9 | Taux conversion site | 2.0-3.5% | Benchmark e-commerce food artisanal |
| H10 | Taux reachat annuel | 2x a 4x/an | Hypothese fromage = produit consommable, reachat plausible |
| H11 | Courbe apprentissage ads | -15%/mois sur CPA apres M2 | Optimisation audiences + creatives avec data |
| H12 | Split budget paid | Meta 70% / TikTok 30% | Meta plus mature pour conversion food, TikTok pour awareness |

**Avertissement marge** : La marge brute reelle de 25.3% est inferieure a la fourchette 40-50% indiquee dans le brief. Cet ecart vient du cout logistique froid international (12 EUR/commande). Ce point est critique pour la viabilite du modele et sera traite dans l'analyse de sensibilite.

---

## 1. BUDGET ALLOCATION DETAILLE (Mois par Mois)

### 1.1 Vue synthetique

| Poste | M1 | M2 | M3 | M4 | M5 | M6 | TOTAL |
|-------|-----|-----|-----|-----|-----|-----|-------|
| **PHASE 1 -- Setup** | | | | | | | **2 000 EUR** |
| Landing page (dev + design) | 1 200 | -- | -- | -- | -- | -- | 1 200 |
| Shooting photo/video | 800 | -- | -- | -- | -- | -- | 800 |
| **PHASE 2 -- Paid Social** | | | | | | | **6 000 EUR** |
| Meta Ads | -- | 700 | 800 | 900 | 900 | 900 | 4 200 |
| TikTok Ads | -- | 300 | 350 | 400 | 400 | 350 | 1 800 |
| **PHASE 3 -- Retargeting + Email** | | | | | | | **2 000 EUR** |
| Retargeting (Meta + TikTok) | -- | -- | 200 | 300 | 300 | 300 | 1 100 |
| Email marketing (outil + setup) | -- | 100 | 100 | 100 | 150 | 150 | 600 |
| Contingence (3%) | -- | -- | -- | -- | -- | 300 | 300 |
| **TOTAL MENSUEL** | **2 000** | **1 100** | **1 450** | **1 700** | **1 750** | **2 000** | **10 000** |

### 1.2 Justification de la montee en charge

- **M1** : Zero depense publicitaire. Le setup (landing + contenu) est un prerequis non-negociable. Lancer des ads sur une page mediocre = bruler du budget.
- **M2** : Budget ads reduit (1 000 EUR) car phase de test. On depense pour apprendre, pas pour scaler.
- **M3-M4** : Montee progressive. Les donnees de M2 permettent d'optimiser audiences et creatives.
- **M5-M6** : Budget stable. L'optimisation vient de la baisse du CPA, pas de l'augmentation du budget.

### 1.3 Split detaille Phase 2 -- Paid Social

| Canal | Budget total | Objectif principal | Format privilegie |
|-------|-------------|-------------------|-------------------|
| Meta (Instagram + Facebook) | 4 200 EUR (70%) | Conversion directe | Reels 15s, carousel produit, UGC |
| TikTok | 1 800 EUR (30%) | Awareness + trafic | Videos 15-30s, food content, decouverte |

---

## 2. PROJECTIONS ACQUISITION -- 3 SCENARIOS

### 2.1 Hypotheses par scenario

| Metrique | Conservateur | Realiste | Optimiste |
|----------|-------------|----------|-----------|
| CPM Meta | 14.00 EUR | 11.00 EUR | 8.00 EUR |
| CPM TikTok | 6.00 EUR | 4.50 EUR | 3.00 EUR |
| CTR Meta | 1.2% | 2.0% | 3.0% |
| CTR TikTok | 0.8% | 1.5% | 2.5% |
| CVR site (depuis Meta) | 1.5% | 2.5% | 3.5% |
| CVR site (depuis TikTok) | 0.8% | 1.5% | 2.5% |
| CPA Meta initial (M2) | 77.78 EUR | 35.20 EUR | 15.24 EUR |
| CPA TikTok initial (M2) | 125.00 EUR | 40.00 EUR | 16.00 EUR |
| Amelioration CPA/mois (M3+) | -10% | -15% | -20% |
| Clients email/retargeting | 5% du total | 12% du total | 20% du total |

> **Formule CPA** : CPA = CPM / (CTR x CVR x 1000)
> Exemple realiste Meta : 11.00 / (0.020 x 0.025 x 1000) = 11.00 / 0.05 = 220.00 EUR ... Non.
> Recalcul : CPM = cout pour 1000 impressions. CPC = CPM / (CTR x 10). CPA = CPC / CVR.
> Meta realiste : CPC = 11.00 / (0.020 x 1000) = 0.55 EUR. CPA = 0.55 / 0.025 = 22.00 EUR.

### 2.2 CPA recalcule correctement

| Canal | Scenario | CPM | CTR | CPC | CVR | CPA |
|-------|----------|-----|-----|-----|-----|-----|
| **Meta** | Conservateur | 14.00 | 1.2% | 1.17 | 1.5% | 77.78 |
| **Meta** | Realiste | 11.00 | 2.0% | 0.55 | 2.5% | 22.00 |
| **Meta** | Optimiste | 8.00 | 3.0% | 0.27 | 3.5% | 7.62 |
| **TikTok** | Conservateur | 6.00 | 0.8% | 0.75 | 0.8% | 93.75 |
| **TikTok** | Realiste | 4.50 | 1.5% | 0.30 | 1.5% | 20.00 |
| **TikTok** | Optimiste | 3.00 | 2.5% | 0.12 | 2.5% | 4.80 |

### 2.3 Acquisition mensuelle -- Scenario REALISTE (detail)

> Courbe d'apprentissage : CPA diminue de 15%/mois a partir de M3 grace a l'optimisation.

| Mois | Budget Meta | CPA Meta | Clients Meta | Budget TikTok | CPA TikTok | Clients TikTok | Retarg/Email | **Total clients** |
|------|------------|----------|-------------|--------------|-----------|----------------|-------------|-----------------|
| M1 | 0 | -- | 0 | 0 | -- | 0 | 0 | **0** |
| M2 | 700 | 22.00 | 31 | 300 | 20.00 | 15 | 2 | **48** |
| M3 | 800 | 18.70 | 42 | 350 | 17.00 | 20 | 8 | **70** |
| M4 | 900 | 15.90 | 56 | 400 | 14.45 | 27 | 12 | **95** |
| M5 | 900 | 13.52 | 66 | 400 | 12.28 | 32 | 15 | **113** |
| M6 | 900 | 11.49 | 78 | 350 | 10.44 | 33 | 18 | **129** |
| **TOTAL** | **4 200** | | **273** | **1 800** | | **127** | **55** | **455** |

### 2.4 Acquisition mensuelle -- Scenario CONSERVATEUR

| Mois | Budget Meta | CPA Meta | Clients Meta | Budget TikTok | CPA TikTok | Clients TikTok | Retarg/Email | **Total clients** |
|------|------------|----------|-------------|--------------|-----------|----------------|-------------|-----------------|
| M1 | 0 | -- | 0 | 0 | -- | 0 | 0 | **0** |
| M2 | 700 | 77.78 | 9 | 300 | 93.75 | 3 | 0 | **12** |
| M3 | 800 | 70.00 | 11 | 350 | 84.38 | 4 | 1 | **16** |
| M4 | 900 | 63.00 | 14 | 400 | 75.94 | 5 | 1 | **20** |
| M5 | 900 | 56.70 | 15 | 400 | 68.34 | 5 | 2 | **22** |
| M6 | 900 | 51.03 | 17 | 350 | 61.51 | 5 | 2 | **24** |
| **TOTAL** | **4 200** | | **66** | **1 800** | | **22** | **6** | **94** |

### 2.5 Acquisition mensuelle -- Scenario OPTIMISTE

| Mois | Budget Meta | CPA Meta | Clients Meta | Budget TikTok | CPA TikTok | Clients TikTok | Retarg/Email | **Total clients** |
|------|------------|----------|-------------|--------------|-----------|----------------|-------------|-----------------|
| M1 | 0 | -- | 0 | 0 | -- | 0 | 0 | **0** |
| M2 | 700 | 7.62 | 91 | 300 | 4.80 | 62 | 15 | **168** |
| M3 | 800 | 6.10 | 131 | 350 | 3.84 | 91 | 30 | **252** |
| M4 | 900 | 4.88 | 184 | 400 | 3.07 | 130 | 45 | **359** |
| M5 | 900 | 3.90 | 230 | 400 | 2.46 | 162 | 55 | **447** |
| M6 | 900 | 3.12 | 288 | 350 | 1.97 | 177 | 65 | **530** |
| **TOTAL** | **4 200** | | **924** | **1 800** | | **622** | **210** | **1 756** |

### 2.6 Synthese des 3 scenarios

| Metrique | Conservateur | Realiste | Optimiste |
|----------|-------------|----------|-----------|
| **Total clients 6 mois** | 94 | 455 | 1 756 |
| **Objectif 200 atteint ?** | NON (47%) | OUI -- M4 | OUI -- M2 |
| **CPA moyen blended** | 85.11 EUR | 17.58 EUR | 4.56 EUR |
| **Cout/client (tout budget)** | 106.38 EUR | 21.98 EUR | 5.69 EUR |

> **Verdict** : Le scenario realiste depasse l'objectif de 200 clients. Le scenario conservateur ne l'atteint pas -- il faudrait alors pivoter (voir section Risques). L'objectif de 200 clients est atteignable entre M3 et M5 dans le scenario realiste.

---

## 3. ANALYSE P&L SIMPLIFIEE (Scenario Realiste)

### 3.1 Hypotheses P&L

| Element | Valeur | Note |
|---------|--------|------|
| Panier moyen | 37.50 EUR | Mix 1.75 unites/commande |
| COGS/commande | 28.00 EUR | 2 x 8 EUR (produit) + 12 EUR (logistique) |
| Marge brute/commande | 9.50 EUR | 25.3% |
| Frais plateforme (Stripe/Shopify) | 3.5% du CA | ~1.31 EUR/commande |
| Marge nette/commande avant marketing | 8.19 EUR | 21.8% |

### 3.2 P&L mensuel -- Scenario Realiste

| Ligne | M1 | M2 | M3 | M4 | M5 | M6 | **TOTAL** |
|-------|-----|-----|-----|-----|-----|-----|----------|
| **Commandes** | 0 | 48 | 70 | 95 | 113 | 129 | **455** |
| **Revenu** | 0 | 1 800 | 2 625 | 3 563 | 4 238 | 4 838 | **17 063** |
| COGS produit | 0 | (768) | (1 120) | (1 520) | (1 808) | (2 064) | (7 280) |
| COGS logistique | 0 | (576) | (840) | (1 140) | (1 356) | (1 548) | (5 460) |
| **Marge brute** | **0** | **456** | **665** | **903** | **1 074** | **1 226** | **4 323** |
| Marge brute % | -- | 25.3% | 25.3% | 25.3% | 25.3% | 25.3% | **25.3%** |
| Frais plateforme (3.5%) | 0 | (63) | (92) | (125) | (148) | (169) | (597) |
| **Marge apres plateforme** | **0** | **393** | **573** | **778** | **926** | **1 057** | **3 726** |
| | | | | | | | |
| Depenses marketing | (2 000) | (1 100) | (1 450) | (1 700) | (1 750) | (2 000) | (10 000) |
| | | | | | | | |
| **Resultat net** | **(2 000)** | **(707)** | **(877)** | **(922)** | **(824)** | **(943)** | **(6 274)** |
| Resultat cumule | (2 000) | (2 707) | (3 584) | (4 507) | (5 331) | (6 274) | |

### 3.3 P&L -- Scenario Conservateur

| Ligne | M1 | M2 | M3 | M4 | M5 | M6 | **TOTAL** |
|-------|-----|-----|-----|-----|-----|-----|----------|
| Commandes | 0 | 12 | 16 | 20 | 22 | 24 | **94** |
| Revenu | 0 | 450 | 600 | 750 | 825 | 900 | **3 525** |
| COGS total | 0 | (336) | (448) | (560) | (616) | (672) | (2 632) |
| Marge brute | 0 | 114 | 152 | 190 | 209 | 228 | **893** |
| Frais plateforme | 0 | (16) | (21) | (26) | (29) | (32) | (123) |
| Depenses marketing | (2 000) | (1 100) | (1 450) | (1 700) | (1 750) | (2 000) | (10 000) |
| **Resultat net** | **(2 000)** | **(1 002)** | **(1 319)** | **(1 536)** | **(1 570)** | **(1 804)** | **(9 230)** |

### 3.4 P&L -- Scenario Optimiste

| Ligne | M1 | M2 | M3 | M4 | M5 | M6 | **TOTAL** |
|-------|-----|-----|-----|-----|-----|-----|----------|
| Commandes | 0 | 168 | 252 | 359 | 447 | 530 | **1 756** |
| Revenu | 0 | 6 300 | 9 450 | 13 463 | 16 763 | 19 875 | **65 850** |
| COGS total | 0 | (4 704) | (7 056) | (10 052) | (12 516) | (14 840) | (49 168) |
| Marge brute | 0 | 1 596 | 2 394 | 3 411 | 4 247 | 5 035 | **16 682** |
| Frais plateforme | 0 | (221) | (331) | (471) | (587) | (696) | (2 305) |
| Depenses marketing | (2 000) | (1 100) | (1 450) | (1 700) | (1 750) | (2 000) | (10 000) |
| **Resultat net** | **(2 000)** | **275** | **613** | **1 240** | **1 910** | **2 339** | **4 377** |

### 3.5 Point mort (Breakeven)

| Scenario | Breakeven mensuel atteint ? | Mois | Commandes/mois au breakeven |
|----------|---------------------------|------|-----------------------------|
| Conservateur | NON | Jamais sur 6 mois | Besoin ~244 commandes/mois a M6 |
| Realiste | NON | Jamais sur 6 mois | Besoin ~244 commandes/mois a M6 |
| Optimiste | OUI | M2 | ~168 commandes (budget M2 = 1 100 EUR) |

> **Breakeven marketing mensuel** = Depense marketing mensuelle / Marge nette par commande
> A M6 (budget 2 000 EUR) : 2 000 / 8.19 = **244 commandes/mois** necessaires.
> Cela correspond a 244 x 37.50 = **9 150 EUR/mois de CA**.

> **Conclusion** : Sur 6 mois avec 10 000 EUR de budget, cette campagne est structurellement deficitaire. C'est normal et attendu. L'objectif n'est pas la rentabilite -- c'est l'acquisition de 200 clients pour debloquer la levee de fonds.

---

## 4. METRIQUES CLES

### 4.1 CAC (Customer Acquisition Cost)

| Scenario | CAC (marketing only) | CAC (all-in, budget total / clients) |
|----------|---------------------|--------------------------------------|
| Conservateur | 85.11 EUR | 106.38 EUR |
| Realiste | 17.58 EUR | 21.98 EUR |
| Optimiste | 4.56 EUR | 5.69 EUR |

> **Note** : Le CAC "all-in" inclut le setup (landing page, shooting) reparti sur tous les clients.

### 4.2 LTV (Lifetime Value) -- Scenarios de reachat

| Frequence reachat | Reachats/an | Panier moyen | Duree relation | LTV brut | LTV net (apres COGS) |
|-------------------|------------|-------------|----------------|----------|---------------------|
| Faible | 2x/an | 37.50 EUR | 2 ans | 150.00 EUR | 32.76 EUR |
| Moyen | 3x/an | 37.50 EUR | 2 ans | 225.00 EUR | 49.14 EUR |
| Eleve | 4x/an | 37.50 EUR | 2 ans | 300.00 EUR | 65.52 EUR |

> **Calcul LTV net** : (Panier moyen - COGS - frais plateforme) x reachats/an x duree = marge nette cumulee
> Exemple moyen : 8.19 EUR x 3 x 2 = 49.14 EUR

### 4.3 Ratio LTV:CAC

| Scenario acquisition | LTV (reachat 3x/an) | CAC all-in | Ratio LTV:CAC | Verdict |
|---------------------|---------------------|-----------|--------------|---------|
| Conservateur | 49.14 EUR | 106.38 EUR | **0.46:1** | ECHEC -- non viable |
| Realiste | 49.14 EUR | 21.98 EUR | **2.24:1** | ACCEPTABLE -- a ameliorer |
| Optimiste | 49.14 EUR | 5.69 EUR | **8.63:1** | EXCELLENT |

> **Seuil investisseur** : LTV:CAC > 3:1. Le scenario realiste est a 2.24:1, insuffisant pour seduire un investisseur sans amelioration de la marge ou du reachat.
>
> **Pour atteindre 3:1 en scenario realiste** :
> - Option A : Augmenter LTV a 65.94 EUR --> reachat 4x/an OU panier moyen a 50 EUR
> - Option B : Baisser CAC a 16.38 EUR --> ameliorer le CPA de 25%
> - Option C : Reduire COGS logistique a 8 EUR/commande (entrepot France)

### 4.4 ROAS (Return on Ad Spend)

| Scenario | Depense ads (Phase 2+3) | Revenu genere | ROAS |
|----------|------------------------|--------------|------|
| Conservateur | 8 000 EUR | 3 525 EUR | **0.44x** |
| Realiste | 8 000 EUR | 17 063 EUR | **2.13x** |
| Optimiste | 8 000 EUR | 65 850 EUR | **8.23x** |

> **Benchmark** : ROAS > 2x est acceptable pour un lancement D2C. Le scenario realiste est a la limite. Le ROAS s'ameliore mecaniquement quand le CPA baisse.

### 4.5 Payback Period

| Scenario | CAC all-in | Marge nette/commande | Commandes pour payback | Payback (si reachat 3x/an) |
|----------|-----------|---------------------|----------------------|---------------------------|
| Conservateur | 106.38 EUR | 8.19 EUR | 13 commandes | **4.3 ans** |
| Realiste | 21.98 EUR | 8.19 EUR | 2.7 commandes | **10.8 mois** |
| Optimiste | 5.69 EUR | 8.19 EUR | 0.7 commande | **Immediat (1ere commande)** |

---

## 5. SCENARIO LEVEE DE FONDS

### 5.1 Metriques a presenter aux investisseurs si 200 clients atteints

| Metrique | Valeur (scenario realiste) | Benchmark D2C food |
|----------|---------------------------|-------------------|
| Clients acquis | 200+ en 4 mois | Proof of demand |
| CAC | 22 EUR | Acceptable < 30 EUR food D2C |
| Panier moyen | 37.50 EUR | Premium positioning confirme |
| Taux conversion | 2.5% | Inline avec D2C food |
| Taux reachat M3-M6 (estime) | 15-25% | A mesurer -- crucial |
| NPS (a collecter) | Cible > 50 | A mesurer |
| Marge brute | 25.3% | FAIBLE -- point d'attention |

### 5.2 Path to 50 000 EUR/mois de revenu

| Jalon | Commandes/mois | Clients actifs requis | Budget marketing mensuel | CPA cible |
|-------|---------------|----------------------|-------------------------|-----------|
| Phase actuelle (M6) | 129 | 455 cumules | 2 000 EUR | 17.58 EUR |
| Palier 1 : 10k EUR/mois | 267 | ~600 | 3 500 EUR | 15.00 EUR |
| Palier 2 : 25k EUR/mois | 667 | ~1 500 | 7 500 EUR | 12.00 EUR |
| **Palier 3 : 50k EUR/mois** | **1 333** | **~3 000** | **13 000 EUR** | **10.00 EUR** |

> **Hypotheses de scaling** :
> - CPA continue de baisser avec le volume (economies d'echelle, meilleur contenu, lookalike audiences)
> - Reachat genere ~30% du revenu sans cout d'acquisition additionnel
> - Passage a un entrepot France reduit la logistique de 12 EUR a 6-8 EUR/commande

### 5.3 Unit Economics a l'echelle (1 333 commandes/mois)

| Element | Actuel | A l'echelle | Delta |
|---------|--------|-------------|-------|
| Panier moyen | 37.50 EUR | 42.00 EUR | +12% (upsell, packs) |
| COGS produit/commande | 16.00 EUR | 13.00 EUR | -19% (volume Chypre) |
| Logistique/commande | 12.00 EUR | 7.00 EUR | -42% (entrepot France) |
| Marge brute | 25.3% | 52.4% | +27 pts |
| CAC | 22.00 EUR | 10.00 EUR | -55% |
| LTV:CAC (3x/an reachat) | 2.24:1 | 6.6:1 | x2.9 |

> **Point critique** : La viabilite du modele a l'echelle depend de l'installation d'un entrepot/stock en France. Sans cela, la logistique froid Chypre-France reste un goulot d'etranglement sur la marge.

### 5.4 Besoins en levee de fonds estimes

| Poste | Montant | Justification |
|-------|---------|---------------|
| Stock initial (3 mois) | 40 000 EUR | 1 333 cmd/mois x 2 unites x 8 EUR x 3 mois (couverture) |
| Entrepot froid France (setup) | 15 000 EUR | Location + equipement froid 6 mois |
| Marketing scaling (6 mois) | 78 000 EUR | 13 000 EUR/mois x 6 mois |
| Tech (site e-commerce, CRM) | 12 000 EUR | Shopify Plus ou custom, email automation |
| Fond de roulement | 25 000 EUR | BFR 45 jours |
| Equipe (1 ops + 1 marketing) | 80 000 EUR | 6 mois de salaires charges |
| **Total levee cible** | **250 000 EUR** | Runway 12 mois jusqu'a rentabilite |

---

## 6. RISQUES FINANCIERS

### 6.1 Top 5 Risques

| # | Risque | Probabilite | Impact | Mitigation |
|---|--------|------------|--------|------------|
| R1 | CPA 2x superieur au prevu (>44 EUR) | Moyenne (35%) | Critique -- seulement 94 clients sur 6 mois | Tester 5+ creatives en M2, pivoter vers micro-influenceurs si CPA > 35 EUR a M3 |
| R2 | Logistique froid defaillante (produit abime) | Moyenne (25%) | Eleve -- destruction de la reputation, retours | Double emballage isotherme, partenaire logistique backup, assurance transport |
| R3 | Reglementation import alimentaire (blocage douane) | Faible (15%) | Critique -- arret total des ventes | Certifications sanitaires anticipees, agent en douane dedie, stock tampon en France |
| R4 | Reachat quasi-nul (< 1x/an) | Moyenne (30%) | Eleve -- LTV s'effondre, modele non viable | Programme de fidelite des M3, abonnement mensuel propose, enquete satisfaction M2 |
| R5 | Saisonnalite (baisse ete) | Elevee (60%) | Moyen -- M4-M5 correspondent a juin-juillet | Budget flexible, creatives "barbecue ete", promotion saisonniere |

### 6.2 Analyse de sensibilite -- CPA x2

| Metrique | Base (realiste) | CPA x2 | Impact |
|----------|----------------|--------|--------|
| CPA moyen | 17.58 EUR | 35.16 EUR | |
| Clients 6 mois | 455 | 228 | -50% |
| Objectif 200 atteint ? | OUI -- M4 | OUI -- M5 (de justesse) | Retard 1 mois |
| Revenu total | 17 063 EUR | 8 550 EUR | -50% |
| Perte nette | (6 274 EUR) | (8 043 EUR) | -28% de perte en plus |
| CAC all-in | 21.98 EUR | 43.86 EUR | x2 |
| LTV:CAC | 2.24:1 | 1.12:1 | NON VIABLE pour levee |

> **Conclusion** : Si le CPA double, on atteint quand meme 200 clients (de justesse) mais le ratio LTV:CAC devient inacceptable pour les investisseurs. Il faudrait alors prouver que le CPA baissera avec le scaling.

### 6.3 Scenario worst case -- Budget brule a M3

**Situation** : 5 550 EUR depenses (M1 setup + M2-M3 ads), 30 clients acquis, CPA > 100 EUR.

**Plan d'urgence** :

| Action | Budget restant utilise | Resultat attendu |
|--------|----------------------|------------------|
| Stop toutes les ads | 0 EUR | Arret de l'hemorragie |
| Pivot micro-influenceurs food (10 x 150 EUR) | 1 500 EUR | 10 posts UGC, CPA potentiel < 30 EUR |
| Programme referral (offre parrainage 5 EUR) | 500 EUR | 5-15 clients via bouche-a-oreille |
| Marches/salons food artisanal (2 events) | 1 000 EUR | 20-40 clients directs + feedback terrain |
| Retargeting email liste existante | 500 EUR | 3-5 conversions des visiteurs non-convertis |
| Contingence | 950 EUR | Reserve |
| **Total plan B** | **4 450 EUR** | **38-90 clients supplementaires** |

> **Conclusion worst case** : Meme dans le pire scenario, on finit entre 68 et 120 clients. Insuffisant pour l'objectif de 200 mais suffisant pour pivoter le pitch investisseur vers "product-market fit qualitatif" (NPS, taux reachat des 68 premiers clients).

### 6.4 Matrice de sensibilite -- Resultat net 6 mois

| | CPA -30% | CPA base | CPA +30% | CPA +100% |
|---|---------|---------|---------|-----------|
| **Marge brute 35%** | (3 891) | (5 018) | (5 810) | (7 287) |
| **Marge brute 25.3% (base)** | (4 712) | (6 274) | (7 348) | (9 230) |
| **Marge brute 20%** | (5 203) | (6 963) | (8 134) | (9 648) |

> Les resultats entre parentheses indiquent une perte. Toutes les cellules sont negatives -- la campagne est deficitaire dans tous les cas sur 6 mois. La question n'est pas "serons-nous rentables ?" mais "atteindrons-nous 200 clients pour lever des fonds ?".

---

## 7. SYNTHESE EXECUTIVE

### Decision Framework

| Question | Reponse |
|----------|---------|
| Le budget de 10 000 EUR est-il suffisant pour 200 clients ? | OUI en scenario realiste (455 clients). NON en conservateur (94). |
| La campagne sera-t-elle rentable ? | NON. Perte nette de 6 274 EUR en scenario realiste. Attendu et acceptable pour un lancement. |
| Le modele est-il viable pour les investisseurs ? | CONDITIONNEL. Le ratio LTV:CAC de 2.24:1 est sous le seuil de 3:1. Viable si : (a) entrepot France (-40% logistique), (b) reachat > 3x/an, ou (c) panier moyen > 42 EUR. |
| Quel est le risque principal ? | La marge brute (25.3%) est faible pour du D2C. La logistique froid internationale est le goulot. |
| Recommandation ? | LANCER avec un go/no-go a M3. Si CPA > 45 EUR a M3, pivoter vers plan B (influenceurs + events). |

### Indicateurs de suivi mensuels (KPI Dashboard)

| KPI | Seuil vert | Seuil orange | Seuil rouge |
|-----|-----------|-------------|-------------|
| CPA blended | < 25 EUR | 25-45 EUR | > 45 EUR |
| Clients cumules vs plan | > 90% du plan | 70-90% | < 70% |
| Taux conversion site | > 2.5% | 1.5-2.5% | < 1.5% |
| Panier moyen | > 35 EUR | 30-35 EUR | < 30 EUR |
| Budget consomme vs plan | +/- 10% | +/- 20% | > 20% ecart |

---

*Modele construit le 2026-05-08. Prochaine revision recommandee : fin M2 (apres 1 mois de donnees publicitaires reelles).*
*Toute decision d'investissement doit etre prise apres validation des hypotheses H3, H4 et H10 avec des donnees terrain.*
