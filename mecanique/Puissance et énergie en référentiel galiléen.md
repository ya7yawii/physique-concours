---
titre: "[[Puissance et énergie en référentiel galiléen]]"
tags:
  - puissance
  - énergie
  - travail
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

> [!note] Technique de linéarisation :
> Essayons d'établir l'équation d'évolution du point matériel au voisinage de la position d'équilibre $x_e$ . Pour cela, développons son énergie potentielle au voisinage de l'équilibre $(x \approx x_e)$ :
> $$\mathcal{E}_P(x) = \mathcal{E}_P(x_e) + \left(\frac{\partial \mathcal{E}_P}{\partial x}\right)_{(x_e)}(x - x_e) + \frac{1}{2}\left(\frac{\partial^{2} \mathcal{E}_P}{\partial x^{2}}\right)_{(x_e)}(x - x_e)^{2} + \ldots$$
> La position $x_e$ étant un équilibre : $\left(\frac{\partial \mathcal{E}_P}{\partial x}\right)_{(x_e)} = -F_x(x_e) = 0$
> Nous supposerons, par la suite, que le terme d'ordre deux du développement n'est pas nul : $k = \left(\frac{\partial^{2} \mathcal{E}_P}{\partial x^{2}}\right)_{(x_e)} \neq 0$
> ce qui permet d'écrire, au voisinage de l'équilibre : $\mathcal{E}_P(x) \approx \mathcal{E}_P(x_e) + \frac{k}{2}(x - x_e)^{2}$ et $F_x(x) = -\frac{\partial \mathcal{E}_P}{\partial x} \approx -k(x - x_e)$
> dans ces conditions, l'équation d'évolution au voisinage de la position d'équilibre peut s'écrire : $m\dfrac{d^{2}(x - x_e)}{dt^{2}} = -k(x - x_e)$.
> La technique de linéarisation, lorsqu'elle est justifiée $(k \neq 0)$, permet de préciser la nature du mouvement au voisinage de la position d'équilibre. En fait, pour $k < 0$, l'équation d'évolution admet une solution qui diverge donc la position d'équilibre est instable et pour $k > 0$, l'équation d'évolution admet une solution sinusoïdale donc la position d'équilibre est stable. 
# Définitions
==**Champ de force**== :
Une force qui ne dépend que de la position de son point d'application définit un champ de forces. C'est le cas des forces de pesanteur et de rappel.
> [!note]
> Il existe des forces n'obéissant pas à une telle définition ; c'est, par exemple, le cas des forces de contact.
> Si le travail de champ de forces ne dépend pas du chemin suivi ; le champ de force est dit <mark style="color: red">conservatif</mark>. Le travail d'une telle force le long d'une courbe fermée est nul.

La fonction énergie potentielle est dite ==stationnaire== lorsqu'elle passe par un maximum ou un minimum : localement, ces variations sont très lentes. En ces points, la force exercée sur la particule s'annule.
Pour l'exemple étudié ([[#^figure1]]), Les abscisses $x_0$ et $x_1$ correspondent donc à des ==positions d'équilibre==.

> [!note] Domaines accessibles à la trajectoire :
> Dans un champ de forces conservatives, l'évolution d'un point matériel est limitée aux zones où l'énergie potentielle reste inférieure à son énergie mécanique : $\mathcal{E}_P(x) \leqslant \mathcal{E}_M$ ([[#^figure2]]).

> [!note]
> La trajectoire de phase d'un système conservatif à une dimension est une courbe à énergie mécanique constante ([[#^figure3]]).
# Diagrammes

# Graphiques
Graphe des variations de l'énergie potentielle $\mathcal{E}_P(x)$ :
![[figure12.png]]^figure1

Évolution du mobile pour quelques valeurs significatives de son énergie mécanique :
![[figure13.png]]^figure2
- Cas ➀: état d'énergie mécanique $0 \leqslant \mathcal{E}_{M_1} \leqslant \mathcal{E}_{P_{0}}(x)$ : le point matériel ne peut s'échapper de la cuvette d'énergie potentielle, à proximité de l'abscisse d'équilibre $x_0$ : c'est un ==état lié==.
- Cas ➁: état d'énergie mécanique $\mathcal{E}_{P_{1}} \leqslant \mathcal{E}_{M_2} \leqslant 0$ : C'est encore un ==état lié==.
- Cas ➂: état d'énergie mécanique $\mathcal{E}_{P_{1}} \leqslant \mathcal{E}_{M_3} \leqslant 0$ : initialement, la particule est en dehors de la cuvette d'énergie potentielle. Le point matériel peut atteindre ici une abscisse minimale (point $A_3$). S'il est envoyé initialement vers $A_3$, nous voyons qu'il ne peut pas franchir la barrière de potentiel : après avoir atteint $A_3$, où il "rebondit", le point matériel repart à l'infini : c'est un ==état de diffusion==.
- Cas ➃: état d'énergie mécanique $\mathcal{E}_{P_{1}} \leqslant \mathcal{E}_{M_4}$ : C'est encore un ==état de diffusion==.

>[!warning]
> Dans le livre, les inégalités sont inversées et je pense que c'est faux. 

Trajectoire de phase d'états liés et d'états de diffusion :
![[figure14.png]]^figure3
Les points $P_0(x_0, 0)$ et $P_1(x_1, 0)$ sont les points d'équilibre dans le plan de phase.
- État lié ➀ : La trajectoire de phase est fermée, ce qui caractérise une évolution périodique du mobile qui oscille entre deux abscisses extrêmes accessibles (points $A_1$ et $B_1$). Notons encore que cette trajectoire de phase ressemble à une ellipse, comme pour un oscillateur harmonique.
>[!note]
>La trajectoire de phase contourne le point d'équilibre dans le sens horaire.

- État lié ➁ : L'évolution est semblable à celle du cas précédent. Cependant, la trajectoire de phase n'est plus du tout elliptique : les oscillations sont d'amplitude assez importante, et les oscillations ne sont plus harmoniques.
- État de diffusion ➂ : La trajectoire de phase n'est plus fermée : le mouvement cesse d'être périodique.
- État de diffusion ➃ : L'évolution correspond encore à un rebroussement simple de la trajectoire de mobile qui finit par s'éloigner pour ne plus revenir. 
> [!note]
 > Nous visualisons ici très clairement la conservation de l'énergie mécanique du point matériel : lorsque l'énergie potentielle augmente, ce qui se produit en particulier lorsque l'abscisse approche la valeur $x_1$ , son énergie cinétique diminue. En effet, la trajectoire de phase se rapproche de l'axe $(Ox)$, ce qui met en évidence un ralentissement du mobile.

> [!note] Point attracteur : 
>  les trajectoires de phase contournent le point $P_0$ dans le sens horaire, tandis qu'elles tendent à éviter le point $P_1$ : le point $P_0$ est un ==centre attracteur==, pas le point $P_1$.

> [!note] Équilibre stable, équilibre instable :
> Un minimum (respectivement maximum) d'énergie potentielle correspond à une position d'équilibre stable (respectivement instable).
# Expériences
## Conservation de l'énergie mécanique (Roue de Maxwell)
> [!warning]
> Ce TP n'est pas dans le livre mais se trouve [en ligne](https://www.ummto.dz/fs/wp-content/uploads/2019/09/Ouvrir-Ici-.pdf).

![[Pasted image 20250818171606.png]]

### Détermination du moment d'inertie de la roue de Maxwell
Afin de déterminer le moment d'inertie de la roue de Maxwell, on étudie le chemin parcouru par le centre de gravité de la roue de Maxwell en fonction du temps. Pour ce faire, on varie la hauteur de chute séparant le point de départ de la roue du faisceau lumineux de la barrière lumineuse à fourchette, en déplaçant la barrière sur la tige (la hauteur est lue sur la règle graduée).
Il faut procéder comme suit :
- Remplir le tableau suivant : ![[Pasted image 20250818174001.png]]
- Tracer le graphe $z = f(t)$ et le graphe $z = g(t^{2})$
- A partir de ce $2^{ème}$ graphe et en utilisant la relation $z(t) = \frac{1}{2}\frac{mg}{m + \frac{J}{r^{2}}}t^{2}$, déterminer le moment d'inertie de la roue de Maxwell.
> [!warning]
> La relation ci-dessus est obtenue en écrivant l'énergie totale E comme la somme de l'énergie potentielle, l'énergie cinétique de translation et l'énergie cinétique de rotation (pour cette dernière voir chapitre théorème du moment cinétique [[sommaire#^e7d531]]) comme suit : $E = m\overrightarrow{g}\overrightarrow{z} + \frac{1}{2}m\overrightarrow{v}^{2} + \frac{1}{2}J\overrightarrow{w}^{2}$
> En utilisant $\overrightarrow{dz} = \overrightarrow{d\phi} \times \overrightarrow{r}$ et $\overrightarrow{v} = \frac{\overrightarrow{dz}}{dt} = \overrightarrow{w} \times \overrightarrow{r}$, on obtient $E = -mgz(t) + \frac{1}{2}mv^{2}(t) + \frac{1}{2}\frac{J}{r^{2}}v^{2}(t)$
> Comme l'énergie totale est constante dans le temps, on obtient après différentiation par rapport au temps la formule $z(t)$.

### Énergie potentielle
En utilisant le tableau ci-dessus, tracer le graphe donnant l'énergie potentielle $E_p$ en fonction du temps.

### Vitesse instantanée de la roue de Maxwell
Pour déterminer la vitesse instantanée de la roue, il suffit de brancher le compteur en porte électronique.
La vitesse est obtenue en faisant : $v(t + \frac{\Delta t}{2}) = \frac{\Delta z}{\Delta t}$ où $\Delta z$ est le diamètre de l'axe de la roue et $\Delta t$ (temps d'obscurcissement) le temps de séjour de l'axe de la roue dans le rayon lumineux (voir figure ci-dessous).
![[Pasted image 20250818183029.png]]

Il faut procéder comme suit :
- Remplir le tableau suivant : ![[Pasted image 20250818183157.png]]
- Tracer le graphe $v = f(t)$

### Énergie cinétique de translation
En utilisant le tableau ci-dessus, tracer le graphe donnant l'énergie cinétique de translation en fonction du temps.

### Énergie cinétique de rotation
En utilisant le tableau ci-dessus et la relation $v = wr$, tracer le graphe donnant l'énergie cinétique de rotation en fonction du temps.

Quelle est la conclusion que vous déduisez en comparant les 3 tracés de trois derniers graphes?

# Autres notes
> [!warning]
> Une force conservative ne dépend pas explicitement du temps car l'énergie n'est pas conservée lorsque la force dépend du temps.

> [!warning] Renversement du temps
>  Le renversement du temps (changement de variable t → – t) provoque le changement de signe de la vitesse. Ceci revient, dans le plan de phase, à effectuer une symétrie par rapport à $(Ox)$.
