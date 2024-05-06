# Opérateurs de base
---
*Pré-requis :* [Variables et types de données - Niveau 1](/variables_datatypes/COURS_variables_lvl_1.md)
## Opérateur `=`
Calculer c'est bien. Mais sans stocker la valeur, on ne peut pas faire grand chose !\
Souvenez-vous que l'ordinateur remplace à l'exécution les variables par leurs valeurs. Si par exemple `poulailler` à été **déclaré** et vaut 3, et `loup` lui aussi **déclaré** et vaut 4, alors :
```c
poulailler = loup + 2;
```
stockera dans la variable `poulailler` la valeur `loup + 2`, ou plutôt `3 + 2` car `loup` vaut 3.

Remarquez une chose importante pour la syntaxe du C, le nom de variable n'est pas précédé par son type ! On a pas écrit `int poulailler` mais bien `poulailler` tout court !\
La différence est que l'emploi du type va dicter si on **déclare** ou si on **accède** à une variable.
```c
int b = 0;
b = 1;
b = b;
b = 89;
a = 2;
int b = 2;
```
Dans ce code, la dernière ligne utilise le type, mais ça ne sert à rien car **b existe déjà**. Or, pour la ligne `a = 2`, on aura une erreur car **a n'existe pas encore**, elle n'a pas été **initialisée** ! Il faudrait écrire `int a;` juste avant, ou `int a = 0;`

Comprendre ça est clé pour comprendre les objets qu'on manipule.\
Définir ou déclarer, j'utilise le type.\
Accéder, lire, modifier, je n'utilise pas le type.

## Opérateurs `+`, `-`, `/`, `*`, `%`
Ces opérateurs sont les mêmes qu'en mathématiques, avec addition, soustraction, division, multiplication et modulo respectivement.\
Voyons comment ils fonctionnent :
``` c
int cagette = 1;
int pissenlit = 2;
cagette = (pissenlit + cagette) / 2
```
Un peu complexe, mais on fait un calcul de maths. Souvenez-vous l'ordinateur **remplace** les variables. Pour lui la dernière ligne demande :
`mets dans la variable cagette la valeur (2 + 1) / 2`
## [Exercices !](/operateurs/EXERCICE_operateurs_lvl_1.md)