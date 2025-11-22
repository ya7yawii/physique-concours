---
titre: "[[01-Systèmes linéaires]]"
tags:
aliases:
crée: 22-11-2025, 13:47
---
# Formules
> [!note] Systèmes linéaires, continus et stationnaires
> ==**Un système est continu lorsque toutes les grandeurs, qui définissent son état, sont des fonctions continues du temps.**==
> Les systèmes continus sont définis par opposition aux ==**systèmes discrets**== (en temps ou en amplitude) qui sont séquentiels, échantillonnés, logiques, quantifiés, etc.
> Un système est linéaire lorsque la relation entre la grandeur d'entrée $e(t)$ et la grandeur de sortie $s(t)$ est une équation différentielle linéaire : $D_0s(t) + D_1\dfrac{ds(t)}{dt} + \cdots + D_n\dfrac{d^{n}s(t)}{dt^{n}} = N_0e(t) + N_1\dfrac{de(t)}{dt} + \cdots + N_m\dfrac{d^{m}e(t)}{dt^{m}}$.
> L'ordre du système linéaire est, par définition, l'ordre de son équation différentielle.
> ==**Un système linéaire est stationnaire, ou invariant dans le temps, si les coefficients $D_k$ et $N_j$ de son équation différentielle sont indépendants du temps.**==
> - Principe de superposition : Soit respectivement $s_1(t)$ et $s_2(t)$ les réponses du système aux excitations $e_1(t)$ et $e_2(t)$. Un système linéaire satisfait au principe de superposition, c'est-à-dire qu'à l'excitation : $e(t) = \lambda_1e_1(t) + \lambda_2e_2(t)$, où $\lambda_1$ et $\lambda_2$ sont des constantes, correspond la réponse : $s(t) = \lambda_1s_1(t) + \lambda_2s_2(t)$, les causes ajoutent leurs effets et les effets sont proportionnels aux causes.
> - Domaines de linéarité : Bien que les systèmes physiques ne soient jamais rigoureusement linéaires, il est cependant possible de les considérer comme tels si l'amplitude et la fréquence des signaux d'entrée sont comprises entre certaines limites qui définissent leurs ==**domaines de linéarité**==. Un exemple classique est celui du pendule simple, qui est un système linéaire quand ses oscillations sont de faible amplitude, les frottements solides étant négligés.
^par1

> [!note] Fonction de transfert d'un système linéaire : signaux sinusoïdaux
> Pour réviser cette notion, on pourra se reporter à l'ouvrage H-Prépa, Électronique-Électrocinétique, 1re année, [[06-Régime sinusoïdal forcé|chapitre 6]].

> [!note] Transformée de Laplace
> Associons à toute fonction $f(t)$ du temps, une fonction $F(p)$ de la variable complexe $p$ définie par : $\displaystyle F(p) = \int_{0_-}^{\infty}f(t)e^{-pt}dt$ sous réserve de convergence de l'intégrale. Cette dernière condition est physiquement peu contraignante.
> La fonction $F(p)$ est la transformée de Laplace de $f(t)$ et la fonction $f(t)$ est l'original de $F(p)$.
> Notons que la borne inférieure de l'intégrale de définition de la transformée de Laplace $F(p)$ est $0_-$. Par exemple, pour $f(t) = u(t)$ échelon débutant à $t = 0$, nous avons $f(0_-) = 0$ et $f(0_+) = 1$.
> - La somme des deux originaux $f_1(t) + f_2(t)$ se traduit par la somme de transformées $F_1(p) + F_2(p)$.
> - La multiplication de l'original $f(t)$ par une constante $a$ se traduit par la même opération sur la transformée $F(p)$ avec la même constante $a$.
> - La transformée de la dérivée de l'original est égale à $pF(p) - f(0_-)$. Dans l'hypothèse où $f(t)$ ainsi que ses dérivées successives $\dfrac{d^{m}f(t)}{dt^{m}}$ (pour $m = 0, \cdots, m = n - 1$) sont nulles à $t = 0_-$, il vient que la transformée de la dérivée $n^{ième}$ de l'original $\dfrac{d^{n}f(t)}{dt^{n}}$ est égale à $p^{n}F(p)$.
> - L'intégration entre $0_-$ et $t$ de l'original $f(t)$ équivaut à la division par $p$ de sa transformée $F(p)$.
> - Un original retardé de $\tau$ $(= f(t - \tau))$ se traduit par la multiplication de la transformée $F(p)$ par $e^{-p\tau}$ à la condition que $f(t) = 0$ pour $t < 0$.

> [!note] Quelques fonctions et transformées de Laplace utiles
> - L'échelon unité, est défini par $u(t) = 1$ pour $t > 0$. Sa transformée de Laplace est : $U(p) = \frac{1}{p}$.
> - Un échelon unité retardé de $\tau$ a pour transformée : $F(p) = \frac{e^{-p\tau}}{p}$.
> - Un créneau unité ([[#^figure2|fig. 2]]) de largeur $t_0$ est défini par : $e(t) = u(t) - u(t -t_0)$. Sa transformée de Laplace est égale à la différence entre les deux transformées précédentes : $E(p) = \frac{1 - e^{-pt_0}}{p}$.
> - L'impulsion unitaire de Dirac $\delta(t)$ ([[#^figure3|fig. 3]]) est égale à la limite pour $t_0 \rightarrow 0$ d'un créneau de largeur $t_0$ débutant à $t = 0$ et d'amplitude $\frac{1}{t_0}$. L'impulsion unitaire $\delta(t)$ est la dérivée de l'échelon unitaire $u(t)$. Nous en "déduisons" l'expression de sa transformée de Laplace $\Delta(p) = 1$. De point de vue dimensionnel, $\delta(t)$ a la dimension de l'inverse d'un temps.
> - La transformée $F(p)$ de $f(t) = e^{\alpha t}$ est égale à $\frac{1}{p - \alpha}$ à condition que $\mathcal{R}e(p) > \mathcal{R}e(\alpha)$.

> [!note] Fonction de transfert opérationnelle d'un signal quelconque (au 1ere année le signal est sinusoïdal)
> Considérons un système initialement au repos ($e(t)$ et $s(t)$ ainsi que leurs dérivées successives sont nulles à $t = 0_-$) dont l'équation différentielle est celui de [[#^par1|paragraphe 1]].
> La transformée de Laplace de l'équation différentielle s'écrit : $(D_0 + D_1p + \cdots + D_np^{n})S(p) = (N_0 + N_1p + \cdots + N_mp^{m})E(p)$, où $E(p)$ et $S(p)$ sont respectivement les transformées de Laplace de l'excitation $e(t)$ et de la réponse $s(t)$.
> Par définition, la fonction de transfert opérationnelle $H(p)$ du système est : $\displaystyle H(p) = \frac{S(p)}{E(p)} = \frac{N_0 + N_1p + \cdots + N_mp^{m}}{D_0 + D_1p + \cdots + D_np^{n}}$.
> Remarques :
> - La fonction de transfert est définie à l’aide d’un régime dont les conditions initiales sont nulles. Dans ce cas (fréquent) la réponse $s(t)$ du système s’obtient en cherchant l’original de $S(p)$.
> - Dans le cas d’une excitation sinusoïdale, nous retrouvons la définition de la fonction de transfert complexe en faisant $p=j\omega$.
> - Pour tenir compte de conditions initiales différentes il faut appliquer les formules de dérivation sous leurs formes complètes.

# Définitions
==**Signal**== : Une grandeur physique mesurable

==**Système**== : Un dispositif dont l'état est déterminé par un ou plusieurs signaux.

==**Opérateur**== :
Un opérateur est un système qui établit une relation entre deux signaux ; la valeur de la grandeur (ou signal) de sortie $s(t)$ est déterminée par l'évolution de la grandeur (ou signal) d'entrée $e(t)$. Un opérateur est unidirectionnel si le signal de sortie est sans influence sur le signal d'entrée.
Ces définitions se généralisent à des opérateurs plus complexes comportant plusieurs signaux d'entrée et/ou plusieurs signaux de sortie.

==**Représentations d’un opérateur**== :
Un utilisateur ne s’intéresse pas au fonctionnement interne de l’opérateur, mais seulement à ses interactions avec l’extérieur. Nous allons donc utiliser des schémas simplifiés où l’opérateur est une « boîte noire ». Nous utiliserons deux types de représentations :
- La représentation unifilaire où les opérateurs d’un système sont représentés par des boîtes reliées par des fils qui symbolisent les signaux. Pour un opérateur unidirectionnel, des flèches indiquent les grandeurs d’entrée et de sortie.
- Les systèmes électriques ou électroniques se prêtent à une représentation bifilaire qui permet de visualiser à la fois les courants et les tensions d’entrée et de sortie.
La [[#^figure1|figure 1]] donne ainsi les différentes représentations d’un potentiomètre avec suiveur. La présence de l’A.O. monté en suiveur lui confère son caractère unidirectionnel.
- Le schéma expérimental est nécessaire pour réaliser concrètement l’opérateur à partir de composants.
- Le schéma bifilaire est suffisant pour déterminer toutes les grandeurs d’entrée et de sortie.
- Le schéma unifilaire est suffisant pour symboliser la relation entre les tensions d’entrée et de sortie, mais insuffisant pour caractériser complètement le comportement de l’opérateur dans un système plus complexe ; ainsi, il ne permet pas de prévoir la valeur du courant $i_e$.
Remarque : Le schéma dit « expérimental » est également symbolique : il ne décrit pas les multiples connexions internes à l’A.O. et ne fait pas mention de son alimentation.

# Diagrammes
Potentiomètre avec suiveur. a. Schéma expérimental. b. Schéma bifilaire. c. Schéma unifilaire
![[electronique2/attachments-electronique2/figure1.png]]^figure1
# Graphiques
Créneau $e(t)$ débutant à $t = 0$ avec une durée $t_0$ et une amplitude unité
![[electronique2/attachments-electronique2/figure2.png]]^figure2

Lorsque la durée $t_0$ du créneau $e(t)$ tend vers zéro, le signal $e(t)$ tend vers l'impulsion unité
![[electronique2/attachments-electronique2/figure3.png]]^figure3
# Expériences

# Autres notes
