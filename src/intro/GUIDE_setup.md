# Préparer l'environnement
---
Les exercices seront en C et en Python.\
Tous les exercices proposés peuvent être fait en codant à la main sur papier, si vous aimez vous faire du mal. Sinon, je vous recommande d'installer à l'aide de ressources externes sur vos machines des outils comme **gcc** pour pouvoir compiler du C, et python, pour faire du python...\
Il existe pléthore de tutoriels, et même des [compilateurs en ligne](https://www.onlinegdb.com/online_c_compiler) !

# Goodbye world :(
---
Vous allez créer votre premier programme ! Le tout premier programme qu'on enseigne aux débutants, et c'est normal.

## Editeur de texte
Pour faire un programme, il faut l'écrire. Sur papier ça marche, mais on ne peut pas l'exécuter, c'est juste de l'encre et un bout d'arbre très plat. Du coup il nous faut un **éditeur de texte**.\
Bloc-note, ça fonctionne.\
Notepad, ça fonctionne pas mal.\
L'écrire sur un terminal, ça fonctionne aussi.\
Mais si je vous disait qu'on peut rédiger du code dans une application **spécialisée**, qui auto-corrige, suggère et signale les erreurs avant même de compiler ?\
Je vous ai vendu du rêve, peut-être que je vous ai perdu. Mais dans tout les cas, téléchargez [VSCode](https://code.visualstudio.com/).\
**VSCode** c'est comme bloc-note mais plus joli et intelligent, avec une grosse communauté derrière, et c'est l'application "par défaut", et c'est très bien comme ça.\
Rappelez-vous qu'un éditeur de texte, aussi sophistiqué soit-il, ne fait principalement qu'écrire du texte. Certains sont plus robustes, avec des fonctionnalités qui brillent, mais restez basique pour le moment.

## Programme C
Dans l'éditeur de texte de votre choix, collez ça :
```c
#include <stdio.h>

int main() {
    printf("Goodbye world :(\n");
    return 0;
}
```
On n'expliquera pas maintenant pourquoi ça marche, et comment.\
Si ? Vraiment vous insistez ? Vous n'arriverez plus à dormir avant de savoir la recette magique qui fait que ce code marche ?\
Pour vraiment tout comprendre il faudrait se pencher sur [Variables et types de données - Niveau 1](/variables_datatypes/COURS_variables_lvl_1.md), et [[COURS - Structure de contrôle]]... mais voilà un résumé utile pour la suite des exercices :
```c
int main() {
	// vos instructions vont ici, entre la première accolade et le "return"
	return 0;
}
```
Ce morceau de code est la **fonction** qui s'appelle **main** (qui veut dire "principale" en Anglais).\
Le code doit se trouver entre les deux accolades, c'est comme ça il faut l'accepter. Dans ce **bloc**, on va donc y mettre nos instructions, comme par exemple, une **fonction** (et oui encore une !) qui affiche du texte !\
Cette fonction, imbriquée dans la fonction **main**, s'appelle **printf**. Elle affiche du texte. `printf("Goodbye world :(\n");`

## Exécution
Sauvegardez le fichier sur votre machine avec un nom type "program.c" ou bien "et_ouais_classe.c", et exécutons-le :
`gcc program.c -o program`
`./program`
ou bien si vous avez choisi le deuxième nom
 `gcc et_ouais_classe.c -o et_ouais_classe`
 `./et_ouais_classe`

Normalement, vous verrez dans le terminal affiché `Goodbye world :(` !\
Dingue.

# Exercices
Pour le reste des exercices de ce cours, utilisez la fonction main :
```c
int main() {
    //blablabla
    return 0;
}
```
et remplacez le blabla par le code que vous souhaitez exécuter.\
Si vous avez des erreurs de compilations, erreur de syntaxe, erreur tout court, il faut chercher de soit même sur internet, idéalement en anglais.