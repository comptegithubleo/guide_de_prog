# Niveau 2 - Paramètres et types de retours
---
*Pré-requis :* 
- [Fonctions - Niveau 1](COURS_fonctions_lvl_1.md)
- [Structures de contrôle - Niveau 1](../structures_controle/COURS_structures_controle_lvl_1.md)

# Sommaire
<!-- toc -->

---
Vous vous souvenez que les fonctions sont comme des **recettes de cuisine** ? Il est l'heure de vous passer à la casserole. Vous allez voir que l'analogie de la cuisine va être vraiment utile.

# A table
---
Imaginons que nous voulons cuisiner un **poulet cajun**. On dresse notre plan d'attaque !
- **Un objectif à atteindre :**
	- Faire un POULET CAJUN 🍽️
- **Des ingrédients à préparer :**
	- Poulet 100g
	- Sauce cajun 10cl
- **Un ordre d'instructions à suivre (simplifiées) :**
	- Cuire le poulet
	- Ajouter la sauce cajun
- **Un résultat à déguster**

Jusque là c'est simple et efficace... mais OH NON ! Sauce cajun ? On en a plus.\
Puisqu'on a les ingrédients, on peut les prendre un par un, les mélanger, et le résultat c'est une sauce cajun !\
Oui mais pourquoi le faire à la main si j'ai une fonction qui traîne au fond du placard, qui s'appelle : `faireSauceCajun` ?\
On a qu'à mettre les ingrédients en tant que **paramètres** dans ma fonction, la regarder mixer toute seule, et nous **retourner** le résultat, qui est une sauce cajun !

Si seulement ça existait dans la vraie vie...
```c
int faireSauceCajun()
```