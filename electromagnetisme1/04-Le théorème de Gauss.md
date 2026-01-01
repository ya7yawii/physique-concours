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
# Définitions
> [!note] Vecteur surface
> Considérons une surface élémentaire « plane » $dS$ contenant le point $M$. Elle possède deux faces (l’une d’entre elle sera nommé *face négative* et l’autre *face positive*) et une *orientation* bien définie dans l’espace.
> Pour décrire complètement une telle surface, nous devons distinguer ses deux faces et indiquer son orientation. Pour ce faire, nous associerons à tout élément de surface $dS$ un *vecteur unitaire* $\overrightarrow{n}(M)$ dont la direction est normale à la surface $dS$ et dont le sens est celui qui amène de la face négative à la face positive ([[#^figure1a|fig. 1a]]).
> Une description plus complète, nous conduit à introduire un *vecteur surface élémentaire* $d\overrightarrow{S}(M) = \overrightarrow{n}(M)dS$, dont la norme est égale à l’aire de chacune des faces de $dS$.
> Lorsque la surface n’est plus élémentaire, les orientations des éléments de surface $d\overrightarrow{S}(M)$ sont définies par continuité à partir de l’orientation de l’un d’entre eux $d\overrightarrow{S}(M_0)$ ([[#^figure1b|fig. 1b]]).
> ==**Dans le cas d’une surface fermée ([[#^figure1c|fig. 1c]]), les vecteurs unitaires $\overrightarrow{n}(M)$ sont toujours dirigés vers l’extérieur (normale sortante).**==
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
# Graphiques

# Expériences

# Autres notes
