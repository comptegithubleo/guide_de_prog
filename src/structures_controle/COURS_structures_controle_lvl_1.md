# Niveau 1 - Blocs et portées
---
*Pré-requis :*
- [Variables et types de données - Niveau 1](../datatypes/COURS_variables_lvl_1.md)

# Sommaire
<!-- toc -->

---
Rappelez-vous que pour l'instant on définit le code comme une **recette de cuisine** qui s'exécute de façon séquentielle.\
Pour organiser un code, on le place dans des "blocs". Les structures de contrôle sont une famille de concepts qui vont nous permettre de contrôler le flot de l'exécution ! Très stylé.

 > [!IMPORTANT]
 > Un code à une "portée", il existe dans un **contexte d'exécution**. Si on sort du bloc où il est définit, on ne peut plus y accéder.

## Bloc par bloc
 Beaucoup de blabla et pas beaucoup de sens peut-être. Voyons un exemple en C:
```c
{
	//ceci est un bloc délimité par des accolades
}
```
Comme toujours, la syntaxe change beaucoup entre les langages, mais beaucoup utilisent les accolades. Ce bloc là est très joli, on va lui ajouter une variable !
```c
{
	int a;
}
```
La **portée** de cette variable commence à partir de la ligne où on l'initialise, et la fin du bloc.
```c
{
	int a;
}
a = 1;
```
Ce code donne une erreur ! On accède à une variable en dehors de sa **portée**, aux yeux de l'ordinateur elle n'existe plus !

## Attrapez les blocs
Si vous avez compris le principe derrière ces blocs, c'est gagné. Bravo.\
A partir de maintenant, selon le langage et sa syntaxe, repérez ces blocs pour mieux comprendre l'exécution du code.

Si je vous jette la fonction `main` en C dans les mains, vous verriez ça :
```c
int main() {
	int a = 1;
	return 0;
}
```
Pas la peine de tout comprendre, on voit les accolades, on comprends le bloc.

Pourquoi pas une fonction `main` en Python !
```c
def main():
	a = 1
```
Bizarre, du côté du serpent les blocs sont gérés par l'indentation, et seulement au niveau des **fonctions**. Peut importe c'est le même principe !

Je vous donne maintenant une structure de condition en C. Attrape !
```c
if (condition) {
	int a;
} else {
	//code
}
a = 2; //ERREUR
```
On voit aussi les accolades, si une variable est définie entre les premières accolades, elle n'existera pas entre les deuxièmes (puisqu'on est sorti de sa portée et qu'elle n'existe plus !)

## [Exercices !](EXERCICE_structures_controle_lvl_1.md)
