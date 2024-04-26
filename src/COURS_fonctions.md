# Niveau 1
---
*Pré-requis :* [[pro/mentorat/guide_de_prog/src/variables_niveau_1]]
## Définition
Les fonctions sont des éléments primordiaux de la plupart des [[Langage de programmation]], elles structurent le code quand elles sont bien gérées, le rendent modulable et surtout compréhensible et lisible.
Si vous avez mis en place votre environnement de code avec [[GUIDE_setup]], vous avez déjà vu comment exécuter la fonction **main**.

A quoi sert-elle et comment elle marche ?
Pour répondre à cette question on va séparer les concepts de la syntaxe.
Les fonctions sont comme de **multiples chefs d'orchestres avec chacun leur partition à suivre.**
Une fonction peut être **appelée**, et une fonction peut **retourner** un résultat.
Quand on exécute la commande **gcc** on appelle la fonction **main**, qui retourne 0.
Souvenez-vous que 0 en C signifie **Vrai**, ou **True**. C'est jute pour s'assurer que la fonction s'est correctement exécutée sans erreur.

Puisqu'on en a déjà manipulé sans s'en rendre compte, créons-en d'autres et apprenons leur comportement !
Pour la suite des consignes souvenez-vous aussi que l'exécution est séquentielle, ligne par ligne. Ca deviendra important.

## Appel de fonctions
Construisons **en dehors du corps de la fonction main** :
``` c
int fonction_une() {
}

int main() {
    fonction_une();
    return 0;
}
```
Plusieurs éléments sont à relever. Premièrement, la fonction `fonction_une` n'est pas **dans** la fonction **main**.