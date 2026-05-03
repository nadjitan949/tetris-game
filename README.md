# 🎮 TETRIS

Un Tetris moderne, responsive et sans dépendances — un seul fichier HTML.

![HTML](https://img.shields.io/badge/HTML-5-orange?style=flat-square&logo=html5)
![CSS](https://img.shields.io/badge/CSS-3-blue?style=flat-square&logo=css3)
![JS](https://img.shields.io/badge/JavaScript-Vanilla-yellow?style=flat-square&logo=javascript)
![Licence](https://img.shields.io/badge/Licence-MIT-green?style=flat-square)

---

## ✨ Fonctionnalités

- **7 pièces classiques** (I, O, T, S, Z, J, L) avec leurs couleurs distinctives
- **Ghost piece** — aperçu transparent de la position de chute
- **Effets visuels** — flash blanc + explosion de particules colorées quand une ligne est effacée
- **Effets sonores** — sons 8-bit générés via Web Audio API (point, ligne, game over)
- **Niveaux progressifs** — la vitesse augmente toutes les 10 lignes
- **Wall kicks** — la rotation teste 5 positions pour éviter les blocages
- **Hard drop** (espace) — chute instantanée jusqu'au bas
- **Pause** intégrée
- **Responsive** — s'adapte aux écrans téléphone, tablette et desktop
- **Contrôles tactiles** — boutons dédiés sur mobile, tap sur la grille pour tourner
- **Aucune dépendance** — zéro framework, zéro librairie externe

---

## 🚀 Lancement

Aucune installation requise. Ouvre simplement le fichier dans ton navigateur :

```bash
# Option 1 — double-clic sur le fichier
tetris.html

# Option 2 — via un serveur local (recommandé)
npx serve .
# ou
python -m http.server 8000
```

---

## 🕹️ Contrôles

### Clavier

| Touche | Action |
|--------|--------|
| `←` `→` | Déplacer la pièce |
| `↑` | Rotation |
| `↓` | Descente accélérée |
| `Espace` | Hard drop (chute instantanée) |
| `P` | Pause / Reprendre |

### Mobile & Tablette

| Bouton | Action |
|--------|--------|
| `◀` `▶` | Déplacer la pièce |
| `▼` | Descendre |
| `🔄` | Rotation |
| `⬇⬇ DROP` | Hard drop |
| `PAUSE` | Pause / Reprendre |
| Tap sur la grille | Rotation rapide |

---

## 🏆 Système de score

| Lignes effacées | Points |
|-----------------|--------|
| 1 ligne | 100 × niveau |
| 2 lignes | 300 × niveau |
| 3 lignes | 500 × niveau |
| 4 lignes (Tetris) | 800 × niveau |

Le niveau augmente toutes les **10 lignes** effacées. La vitesse de chute augmente avec chaque niveau jusqu'à un minimum de 100 ms.

---

## 🛠️ Architecture

Le projet tient en **un seul fichier** `tetris.html` structuré en trois parties :

```
tetris.html
├── <style>     — CSS avec variables, responsive, animations
├── <body>      — Structure HTML (canvas board, panel, contrôles tactiles)
└── <script>    — Logique de jeu en JS vanilla
    ├── Audio       (Web Audio API — sons génératifs)
    ├── Canvas      (rendu board + next piece)
    ├── Particles   (système de particules canvas)
    ├── Game state  (board, pièces, score, niveau)
    ├── Physique    (collision, rotation, wall kicks, drop)
    ├── Loop        (setInterval adaptatif au niveau)
    └── Inputs      (keyboard + touch events)
```

---

## 🎨 Design

- Police d'affichage : **Press Start 2P** (titres, rétro)
- Police UI : **Orbitron** (panneaux, valeurs)
- Thème sombre avec accents **violet** (#7c3aed) et **cyan** (#06b6d4)
- Blocs en dégradé avec reflet lumineux simulé
- Effets de particules et flash sur effacement de lignes
- Fond ambiant avec radial-gradients subtils

---

## 📱 Compatibilité

| Navigateur | Support |
|------------|---------|
| Chrome / Edge | ✅ |
| Firefox | ✅ |
| Safari (iOS) | ✅ |
| Samsung Internet | ✅ |

> **Note :** Le son nécessite une première interaction utilisateur (politique des navigateurs modernes). Le son s'active automatiquement dès le premier clic ou appui de touche.

---

## 📄 Licence

MIT — libre de réutiliser, modifier et distribuer.
