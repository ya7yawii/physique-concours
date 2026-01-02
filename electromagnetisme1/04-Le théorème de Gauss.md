---
titre: "[[04-Le théorème de Gauss]]"
tags:
aliases:
crée: 01-01-2026, 10:20
---
# Formules
 Flux du champ électrostatique : $\displaystyle \Phi = \int_{(S)}\overrightarrow{E}(M).d\overrightarrow{S}(M)$.
 
 > [!note] Flux créé par une charge ponctuelle
 > La charge ponctuelle $q$ placée en $O$ ([[#^figure2|fig. 2]]), crée en $M$ le champ $\overrightarrow{E} = \frac{q}{4\pi\epsilon_0}\frac{\overrightarrow{e}_r}{r^{2}}$ dont le flux à travers $d\overrightarrow{S}(M)$ est : $d\Phi = \frac{q}{4\pi\epsilon_0}\frac{\overrightarrow{e}_r.d\overrightarrow{S}(M)}{r^{2}}$.
 > Pour interpréter le produit scalaire $\overrightarrow{e}_r.d\overrightarrow{S}$, considérons la surface d’aire $d\Sigma$, projeté de $dS$ sur un plan orthogonal à $\overrightarrow{e}_r.d\Sigma$ représente également l’aire découpée sur une sphère de centre $O$ et de rayon $r = OM$ par un cône de sommet $O$ et qui s’appuie sur le contour définissant $dS$. L’aire $d\Sigma$ est une aire algébrique, positive quand du point $O$ on voit la face négative de $dS$, négative dans le cas contraire.
 > Donc nous pouvons écrire : $\overrightarrow{e}_r.d\overrightarrow{S} = dS\cos\alpha = d\Sigma$ soit : $d\Phi = \frac{qd\Sigma}{4\pi\epsilon_0r^{2}}$.
 > Considérons maintenant une sphère de rayon $R_0$, centrée en $O$. Le cône de sommet $O$ qui s’appuie sur le contour de $dS$ découpe sur cette sphère une pastille d’aire $d\Sigma_0$ telle que $\frac{d\Sigma_0}{R_{0}^{2}} = \frac{d\Sigma}{r^{2}}$.
 > En effet, si nous multiplions par $\lambda$ (coefficient positif quelconque) le rayon d’une sphère, toutes les dimensions mesurées sur celle-ci sont multipliées par $\lambda$ et les aires par $\lambda^{2}$ : **l’aire découpée par un cône de centre $O$ sur une sphère de centre $O$ est proportionnelle au carré de son rayon.**
 > Finalement : $d\Phi = \frac{qd\Sigma_0}{4\pi\epsilon_0R_{0}^{2}}$.

> [!note] Flux à travers une surface fermée contenant la charge
> Soit $(S)$ une surface fermée entourant la charge $q$ placée en $O$ et $(S)$ la sphère de centre $O$ et de rayon $R$ ([[#^figure3|fig. 3]]). Le flux élémentaire du champ créé par la charge $q$ à travers $d\overrightarrow{S}(M)$ est : $d\Phi = \frac{q}{4\pi\epsilon_0}\frac{\overrightarrow{e}_r.d\overrightarrow{S}(M)}{r^{2}} = \frac{q}{4\pi\epsilon_0}\frac{d\Sigma}{R^{2}}$ où $d\Sigma$ est l’élément de surface découpé, sur la sphère $(\Sigma)$ de centre $O$ et de rayon $R$, par le cône de sommet $O$ s’appuyant sur le contour de $dS$.
> Par intégration sur $(S)$, il vient : $\displaystyle \Phi = \frac{q}{4\pi\epsilon_0}\int_{(S)}\frac{\overrightarrow{e}_r.d\overrightarrow{S}(M)}{r^{2}} = \frac{q}{4\pi\epsilon_0R^{2}}\int_{(\Sigma)}d\Sigma = \frac{q}{4\pi\epsilon_0R^{2}}4\pi R^{2} = \frac{q}{\epsilon_0}$.
> 
> ==**Le flux (sortant) du champ créé par une charge $q$, à travers une surface fermée $(S)$ contenant cette charge, est : $\displaystyle \Phi = \frac{q}{4\pi\epsilon_0}\int_{(S)}\frac{\overrightarrow{e}_r.d\overrightarrow{S}(M)}{r^{2}} = \frac{q}{\epsilon_0}$.**==

> [!note] Flux à travers une surface fermée ne contenant pas la charge
> Soit $q$ une charge placée en $O$, à l’extérieur de la surface fermée $(S)$. Un cône élémentaire de sommet $O$ découpe sur $(S)$ un nombre *pair* d’éléments de surface telles que $dS_1$, $dS_2$, etc. La moitié de ces surfaces présentent au point $O$ leurs faces négatives et l’autre moitié leurs faces positives ([[#^figure4|fig. 4]]).
> Associons ces éléments de surface deux à deux tels, par exemple, $dS_1$ et $dS_2$ et notons respectivement $d\phi_1$ et $d\phi_2$ les flux à travers ces surfaces. Ces flux élémentaires sont de signes opposés et, en outre, avec les notations de [[#^figure4|figure 4]], nous pouvons écrire ($r_1 = OM_1$ et $r_2 = OM_2$) : $d\Phi_1 = \frac{q}{4\pi\epsilon_0}\frac{\overrightarrow{e}_r.d\overrightarrow{S}_1}{r_{1}^{2}} = \frac{q}{4\pi\epsilon_0}\frac{d\Sigma}{R^{2}}$ et $d\Phi_2 = \frac{q}{4\pi\epsilon_0}\frac{\overrightarrow{e}_r.d\overrightarrow{S}_2}{r_{2}^{2}} = -\frac{q}{4\pi\epsilon_0}\frac{d\Sigma}{R^{2}}$ donc : $d\phi_1 + d\phi_2 = 0$. Par intégration sur $(S)$, il vient :
> 
> ==**Le flux du champ créé par une charge $q$, à travers une surface fermée $(S)$ ne contenant pas cette charge, est nul : $\displaystyle \Phi = \frac{q}{4\pi\epsilon_0}\int_{(S)}\frac{\overrightarrow{e}_r.d\overrightarrow{S}(M)}{r^{2}} = 0$.**==

Flux du champ de gravitation à travers une surface fermée contenant la masse $m$ : $\displaystyle \Phi = -Gm\int_{(S)}\frac{\overrightarrow{e}_r.d\overrightarrow{S}(M)}{r^{2}} = -4\pi Gm$.
Flux du champ de gravitation à travers une surface fermée ne contenant pas la masse $m$ : $\displaystyle \Phi = -Gm\int_{(S)}\frac{\overrightarrow{e}_r.d\overrightarrow{S}(M)}{r^{2}} = 0$.

> [!note] Théorème de Gauss
> Pour une distribution de charges $\mathcal{D}$, les résultats précédents permettent, par utilisation du principe de superposition, de calculer le flux sortant du champ créé à travers une surface fermée $S$. Pour une charge élémentaire $dq$ de $\mathcal{D}$, la contribution au flux total est $\frac{dq}{\epsilon_0}$ si $dq$ est à l’intérieur de $S$, et nulle si $dq$ est à l’extérieur de $S$ ([[#^figure5|fig. 5]]).
> 
> ==**Le flux sortant du champ d’une distribution $\mathcal{D}$ à travers une surface fermée $S$ est égal à la charge de $\mathcal{D}$ située à l’intérieur de $S$ divisée par $\epsilon_0$ : $\displaystyle \Phi = \oiint_{S}\overrightarrow{E}.d\overrightarrow{S} = \frac{Q_{int}}{\epsilon_0}$, avec $d\overrightarrow{S} = \overrightarrow{n}_{ext}.dS$.**==
> 
> Pour le champ gravitationnel, le théorème de Gauss s’énonce de façon analogue :
> 
> ==**Le flux sortant du champ d’une distribution $\mathcal{D}$ de masses à travers une surface fermée $S$ est égal à la masse $M_{int}$ située à l’intérieur de $S$ multipliée par $-4\pi G$ : $\displaystyle \Phi_g = \oiint_{S}\overrightarrow{e}_g.d\overrightarrow{S} = -4\pi GM_{int}$.**==
> 
> Remarque : Le caractère remarquable de ce résultat est dû seulement au fait que la dépendance du champ à la distance $r$ d’observation est une loi en $\frac{\overrightarrow{e}_r}{r^{2}}$.

> [!note] Conséquences du théorème de Gauss
> - Propriétés générales d’un champ électrostatique :
> Ayant postulé la loi de Coulomb et la linéarité, nous avons montré que le champ électrostatique était :
> 	- un champ de circulation nulle sur un contour fermé, c’est-à-dire un champ de gradient ;
> 	- un champ lié à ses sources (les charges) par le théorème de Gauss.
> 	
> 	Il est possible de montrer que, réciproquement, ces deux propriétés permettent de retrouver la loi de Coulomb.
> 	==**Le théorème de Gauss et le caractère conservatif de la circulation permettent une étude complète du champ électrostatique.**==
> 	L’[[#^app1|application 1 page 65]] illustre l’étude du comportement local du champ à l’aide de ces outils.
> - Conservation du flux du champ :
> ==**En l’absence de charges, le flux du champ électrostatique est conservatif : le flux est le même à travers toutes les sections d’un même tube de champ.**==
> - [[#^demo1|Extrema du potentiel électrostatique]] :
> ==**Le potentiel électrostatique ne possède pas d’extremum en dehors des charges.**==

> [!note] Calcul d'un champ électrostatique à l'aide du théorème de Gauss : Distribution à symétrie plane
> À titre d’exemple, nous nous intéressons à la détermination du champ créé par une couche plane infinie, d'épaisseur $e$ et de charge volumique $\rho$ uniforme ([[#^figure6|fig. 6]]).
> - Première étape : utilisation des symétries de la distribution :
> Celle-ci est invariante par symétrie par rapport aux plans $\Pi_1$ et $\Pi_2$ contenant le point $M$ où nous cherchons à déterminer le champ, donc ([[#^figure6|fig. 6]]) : $\overrightarrow{E}(x, y, z) = E(x, y, z)\overrightarrow{e}_z$.
> L’invariance du problème par translation parallèlement à $(Ox)$, ou bien $(Oy)$, nous permet la simplification supplémentaire $\overrightarrow{E}(x, y, z) = E(z)\overrightarrow{e}_z$.
> Notons aussi que le plan $(xOy)$ est un plan de symétrie de la distribution. Au point $M'$, symétrique du point $M$ par rapport à ce plan, le champ $\overrightarrow{E'}$ est symétrique du champ $\overrightarrow{E}$ en $M$ : la fonction $E(z)$ est impaire : $E(-z) = -E(z)$.
> - Deuxième étape : choix de la « surface de Gauss » :
> Une surface fermée $(S)$ permettant un calcul aisé du flux doit posséder des parties planes à $z = cte$, le caractère impair de $E(z)$ nous conduisant naturellement au choix de [[#^figure6|figure 6]]. Le flux du champ à travers cette surface fermée est : $\Phi = SE(z) - SE(-z) = 2SE(z)$.
> - Troisième étape : application du théorème de Gauss :
> Appliquons le théorème de Gauss à cette surface :
> 	- cas 1 : $0 \leqslant |z| \leqslant \frac{e}{2}$ : $2SE(z) = \frac{2\rho Sz}{\epsilon_0}$ ;
> 	- cas 2 : $|z| \geqslant \frac{e}{2}$ : $2SE(z) = \frac{\rho Se}{\epsilon_0}$.
> 	
> 	Nous en déduisons :
> 	- si $0 \leqslant |z| \leqslant \frac{e}{2}$ : $\overrightarrow{E} = \frac{\rho z}{\epsilon_0}\overrightarrow{e}_z$ ;
> 	- si $|z| \geqslant \frac{e}{2}$ : $\overrightarrow{E} = \frac{\rho e}{2\epsilon_0}\,\text{signe}(z)\,\overrightarrow{e}_z$, c'est-à-dire $E(z > \frac{e}{2}) = \frac{\rho e}{2\epsilon_0}$ et $E(z < -\frac{e}{2}) = -\frac{\rho e}{2\epsilon_0}$.
> 	
> Nous pouvons en déduire le potentiel créé, en faisant par exemple le choix $V = 0$ sur le plan $z = 0$. $E_x$ et $E_y$ étant nuls, le potentiel ne dépend que de la variable $z$, avec $\dfrac{dV}{dz} = -E_z$. Raccordant le potentiel par continuité aux extrémités des intervalles caractéristiques, nous avons :
> - si $0 \leqslant |z| \leqslant \frac{e}{2}$ : $V = -\frac{\rho z^{2}}{2\epsilon_0}$ ;
> - si $|z| \geqslant \frac{e}{2}$ : $V = -\frac{\rho e(4|z| - e)}{8\epsilon_0}$.
> 
> Et la fonction potentiel $V(z)$ est paire ([[#^figure7|fig. 7]]).

> [!note] Calcul d'un champ électrostatique à l'aide du théorème de Gauss : Distribution à symétrie cylindrique
> L’exemple de distribution à symétrie cylindrique que nous allons traiter correspond à un cylindre d’axe noté $(Oz)$ et de rayon $R$ à l’intérieur duquel se trouve une charge volumique uniformément répartie $\rho$.
> - Première étape : utilisation des symétries de la distribution :
> En un point $M$ de l’espace passent deux plans de symétrie de la distribution : $\Pi_1$ qui contient le point $M$ et l’axe $(Oz)$, et $\Pi_2$ perpendiculaire à $(Oz)$ qui contient le point $M$ ([[#^figure8|fig. 8]]). Nous en déduisons, en coordonnées cylindriques d’axe $(Oz)$ : $\overrightarrow{E} = E(r, \theta, z) \overrightarrow{e}_r$.
> Les invariances du problème par translation parallèlement à $(Oz)$ et par rotation autour de cet axe amènent les simplifications supplémentaires $\overrightarrow{E} = E(r) \overrightarrow{e}_r$.
> - Deuxième étape : choix de la surface de Gauss :
> Une surface $(S)$ cylindrique d’axe $(Oz)$ et de rayon $r$, fermée par deux disques séparés par une hauteur arbitraire $h$ ([[#^figure8|fig. 8]]), constitue une surface de Gauss adaptée à la géométrie du problème. Le flux du champ à travers cette surface fermée s’écrit simplement $\Phi = 2\pi rhE(r)$, puisque ce flux est nul à travers les deux disques.
> - Troisième étape : application du théorème de Gauss :
> La charge intérieure à cette surface est : $Q_{int} = \rho\pi r^{2}h$, si $r < R$ et $Q_{int} = \rho\pi R^{2}h$, si $r > R$.
> Nous en déduisons :
> 	- $r < R$ : $\overrightarrow{E} = \frac{\rho r}{2\epsilon_0}\overrightarrow{e}_r$ ;
> 	- $r > R$ : $\overrightarrow{E} = \frac{\rho R^{2}}{2\epsilon_0r}\overrightarrow{e}_r$.
> 	
> 	Les inégalités pouvant être étendues au sens large puisque le champ créé par cette distribution volumique est continu.
> 	*Remarque : Le calcul du champ à l’aide du théorème de Gauss est remarquablement simple. Pour un cylindre chargé de hauteur finie, le théorème de Gauss serait bien entendu applicable, mais malheureusement inutilisable (les plans parallèles à $(xOy)$ ne sont plus des plans de symétrie de la distribution de charges).*
> 
> Utilisant $\displaystyle \overrightarrow{E} = -\overrightarrow{grad}V = -\left(\dfrac{\partial V}{\partial r}\right)\overrightarrow{e}_r - \frac{1}{r}\left(\dfrac{\partial V}{\partial \theta}\right)\overrightarrow{e}_{\theta} - \left(\dfrac{\partial V}{\partial z}\right)\overrightarrow{e}_z$, nous obtenons $V(r, \theta, z) = V(r)$, et en raccordant la solution par continuité en $r = R$ :
> - $r < R$ : $V = \frac{\rho(R^{2} - r^{2})}{2\epsilon_0} + V_0$ ;
> - $r > R$ : $V = -\left(\frac{\rho R^{2}}{2\epsilon_0}\right)\ln\left(\frac{R}{r}\right) + V_0$.
> 
> $V_0$ étant une constante arbitraire (indétermination du potentiel) ; notons qu’il est impossible de fixer $V = 0$ à l’infini car il y a des charges à l’infini.
> $E(r)$ et $V(r)$ sont représentés sur la [[#^figure9|figure 9]]. Une représentation de $V(r)$ dans l’espace est donnée sur la [[#^figure10|figure 10]].
^par1
# Définitions
> [!note] Vecteur surface
> Considérons une surface élémentaire « plane » $dS$ contenant le point $M$. Elle possède deux faces (l’une d’entre elle sera nommé *face négative* et l’autre *face positive*) et une *orientation* bien définie dans l’espace.
> Pour décrire complètement une telle surface, nous devons distinguer ses deux faces et indiquer son orientation. Pour ce faire, nous associerons à tout élément de surface $dS$ un *vecteur unitaire* $\overrightarrow{n}(M)$ dont la direction est normale à la surface $dS$ et dont le sens est celui qui amène de la face négative à la face positive ([[#^figure1a|fig. 1a]]).
> Une description plus complète, nous conduit à introduire un *vecteur surface élémentaire* $d\overrightarrow{S}(M) = \overrightarrow{n}(M)dS$, dont la norme est égale à l’aire de chacune des faces de $dS$.
> Lorsque la surface n’est plus élémentaire, les orientations des éléments de surface $d\overrightarrow{S}(M)$ sont définies par continuité à partir de l’orientation de l’un d’entre eux $d\overrightarrow{S}(M_0)$ ([[#^figure1b|fig. 1b]]).
> ==**Dans le cas d’une surface fermée ([[#^figure1c|fig. 1c]]), les vecteurs unitaires $\overrightarrow{n}(M)$ sont toujours dirigés vers l’extérieur (normale sortante).**==

> [!note] Calcul d'un champ électrostatique à l'aide du théorème de Gauss : Principe du calcul
> Le résultat du théorème de Gauss est remarquablement simple dans sa formulation. Pour une distribution de charges connue, on peut penser calculer le flux du champ à travers une surface fermée, puis en déduire l’expression du champ. Cette méthode est séduisante puisqu’elle permet de s’affranchir du calcul du champ (ou du potentiel) à l’aide d’expressions intégrales généralement assez contraignantes. Elle n’est toutefois envisageable que lorsque le lien entre le calcul du flux et le champ reste élémentaire : champ électrostatique d’expression déjà bien simplifiée, surface de géométrie simple..., c’est-à-dire lorsque la distribution de charges possède de bonnes symétries.
> *Le calcul d’un champ électrostatique à l’aide du théorème de Gauss n’est en général envisageable que dans des cas de distributions de charges à symétries élevées tels que ceux développés ici.*
> Dans ces conditions, le principe de calcul correspond à la démarche suivante :
> ==**Le théorème de Gauss constitue un outil de calcul rapide du champ électrostatique créé par une distribution de charges possédant une symétrie élevée : après détermination de la forme du champ, à l’aide de considérations de symétrie, l’application du théorème de Gauss à une surface fermée, *de géométrie adaptée aux symétries du problème*, permet de déterminer l’amplitude du champ.**==
> - Première étape : considérations de symétries :
> Il faut obtenir, à l’aide des symétries de la distribution, la forme du champ électrostatique :
> 	- utilisation de plans de symétrie ou antisymétrie pour déterminer sa direction ;
> 	- utilisation d’invariance par rotation ou translation pour réduire la dépendance de ses composantes vis-à-vis des coordonnées (un choix de coordonnées adapté à la symétrie du problème est évidemment indispensable).
> - Deuxième étape : choix de la surface de Gauss :
> La forme obtenue pour le champ détermine le choix d’une surface de Gauss rendant élémentaire le calcul du flux. Cette surface, dite de Gauss, doit être fermée et elle doit passer par le point $M$ où on veut calculer le champ.
> - Troisième étape : application du théorème de Gauss :
> L’application du théorème de Gauss achève la détermination du champ électrostatique.
# Diagrammes
Définition du vecteur surface élémentaire $d\overrightarrow{S}(M)$
![[electromagnetisme1/attachments-electromagnetisme1/figure38.png]]^figure1a

![[electromagnetisme1/attachments-electromagnetisme1/figure39.png]]^figure1b

Pour une surface fermée, la normale est dirigée vers l’extérieur
![[electromagnetisme1/attachments-electromagnetisme1/figure40.png]]^figure1c

$d\Sigma$ est le projeté de l’aire élémentaire $dS$ sur un plan orthogonal à $\overrightarrow{e}_r$ et passant par $M$
![[electromagnetisme1/attachments-electromagnetisme1/figure41.png]]^figure2

La charge $q$ est à l’intérieur de la surface $(S)$ fermée
![[electromagnetisme1/attachments-electromagnetisme1/figure42.png]]^figure3

La charge $q$ est à l’extérieur de la surface $(S)$ fermée
![[electromagnetisme1/attachments-electromagnetisme1/figure43.png]]^figure4

Le flux de $\overrightarrow{E}$ (créé par $Q_{int} + Q_{ext}$) à travers $(S)$ ne dépend que de $Q_{int}$
![[electromagnetisme1/attachments-electromagnetisme1/figure44.png]]^figure5

Utilisation des symétries et choix de la « surface de Gauss ». $M'$ est le symétrique de $M$ par rapport au plan $(xOy)$
![[electromagnetisme1/attachments-electromagnetisme1/figure46.png]]^figure6

Surface de Gauss pour une distribution à symétrie cylindrique
![[electromagnetisme1/attachments-electromagnetisme1/figure48.png]]^figure8
# Graphiques
Champ $E$ et potentiel $V$ créés par une couche plane infinie d’épaisseur $e$ et de charge volumique $\rho$ uniforme
![[electromagnetisme1/attachments-electromagnetisme1/figure47.png]]^figure7

Champ et potentiel d’un cylindre infini ($V = 0$ pour $r = R$)
![[electromagnetisme1/attachments-electromagnetisme1/figure49.png]]^figure9

Potentiel créé par un cylindre uniformément chargé en volume. L’équipotentielle $V = 0$ est choisie sur la surface du cylindre
![[electromagnetisme1/attachments-electromagnetisme1/figure50.png]]^figure10
# Expériences

# Autres notes
> [!warning] Application 1 page 65
> ![[electromagnetisme1/attachments-electromagnetisme1/figure45.png]]
^app1

> [!warning] Existe-t-il des extrema de potentiel dans une zone sans charge ?
> Imaginons une région vide de charges, où le potentiel électrostatique posséderait un extremum en un point $M$. Supposons qu’il s’agisse, par exemple, d’un maximum (au moins local). Les lignes de champ passant par le point $M$ doivent toutes diverger à partir de celui-ci, car elles sont orientées dans le sens des potentiels décroissants. Le flux du champ électrostatique à travers une petite surface fermée contenant le point est ainsi positif, ce qui contredit l’hypothèse d’absence de charges dans la région du point $M$. Ce raisonnement par l’absurde s’applique, de même, à un cas de potentiel minimal en $M$ et prouve que le potentiel électrostatique ne possède pas d’extremum en dehors des charges.
^demo1

> [!warning] Application 5 page 70
> L'étude précédente est celle de [[#^par1|paragraphe ci-dessus]].
> ![[electromagnetisme1/attachments-electromagnetisme1/figure51.png]]
> Remarques :
> - Le champ n’est évidemment pas défini sur le fil, car cette distribution linéique correspond à une distribution volumique locale tendant vers l’infini.
> - Comme précédemment, le théorème de Gauss est valable pour le champ électrostatique créé par un segment uniformément chargé, mais totalement inapplicable pour le calcul de ce champ !