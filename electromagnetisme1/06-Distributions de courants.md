---
titre: "[[06-Distributions de courants]]"
tags:
  - courant-électrique
  - intensité-électrique
  - distribution-de-courant
  - courant-filiforme
  - courant-volumique
  - vecteur-densité-volumique-de-courants
  - courant-surfacique
  - vecteur-densité-surfacique-de-courants
  - symétrie
  - invariance
crée: 05-01-2026, 09:09
---
# Formules
> [!note] Intensité électrique
> Considérons une surface $S$ liée au référentiel $\mathcal{R}$, munie en tout point $M$ d'une normale orientée par un vecteur unitaire $\overrightarrow{n}$ ([[#^figure1|fig. 1]]). Notons $\delta Q_m$ la charge mobile traversant cette surface entre les instants $t$ et $t + \delta t$, comptée positivement dans le sens choisi par l'orientation de $S$.
> *Remarque : L'intervalle de temps élémentaire $\delta t$ est infinitésimal si $\frac{\delta t}{T} \ll 1$, $T$ étant une durée caractéristique du phénomène étudié (par exemple la période pour un courant sinusoïdal).*
> ==**L'intensité $I(S, t)$ du courant électrique à travers une surface $S$ est liée à la charge $\delta Q_m$ qui traverse $S$ entre les instants $t$ et $t + \delta t$ par la relation $\delta Q_m = I(S, t)\delta t$.**==
> ==**L'intensité, grandeur électrique, dépend de l'orientation de $S$.**==
> ==**Elle s'exprime en ampère (symbole : $A$), unité de base du Système International d'unités.**==

> [!note] Distributions de courants : Courants filiformes : Conducteur filiforme
> Un fil conducteur de faible section à l'échelle macroscopique peut être assimilé à une courbe $\mathcal{C}$ (sans épaisseur). Dans cette modélisation, la seule information à laquelle nous avons accès est la quantité de charge passant au point $M$ par unité de temps, c'est-à-dire à l'intensité $i(M, t)$ ([[#^figure3|fig. 3]]).
> L'intensité $i(M, t)$ du courant dépend en général à la fois du point $M$ et du temps. La flèche tracée sur le schéma indique l'orientation du vecteur unitaire normal à une section du fil. Ainsi, $i(M, t) > 0$ correspond à un écoulement de charges positives dans le sens de la flèche **ou** à un écoulement de charges négatives dans le sens opposé.

> [!note] Distributions de courants : Courants filiformes : Cas du régime statique ou indépendant du temps
> Considérons le fil représenté sur la [[#^figure3|figure 3]]. Pendant la durée élémentaire $dt$ la variation élémentaire de la charge électrique $q_{12}$ comprise entre $M_1$ et $M_2$ est : $dq_{12} = \delta q_{entrant\, en\, M_1} - \delta q_{sortant\, en\, M_2} = i(M_1)dt - i(M_2)dt$ soit : $\dfrac{dq_{12}}{dt} = i(M_1) - i(M_2)$
> En régime permanent, toutes les grandeurs sont constantes, et en particulier $q_{12}$, donc : $\dfrac{dq_{12}}{dt} = 0$ soit : $i(M_1) = i(M_2)$.
> ==**En régime permanent, l'intensité d'un courant filiforme a la même valeur en tout point d'un fil sans dérivation.**==
> Imaginons maintenant un fil $AB$ non fermé. La charge ne pouvant s'accumuler ni en $A$ ni en $B$, nous pouvons affirmer : $i(A) = i(B) = 0$.
> Comme, en régime permanent, le courant est uniforme dans le fil, ce courant est nul partout. Nous pouvons donc affirmer que :
> ==**En régime permanent, un courant filiforme ne peut exister que sur un circuit fermé.**==
> *Le modèle de courant filiforme ne donne aucun renseignement sur la façon dont les mouvements de charges se répartissent à l'intérieur du fil. Il peut être nécessaire de disposer d'une description plus fine : c'est le modèle du courant volumique.*
> *Par ailleurs, il arrive que les fils d'un circuit soient jointifs et se répartissent sur une surface (fils d'un bobinage de solénoïde, par exemple). Les effets de ces courants seront plus faciles à étudier en modélisant le circuit par une nappe de courants surfaciques.*
> *Les deux paragraphes qui suivent introduisent des notions qui, bien que n'étant pas au programme de première année, éclairent la notion de courant électrique.*

> [!note] Distributions de courants : Courants volumiques : Vecteur densité volumique de courants
> Considérons un ensemble de particules de charges $q$, de densité particulaire $n$ et ayant un mouvement d'ensemble à vitesse $\overrightarrow{v}$.
> Nous appellerons *densité volumique de charges mobiles* la quantité : $\rho_m = nq$.
> *Remarque : $\rho_m = nq$ désigne la densité volumique de charges mobiles (en $C\, . m^{-3}$), à ne pas confondre avec $\rho$, densité totale de charges, qui prend également en compte les charges qualifiées de fixes (par exemple les ions formant le réseau cristallin dans un conducteur métallique).*
> ==**Le vecteur densité volumique de courant associé à un mouvement d'ensemble à vitesse $\overrightarrow{v}$ est : $\overrightarrow{j} = nq\overrightarrow{v} = \rho_m\overrightarrow{v}$.**==
> ==**Ce vecteur, dont la valeur s'exprime en $A\, . m^{-2}$, est par construction une grandeur nivelée.**==
> Pour un tel mouvement, la charge mobile $\delta Q_m$ traversant entre les instants $t$ et $t + \delta t$ la surface élémentaire $d\overrightarrow{S}$, représentée sur la [[#^figure4|figure 4]], est contenue à la date $t$ dans le cylindre oblique de hauteur $v\delta t$ et de volume $d\tau = \overrightarrow{v}\,\,\delta t\, . d\overrightarrow{S}$. Par conséquent : $\delta Q_m = nqd\tau = nq\,\overrightarrow{v}\,\,\delta t\,d\overrightarrow{S}$.
> L'intensité $dI$ traversant l'élément de surface $d\overrightarrow{S}$ est : $dI = nq\,\overrightarrow{v}\,.d\overrightarrow{S} = \overrightarrow{j}\,.d\overrightarrow{S}$.
> ==**L'intensité du courant électrique traversant une surface $S$ est égale au flux du vecteur densité volumique de courants $\overrightarrow{j}(\overrightarrow{r}, t)$ à travers cette surface : $\displaystyle I(S, t) = \iint_S\overrightarrow{j}\,(\overrightarrow{r}, t)\,.d\overrightarrow{S}$.**==
> Lorsqu'il existe différents types de porteurs de charges (électrolyte par exemple), les contributions au courant électrique de chaque type, indicé $\alpha$, s'ajoutent. Le vecteur densité résultant est alors : $\displaystyle\overrightarrow{j} = \sum_{\alpha}\overrightarrow{j}_{\alpha} = \sum_{\alpha}n_{\alpha}q_{\alpha}\overrightarrow{v}_{\alpha}$.

> [!note] Distributions de courants : Courants volumiques
> - Lignes et tubes de courant :
> ==**Une ligne de courant est une ligne en tout point de laquelle le vecteur densité volumique de courant est tangent.**==
> ==**Un tube de courant est un ensemble de lignes de courant s'appuyant sur un contour $C$ ([[#^figure5|fig. 5]]).**==
> - Flux conservatif de $\overrightarrow{j}$ en régime permanent statique :
> En régime permanent, la charge contenue à l'intérieur d'une surface fermée $S$ (fixe) n'évolue pas. L'intensité traversant cette surface est donc nulle, c'est-à-dire que le flux sortant de $\overrightarrow{j}$ à travers $S$ est nul.
> Appliquons ce résultat à une surface fermée obtenue par la réunion de deux sections $S_1$ et $S_2$ d'un même tube de courant et de la surface $\Sigma$ du tube joignant ces surfaces ([[#^figure6|fig. 6]]).
> Comme il n'y a aucun mouvement de charges à travers la surface $\Sigma$ $(\overrightarrow{j}\, . \overrightarrow{n} = 0)$, l'intensité traversant la surface $S_1$ $\displaystyle\left(I_1 = \iint \overrightarrow{j}\, . d\overrightarrow{S}_1\right)$ est égale à celle traversant $S_2$ $\displaystyle\left(I_2 = \iint \overrightarrow{j}\, . d\overrightarrow{S}_2\right)$.
> ==**En régime permanent statique (indépendant du temps), le vecteur $\overrightarrow{j}$ a un flux conservatif : le courant électrique est le même à travers toutes les sections d'un même tube de courant.**==

> [!note] Distributions de courants : Courants surfaciques
> - Vecteur densité surfacique de courants :
> Lorsque la distribution de courants se trouve confinée dans une écorce d'épaisseur $h$ faible à l'échelle macroscopique, nous pouvons assimiler celle-ci à une distribution surfacique de courants.
> Considérons une section élémentaire $dS = h\,dl$ ([[#^figure7|fig. 7]]) de l'écorce, orientée selon le vecteur unitaire $\overrightarrow{u}$, $d\overrightarrow{S} = dS\,.\overrightarrow{u}$. Pour $h$ faible, le vecteur $\overrightarrow{j}$ est dans le plan tangent à la nappe et le courant traversant $dS$ est $dI = \overrightarrow{j}\, . d\overrightarrow{S} =  \overrightarrow{j}\, h\,\overrightarrow{u}\, dl$.
> Pour une épaisseur $h$ très faible, nous envisagerons la représentation limite « $h$ tend vers zéro » à courant $dI$ constant pour un élément de longueur $dl$ donné. Le produit $\overrightarrow{j}\,. h$, maintenu constant lors de cette opération, sera noté $\overrightarrow{j}_S$, *vecteur densité surfacique de courants*. Sa norme se mesure en $A\, . m^{-1}$.
> ==**Lorsque les courants circulent sur des nappes surfaciques, le vecteur densité surfacique de courants $\overrightarrow{j}_S$ associé est défini par : $dI = \overrightarrow{j}_S\,.\overrightarrow{u}\, dl$, $dI$ étant l'intensité traversant l'élément de longueur $dl$ tracé sur la surface. Le vecteur $\overrightarrow{j}_S$, dont la valeur s'exprime en $A\, . m^{-1}$, est par construction une grandeur nivelée.**==
> - Densité surfacique de courant associée à une distribution de courants filiformes en surface :
> Considérons le circuit filiforme hélicoïdal d'un bobinage « simple couche » d'un solénoïde parcouru par un courant $I$ ([[#^figure8|fig. 8]]).
> Si les fils sont très rapprochés les uns des autres (ou jointifs) il est avantageux de modéliser ce circuit hélicoïdal par un empilement de courants circulaires placés les uns à côté des autres.
> Notons $n = \frac{1}{a}$ le nombre de circuits circulaires par unité de longueur le long de l'axe $(Oz)$. Nous pouvons encore pousser la modélisation en effectuant une opération de nivelage, substituant à l'empilement des courants circulaires, un courant surfacique de densité : $\overrightarrow{j}_S = n\,I\,\overrightarrow{e}_{\theta}$.
> Cette façon de procéder a l'avantage considérable de simplifier les calculs des grandeurs liées au circuit hélicoïdal.
> Cette situation se retrouve pour de nombreux circuits filiformes répartis en surface et leur modélisation par une distribution de courants surfacique apporte souvent une grande commodité de calcul.

> [!note] Symétries des distributions de courants : Symétries usuelles
> Nous allons étudier l'influence d'opérations simples (déplacements) sur une distribution de courants $\mathcal{D}$, comme nous l'avions fait pour les distributions de charges vues en électrostatique.
> ==**Les distributions de courants peuvent présenter des symétries remarquables. Les symétries élémentaires sont les symétries et les antisymétries planes, l'invariance par translation selon un axe et l'invariance par rotation autour d'un axe.**==
> - Symétrie plane :
> Nous considérons une distribution de courants telle que le plan $(xOy)$ noté $\Pi$, soit un plan de symétrie (ou plan-miroir) de la distribution.
> Notons $M'(x, y, -z)$ le symétrique du point $M(x, y, z)$ par rapport au plan $\Pi$.
> 	- Courants filiformes ([[#^figure9|fig. 9]]) :
> 	La distribution de courants filiformes est invariante par symétrie par rapport au plan $\Pi$ si les circuits **orientés** sont inchangés par cette symétrie et si l'intensité en $M$ est égale à l'intensité en $M'$.
> 	- Courants volumiques ([[#^figure10|fig. 10]]) :
> 	La distribution de courants volumiques est invariante par symétrie par rapport au plan $\Pi$ si les densités de courant $\overrightarrow{j}$ et $\overrightarrow{j'}$ en $M$ et $M'$ sont symétriques l'une de l'autre par rapport au plan $\Pi$, soit ici : $j_{x}^{'} = j_{x}$ ; $j_{y}^{'} = j_{y}$ ; $j_{z}^{'} = -j_{z}$.
> - Antisymétrie plane :
> Nous considérons maintenant une distribution de courants telle que le plan $(xOy)$, noté $\Pi^{*}$ soit un plan d'antisymétrie (ou plan anti-miroir) de la distribution.
> Notons $M'(x, y, -z)$ le symétrique du point $M(x, y, z)$ par rapport au plan $\Pi^{*}$.
> 	- Courants filiformes :
> 	Le plan $\Pi^{*}$ est plan d'antisymétrie pour la distribution de courants filiformes ([[#^figure11|fig. 11]]) si lors d'une symétrie par rapport à $\Pi^{*}$ :
> 		- les circuits **non orientés** sont inchangés,
> 		- l'orientation des circuits change de sens,
> 		- l'intensité en $M$ est égale à l'intensité en $M'$.
> 	- Courants volumiques :
> 	Notons encore $\overrightarrow{j}$ et $\overrightarrow{j'}$ les vecteurs densité de courant en $M$ et $M'$. Le plan $\Pi^{*}$ est plan d'antisymétrie pour la distribution de courants volumiques ([[#^figure12|fig. 12]]) si $\overrightarrow{j'}$ est égal à l'opposé du symétrique de $\overrightarrow{j}$ par rapport à $\Pi^{*}$, soit ici : $j_{x}^{'} = -j_{x}$ ; $j_{y}^{'} = -j_{y}$ ; $j_{z}^{'} = j_{z}$.

> [!note] Symétries des distributions de courants : Symétries usuelles : Invariance par translation
> Une distribution est invariante par translation parallèlement à un axe $\Delta$ lorsque le courant en $M$ est identique au courant en tout point $M'$ obtenu par une translation de $M$ parallèlement à cet axe. Il est nécessaire pour cela que la distribution soit illimitée dans la direction de l'axe $\Delta$.
> - Courants volumiques :
> Une distribution est invariante par translation le long de l'axe $(Oz)$ si le vecteur densité de courant $\overrightarrow{j}$ ne dépend pas de la coordonnée $z$ : $\overrightarrow{j}(x, y, z) = \overrightarrow{j}(x, y)$.
> - Courants filiformes :
> Envisageons deux cas particuliers :
> 	- Courant parallèles à l'axe $\Delta$ ([[#^figure13|fig. 13]]) :
> 	Une distribution de courants portés par un ensemble de fils rectilignes infiniment longs et parallèles à l'axe $\Delta$ est invariante par translation ([[#^figure13|fig. 13]]). Rigoureusement, une telle distribution est impossible car incompatible avec la nécessité de fermer les circuits. En revanche, il peut s'agir d'une excellente approximation dans un domaine limité de l'espace, à proximité des fils.
> 	Notons que tout plan orthogonal à $\Delta$ est un plan anti-miroir pour cette distribution.
> 	- Courants dans un plan orthogonal à $\Delta$ :
> 	Considérons le système de spires filiformes identiques et régulièrement espacées représenté sur la [[#^figure14|figure 14]]. Au sens strict, cette distribution n'est pas invariante par translation le long de $\Delta$. Mais si les fils sont fins et très proches les uns des autres, un observateur un peu éloigné peut considérer qu'il s'agit d'une nappe continue, invariante par translation.
> 	Notons que tout plan orthogonal à $\Delta$ est plan-miroir pour cette distribution.

> [!note] Symétries des distributions de courants : Symétries usuelles : Invariance par rotation
> - Courants volumiques :
> Pour une distribution de courants invariante par rotation autour de l'axe $(Oz)$ ([[#^figure15|fig. 15]]), les coordonnées de $\overrightarrow{j}$, dans la base locale $(\overrightarrow{e}_r, \overrightarrow{e}_{\theta}, \overrightarrow{e}_z)$ des coordonnées cylindriques d'axe $(Oz)$, sont indépendantes de l'angle $\theta$ : $\overrightarrow{j}(r, \theta, z) = j_r(r, z)\overrightarrow{e}_r + j_{\theta}(r, z)\overrightarrow{e}_{\theta} + j_z(r, z)\overrightarrow{e}_z$.
> Notons que pour une distribution de courants invariante par rotation, le passage de $\overrightarrow{j}(M)$ à $\overrightarrow{j'}(M')$ s'obtient par une rotation.
> - Courants filiformes :
> Pratiquement, nous trouvons deux cas de distributions filiformes invariantes par rotation :
> 	- Ensemble de spires circulaires d'axe $(Oz)$ ([[#^figure16|fig. 16]]) :
> 	Notons que dans ce cas, tout plan contenant l'axe $(Oz)$ est un plan anti-miroir de la distribution de courant : $I(r, \theta, z) = I(r, z)$.
> 	- Fil confondu avec l'axe $(Oz)$ :
> 	Dans ce cas, tout plan contenant l'axe $(Oz)$ est plan-miroir

> [!note] Symétries des distributions de courants : Distributions à symétries multiples
> Les distributions que nous rencontrerons seront fréquemment invariantes vis-à-vis de plusieurs symétries élémentaires. Les cas particuliers de distributions invariantes par translation ou par rotation présentés possédaient ainsi déjà des plans-miroirs ou anti-miroirs.
> - Symétrie cylindrique :
> Une distribution à symétrie cylindrique est invariante par translation parallèlement à un axe $(Oz)$ et invariante par rotation autour de cet axe.
> La densité de courants doit donc être de la forme : $\overrightarrow{j}(r, \theta, z) = j_r(r)\overrightarrow{e}_r + j_{\theta}(r)\overrightarrow{e}_{\theta} + j_z(r)\overrightarrow{e}_z$.
> Nous pourrons rencontrer les cas suivants :
> 	- courants plans et annulaires d'axe $(Oz)$ : $\overrightarrow{j} = j_{\theta}(r)\overrightarrow{e}_{\theta}$.
> 	Pour ces courants, tout plan perpendiculaire à $(Oz)$ est un plan de symétrie des courants et tout plan contenant $(Oz)$ est un plan d'antisymétrie ([[#^figure17|fig. 17]]).
> 	C'est le cas des courants solénoïdaux ou sur des spires ([[#^figure18|fig. 18]]).
> 	- courants de direction $(Oz)$ : $\overrightarrow{j} = j_{z}(r)\overrightarrow{e}_{z}$.
> 	Pour ces courants, tout plan perpendiculaire à $(Oz)$ est un plan d'antisymétrie des courants et tout plan contenant $(Oz)$ est un plan de symétrie ([[#^figure19|fig. 19]]). C'est le cas des courants filiformes sur un fil infini ;
> 	- courants radiaux : $\overrightarrow{j} = j_{r}(r)\overrightarrow{e}_{r}$.
> 	Pour ces courants, tout plan perpendiculaire à $(Oz)$ et tout plan contenant $(Oz)$ sont des plans de symétrie des courants.
> 	Les deux répartitions de courants précédentes sont à flux conservatif, quelle que soit la fonction de $r$. En régime permanent, sans accumulateur de charges, la conservation de la charge impose que l'intensité $I$ soit la même à travers tout cylindre de rayon $r$, de hauteur $h$ et d'axe $(Oz)$. Ainsi, pour les courants radiaux : $2\pi rhj_r(r) = I$ ou encore $\overrightarrow{j} = \frac{k}{r}\overrightarrow{e}_{r}$.
> 	C'est le cas des courants radiaux existant dans une diode à vide à symétrie cylindrique dont la cathode est confondue avec l'axe $(Oz)$ ([[#^figure20|fig. 20]]).

> [!note] Symétries des distributions de courants : Distributions à symétries multiples : Symétrie sphérique
> La distribution est invariante par rotation autour de tous les axes passant par le centre de symétrie. Elle l'est aussi par rapport à tout plan contenant ce même point. En utilisant les coordonnées sphériques $r$, $\theta$ et $\varphi$ avec origine au point centre de symétrie, nous avons ([[#^figure21|fig. 21]]) : $\overrightarrow{j}(r, \theta, \varphi) = j(r)\overrightarrow{e}_r$.
> En régime permanent, sans accumulation de charges, la conservation de la charge électrique impose que l'intensité $I$ soit la même à travers toute sphère de centre $O$, soit : $4\pi r^{2}j(r) = cte = I$.
> Ceci impose l'existence d'une source de charges au point $O$ et d'intensité $I$, par exemple sous la forme de courant d'amenée filiforme.
# Définitions
==**Courant électrique**== :
Étant donné un référentiel $\mathcal{R}$, on appelle *courant électrique* tout mouvement d'ensemble (mouvement ordonné) de particules chargées dans ce référentiel.

> [!note] Conservation de la charge électrique
> - Cas d'un système fermé : 
> Un système fermé est un système qui n'échange pas de matière avec le milieu qui l'entoure.
> Pour un tel système, l'expérience montre que la charge reste constante.
> - Cas d'un système ouvert :
> Un système ouvert peut échanger de la matière avec le milieu qui l'entoure. Il est donc susceptible de recevoir ou de céder des charges électriques.
> Considérons un tel système occupant un volume $V$. La conservation de la charge électrique impose que l'évolution de la charge contenue dans $V$ soit due uniquement aux transferts de charges entre le système et l'extérieur, donc qu'elle soit liée aux courants électriques entrant ou sortant à travers la surface fermée $S$ délimitant son volume $V$.
> Pour le cas représenté sur la [[#^figure2|figure 2]], en notant $Q_V$ la charge contenue dans le volume $V$, la conservation de la charge se traduit par : $\delta Q_V = (I_1 + I_2 + I_3 - I_4)\delta t$.

> [!note] Divers courants électriques
> - Les courants de conduction :
> Ils sont associés au *déplacement d'ensemble* d'électrons dans les métaux, d'ions dans les solutions d'électrolytes, d'électrons ou de lacunes électroniques (« trous ») dans les semi-conducteurs.
> Pour un conducteur métallique fixe dans le référentiel d'étude $\mathcal{R}$, ce sont les électrons dits de conduction qui autorisent l'existence d'un courant électrique.
> Leur densité particulaire $n_e$ (nombre par unité de volume) est élevée, de l'ordre de $10^{29}\, m^{-3}$. Un volume mésoscopique $d\tau$, bien que macroscopiquement très petit, contient un nombre $n_e d\tau$ important d'électrons de conduction.
> Les électrons de conduction, indicés $k$, sont animés de vitesses $\overrightarrow{V_k}$. Pour le volume $d\tau$, nous définirons la *vitesse d'ensemble* des porteurs par $\displaystyle\overrightarrow{v} = \frac{1}{n_e d\tau}\sum_k\overrightarrow{V_k}$. Cette vitesse est une *grandeur nivelée*, ou *valeur moyenne spatiale*.
> Les vitesses $\overrightarrow{V_k}$, de l'ordre de $10^{6}\, m \,. s^{-1}$, résultent d'une agitation désordonnée à laquelle se superpose un mouvement d'ensemble à vitesse $\overrightarrow{v}$ (dû par exemple à l'application d'un champ électrique au conducteur). Leur valeur est sans commune mesure avec l'ordre de grandeur de la vitesse d'ensemble des électrons de conduction. Leur partie aléatoire $\overrightarrow{V_k} - \overrightarrow{v}$ évolue très rapidement aux échelles de temps $T$ caractérisant les expériences usuelles :
> ==**Le courant électrique de conduction résulte d'un mouvement d'ensemble (ou de dérive) des porteurs de charges dans un support matériel fixe.**==
> - Les courants de convection :
> *De tels courants sont obtenus par déplacement dans un référentiel donné d'un support matériel portant des charges*. C'est le cas d'un disque chargé qui tourne autour de son axe, mouvement donnant naissance à des courants annulaires (ou orthoradiaux).
> - Les courants particulaires :
> À un faisceau de particules chargées (électrons ou ions dans les tubes à vide) est associé un courant électrique dit particulaire.
# Diagrammes
Surface $S$ orientée par un vecteur unitaire $\overrightarrow{n}$
![[electromagnetisme1/attachments-electromagnetisme1/figure74.png]]^figure1

L'évolution $\delta Q_V$ de la charge contenue dans le volume $V$ pendant le temps $\delta t$ est égale à : $\delta Q_V = (I_1 + I_2 + I_3 - I_4)\delta t$
![[electromagnetisme1/attachments-electromagnetisme1/figure75.png]]^figure2

Courant filiforme
![[electromagnetisme1/attachments-electromagnetisme1/figure76.png]]^figure3

Les particules qui traversent la surface $dS$ pendant le temps $\delta t$ sont situées dans un cylindre de base $dS$ et de génératrice $\overrightarrow{v}\,\,\delta t$
![[electromagnetisme1/attachments-electromagnetisme1/figure77.png]]^figure4

Lignes et tube de courant s'appuyant sur un contour $C$
![[electromagnetisme1/attachments-electromagnetisme1/figure78.png]]^figure5

Tube de courant
![[electromagnetisme1/attachments-electromagnetisme1/figure79.png]]^figure6

Écorce orientée pour $h$ faible
![[electromagnetisme1/attachments-electromagnetisme1/figure80.png]]
$h$ très faible
![[electromagnetisme1/attachments-electromagnetisme1/figure81.png]]^figure7

Solénoïde « simple couche »
![[electromagnetisme1/attachments-electromagnetisme1/figure82.png]]^figure8

Les courants circulant dans $\mathcal{C}_1$, $\mathcal{C}_{1}^{'}$, $\mathcal{C}_2$ et $\mathcal{C}_{2}^{'}$ forment une distribution invariante par symétrie par rapport au plan $\Pi$
![[electromagnetisme1/attachments-electromagnetisme1/figure83.png]]^figure9

Symétrie plane
![[electromagnetisme1/attachments-electromagnetisme1/figure84.png]]^figure10

Les courants circulant dans $\mathcal{C}_1$, $\mathcal{C}_{1}^{'}$, $\mathcal{C}_2$ et $\mathcal{C}_{2}^{'}$ forment une distribution pour laquelle $\Pi^{*}$ est un plan d'antisymétrie
![[electromagnetisme1/attachments-electromagnetisme1/figure85.png]]^figure11

$\Pi^{*}$ est un plan d'antisymétrie pour la distribution de courants
![[electromagnetisme1/attachments-electromagnetisme1/figure86.png]]^figure12

Distribution de courants filiformes invariante par translation parallèlement à $\Delta$. $\Pi^{*}$ est un plan anti-miroir
![[electromagnetisme1/attachments-electromagnetisme1/figure88.png]]^figure13

Distribution invariante par translation dans le cas limite où les fils sont très serrés. ($\Pi$) est un plan miroir
![[electromagnetisme1/attachments-electromagnetisme1/figure89.png]]^figure14

Invariance par rotation autour de $(Oz)$
![[electromagnetisme1/attachments-electromagnetisme1/figure90.png]]^figure15

Distribution de courants filiformes invariante par rotation d'axe $(Oz)$
![[electromagnetisme1/attachments-electromagnetisme1/figure91.png]]^figure16

Distribution de courants annulaires
![[electromagnetisme1/attachments-electromagnetisme1/figure92.png]]^figure17

Courants solénoïdaux, ou sur des spires
![[electromagnetisme1/attachments-electromagnetisme1/figure93.png]]^figure18

Courant filiforme sur un fil infini
![[electromagnetisme1/attachments-electromagnetisme1/figure94.png]]^figure19

Courants à symétrie cylindrique
![[electromagnetisme1/attachments-electromagnetisme1/figure95.png]]^figure20

Courants à symétrie sphérique
![[electromagnetisme1/attachments-electromagnetisme1/figure96.png]]^figure21
# Graphiques

# Expériences

# Autres notes
> [!warning] Application 2 page 108
> ![[electromagnetisme1/attachments-electromagnetisme1/figure87.png]]
> Les documents 11 et 13 sont respectivement les figures [[#^figure10|10]] et [[#^figure12|12]].

> [!warning] Application 3 page 111
> ![[electromagnetisme1/attachments-electromagnetisme1/figure97.png]]