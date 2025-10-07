---
titre: "[[04-Moment cinétique d'un solide]]"
tags:
aliases:
crée: 07-10-2025, 10:28
---
# Formules
> [!warning]
> Rappelons que le mouvement de rotation autour d’un axe de rotation de direction fixe se rapporte à l’étude d’un mouvement de rotation autour d’un axe fixe dans le référentiel barycentrique.

Moment d’inertie d’un système par rapport à un axe : $\displaystyle J_{\Delta} = \sum_{i=1}^{N} m_id_{i}^{2}$ où $d_i$ est la distance entre le point matériel $P_i$ de masse $m_i$ et l'axe $\Delta$. $J_{\Delta}$ dépend de la répartition de masse du solide et de l’axe $\Delta$. Le moment d'inertie s'exprime en $kg.m^{2}$.

> [!note] Théorème d’Huygens
> Soit G le centre de masse d’un système matériel ([[#^figure1]]) dont la masse totale est M. Soit $J_{\Delta_G}$ le moment d’inertie de ce solide par rapport à un axe $\Delta_G$ passant par G. On note $J_{\Delta_O}$ le moment d’inertie de ce solide par rapport à un axe $\Delta_O$ passant par un point O du solide et parallèle à $\Delta_G$. Alors les deux moments d'inertie sont reliés par : $J_{\Delta_O} = J_{\Delta_G} + Md^{2}$.

Exemples :
![[mecanique2/attachments-mecanique2/figure17.png]]
![[mecanique2/attachments-mecanique2/figure18.png]]
![[mecanique2/attachments-mecanique2/figure19.png]][[#^info1|Clique ici pour savoir la différence entre la sphère et la boule.]]

> [!note] Moment cinétique en un point d’un axe de rotation fixe :
> $$
> \begin{align*}
> \displaystyle\overrightarrow{\sigma}_O(t) &= \iiint_{(S)} \overrightarrow{OP} \wedge \overrightarrow{v}(P,t) dm\\
> &= \iiint_{(S)} \overrightarrow{OP} \wedge (\overrightarrow{\Omega}(t) \wedge \overrightarrow{OP}) dm\\
> &= \iiint_{(S)} [OP^{2}\overrightarrow{\Omega}(t) - (\overrightarrow{\Omega}(t).\overrightarrow{OP})\overrightarrow{OP}]dm
> \end{align*}
> $$
> avec $\overrightarrow{\Omega}(t)$ est le vecteur instantané de rotation, porté par $\overrightarrow{e}_z$ ([[#^figure2]]). Cette expression est obtenue en utilisant [[#^info2|la formule du double produit vectoriel]].
> Considérons deux axes $(Ox)$ et $(Oy)$ attachés au solide et tels que $(Oxyz)$ soit orthogonal direct ([[#^figure3|fig. 3]]). On obtient ainsi, en notant $(x, y, z)$ les coordonnées d’un point P du solide : $OP^{2} = x^{2} + y^{2} + z^{2}$ et $\overrightarrow{\Omega}(t) = \Omega(t) \overrightarrow{e}_z$. Ainsi, le moment cinétique en O, point de l’axe de rotation, a pour expression : $\displaystyle\overrightarrow{\sigma}_O(t) = \iiint_{(S)} (r^{2}\overrightarrow{\Omega} - \Omega z(x\overrightarrow{e}_x + y\overrightarrow{e}_y))dm$ en posant $r^{2} = x^{2} + y^{2}$ où r désigne alors la distance d’un point P du solide à l’axe de rotation $(Oz)$.
> Le moment cinétique se décompose en deux contributions que l’on note respectivement $\overrightarrow{\sigma}_{O,\parallel}(t)$ et $\overrightarrow{\sigma}_{O,\perp}(t)$. La première est parallèle à l’axe, la seconde lui est orthogonale. Leurs expressions sont respectivement :
> $$
> \begin{align*}
> \overrightarrow{\sigma}_{O,\parallel}(t) &= \left(\iiint_{(S)} r^{2}dm\right)\overrightarrow{\Omega} = J_{Oz}\overrightarrow{\Omega}\\
> \overrightarrow{\sigma}_{O,\perp}(t) &= -\Omega(t)\left(\iiint_{(S)} z\,x\,dm\,\overrightarrow{e}_x + \iiint_{(S)} z\,y\,dm\,\overrightarrow{e}_y\right)
> \end{align*}
> $$
> Les deux intégrales qui apparaissent dans l'expression de $\overrightarrow{\sigma}_{O,\perp}(t)$ sont appelées « produits d’inertie » par rapport au plan $(Oxz)$, respectivement $(Oyz)$.

# Définitions
![[mecanique2/attachments-mecanique2/figure20.png]]^figure2

![[mecanique2/attachments-mecanique2/figure21.png]]^figure3
# Diagrammes
![[mecanique2/attachments-mecanique2/figure16.png]]^figure1
# Graphiques

# Expériences

# Autres notes
> [!warning] Différence entre une sphère et une boule
> La **sphère** est représent​ée par l'ensemble des points situés à une même distance du centre appelée «rayon».
> Quant à elle, la **boule** représente l'ensemble des points qui sont situés à une distance inférieure ou égale au rayon par rapport au centre.
> En d'autres mots, la sphère fait référence à la surface de la boule. Ainsi, le concept de sphère est associé à l'aire et celui de boule au volume.
^info1

> [!warning] Double produit vectoriel
> $\overrightarrow{A} \wedge (\overrightarrow{B} \wedge \overrightarrow{C}) = (\overrightarrow{A} . \overrightarrow{C})\overrightarrow{B} - (\overrightarrow{A} . \overrightarrow{B})\overrightarrow{C}$
^info2
