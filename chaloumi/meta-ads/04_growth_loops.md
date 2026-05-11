# CHALOUMI -- Growth Loops & Programmes
## APEX DIGITAL | Activation Phase 1-2

---

## 1. PROGRAMME DE PARRAINAGE

### Mecanique
- **Offre** : Parraine un ami → tu recois -10 EUR, il recoit -10%
- **Code unique** : PARRAIN-[PRENOM] genere automatiquement
- **Tracking** : Code associe au compte client dans Brevo/Shopify
- **Activation** : Email post-achat J+7 (template 11_postachat_avis)

### Implementation
1. Generer codes promos uniques par client dans Shopify/WooCommerce
2. Email automatique J+7 apres premier achat avec le code parrainage
3. Quand le filleul utilise le code → credit -10 EUR sur le compte du parrain
4. Email de notification "Ton ami a commande ! Voici tes -10 EUR"

### KPIs
- Taux de partage du code : 15% cible
- Taux de conversion filleul : 8% cible
- CAC parrainage : < 10 EUR (10 EUR offerts / 12.5% conversion)

---

## 2. LEAD MAGNET RECETTES

### Mecanique
- **Offre** : "5 recettes exclusives au Chaloumi" en PDF
- **Capture** : Formulaire email sur la landing page (TastingSection)
- **Delivery** : Email automatique avec PDF + code BIENVENUE10
- **Sequence** : Integre dans le welcome flow (emails 01-05)

### Contenu du PDF
1. Chaloumi grille miel-thym (classique)
2. Salade pasteque-Chaloumi-menthe (ete)
3. Burger vegetarien au Chaloumi (gourmand)
4. Bowl mediterraneen quinoa-Chaloumi (healthy)
5. Chaloumi frit confiture de figues (apero chic)

Chaque recette : photo, ingredients, etapes, temps, difficulte, astuce chef.

### Brevo Setup
- Liste : "Leads Recettes"
- Tag : lead_source=recettes
- Workflow : Lead → Email PDF → Sequence Welcome (01-05)

---

## 3. UGC #MonChaloumiMoment

### Mecanique
- **Hashtag** : #MonChaloumiMoment (Instagram + TikTok)
- **Incentive** : Repost officiel + chance de gagner 1 mois de Chaloumi gratuit
- **Frequence** : Repost hebdomadaire le dimanche
- **Curation** : Surveiller le hashtag quotidiennement

### Implementation
1. Lancement S5 du calendrier editorial (post 13 + TikTok 09)
2. Rappel dans chaque email post-achat
3. Carte physique dans le colis : "Partagez avec #MonChaloumiMoment"
4. Tirage au sort mensuel : 1 coffret offert parmi les participants
5. Meilleurs UGC reutilises en Spark Ads (TikTok) et temoignages (Meta)

### KPIs
- UGC recus/mois : 10 cible M1, 30 cible M3
- Repost engagement rate : 8%+
- UGC reutilises en ads : 3/mois

---

## 4. ABONNEMENT MENSUEL

### Mecanique
- **Offre** : Coffret Best-Seller chaque mois
- **Prix** : 50,91 EUR/mois (au lieu de 59,90 EUR = -15%)
- **Engagement** : Aucun — modifiable et annulable a tout moment
- **Activation** : Email post-achat J+14 (template 12_postachat_reachat)

### Avantages abonne
- -15% a vie sur le coffret mensuel
- Livraison offerte
- Acces aux editions limitees en avant-premiere
- Recette exclusive mensuelle
- Choix de la date de livraison

### Implementation
1. Page abonnement sur le site
2. Integration paiement recurrent (Stripe/Shopify Subscriptions)
3. Email J+14 post-premier-achat avec presentation abonnement
4. Relance J+30 si pas converti : "FIDELE10" -10% sur commande ponctuelle

### KPIs
- Taux de conversion abo : 8% des premiers acheteurs
- Churn mensuel : < 10%
- LTV abonne : 6x panier moyen (6 mois minimum)

---

## 5. RECIPE SHARING LOOP

### Mecanique
- **Contenu** : Recettes sur le blog/site
- **Partage** : Boutons partage social sur chaque recette
- **SEO** : Schema.org Recipe pour apparaitre dans Google Recettes
- **Pinterest** : Chaque recette = 1 epingle optimisee
- **Email** : Recette du mois dans chaque newsletter

### Boucle virale
1. Visiteur decouvre une recette (SEO/Pinterest/Social)
2. Il s'inscrit pour recevoir le PDF complet (lead magnet)
3. Il recoit la sequence welcome (emails 01-05)
4. Il achete le Chaloumi
5. Il cuisine et partage #MonChaloumiMoment
6. Son contenu UGC amene de nouveaux visiteurs
7. Retour a l'etape 1

---

## 6. TIMELINE D'ACTIVATION

| Semaine | Action |
|---------|--------|
| S1 | Lead magnet PDF actif + welcome flow Brevo |
| S2 | Parrainage actif (codes dans email J+7) |
| S3 | Carte physique #MonChaloumiMoment dans les colis |
| S5 | Lancement officiel challenge #MonChaloumiMoment |
| S6 | Page abonnement live |
| S8 | Premier tirage au sort UGC |
| S10 | Premier coffret saisonnier ete |
| S12 | Bilan + optimisation boucles |
