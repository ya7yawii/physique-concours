---
titre: "[[07-Champ magnétique]]"
tags:
aliases:
crée: 06-01-2026, 13:08
---
# Formules
> [!note] Force de Lorentz et champ magnétique
> - Force de Lorentz :
> Nous savons qu’un aimant ou une bobine de spires conductrices parcourues par un courant électrique sont sources de champs magnétiques $\overrightarrow{B}$. Ces champs se manifestent par la force de Lorentz que subit une particule mobile de charge $q$ et de vitesse $\overrightarrow{v}$ : $\overrightarrow{F} = q\overrightarrow{v} \wedge \overrightarrow{B}$, ou par la force de Laplace que subit un élément $d\overrightarrow{l}$ de circuit parcouru par un courant d’intensité $I$ : $d\overrightarrow{F} = Id\overrightarrow{l} \wedge \overrightarrow{B}$.
> Nous n’étudierons dans ce cours que le champ magnétique créé par des courants.
> *Remarque : Rappelons qu’il existe un champ magnétique terrestre (cf. chapitre 9) dont la composante horizontale, en France, est de l’ordre de $2\,.10^{-5}$ tesla.*
> - [[#^app1|Cadre d’étude]] :
> Les lois à venir sont rigoureusement valables dans le cas de la magnétostatique, c’est-à-dire pour des régimes indépendants du temps (courants constants, pas d’accumulation de charges). Nous emploierons souvent l’expression « champ magnétique » au sens de « champ magnétostatique » par la suite.
> Ces lois sont encore applicables à des dispositifs expérimentaux de dimension caractéristique $L$, dans le cas des régimes variables de temps caractéristique $T$, tant que $L \ll cT$ où $c$ est la vitesse de la lumière dans le vide.
> - Mesure du champ :
> *La force de Laplace*, subie par un élément $d\overrightarrow{l}$ de circuit parcouru par un courant d’intensité $i$ : $d\overrightarrow{F} = Id\overrightarrow{l} \wedge \overrightarrow{B}$, est mesurable.
> Le champ magnétique $\overrightarrow{B}$ appliqué à un circuit parcouru par un courant $i$ peut donc être mesuré à partir de la mesure de la force $\overrightarrow{F}$ subie par celui-ci ([[#^figure1|fig. 1]]).
> En fait une sonde à effet Hall, moins encombrante et plus précise, sera généralement préférée pour la mesure des champs magnétiques.

> [!note] Loi de Biot et Savart : Vecteur élément de courant
> - Considérons un circuit filiforme parcouru par un courant d’intensité $I$ et notons $d\overrightarrow{l}$ un déplacement élémentaire le long de ce circuit, dans le sens que du courant ([[#^figure2|fig. 2]]).
> Par définition, on appelle *élément de courant* le vecteur polaire : $d\overrightarrow{C} = Id\overrightarrow{l}$.
> La norme d’un élément de courant s’évalue en A.m.
> - Lorsque la section du circuit n’est plus petite à l’échelle macroscopique, il est pertinent, sinon indispensable, de s’interroger sur la répartition du courant dans le circuit. Pour cela nous serons obligés d’introduire une modélisation continue. Nous analyserons alors le circuit comme un ensemble de tubes de courants mésoscopiques, filiformes, jointifs, d’intensité $dI$, placés à l’intérieur de la surface externe du circuit ([[#^figure3a|fig. 3a]]). À un élément de longueur $d\overrightarrow{l}$ d’un tube de courant mésoscopique, sera associé le vecteur de courant : $d\overrightarrow{C} = dI\,d\overrightarrow{l}$. Notons $s$ la section de ce tube de courant et $\overrightarrow{j}$ le vecteur densité volumique de courant à travers la section considérée, il vient : $d\overrightarrow{C} = dI\,d\overrightarrow{l} = jsd\overrightarrow{l} = \overrightarrow{j}d\tau$ puisque $\overrightarrow{j}$ et $d\overrightarrow{l}$ sont colinéaires et de même sens.
> *Une distribution volumique de courants peut s’analyser en une distribution continue de courants filiformes mésoscopiques.*
> Cette équivalence est fréquemment utilisée. En effet, dans la pratique, nombre de circuits filiformes se présentent sous la forme de bobinages multicouches avec des spires jointives de faible section. La structure d’une telle bobine, avec ses spires filiformes, rappelle en tous points celle du courant précédent lorsqu’il est analysé en tubes de courant mésoscopiques. Pour calculer les champs créés par de tels circuits, il sera alors très commode d’avoir recours à une modélisation volumique, continue, nivelant le caractère discret du bobinage.
> - Une démarche analogue peut être adoptée pour une distribution de courants surfaciques. Tout courant surfacique peut être analysé comme une distribution continue de rubans mésoscopiques, filiformes, jointifs, d’intensité $dI$ ([[#^figure3b|fig. 3b]]). À un élément de longueur $d\overrightarrow{l}$ d’un ruban de courant mésoscopique, sera associé le vecteur de courant : $d\overrightarrow{C} = dI\,d\overrightarrow{l}$. Notons $a$ la section d’un ruban de courant et $j_s$ le vecteur densité surfacique de courant à travers la section considérée, il vient : $d\overrightarrow{C} = dI\,d\overrightarrow{l} = j_s\,a\,d\overrightarrow{l} = \overrightarrow{j_s}dS$ puisque $\overrightarrow{j_s}$ et $d\overrightarrow{l}$ sont colinéaires et de même sens.
> Cette équivalence pourra être utilement exploitée quand il s’agira, par exemple, de calculer le champ créé par une bobine monocouche à spires jointives de faible section.
> *Une distribution surfacique de courant peut s’analyser en une distribution continue de courants filiformes mésoscopiques.*
> - En conclusion, nous retiendrons que :
> ==**Toute distribution de courants peut s’analyser comme une distribution de courants filiformes dont la caractéristique locale est l’élément de courant $d\overrightarrow{C}$.**==
> 
> Par la suite, cette analyse ne sera pas toujours explicitement faite sur les distributions de courants étudiés, mais il ne tient qu’au lecteur de s’en convaincre en l’effectuant.

> [!note] Loi de Biot et Savart : Champ attribué à un élément de courant
> Alors que les charges sont les sources du champ électrostatique, les éléments de courant sont les sources du champ magnétique.
> ==**Nous *postulons* que l’expression de la contribution d’un élément de courant $d\overrightarrow{C}$, situé au point $P$, au champ total $\overrightarrow{B}(M)$ créé en $M$ par une distribution de courants est donnée par la loi de Biot et Savart : $\displaystyle d\overrightarrow{B}(M) = \frac{\mu_0}{4\pi} d\overrightarrow{C}\wedge\frac{\overrightarrow{e}_{P\rightarrow M}}{\left\Vert PM \right\Vert^{2}} = \frac{\mu_0}{4\pi}d\overrightarrow{C}\wedge\frac{\overrightarrow{PM}}{\left\Vert PM \right\Vert^{3}}$.**==
> ==**Le champ $\overrightarrow{B}(M)$ étant la somme des contributions élémentaires, avec $d\overrightarrow{C} = \overrightarrow{j}d\tau$ ou $d\overrightarrow{C} = \overrightarrow{j}_SdS$ ou $d\overrightarrow{C} = I\,d\overrightarrow{l}$ selon les cas.**==
> Comme il est impossible d’isoler un élément de courant, nous ne pouvons pas vérifier directement ce postulat : la seule grandeur ayant une signification physique (en tant que grandeur mesurable) est le champ résultant $\overrightarrow{B}$ créé par toute la distribution de courants $\mathcal{D}$.
> ==**Le coefficient $\mu_0$, dimensionné, vaut exactement $\mu_0 = 4\pi\, . 10^{-7}\, H\, . m^{-1}$ ($H$ désigne le henry, unité d’inductance).**==
> ==**L’unité de champ magnétique est le tesla (symbole : $T$).**==
> - Nous pouvons aussi attribuer un élément de courant à chaque particule chargée en mouvement. Imaginons que sur une longueur $\delta l$ d’un fil conducteur, il y ait $N$ particules mobiles de charge $q$ et de vitesse $v$. Ces $N$ particules traversent une section du fil pendant la durée $\delta t = \frac{\delta l}{v}$, d’où la valeur de l’intensité : $I = \frac{Nqv}{\delta l}$ et donc pour l’élément de fil : $\delta \overrightarrow{C} = N q \overrightarrow{v}$.
> Nous pouvons associer à chaque particule en mouvement un élément de courant : $\overrightarrow{C} = q \overrightarrow{v}$.

# Définitions

# Diagrammes
Force de Laplace s’exerçant sur le rail $A_1A_2$
![[electromagnetisme1/attachments-electromagnetisme1/figure99.png]]^figure1

Élément de courant d’un courant filiforme : $d\overrightarrow{C} = Id\overrightarrow{l}$
![[electromagnetisme1/attachments-electromagnetisme1/figure100.png]]^figure2

Tube de courant mésoscopique considéré comme circuit filiforme : $d\overrightarrow{C} = \overrightarrow{j}d\tau$
![[electromagnetisme1/attachments-electromagnetisme1/figure101.png]]^figure3a

Ruban de courant mésoscopique considéré comme circuit filiforme : $d\overrightarrow{C} = \overrightarrow{j_s}dS$
![[electromagnetisme1/attachments-electromagnetisme1/figure102.png]]^figure3b
# Graphiques

# Expériences

# Autres notes
> [!warning] Application 1 page 117
> ![[electromagnetisme1/attachments-electromagnetisme1/figure98.png]]
^app1