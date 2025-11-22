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

> [!note] Fonction de transfert d'un système linéaire : signaux sinusoïdaux
> Pour réviser cette notion, on pourra se reporter à l'ouvrage H-Prépa, Électronique-Électrocinétique, 1re année, [[06-Régime sinusoïdal forcé|chapitre 6]].


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

# Expériences

# Autres notes
