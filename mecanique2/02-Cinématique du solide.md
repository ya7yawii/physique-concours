---
titre: "[[02-Cinématique du solide]]"
tags:
aliases:
crée: 02-10-2025, 16:56
---
# Formules
> [!note] Formule de Varignon
> Si M et N sont deux points qui appartiennent <mark style="color: red">au même solide</mark>, alors leurs vitesses au même instant t sont liées par la formule de Varignon : $\overrightarrow{V}(N, t) = \overrightarrow{V}(M, t) + \overrightarrow{NM} \wedge \overrightarrow{\Omega}(t)$ qui s'écrit aussi $\overrightarrow{V}(N, t) = \overrightarrow{V}(M, t) + \overrightarrow{\Omega}(t) \wedge \overrightarrow{MN}$ avec $\overrightarrow{\Omega}(t)$ est le <mark style="color: red">vecteur rotation instantané</mark>, aussi appelé vecteur vitesse angulaire instantané.
> Le champ des vitesses d’un solide est ainsi décrit par un torseur dont les éléments de réduction sont le vecteur rotation instantané et la vitesse en un point du solide. La formule de Varignon n’est en fait rien d’autre qu’une relation de transport caractéristique des torseurs. Ainsi, l’hypothèse d’indéformabilité d’un solide impose une relation entre les vitesses au même instant de deux points appartenant au solide.
> À chaque instant, le mouvement d’un solide $(S)$ est déterminé par les deux vecteurs correspondant aux éléments de réduction du torseur cinématique. Il s’agit donc de 6 scalaires. On dit que le solide est un système à 6 degrés de liberté. Ces degrés de liberté sont répartis de la façon suivante :
> - 3 degrés de liberté de translation, associés aux trois coordonnées d’un point du solide ;
> - 3 degrés de liberté d’orientation, associés aux rotations d’axes liés au solide.
>
> Le champ des accélérations d’un solide n’est généralement pas décrit par un torseur.

> [!note] Cas particuliers de mouvements d’un solide
> - Solide en translation : un solide est en translation si le vecteur rotation instantané est constamment nul. La vitesse est alors la même en tout point du solide.
> - Solide en rotation autour d’un axe fixe :  Si un point du solide est sur l’axe de rotation, sa vitesse est nulle. Notons O un tel point. Le champ des vitesses s’écrit alors sous la forme $\overrightarrow{V}(M) = \overrightarrow{\Omega} \wedge \overrightarrow{OM}$. L’axe de rotation est dirigé selon le vecteur rotation instantané $\overrightarrow{\Omega}$ qui présente une direction fixe. Tous les points du solide décrivent des cercles de même axe, l’axe de rotation. Si aucun point du solide ne se trouve sur l’axe de rotation, on peut cependant considérer un point O de l’axe et retenir l’expression précédente pour le champ des vitesses du solide.
> - Solide en rotation autour d’un axe de direction fixe : Une importance particulière est accordée aux mouvements de rotation autour d’axes de direction fixe. Lorsqu’un solide est en rotation autour d’un axe de direction fixe, son mouvement se décompose en une rotation dans son référentiel barycentrique autour d’un axe de même direction et en une translation de son centre d’inertie G. Un tel mouvement est par exemple observé dans le cas d’une roue qui roule sur un plan. La roue présente alors, a priori, deux degrés de liberté. En effet, sa position à un instant donné est décrite par :
> 	- l'abscisse x du centre d'inertie G ;
> 	- l'angle $\theta = (\overrightarrow{e_x}, \overrightarrow{GM})$ où M est un point fixe sur la roue ([[#^figure1]]).
> - Mouvement général d’un solide : Le mouvement le plus général d’un solide est la composition, à chaque instant, d’une rotation à vitesse angulaire $\Omega$ autour de l’axe instantané de rotation et d’une translation à vitesse v le long de cet axe ([[#^figure2]]). L’axe instantané de rotation peut varier au cours du temps, à la fois dans le référentiel d’étude et par rapport au solide. On parle de mouvement hélicoïdal si $\overrightarrow{\Omega}$ et $\overrightarrow{v}$ sont constants.
> - Mouvement plan : Un solide est en mouvement plan si les vitesses de tous ses points sont colinéaires à un plan fixe donné, pendant toute la durée du mouvement. On représente alors communément ce champ des vitesses dans le plan ([[#^figure3]]).

# Définitions
==**Cinématique**== :
La cinématique est l’étude du mouvement des systèmes matériels sans chercher à en expliquer les causes. Un solide présente en général six degrés de liberté. Son champ des vitesses est décrit par un « torseur cinématique ». Le mouvement relatif de deux solides en contact se décompose en glissement, roulement et pivotement. Le roulement sans glissement joue un rôle particulier dans de nombreux systèmes mécaniques.

==**Modèle du solide**== :
En mécanique, le solide est un système matériel ==**indéformable**==. La distance entre deux points quelconques du système est donc indépendante du temps.
Il s’agit d’un modèle. Soumis à des contraintes suffisamment importantes, un solide se déforme. La physique des matériaux s’intéresse à ces propriétés que nous ignorons dans tout ce cours de mécanique des solides.
Étant donné l’hypothèse d’indéformabilité, on peut définir un référentiel attaché à un solide $\Sigma$. On choisit ainsi quatre points $(O, A, B, C)$ d’un solide $\Sigma$ tels que le repère $(\overrightarrow{OA}, \overrightarrow{OB}, \overrightarrow{OC})$ soit orthonormé direct. Décrire le mouvement du solide dans un référentiel $(R)$ revient à décrire le mouvement du référentiel attaché au solide par rapport à $(R)$.

> [!note] Nature du contact entre deux solides
> Le contact entre deux solides peut se faire :
> - selon une surface (par exemple, lorsqu’un livre glisse sur une table plane) ;
> - selon une ligne (par exemple, lorsqu’un cylindre roule sur un plan) ;
> - en un point (par exemple, lorsqu’une boule est en mouvement sur une table) ([[#^figure4]]).
> 
> Les deux derniers cas sont en fait des modèles. Le contact réel se fait toujours selon une surface, de dimensions éventuellement très petites. On se ramènera cependant au cas d’un point de contact pour des systèmes dont on peut étudier la « trace » dans un plan (roue cylindrique).
> Sur les schémas précédents, on a représenté des liaisons unilatérales. Dans certains cas, le mouvement d’un solide par rapport à un autre est limité par d’autres contraintes que celles imposées par un simple contact. On définit ci-dessous les principales liaisons.
> ![[mecanique2/attachments-mecanique2/figure10.png]]

# Diagrammes
![[mecanique2/attachments-mecanique2/figure7.png]]^figure2

![[mecanique2/attachments-mecanique2/figure8.png]]^figure3

![[mecanique2/attachments-mecanique2/figure9.png]]^figure4
# Graphiques
![[mecanique2/attachments-mecanique2/figure6.png]]^figure1
# Expériences

# Autres notes
