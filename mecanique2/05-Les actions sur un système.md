---
titre: "[[05-Les actions sur un système]]"
tags:
aliases:
crée: 11-10-2025, 11:12
---
# Formules
> [!note]
> Le vecteur force apparaissant dans le principe fondamental de la dynamique est ici généralisé au cas d’un ensemble de points, discret ou continu. Ce vecteur force est remplacé par un ensemble de vecteurs appelé « actions sur le système ».
> Cet ensemble n’est pas équivalent, en général, à un seul vecteur s’appliquant sur le système en un seul point. C’est pourquoi on utilisera le terme d’«actions» ou d’«efforts» sur le système $(S)$. On déterminera plus loin sous quelles conditions les actions sont équivalentes à une force unique.

Résultante des actions : $\displaystyle \overrightarrow{F} = \sum_{i=1}^{N} \overrightarrow{f}_i$ avec $\overrightarrow{f}_i$ est la force exercée sur le point $P_i$ ; $\overrightarrow{f}_i = \overrightarrow{f}_{i\,ext} + \overrightarrow{f}_{i\,int}$.
> [!note]
> La définition de la résultante des actions sur les systèmes continus est analogue, l’intégrale remplaçant la somme et l’élément de force $d\overrightarrow{f}(P)$ que subit l’élément matériel en P remplaçant la force $\overrightarrow{f}_i$.

Résultante des forces extérieures : $\displaystyle \overrightarrow{F}_{ext} = \sum_{i=1}^{N} \overrightarrow{f}_{i\,ext}$ où $\overrightarrow{f}_{i\,ext} = \overrightarrow{f}_{(S')\rightarrow i} + \overrightarrow{f}_{i\,ie} + \overrightarrow{f}_{i\,ic}$ ; $\overrightarrow{f}_{(S')\rightarrow i}$, $\overrightarrow{f}_{i\,ie}$ et $\overrightarrow{f}_{i\,ic}$ sont définis dans la [[#^484f10|définition des actions extérieures]].

Résultante des [[#^9ef48c|forces d'interaction]] ==**sur le point $P_i$**== : $\displaystyle \overrightarrow{f}_{i \, int} = \sum_{j=1}^{N} \overrightarrow{f}_{j\rightarrow i}$.
> [!note] Propriétés des actions intérieures
> Les forces d'interaction vérifient la loi des actions réciproques ou $3^e$ loi de Newton :
> - $\overrightarrow{f}_{i \rightarrow j} = -\overrightarrow{f}_{j \rightarrow i}$ ;
> - $\overrightarrow{P_iP_j} \wedge \overrightarrow{f}_{j \rightarrow i} = \overrightarrow{0}$.
> 
> Par convention, on posera : $\overrightarrow{f}_{i \rightarrow i} = \overrightarrow{0}$ un point n'exerçant aucune force sur lui-même.
> Pour les systèmes continus, ces actions sont décrites par des éléments de force infinitésimaux : on écrit l’élément de force sur un élément infinitésimal de volume $d\tau$ repéré par le point $P$ dont l’origine est un autre volume $d\tau'$ autour d’un point $P'$ du système : $d\overrightarrow{f}_{P'\rightarrow P}$ ([[#^figure1|fig. 1]]).

> [!note]
> La résultante des forces intérieures à un système est nulle : $\overrightarrow{F}_{int} = \overrightarrow{0}$.
> Une conséquence de ce théorème est importante : la résultante des actions $\overrightarrow{F}$ s’exprime uniquement à partir des actions extérieures : $\overrightarrow{F} = \overrightarrow{F}_{ext}$.

# Définitions
==**Actions extérieures**== :
Dans un référentiel galiléen, une force est dite ==**extérieure**== à un système si elle est exercée par un système matériel $(S')$ situé à l’extérieur de $(S)$. Il s’agit dans ce cas d’une force d’interaction entre les deux systèmes : $\overrightarrow{f}_{(S')\rightarrow i}$.
Dans le cas d’un référentiel non galiléen, les forces ==**d’inertie d’entraînement $\overrightarrow{f}_{ie}$ et de Coriolis $\overrightarrow{f}_{ic}$**== sont considérées comme des forces extérieures, même s’il n’existe pas de système matériel qui en serait la cause.
Les forces exercées par les systèmes extérieurs (forces d’interaction) sont invariantes par tout changement de référentiel. Les forces d’inertie dépendent du référentiel d’étude. ^484f10

==**Actions intérieures**== :
Une force est dite intérieure au système $(S)$ si elle est exercée sur un point $P_i$ du système $(S)$ par un autre point $P_j$ de ce même système. Elle est notée $\overrightarrow{f}_{j\rightarrow i}$.
L’ensemble de ces forces $\{\overrightarrow{f}_{j\rightarrow i}\}_{i = 1,\, \ldots, N \,;\, j = 1,\, \ldots, N}$ constitue les actions intérieures. Ce sont des forces d’interaction.
Cette force peut être une force d’interaction à courte portée (Van der Waals, contact, pression) ou à longue portée (interaction gravitationnelle ou électromagnétique, dont les charges et les masses sont intérieures au système). ^9ef48c

# Diagrammes
![[mecanique2/attachments-mecanique2/figure25.png]]^figure1
# Graphiques

# Expériences

# Autres notes
