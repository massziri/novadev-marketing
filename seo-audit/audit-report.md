# 🔍 SEO Audit Report — Ziri Dev & Nova Dev
**Date :** Avril 2026

---

## 1. STATUT D'INDEXATION

| Site | Indexé Google | Statut |
|------|--------------|--------|
| ziridev-fr.vercel.app | ✅ Oui (2 jours) | Crawlé |
| novadev-fr-audit.vercel.app | ✅ Oui (3 jours) | Crawlé |
| novadev-audit.vercel.app | ✅ Oui (2 jours) | Crawlé |
| ziridev.vercel.app | ✅ Oui | Crawlé |

**⚠️ Problème critique :** Tous les 4 sites sont sur des sous-domaines `.vercel.app` → DA=0. Les backlinks sont le levier #1.

---

## 2. PROBLÈMES ON-PAGE IDENTIFIÉS

| Problème | Sévérité | Sites concernés |
|----------|----------|----------------|
| Title tags non différenciés | HIGH | Tous 4 |
| Meta descriptions génériques | HIGH | Tous 4 |
| H1 non optimisé pour les mots-clés | HIGH | Tous 4 |
| Pas de sitemap.xml détecté | HIGH | Tous 4 |
| Pas de robots.txt détecté | MEDIUM | Tous 4 |
| Schema.org LocalBusiness manquant | HIGH | Tous 4 |
| Schema.org FAQPage manquant | MEDIUM | Tous 4 |
| Compteurs à 0 (0 projets, 0% satisfaction) | HIGH | Tous 4 |
| Open Graph / Twitter Cards absents | MEDIUM | Tous 4 |
| Contenu quasi-identique entre les sites FR | CRITICAL | ziridev-fr / novadev-fr |
| Pas de balises canonical | CRITICAL | Tous 4 |

---

## 3. CORRECTIONS META TAGS PRIORITAIRES

### ziridev-fr.vercel.app
```
AVANT:  "Agence premium de création de sites web | Ziri Dev France"
APRÈS:  "Agence Création Site Web Premium en France | Design & SEO | Ziri Dev"

MÉTA:   "Ziri Dev crée des sites web premium pour entreprises françaises.
         Design sur-mesure, SEO avancé, performance 100/100. Audit gratuit."
```

### novadev-fr-audit.vercel.app
```
AVANT:  "Agence premium de création de sites web | Nova Dev France"
APRÈS:  "Agence Web Premium France — Sites Pro & Audit Gratuit | Nova Dev"

MÉTA:   "Nova Dev : agence web premium en France. Sites professionnels pour
         PME, cabinets & startups. Audit gratuit offert. Résultats concrets."
```

### novadev-audit.vercel.app (EN)
```
AVANT:  "Nova Dev: Premium Web Design & Development Agency"
APRÈS:  "Premium Web Design Agency | Free Audit Included | Nova Dev"

MÉTA:   "Nova Dev builds premium websites for businesses that take their brand
         seriously. Free audit included. Sharp design, high performance, SEO-ready."
```

### ziridev.vercel.app (EN)
```
AVANT:  "Ziri Dev: Premium Web Design & Development Agency"
APRÈS:  "Premium Web Agency | Free Website Audit | Ziri Dev"

MÉTA:   "Ziri Dev — premium web design agency. Fast, clean, conversion-optimised
         websites that generate qualified leads. Free audit. Starting at $150."
```

---

## 4. CHECKLIST ACTIONS IMMÉDIATES

- [ ] Ajouter schema.org dans `<head>` (fichiers `schema-markup/`)
- [ ] Mettre à jour title + meta description (voir corrections ci-dessus)
- [ ] Ajouter `sitemap.xml` dans `public/` de chaque site
- [ ] Ajouter `robots.txt` dans `public/` de chaque site
- [ ] Ajouter balises `<link rel="canonical" href="...">` auto-référençantes
- [ ] Ajouter balises `hreflang` (FR ↔ EN) entre les sites jumeaux
- [ ] Corriger les compteurs à 0
- [ ] Vérifier + soumettre dans Google Search Console
- [ ] Activer le rapport Core Web Vitals dans GSC

---

## 5. BALISES HREFLANG RECOMMANDÉES

```html
<!-- Sur ziridev-fr.vercel.app -->
<link rel="alternate" hreflang="fr" href="https://ziridev-fr.vercel.app/" />
<link rel="alternate" hreflang="en" href="https://ziridev.vercel.app/" />
<link rel="alternate" hreflang="x-default" href="https://ziridev.vercel.app/" />

<!-- Sur novadev-fr-audit.vercel.app -->
<link rel="alternate" hreflang="fr" href="https://novadev-fr-audit.vercel.app/" />
<link rel="alternate" hreflang="en" href="https://novadev-audit.vercel.app/" />
<link rel="alternate" hreflang="x-default" href="https://novadev-audit.vercel.app/" />
```
