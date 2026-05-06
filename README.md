# 🔋 Tri de piles usagées — Histogramme interactif

![HTML](https://img.shields.io/badge/HTML-Single%20File-orange?style=flat-square&logo=html5)
![CSS](https://img.shields.io/badge/CSS-Vanilla-blue?style=flat-square&logo=css3)
![JS](https://img.shields.io/badge/JavaScript-Vanilla-yellow?style=flat-square&logo=javascript)
![Niveau](https://img.shields.io/badge/Niveau-Seconde-green?style=flat-square)
![Durée](https://img.shields.io/badge/Durée-1h-lightgrey?style=flat-square)
![Licence](https://img.shields.io/badge/Licence-MIT-informational?style=flat-square)

> Application pédagogique clé en main pour un TP de **classe de Seconde**.  
> Les élèves saisissent les tensions mesurées au voltmètre sur un lot de piles AA ;  
> l'histogramme se trace **en temps réel** et les statistiques se calculent automatiquement.

---

## 📋 Aperçu

```
┌─────────────────────────────────────────────────────────┐
│  En-tête : nom · prénom · classe · groupe · date        │
├───────────────────────────┬─────────────────────────────┤
│  Saisie P1 … P20          │  Histogramme SVG animé      │
│  ● couleur en temps réel  │  ─────────────────────────  │
│                           │  Statistiques               │
│                           │  min · max · étendue        │
│                           │  moyenne · médiane          │
│                           │  ─────────────────────────  │
│                           │  Bilan 🟢 🟠 🔴 + %        │
└───────────────────────────┴─────────────────────────────┘
              [ Enregistrer en PDF ]
```

---

## ✨ Fonctionnalités

| Fonctionnalité | Détail |
|---|---|
| **Saisie clavier fluide** | 20 champs P1–P20, navigation ↑ ↓ / Entrée, accepte virgule et point |
| **Histogramme animé** | 6 intervalles SVG mis à jour à chaque frappe, barres avec transition CSS |
| **Tri en 3 catégories** | 🟢 Bonne ≥ 1,3 V · 🟠 Faible 1,1–1,3 V · 🔴 Usée < 1,1 V |
| **Statistiques en direct** | min, max, étendue, moyenne, médiane recalculés en continu |
| **Barre de progression** | Répartition tricolore proportionnelle en temps réel |
| **Coloration des lignes** | Chaque ligne de saisie se colore selon la catégorie détectée |
| **Export PDF** | Impression navigateur avec CSS A4 dédié, couleurs préservées |
| **Zéro dépendance** | Fichier HTML unique, fonctionne hors ligne |

---

## 🚀 Utilisation

### Option 1 — Directement depuis GitHub Pages

```
https://<votre-compte>.github.io/<nom-du-repo>/piles_histogramme_interactif.html
```

### Option 2 — En local

```bash
git clone https://github.com/<votre-compte>/<nom-du-repo>.git
# Ouvrir le fichier dans un navigateur
open piles_histogramme_interactif.html   # macOS
start piles_histogramme_interactif.html  # Windows
xdg-open piles_histogramme_interactif.html  # Linux
```

> ⚡ Aucune installation, aucun serveur, aucune dépendance npm.

---

## 🎓 Contexte pédagogique

**Discipline** : Sciences Physiques · STI2D · SNT  
**Niveau** : Classe de Seconde  
**Durée** : 1 heure  

### Compétences travaillées

- Utilisation correcte d'un voltmètre (calibre, branchement, lecture)
- Rigueur dans le relevé et la saisie de mesures
- Calcul de grandeurs statistiques : moyenne, médiane, étendue
- Lecture et interprétation d'un histogramme de fréquences
- Sens critique sur la méthode de mesure (tension à vide vs. sous charge)

### Déroulement suggéré (1h)

```
10 min  Mise en situation + protocole voltmètre
20 min  Mesures sur le lot de piles (par binôme)
15 min  Saisie dans l'application + lecture des statistiques
10 min  Interprétation : pourcentages, moyenne vs médiane
 5 min  Ouverture : limite de la mesure à vide, résistance interne
```

---

## 🗂️ Structure du dépôt

```
├── piles_histogramme_interactif.html   ← Application interactive élève
├── fiche_piles_statistiques.html       ← Fiche TP complète (élève + corrigé)
└── README.md
```

---

## 🔧 Technique

- **Histogramme** : SVG natif, transitions CSS sur les attributs `height` / `y`  
- **Statistiques** : calcul JavaScript pur à chaque événement `input`  
- **Export PDF** : `window.print()` avec `@media print` dédié (`print-color-adjust: exact`)  
- **Polices** : Google Fonts — Playfair Display · Source Serif 4 · JetBrains Mono  
- **Compatibilité** : Chrome, Firefox, Safari, Edge (versions récentes)

---

## 📄 Licence

[MIT](LICENSE) — Libre d'utilisation, de modification et de redistribution.  
Mention appréciée si utilisé dans un établissement scolaire. 🙏
