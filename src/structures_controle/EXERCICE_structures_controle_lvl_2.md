# Exercices - Opérateurs
---

## Q1 : Qu'affiche ce programme ?
```c
int main() {
  if (1 == 1) { printf("1 = 1"); }

  if (1 == 2) {
    printf("1 = 2");
  }
  else { printf("1 != 2"); }

  return 0;
}
```
<details>
  <summary>Réponse</summary>

Le code affiche

`1 = 1`

`1 != 2`

On voit quelque chose de nouveau. Le premier `if` n'a pas de clause `else` à sa suite ! Et oui ça arrive. Ici, 1 est égal à 1 ! Donc on rentre dans la boucle `if`, et on affiche `1 = 1`.

Ensuite, on teste si 1 est égal à 2. Comme ce n'est pas le cas, la condition n'est pas satisfaite, donc on passe dans la structure de contrôle alternative `else`, qui nous demande d'afficher `1 != 2`

</details>

---

## Q2 : Plus dur, qu'affiche ce programme ?
```c
int main() {
  int a = 5;

  if (a < 1) {
    if (a == 5) {
      printf("ta\n");
    } else {
      printf("ren\n");
    }
    printf("tu\n");

  } else {
    printf("le!\n");
  }

  return 0;
}
```
<details>
  <summary>Réponse</summary>

Il affiche `le!`.

Si vous avez pas compris pourquoi, alors **BLOCS BLOCS BLOCS BLOCS !**

Désolé si je vous ai fait extrêmement peur, mais au moins ça restera gravé à jamais dans votre mémoire jusqu'à vos derniers instants.

La clé, c'est le raisonnement par blocs, regardez comment c'est joli. Vous voyez la fonction `main` ? Écrivons là en **repliant** ses instructions sur elle-même, en version **compacte** si vous préférez :
```c
int main() {
	// code ...
}
```
En [pseudo-code](../definitions/pseudo_code.md), j'ai le droit d'écrire comme ça, parce que j'ai envie. Pour l'instant rien de difficile, on a juste replié la fonction principale. Et pourtant c'est la clé pour le reste. On peut aussi replier les blocs `if`, et tous les autres :

```c
int main() {
	int a = 5;

	if (a < 1) {
		//code ...
	} else {
		printf("le!");
	}
	return 0;
}
```
Ici j'ai replié la première instruction `if` sur elle-même, c'est le premier test que l'ordinateur fait puisque c'est la première ligne qui arrive après l'affectation `int a = 5`.

L'ordinateur teste si `a < 1`, comme c'est faux (car ` 5 < 1` est faux), on ne rentre meme pas dans le bloc du `if` ! Pas la peine de s'embêter. Puisqu'on a un `else`, on rentre dedans, et on affiche `le!`.

En revanche, si la condition était vraie, alors on serait rentré dans l'instruction `if` et là il aurait fallu exécuter le reste, etc...

</details>

---

## Q2.2 : Bonus question 2 ! la valeur de `a` change, qu'affiche le programme ?
```c
int main() {
  int a = -5;

  if (a < 1) {
    if (a == 5) {
      printf("ta\n");
    } else {
      printf("ren\n");
    }
    printf("tu\n");

  } else {
    printf("le!\n");
  }

  return 0;
}
```
<details>
  <summary>Réponse</summary>

Il affiche

`ren`

`tu`

Alors ? Si c'est encore compliqué, on peut essayer d'aller plus doucement.

L'ordinateur voit d'abord `int a = -5`. Ca c'est ok on connaît.

Ensuite il doit faire le test : `a < 1`. Dans notre cas, c'est **vrai** car -5 < 1. Comme la condition est **vraie**, on rentre dans le bloc du `if`, et on se rappelle que l'on éxécutera pas son bloc `else` ! C'est soit l'un soit l'autre.

Une fois dedans, l'ordinateur voit ça :

```c
if (a == 5) {
      printf("ta\n");
} else {
      printf("ren\n");
}
printf("tu\n");
```
Donc on doit tester une autre condition : `a == 5` dans notre cas est **faux** donc on ne rentre pas dans la boucle `if`, mais on exécute le code dans `else`, c'est à dire qu'on affiche `ren` !

Et là, après le `else`, on a encore une dernière instruction à éxécuter. Elle ne fait pas partie du `if/else` imbriqué, elle est en réalité dans le premier `if` dans lequel on est rentré. On affiche donc `tu`.

</details>

---
