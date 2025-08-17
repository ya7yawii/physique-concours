---
titre: "[[Puissance et énergie en référentiel galiléen]]"
tags: 
aliases: 
crée: 16-08-2025, 17:14
---
# Formules
Puissance d'une force dans un référentiel : $\mathcal{P}(\overrightarrow{F})_{/\mathcal{R}} = \overrightarrow{F}.\overrightarrow{v}(M)_{/\mathcal{R}}$

Puissance d'une force de contact sans frottement : $\mathcal{P}(\overrightarrow{R})_{/\mathcal{R}} = \overrightarrow{R}.\overrightarrow{v} = 0$

Travail d'une force dans un référentiel : $\delta\mathcal{T}(\overrightarrow{F})_{/\mathcal{R}} = \mathcal{P}(\overrightarrow{F})_{/\mathcal{R}}dt = \overrightarrow{F}.d\overrightarrow{OM}$ où $\delta\mathcal{T}$ est la **circulation élémentaire** de la force $\overrightarrow{F}$.
> [!note]
> En intégrant l'équation ci-dessus, on obtient la circulation de la force $\overrightarrow{F}$ (ou le travail) qui dépend a priori de la forme de la trajectoire.

Travail d'une force constante au cours d'un déplacement fini : $\mathcal{T} = \overrightarrow{F}.\overrightarrow{M_1M_2}$

Théorème de la puissance cinétique : $\mathcal{P} = \dfrac{d\mathcal{E}_{K}}{dt}$ où $\mathcal{P}$ est la puissance de la force totale et $\mathcal{E}_{K}$ est l'énergie cinétique. 
> [!note]
> Ce résultat est obtenu en multipliant les deux membres de la relation fondamentale de la dynamique par $\overrightarrow{v}$

Théorème de l'énergie cinétique : $\mathcal{T} = \int_{t_1}^{t_2} \mathcal{P}dt = \int_{M_1}^{M_2} \overrightarrow{F}.d\overrightarrow{M} = \mathcal{E}_K(t_2) - \mathcal{E}_K(t_1)$
> [!note]
> Cette théorème permet de trouver l'équation différentielle du mouvement.
> Par exemple à un degré de liberté et sans vitesse initiale, cette théorème s'écrit comme suit:
> $$\mathcal{E}_K(t) - \mathcal{E}_K(0) = \frac{1}{2}m\left(\dfrac{dx}{dt}\right)^{2} = \int_{x_0}^{x} F(x')dx'$$

Un champ de force dérive d'une énergie potentielle s'il existe une fonction $\mathcal{E}_P(\overrightarrow{F})$, telle que le travail élémentaire de la force vérifie : $\delta\mathcal{T} = -d\mathcal{E}_P$.
Dans le cas d'un problème à un degré de liberté, noté x, nous aurons : $F(x) = -\dfrac{d\mathcal{E}_P(x)}{dx}$.

Énergie potentielle associée au champ de pesanteur uniforme : $\mathcal{E}_P = mgz + cte$ avec $(Oz)$ orienté vers le haut.

Énergie potentielle associée à l'effort de rappel élastique du ressort : $\mathcal{E}_P = \frac{1}{2}k(l - l_0)^{2} + cte$

Dans un référentiel galiléen, la variation de l'énergie mécanique est égale au travail des forces non conservatives : : $d\mathcal{E}_M = \delta\mathcal{T}_{nc}$ ou encore $\dfrac{d\mathcal{E}_M}{dt} = \mathcal{P}_{nc}$

Intégrale première de l'énergie : $\mathcal{E}_M = cte$
> [!note]
> Si une seule coordonnée suffit à repérer la position de M , cette équation est de la forme : $f(x, \dot{x}) = 0$
> Une telle situation à énergie mécanique constante est souvent une approximation en pratique, compte tenu de frottements inévitables en cas de liaisons. Elle permet néanmoins une première approche de la résolution des problèmes.
> Elle est remarquablement vérifiée pour le mouvement des planètes et des satellites.
# Définitions
==**Champ de force**== :
Une force qui ne dépend que de la position de son point d'application définit un champ de forces. C'est le cas des forces de pesanteur et de rappel.
> [!note]
> Il existe des forces n'obéissant pas à une telle définition ; c'est, par exemple, le cas des forces de contact.
> Si le travail de champ de forces ne dépend pas du chemin suivi ; le champ de force est dit <mark style="color: red">conservatif</mark>. Le travail d'une telle force le long d'une courbe fermée est nul.

La fonction énergie potentielle est dite ==stationnaire== lorsqu'elle passe par un maximum ou un minimum : localement, ces variations sont très lentes. En ces points, la force exercée sur la particule s’annule.
Pour l’exemple étudié ([[#^figure1]]), Les abscisses $x_0$ et $x_1$ correspondent donc à des ==positions d’équilibre==.

> [!note] Domaines accessibles à la trajectoire :
> Dans un champ de forces conservatives, l’évolution d’un point matériel est limitée aux zones où l’énergie potentielle reste inférieure à son énergie mécanique : $\mathcal{E}_P(x) \leqslant \mathcal{E}_M$ ([[#^figure2]]).

# Diagrammes

# Graphiques
Graphe des variations de l’énergie potentielle $\mathcal{E}_P(x)$ :
![[figure12.png]]^figure1

Évolution du mobile pour quelques valeurs significatives de son énergie mécanique :
![[figure13.png]]^figure2
- Cas ➀: état d’énergie mécanique $\mathcal{E}_{P_{0}}(x) \leqslant \mathcal{E}_{M_1} \leqslant 0$ : le point matériel ne peut s’échapper de la cuvette d’énergie potentielle, à proximité de l’abscisse d’équilibre $x_0$ : c’est un ==état lié==.
- Cas ➁: état d’énergie mécanique $0 \leqslant \mathcal{E}_{M_2} \leqslant \mathcal{E}_{P_{1}}$ : C’est encore un ==état lié==.
- Cas ➂: état d’énergie mécanique $0 \leqslant \mathcal{E}_{M_3} \leqslant \mathcal{E}_{P_{1}}$ : initialement, la particule est en dehors de la cuvette d’énergie potentielle. Le point matériel peut atteindre ici une abscisse minimale (point $A_3$). S’il est envoyé initialement vers $A_3$, nous voyons qu’il ne peut pas franchir la barrière de potentiel : après avoir atteint $A_3$, où il "rebondit", le point matériel repart à l’infini : c’est un ==état de diffusion==.
- Cas ➃: état d’énergie mécanique $\mathcal{E}_{M_4} \leqslant \mathcal{E}_{P_{1}}$ : C’est encore un ==état de diffusion==.
# Expériences

# Autres notes
