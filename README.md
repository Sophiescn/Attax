# ATTAX - Jeu de plateau

ATTAX est une variante du jeu Reversi (Othello) développée en langage C utilisant la bibliothèque graphique MLV.

## Description

ATTAX est un jeu de plateau à deux joueurs où l'objectif est de contrôler le plus de cases possible en fin de partie. Vous placez vos pions sur le plateau et contaminez les pions adverses adjacents pour les convertir à votre couleur.

## Fonctionnalités

Le jeu propose plusieurs modes et options :

- **Modes d'affichage** :
  - `-a` : Mode ASCII (console)
  - `-g` : Mode graphique (interface MLV)

- **Modes de jeu** :
  - `-h` : Joueur contre Joueur
  - `-o` : Joueur contre Ordinateur

- **Options supplémentaires** :
  - `-s` : Plateau avec des cases "trous" sur lesquelles on ne peut pas jouer
  - `-p` : Contamination avec probabilité (75% de chance de convertir un pion adverse)

## Prérequis

- GCC ou autre compilateur C
- Bibliothèque MLV installée

## Installation

1. Clonez ce dépôt ou téléchargez le code source
2. Compilez le programme avec la commande :
   ```
   gcc -o attax Attax.c -lMLV
   ```

## Utilisation

Pour lancer le jeu, utilisez une des commandes suivantes :

```
./attax -a -h        # Mode ASCII, Joueur contre Joueur
./attax -a -o        # Mode ASCII, Joueur contre Ordinateur
./attax -g -h        # Mode Graphique, Joueur contre Joueur
./attax -g -o        # Mode Graphique, Joueur contre Ordinateur
```

Vous pouvez ajouter une option supplémentaire (`-s` ou `-p`) :

```
./attax -g -o -s     # Mode Graphique, Joueur contre Ordinateur, avec cases trous
./attax -a -h -p     # Mode ASCII, Joueur contre Joueur, avec probabilité de contamination
```

## Comment jouer

1. Lancez le jeu dans le mode de votre choix
2. En mode ASCII, entrez les coordonnées où vous voulez jouer (entre 1 et 7)
3. En mode graphique, cliquez sur la case où vous voulez jouer
4. Le but est de finir avec plus de pions que votre adversaire

## Règles du jeu

- Les joueurs jouent à tour de rôle en plaçant un pion de leur couleur
- Quand vous placez un pion, il contamine tous les pions adverses adjacents (horizontalement, verticalement et en diagonale)
- En mode probabilité, chaque contamination a 75% de chance de réussir
- La partie se termine quand le plateau est plein ou qu'un joueur n'a plus de pions
- Le joueur avec le plus de pions à la fin remporte la partie

## Structure du code

Le code est organisé autour de la structure `Plateau` qui gère :
- La représentation du plateau de jeu
- Les joueurs et leurs scores
- Les coordonnées pour l'affichage graphique

## Auteurs

- Cousson Sophie
- Naudin Maxime

## Date

Décembre 2021
