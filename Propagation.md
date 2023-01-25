# ✥ TP - Propagation ✥

## Exercice 1 
### Typage
Déclarer une constante représentant un nombre de personne
Déclarer un type matrice , qui sera une matrice carré de taille du nombre de personne et contenant des booléens
Elle nous sera utile pour se souvenir de qui à vu qui

## Exercice 2 
### Lecture 
Réaliser une méthode qui à partir d'un nom de fichier va remplir une matrice, via le contenu dans le fichier qui aura sur chacune de ces lignes deux entier signifiant que la personne a à vu la personne b

## Exercice 3
### Core 
Faire une méthode `vue` qui à partir d'une matrice et d'un entier représentant une personne affiche toutes les personnes qu'elle a vu directement ou indirectement ( si a à vu directement b et b à vu directement c alors a à vu indirectement b et c )

## Exercice 4 
### Un soucis ?
La méthode `vue` comporte un problème, lequel ? 

## Exercice 5 
### Correctif
Il existe plusieurs solution pour pallier à ce problème nous utiliserons un tableau de booléen interne à la fonction pour garder en mémoire qui a été déjà vu afin de ne pas boucler à l'infini

## Exercice 6 
### L'objectif
L'objectif final est d'obtenir une image de l'évolution de comment se répand une information ou une maladie au sein d'une population pour cela on va remplacer le type booléen du tableau par des entier avec -1 par défaut 
0 pour la personne de base 1 pour ces voisins direct 2 pour les voisin des voisins etc

## Exercice 7
### Utilitaire
Faire une fonction `toChar` qui retourne une lettre majuscule correspondant à l'enteir fourni en paramètre

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
Réaliser un programme principal qui demande à utilisateur un nom de fichier (sans l'extention)
utilise la fonction de lecture de fichier sur le nom du fichier `.txt` 
enregistre l résultat de  la fonction `générerImage` dans le nom du fichier `.dot`

## Exercice  10 
### Test
Si vous avez bien tout fait à partir des différents fichier disponibles vous pourrez faire la commande
`./monProgramme.out | dot -Tpng -o resultat.png && firefox resultat.png`

## Fichiers source