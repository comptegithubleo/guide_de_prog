# Fonctions, déclaration et appel
---
*Pré-requis :* [Variables et types de données - Niveau 1](../variables_datatypes/COURS_variables_lvl_1.md)
## Définition
Les fonctions sont des éléments primordiaux de la plupart des [langages de programmation](../definitions/langages_de_programmation.md), elles structurent le code quand elles sont bien gérées, le rendent modulable et surtout compréhensible et lisible.\
*A quoi sert-elle et comment elle marche ?*\
Pour répondre à cette question on va séparer les concepts de la syntaxe.

Les fonctions sont comme de **multiples chefs d'orchestres avec chacun leur partition à suivre**. Quand un chef d'orchestre est appelé, il joue sa pièce de musique, puis quand il a fini, il s'arrête.

> Une fonction est un peu similaire, elle peut être **appelée**, et elle peut **retourner** un résultat.

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
Plusieurs éléments sont à relever.\  
Premièrement, la fonction `rouler` n'est pas **dans** la fonction **main**.

> [!TIP]
> Optional information to help a user be more successful.