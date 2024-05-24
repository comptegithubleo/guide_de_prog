# Niveau 3 - Boucles itératives
---
*Pré-requis :*
- [Structures de controle - Niveau 1](COURS_structures_controle_lvl_1.md)
- [Opérateurs - Niveau 3](../operateurs/COURS_operateurs_lvl_3.md)

# Sommaire
<!-- toc -->

---
## Boucles for / while
Les structures "for" et "while" sont des boucles qui vont **itérer**. Elles sont particulièrement utiles pour les tâches répétitives.\
Pour comprendre leurs différences et leur fonctionnement, on va prendre deux exemples.
### Boucle for
La boucle "for" (qui signifie en français "pour"), demande à l'ordinateur :
**Ordinateur, pour un nombre définit de répétition, fait ça.**\
Imaginons que nous voulons faire pousser des fleurs, plus précisément des [soucis](https://fr.wikipedia.org/wiki/Calendula), dans votre jardin. Votre poche a 12 graines de soucis, et vous voulez les planter en ligne, pour faire joli.\
A quoi ressemblerait la logique de la **recette** pour planter toutes ces plantes ?

En langage naturel, on peut dire qu'on se place au début de la ligne, on sort une graine de sa poche, on fait un trou dans la terre, on plante la graine, on recouvre de terre, et on arrose, puis **on vérifie qu'on peut toujours avancer d'un pas** et on recommence.\
Du 1er pas au 12eme pas, on fait des actions à chaque pas, c'est exactement le fonctionnement d'une boucle **for** !

Les syntaxes changent beaucoup selon les langages, mais souvenez vous des principes :
- Au début on fixe une valeur de départ, et une condition de fin. Dans notre cas on commence au pas 1 et on finis au 12eme pas. A chaque itération, l'ordinateur vérifiera si la variable `pas` sera plus petite que 12. Si c'est le cas, c'est qu'on est à la fin du jardin donc la boucle s'arrête.
- Enfin on choisit l'incrément ou décrément de la variable, à chaque fois que la boucle se termine, l'ordinateur va modifier la variable `pas`. Dans notre cas, on avance d'un pas à chaque fois alors on l'incrémente de 1.

En C, la syntaxe est la suivante :
```c
for (initialisation variable ; test condition ; mise a jour variable) {
	//code
}
```
Et ci-dessous notre exemple concret : 
```c
for (int i = 1; i < 12; i++) {
	planter_soucis();
}
```
Ici, la variable `i` représente les pas, par convention on appelle cette variable `i` dans les boucles.\
Le code dit que `i` commence à 1, et qu'à chaque itération, on vérifie que `i < 12`. Si c'est le cas, alors on fait l'opération `i++` et on exécute le code à l'intérieur du corps de la boucle. Sinon, on sort de la boucle.

### Boucle while
La boucle "while" (qui signifie en français "tant que"), demande à l'ordinateur :
**Ordinateur, tant que la condition n'est pas remplie, fait ça.**\
C'est différent de la boucle **for**, car là on ne définit pas explicitement de nombre de répétition, simplement le fait qu'on s'arrête quand la condition est remplie.\
Imaginons qu'on veuille faire pousser un citronnier, et qu'on veuille l'arroser tant qu'il n'a pas atteint 1 mètre 30.\
A quoi ressemblerait la logique de la **recette** pour le faire pousser ?

En langage naturel, on regarde la taille du citronnier, s'il n'est pas à 1 mètre 30, alors on l'arrose s'il en a besoin. Si en revanche il fait 1 mètre 30 ou plus, on ne l'arrose plus ! Tant pis pour lui.

En C, la syntaxe est la suivante :
```c
while (test condition) {
	//code
}
```
Et voila ci-dessous note exemple concret :
```c
while (taille_citronnier_cm < 130) {
	arroser_citronnier();
}
```
Ici on n'a pas de variable incrémentée contrairement à la boucle **for**. A chaque itération, l'ordinateur teste la condition et si elle est vraie, exécute le code. Sinon, on sort de la boucle.

## [Exercices !](EXERCICE_structures_controle_lvl_2.md)

