---
titre: "[[01-Le centre de masse des systèmes matériels]]"
tags:
aliases:
crée: 01-10-2025, 10:14
---
# Formules
Masse d’un système de points matériels : $\displaystyle M = \sum_{i = 1}^{N} m_i$ ; La description de l’état complet du système (S) de N points matériels $P_i$ nécessite donc $3N$ coordonnées de position (3 pour chaque vecteur position $\overrightarrow{OP_i}$) et N masses.

> [!note] Centre de masse d’un système de points matériels
> Le centre de masse (ou centre d’inertie) G d’un système matériel $(S) = \{(P_i, m_i), i \in (1, \ldots, N)\}$ est le point géométrique G tel que : $\displaystyle \sum_{i = 1}^{N} m_i \overrightarrow{GP_i} = \overrightarrow{0}$.
> Il s’agit donc du <mark style="color: red">barycentre</mark> des points matériels, pondérés par leur masse.
> Une expression plus utilisée pour déterminer explicitement la position de G est celle qui fait intervenir un point particulier du repère d’espace, son origine O le plus souvent. Dans ce cas, on montre que : $\displaystyle \overrightarrow{OG} = \frac{1}{M} \sum_{i = 1}^{N} m_i \overrightarrow{OP_i}$.
> Cette définition est intrinsèque. Elle ne fait intervenir que les positions des points matériels de $(S)$ et leur masse, indépendamment de tout système de coordonnées. G est unique, sous réserve que la masse M du système soit non nulle, ce qui est le cas des systèmes physiques en mécanique newtonienne.

Coordonnées du centre de masse : $\overrightarrow{OG} = x_G\overrightarrow{e_x} + y_G\overrightarrow{e_y} + z_G\overrightarrow{e_z}$ avec $\displaystyle x_G = \frac{1}{M} \sum_{i = 1}^{N} m_ix_i$, $\displaystyle y_G = \frac{1}{M} \sum_{i = 1}^{N} m_iy_i$ et $\displaystyle z_G = \frac{1}{M} \sum_{i = 1}^{N} m_iz_i$. Soient $(x_i, y_i, z_i)$ les trois coordonnées cartésiennes de chaque point matériel $P_i$ du système.

> [!note] Associativité du centre de masse
> On est souvent amené, par commodité des calculs par exemple, à décomposer un système complexe $(S)$ en plusieurs sous-systèmes plus simples $(s)$. Sur la [[#^figure1]], $(S)$ est formé de la réunion de trois sous-ensembles disjoints.
> Soit un système matériel $(S)$ formé de $N'$ sous-systèmes matériels, notés $(s_1)$ à $(s_{N'})$. Utilisons l’indice entier j pour indicer ces sous-systèmes : $j = 1, \ldots, N'$.
> Soit $G_j$ le centre de masse du sous-système $(s_j)$ et $m_j = m(s_j)$ la masse de ce sous-système.
> Soit G le centre de masse du système matériel $(S)$ et M sa masse totale : $\displaystyle M = \sum_{j = 1}^{N} m_j$.
> Soit O un point de l'espace.
> Alors on a : $\displaystyle \overrightarrow{OG} = \frac{1}{M} \sum_{j = 1}^{N'} m_j \overrightarrow{OG_j}$
> Pour la détermination du centre de masse d’un système matériel $(S)$ composé, chaque sous-système $(s_j)$ est équivalent à un seul point matériel : son centre de masse $G_j$ affecté de la masse du système $m_j$.

> [!note] Centre de masse d’un système tridimensionnel
> Un système $(S)$ de volume V, de masse M, est découpé (par la pensée) en éléments matériels de volume $\delta V$ et de masse $\delta m$. Chaque élément est repéré et distingué des autres par son centre de masse P. On notera donc les volume et masse $\delta V(P)$ et $\delta m(P)$ pour les distinguer entre eux ([[#^figure2]]).
> On définit la masse volumique moyenne $\bar{\rho}(P)$ de l’élément matériel : $\bar{\rho}(P) = \frac{\delta m(P)}{\delta V(P)}$.
> Lorsque l’élément de volume $\delta V$ tend vers 0, on obtient la masse volumique locale : $\displaystyle \rho(P) = \lim_{\delta V \rightarrow 0} \frac{\delta m}{\delta V} = \dfrac{d m}{d V}$. Cette relation peut se noter de manière équivalente $d m = \rho(P) d V$.
> Le symbole de sommation discrète $\sum$, qui utilise des indices entiers, est remplacé par le symbole $\iiint_{V}$ qui décrit une sommation continue sur un ensemble de points P du volume V qui définit le système $(S)$.
> La masse totale s’exprime alors par : $M = \iiint_{V} d m$ et le centre de masse G est défini par : $\displaystyle \overrightarrow{OG} = \frac{1}{M} \iiint_{V} \overrightarrow{OP} d m = \frac{1}{M} \iiint_{V} \rho(P)\overrightarrow{OP} d V$.
> De même, les coordonnées de G s’obtiennent en projetant cette expression vectorielle sur une base cartésienne telle que les coordonnées du point P soient $(x, y, z)$ : $x_G = \frac{1}{M} \iiint_{V} \rho(P)x d V$, $y_G = \frac{1}{M} \iiint_{V} \rho(P)y d V$ et $z_G = \frac{1}{M} \iiint_{V} \rho(P)z d V$.


# Définitions
> [!warning]
> Dans un référentiel galiléen, le centre de masse d’un système isolé a un mouvement rectiligne et uniforme, alors que ce n’est généralement pas le cas d’un point quelconque du système.

==**Masse**== :
La masse est une grandeur physique qui, en physique newtonienne, a les propriétés suivantes :
- elle est strictement positive ;
- elle est additive : on peut sommer les masses de sous-systèmes disjoints (on dit que la masse est une grandeur extensive) ;
- elle est conservée au cours du temps, quand le système est fermé ;
- elle garde la même valeur dans tous les référentiels (on dit que c’est une grandeur invariante).

==**Modèle du point matériel**== :
Le point matériel est le système physique le plus simple, c’est-à-dire celui dont l’état complet est décrit avec le plus petit nombre de paramètres. Ce nombre se réduit à trois variables réelles, les trois coordonnées de position dans l’espace ($(x, y, z)$ dans une base cartésienne ou $(r, θ, z)$ dans une base cylindrique par exemple).
Il ne faut pas confondre un point matériel avec un système ponctuel. Ce dernier peut posséder d’autres paramètres d’état qui en font un système plus complexe qu’un point matériel.
Par exemple, un dipôle électrostatique ponctuel possède, en plus de sa position et de sa masse, un vecteur moment dipolaire électrique. L’état complet du dipôle nécessite de connaître l’orientation de son moment dipolaire.
# Diagrammes
![[mecanique2/attachments-mecanique2/figure1.png]]^figure1

![[mecanique2/attachments-mecanique2/figure2.png]]^figure2
# Graphiques

# Expériences

# Autres notes
