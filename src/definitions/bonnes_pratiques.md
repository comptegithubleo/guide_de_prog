# Bonnes pratiques
---
Vous connaissez l'[IOCCC](https://www.ioccc.org/) ? C'est le concours international d'obfuscation de code en C.\
C'est des personnes brillantes qui font des programmes tout simples, mais de la manière la plus compliquée.\
Bizarre d'en parler dans la partie "Bonne pratique", pourtant ça suit un raisonnement que j'aime bien et qui s'applique à beaucoup de choses.

>[!IMPORTANT]
>Pour devenir maître, il faut apprendre les codes.
>Pour surpasser les maîtres, il faut casser les codes.

Ce concours est la matérialisation (digitale...) de ce concept.\
Pour bien commencer, et bien progresser, il faut apprendre les codes, rendre son travail accessible, et rester dans le partage et l'entraide. C'est pour cela que les bonnes pratiques sont essentielles, elles donnent un cadre et nous rend rigoureux !

```c
#include <stdio.h>
#include <math.h>
#include <unistd.h>
#include <sys/ioctl.h>

             main() {
         short a[4];ioctl
      (0,TIOCGWINSZ,&a);int
    b,c,d=*a,e=a[1];float f,g,
  h,i=d/2+d%2+1,j=d/5-1,k=0,l=e/
 2,m=d/4,n=.01*e,o=0,p=.1;while (
printf("\x1b[H\x1B[?25l"),!usleep(
79383)){for (b=c=0;h=2*(m-c)/i,f=-
.3*(g=(l-b)/i)+.954*h,c<d;c+=(b=++
b%e)==0)printf("\x1B[%dm ",g*g>1-h
*h?c>d-j?b<d-c||d-c>e-b?40:100:b<j
||b>e-j?40:g*(g+.6)+.09+h*h<1?100:
 47:((int)(9-k+(.954*g+.3*h)/sqrt
  (1-f*f))+(int)(2+f*2))%2==0?107
    :101);k+=p,m+=o,o=m>d-2*j?
      -.04*d:o+.002*d;n=(l+=
         n)<i||l>e-i?p=-p
             ,-n:n;}}
```
Peter Eastman, IOCCC 2011.

Si vous voulez tester, copiez le code, et lancez la commande :\
`gcc eastball.c -o eastball -lm && ./eastball`


## Fonctions

```c

```