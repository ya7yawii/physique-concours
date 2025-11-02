---
titre: "[[11-Actions de contact]]"
tags:
  - force-de-réaction
  - force-de-frottement
  - lois-de-Coulomb-du-frottement
  - contact-ponctuel
  - contact-quasi-ponctuel
crée: 01-11-2025, 16:08
---
# Formules
> [!note] Contact ponctuel
> Soient deux solides $S_1$ et $S_2$ en contact ponctuel, en un point $I$ commun de leurs surfaces respectives $(\Sigma_1)$ et $(\Sigma_2)$ ([[#^figure1|fig. 1]]).
> Le solide $S_1$ exerce sur le solide $S_2$ des actions de contact localisées au point de contact $I$.
> $\overrightarrow{R}_{1\rightarrow 2}$ est la résultante des actions de $S_1$ sur $S_2$. Elle s'applique en $I$.
> Conséquence : le moment des actions de contact $\overrightarrow{M}_{I\,1\rightarrow 2}$ en $I$ est nul : $\overrightarrow{M}_{I\,1\rightarrow 2} = 0$. Selon le principe des actions réciproques (ou de l'action et de la réaction), la résultante des actions du solide $S_2$ sur le solide $S_1$ est l'opposée de $\overrightarrow{R}_{1\rightarrow 2}$ ($\overrightarrow{R}_{2\rightarrow 1} = -\overrightarrow{R}_{1\rightarrow 2}$).
> Soit $(\pi)$ le plan tangent aux deux solides en $I$ et $\overrightarrow{n}_{1\rightarrow 2}$ le vecteur unitaire normal au plan $(\pi)$, dirigé du solide $S_1$ vers le solide $S_2$ ([[#^figure2|fig. 2]]).
> On décompose la résultante des actions de contact $\overrightarrow{R}_{1\rightarrow 2}$ ([[#^figure3|fig. 3]]) : $\overrightarrow{R}_{1\rightarrow 2} = \overrightarrow{N}_{1\rightarrow 2} + \overrightarrow{T}_{1\rightarrow 2}$ où :
> - $\overrightarrow{N}_{1\rightarrow 2} = (\overrightarrow{R}_{1\rightarrow 2} . \overrightarrow{n}_{1\rightarrow 2})\overrightarrow{n}_{1\rightarrow 2}$ est la composante <mark style="color: red">normale</mark> de $\overrightarrow{R}_{1\rightarrow 2}$ ou <mark style="color: red">force de réaction</mark> de $S_1$ sur $S_2$ ;
> - $\overrightarrow{T}_{1\rightarrow 2} = \overrightarrow{R}_{1\rightarrow 2} - \overrightarrow{N}_{1\rightarrow 2}$ est la composante <mark style="color: red">tangentielle</mark> de $\overrightarrow{R}_{1\rightarrow 2}$ ou <mark style="color: red">force de frottement</mark> de $S_1$ sur $S_2$.
> 
> Propriétés : La réaction est dirigée vers le solide sur lequel elle s'exerce : $\overrightarrow{R}_{1\rightarrow 2} . \overrightarrow{n}_{1\rightarrow 2} = \overrightarrow{N}_{1\rightarrow 2} . \overrightarrow{n}_{1\rightarrow 2} \geqslant 0$. Il s'agit de la condition de contact non adhésif entre les deux solides. Le contact se rompt si $\overrightarrow{N}_{1\rightarrow 2}$ s'annule.

> [!note] Contact quasi-ponctuel
> Le contact ponctuel est un modèle qui décrit des solides idéaux (boules, plans, cylindres parfaits). Dans la pratique, les solides en contact ont en commun une surface.
> Les actions de contact se répartissent cette fois sur une surface $(\Sigma)$ d'aire non nulle mais d'extension faible devant les surfaces des solides. En chaque point $P$ de $(\Sigma)$, le solide $S_1$ exerce sur $S_2$ une force infinitésimale $d\overrightarrow{r}_{1\rightarrow 2}(P)$ ([[#^figure4|fig. 4]]).
> Soit $I$ un point de $(\Sigma)$.
> La résultante des actions $d\overrightarrow{r}_{1\rightarrow 2}(P)$ et le moment $\overrightarrow{M}_{I\,1\rightarrow 2}$ de ces actions en $I$ sont donnés par : $\displaystyle \overrightarrow{R}_{1\rightarrow 2} = \iint_{(\Sigma)} d\overrightarrow{r}_{1\rightarrow 2}$ et $\displaystyle \overrightarrow{M}_{I\,1\rightarrow 2} = \iint_{(\Sigma)} \overrightarrow{IP} \wedge d\overrightarrow{r}_{1\rightarrow 2}$.
> Le contact entre solides est en général accompagné d'un moment $\overrightarrow{M}_{I\,1\rightarrow 2}$ non nul. On ne traitera pas ici ses propriétés, qui ne sont pas au programme, et on utilisera uniquement le modèle du contact ponctuel, où $\overrightarrow{M}_{I\,1\rightarrow 2} = 0$.

> [!note] Lois de Coulomb du frottement
> On décrit ici ces lois, relatives à la résultante des actions de contact, $\overrightarrow{R}_{1\rightarrow 2} = \overrightarrow{N}_{1\rightarrow 2} + \overrightarrow{T}_{1\rightarrow 2}$.
> Le comportement de $\overrightarrow{R}_{1\rightarrow 2}$ impose de distinguer deux cas, selon que les solides glissent ou ne glissent pas l'un sur l'autre. Cette condition est décrite par la vitesse de glissement $\overrightarrow{u}_{S_2/S_1} = \overrightarrow{v}(I_2 \in S_2) - \overrightarrow{v}(I_1 \in S_1)$, définie au [[02-Cinématique du solide|chapitre 2]]. Les points $I$, $I_1$ et $I_2$ sont confondus.
> - La vitesse de glissement est non nulle : $\overrightarrow{u}_{S_2/S_1} \neq \overrightarrow{0}$. Dans ce cas, les lois de Coulomb du glissement stipulent : $\left \Vert \overrightarrow{T}_{1\rightarrow 2} \right\Vert = f_c \left \Vert \overrightarrow{N}_{1\rightarrow 2} \right\Vert$ et $\overrightarrow{T}_{1\rightarrow 2}$ est opposé à $\overrightarrow{u}_{S_2/S_1}$ ([[#^figure5|fig. 5]]). $f_c$ le <mark style="color: red">coefficient de frottement cinétique</mark> (ou dynamique) est un nombre sans dimension et dépend de la nature et de l'état des surfaces en contact. Dans la plupart des cas, le coefficient $f_c$ est de l'ordre de 0,3 à 0,7.
> - La vitesse de glissement est nulle : $\overrightarrow{u}_{S_2/S_1} = \overrightarrow{0}$, les deux solides roulent sans glisser l'un sur l'autre. On dit qu'il y a adhérence entre les solides. Dans ce cas, la loi de Coulomb du <mark style="color: red">non-glissement</mark> stipule : $\left\Vert \overrightarrow{T}_{1\rightarrow 2} \right\Vert \leqslant f_s \left \Vert \overrightarrow{N}_{1\rightarrow 2} \right\Vert$. $f_s$ le <mark style="color: red">coefficient de frottement statique</mark> est un nombre sans dimension et dépend fortement de la nature et de l'état des surfaces en contact. Cette inéquation est la condition du non-glissement. <mark style="color: red">On a toujours $f_c \leqslant f_s$</mark>. Une approximation courante consiste à prendre $f_c = f_s$. On ne distingue alors pas les deux coefficients statique et cinétique. Par la suite, on notera $f$ leur valeur commune.
> 
> On se place dans l'approximation $f_c = f_s = f$.
> Une représentation géométrique particulièrement intéressante est celle définissant le cône de révolution autour de la normale $\overrightarrow{n}_{1\rightarrow 2}$ et dont le demi angle au sommet $\alpha$ est donné par : $\tan\alpha = f$. Les lois de Coulomb ont alors une interprétation géométrique :
> - s'il y a glissement, le vecteur $\overrightarrow{R}_{1\rightarrow 2}$ est sur une génératrice du cône ([[#^figure6|fig. 6a]]) ;
> - s'il n'y a pas de glissement, le vecteur $\overrightarrow{R}_{1\rightarrow 2}$ est à l'intérieur du cône ([[#^figure7|fig. 6b]]).

> [!note] Puissance des actions de contact
> La puissance des actions de contact s'exprime par : $P = \overrightarrow{T}_{1\rightarrow 2} . \overrightarrow{u}_{S_2/S_1}$. Dans le modèle du contact ponctuel, seule la force de frottement $\overrightarrow{T}_{1\rightarrow 2}$ a une puissance non nulle. Lorsqu'elle est non nulle, la puissance des forces de frottement est dissipative : $P = \overrightarrow{T}_{1\rightarrow 2} . \overrightarrow{u}_{S_2/S_1} \leqslant 0$. La puissance des actions de contact est indépendante du référentiel.
> Cas où la puissance est nulle : Il existe deux cas particuliers <mark style="color: red">importants</mark> où la puissance des actions de contact est nulle :
> - la vitesse de glissement est nulle, les solides roulent l'un sur l'autre sans glisser : $\overrightarrow{u}_{S_2/S_1} = \overrightarrow{0}\,:\,\text{roulement sans glissement}$.
> - la force de frottement est nulle : $\overrightarrow{T}_{1\rightarrow 2} = \overrightarrow{0}\,:\,\text{mouvement sans frottement}$.
> 
> Dans chacun des deux cas, le système des deux solides peut être qualifié de <mark style="color: red">conservatif</mark> (s'il n'y a pas d'autres forces non conservatives bien entendu).
> Les deux cas précédents sont en général antagonistes. Un mouvement de roulement sans glissement n'est possible que s'il existe des forces de frottement (il est difficile de rouler sur la glace sans patiner).
# Définitions
==**Force de réaction**== :
La force de réaction est due à la répulsion des atomes des deux solides. Elle est dirigée vers l'intérieur du solide sur lequel elle s'applique. Dans les cas de surfaces adhésives, cette réaction peut être attractive mais elle devient répulsive si l'on comprime un solide sur l'autre. Il n'y a pas d'expression théorique de la réaction dans le cas de solides. La réaction intervient dans les équations de la dynamique pour empêcher l'interpénétration des deux solides en contact.

==**Force de frottement**== :
La force de frottement est due aux interactions entre les couches atomiques en contact. Elle est très dépendante de la nature (composition des matériaux) et de l'état (lisse, rugueux) des surfaces en contact. La force de frottement est le résultat d'interactions nombreuses et difficiles à exprimer en général. Ses éventuelles expressions sont empiriques. La force de frottement est nulle si les surfaces sont parfaitement lisses.
# Diagrammes
![[mecanique2/attachments-mecanique2/figure39.png]]^figure1

![[mecanique2/attachments-mecanique2/figure40.png]]^figure2

![[mecanique2/attachments-mecanique2/figure41.png]]^figure3

![[mecanique2/attachments-mecanique2/figure42.png]]^figure4

![[mecanique2/attachments-mecanique2/figure43.png]]^figure5

![[mecanique2/attachments-mecanique2/figure44.png]]^figure6

![[mecanique2/attachments-mecanique2/figure45.png]]^figure7
# Graphiques

# Expériences

# Autres notes
