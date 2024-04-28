# Variables - Base
---
## Concept
Une variable en programmation exprime une boîte dans laquelle on range quelque chose.\
Par exemple, `a = 1` affecte la valeur 1 à la variable **a**, on range 1 dans la boîte nommée **a**.\
En [pseudo-code](/definitions/pseudo-code.md), on peut tout à fait écrire `a = 0.3` ou `a = Bonjour`, c'est à dire que la boîte peut prendre n'importe quelle valeur.

On peut utiliser plusieurs termes pour décrire ça, on dit qu'on **affecte** une valeur à une boîte, qu'on **déclare** une variable, ou bien qu'on **l'initialise**.

## Type de la variable
Certains [langages de programmation](/definitions/langages_de_programmation.md) ont une syntaxe et des **exigences** différentes.\
Comme parfois en maths, certains langages vont vous demander de ne pas additionner des pommes avec des bananes.\
Pour ces langages **moins permissifs**, ou parfois [bas niveau](/definitions/bas_niveau.md), plutôt de spécifier le types des variables que l'on manipule.

> [!WARNING]
> **ATTENTION**, certains langages incluent certains types et d'autres non ! Cela dépend de leur flexibilité et s'ils sont orientés pour être accessibles ([haut niveau](/definitions/haut_niveau.md)) ou pas ([bas niveau](/definitions/bas_niveau.md)).

*Mais qu'est ce qu'un type ?*\
"Bonjour" est un mot, "C'est le meilleur cours de programmation !" est une phrase, et 1 est un nombre. Un type en langage français, c'est ça.

*Mais qu'en est-il des ordinateurs ?*\
Bien que les mots, les phrases, soit importants pour nous les humains, les ordinateurs ont besoin de types encore plus simples pour calculer et se souvenir de choses.

Pour la plupart des langages, on reconnait des types basiques comme :
- L'**entier naturel**
	- *int* : signifie en anglais **integer**, traduit en français par : **entier**.
		- 1, 2, -45, 69, -8080, ...
- Le nombre **réel**
	- *float* : signifie en français **flottant**, c'est à dire un nombre réel à virgule. Utilisé quand on ne veut pas perdre de précision dans les calculs.
		- 0.875, -2.4, 0.01, ...
- Le **booléen**
	- *bool* : signifie **boule**. Non c'est pas vrai. Presque. Ca veut dire soit vrai soit faux, c'est la logique de George Boole.
		- vrai, faux / 1, 0
		- La c'est un peu étrange, mais certains langages traitent l'entier 1 comme vrai, et le 0 comme faux.
- Le **caractère** ou **chaîne de caractère** (parfois présent, absent en C par exemple)
	- *char* : signifie **caractère** pour représenter une lettre par exemple.
		- 'a', 'b', 'c', ...
		- "bonjour", "comment ça va ?", "ça va", "au revoir", ...

## Nom de la variable
Cette magnifique [convention de nommage des variables](https://en.wikipedia.org/wiki/Naming_convention_(programming)) est importante. En résumé :
- Les noms de variables doivent être lisibles et clairs
- Ne doit pas contenir d'espace
- Contenir des lettres, des tirets, et idéalement c'est tout
Si vous voulez lancer un débat ou même une altercation avec vos camarades de classe, pourquoi pas s'approprier un de ces style d'écriture et le revendiquer comme étant le meilleur ? Choisissez-en un avec pour example le nom de variable "taux de conversion"
- Le **Pascal case** : `TauxDeConversion`
- Le **Camel case** : `tauxDeConversion`
- Le **Snake case** : `taux_de_conversion`
- Le **Kebab case** : `taux-de-conversion`
- Le **Reduced case** : `tdc` (ne faites jamais ça je viens de l'inventer)

## Code
En C comme dans la grande majorité des langages, pour **déclarer** une variable et ainsi l'initialiser, la syntaxe est la suivante :
`type_de_la_variable nom_de_variable = valeur_de_la_variable`
C'est tout moche, mais quand on remplace les termes, en jouant avec les définitions des types vus précédemment, on peut écrire du code valide :
```c
int a = 1;
float baobab = 0.123;
char p_majuscule = 'p';
int *s = (int*) malloc(100 * sizeof(int));
```
Et là vous vous dites wow, j'ai tout compris ! Si c'est le cas c'est que vous avez pas lu, ou que vous êtes déjà trop fort, parce que la dernière ligne fait peur... mais elle respecte la structure !\
Effectivement la théorie semble simple, les entiers, les nombres réels, certes. Mais certains langages cachent encore des concepts plus avancés que nous verrons dans les prochains niveaux !
## Exercices