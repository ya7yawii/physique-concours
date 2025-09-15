---
titre: "[[08-Changements de référentiels. Mécanique non galiléenne]]"
tags:
aliases:
crée: 13-09-2025, 11:28
---
# Formules
> [!note] Mouvement relatif de deux référentiels
> Le mouvement relatif de deux référentiels $\mathcal{R}_1$ et $\mathcal{R}_2$ est la superposition :
> - d’une rotation à vitesse angulaire $\overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1}$, appelé vecteur rotation d’entraînement de $\mathcal{R}_2$ par rapport à $\mathcal{R}_1$ ;
> - d’une translation caractérisée, par exemple, par $\displaystyle \overrightarrow{v}(O_2)_{/\mathcal{R}_1} = \left(\dfrac{d\overrightarrow{O_1O_2}}{dt}\right)_{\hspace{-0.6em}/\mathcal{R}_1}$, où $O_1$ et $O_2$ sont des points fixes de $\mathcal{R}_1$ et $\mathcal{R}_2$ respectivement.
> 
> Cas particuliers :
> - $\mathcal{R}_2$ est en translation par rapport à $\mathcal{R}_1$ : $\overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} = \overrightarrow{0}$. Notons que la translation de $\mathcal{R}_2$ n’est pas forcément rectiligne et que la trajectoire du point $O_2$ est, a priori, quelconque (cette trajectoire peut même être un cercle ; $\mathcal{R}_2$ est alors en translation circulaire par rapport à $\mathcal{R}_1$ ([[#^figure1]]).
> - $\mathcal{R}_2$ est en rotation autour d’un axe fixe de $\mathcal{R}_1$ : $\overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} = \dot{\theta}\overrightarrow{e_{z_1}}$ ([[#^figure2]]).

> [!note] Loi de dérivation composée d’un vecteur et composition des rotations
> Les évolutions d’un vecteur $U(t)$ dans deux référentiels $\mathcal{R}_1$ et $\mathcal{R}_2$ sont liées par la relation de dérivation composée : $\left(\dfrac{d\overrightarrow{U}}{dt}\right)_{\hspace{-0.6em}/\mathcal{R}_1} = \left(\dfrac{d\overrightarrow{U}}{dt}\right)_{\hspace{-0.6em}/\mathcal{R}_2} + \overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} \wedge \overrightarrow{U}(t)$
> Le mouvement de rotation relative de deux référentiels est, a priori, décrit par trois paramètres. Cette rotation peut éventuellement être décomposée en rotations « élémentaires » grâce à la loi de composition des rotations d’entraînement : $\overrightarrow{\Omega}_{\mathcal{R}_3/\mathcal{R}_1} = \overrightarrow{\Omega}_{\mathcal{R}_3/\mathcal{R}_2} + \overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1}$.

> [!note] Vitesse absolue, vitesse relative
> $\overrightarrow{v}(M)_{/\mathcal{R}_1} = \left(\dfrac{d\overrightarrow{O_1O_2}}{dt}\right)_{\hspace{-0.6em}/\mathcal{R}_1} + \left(\dfrac{d\overrightarrow{O_2M}}{dt}\right)_{\hspace{-0.6em}/\mathcal{R}_2} + \overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} \wedge \overrightarrow{O_2M}$
> Donc $\overrightarrow{v}(M)_{/\mathcal{R}_1} = \overrightarrow{v}(M)_{/\mathcal{R}_2} + [\overrightarrow{v}(O_2)_{/\mathcal{R}_1} + \overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} \wedge \overrightarrow{O_2M}]$ avec $\overrightarrow{v}(M)_{/\mathcal{R}_1}$ est la vitesse absolue et $\overrightarrow{v}(M)_{/\mathcal{R}_2}$ est la vitesse relative.

> [!note] Point coïncident
> Le point coïncident (ou coïncidant) est le point, fixe dans $\mathcal{R}_2$, qui coïncide avec le point M à l’instant t. Par définition, le point coïncident n’a pas de vitesse relative.
> La vitesse du point coïncident appelée aussi vitesse d’entraînement est : $\overrightarrow{v_e}(M) = \overrightarrow{v}(O_2)_{/\mathcal{R}_1} + \overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} \wedge \overrightarrow{O_2M}$.

> [!note] Cas où $\mathcal{R}_2$ est en translation par rapport à $\mathcal{R}_1$
> $\overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} = \overrightarrow{0}$ et $\overrightarrow{v_e}$ est ainsi indépendant du point M. Donc tous les points liés à $\mathcal{R}_2$ ont même vitesse par rapport à $\mathcal{R}_1$.

> [!note] Cas où $\mathcal{R}_2$ est en rotation par rapport à $\mathcal{R}_1$ autour d’un axe fixe
> Notons $(Oz) = (O_1z_1) = (O_2z_2)$ l’axe fixe dans le référentiel $\mathcal{R}_1$, autour duquel le référentiel $\mathcal{R}_2$ ([[#^figure3]]) tourne à la vitesse angulaire : $\overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} = \omega\overrightarrow{e_z} = \dot{\theta}\overrightarrow{e_z}$.
> Alors la vitesse d'entraînement est : $\overrightarrow{v_e}(M) = \overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} \wedge \overrightarrow{OM} = \omega\overrightarrow{e_z} \wedge \overrightarrow{HM}$.

> [!note] Accélération absolue
> $$
> \begin{multline*}
> \overrightarrow{a}(M)_{/\mathcal{R_1}} = \left(\dfrac{d\overrightarrow{v}(M)_{/\mathcal{R_1}}}{dt}\right)_{\hspace{-0.6em}/\mathcal{R}_1}\\
> = \left(\dfrac{d^{2}\overrightarrow{O_1O_2}}{dt^{2}}\right)_{\hspace{-0.6em}/\mathcal{R}_1} + \left(\dfrac{d^{2}\overrightarrow{O_2M}}{dt^{2}}\right)_{\hspace{-0.6em}/\mathcal{R}_2} + \dfrac{d\overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1}}{dt} \wedge \overrightarrow{O_2M} + \overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} \wedge \left(\dfrac{d\overrightarrow{O_2M}}{dt}\right)_{\hspace{-0.6em}/\mathcal{R}_1}\\
> = \left(\dfrac{d^{2}\overrightarrow{O_1O_2}}{dt^{2}}\right)_{\hspace{-0.6em}/\mathcal{R}_1} + \left(\dfrac{d^{2}\overrightarrow{O_2M}}{dt^{2}}\right)_{\hspace{-0.6em}/\mathcal{R}_2} + \dfrac{d\overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1}}{dt} \wedge \overrightarrow{O_2M} + \overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} \wedge \left(\dfrac{d\overrightarrow{O_2M}}{dt}\right)_{\hspace{-0.6em}/\mathcal{R}_2} \\
> + \overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} \wedge \left\{\left(\dfrac{d\overrightarrow{O_2M}}{dt}\right)_{\hspace{-0.6em}/\mathcal{R}_2} + \overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} \wedge \overrightarrow{O_2M}\right\}
> \end{multline*}
> $$
> Il n’est pas utile de préciser dans quel référentiel est exprimée la dérivée du vecteur rotation car la loi de dérivation composée, appliquée à ce vecteur, nous donne : $\displaystyle \left(\dfrac{d\overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1}}{dt}\right)_{\hspace{-0.6em}/\mathcal{R}_1} = \left(\dfrac{d\overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1}}{dt}\right)_{\hspace{-0.6em}/\mathcal{R}_2}$

Accélération relative : $\overrightarrow{a}(M)_{/\mathcal{R_2}} = \left(\dfrac{d^{2}\overrightarrow{O_2M}}{dt^{2}}\right)_{\hspace{-0.6em}/\mathcal{R}_2}$.
Accélération d’entraînement : $\overrightarrow{a_e}(M) = \left(\dfrac{d^{2}\overrightarrow{O_1O_2}}{dt^{2}}\right)_{\hspace{-0.6em}/\mathcal{R}_1}  + \dfrac{d\overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1}}{dt} \wedge \overrightarrow{O_2M} + \overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} \wedge \left\{ \overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} \wedge \overrightarrow{O_2M}\right\}$.
> [!warning]
> Il est inutile de vouloir retenir l’expression de $\overrightarrow{a_e}(M)$.


> [!note] Accélération de Coriolis
> $\overrightarrow{a}(M)_{/\mathcal{R_1}} = \overrightarrow{a}(M)_{/\mathcal{R_2}} + \overrightarrow{a_e}(M) + 2\overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} \wedge \overrightarrow{v}(M)_{/\mathcal{R}_2}$ avec $\overrightarrow{a_C}(M) = 2\overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} \wedge \overrightarrow{v}(M)_{/\mathcal{R}_2}$ est appelé accélération de Coriolis.

> [!note] Cas où $\mathcal{R}_2$ est en translation par rapport à $\mathcal{R}_1$
> - Les champs de vitesse d’entraînement et d’accélération d’entraînement sont uniformes : $\overrightarrow{v_e}(M) = \overrightarrow{v}(O_2)_{/\mathcal{R}_1}$ et $\overrightarrow{a_e}(M) = \overrightarrow{a}(O_2)_{/\mathcal{R}_1}$ ne dépendent pas du point M ;
> - il n’y a pas d’accélération de Coriolis.

> [!note] Cas où $\mathcal{R}_2$ est en rotation autour d’un axe fixe $(\Delta)$ de $\mathcal{R}_1$
> Comme précédemment (pour la vitesse), on suppose que la rotation se fait autour de l’axe commun $(\Delta) = (O_1z_1) = (O_2z_2)$ avec la vitesse angulaire $\overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} = \dot{\theta}\overrightarrow{e_z}$  ([[#^figure3]]).
> L’accélération d’entraînement du point M (de projection H sur $(\Delta)$) est : $\overrightarrow{a_e}(M) = \dfrac{d\overrightarrow{\Omega}}{dt} \wedge \overrightarrow{HM} - \overrightarrow{\Omega}^{2}\overrightarrow{HM}$.
> Si la rotation est uniforme, l’accélération d’entraînement est radiale et centripète : $\overrightarrow{a_e}(M) = - \overrightarrow{\Omega}^{2}\overrightarrow{HM}$

Relation fondamentale de la dynamique en référentiel non galiléen : $\overrightarrow{F} + \overrightarrow{F_{i_e}} + \overrightarrow{F_{i_C}} = m\overrightarrow{a}(M)_{/\mathcal{R}}$ où $\mathcal{R}$ est un référentiel en mouvement accéléré par rapport à un référentiel galiléen, $\overrightarrow{F_{i_e}} = -m\overrightarrow{a_e}(M)$ est la force d’inertie d'entraînement et $\overrightarrow{F_{i_C}} = -m\overrightarrow{a_C}(M)$ est la force d’inertie de Coriolis.

> [!note] Exemple d’un mouvement de translation accéléré de $\mathcal{R}$ dans $\mathcal{R_g}$
> Les forces d’inertie se réduisent à la seule force d’inertie d’entraînement : $\overrightarrow{F_{i_e}} = -m\overrightarrow{a_e}$ où l’accélération d’entraînement $\overrightarrow{a_e}$ est indépendante de la position du point M.

> [!note] Exemple d’une rotation de $\mathcal{R}$ autour d’un axe fixe de $\mathcal{R_g}$
> Il faut tenir compte des forces d’inertie mais si la rotation est uniforme à vitesse $\omega\overrightarrow{e_z} = \overrightarrow{cte}$ :
> - la force d’inertie d’entraînement est centrifuge : $\overrightarrow{F_{i_e}} = +m\omega^{2}\overrightarrow{HM}$ ;
> - la force d’inertie de Coriolis n’est en général pas nulle.

> [!note] Théorème du moment cinétique dans $\mathcal{R}$ non galiléen
> Le théorème du moment cinétique reste valable en référentiel non galiléen, en remplaçant la force galiléenne $\overrightarrow{F}$ par $\overrightarrow{F} + \overrightarrow{F_{i_e}} + \overrightarrow{F_{i_C}}$.

Théorème de l’énergie cinétique en référentiel non galiléen : $\Delta\mathcal{E}_K = \mathcal{T}(\overrightarrow{F}) + \mathcal{T}(\overrightarrow{F_{i_e}})$ avec le travail de la force d’inertie de Coriolis est nul.

> [!note]
> La force d’inertie d’entraînement travaille, mais n’est en général pas conservative. Cependant, il existe parfois des cas où la force d’inertie d’entraînement est conservative, par exemple :
> - Dans un référentiel $\mathcal{R}$ tournant à vitesse angulaire constante $\overrightarrow{\Omega}_{\mathcal{R}/\mathcal{R}_g} = \omega\overrightarrow{e_z}$ autour de l’axe $(Oz)$ fixe dans $\mathcal{R}_g$, la force d’inertie d’entraînement $\overrightarrow{F_{i_e}} = mr\omega^{2}\overrightarrow{e_r}$ dérive de l'énergie potentielle : $\mathcal{E}_{Pi_e} = -\frac{1}{2}mr^{2}\omega^{2}$ (coordonnées cylindriques d’axe $(Oz)$).
# Définitions
==**Référentiel galiléen**== :
Un référentiel est galiléen si l’application de la relation fondamentale de la dynamique à un point matériel permet de prévoir une évolution confirmée par l’expérience.

==**Classe des référentiels galiléens**== :
L’ensemble des référentiels galiléens est constitué par tous les référentiels en translation rectiligne et uniforme par rapport à l’un d’entre eux.

==**« Pseudo-forces »**== :
Les forces d’inertie ne traduisent pas une interaction, mais le caractère non galiléen du référentiel d’étude. Les effets de ces « pseudo-forces » sont cependant bien réels dans le référentiel non galiléen.
# Diagrammes

# Graphiques
$\mathcal{R}_2$ est en translation circulaire par rapport à $\mathcal{R}_1$ :
![[figure68.png]]^figure1

$\mathcal{R}_2$ est en rotation autour de l’axe $(Oz_1)$ dans $\mathcal{R}_1$ :
![[figure69.png]]^figure2

Rotation autour d’un axe fixe, trajectoire circulaire du point coïncident :
![[figure70.png]]^figure3
# Expériences

# Autres notes
