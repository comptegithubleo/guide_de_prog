# Opérateurs relationnels
---
*Pré-requis :*
- [Variables et types de données - Niveau 1](../datatypes/COURS_variables_lvl_1.md)

Vous les avez surement déjà vu en mathématiques, les opérateurs **relationnels** sont là pour comparer deux expressions, deux valeurs.
La syntaxe change selon le langage et ne correspondent pas exactement aux signes mathématiques, mais la logique reste la même.
Attention car ce sont des opérateurs **logiques**, leur résultat donne **Vrai** ou **Faux**

## Opérateur `!`
L'opérateur point d'exclamation signifie **NON**.
Non quoi ? Non à tout. Pas très fun, c'est la **négation booléenne**.
Prenons comme exemple vous, vous êtes magnifique. On pourrait créer une variable **booléenne**, que l'on appellerait "`magnifique`" et à laquelle on affectera la valeur  `True` (en français: "Vrai").

Si j'affiche la variable `magnifique`, je devrais voir `True` ! Jusque là c'est normal.
Si j'affiche en revanche `!magnifique`, je devrais voir `False` !
Même en langage courant, si c'est NON vrai, alors c'est faux. Si c'est NON faux, alors c'est vrai.

## Opérateurs `==` et `!=`
Pour tester l'égalité entre deux membres, on utilise l'opérateur `==` pour savoir s'ils sont égaux, ou l'opérateur `!=` pour savoir s'ils sont inégaux (`!=` veut littéralement dire`NON égal ?`)
C'est littéralement la question "est ce que c'est égal ?" ou "est ce que ce n'est pas égal ?"
Il peut prendre plusieurs formes:
- `===` en Javascript
- `equals()` (syntaxe d'appel de [fonction](../fonctions/COURS_fonctions_lvl_1.md) !), ou `==` en Java 
- etc ...

### Exemple
En C:
```c
int a = 1;
int b = 2;
printf("%d\n", a == b);
```
Nous affiche `0` pour dire `False`. Si 

En python:
```python
a = 1
b = 2
print(a == b)
```
## Opérateurs `>`, `<`, `>=`, `<=`
Ceux là son assez 


`==`, `!=`, `>`, `<`, `>=`, `<=`