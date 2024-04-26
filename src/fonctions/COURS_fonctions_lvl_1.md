# Fonctions, déclaration et appel
---
*Pré-requis :* [Variables et types de données - Niveau 1](../variables_datatypes/COURS_variables_lvl_1.md)
## Définition
Les fonctions sont des éléments primordiaux de la plupart des [langages de programmation](../definitions/langages_de_programmation.md), elles structurent le code quand elles sont bien gérées, le rendent modulable et surtout compréhensible et lisible.\
*A quoi sert-elle et comment elle marche ?*\
Pour répondre à cette question on va séparer les concepts de la syntaxe.

Les fonctions sont comme de **multiples chefs d'orchestres avec chacun leur partition à suivre**. Quand un chef d'orchestre est appelé, il joue sa pièce de musique, puis quand il a fini, il s'arrête.

> Une fonction est un peu similaire, elle peut être **appelée**, et elle peut **retourner** un résultat.

**ATTENTION** la syntaxe entre les différents langages change énormément ! Assimilez bien le concept.

Quand on exécute la commande **gcc** on appelle la fonction **main**, qui retourne 0.\
Souvenez-vous que 0 en C signifie **Vrai**, ou **True**. C'est jute pour s'assurer que la fonction s'est correctement exécutée sans erreur.

Si vous avez mis en place votre environnement de code avec [GUIDE_setup](../intro/GUIDE_setup.md.md), vous avez déjà vu comment exécuter la fonction **main**.\
Puisqu'on en a déjà manipulé sans s'en rendre compte, créons-en d'autres et apprenons leur comportement !\
Pour la suite des consignes souvenez-vous aussi que l'exécution est séquentielle, ligne par ligne. Ca deviendra important.

## Déclaration d'une fonction
Souvenez-vous de la structure de la fonction **main** et servons-nous en pour construire la fonction `rouler`:
``` c
int rouler() {
	return 0;
}
```
Cette fonction marche parfaitement ! Elle ne fait rien de spécial, puisque si on l'appelle, elle renvoie 0, c'est à dire "aucun problème".

> [!IMPORTANT]
> On appelle la façon d'écrire une fonction sa **signature**.\
> On parlera dans un autre niveau des **paramètres** d'une fonction et de ce qu'elle **retourne**.

## Appel d'une fonction
Maintenant qu'on a déclaré une fonction, on va l'implémenter dans le code et l'appeler depuis la fonction **main**.

```c
#include <stdio.h>

int rouler() {
	return 0;
}

int main() {
	rouler();
    return 0;
}
```
On peut déjà relever plusieurs choses :
- La fonction **rouler** est déclarée **en dehors du corps de la fonction main**. Ca veut dire quoi ? Les fonctions sont délimitées par leurs corps, c'est à dire les accolades.
- Cette nouvelle fonction retourne 0, comme la fonction main, pour nous dire que tout s'est bien déroulé.
- On **appelle** la fonction **rouler** depuis la fonction main, avec une syntaxe très courante : `nom_de_la_fonction()`. Ces parenthèses sont souvent la clé pour deviner si on appelle une fonction, on autre chose !

> [!IMPORTANT]
> Parfois, les appels de fonctions ont une syntaxe différente, rappelez-vous bien de séparer concept et syntaxe !

## Exécution
Que va-t-il se passer lors de l'exécution ?\
Là, il va falloir s'accrocher un peu mais fait confiance. Inspire, expire, inspire, inspire, inspire ...\
J'ai déjà dit plusieurs fois que l'exécution est séquentielle, est c'est toujours vrai, mais cette fois-ci il va falloir discerner **déclaration** (ou **définition**, **initialisation**) d'une fonction et **appel** d'une fonction. Pas de panique en réalité c'est plutôt intuitif avec les bons exemples.

Replongeons dans les profondeurs du code précédent :
```c
int rouler() {
	return 0;
}
```
Ici, ma fonction est **définie**, c'est à dire que j'ai modelé sa forme, sa structure, j'ai dit "le chef d'orchestre **rouler** existe, et fera ça et ça, puis retournera 0 !"