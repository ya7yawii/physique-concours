---
titre: "[[03-Potentiel électrostatique]]"
tags:
aliases:
crée: 30-12-2025, 11:06
---
# Formules
Circulation du champ électrostatique : $\displaystyle C_{AB(\Gamma)} = \int_{A_{(\Gamma)}}^{B}\overrightarrow{E}.d\overrightarrow{l}$ ([[#^figure1|fig. 1]]).
> [!note] Conservation de la circulation du champ
> La circulation du champ, d’un point $A$ à un point $B$, se conserve lorsque nous passons d’un chemin $\Gamma$ à un chemin $\Gamma'$ reliant ces deux points : ==**la [[#^demo1|circulation du champ créée par une charge]] est conservative**== : $C_{AB(\Gamma)} = C_{AB(\Gamma')}$.
> ==**La circulation du champ électrostatique d'une distribution est aussi conservative.**==
> Ou, ce qui est équivalent :
> ==**La circulation du champ électrostatique sur un contour (courbe fermée) est nulle : $\displaystyle \oint_{\Gamma}\overrightarrow{E}.d\overrightarrow{l} = 0$. Le résultat est indépendant du contour.**==
> Signalons une conséquence de cette propriété qu’il faut avoir à l’esprit lors du tracé de lignes de champ : une ligne de champ électrostatique ne peut pas avoir la forme d’une boucle fermée sur elle-même. En effet, la circulation du champ sur cette boucle, orientée par le champ, ne pourrait être que strictement positive (à moins que le champ ne soit nul sur toute la boucle ou non défini en certains points, ce qui interdit alors de la définir comme une ligne de champ), ce qui est en contradiction avec la propriété précédente. ==**Il n'existe pas de ligne de champ fermée**==.

> [!note] Potentiel électrostatique
> ==**La différence de potentiel entre deux points $A$ et $B$ est : $\displaystyle V_A - V_B = \int_{A}^{B}\overrightarrow{E}.d\overrightarrow{l}$.**==
> Ainsi, l’expression du potentiel $V(M)$ (s’annulant à l’infini) créée par une charge ponctuelle $q$ en $O$ est : $V(M) = \frac{q}{4\pi\epsilon_0r}$.
> 
> ==**Le champ électrostatique est un champ de gradient s’écrivant : $\overrightarrow{E}(M) = -\overrightarrow{grad}_MV(M)$.**==
> Nous pouvons ainsi remarquer :
> ==**Un champ de vecteur $\overrightarrow{E}$ à circulation conservative est un champ de gradient.**==
> La circulation élémentaire du champ s’identifie ainsi au signe près à la différentielle (exacte) de la fonction $V(M)$ : $\overrightarrow{E}.d\overrightarrow{l} = E_xdx + E_ydy + E_zdz = -\left(\dfrac{\partial V}{\partial x}\right)dx - \left(\dfrac{\partial V}{\partial y}\right)dy - \left(\dfrac{\partial V}{\partial z}\right)dz = -dV$.
> Remarque : Le choix du signe moins est pour l’instant arbitraire ; nous verrons cependant qu’il est bien adapté à une association directe entre le potentiel électrostatique et la notion d’énergie potentielle.
> 
> Invariance de jauge : Le potentiel électrostatique créé n’est pas unique.
> ==**Le potentiel électrostatique est défini à une constante près.**==
> $V'(\overrightarrow{r}) = V(\overrightarrow{r}) + V_0$ ($V_0$ étant une constante arbitraire) est un autre potentiel acceptable. Ce choix d’origine, appelé aussi *choix de jauge*, ne modifie pas le champ, grandeur physique mesurable par ses effets (force de Coulomb) :
> ==**Le champ électrostatique est invariant de jauge, c’est-à-dire de la référence de potentiel.**==

> [!note] Expressions du potentiel
> ==**L’expression intégrale du potentiel, s’annulant à l’infini (référence de potentiel nulle à l’infini), créé par une distribution de charges $\mathcal{D}$ d’extension finie est de la forme : $\displaystyle V(M) = \iiint_{\mathcal{D}}\frac{1}{4\pi\epsilon_0}\frac{\delta q_P}{PM}$.**== En remplaçant $\delta q_P$ par son expression approprié, on trouve l'expression du potentiel pour une distribution volumique ou une distribution surfacique ou une distribution linéique.
> Remarques :
> - Ces expressions ne sont a priori applicables que dans le cas de distributions d’extension finie afin d’assurer une signification aux intégrales. Elles correspondent dans ce cas au choix de potentiel nul à l’infini.
> - L’application de la dernière expression au cas du fil infini étudié conduirait à une divergence logarithmique de l’intégrale, alors que l’intégrale correspondant au champ converge. Pour lever cette difficulté, nous choisissons par exemple $V_A = 0$ à distance $r_A = R$ du fil. En tout cas, il est impossible de fixer $V = 0$ à l’infini pour ce modèle.
> - Un autre problème de convergence de l’intégrale apparaît, si nous nous intéressons au calcul du potentiel, en un point de la distribution, c’est-à-dire en un point tel que $PM = 0$ lors du calcul de l’intégrale. Dans le cas d’une distribution volumique, l’intégrale converge s’il n’y a pas de charges à l’infini.
> 
> Expression du potentiel pour un ensemble de charges ponctuelles : ==**$\displaystyle\sum_{i=1}^{N}\frac{1}{4\pi\epsilon_0}\frac{q_i}{P_iM}$**==.

> [!note] Potentiel d’un disque uniformément chargé sur son axe
> Déterminons le potentiel $V(M)$ d’un disque, de rayon $R$ uniformément chargé avec la densité $\sigma$, en un point $M$ de son axe ([[#^figure2|fig. 2]]).
> Notons $(r, \theta)$ les coordonnées polaires d’un point $P$ du disque et $d^{2}S = rdrd\theta$ l’élément de surface associé à ce point. La charge élémentaire $d^{2}q = \sigma rdrd\theta$ (infiniment petit d’ordre deux) localisée en $P$, crée le potentiel élémentaire : $d^{2}V = \frac{1}{4\pi\epsilon_0}\frac{\sigma rdrd\theta}{\rho}$.
> Une première intégration sur $\theta$ fait apparaître la contribution à $V(M)$ d’une bande circulaire de rayon $r$ et d’épaisseur $dr$ : $\displaystyle dV = \frac{\sigma}{4\pi\epsilon_0}\frac{rdr}{\rho}\int_{0}^{2\pi}d\theta = \frac{\sigma}{2\epsilon_0}\frac{rdr}{\rho}$.
> Nous devons maintenant intégrer sur $r$. La dépendance de $\rho$ à $r$ ne s’exprimant pas simplement, nous prendrons comme variable d’intégration l’angle $\alpha$ : $r = z \tan\alpha$ et $\rho = \frac{z}{\cos\alpha}$.
> Après simplification, l’expression à intégrer s’écrit : $dV = \frac{\sigma z}{2\epsilon_0}\frac{\sin\alpha . d\alpha}{\cos^{2}\alpha} = -\frac{\sigma z}{2\epsilon_0}\frac{d(\cos\alpha)}{\cos^{2}\alpha}$.
> d'où : $V = \frac{\sigma z}{2\epsilon_0}\left(\frac{1}{\cos\alpha_{max}} - 1\right) = \frac{\sigma}{2\epsilon_0}(\rho_{max} - |z|) = \frac{\sigma}{2\epsilon_0}(\sqrt{z^{2} + R^{2}} - |z|)$.
> À la traversée de la surface chargée, le champ subit une discontinuité alors que le potentiel est continu ([[#^figure3|fig. 3]]). Ce dernier résultat est général et nous l’admettrons.
> ==**Le potentiel est continu quand il est défini.**==
> Remarque :
> Notons que la connaissance de la valeur du potentiel sur l’axe ne permet pas a priori de déterminer le champ sur celui-ci : $V(0, 0, z)$ est connue, et nous ne pouvons que calculer : $E_z(0, 0, z) = \dfrac{\partial V(0, 0, z)}{\partial z}$.
> Toutefois, l’axe $(Oz)$ étant un axe de révolution de la distribution, nous avons sur celui-ci $E_x = E_y = 0$, ce qui achève la détermination du champ sur l’axe, en accord avec le résultat établi au [[02-Champ électrostatique|chapitre 2]].
# Définitions

# Diagrammes
Courbe $\Gamma$ liant deux points $A$ et $B$
![[electromagnetisme1/attachments-electromagnetisme1/figure28.png]]^figure1

Potentiel d’un disque chargé
![[electromagnetisme1/attachments-electromagnetisme1/figure30.png]]^figure2
# Graphiques
Le potentiel est continu à la traversée d’une surface chargée
![[electromagnetisme1/attachments-electromagnetisme1/figure31.png]]^figure3
# Expériences

# Autres notes
> [!warning] Conservation de la circulation du champ d'une charge ponctuelle
> ![[electromagnetisme1/attachments-electromagnetisme1/figure29.png]]
^demo1