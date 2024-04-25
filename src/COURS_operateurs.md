# Niveau 1
---
*Pré-requis :* [[pro/mentorat/guide_de_prog/src/variables_niveau_1#Niveau 1]]

En informatique, les opérateurs ressemblent énormément aux opérateurs mathématiques.
On va voir comment un ordinateur procède pour ce genre de tâches.
## Opérateur `=`
Calculer c'est bien. Mais sans stocker la valeur, on ne peut pas faire grand chose !
Souvenez-vous que l'ordinateur remplace à l'exécution les variables par leurs valeurs. Si par exemple `poulailler` à été **déclaré** et vaut 3, et `loup` lui aussi **déclaré** et vaut 4, alors :
```c
poulailler = loup + 2;
```
stockera dans la variable `poulailler` la valeur `loup + 2`, ou plutôt `3 + 2` car `loup` vaut 3.

Remarquez une chose importante pour la syntaxe du C, le nom de variable n'est pas précédé par son type ! On a pas écrit `int poulailler` mais bien `poulailler` tout court !
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

Comprendre ça est clé pour comprendre les objets qu'on manipule.
Définir ou déclarer, j'utilise le type.
Accéder, lire, modifier, je n'utilise pas le type.

# Opérateurs `+`, `-`, `/`, `*`
Ces opérateurs sont les mêmes qu'en mathématiques, avec addition, soustraction, division et multiplication respectivement.
Voyons comment ils fonctionnent :
``` c
int cagette = 1;
int pissenlit = 2;
cagette = (pissenlit + cagette) / 2
```
Un peu complexe, mais on fait un calcul de maths. Souvenez-vous l'ordinateur **remplace** les variables. Pour lui la dernière ligne demande :
`mets dans la variable cagette la valeuur (2 + 1) / 2`
## Exercice

> [!question]- Q1 : Quelle est la valeur de la variable `b` à la fin de l'exécution du programme ?
```c
int a = 1;
int b = 0;
b = 3;
b = a;
```
> [!question]- Q1 Réponse
> **b = 1**
> On va comprendre ligne par ligne
> 1ere ligne, `a` = 1 et `b` n'existe pas encore !
> 2eme ligne, `b` est initialisé à 0 (et `a` existe toujours)
> 3eme ligne, `b` vaut 3, c'est à dire qu'on met la valeur 3 dans la boîte `b`
> 4eme ligne, `b` vaut `a`, et comme `a` vaut 1 aux dernière nouvelles, alors `b` vaut 1 !
> Il faut vraiment comprendre cette exécution séquentielle, ligne par ligne.

> [!question]- Q2 : Si la variable `escargot` vaut 4, quel est le résultat de `escargot = escargot + 1;` ?
> **5**
> Vous comprenez le principe ?
> Avec cette méthode je peux deviner votre âge dans 5 ans ! C'est simplement votre âge aujourd'hui + 5 ans. C'est de la triche, mais ça marche ! Peut importe ce que je mets dans la boîte `escargot`, je vais juste ajouter 1 à la boîte.

> [!question]- Q3 : Quelle est la valeur de la variable `palmier` après l'exécution du code ?
```c
int palmier = 5;
int poire = 3;
palmier = poire + palmier
```
> [!question]- Q1 Réponse
> **palmier  = 8**
> Encore une fois ligne par ligne
> 1ere et 2eme ligne on déclare les deux variables avec les valeurs 5 et 3
> 3eme ligne, on prends la boîte `palmier` et on y met sa propre valeur avec poire en plus. D'ailleurs, que ce soit `palmier` ou une autre variable, le contenu de la boîte est effacé et remplacé par la valeur du membre à droite du `=`.
> On range donc dans cette boîte `palmier` la valeur `palmier + poire`, c'est à dire `5 + 3` donc au final `palmier` vaut 8.


# Niveau 2
---
`+=`, `-=`, `:=`, `++`

# Niveau 3
---
`<<`, `&`, `&&`, `+`