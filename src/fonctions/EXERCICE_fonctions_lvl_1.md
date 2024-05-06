# Exercices - Fonctions
---

## Q1 : Une fonction, peut-elle être définie mais pas appelée ?
<details>
  <summary>Réponse</summary>

**Oui**.

Une fonction peut être définie, mais pas forcément appelée, pas forcément utilisée !

La fonction est bien là, elle existe dans le programme, mais dans ce cas ne servira pas pour le moment.

En revanche, on ne peut pas appeler une fonction si elle n'est pas définie !

</details>

---

## Q2 : Qu'affichera ce code ?

Tips : L'exécution commence dans la fonction **main**.\
La fonction **printf** sert à afficher des éléments, et le `\n` à la fin des phrases sert à marquer une fin de ligne (il ne s'affichera pas)
```c
#include <stdio.h>

int seBallader() {
  printf("je me ballade\n");
  return 0;
}

int sePerdre() {
  printf("je suis perdu dans la forêt\n");
  return 0;
}

int main() {

  sePerdre();
  seBallader();

  return 0;
}
```
<details>
  <summary>Réponse</summary>

```
je suis perdu dans la forêt
je me ballade
```
En effet, la fonction `main` commence et exécute la première instruction, c'est à dire l'appel de la fonction `sePerdre`.

La baguette d'exécution est donnée à la fonction `sePerdre`, pendant que `main` attends la fin de l'exécution de celle-ci.

`sePerdre` exécute ses instructions et "je suis perdu dans la forêt" s'affiche en marquant une fin de ligne, puis retourne 0 à l'ordinateur, qui rends la baguette de l'exécution à la fonction `main`.

De là, la fonction `main` exécute sa prochaine instruction, c'est l'appel de la fonction `seBallader`, qui vous l'avez deviné, affiche "je me ballade", retourne 0, rends la baguette d'exécution à `main` qui elle aussi retourne 0, et tout est terminé.

</details>

---

## Q3 : Qu'affichera ce code ?
```c
#include <stdio.h>

int babord() {
  printf("a gauche!\n");
  return 0;
}

int tribord() {
  babord();
  printf("a droite!\n");
  return 0;
}

int main() {
  tribord();
  return 0;
}
```
<details>
  <summary>Réponse</summary>

```
a gauche!\
a droite!
```
La fonction `main` appelle `tribord`.

`tribord` exécute donc ses instructions. La première est un appel vers la fonction `babord`, et lui donne donc la baguette d'exécution. Cela signifie que l'ordinateur n'exécute pas la ligne `printf("a droite!\n");` pour le moment !

La fonction `babord` s'exécute, et affiche `a gauche!`, puis elle rend le contrôle de l'exécution à la fonction `tribord` qui affichera `a droite!`, qui elle-même rend le contrôle de l'exécution à la fonction `main`, qui s'arrête ensuite.

</details>
