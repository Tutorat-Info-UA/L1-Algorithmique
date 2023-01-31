# ✥ TP - Propagation ✥

## Exercice 1 
### Typage
1. Déclarer une constante représentant un nombre de personne (250)
2. Déclarer un type matrice , qui sera une matrice carré de taille du nombre de personne et contenant des booléens. _Elle nous sera utile pour se souvenir de qui à vu qui._

## Exercice 2 
### Lecture 
Réaliser une méthode `import` qui à partir d'un nom de fichier va remplir une matrice, via le contenu dans le fichier qui aura sur chacune de ces lignes deux entier signifiant que la personne a à vu la personne b. Avant de lire le fichier on mettera toutes les cases àa la valeur par défaut : `false`.

Si dans le fichier nous avons :
```txt
3 4
1 2
```
La matrice sera donc :
```txt
0 0 0 0 0
0 0 0 0 0
0 1 0 0 0
0 0 0 0 0
0 0 0 1 0
```

## Exercice 3
### Core 
1. Faire une méthode `vue` qui à partir d'une matrice et d'un entier représentant une ligne, affiche toutes les personnes qu'elle a vu directement. Cela correspond donc à toutes les colonnes où la ligne fourni est à `true`. _conseil : itératif_
2. Améliorrer la méthode `vue` pour aussi gérer les personnes vu indirectement ( si `a` a vu directement `b` et `b` à vu directement `c` alors `a` a vu indirectement `c` ). _conseil : récursif, et une seul ligne suffis_

## Exercice 4 
### Un soucis ?
La méthode `vue` comporte un problème, lequel ? 

## Exercice 5 
### Correctif
Il existe plusieurs solutions pour pallier à ce problème nous utiliserons un tableau de booléen interne à la fonction pour garder en mémoire qui a été déjà vu afin de ne pas boucler à l'infini.

1. Créer un type `tab` qui est un tableau de booléen de la taille du nombre de personne
2. Faire une fonction `initTab` qui initialise un `tab` à faux en tout points
3. Rajouter à la méthode `vue` un paramètre de type `tab`
4. Ne pas faire l'appel récursif si dans `tab` on a déjà vu la personne.

## Exercice 6 
### L'objectif
L'objectif final est d'obtenir une image de l'évolution de comment se répand une information ou une maladie au sein d'une population pour cela on va remplacer le type booléen du tableau par des entier avec -1 par défaut 
0 pour la personne de base 1 pour ces voisins direct 2 pour les voisin des voisins etc

## Exercice 7
### Utilitaire
Faire une fonction `toChar` qui retourne une lettre majuscule correspondant à la n-ième lettre de l'alphabet avec ce `n` en paramètre.

## Exercice 8
### Écriture
Faire une méthode `générerImage` qui prend en paramètre un tableau d'entier une matrice de booléen et un nom de fichier et écrit dans le format suivant les fichiers 

```dot
digraph {
  "A" [shape=circle, style=filled, fillcolor=red]
  "B" [shape=circle, style=filled, fillcolor=green]
  "C" [shape=circle, style=filled, fillcolor=purple]
  "A" -> "B"
  "A" -> "C"
  "B" -> "C"
  "B" -> "A"
}
```
en sachant que la `fillcolor` sera :

valeur | couleur
-------|---------
 -1    | white
 0     | black
 1     | purple
 2     | red
 3     | orange
 4     | yellow
 5+    | green

## Exercice 9
### Fin
Réaliser un programme principal qui :
 - Demande à utilisateur un nom de fichier (sans l'extention)
 - Utilise la fonction de lecture de fichier sur le nom du fichier avec `.txt` 
 - Demande à utilisateur une source (un entier n compris entre 1 et la constante)
 - Propage l'information à l'aide de la méthode `vue`
 - Utilise le résultat dans le tableau de la méthode `vue` pour `générerImage` avec le nom du fichier avec `.dot`

## Exercice  10 
### Test
Si vous avez bien tout fait à partir des différents fichier disponibles vous pourrez faire la commande
`./monProgramme.out | dot -Tpng -o resultat.png && firefox resultat.png`

## Fichiers source
_à coté de fichier vous trouverez une archive contenant pleins d'exemples!_