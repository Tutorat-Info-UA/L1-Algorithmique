# 💯 Fake Exam P3 💯

## 1. 
### Comment calculer π ?

La suite de NewtonLeibniz est définie ainsi : 
> `NL₀ = 1`
> `NLₐ₊₁ = NLₐ - 1/(2a-1)` si a est pair
> `NLₐ₊₁ = NLₐ + 1/(2a-1)` si a est impair

Donner le code récursif de :
```cpp
float NewtonLeibniz(int a)
``` 

 _Lore : quand  `a` tend vers l'infini alors `NLₐ` tend vers `π/4` et en plus si a est pair `NLₐ>π/4` et inversement, c'est une méthode qui a été longtemps utilisé par les mathématiciens pour obtenir une approximation de π pour des calculs._


## 2. 
### Compatibilité ?!
On dit que deux tableau de taille `n` sont compatible si la somme de la i-ème case du premier tableau multiplier par la i-ème case du second tableau pour tous les `i` de 1 à `n`  vaut 0.

Donner le code de : `compatible` en récursif qui permet de faire fonctionner ce code :
```cpp
#include <array>
#include <iostream>

using tab = std::array< int , 5 >;

int main() {
  tab a = { 6, 8, 9, 0, 3}, b = {7 , 0 , 12 , 8 , 3};
  if( compatible( a , b , 4 ) ) {
    std::cout << "a et b est compatible" << std::endl;
  }
  return 0;
} 
```


## 3.  
### Marine
#### a. 
Définir le type structuré `pays` qui contient le nom d'un pays, un nombre de porte-avion et  de cuirassé et de croiseur ainsi que de destroyer. Ainsi qu'un tableau dynamique de chaîne de caractère pour stocker les noms des portes-avions.

#### b. 
Définir que le type structuré `monde` qui est un tableau dynamique de `pays`

#### c. 
Définir une méthode `import` qui permet de charger depuis un fichier avec son nom en paramètre avec un monde qui permet de lire le fichier. _`FakeExamP3.txt`_
La première ligne contient ainsi le nombre de pays dans le monde puis sur chaque ligne suivante
Le nom du pays suivi du nombre de destroyer de croiseur de cuirassé et enfin de porte-avions et ensuite n nom de porte avions

#### d. 
Faire une fonction `plusPuissant` qui retourne vrai si et seulement si la première nation donné est plus puissante que la seconde dans un monde fournis en paramètre. La puissance est calculer par la somme de :
 - 35 pts par destroyer
 - 45 pts par croiseur
 - 60 pts par cuirassé
 - 100 pts par porte-avions 

#### e. 
Faire en itératif une fonction qui retourne le nom du pays le le plus puissant

#### f. 
Faire une méthode neutraliser qui libère la mémoire d'un pays et pacifier qui libère la mémoire d'un monde

#### g. 
Faire un programme principal qui permet de charger un fichier terre.txt et d'afficher le plus puissant et tout ce qui vous semblera aussi utile de faire