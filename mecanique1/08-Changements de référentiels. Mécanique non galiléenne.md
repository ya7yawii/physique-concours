---
titre: "[[08-Changements de référentiels. Mécanique non galiléenne]]"
tags:
  - référentiel-galiléen
  - entraînement
  - coriolis
crée: 13-09-2025, 11:28
---
# Formules
> [!note] Mouvement relatif de deux référentiels
> Le mouvement relatif de deux référentiels $\mathcal{R}_1$ et $\mathcal{R}_2$ est la superposition :
> - d'une rotation à vitesse angulaire $\overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1}$, appelé vecteur rotation d'entraînement de $\mathcal{R}_2$ par rapport à $\mathcal{R}_1$ ;
> - d'une translation caractérisée, par exemple, par $\displaystyle \overrightarrow{v}(O_2)_{/\mathcal{R}_1} = \left(\dfrac{d\overrightarrow{O_1O_2}}{dt}\right)_{\hspace{-0.6em}/\mathcal{R}_1}$, où $O_1$ et $O_2$ sont des points fixes de $\mathcal{R}_1$ et $\mathcal{R}_2$ respectivement.
> 
> Cas particuliers :
> - $\mathcal{R}_2$ est en translation par rapport à $\mathcal{R}_1$ : $\overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} = \overrightarrow{0}$. Notons que la translation de $\mathcal{R}_2$ n'est pas forcément rectiligne et que la trajectoire du point $O_2$ est, a priori, quelconque (cette trajectoire peut même être un cercle ; $\mathcal{R}_2$ est alors en translation circulaire par rapport à $\mathcal{R}_1$ ([[#^figure1]]).
> - $\mathcal{R}_2$ est en rotation autour d'un axe fixe de $\mathcal{R}_1$ : $\overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} = \dot{\theta}\overrightarrow{e_{z_1}}$ ([[#^figure2]]).

> [!note] Loi de dérivation composée d'un vecteur et composition des rotations
> Les évolutions d'un vecteur $U(t)$ dans deux référentiels $\mathcal{R}_1$ et $\mathcal{R}_2$ sont liées par la relation de dérivation composée : $\left(\dfrac{d\overrightarrow{U}}{dt}\right)_{\hspace{-0.6em}/\mathcal{R}_1} = \left(\dfrac{d\overrightarrow{U}}{dt}\right)_{\hspace{-0.6em}/\mathcal{R}_2} + \overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} \wedge \overrightarrow{U}(t)$
> Le mouvement de rotation relative de deux référentiels est, a priori, décrit par trois paramètres. Cette rotation peut éventuellement être décomposée en rotations « élémentaires » grâce à la loi de composition des rotations d'entraînement : $\overrightarrow{\Omega}_{\mathcal{R}_3/\mathcal{R}_1} = \overrightarrow{\Omega}_{\mathcal{R}_3/\mathcal{R}_2} + \overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1}$.

> [!note] Vitesse absolue, vitesse relative
> $\overrightarrow{v}(M)_{/\mathcal{R}_1} = \left(\dfrac{d\overrightarrow{O_1O_2}}{dt}\right)_{\hspace{-0.6em}/\mathcal{R}_1} + \left(\dfrac{d\overrightarrow{O_2M}}{dt}\right)_{\hspace{-0.6em}/\mathcal{R}_2} + \overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} \wedge \overrightarrow{O_2M}$
> Donc $\overrightarrow{v}(M)_{/\mathcal{R}_1} = \overrightarrow{v}(M)_{/\mathcal{R}_2} + [\overrightarrow{v}(O_2)_{/\mathcal{R}_1} + \overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} \wedge \overrightarrow{O_2M}]$ avec $\overrightarrow{v}(M)_{/\mathcal{R}_1}$ est la vitesse absolue et $\overrightarrow{v}(M)_{/\mathcal{R}_2}$ est la vitesse relative.

> [!note] Point coïncident
> Le point coïncident (ou coïncidant) est le point, fixe dans $\mathcal{R}_2$, qui coïncide avec le point M à l'instant t. Par définition, le point coïncident n'a pas de vitesse relative.
> La vitesse du point coïncident appelée aussi vitesse d'entraînement est : $\overrightarrow{v_e}(M) = \overrightarrow{v}(O_2)_{/\mathcal{R}_1} + \overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} \wedge \overrightarrow{O_2M}$.

> [!note] Cas où $\mathcal{R}_2$ est en translation par rapport à $\mathcal{R}_1$
> $\overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} = \overrightarrow{0}$ et $\overrightarrow{v_e}$ est ainsi indépendant du point M. Donc tous les points liés à $\mathcal{R}_2$ ont même vitesse par rapport à $\mathcal{R}_1$.

> [!note] Cas où $\mathcal{R}_2$ est en rotation par rapport à $\mathcal{R}_1$ autour d'un axe fixe
> Notons $(Oz) = (O_1z_1) = (O_2z_2)$ l'axe fixe dans le référentiel $\mathcal{R}_1$, autour duquel le référentiel $\mathcal{R}_2$ ([[#^figure3]]) tourne à la vitesse angulaire : $\overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} = \omega\overrightarrow{e_z} = \dot{\theta}\overrightarrow{e_z}$.
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
> Il n'est pas utile de préciser dans quel référentiel est exprimée la dérivée du vecteur rotation car la loi de dérivation composée, appliquée à ce vecteur, nous donne : $\displaystyle \left(\dfrac{d\overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1}}{dt}\right)_{\hspace{-0.6em}/\mathcal{R}_1} = \left(\dfrac{d\overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1}}{dt}\right)_{\hspace{-0.6em}/\mathcal{R}_2}$

Accélération relative : $\overrightarrow{a}(M)_{/\mathcal{R_2}} = \left(\dfrac{d^{2}\overrightarrow{O_2M}}{dt^{2}}\right)_{\hspace{-0.6em}/\mathcal{R}_2}$.
Accélération d'entraînement : $\overrightarrow{a_e}(M) = \left(\dfrac{d^{2}\overrightarrow{O_1O_2}}{dt^{2}}\right)_{\hspace{-0.6em}/\mathcal{R}_1}  + \dfrac{d\overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1}}{dt} \wedge \overrightarrow{O_2M} + \overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} \wedge \left\{ \overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} \wedge \overrightarrow{O_2M}\right\}$.
> [!warning]
> Il est inutile de vouloir retenir l'expression de $\overrightarrow{a_e}(M)$.


> [!note] Accélération de Coriolis
> $\overrightarrow{a}(M)_{/\mathcal{R_1}} = \overrightarrow{a}(M)_{/\mathcal{R_2}} + \overrightarrow{a_e}(M) + 2\overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} \wedge \overrightarrow{v}(M)_{/\mathcal{R}_2}$ avec $\overrightarrow{a_C}(M) = 2\overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} \wedge \overrightarrow{v}(M)_{/\mathcal{R}_2}$ est appelé accélération de Coriolis.

> [!note] Cas où $\mathcal{R}_2$ est en translation par rapport à $\mathcal{R}_1$
> - Les champs de vitesse d'entraînement et d'accélération d'entraînement sont uniformes : $\overrightarrow{v_e}(M) = \overrightarrow{v}(O_2)_{/\mathcal{R}_1}$ et $\overrightarrow{a_e}(M) = \overrightarrow{a}(O_2)_{/\mathcal{R}_1}$ ne dépendent pas du point M ;
> - il n'y a pas d'accélération de Coriolis.

> [!note] Cas où $\mathcal{R}_2$ est en rotation autour d'un axe fixe $(\Delta)$ de $\mathcal{R}_1$
> Comme précédemment (pour la vitesse), on suppose que la rotation se fait autour de l'axe commun $(\Delta) = (O_1z_1) = (O_2z_2)$ avec la vitesse angulaire $\overrightarrow{\Omega}_{\mathcal{R}_2/\mathcal{R}_1} = \dot{\theta}\overrightarrow{e_z}$  ([[#^figure3]]).
> L'accélération d'entraînement du point M (de projection H sur $(\Delta)$) est : $\overrightarrow{a_e}(M) = \dfrac{d\overrightarrow{\Omega}}{dt} \wedge \overrightarrow{HM} - \overrightarrow{\Omega}^{2}\overrightarrow{HM}$.
> Si la rotation est uniforme, l'accélération d'entraînement est radiale et centripète : $\overrightarrow{a_e}(M) = - \overrightarrow{\Omega}^{2}\overrightarrow{HM}$

Relation fondamentale de la dynamique en référentiel non galiléen : $\overrightarrow{F} + \overrightarrow{F_{i_e}} + \overrightarrow{F_{i_C}} = m\overrightarrow{a}(M)_{/\mathcal{R}}$ où $\mathcal{R}$ est un référentiel en mouvement accéléré par rapport à un référentiel galiléen, $\overrightarrow{F_{i_e}} = -m\overrightarrow{a_e}(M)$ est la force d'inertie d'entraînement et $\overrightarrow{F_{i_C}} = -m\overrightarrow{a_C}(M)$ est la force d'inertie de Coriolis.

> [!note] Exemple d'un mouvement de translation accéléré de $\mathcal{R}$ dans $\mathcal{R_g}$
> Les forces d'inertie se réduisent à la seule force d'inertie d'entraînement : $\overrightarrow{F_{i_e}} = -m\overrightarrow{a_e}$ où l'accélération d'entraînement $\overrightarrow{a_e}$ est indépendante de la position du point M.

> [!note] Exemple d'une rotation de $\mathcal{R}$ autour d'un axe fixe de $\mathcal{R_g}$
> Il faut tenir compte des forces d'inertie mais si la rotation est uniforme à vitesse $\omega\overrightarrow{e_z} = \overrightarrow{cte}$ :
> - la force d'inertie d'entraînement est centrifuge : $\overrightarrow{F_{i_e}} = +m\omega^{2}\overrightarrow{HM}$ ;
> - la force d'inertie de Coriolis n'est en général pas nulle.

> [!note] Théorème du moment cinétique dans $\mathcal{R}$ non galiléen
> Le théorème du moment cinétique reste valable en référentiel non galiléen, en remplaçant la force galiléenne $\overrightarrow{F}$ par $\overrightarrow{F} + \overrightarrow{F_{i_e}} + \overrightarrow{F_{i_C}}$.

Théorème de l'énergie cinétique en référentiel non galiléen : $\Delta\mathcal{E}_K = \mathcal{T}(\overrightarrow{F}) + \mathcal{T}(\overrightarrow{F_{i_e}})$ avec le travail de la force d'inertie de Coriolis est nul.

> [!note]
> La force d'inertie d'entraînement travaille, mais n'est en général pas conservative. Cependant, il existe parfois des cas où la force d'inertie d'entraînement est conservative, par exemple :
> - Dans un référentiel $\mathcal{R}$ tournant à vitesse angulaire constante $\overrightarrow{\Omega}_{\mathcal{R}/\mathcal{R}_g} = \omega\overrightarrow{e_z}$ autour de l'axe $(Oz)$ fixe dans $\mathcal{R}_g$, la force d'inertie d'entraînement $\overrightarrow{F_{i_e}} = mr\omega^{2}\overrightarrow{e_r}$ dérive de l'énergie potentielle : $\mathcal{E}_{Pi_e} = -\frac{1}{2}mr^{2}\omega^{2}$ (coordonnées cylindriques d'axe $(Oz)$).
# Définitions
==**Référentiel galiléen**== :
Un référentiel est galiléen si l'application de la relation fondamentale de la dynamique à un point matériel permet de prévoir une évolution confirmée par l'expérience.

==**Classe des référentiels galiléens**== :
L'ensemble des référentiels galiléens est constitué par tous les référentiels en translation rectiligne et uniforme par rapport à l'un d'entre eux.

==**« Pseudo-forces »**== :
Les forces d'inertie ne traduisent pas une interaction, mais le caractère non galiléen du référentiel d'étude. Les effets de ces « pseudo-forces » sont cependant bien réels dans le référentiel non galiléen.
# Diagrammes

# Graphiques
$\mathcal{R}_2$ est en translation circulaire par rapport à $\mathcal{R}_1$ :
![[mecanique1/attachments-mecanique1/figure68.png]]^figure1

$\mathcal{R}_2$ est en rotation autour de l'axe $(Oz_1)$ dans $\mathcal{R}_1$ :
![[figure69.png]]^figure2

Rotation autour d'un axe fixe, trajectoire circulaire du point coïncident :
![[figure70.png]]^figure3
# Expériences
## Force Centrifuge
> [!warning]
> Ce TP n'est pas dans le livre mais se trouve dans les liens suivants :[lien 1](https://ilm-perso.univ-lyon1.fr/~oramos/documents/TPMechanics/fasciculeTP.pdf), [lien 2](https://fr.scribd.com/document/814469940/TP-ENSAM), [lien 3](https://fr.scribd.com/document/377710851/Tp-Force-Centrifuge).

![[figure71.png]]

### Détermination de la force centrifuge en fonction de la masse du corps (rayon et vitesse angulaire constants)
- Choisir une vitesse de rotation adéquate et le rayon de rotation qui place le chariot au début du bras en rotation. Noter ces valeurs.
- Mesurer la force centrifuge pour différentes masses du chariot (réaliser au moins 6 mesures, pour la première mesure on prendra le chariot seul, et on ajoutera un poids de 10 g pour chaque mesure).
- L'incertitude sur la masse sera prise nulle. Evaluer l'incertitude sur la mesure de la force.
- Tracer l'évolution de la force en fonction de la masse. Modéliser (choisir le modèle adéquat, voir la théorie) la courbe et noter les paramètres de modélisation.
- Déduire de la courbe (sa modélisation) la pente expérimentale et son incertitude. Les noter et donner l'unité de la pente.
- Évaluer l'incertitude sur la période de rotation du moteur, puis sur sa vitesse angulaire, évaluer l'incertitude sur la mesure du rayon. Calculer la pente théorique (donner son expression, sa valeur et son unité) et son incertitude.
- Comparer théorie et expérience. Commenter, notamment la valeur des incertitudes.
### Détermination de la force centrifuge en fonction de la vitesse angulaire (masse et rayon constants)
- Choisir une masse de chariot adéquate et le rayon de rotation qui place le chariot à mi-course du bras en rotation. Noter ces valeurs.
- Mesurer la force centrifuge pour différentes vitesses de rotation (réaliser au moins 6 mesures).
- Évaluer l'incertitude sur la mesure de la force, sur la mesure de la période de rotation pour en déduire celle sur la vitesse angulaire de rotation.
- Tracer l'évolution de la force en fonction de la vitesse de rotation (et de la vitesse de rotation portée au carré). Modéliser (choisir le modèle adéquat) les courbes.
- Déduire de la courbe de vitesse au carré (sa modélisation) la pente expérimentale et son incertitude. Les noter et donner l'unité de la pente.
- L'incertitude sur la masse sera prise nulle. Évaluer l'incertitude sur la mesure du rayon. Calculer la pente théorique (donner son expression, sa valeur et son unité) et son incertitude. Les noter.
- Comparer théorie et expérience. Commenter, notamment la valeur des incertitudes.
### Détermination de la force centrifuge en fonction de la distance du corps à l'axe de rotation (masse et vitesse angulaire constantes)
- Choisir une vitesse de rotation et une masse du chariot adéquats. Noter ces valeurs.
- Mesurer la force centrifuge pour différents rayons de rotation (réaliser au moins 6 mesures).
- Évaluer l'incertitude sur la mesure de la force et sur la mesure du rayon.
- Tracer l'évolution de la force en fonction du rayon. Modéliser (choisir le modèle adéquat) la courbe.
- Déduire de la courbe (sa modélisation) la pente expérimentale et son incertitude. Les noter et donner l'unité de la pente.
- Évaluer l'incertitude sur la période de rotation du moteur puis sur sa vitesse angulaire, l'incertitude sur la masse sera prise nulle. Calculer la pente théorique (donner son expression, sa valeur et son unité) et son incertitude. Les noter.
- Comparer théorie et expérience. Commenter, notamment la valeur des incertitudes.
### Détermination de la raideur du ressort
Le dynamomètre est en fait un simple ressort, parallèle à l'axe $Oz$. Il est relié à la voiture par un fil tendu et une poulie ; en conséquence, le fil tendue et la poulie transmettent intégralement la force exercée par le ressort sur la voiture, comme si celle-ci était directement accrochée au ressort. Le bilan des forces s'écrit donc, en norme, $k(l- l_0) = mr\omega^{2}$.
- Choisir une vitesse de rotation et une masse adéquates et le rayon de rotation qui place le chariot à mi-course du bras en rotation. Noter ces valeurs ;
- A partir du bilan des forces, déterminer la raideur du ressort.
# Autres notes
