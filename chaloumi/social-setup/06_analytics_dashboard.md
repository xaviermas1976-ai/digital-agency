# ANALYTICS & DASHBOARD — Setup Metricool + Pixels

---

## METRICOOL (Dashboard unifie)

### Comptes a connecter
1. Instagram @chaloumi.fr
2. TikTok @chaloumi.fr
3. Pinterest Chaloumi France
4. Facebook Chaloumi
5. Google Analytics 4

### KPIs a suivre par plateforme

#### Instagram
| KPI | Objectif M1 | Objectif M3 | Objectif M6 |
|-----|-------------|-------------|-------------|
| Followers | 300 | 1 500 | 5 000 |
| Engagement rate | 5%+ | 4%+ | 3.5%+ |
| Reach/post | 500 | 2 000 | 5 000 |
| Saves/post | 10+ | 30+ | 50+ |
| Profile visits/semaine | 100 | 500 | 1 500 |
| Link clicks/semaine | 20 | 100 | 300 |

#### TikTok
| KPI | Objectif M1 | Objectif M3 | Objectif M6 |
|-----|-------------|-------------|-------------|
| Followers | 200 | 2 000 | 8 000 |
| Average views | 500 | 3 000 | 10 000 |
| Engagement rate | 8%+ | 6%+ | 5%+ |
| Shares/video | 5+ | 20+ | 50+ |
| Profile visits/semaine | 50 | 300 | 1 000 |

#### Pinterest
| KPI | Objectif M1 | Objectif M3 | Objectif M6 |
|-----|-------------|-------------|-------------|
| Impressions/mois | 5 000 | 30 000 | 100 000 |
| Outbound clicks/mois | 50 | 300 | 1 000 |
| Saves/mois | 20 | 150 | 500 |
| Engaged audience | 100 | 500 | 2 000 |

#### Facebook
| KPI | Objectif M1 | Objectif M3 | Objectif M6 |
|-----|-------------|-------------|-------------|
| Page likes | 100 | 500 | 1 500 |
| Post reach | 200 | 1 000 | 3 000 |
| Link clicks/semaine | 10 | 50 | 150 |

---

## META PIXEL

### Installation
```html
<!-- Meta Pixel Code — dans <head> de layout.tsx -->
<script>
!function(f,b,e,v,n,t,s)
{if(f.fbq)return;n=f.fbq=function(){n.callMethod?
n.callMethod.apply(n,arguments):n.queue.push(arguments)};
if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
n.queue=[];t=b.createElement(e);t.async=!0;
t.src=v;s=b.getElementsByTagName(e)[0];
s.parentNode.insertBefore(t,s)}(window, document,'script',
'https://connect.facebook.net/en_US/fbevents.js');
fbq('init', 'PIXEL_ID_ICI');
fbq('track', 'PageView');
</script>
```

### Events a configurer
| Event | Declencheur | Page |
|-------|-------------|------|
| `PageView` | Toute page | Toutes |
| `ViewContent` | Page produit | /boutique/[product] |
| `AddToCart` | Clic "Ajouter au panier" | /boutique |
| `InitiateCheckout` | Debut checkout | /checkout |
| `Purchase` | Confirmation commande | /confirmation |
| `Lead` | Inscription newsletter | / (popup) |
| `CompleteRegistration` | Creation compte | /compte |

### Conversions API (CAPI)
Configurer le server-side tracking via Conversions API pour :
- Resilience aux ad blockers
- Meilleure attribution
- Score qualite event > 8/10

---

## TIKTOK PIXEL

### Installation
```html
<!-- TikTok Pixel — dans <head> de layout.tsx -->
<script>
!function (w, d, t) {
  w.TiktokAnalyticsObject=t;var ttq=w[t]=w[t]||[];
  ttq.methods=["page","track","identify","instances","debug","on","off","once","ready","alias","group","enableCookie","disableCookie"];
  ttq.setAndDefer=function(t,e){t[e]=function(){t.push([e].concat(Array.prototype.slice.call(arguments,0)))}};
  for(var i=0;i<ttq.methods.length;i++)ttq.setAndDefer(ttq,ttq.methods[i]);
  ttq.instance=function(t){for(var e=ttq._i[t]||[],n=0;n<ttq.methods.length;n++)ttq.setAndDefer(e,ttq.methods[n]);return e};
  ttq.load=function(e,n){var i="https://analytics.tiktok.com/i18n/pixel/events.js";
  ttq._i=ttq._i||{};ttq._i[e]=[];ttq._i[e]._u=i;ttq._t=ttq._t||{};ttq._t[e]=+new Date;
  ttq._o=ttq._o||{};ttq._o[e]=n||{};
  var o=document.createElement("script");o.type="text/javascript";o.async=!0;o.src=i+"?sdkid="+e+"&lib="+t;
  var a=document.getElementsByTagName("script")[0];a.parentNode.insertBefore(o,a)};
  ttq.load('PIXEL_ID_ICI');
  ttq.page();
}(window, document, 'ttq');
</script>
```

### Events
| Event | Declencheur |
|-------|-------------|
| `PageView` | Automatique |
| `ViewContent` | Page produit |
| `AddToCart` | Ajout panier |
| `PlaceAnOrder` | Achat confirme |
| `CompleteRegistration` | Inscription |

---

## PINTEREST TAG

### Installation
```html
<!-- Pinterest Tag — dans <head> de layout.tsx -->
<script>
!function(e){if(!window.pintrk){window.pintrk=function(){
window.pintrk.queue.push(Array.prototype.slice.call(arguments))};
var n=window.pintrk;n.queue=[],n.version="3.0";
var t=document.createElement("script");t.async=!0,
t.src=e;var r=document.getElementsByTagName("script")[0];
r.parentNode.insertBefore(t,r)}}("https://s.pinimg.com/ct/core.js");
pintrk('load', 'TAG_ID_ICI');
pintrk('page');
</script>
```

### Events
| Event | Declencheur |
|-------|-------------|
| `pagevisit` | Automatique |
| `addtocart` | Ajout panier |
| `checkout` | Achat confirme |
| `signup` | Inscription newsletter |

---

## GOOGLE ANALYTICS 4

### Property
- Nom : Chaloumi.fr
- Devise : EUR
- Fuseau : Europe/Paris
- Industrie : Food & Beverages

### Events e-commerce recommandes
| Event GA4 | Mapping |
|-----------|---------|
| `view_item` | Page produit |
| `add_to_cart` | Ajout panier |
| `begin_checkout` | Debut checkout |
| `purchase` | Confirmation |
| `sign_up` | Creation compte |
| `generate_lead` | Inscription newsletter |

### Audiences personnalisees a creer
1. **Visiteurs 7j** — tous les visiteurs des 7 derniers jours
2. **Visiteurs recettes** — ont visite /recettes
3. **Abandonistes** — add_to_cart sans purchase
4. **Clients** — event purchase
5. **Newsletter** — event generate_lead
6. **Social traffic** — utm_medium = social ou paid_social

---

## REPORTING HEBDOMADAIRE

### Rapport Metricool auto (chaque lundi 9h)
- Croissance followers toutes plateformes
- Top 3 posts de la semaine (par engagement)
- Meilleur jour/heure de publication
- Clicks vers le site
- ROI ads (depense vs conversions)

### Rapport mensuel (a faire manuellement)
- Comparaison KPIs vs objectifs
- CAC par canal
- LTV projete
- Recommendations ajustements budget
- Top content → dupliquer
- Flop content → analyser et pivoter
