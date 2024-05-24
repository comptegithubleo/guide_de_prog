# Exercices - Opérateurs
---

## Q1 : Est ce que ce code renvoie une erreur ?
```c
int main() {
	{
		int a = 1;
	}
	a = 2;
	return 0;
}
```
<details>
  <summary>Réponse</summary>

Le code est **invalide**.

On a vu ensemble les blocs de code, et qu'en C par exemple c'est les accolades qui les délimitent.

Ici `a` est initialisée dans un bloc, puis en dehors de celui ci on essaie d'accéder à la variable `a`, mais dans ce **contexte** d'exécution, elle n'existe pas !

Un code valide serait
```c
int main() {
	//on initialise et accède à la variable dans le meme bloc, c'est ok !
	{
		int a = 1;
		a = 2;
	}
	return 0;
}
```
ou bien
```c
int main() {
	//ici on s'est complètement affranchi du bloc qui posait problème
	//on remarque qu'on reste quand meme dans une fonction qui elle aussi est un bloc
	int a = 1;
	a = 2;
	return 0;
}
```

</details>

---

## Q2 : Plus difficile, est ce que ce code renvoie une erreur ?
```c
int main() {
	int a = 1;
	{
		a = 2;
	}
}
```
<details>
  <summary>Réponse</summary>

Le code est **valide**.

Ca peut paraître étrange, mais la ligne `int a = 1` est dans le bloc de la **fonction**. Donc pour toute la portée de la fonction, et donc les lignes suivantes jusqu'à la fin de la fonction, la variable existe !

Quand on ouvre ensuite le petit bloc où l'on place `a = 2`, on hérite des objets déjà existants dont la variable `a` déjà existante, et on peut la modifier !

</details>

---

## Q3 : Encore plus dur, est ce que ce code renvoie une erreur ?
```c
int main() {

  {int a = 1;} a = 2;
}
```
<details>
  <summary>Réponse</summary>

Le code est **invalide**, et moche.

Ici le plus important c'est de comprendre qu'il n'y a pas vraiment de règles en C pour le formatage, comparé à d'autres langages. Regardez [Les bonnes pratiques](../definitions/bonnes_pratiques.md) qui à un bon exemple.

En corrigeant le formatage, on peut réécrire la fonction comme ceci:

```c
int main() {

	{
		int a = 1;
	}
	a = 2;
}
```
Là on comprends mieux que la ligne `a = 2` ne peut pas accéder à la variable.

</details>

---
