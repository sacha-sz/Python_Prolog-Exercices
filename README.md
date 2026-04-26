# 📚 IA02 - Travaux Pratiques en Python & Prolog

Ce dépôt regroupe l'ensemble des codes sources réalisés dans le cadre de l'UV **IA02** à l'UTC, dédiée à la **logique, à la vérification formelle et à la représentation des connaissances**.

Les programmes sont écrits en **Python** et **Prolog**, organisés par **TP** et **TD**, chacun dans un dossier indépendant.

<br/>

## 📌 Vue d'ensemble

| # | Thème principal | Dossier | Langage |
|---|----------------|---------|---------|
| TP1 | Model Checking - vérification d'interprétations logiques | [`TP/TP1/`](TP/TP1/) | Python |
| TP2 | Solveur SAT - coloration de graphe par encodage CNF | [`TP/TP2/`](TP/TP2/) | Python |
| TP3 | Résolution du Sudoku par solveur SAT | [`TP/TP3-Sudoku/`](TP/TP3-Sudoku/) | Python |
| TP4 | Mastermind en Prolog | [`TP/TP4-Mastermind/`](TP/TP4-Mastermind/) | Prolog |
| TP5 | Résolution du Sokoban par recherche dans un graphe | [`TP/TP5-Sokoban/`](TP/TP5-Sokoban/) | Python |
| TD | Exercices Prolog & MinMax | [`TD-Prolog/`](TD-Prolog/) | Prolog / Python |

<br/>

## 🗂 Détail des exercices

### TP1 - Model Checking

Implémentation d'un **vérificateur de modèle** pour la logique propositionnelle :

| Fichier | Contenu |
|---------|---------|
| `TP1.py` | Décomposition binaire, évaluation d'interprétations, vérification de formules logiques |

> 📄 Sujet : [`TP1-Sujet.html`](TP/TP1/TP1-Sujet.html)

---

### TP2 - Solveur SAT : coloration de graphe

Encodage d'un problème de **coloration de graphe** en CNF puis résolution par un solveur SAT :

| Fichier | Contenu |
|---------|---------|
| `coloration.py` | Génération des clauses CNF (unicité et exclusion de couleur par sommet et par arc), appel au solveur |
| `coloration.cnf` | Fichier CNF généré pour le graphe de coloration |
| `CNF/` | Jeux de tests CNF variés (licorne, dubois, sudoku, zebra, hole6…) |

> 📄 Sujet : [`TP2-Utilisation_de_solveurs_SAT.pdf`](TP/TP2/TP2-Utilisation_de_solveurs_SAT.pdf)

---

### TP3 - Résolution du Sudoku par SAT

Encodage d'une grille de **Sudoku** en formule CNF et résolution par solveur SAT :

| Fichier | Contenu |
|---------|---------|
| `sudoku.py` | Encodage CNF des contraintes Sudoku (unicité, lignes, colonnes, blocs), lecture de grille, affichage de la solution |
| `sudoku.txt` | Grille Sudoku d'entrée |
| `sudoku.cnf` | Formule CNF complète générée |
| `objectif_sudoku.cnf` | CNF de l'objectif seul (contraintes de la grille initiale) |
| `grille_test.png` | Aperçu de la grille de test |
| `Sudoku_with_solution.jpg` | Grille résolue |

---

### TP4 - Mastermind en Prolog

Implémentation du jeu **Mastermind** en Prolog par programmation logique et contraintes :

| Fichier | Contenu |
|---------|---------|
| `Mastermind-Game.pl` | Prédicats de base : `nBienPlace`, `longueur`, `gagne`, `element`, génération et vérification de combinaisons |
| `Mastermind-Game-Bonus.pl` | Version étendue avec stratégie de résolution améliorée |

---

### TP5 - Sokoban

Résolution automatique du jeu **Sokoban** par recherche dans un graphe d'états :

| Fichier | Contenu |
|---------|---------|
| `sokoban.py` | Représentation de l'état (plateau, joueur, caisses, objectifs), génération des successeurs, algorithme de recherche |

---

### TD - Prolog & MinMax

Exercices de TD réalisés en Prolog et Python :

| Fichier | Contenu |
|---------|---------|
| `TD6-premiers_pas.pl` | Arbre généalogique d'Œdipe - prédicats `pere`, `mere`, `epoux`, `ancetre` |
| `TD7-Liste_en_Prolog.pl` | Manipulation de listes - `tete`, `reste`, `element`, `longueur`, `append` |
| `TD8-Somme-Maison.pl` | Résolution par génération et test - contraintes sur des chiffres |
| `TD11-MinMax.py` | Algorithme MinMax pour le jeu de morpion (Tic-Tac-Toe) - évaluation, successeurs, décision optimale |
| `labdacides2.png` | Arbre généalogique de la famille des Labdacides (Œdipe) |

<br/>

## 🛠 Exécution

### Python (TP1, TP2, TP3, TP5, TD11)

Python 3 est requis.

```bash
# Lancer le model checker (TP1)
python TP/TP1/TP1.py

# Générer et résoudre la coloration de graphe (TP2)
python TP/TP2/coloration.py

# Résoudre le Sudoku par SAT (TP3)
python TP/TP3-Sudoku/sudoku.py

# Résoudre le Sokoban (TP5)
python TP/TP5-Sokoban/sokoban.py

# Lancer l'algorithme MinMax morpion (TD11)
python TD-Prolog/TD11-MinMax.py
```

### Prolog (TP4, TD6, TD7, TD8)

Un interpréteur Prolog standard suffit (SWI-Prolog recommandé).

```bash
# Installer SWI-Prolog (Linux/macOS)
sudo apt install swi-prolog    # Debian/Ubuntu
brew install swi-prolog        # macOS

# Charger le Mastermind (TP4)
swipl -l TP/TP4-Mastermind/Mastermind-Game.pl

# Charger les exercices TD6
swipl -l TD-Prolog/TD6-premiers_pas.pl
```

<br/>

## 🧰 Technologies utilisées

- **Python 3** - model checking, encodage SAT, résolution de puzzles, MinMax
- **Prolog / SWI-Prolog** - programmation logique, Mastermind, exercices TD
- **Format CNF (DIMACS)** - encodage des problèmes de satisfiabilité propositionnelle

<br/>

## 📄 Licence

Ce projet est distribué sous licence **MIT** - voir le fichier [LICENSE](LICENSE) pour plus d'informations.

<br/>

## 👤 Auteur

- **[@sacha-sz](https://github.com/sacha-sz)**

<br/>

## 🔗 Références

- [🔒 Cours IA02 sur Moodle (accès UTC requis)](https://moodle.utc.fr/enrol/index.php?id=1002)
- [UTC - Université de Technologie de Compiègne](https://www.utc.fr/)
- [SWI-Prolog](https://www.swi-prolog.org/)
- [Format CNF DIMACS](https://people.sc.fsu.edu/~jburkardt/data/cnf/cnf.html)

## :technologist: - Langage utilisé

- [Python](https://www.python.org/)
- [Prolog](https://www.wikiwand.com/en/Prolog)

## :memo: - Licence

[MIT](LICENSE)

## :notebook_with_decorative_cover: - Auteurs et contributeurs

- **sacha-sz** - Tous les TP - [sacha-sz](https://github.com/sacha-sz/)
- **LucasColas**  - Collaboration sur les TP - [LucasColas](https://github.com/LucasColas/)

## :bookmark_tabs: - Références

- **Lien moodle vers le cours**, (nécessite d'être connecté pour y accéder): [UTC-IA02](https://moodle.utc.fr/course/view.php?id=20)
- **Python** :
  - **Documentation Python 3.10**, [URL](https://docs.python.org/fr/3.10/)
  - **Tutoriel Python 3.10**, [URL](https://docs.python.org/fr/3.10/tutorial/)
- **Prolog** :
  - **Utilisation de swi-prolog** : [URL](https://swish.swi-prolog.org/)

## Aide

Si vous téléchargez SWI-Prolog sur votre ordinateur, voici les codes à saisir dans terminal pour ouvrir le fichier *.pl :
> swipl *.pl
