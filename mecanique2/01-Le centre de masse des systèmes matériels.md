---
titre: "[[01-Le centre de masse des systèmes matériels]]"
tags:
  - système
  - centre
  - guldin
  - symétrie
crée: 01-10-2025, 10:14
---
# Formules
Masse d'un système de points matériels : $\displaystyle M = \sum_{i = 1}^{N} m_i$ ; La description de l'état complet du système (S) de N points matériels $P_i$ nécessite donc $3N$ coordonnées de position (3 pour chaque vecteur position $\overrightarrow{OP_i}$) et N masses.

> [!note] Centre de masse d'un système de points matériels
> Le centre de masse (ou centre d'inertie) G d'un système matériel $(S) = \{(P_i, m_i), i \in (1, \ldots, N)\}$ est le point géométrique G tel que : $\displaystyle \sum_{i = 1}^{N} m_i \overrightarrow{GP_i} = \overrightarrow{0}$.
> Il s'agit donc du <mark style="color: red">barycentre</mark> des points matériels, pondérés par leur masse.
> Une expression plus utilisée pour déterminer explicitement la position de G est celle qui fait intervenir un point particulier du repère d'espace, son origine O le plus souvent. Dans ce cas, on montre que : $\displaystyle \overrightarrow{OG} = \frac{1}{M} \sum_{i = 1}^{N} m_i \overrightarrow{OP_i}$.
> Cette définition est intrinsèque. Elle ne fait intervenir que les positions des points matériels de $(S)$ et leur masse, indépendamment de tout système de coordonnées. G est unique, sous réserve que la masse M du système soit non nulle, ce qui est le cas des systèmes physiques en mécanique newtonienne.

Coordonnées du centre de masse : $\overrightarrow{OG} = x_G\overrightarrow{e_x} + y_G\overrightarrow{e_y} + z_G\overrightarrow{e_z}$ avec $\displaystyle x_G = \frac{1}{M} \sum_{i = 1}^{N} m_ix_i$, $\displaystyle y_G = \frac{1}{M} \sum_{i = 1}^{N} m_iy_i$ et $\displaystyle z_G = \frac{1}{M} \sum_{i = 1}^{N} m_iz_i$. Soient $(x_i, y_i, z_i)$ les trois coordonnées cartésiennes de chaque point matériel $P_i$ du système.

> [!note] Associativité du centre de masse
> On est souvent amené, par commodité des calculs par exemple, à décomposer un système complexe $(S)$ en plusieurs sous-systèmes plus simples $(s)$. Sur la [[#^figure1]], $(S)$ est formé de la réunion de trois sous-ensembles disjoints.
> Soit un système matériel $(S)$ formé de $N'$ sous-systèmes matériels, notés $(s_1)$ à $(s_{N'})$. Utilisons l'indice entier j pour indicer ces sous-systèmes : $j = 1, \ldots, N'$.
> Soit $G_j$ le centre de masse du sous-système $(s_j)$ et $m_j = m(s_j)$ la masse de ce sous-système.
> Soit G le centre de masse du système matériel $(S)$ et M sa masse totale : $\displaystyle M = \sum_{j = 1}^{N} m_j$.
> Soit O un point de l'espace.
> Alors on a : $\displaystyle \overrightarrow{OG} = \frac{1}{M} \sum_{j = 1}^{N'} m_j \overrightarrow{OG_j}$
> Pour la détermination du centre de masse d'un système matériel $(S)$ composé, chaque sous-système $(s_j)$ est équivalent à un seul point matériel : son centre de masse $G_j$ affecté de la masse du système $m_j$.

> [!note] Centre de masse d'un système tridimensionnel
> Un système $(S)$ de volume V, de masse M, est découpé (par la pensée) en éléments matériels de volume $\delta V$ et de masse $\delta m$. Chaque élément est repéré et distingué des autres par son centre de masse P. On notera donc les volume et masse $\delta V(P)$ et $\delta m(P)$ pour les distinguer entre eux ([[#^figure2]]).
> On définit la masse volumique moyenne $\bar{\rho}(P)$ de l'élément matériel : $\bar{\rho}(P) = \frac{\delta m(P)}{\delta V(P)}$.
> Lorsque l'élément de volume $\delta V$ tend vers 0, on obtient la masse volumique locale : $\displaystyle \rho(P) = \lim_{\delta V \rightarrow 0} \frac{\delta m}{\delta V} = \dfrac{d m}{d V}$. Cette relation peut se noter de manière équivalente $d m = \rho(P) d V$.
> Le symbole de sommation discrète $\sum$, qui utilise des indices entiers, est remplacé par le symbole $\iiint_{V}$ qui décrit une sommation continue sur un ensemble de points P du volume V qui définit le système $(S)$.
> La masse totale s'exprime alors par : $M = \iiint_{V} d m$ et le centre de masse G est défini par : $\displaystyle \overrightarrow{OG} = \frac{1}{M} \iiint_{V} \overrightarrow{OP} d m = \frac{1}{M} \iiint_{V} \rho(P)\overrightarrow{OP} d V$.
> De même, les coordonnées de G s'obtiennent en projetant cette expression vectorielle sur une base cartésienne telle que les coordonnées du point P soient $(x, y, z)$ : $x_G = \frac{1}{M} \iiint_{V} \rho(P)x d V$, $y_G = \frac{1}{M} \iiint_{V} \rho(P)y d V$ et $z_G = \frac{1}{M} \iiint_{V} \rho(P)z d V$.

> [!note] Théorèmes de Guldin
> - Premier théorème de Guldin : Soit $(\mathscr{C})$ une courbe plane, de masse linéique $\lambda$ uniforme, de longueur L, de centre de masse G ([[#^figure3]]). Soit $\Delta$ un axe ==ne coupant pas== $(\mathscr{C})$. La rotation de $(\mathscr{C})$ autour de $\Delta$ engendre une surface $(\Sigma)$ d'aire S. Alors la distance d de G à l'axe $\Delta$ est $d = \frac{S}{2\pi L}$.
> - Second théorème de Guldin : Soit $(\mathscr{S})$ une surface plane, de masse surfacique $\sigma$ uniforme, d'aire S, de centre de masse G ([[#^figure4]]). Soit $\Delta$ un axe ne coupant pas $(\mathscr{S})$. La rotation de $(\mathscr{S})$ autour de $\Delta$ engendre un volume V. Alors la distance d de G à l'axe $\Delta$ est $d = \frac{V}{2\pi S}$.
# Définitions
> [!warning]
> Dans un référentiel galiléen, le centre de masse d'un système isolé a un mouvement rectiligne et uniforme, alors que ce n'est généralement pas le cas d'un point quelconque du système.

==**Masse**== :
La masse est une grandeur physique qui, en physique newtonienne, a les propriétés suivantes :
- elle est strictement positive ;
- elle est additive : on peut sommer les masses de sous-systèmes disjoints (on dit que la masse est une grandeur extensive) ;
- elle est conservée au cours du temps, quand le système est fermé ;
- elle garde la même valeur dans tous les référentiels (on dit que c'est une grandeur invariante).

==**Modèle du point matériel**== :
Le point matériel est le système physique le plus simple, c'est-à-dire celui dont l'état complet est décrit avec le plus petit nombre de paramètres. Ce nombre se réduit à trois variables réelles, les trois coordonnées de position dans l'espace ($(x, y, z)$ dans une base cartésienne ou $(r, θ, z)$ dans une base cylindrique par exemple).
Il ne faut pas confondre un point matériel avec un système ponctuel. Ce dernier peut posséder d'autres paramètres d'état qui en font un système plus complexe qu'un point matériel.
Par exemple, un dipôle électrostatique ponctuel possède, en plus de sa position et de sa masse, un vecteur moment dipolaire électrique. L'état complet du dipôle nécessite de connaître l'orientation de son moment dipolaire.

==**Enveloppe convexe (ou minimale) d'un système de points**== :
- Dans le cas d'un système plan, l'enveloppe minimale du système est la courbe de plus petite longueur contenant tous les points ([[#^figure5]]).
- Dans le cas d'un système à trois dimensions, l'enveloppe minimale est la surface de plus petite aire contenant tous les points.
Le centre de masse G d'un système matériel $(S)$ se trouve à l'intérieur de l'enveloppe minimale de $(S)$.
On montre mathématiquement que cette enveloppe est convexe, c'est-à-dire qu'elle contient tous les points du segment reliant deux points quelconques à l'intérieur de l'enveloppe.

==**Invariance d'un système**== :
on dit que le système $(S)$ est invariant par une transformation T si pour tout point M de $(S)$ d'image $M' = T[M]$, $\rho(M') = \rho(M)$.
**Autrement dit, on ne peut pas distinguer le système après la transformation du système avant l'opération.**
La transformation T laissant le système $(S)$ invariant est aussi appelée ==**symétrie**== du système $(S)$.
Couramment, les symétries des systèmes matériels sont constituées par, outre l'élément neutre, les opérations suivantes :
- les translations ;
- les rotations ;
- les symétries planes (opération miroir) et ponctuelles (inversion).

> [!warning]
> Il ne faut pas confondre « élément de symétrie » (un point, une droite ou un plan) d'un système et les opérations « symétrie ponctuelle » ou « symétrie plane ».
> L'ensemble des symétries d'un système forme un groupe. L'opération identité, qui correspond à une symétrie pour tous les systèmes, constitue l'élément neutre du groupe de symétrie d'un système.

==**Points invariants**== :
un point P d'un système $(S)$ est dit invariant par une transformation T si $P = T[P]$.
Exemples :
- l'opération identité : tous les points sont invariants ;
- les translations : aucun point n'est invariant ;
- les rotations : l'ensemble des points invariants constitue l'axe de rotation ;
- les symétries planes (opération miroir) : l'ensemble des points invariants constitue le plan de symétrie ;
- les symétries ponctuelles (inversion) : le point invariant est le point de symétrie.
**Il s'agit de déterminer les invariances de $\rho(P)$ par ces transformations.**

> [!note] Symétries et centre de masse
> Le centre de masse G d'un système matériel $(S)$ est un point invariant des opérations de symétrie du système.
> En d'autres termes, si le système $(S)$ possède une symétrie T, son centre de masse est invariant par cette transformation : $T[G] = G$.
> Le centre de masse est un des points du système invariant par l'ensemble des éléments de symétrie du système. Si on peut montrer que les symétries ne préservent qu'un seul point, le centre de masse est alors entièrement déterminé, et l'on évite ainsi de longs calculs.
# Diagrammes
![[mecanique2/attachments-mecanique2/figure1.png]]^figure1

![[mecanique2/attachments-mecanique2/figure2.png]]^figure2

![[mecanique2/attachments-mecanique2/figure3.png]]^figure3

![[mecanique2/attachments-mecanique2/figure4.png]]^figure4

![[mecanique2/attachments-mecanique2/figure5.png]]^figure5
# Graphiques

# Expériences

# Autres notes
> [!warning] Tester ses connaissances page 13
> - Une symétrie plane est la composée d'une rotation d'angle $\pi$ et d'une symétrie ponctuelle.
> - Une symétrie ponctuelle est la composée d'une rotation d'angle $\pi$ et d'une symétrie plane.
> - Une symétrie axiale est une rotation d'angle $\pi$.

> [!warning] Savoir appliquer le cours page 14
> - Des symétries d'une boule homogène sont par exemple les suivants :
> 	- les rotations (d'angle quelconque) autour de tous les axes passant par son centre ;
> 	- les symétries planes par rapport aux plans passant par son centre.
> Le seul point invariant par toutes ces symétries est le centre de la boule, qui constitue donc son centre de masse.
> - Le cube admet comme symétries :
> 	- les rotations d'angle $\frac{\pi}{4}$ et $\frac{\pi}{2}$ autour des axes passant par son centre et le centre des faces ; les rotations d'angle $\frac{3\pi}{2}$ autour des grandes diagonales du cube ;
> 	- les symétries planes par rapport aux plans passant par deux arêtes opposées ou par les centres de quatre arêtes parallèles.
> Le seul point invariant est le centre du cube.
> - Le cylindre est invariant par toute rotation autour de l'axe de révolution ainsi que par la symétrie plane par rapport au plan qui le coupe en deux parties égales. On en déduit que le centre de masse est l'intersection de l'axe de révolution et de ce plan.

> [!warning] Méthodes pour la détermination de la position du centre de masse
> 1. Méthode utilisant les théorèmes de Guldin : voir la correction des questions 3 et 4 du section savoir appliquer le cours pages 20 et 21.
> 2. Méthode de la masse négative : voir la correction de la question 5 du section savoir appliquer le cours page 21.
> 3. Méthode intégrale : voir la correction de la question 6 de section savoir appliquer le cours pages 21 et 22. Consulter aussi l'exercice de la section savoir résoudre les exercices page 15.
> Lorsque les symétries ne suffisent pas à déterminer entièrement la position du centre de masse, il faut utiliser la méthode intégrale.

> [!warning] Qu'est-ce qu'une équation de l'hypoténuse dans la question savoir résoudre les exercices?
> En fait, il s'agit de l'équation de la droite $y = -\frac{b}{a}x + b$ qui passe par l'hypoténuse. Alors pour retrouver la borne maximale de l'intégrale en x qui est en fonction de y, il suffit juste de remplacer x par $x_max$ dans l'équation de la droite.