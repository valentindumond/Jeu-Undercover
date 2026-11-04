# 🕵️ Undercover

Version console du jeu de société **Undercover**, développée en Python. Les joueurs reçoivent un mot en secret, donnent chacun un indice, puis votent pour éliminer celui qu'ils soupçonnent d'être l'intrus.

Projet réalisé dans le cadre de ma licence d'informatique.

## 🎮 Règles

- 4 joueurs minimum
- Chaque joueur reçoit un rôle tiré au hasard :
  - **Innocents** : ils ont tous le même mot
  - **Undercover** (1) : il a un mot proche de celui des innocents
  - **Mr. White** (1) : il n'a aucun mot (il voit `???`)
- À chaque tour, chaque joueur donne un indice sur son mot sans le prononcer
- Tous votent ensuite pour éliminer un joueur
- Les innocents gagnent quand l'Undercover est éliminé, l'Undercover gagne s'il reste en jeu jusqu'à la fin

## ✨ Fonctionnalités

- Distribution aléatoire des rôles (`random.shuffle`)
- Plus de 100 paires de mots (pomme/poire, chien/chat, plage/mer...)
- Affichage du mot en privé : l'écran est effacé après chaque joueur pour garder le secret
- Ordre de parole mélangé à chaque tour
- Validation des indices : on ne peut pas utiliser son propre mot
- Vote sécurisé : la saisie est refusée si le nom n'est pas dans la liste (`safe_input`)
- Sortie en couleur avec `colorama`
- Affichage des rôles et des éliminés en fin de partie

## 🛠️ Technologies

- Python 3
- `colorama` (couleurs dans le terminal)
- Modules standard : `random`, `os`

## 📖 Exemple de partie

```
Bienvenue dans le jeu Undercover !
Entrez le nombre de joueurs (minimum 4) : 4
Nom du joueur 1 : Alice
...
--- Tour de jeu ---
Alice, donnez un indice sur votre mot : sucré
...
--- Vote ---
Alice, votez pour éliminer un joueur (Bob, Chloé, David) : Bob

--- Résultats du vote ---
Bob : 2 vote(s)

Bob est éliminé.
```

## 🧠 Ce que j'ai appris

Structurer un programme en fonctions, manipuler listes, dictionnaires et ensembles, valider les entrées utilisateur dans une boucle, et gérer la logique d'une partie (rôles, tours, conditions de victoire).

## ⚠️ Limites connues

- Pas de gestion des égalités au vote : le premier joueur le plus voté est éliminé
- Mr. White n'a pas de phase pour deviner le mot
- Deux joueurs ne doivent pas porter le même nom

## 👤 Auteur

Valentin Dumond · [Portfolio](https://valentindumond.github.io/Portfolio/) · [LinkedIn](https://www.linkedin.com/in/valentindumond)
