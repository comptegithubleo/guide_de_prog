# Exercices - Variable de base
---
## Q1 : Citez quelques types d'une variable
<details>
  <summary>Réponse</summary>

- Entier naturel : *int*

- Nombre réel : *float*

- Booléen : *bool*

- Caractère : *char*  
</details>

---

## Q2 : Quelle est la syntaxe de la déclaration d'une variable en C ?
<details>
  <summary>Réponse</summary>

Attention à cette subtilité, le langage C à besoin d'un point virgule quand on termine une **instruction** ! C'est normal de ne pas le savoir.

`type_var nom_var = valeur_var;`, par exemple `int a = 1;`
</details>

---

## Q3 : Déclarez trois variables en C avec les valeurs 9.835, 5, et False respectivement, et choisissez les types les plus adéquat
<details>
  <summary>Réponse</summary>

`float variable1 = 9.835;`
- Comme 9.835 n'est pas un entier mais un nombre réel, on utilise le type *float*.

`int variable2 = 5;`
- Comme 5 est un entier, on utilise le type *int*. Notez qu'on aurait aussi pu utiliser le type *float*, on n'aurait eu aucune **perte d'information**, ça aurait été l'équivalent de 5.00000 ...

`bool variable3 = 0;`
- Attention ici, "False", ou "false", n'est pas reconnu en C ! Cependant dans d'autres langages, comme en Python, `a = False` est tout à fait valide. Comprennez bien le **principe**, retenez bien la **syntaxe**.

</details>

---

## Q4 : Déclarez trois variables en Python avec les valeurs 5, 0.01 et "Bonjour" respectivement.
<details>
  <summary>Réponse</summary>

` a, b, c = 5, 0.01, "Bonjour"`

Wow. Si simple, et si pratique. C'est aussi un sacré piège car Python est très permissif, et permet d'omettre non seulement les types, mais aussi de déclarer sur la même ligne plusieurs variables !

Mais ne vous laissez pas trop séduire par son accessibilité, l'apprentissage du C en parallèle aidera à consolider les bases. Gardez en tête la vaste différence des syntaxes !

</details>

---

## Q5 : Quelle sera la valeur de la variable mouton à la fin de l'exécution du programme ?
```c
int mouton = 1;
int berger = 2;

mouton = berger + 10;
```
<details>
  <summary>Réponse</summary>

**mouton** sera égal à `berger + 10`, c'est à dire `2 + 10` car `berger = 2` donc `mouton = 11` !

Syntaxe à part, la logique est là. Les **noms de variables** sont remplacés par l'ordinateur à l'exécution par leur valeur respective. Berger, devient 2. Mouton, devient 11.

Si on regarde la syntaxe, on relève plusieurs choses, le mot `mouton` à la 4ème ligne n'a pas de type ! (il n'est pas précédé par le terme *int*)

On étudie ça dans la partie [Opérateurs - Niveau 1](/operateurs/COURS_operateurs_lvl_1.md) !

</details>