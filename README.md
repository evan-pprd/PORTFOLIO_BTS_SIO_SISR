# Portfolio BTS SIO 1 — Poupard Evan

Portfolio statique en HTML/CSS conçu pour répondre au cahier des charges du
formateur Lucas Chapel (UFITECH) : 7 pages principales, structure conforme,
critères bloquants couverts.

---

## 📁 Structure du projet

```
portfolio-evan/
├── index.html                 ← Accueil (point d'entrée du site)
├── entreprise.html            ← Page Entreprise (Vinci Construction)
├── cv.html                    ← Page CV (image + bouton téléchargement PDF)
├── competences.html           ← Vue d'ensemble des compétences (référentiel E4)
├── situations.html            ← Vue d'ensemble des situations professionnelles
├── realisations.html          ← Vide (à remplir en 2ᵉ année)
├── veille.html                ← Veille technologique (définition, planning, thèmes)
│
├── competences/
│   └── exemple-competence.html   ← Template à dupliquer
├── situations/
│   └── exemple-situation.html    ← Template à dupliquer
├── veille/
│   └── exemple-veille.html       ← Template à dupliquer
│
├── assets/
│   ├── css/style.css          ← Toute la mise en forme (1 seul fichier)
│   ├── img/
│   │   ├── logo-ufitech.png   ← Déjà fourni
│   │   ├── logo-vinci.png     ← Déjà fourni
│   │   ├── photo.jpg          ← À AJOUTER (ta photo)
│   │   └── cv.png             ← À AJOUTER (ton CV en image)
│   ├── files/
│   │   └── cv.pdf             ← À AJOUTER (ton CV en PDF)
│   └── screenshots/           ← Tes captures d'écran pour les situations
│
└── README.md                  ← ce fichier
```

---

## 🚀 Déploiement sur GitHub Pages

### Étape 1 — Créer un compte GitHub
Si ce n'est pas déjà fait, inscris-toi sur [github.com](https://github.com/signup).
Choisis un nom d'utilisateur **propre et professionnel** : il apparaîtra dans
l'URL finale du portfolio (par exemple `evanpoupard.github.io`).

### Étape 2 — Créer le dépôt
1. Sur GitHub, clique en haut à droite sur le `+` puis **New repository**.
2. Nom du dépôt : **`evanpoupard.github.io`** (remplace par ton nom d'utilisateur exact).
   ⚠️ Ce nom précis est important : il déclenche automatiquement la publication GitHub Pages à la racine de ton compte.
3. Visibilité : **Public**.
4. Coche **Add a README file** (puis tu écraseras le fichier).
5. Clique **Create repository**.

### Étape 3 — Téléverser les fichiers
**Méthode simple (interface web)** :
1. Sur la page de ton dépôt, clique **Add file → Upload files**.
2. Glisse-dépose l'ensemble du contenu du dossier `portfolio-evan/`
   (les fichiers .html, le dossier `assets/`, les sous-dossiers, etc.).
3. Tout en bas, clique **Commit changes**.

**Méthode Git (recommandée pour un SISR — montre une compétence supplémentaire)** :
```bash
# Dans le dossier portfolio-evan
git init
git add .
git commit -m "Initialisation du portfolio"
git branch -M main
git remote add origin https://github.com/evanpoupard/evanpoupard.github.io.git
git push -u origin main
```

### Étape 4 — Activer GitHub Pages
1. Dans ton dépôt, va dans **Settings → Pages** (menu de gauche).
2. Sous **Source**, choisis : `Deploy from a branch`.
3. Sélectionne la branche `main` et le dossier `/ (root)`.
4. Clique **Save**.
5. Attends 1 à 2 minutes : ton site est en ligne sur
   `https://evanpoupard.github.io` 🎉

> Pour **mettre à jour** le site, il suffira de pousser de nouveaux commits
> (ou de re-téléverser des fichiers via l'interface). Le déploiement est
> automatique à chaque push.

---

## ✏️ Personnalisation — checklist

### Avant la mise en ligne, complète au minimum :

- [ ] **`index.html`** — vérifie le texte d'introduction.
- [ ] **`assets/img/photo.jpg`** — ajoute ta photo (format portrait recommandé, 4/5).
- [ ] **`entreprise.html`** — remplace tous les blocs entre crochets `[...]`.
- [ ] **`assets/img/cv.png`** + **`assets/files/cv.pdf`** — ajoute ton CV.
- [ ] **`competences.html`** — vérifie les libellés avec ta grille E4 officielle.
- [ ] **`situations.html`** — adapte les 3 cartes à tes vraies missions.
- [ ] **`veille.html`** — adapte les 3 thèmes et exemples de veille.

### Pour ajouter une nouvelle situation professionnelle :
1. Copie `situations/exemple-situation.html` → `situations/sp-nom-de-la-mission.html`
2. Modifie le titre, le contexte, le déroulé, ajoute tes captures.
3. Place tes captures dans `assets/screenshots/` avec un nom clair
   (ex. `SP1_etape3_dhcp.png` comme suggéré dans le cahier des charges).
4. Dans `situations.html`, ajoute une nouvelle carte qui pointe vers
   ton nouveau fichier.

Même principe pour **`competences/`** et **`veille/`**.

---

## 🎨 Personnaliser le design

Toutes les couleurs et polices sont définies en **variables CSS** au début
de `assets/css/style.css` :

```css
:root {
  --ink:    #0a1628;   /* couleur du texte */
  --paper:  #fbfaf7;   /* fond de page */
  --blue:   #0e2a52;   /* bleu profond (titres, accent) */
  --cyan:   #0aa5c2;   /* cyan accent (liens, hover) */
  --mute:   #6b7280;   /* texte secondaire */
}
```

Modifie ces valeurs pour changer toute la palette du site d'un coup.
La règle du cahier des charges (2 à 3 couleurs hors noir/blanc) est respectée
avec le bleu profond et le cyan d'accent.

---

## 🔍 Tester en local avant de publier

Pour prévisualiser le site avant de le pousser sur GitHub, ouvre simplement
`index.html` dans ton navigateur (double-clic).

Pour un rendu plus fidèle (avec les chemins relatifs corrects), tu peux
lancer un serveur local avec Python :

```bash
cd portfolio-evan
python3 -m http.server 8000
# puis ouvre http://localhost:8000
```

---

## ✅ Critères du barème — couverture

| Critère du barème (Lucas Chapel) | Couvert ? |
|----------------------------------|-----------|
| Pages principales présentes (Accueil, Entreprise, CV, Compétences, Situations, Veille) | ✅ |
| Accueil placé en premier dans le menu | ✅ |
| Menu accessible depuis toutes les pages | ✅ |
| Cohérence graphique (palette 2-3 couleurs) | ✅ |
| Logos UFIP/UFITECH + entreprise sur l'accueil | ✅ |
| CV intégré comme image + bouton de téléchargement PDF | ✅ |
| Compétences avec page dédiée par compétence | ✅ (template fourni) |
| Situations pro : structure contexte / déroulé / conclusion | ✅ (template fourni) |
| Veille : définition + planning + thèmes + exemples | ✅ |
| Captures d'écran et preuves | ⚠️ **À ajouter par toi** |
| 3 situations professionnelles minimum | ⚠️ **À rédiger par toi** |
| 3 exemples de veille minimum | ⚠️ **À rédiger par toi** |

---

## 💡 Astuce bonus

La création et la mise en ligne de ce portfolio peuvent **elles-mêmes**
constituer un exemple de veille technologique (sur Git, GitHub Pages, le
HTML statique, l'hébergement gratuit) — ou une situation professionnelle
si elle s'inscrit dans un besoin de communication chez Vinci. À discuter
avec ton formateur·rice.
