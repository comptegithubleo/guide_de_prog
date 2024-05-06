# Fonctions, déclaration et appel
---
*Pré-requis :* [Variables et types de données - Niveau 1](../datatypes/COURS_variables_lvl_1.md)
## Définition
Les fonctions sont des éléments primordiaux de la plupart des [langages de programmation](../definitions/langages_de_programmation.md), elles structurent le code quand elles sont bien gérées, le rendent modulable et surtout compréhensible et lisible.

*A quoi sert-elle et comment elle marche ?*\
Pour répondre à cette question on va séparer les concepts de la syntaxe.\
Les fonctions sont comme de **multiples chefs d'orchestres avec chacun leur partition à suivre**. Quand un chef d'orchestre est appelé, il joue sa pièce de musique, puis quand il a fini, il s'arrête.\
Une autre jolie image c'est que les fonctions sont comme des **recettes de cuisine**, on commence une recette, on fait les étapes, puis on a un résultat comestible, on espère.\
Dans tout les cas, essayez de créer votre propre analogie ou compréhension une fois que vous aurez appris son comportement.

> Une fonction peut être **appelée**, et elle peut **retourner** un résultat.

Si vous avez mis en place votre environnement de code avec [Préparer l'environnement](/intro/GUIDE_setup.md), vous avez déjà vu comment exécuter la fonction **main**.

Quand on exécute la commande `gcc` on **appelle** la fonction `main` qui **retourne** 0.\
Souvenez-vous que 0 en C signifie **Vrai**, ou **True**. C'est jute pour s'assurer que la fonction s'est correctement exécutée sans erreur.\
Puisqu'on en a déjà manipulé sans s'en rendre compte, créons-en d'autres et apprenons leur comportement !\
Pour la suite des consignes souvenez-vous aussi que l'exécution est séquentielle, ligne par ligne. Ca deviendra important.

## Déclaration d'une fonction
Souvenez-vous de la structure de la fonction **main** et servons-nous en pour construire la fonction `arroser_les_plantes`:
``` c
int arroser_les_plantes() {
	return 0;
}
```
Cette fonction marche parfaitement ! Elle ne fait rien de spécial, puisque si on l'appelle, elle renvoie 0, c'est à dire "aucun problème".

On appelle la façon d'écrire une fonction sa **signature**.\
Notre fonction à :
- Un **type de retour**, ici, *int*
- Un **nom**, ici *arroser_les_plantes*
- Des **paramètres**, ici les parenthèses vides, c'est à dire aucun paramètre

On parlera dans un autre niveau des **paramètres** d'une fonction et de son **type de retour**.

## Appel d'une fonction
Maintenant qu'on a déclaré une fonction, on va l'implémenter dans le code et l'appeler depuis la fonction **main**.

```c
int arroser_les_plantes() {
	return 0;
}

int main() {
	arroser_les_plantes();
    return 0;
}
```
On peut déjà relever plusieurs choses :
- La fonction **arroser_les_plantes** est déclarée **en dehors du corps de la fonction main**. Ca veut dire quoi ? Etant donné que les fonctions sont délimitées par leurs corps, c'est à dire les accolades, la fonction **arroser_les_plantes** est placée en dehors de celles-ci.
- Cette nouvelle fonction retourne 0, comme la fonction main, pour nous dire que tout s'est bien déroulé.
- On **appelle** la fonction **arroser_les_plantes** depuis la fonction main, avec une syntaxe très courante : `nom_de_la_fonction()`. Ces parenthèses sont souvent la clé pour deviner si on appelle une fonction ! On verra plus tard que ces parenthèses sont synonymes de **paramètres** d'une fonction.

> [!IMPORTANT]
> Parfois, les appels de fonctions ont une syntaxe différente, rappelez-vous bien de séparer concept et syntaxe !

## Exécution
Que va-t-il se passer lors de l'exécution ?\
Là, il va falloir s'accrocher un peu mais faites moi confiance. Inspire, expire, inspire, inspire, inspire ...\
J'ai déjà dit plusieurs fois que l'exécution est séquentielle, est c'est toujours vrai, mais cette fois-ci il va falloir discerner **déclaration** (ou **définition**, **initialisation**) d'une fonction et **appel** d'une fonction. Pas de panique en réalité c'est plutôt intuitif avec les bons exemples.

Replongeons dans les profondeurs du code précédent :
```c
int arroser_les_plantes() {
	return 0;
}
```
Ici, ma fonction est **définie**, c'est à dire que j'ai modelé sa forme, sa structure.\
Pour imager, ces lignes signifient "je créée la recette **arroser_les_plantes**, elle existe, et fera ça et ça, puis retournera 0" mais à **aucun moment** on ne l'appelle !\
Certes, arroser les plantes est un nom de recette étrange, mais c'est comme faire à manger pour les plantes :)\
Si on omet la ligne `arroser_les_plantes()` dans la fonction main, elle ne sera jamais appelée, mais elle existera.

## Résumé
La fonction est d'abord définie, puis elle peut être appelée ou non ! Définie, c'est juste qu'elle existe.\
**On ne pourra en revanche jamais appeler une fonction non définie !**

## [Exercices !](EXERCICE_fonctions_lvl_1.md)