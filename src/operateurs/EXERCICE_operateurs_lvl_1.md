# Exercices - Opérateurs
---

## Q1 : Quelle est la valeur de la variable `b` à la fin de l'exécution du programme ?
```c
int a = 1;
int b = 0;
b = 3;
b = a;
```
<details>
  <summary>Réponse</summary>

**b = 1**  

On va comprendre ligne par ligne  

1ere ligne, `a` = 1 et `b` n'existe pas encore !  

2eme ligne, `b` est initialisé à 0 (et `a` existe toujours)  

3eme ligne, `b` vaut 3, c'est à dire qu'on met la valeur 3 dans la boîte `b`  

4eme ligne, `b` vaut `a`, et comme `a` vaut 1 aux dernière nouvelles, alors `b` vaut 1 !  

Il faut vraiment comprendre cette exécution séquentielle, ligne par ligne.
</details>

---

## Q2 : Si la variable `escargot` vaut 4, quel est le résultat de `escargot = escargot + 1;` ?

<details>
  <summary>Réponse</summary>

**5**

Vous comprenez le principe ?  

On aurait pu ranger la valeur `escargot + 1` dans une autre boîte, mais c'est pratique de le ranger dans elle-même, ça prends moins de travail à faire.

Avec cette méthode je peux même deviner votre âge dans 5 ans ! C'est simplement votre âge aujourd'hui + 5 ans. C'est de la triche, mais ça marche ! Peut importe ce que je mets dans la boîte `escargot`, je vais juste ajouter 1 à la boîte.
</details>

---

## Q3 : Quelle est la valeur de la variable `palmier` après l'exécution du code ?
```c
int palmier = 5;
int poire = 3;
palmier = poire + palmier
```

<details>
  <summary>Réponse</summary>

**palmier = 8**  

Encore une fois ligne par ligne  

1ere et 2eme ligne on déclare les deux variables avec les valeurs 5 et 3  

3eme ligne, on prends la boîte `palmier` et on y met sa propre valeur avec poire en plus.

On range donc dans cette boîte `palmier` la valeur `palmier + poire`, c'est à dire `5 + 3` donc au final `palmier` vaut 8 !

Petit tips bonus, que ce soit `palmier` ou une autre variable, quand on met un opérateur `=`, le contenu de la boîte est effacé et remplacé par la 
valeur du membre à droite.
</details>
