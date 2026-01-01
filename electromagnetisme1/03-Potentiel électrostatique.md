---
titre: "[[03-Potentiel électrostatique]]"
tags:
  - circulation
  - potentiel-électrostatique
  - énergie-potentielle-d-interaction-électrostatique
  - conducteur-en-équilibre-électrostatique
  - condensateur-plan
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

> [!note] Surfaces équipotentielles d’une distribution
> Une surface équipotentielle, de potentiel $V_0$, est définie par l’équation $V(M) = V_0$. Deux surfaces équipotentielles correspondant à des potentiels distincts ne peuvent pas avoir d’intersection.
> 
> Considérons deux points très proches appartenant à une même surface équipotentielle de potentiel $V_0$ ([[#^figure4|fig. 4]]). Par définition du potentiel $V(N) = V(M) - \overrightarrow{E}(M) . d\overrightarrow{r}$, et par définition de la surface $V(N) = V(M)$. Le champ électrostatique est donc normal à la surface équipotentielle (propriété du gradient).
> 
> Considérons maintenant une ligne de champ rencontrant deux surfaces équipotentielles, de potentiels $V_1$ et $V_2$, aux points $M_1$ et $M_2$ ([[#^figure5|fig. 5]]). Si le champ oriente la ligne de $M_1$ vers $M_2$, nous avons : $\displaystyle V_2 - V_1 = V(M_2) - V(M_1) = \int_{M_1}^{M_2}-\overrightarrow{E}.d\overrightarrow{l} < 0$.
> 
> ==**Le champ est perpendiculaire aux surfaces équipotentielles et les lignes de champ sont orientées dans le sens des potentiels décroissants.**==
> 
> Remarques :
> - L’orthogonalité des lignes de champ aux surfaces équipotentielles est à retenir pour effectuer des tracés qualitatifs de lignes de champ et de coupes de surfaces équipotentielles sur une figure.
> Attention cependant : le champ électrostatique est perpendiculaire aux surfaces équipotentielles : mais nous pourrons rencontrer le cas d’une ligne de champ non perpendiculaire à une surface équipotentielle, lorsque le point qu’elle atteint sur cette surface est un point de champ nul.
> - Sur une carte de lignes équipotentielles, les régions de champ intense sont caractérisées par des lignes équipotentielles rapprochées. En effet, si $|V_2 - V_1|$ est faible, il est possible d’évaluer le champ en $M_1$ par l’expression : $|V_2 - V_1| \approx E(M_1) . M_1M_2$. Plus $M_1M_2$ est faible, plus $E(M_1)$ est intense. Ainsi sur la [[#^figure6|figure 6]], le module du champ est plus intense en $A$ qu’en $B$ : $|\overrightarrow{E}(A)| > |\overrightarrow{E}(B)|$.

> [!note] Considérations de symétrie
> - Champ scalaire :
> La circulation élémentaire $\overrightarrow{E}.d\overrightarrow{l}$ fait intervenir le produit des deux vecteurs (polaires), et possède les propriétés de symétrie d’un champ scalaire.
> Nous pourrons choisir la jauge (constante d’intégration) de façon à obtenir un potentiel $V(\overrightarrow{r})$ ayant les propriétés de symétrie de la distribution de charges.
> Par exemple, dans le cas d’une distribution $\mathcal{D}$ admettant un plan d’antisymétrie $\Pi^{*}$, nous prendrons $V = 0$ sur ce plan. En un point $M$ et en son symétrique $M'$ par rapport au plan $\Pi^{*}$, le potentiel prend alors des valeurs opposées.
> Dans le cas d’une distribution $\mathcal{D}$ admettant un plan de symétrie $\Pi$, le potentiel a la même valeur en un point $M$ et en son symétrique $M'$ par rapport au plan $\Pi$.
> Les propriétés de symétrie du potentiel peuvent aussi s’obtenir à l’aide de celles du champ créé par la distribution étudiée. Pour les symétries usuelles, les propriétés du potentiel s’obtiennent intuitivement comme l’illustrent les exemples qui suivent.
> - Invariances :
> Étudions l’expression générale du potentiel pour diverses invariances.
> 	- Pour une *distribution invariante par toute translation parallèlement à l’axe $(Oz)$*, le potentiel ne peut dépendre que des variables de position $x$ et $y$. Ceci peut être confirmé par le résultat obtenu au [[02-Champ électrostatique|chapitre 2]], donnant la forme du champ : $\overrightarrow{E}(x, y, z) = \overrightarrow{E}(x, y) = E_x(x, y)\overrightarrow{e}_x + E_y(x, y)\overrightarrow{e}_y$.
> 	- Pour une *distribution possédant la symétrie de révolution par rapport à l’axe $(Oz)$*, il apparaît immédiatement que la fonction potentiel ne dépend que des variables $r$ et $z$ des coordonnées cylindriques d’axe $(Oz)$, en accord avec le champ déjà obtenu : $\overrightarrow{E}(r, \theta, z) = E_r(r, z)\overrightarrow{e}_r + E_z(r, z)\overrightarrow{e}_z$.
> 	- Pour une *distribution possédant la symétrie cylindrique d’axe $(Oz)$*, la fonction potentiel ne peut dépendre que de la distance $r$ à l’axe $(Oz)$ : $V(\overrightarrow{r}) = V(r, \theta, z) = V(r)$, en accord avec la forme du champ : $\overrightarrow{E}(r, \theta, z) = E(r)\overrightarrow{e}_r$.
> 	-  Pour une *distribution possédant la symétrie sphérique de centre $O$*, la fonction potentiel ne dépend que de la distance $r$ au point $O$ : $V(\overrightarrow{r}) = V(r, \theta, \varphi) = V(r)$.
> 	Le champ est d’ailleurs de la forme : $\overrightarrow{E}(r, \theta, \varphi) = E(r)\overrightarrow{e}_r$.

> [!note] Énergie potentielle d’une charge placée dans un champ
> Le travail de la force électrostatique $\overrightarrow{f} = q\overrightarrow{E}$ correspondant à un déplacement de la charge $q$ d’un point $A$ à un point $B$ est ainsi $W_{AB} = -q(V_B - V_A)$.
> Ce travail ne dépend pas du chemin suivi et s’identifie à la variation d’une fonction d’état qui ne dépend que de la position de la particule.
> ==**L’énergie potentielle d’interaction entre une charge $q$ et un champ électrostatique $\overrightarrow{E}$ créant le potentiel $V$ est $\mathcal{E}_P = qV$.**==
> La force de Coulomb $\overrightarrow{f} = q\overrightarrow{E}$ exercée par le champ électrostatique dérive de cette énergie potentielle, définie (comme le potentiel électrostatique) à une constante près : $\overrightarrow{f} = q\overrightarrow{E} = -\overrightarrow{grad}\,\mathcal{E}_P$.
> Ainsi, ce champ de force est un champ de gradient et, à ce titre, la force électrostatique est une force conservative : son travail entre deux points $A$ et $B$ ne dépend pas du chemin suivi.
> Le travail de la force électrostatique entre $A$ et $B$ est : $W_{AB} = -\mathcal{E}_{P(B)} + \mathcal{E}_{P(A)} = -\Delta\mathcal{E}_{P}$.

> [!note] Énergie d’interaction de deux charges ponctuelles
> ==**L’énergie potentielle d’interaction électrostatique entre les charges $q_1$ et $q_2$ est : $\displaystyle \mathcal{E}_{P_{12}} = \frac{1}{4\pi\epsilon_0}\frac{q_1q_2}{M_1M_2}$.**==
> En notant $V_1(M_2)$ le potentiel créé par la charge $q_1$ au point $M_2$ et $V_2(M_1)$ le potentiel créé par la charge $q_2$ au point $M_1$, nous pouvons aussi écrire cette énergie sous les formes suivantes : $\mathcal{E}_{P_{12}} = q_1V_2(M_1) = q_2V_1(M_2) = \frac{1}{2}[q_1V_2(M_1)  + q_2V_1(M_2)]$.

> [!note] Conducteurs en équilibre électrostatique
> Un conducteur est un corps qui contient des *charges libres*, c’est-à-dire des particules chargées capables de se déplacer sous l’action de forces appliquées. En électrostatique, la seule force considérée est la force électrostatique : $\overrightarrow{F} = q\overrightarrow{E}$.
> Un conducteur est en *équilibre électrostatique* quand ses charges libres n’ont aucun mouvement d’ensemble dans un référentiel lié au conducteur :
> ==**Le champ électrostatique $E(P)$ est alors nul dans tout le volume du conducteur.**==
> Il est possible de démontrer (et nous admettrons le résultat) que :
> ==**En un point $P$ situé à l’intérieur d’un conducteur, la densité volumique de charge $\rho(P)$ est nulle dans un conducteur en équilibre électrostatique.**==
> ==**La charge d’un conducteur en équilibre électrostatique est donc superficielle et elle est caractérisée par la densité surfacique de charges $\sigma(Q)$.**==
> 
> ==**En un point $M$ situé au voisinage immédiat d’un point $Q$ de la surface extérieure d’un conducteur, où la densité surfacique est $\sigma(Q)$, le champ vaut : $\overrightarrow{E}(M) = \frac{\sigma(Q)}{\epsilon_0}\overrightarrow{n}(Q)$ avec $\overrightarrow{n}(Q)$ le vecteur unitaire de la normale sortante en $Q$ pris à la surface du conducteur en équilibre électrostatique ([[#^figure7|fig. 7]]).**==
> 
> Par ailleurs, de la relation $\overrightarrow{E} = -\overrightarrow{grad}(V)$ nous en déduisons que *le potentiel $V(M)$ est constant dans un conducteur en équilibre électrostatique*. La continuité du potentiel à la traversée des surfaces chargées, nous permet d’affirmer que : ==**La surface d’un conducteur est une surface équipotentielle.**==
> Les lignes de champ sont donc normales à la surface des conducteurs en équilibre électrostatique.
> Sur la [[#^figure8|figure 8]], un conducteur porté au potentiel $V$ est placé en présence d’une charge ponctuelle $Q > 0$. À l’équilibre électrostatique, on observe sur le conducteur une ligne neutre $(\sigma = 0)$ (en pointillés) séparant une région où $(\sigma < 0)$ (en bleu) d’une autre où $(\sigma > 0)$. Concernant le conducteur, on voit que les lignes de champ partent des régions chargées positivement et qu’elles aboutissent sur des régions chargées négativement.

> [!note] Condensateur plan
> Considérons un ensemble de deux plaques métalliques parallèles $A_1$ et $A_2$, reliées à une source de tension constante $U = V_1 - V_2$. Notons $e$ la distance entre les deux plaques et $S$ l’aire des surfaces en regard ([[#^figure9|fig. 9]]).
> Quand $e$ est faible devant les dimensions latérales des plaques, cet ensemble des deux plaques est appelé *condensateur* et les plaques métalliques baptisées *armatures*.
> Dans ces conditions, nous constatons que le champ est beaucoup plus intense dans la région interarmatures. Pour la suite, *nous négligerons les effets de bord*, c’est-à-dire les effets liés à la présence d’un champ faible à l’extérieur du condensateur. Cette approximation est excellente dans les conditions où nous la faisons.
> Cela étant, nous observons que les lignes de champ sont parallèles, ce qui est la caractéristique d’un *champ uniforme* : $\overrightarrow{E} = E_z \overrightarrow{e}_z$ $(E_z = cte)$.
> En outre, les lignes de champ partent de l’une des armatures pour aboutir sur l’autre, cela signifie que les densités surfaciques des deux faces en regard sont de signes opposés. Comme le champ est uniforme, cela signifie plus précisément que *ces densités surfaciques sont uniformes et opposées*.
> ==**Les armatures d’un condensateur portent, sur leurs faces en regard, des charges opposées.**==
> Dans le cas de [[#^figure9|figure 9]], notons $q$ la charge positive de l’armature $A_1$, il vient : $q = \sigma S = \epsilon_0E_zS$.
> La circulation du champ électrostatique entre les deux plaques, calculée le long d’une ligne de champ, s’écrit : $\displaystyle U = V_1 - V_2 = \int_{M_1}^{M_2}\overrightarrow{E}.d\overrightarrow{l} = E_z\int_{0}^{z}dz = E_z e$.
> En éliminant $E_z$ entre les deux relations précédentes, il vient : $q = \frac{\epsilon_0S}{e}U$.
> ==**Les charges $\pm q$ des armatures d’un condensateur sont proportionnelles à la tension U appliquée entre les armatures.**==
> Le facteur de proportionnalité $C = \frac{\epsilon_0S}{e}$ est appelé **capacité du condensateur plan**. Il s’évalue en farad $(F)$.
# Définitions

# Diagrammes
Courbe $\Gamma$ liant deux points $A$ et $B$
![[electromagnetisme1/attachments-electromagnetisme1/figure28.png]]^figure1

Potentiel d’un disque chargé
![[electromagnetisme1/attachments-electromagnetisme1/figure30.png]]^figure2

Sur la surface iso-$V_0$ : $V(M) = V(N)$
![[electromagnetisme1/attachments-electromagnetisme1/figure32.png]]^figure4

$\overrightarrow{E}$ est orienté dans le sens des potentiels décroissants : $V_1 > V_2$
![[electromagnetisme1/attachments-electromagnetisme1/figure33.png]]^figure5

$\overrightarrow{E}(M) = \frac{\sigma(Q)}{\epsilon_0}\overrightarrow{n}(Q)$. $M$ est au voisinage immédiat de $Q$
![[electromagnetisme1/attachments-electromagnetisme1/figure35.png]]^figure7

Influence d’une charge $Q$ $(> 0)$ sur un conducteur
![[electromagnetisme1/attachments-electromagnetisme1/figure36.png]]^figure8

Condensateur plan
![[electromagnetisme1/attachments-electromagnetisme1/figure37.png]]^figure9
# Graphiques
Le potentiel est continu à la traversée d’une surface chargée
![[electromagnetisme1/attachments-electromagnetisme1/figure31.png]]^figure3

L’équipotentielle de potentiel $V_0$ est un cercle de diamètre $AB$, avec $A(+6)$ et $B(+12)$ 
![[electromagnetisme1/attachments-electromagnetisme1/figure34.png]]^figure6
# Expériences
> [!warning]
> Voici des exemples de travaux pratiques qui abordent le sujet de ce chapitre : le [lien 1](https://www.fresnel.fr/perso/soriano/fr/tpSPI401AJ.pdf), le [lien 2](https://fr.scribd.com/document/794459701/TP-7-Champ-Electrostatique-Cree-Par-Un-Condensateur-Plan-Correction), le [lien 3](https://fr.scribd.com/document/925428799/Copy-of-TP-electromagnetisme).
# Autres notes
> [!warning] Conservation de la circulation du champ d'une charge ponctuelle
> ![[electromagnetisme1/attachments-electromagnetisme1/figure29.png]]
^demo1