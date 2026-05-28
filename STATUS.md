# STATUS — Présentation LNE Academy

> Pour reprendre la session demain ou ailleurs.
> Dernière mise à jour : 28 mai 2026

---

## 1. Où on en est

### Livrable principal
- **`index.html`** (~129 KB, autosuffisant) — Deck Reveal.js premium, 30 slides, charte LNE + photos Unsplash + animations cinématiques.
- Versions : 2 commits sur la branche `claude/eager-turing-bqzQ0`
  - `8ccfb3c` — V1 deck interactif
  - `4d6e8cd` — Refonte premium éditoriale (texte allégé, photos, animations)

### Ouverture
- Double-clic sur `index.html` → Chrome (recommandé)
- Navigation : `←` `→` `Espace`
- **Mode présentateur : touche `S`** — affiche slide + notes orales + chrono + slide suivante
- Plein écran : `F`
- Vue d'ensemble : `Échap`

---

## 2. Structure du deck (30 slides)

```
0  Cover                              — tous
1  Problématique + 4 leviers          — intro
2  Diagnostic 4 mots (Légitimité…)    — intro

3  Divider Partie I                   — Jacques + Enzo
4  SWOT                               — Jacques
5  Benchmark 3 familles               — Jacques
6  Standard 0/6                       — Jacques
7  4 insights stratégiques            — Jacques
8  STP                                — Enzo
9  Triptyque B2B                      — Enzo

10 Divider Partie II                  — Vojin
11 Méthodologie (3 corpus)            — Vojin
12 Périmètre + score 31/100           — Vojin
13 Word cloud jargon (78 %)           — Vojin
14 Heatmap 6×5 (cliquable)            — Vojin
15 Radar 4 personas (switchable)      — Vojin
16 Plan 6 actions P1/P2/P3            — Vojin

17 Divider Partie III                 — Kessy-Rose + Louise
18 Cognitif/Affectif/Conatif          — Kessy-Rose
19 Tableau de cohérence               — Kessy-Rose
20 Mix digital (filtre persona)       — Louise
21 Levier A — Refonte site            — Louise
22 Levier B — SEO/SEA                 — Louise
23 Levier C — Content marketing       — Louise
24 Levier D — LinkedIn                — Louise
25 Levier E — Email marketing         — Louise

26 Recommandation phare LNE Academy   — clôture
27 Roadmap P1/P2/P3                   — clôture
28 Sources bibliographiques           — clôture
29 Merci + Q&R                        — clôture
```

Durée cible totale : **15-20 min** (3-4 min par intervenant).

---

## 3. Cadrage validé (à ne pas remettre en question)

| Décision | Choix retenu |
|---|---|
| Périmètre | Toute la présentation collective (5 parties) |
| Format | Slides Reveal.js |
| Style | Rapport conseil premium type McKinsey/BCG |
| Visuels | Photos Unsplash (labo, métrologie, business) |
| Animations | Cinématique / immersif (Ken Burns, particules, blur reveal) |
| Densité texte | 3 bullets max de 5-7 mots — détail dans speaker notes |
| Mode présentateur | Oui, notes orales par slide |
| Connexion internet | OK le jour J (CDN utilisables) |
| Charte | Bleu `#003A70` · Rouge `#E6192D` · Barlow / Barlow Condensed / Fraunces |

---

## 4. À faire avant la présentation

### Bloquant
- [ ] **Pousser sur GitHub** — `git push` est bloqué par le proxy de cet environnement (403). À faire depuis ton poste local :
  ```bash
  git fetch origin
  git checkout claude/eager-turing-bqzQ0
  # ou récupérer index.html via le fichier livré dans le chat
  git push -u origin claude/eager-turing-bqzQ0
  ```
- [ ] **Tester l'ouverture dans Chrome** — vérifier que les photos Unsplash chargent (si une 404, on bascule sur un fallback)
- [ ] **Tester le mode présentateur** — touche `S`, vérifier l'écran 2

### À valider avec l'équipe
- [ ] Lecture des speaker notes par chaque intervenant (Jacques, Enzo, Vojin, Kessy-Rose, Louise) — adapter au ton de chacun
- [ ] Timing : chronométrer les 5 prises de parole
- [ ] Transitions orales entre intervenants (le passage de relais)

### Améliorations possibles si du temps
- [ ] Ajouter le **logo LNE officiel** (image vectorielle) en remplacement du lockup texte
- [ ] Remplacer certaines photos Unsplash si une ne charge pas ou ne plaît pas
- [ ] Faire un export PDF (Reveal supporte `?print-pdf` dans l'URL) en backup si Chrome plante
- [ ] Ajouter une slide "Méthodologie projet" en annexe si le jury la demande

---

## 5. Fichiers du repo

```
LNE/
├── index.html                                        # ← LE DECK
├── CONTEXT_LNE.md                                    # Brief original
├── STATUS.md                                         # ← Ce fichier
├── Projet collectif de recherche en gestion (Groupe 1).pdf   # Livrable écrit source
└── charte-graphique-marques-certification-LNE.pdf    # Charte officielle LNE
```

---

## 6. Backup PDF (si besoin)

Si Chrome devient instable demain, exporter en PDF :
1. Ouvrir `index.html?print-pdf` dans Chrome
2. `Cmd/Ctrl + P`
3. Destination : Enregistrer en PDF
4. Marges : aucune · Arrière-plans : oui
5. Le PDF servira de filet de sécurité (sans interactivité)

---

## 7. Choses à savoir si on reprend dans une nouvelle session

- Tout le contenu vient du PDF `Projet collectif de recherche en gestion (Groupe 1).pdf` (48 pages) — lu et synthétisé dans le deck
- Les photos Unsplash sont hotlinked, pas downloadées — connexion requise
- Les libs (Reveal 5.1, Chart.js 4.4, D3 7.9) sont en CDN jsDelivr
- 3 polices Google Fonts : Barlow, Barlow Condensed, Fraunces
- Les composants interactifs sont en JS vanilla dans la balise `<script>` finale du HTML

---

## 8. Diff potentiel à explorer (si tu veux itérer)

| Slide | Idée d'évolution |
|---|---|
| Cover | Mettre une vraie photo labo LNE si dispo |
| 6 (0/6) | Ajouter un mini-graphique en miroir « 6/6 chez NPL, TÜV, SGS » |
| 14 (heatmap) | Lier chaque cellule vers une capture annotée du site lne.fr |
| 20 (mix) | Ajouter un slide annexe « budget indicatif » par levier |
| 26 (brand) | Animer le reveal du logo lettre par lettre |
| 29 (merci) | Ajouter QR code vers le PDF du livrable écrit |
