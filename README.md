# 🚀 SEO & Backlinks Strategy — Ziri Dev / Nova Dev
## Google Page 1 in 30 Days — Full Execution Playbook

**Sites ciblés :**
| Site | Langue | Marché |
|------|--------|--------|
| https://ziridev-fr.vercel.app | 🇫🇷 FR | France |
| https://ziridev.vercel.app | 🇬🇧 EN | UK / US / Global |
| https://novadev-fr-audit.vercel.app | 🇫🇷 FR | France |
| https://novadev-audit.vercel.app | 🇬🇧 EN | UK / US / Global |

---

## 📁 Structure du projet

```
webapp/
├── seo-audit/
│   ├── audit-report.md                    ← Audit SEO complet des 4 sites
│   ├── robots-txt-all-sites.txt           ← robots.txt pour les 4 sites
│   └── sitemaps/
│       ├── sitemap-ziridev-fr.xml
│       ├── sitemap-novadev-fr.xml
│       └── sitemap-novadev-en.xml
│
├── keyword-research/
│   └── keywords-master.md                 ← 60+ mots-clés FR + EN classés
│
├── schema-markup/
│   ├── ziridev-fr-schema.html             ← Coller dans <head> ziridev-fr
│   ├── novadev-fr-schema.html             ← Coller dans <head> novadev-fr
│   └── novadev-en-schema.html             ← Coller dans <head> novadev-en
│
├── blog-articles/
│   ├── fr/
│   │   ├── FR-01-combien-coute-site-web.md
│   │   └── FR-02-signes-site-nuit-image-marque.md
│   └── en/
│       ├── EN-01-website-losing-clients.md
│       ├── EN-02-free-website-audit-what-to-expect.md
│       └── EN-03-100-pagespeed-technical.md
│
├── guest-posts/
│   ├── fr/
│   │   └── GP-FR-01-5-erreurs-seo-pme.md
│   └── en/
│       └── GP-EN-01-5-website-mistakes.md
│
├── pr-articles/
│   ├── fr/
│   │   └── PR-FR-01-lancement-ziridev.md
│   └── en/
│       └── PR-EN-01-nova-dev-launch.md
│
├── backlinks/
│   └── submission-tracker.md              ← 60+ sources classées par tier
│
└── social-citations/
    └── profiles-templates.md              ← Templates profils LinkedIn, Clutch, etc.
```

---

## 🎯 Règle éditoriale fondamentale

> **Les articles EN ne parlent PAS de la France.** Ils ciblent le marché UK/US/global en tant qu'agence web premium internationale. Les articles FR ciblent exclusivement le marché français.

---

## 📅 Plan d'action — Semaine 1

### Actions sur les sites (code)
1. Coller les schémas `schema-markup/*.html` dans le `<head>` de chaque site
2. Mettre à jour les meta titles/descriptions (voir fichiers schema-markup)
3. Ajouter `sitemap.xml` depuis `seo-audit/sitemaps/` dans chaque `public/`
4. Ajouter `robots.txt` depuis `seo-audit/robots-txt-all-sites.txt`
5. **Corriger les compteurs à 0** (0 projets, 0% satisfaction) — signal de méfiance

### Actions off-page (backlinks — sans code)
| Priorité | Action | Plateforme | Impact |
|----------|--------|-----------|--------|
| 🔴 1 | Soumettre sitemaps | Google Search Console | ⭐⭐⭐⭐⭐ |
| 🔴 2 | Créer profil Google Business | business.google.com | ⭐⭐⭐⭐⭐ |
| 🔴 3 | Lancer sur ProductHunt | producthunt.com | ⭐⭐⭐⭐ |
| 🔴 4 | Créer pages LinkedIn company | linkedin.com | ⭐⭐⭐⭐ |
| 🔴 5 | Créer profil Clutch.co | clutch.co | ⭐⭐⭐⭐ |
| 🟠 6 | Publier EN-01 sur Medium | medium.com | ⭐⭐⭐ |
| 🟠 7 | Publier EN-03 sur dev.to | dev.to | ⭐⭐⭐ |
| 🟠 8 | Publier EN-03 sur Hashnode | hashnode.com | ⭐⭐⭐ |
| 🟠 9 | Distribuer PR-EN-01 | PRLog + OpenPR | ⭐⭐⭐ |
| 🟠 10 | Distribuer PR-FR-01 | Presselib + 24presse | ⭐⭐⭐ |

---

## 📅 Plan d'action — Semaine 2

| Action | Plateforme |
|--------|-----------|
| Publier FR-01 + FR-02 sur Medium FR | medium.com |
| Soumettre GP-FR-01 au Blog du Modérateur | blogdumoderateur.com |
| Soumettre GP-EN-01 à Indie Hackers | indiehackers.com |
| Créer profil DesignRush | designrush.com |
| Créer profil AgencesME | agences.me |
| Créer profil GoodFirms | goodfirms.co |
| Répondre 5 questions Quora FR + 5 EN | quora.com |
| Inscription Pages Jaunes + Kompass | pagesjaunes.fr, kompass.com |
| Publier Show HN (EN-03) | news.ycombinator.com |
| Inscription Sortlist France | sortlist.fr |

---

## 🔑 Mots-clés prioritaires à tracker

### 🇫🇷 Français
1. `audit site web gratuit france` — 1,300/mo, Low
2. `agence web premium france` — 590/mo, Low
3. `agence web premium pour PME` — 110/mo, Very Low
4. `création site web professionnel france` — 1,800/mo, Medium
5. `audit SEO site internet france` — 880/mo, Low

### 🇬🇧 Anglais
1. `free website audit` — 1,300/mo, Low
2. `premium web design agency` — 720/mo, Medium
3. `premium web design agency for small business` — 260/mo, Very Low
4. `website performance audit agency` — 210/mo, Very Low
5. `web design agency for professional services` — 210/mo, Very Low

---

## ⚠️ Points critiques

1. **Domaines personnalisés** : Les `.vercel.app` ne peuvent pas avoir de Google Business Profile avec adresse physique. Investir dans `ziridev.fr` et `novadev.fr` accélérerait massivement le SEO local.
2. **Contenu dupliqué** : ziridev-fr et novadev-fr ont des textes très similaires → différencier ou ajouter canonical cross-domain.
3. **Compteurs à 0** : À supprimer ou remplacer immédiatement.
4. **Preuve sociale** : Les témoignages ont des attributions génériques → ajouter prénoms/entreprises réels dès que possible.

---

## 📊 KPIs à suivre (hebdomadaire)

| KPI | Outil | Cible S4 |
|-----|-------|---------|
| Position mots-clés prioritaires | Google Search Console | Top 10 |
| Nombre de backlinks | Ahrefs Free / GSC | 20+ |
| Impressions Google | GSC | +500% |
| Clics organiques | GSC | 50+/semaine |
| Core Web Vitals | GSC / PageSpeed | 90+ |

---

## 🔗 Ressources

- **Google Search Console :** https://search.google.com/search-console
- **PageSpeed Insights :** https://pagespeed.web.dev
- **Schema Validator :** https://validator.schema.org
- **Rich Results Test :** https://search.google.com/test/rich-results
- **Ahrefs Free Backlink Checker :** https://ahrefs.com/backlink-checker
- **Mobile-Friendly Test :** https://search.google.com/test/mobile-friendly
