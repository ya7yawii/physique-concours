---
titre: "[[10-La force de Lorentz]]"
tags:
aliases:
crée: 12-01-2026, 11:13
---
# Formules
> [!note] L'interaction électromagnétique : La force de Lorentz : Formulation
> C’est Lorentz qui, le premier, a décrit la force électromagnétique $\overrightarrow{F}$ agissant sur une particule chargée.
> ==**La force électromagnétique subie par une particule de charge $q$ et de masse $m$, se trouvant, à la date $t$, au point $M$ du référentiel galiléen $\mathcal{R}$, en présence d’un champ électrique $\overrightarrow{E}(M, t)$ et d’un champ magnétique $\overrightarrow{B}(M, t)$, et se déplaçant à la vitesse $\overrightarrow{v}(M, t)_{\!/\mathcal{R}}$  est donnée par : $\overrightarrow{F}_{Lo} = q[\overrightarrow{E}(M, t) + \overrightarrow{v}(M, t)_{\!/\mathcal{R}}\wedge\overrightarrow{B}(M, t)]$.**==
> ==**Dans le cas de champs permanents et indépendants du temps nous avons : $\overrightarrow{F}_{Lo} = q(\overrightarrow{E} + \overrightarrow{v}\wedge\overrightarrow{B})$.**==
> Cette force de Lorentz traduit l’une des interactions fondamentales de la physique ; son domaine de validité n’est pas limité dans le cadre de nos connaissances actuelles.
> Les champs $\overrightarrow{E}$ et $\overrightarrow{B}$ introduits ici sont créés par des sources (charges et courants) et définis relativement au référentiel $\mathcal{R}$.
> Comme toute force d’interaction, $\overrightarrow{F}_{Lo}$ ne dépend pas du référentiel alors que la vitesse en dépend. Les champs $\overrightarrow{E}$ et $\overrightarrow{B}$ peuvent donc dépendre du référentiel.
> Remarquons que les champs $\overrightarrow{E}$ et $\overrightarrow{B}$ sont de natures différentes ; le rapport $\frac{E}{B}$ est homogène à une vitesse. Dans le Système International d’unités, $E$ s’exprime en volts par mètre $(V . m^{-1})$ et $B$ en testa $(T)$.
> La charge $q$ est une propriété intrinsèque de la particule : elle est indépendante du temps et du référentiel.

> [!note] L'interaction électromagnétique : La force de Lorentz
> - Comparaison avec la force gravitationnelle :
> La comparaison des forces électrostatique et gravitationnelle a été mentionnée dans le chapitre 2, [[#^app1|Application 1]] : le rapport colossal obtenu justifie que nous négligions par la suite les forces de gravitation (et donc de pesanteur).
> - Puissance :
> La puissance de la force de Lorentz est : $\mathcal{P}_{Lo} = \overrightarrow{F}_{Lo}\,.\overrightarrow{v} = q\,\overrightarrow{E}\,.\overrightarrow{v}$.
> Elle est nulle si le champ électrique est nul.
> - Hypothèses d’étude :
> Considérons le mouvement de particules dans des champs $\overrightarrow{E}$ et (ou) $\overrightarrow{B}$ indépendants du temps (ou très exceptionnellement à variation temporelle suffisamment lente pour que l'approximation du régime quasi permanent soit applicable (cf. [[07-Champ magnétique|chapitre 7]]).
> Nous utiliserons une propriété des champs électriques indépendants du temps, à savoir l'existence d'un potentiel scalaire $V(M)$ tel que : $\overrightarrow{E} = -\overrightarrow{grad}\,V$.
> *Remarque :*
> *La plupart des expériences et des exercices étudiés ci-dessous supposent la réalisation d’un vide poussé (pression inférieure à un pascal), ce qui élimine tout frottement lors du déplacement des particules.*
> La relation fondamentale de la mécanique appliquée à une particule de masse $m$ et de charge $q$ s’écrit alors : $m\dfrac{d\overrightarrow{v}}{dt} = q(\overrightarrow{E} + \overrightarrow{v}\wedge\overrightarrow{B})$.
> La masse $m$ et la charge $q$ interviennent par leur rapport $\frac{q}{m}$. Il est donc inutile de chercher à déterminer séparément $q$ et $m$ par l’étude du mouvement.

> [!note] Mouvement d'une particule chargée dans les champs $\overrightarrow{E}$ et (ou) $\overrightarrow{B}$ : Champ $\overrightarrow{E}$ seul
> - Rôle accélérateur d’un champ électrique :
> Lorsqu’une charge $q$ se déplace dans un champ électrostatique $\overrightarrow{E} = -\overrightarrow{grad}\,V$, elle subit la force : $\overrightarrow{F} = q\overrightarrow{E} = -\overrightarrow{grad}(qV)$, qui dérive de l’énergie potentielle $\mathcal{E}_P = qV$.
> L’énergie mécanique $\mathcal{E}_M = \frac{1}{2}mv^{2} + qV$ se conserve et en deux positions $M_1$ et $M_2$ de la particule, il vient : $v^{2}(M_2) = v^{2}(M_1) + 2\frac{q}{m}(V_1 - V_2)$.
> En supposant que la particule parte d’un point $O$ de potentiel nul (potentiel de référence) avec une vitesse nulle, son énergie cinétique en un point $M$ est : $\mathcal{E}_K(M) = -qV(M)$.
> Cette particule possède une énergie cinétique exprimable naturellement en électron-volt (*symbole* : $eV$).
> Remarquons que pour un *électron* $(q = -e)$ , il faut que $V(M) > 0$ pour qu’il puisse acquérir une vitesse.
> - Mouvement dans un champ électrique $\overrightarrow{E}$ uniforme et indépendant du temps :
> Une particule passant à l’intérieur d’un condensateur plan subit une déviation proportionnelle à la différence de potentiel entre les plaques du condensateur (cf. l’[[#^app2|Application 3]]) ; ce principe est utilisé dans un oscilloscope analogique.
> Limitons-nous à rappeler succinctement la description du tube cathodique d’un oscilloscope ([[#^figure1|fig. 1]]).
> Dans le tube règne un vide poussé $(p < 10^{-4} Pa)$. Le pinceau électronique est produit par un canon à électron comportant un fil chauffé ($1000\,K$ environ) à fort pouvoir émissif en électrons, une électrode appelée wehnelt permettant de régler l’intensité du courant électronique, et des électrodes de concentration et d’accélération (lentilles électroniques).
> Les électrons traversent ensuite les plaques de déviations verticales et horizontales. Quand les électrons traversent les plaques horizontales soumises à une différence de potentiel $U_V$, ils sont déviés verticalement ; cette déviation était proportionnelle à $U_V$ (cf. l’[[#^app2|Application 3]]).
> Il en est de même pour la traversée des plaques verticales, la déviation horizontale associée étant proportionnelle à la tension $U_H$ appliquée entre ces plaques.
> Sur l’écran la trace de l’électron (spot) traduit ces déviations : $X = K_1U_H$ et $Y = K_2U_V$.
> Nous nous reporterons aux travaux pratiques pour l’utilisation de cette propriété.

> [!note] Mouvement d'une particule chargée dans les champs $\overrightarrow{E}$ et (ou) $\overrightarrow{B}$ : Champ $\overrightarrow{B}$ seul : Propriétés du mouvement dans un champ $\overrightarrow{B}$ stationnaire
> Un électron mobile dans un champ magnétique $\overrightarrow{B}$ indépendant du temps (stationnaire) est uniquement soumis à la force magnétique $\overrightarrow{F} = q\overrightarrow{v}\wedge\overrightarrow{B}$ (souvent appelée également force de Lorentz).
> La puissance de cette force est nulle, car : $\overrightarrow{F}\, . \overrightarrow{v} = (q\overrightarrow{v}\wedge\overrightarrow{B}) . \overrightarrow{v} = 0$, (produit mixte avec deux vecteurs colinéaires).
> Le travail de la force magnétique $\overrightarrow{F} = q\overrightarrow{v}\wedge\overrightarrow{B}$ qui s’exerce sur une particule est nul.
> L’énergie cinétique de cette particule est constante (théorème de la puissance cinétique). La norme de sa vitesse au cours du mouvement est constante : $\dfrac{d\mathcal{E}_K}{dt} = \overrightarrow{F}\, . \overrightarrow{v} = 0$, donc $\mathcal{E}_K = cte$ et $v = cte$.
> *Remarques :*
> - *Si $\overrightarrow{B}$ dépend du temps selon $\overrightarrow{B} = \overrightarrow{B}(M, t)$, la force magnétique ne travaille toujours pas, mais il apparaît (phénomène d’induction) un champ électrique dont la puissance est en général non nulle. Une telle situation est exclue de nos hypothèses d’étude.*
> - *La puissance de la force magnétique est nulle mais ses effets ne le sont pas ; la force magnétique dévie les particules chargées en mouvement et cela d'autant fortement que leur vitesse est élevée.*

> [!note] Mouvement d'une particule chargée dans les champs $\overrightarrow{E}$ et (ou) $\overrightarrow{B}$ : Champ $\overrightarrow{B}$ seul : Mouvement dans un champ $\overrightarrow{B}$ uniforme et indépendant du temps
> - Cas général d’une vitesse initiale quelconque :
> Étudions le mouvement d’une particule $(q, m)$ placée à l’origine $O$ du trièdre trirectangulaire $(O ; x, y, z)$ à l’instant initial $t = 0$ (vitesse initiale $\overrightarrow{v}_0$) dans un champ magnétostatique $\overrightarrow{B} = B\,\overrightarrow{e}_z$ $(B > 0)$ uniforme dans un domaine donné ([[#^figure2|fig. 2]]).
> Posons $\overrightarrow{v}_0 = v_0(\sin\alpha\, . \overrightarrow{e}_x + \cos\alpha\, . \overrightarrow{e}_z)$.
> La relation fondamentale de la dynamique appliquée au point matériel donne : $m\dfrac{d\overrightarrow{v}}{dt} = q\,\overrightarrow{v}\wedge B\,\overrightarrow{e}_z$.
> Posons $q = \epsilon e$ ($\epsilon = +1$ pour un proton, et $\epsilon = -1$ pour un électron).
> Introduisons la grandeur $\omega_c = \frac{eB}{m}$ homogène à l’inverse d’un temps et que nous appellerons **pulsation cyclotron**.
> Nous obtenons : $\dfrac{dv_x}{dt} = \epsilon\omega_cv_y$, $\dfrac{dv_y}{dt} = -\epsilon\omega_cv_x$ et $\dfrac{dv_z}{dt} = 0$.
> 	- Mouvement projeté sur le plan $(xOy)$ :
> 	En intégrant les deux premières équations par rapport au temps, nous obtenons : $v_x = \epsilon\omega_cy + v_0\sin\alpha$ et $v_y = -\epsilon\omega_cx$. Il est possible de reporter $v_x$ et $v_y$ dans les équations précédentes et d’intégrer à nouveau, mais il est aussi efficace d’introduire la variable $\xi = x + i y$ qui représente *l’affixe* de la projection orthogonale du vecteur $\overrightarrow{OM}$ (vecteur position de la particule) dans le plan $(xOy)$.
> 	Comme $\dfrac{d\xi}{dt} = v_x + i v_y$, nous avons $\dfrac{d\xi}{dt} = -\epsilon i \omega_c\xi + v_0\sin\alpha$, dont la solution est : $\xi = -i\frac{\epsilon v_0}{\omega_c}\sin\alpha + A\exp(-i\epsilon\omega_ct)$.
> 	À $t = 0$, $\xi = 0$, donc $A = i\frac{\epsilon v_0}{\omega_c}\sin\alpha$ et $\xi = i\frac{\epsilon v_0}{\omega_c}\sin\alpha[\exp(-i\epsilon\omega_ct) - 1]$.
> 	Les lois horaires sont donc : $x(t) = -\frac{\epsilon v_0}{\omega_c}\sin\alpha\sin(-\epsilon\omega_ct)$ et $y(t) = -\frac{\epsilon v_0}{\omega_c}\sin\alpha[1 - \cos(-\epsilon\omega_ct)]$.
> 	$x$ et $y$ vérifient $x^{2} + \left(\frac{\epsilon v_0}{\omega_c}\sin\alpha + y\right)^{2} = \left(\frac{v_0}{\omega_c}\sin\alpha\right)^{2}$ : le mouvement projeté dans le plan $(xOy)$ est un cercle de centre $C$ ($x_C = 0$ et $y_C = -\frac{\epsilon v_0}{\omega_c}\sin\alpha$) et de rayon $\rho = \frac{v_0}{\omega_c}\sin\alpha$ ([[#^figure3|fig. 3a]]). Ce cercle est décrit avec la vitesse angulaire $-\epsilon\omega_c$ égale en valeur absolue à la pulsation cyclotron.
> 	- Mouvement suivant $(Oz)$ :
> 	La troisième équation fournit : $v_z = cte = v_0\cos\alpha$, soit $z = v_0\cos\alpha t$ (mouvement uniforme parallèlement à $(Oz)$). La particule décrit donc une hélice circulaire ([[#^figure4|fig. 4]]).
> 	*Remarque : Le pas de l'hélice ([[#^figure3|fig. 3b et c]]) est $h = v_0\cos\alpha T$, où $T = \frac{2\pi}{\omega_c} = 2\pi\frac{m}{eB}$, donc : $h = 2\pi\frac{mv_0}{eB}\cos\alpha$.*
> - Le cas particulier d’une vitesse initiale normale au champ magnétique :
> Si la vitesse initiale $\overrightarrow{v}_0$ de la particule est normale au champ magnétique $\overrightarrow{B}$, $\left(\alpha = \frac{\pi}{2}\right)$, cette particule décrit une trajectoire circulaire dans un plan orthogonal à $\overrightarrow{B}$, et contenant $\overrightarrow{v}_0$.
> 

> [!note] Mouvement d'une particule chargée dans les champs $\overrightarrow{E}$ et (ou) $\overrightarrow{B}$ : Actions simultanées des champs $\overrightarrow{E}$ et $\overrightarrow{B}$
> Qualitativement, nous pouvons prévoir pour des champs uniformes $\overrightarrow{E}$ et $\overrightarrow{B}$ appliqués les propriétés suivantes.
> - Cas de champs parallèles :
> Si $\overrightarrow{E}$ et $\overrightarrow{B}$ sont parallèles, le projeté de la trajectoire sur un plan orthogonal aux champs est toujours un cercle. En revanche, la composante de la vitesse parallèle aux champs est accélérée. La vitesse n’est pas constante et la trajectoire n’est pas une hélice de pas constant.
> - Cas de champs $\overrightarrow{E}$ et $\overrightarrow{B}$ croisés :
> Si $\overrightarrow{E}$ et $\overrightarrow{B}$ sont croisés, le champ magnétique a pour effet d’incurver la trajectoire. Les exemples suivants montre qu’il en résulte une dérive, c’est-à-dire un mouvement « moyen » dont la vitesse est normale à $\overrightarrow{E}$ et à $\overrightarrow{B}$.
> 	- Cas d’une vitesse initiale nulle : voir l'[[#^app3|Application 5]].
> 	- Vitesse initiale quelconque :
> 	Une étude complète montre la généralité de cette vitesse de dérive $\overrightarrow{v_D} = \frac{\overrightarrow{E}\wedge\overrightarrow{B}}{B^{2}}$. En posant $\overrightarrow{v}' = \overrightarrow{v} - \overrightarrow{v}_D$, nous obtenons l’équation d’évolution : $m\dfrac{d\overrightarrow{v'}}{dt} = q\,\overrightarrow{v'}\wedge\overrightarrow{B}$. La trajectoire est circulaire dans le repère $(\mathcal{R}')$ en translation à la vitesse $\overrightarrow{v}_D$ dans $(\mathcal{R})$ contenant les champs $\overrightarrow{E}$ et $\overrightarrow{B}$.
> 	==**Une particule placée dans des champs $\overrightarrow{E}$ et $\overrightarrow{B}$ croisés, uniformes, et indépendants du temps, subit une vitesse de dérive : $\displaystyle\overrightarrow{v_D} = \frac{\overrightarrow{E}\wedge\overrightarrow{B}}{B^{2}}$.**==
> 	- Mesure de $\frac{e}{m}$ avec $\overrightarrow{E}$ et $\overrightarrow{B}$ croisés : Voir l'[[#^app4|Application 6]].

> [!note] Applications diverses
> - Notions sur les spectrographes de masse :
> Les propriétés des mouvements des particules (après ionisation) dans des champs $\overrightarrow{E}$ et $\overrightarrow{B}$ sont utilisées pour mettre en évidence la présence d’isotopes dans un échantillon. Étudions le principe d’un spectrographe destiné à trier les isotopes selon leur masse.
> 	- Le spectrographe de Bainbridge : voir l'[[#^app5|Application 7]].
> - Un accélérateur de particule : le cyclotron :
> Le premier cyclotron, réalisé par Lawrence, accélérait des électrons. Actuellement, les cyclotrons sont utilisés essentiellement pour l’accélération d’ions.
> Nous nous limiterons à une description élémentaire de l’appareil ([[#^figure5|fig. 5]]) ; l’étude exhaustive des accélérateurs sortant du cadre de cet ouvrage.
> 	- Description :
> 	Un cyclotron accélérant des ions (des protons par exemple) comprend essentiellement un cylindre d’axe $(Oz)$ placé dans l’entrefer d’un électro-aimant, où règne un vide poussé. Un champ magnétique $\overrightarrow{B} = B\overrightarrow{e}_z$ uniforme est appliqué sur tout le domaine du cylindre de rayon $R$. Les parois de ce cylindre sont matérialisées par deux électrodes conductrices creuses, appelées *dees*, séparées par une région de faible épaisseur $d$, s’étendant de part et d’autre d’un plan contenant l’axe du cylindre. Une source (non décrite ici) permet d’injecter les ions au centre avec une énergie cinétique négligeable.
> 	Un générateur applique entre les électrodes métalliques (*dees*) une tension sinusoïdale de fréquence $\nu$, créant ainsi entre les *dees* un champ électrique uniforme $\overrightarrow{E}$ variant sinusoïdalement à la fréquence $\nu$ : $E = E_m\cos(2\pi\nu t) = \frac{U}{d}\cos(2\pi\nu t)$.
> 	À l’intérieur de chaque *dee*, le champ électrique est considéré comme nul. Admettons que les ions sont accélérés une première fois par un champ électrique $E_m$ sur la distance $d$ avant de pénétrer dans le premier *dee*.
> 	- Fonctionnement optimal :
> 	Quand un ion pénètre dans l’un des *dees* avec la vitesse $\overrightarrow{v}$ (supposé normale à $(Oz)$ et aux faces des *dees*), il y décrit une trajectoire circulaire (donc un demi-cercle) de rayon $\rho = \frac{mv}{qB}$ , avant de retraverser l’espace entre les armatures, de largeur $d$. La durée du séjour dans le *dee*, indépendante de la vitesse de la particule, est $\Delta t = \frac{T}{2} = \frac{\pi}{\omega_c}$ en posant $\omega_c = \frac{qB}{m}$ (pulsation cyclotron des ions considérés). Si cette durée est égale à la demi-période de variation du champ électrique (soit $\omega_c = 2\pi\nu$ ou $\nu = \frac{qB}{2\pi m}$), alors le champ $E = -E_m$ accélère à nouveau les ions à la sortie du dee.
> 	Ainsi, à chaque demi-tour, le champ électrique fournit le travail optimal : $W = qE_md = qU$, servant à accroître l’énergie cinétique de l’ion.
> 	Après $n$ traversées dans ces conditions, l’énergie cinétique de l’ion vaut : $\mathcal{E}_K = \frac{1}{2}mv_{n}^{2} = nqU$ et $\rho_n = \frac{mv_n}{eB}$.
> 	Les rayons $\rho_n$ augmentent donc proportionnellement à $\sqrt{n}$. Le nombre de demi-tours est limité par le rayon maximal des électrodes. Lorsque $\rho_n = R$, un déflecteur dévie les ions accélérés pour les utiliser dans une chambre d’étude (chocs, etc.).

> [!note] Les électrons de conduction d'un métal : Modèle du mouvement d’ensemble
> Un courant électrique est créé par un déplacement d’ensemble de charges dans un référentiel $\mathcal{R}$ donné. Nous nous limitons au cas du déplacement d’ensemble des électrons libres dans des métaux immobiles dans $\mathcal{R}$, réalisant ainsi un courant appelé **courant de conduction**.
> - Les électrons de conduction :
> Dans un modèle classique, les charges mobiles (ou porteurs) dans les métaux sont les électrons libres, encore appelés électrons de conduction (par opposition aux électrons de valence liés aux ions du réseau et non susceptibles de se déplacer dans tout le conducteur). Les électrons de conduction (en nombre par unité de volume très élevé), peuvent être assimilés à un gaz dans tout le conducteur. De façon plus générale, nous appellerons porteur toute charge susceptible de se déplacer dans un milieu conducteur.
> En l’absence de force appliquée, on admet que les vitesses $\overrightarrow{u}_i$ des différents électrons de conduction se distribuent de manière aléatoire de sorte que la valeur moyenne définie par $\displaystyle\overrightarrow{v} = \langle\overrightarrow{u}_i\rangle = \frac{1}{\delta N}\sum_{\delta N}\overrightarrow{u}_i$ est nulle, où $\delta N$ représente le nombre d’électrons de conduction contenus dans un élément de volume $\delta\tau$.
> Donc, en l’absence de champ électrique $\overrightarrow{E}$ appliqué (c’est-à-dire quand le conducteur est équipotentiel) il n’existe aucun courant. En revanche, quand un champ électrique est appliqué, la vitesse moyenne des porteurs, que nous appellerons vitesse d’ensemble ou vitesse de dérive, n’est plus nulle.

> [!note] Les électrons de conduction d'un métal : Modèle du mouvement d’ensemble : Vitesse d’ensemble (ou de dérive) en présence d’une force $\overrightarrow{F}$ appliquée aux porteurs
> Nous considérons un conducteur dans lequel chaque porteur est soumis à une force $\overrightarrow{F}$ (ayant pour origine, par exemple, un champ électrique). Pour simplifier, nous supposons que tous les porteurs d’un volume mésoscopique sont soumis à la même force $\overrightarrow{F}$. Appliquons le principe fondamental de la dynamique au système constitué des porteurs d’un élément de volume mésoscopique $\delta\tau$, dont le barycentre se déplace à la vitesse d’ensemble $\overrightarrow{v}$. Le nombre de porteurs de ce système est $\delta N = n\delta\tau$ ($n$ représente donc le nombre de porteurs par unité de volume) et sa masse est égale à $nm\delta\tau$. Nous obtenons donc : $nm\delta\tau\dfrac{d\overrightarrow{v}}{dt} = n\delta\tau\overrightarrow{F} + \delta\overrightarrow{f}$ où $\delta\overrightarrow{f}$ désigne une force due aux interactions entre les porteurs mobiles de ce système et le réseau immobile dans lequel ils se déplacent. Cette force s’oppose au mouvement, et nous faisons l’hypothèse qu’elle est de la forme : $\delta\overrightarrow{f} = -k\overrightarrow{v}\delta\tau$ analogue à une force de frottement visqueux pour modéliser les collisions. Nous en déduisons une équation différentielle vérifiée par $\overrightarrow{v}(t)$ : $nm\dfrac{d\overrightarrow{v}}{dt} = n\overrightarrow{F} - k\overrightarrow{v}$, que l’on peut écrire : $m\dfrac{d\overrightarrow{v}}{dt} = \overrightarrow{F} - \frac{m\overrightarrow{v}}{\tau}$, avec $\tau = \frac{nm}{k}$.
> $\tau$ (homogène à un temps) est une grandeur caractéristique du phénomène étudié : c’est le *temps de relaxation de conduction*.
> Pour interpréter simplement ce temps $\tau$, supposons que nous appliquions une force $\overrightarrow{F}$ uniforme et constante à compter de la date initiale $t = 0$. Supposons, en outre, qu’à cette date $\overrightarrow{v} = \overrightarrow{0}$, la solution de l’équation précédente serait : $\overrightarrow{v} = \frac{\overrightarrow{F}\tau}{m}\left(1 - e^{-\frac{t}{\tau}}\right)$ ;
> $\tau$ traduit donc un ordre de grandeur du temps d’instauration d’un régime permanent donnant une vitesse d’ensemble $\overrightarrow{v} = \frac{\overrightarrow{F}\tau}{m}$ proportionnelle à $\overrightarrow{F}$.
^par1

> [!note] Les électrons de conduction d'un métal : Modèle du mouvement d’ensemble : Le modèle des collisions
> Seule la mécanique quantique permet de décrire de façon réellement satisfaisante le comportement des électrons de conduction dans un métal. Nous pouvons cependant justifier l’existence de la force de « frottement » en $-k\overrightarrow{v}$ à partir d’un modèle simplifié où les porteurs sont assimilés à des particules libres qui subissent des collisions.
> - Les hypothèses du modèle :
> 	-  Les porteurs ont un mouvement désordonné (agitation thermique) et subissent des collisions sur des sites (immobiles) du réseau dans lequel ils se déplacent.
> 	- Entre deux collisions, un porteur n’est soumis qu’à la force $\overrightarrow{F}$ que nous supposons ici constante et uniforme. Si la force $\overrightarrow{F}$ est due à un champ électrique appliqué, cette hypothèse revient à admettre que nous pouvons remplacer $\overrightarrow{E}$ par sa valeur moyenne (nivelée).
> 	- La valeur moyenne de la vitesse des porteurs juste après une collision est nulle. Cela revient à considérer que, en moyenne, les vitesses après un choc ont une répartition isotrope.
> - Vitesse moyenne des porteurs :
> Étudions le mouvement d’un porteur de masse $m$ à partir d’une collision qui a lieu à la date $t = t_0$. Il a une vitesse initiale $\overrightarrow{v}_0$ dont, par hypothèse, la valeur moyenne (prise sur un grand nombre de collisions) est nulle.
> D’après la relation fondamentale de la dynamique : $m\dfrac{d\overrightarrow{v}}{dt} = \overrightarrow{F}$.
> Intégrons cette équation différentielle vectorielle : $m[\overrightarrow{v}(t) - \overrightarrow{v}_0] = -e\overrightarrow{E}(t - t_0)$ soit : $\overrightarrow{v}(t) = \overrightarrow{v}_0 + \frac{\overrightarrow{F}}{m}(t - t_0)$.
> Calculons la valeur moyenne $\langle\overrightarrow{v}\rangle$ de $\overrightarrow{v}(t)$ pour les porteurs d’un volume mésoscopique.
> $\langle\overrightarrow{v}\rangle = \langle\overrightarrow{v}_0\rangle + \frac{\overrightarrow{F}}{m}\langle t - t_0\rangle$.
> 	- Par hypothèse $\langle\overrightarrow{v}_0\rangle = \overrightarrow{0}$.
> 	- $\langle t - t_0\rangle$ représente la durée moyenne écoulée depuis le dernier choc. C’est une quantité constante dans le temps que nous notons $\tau$. Un modèle statistique simple pourrait montrer que $\tau$ représente aussi la durée moyenne entre deux collisions.
> 	
> 	Finalement, nous obtenons avec ce modèle : $\langle\overrightarrow{v}\rangle = \frac{\overrightarrow{F}\tau}{m}$.
> 	Le « gaz de porteurs » a donc, en moyenne, une vitesse de dérive $\langle\overrightarrow{v}\rangle$ qui se superpose à la [[#^info1|vitesse d’agitation thermique]] aléatoire et de valeur moyenne nulle.

> [!note] Les électrons de conduction d'un métal : Vecteur densité de courants de conduction
> Rappelons la définition du vecteur densité de courant $\overrightarrow{j}$ (cf. [[06-Distributions de courants|chapitre 6]]) :
> - ==**À un mouvement de porteurs de vitesse moyenne $\overrightarrow{v}$ non nulle on associe un vecteur densité de courant $\overrightarrow{j} = nq\overrightarrow{v}$ où $n$ représente le nombre de porteurs par unité de volume et $q$ la charge de chacun de ces porteurs.**==
> - ==**L’intensité $I_S(t)$ qui traverse la surface $S$ à la date $t$ est donnée par le flux du vecteur densité de courant à travers $S$ ([[#^figure6|fig. 6]]) : $\displaystyle I_S(t) = \iint_S\overrightarrow{j}(t)\, . d\overrightarrow{S}$.**==
> 
> On peut vérifier que $I(t)$ est bien la charge traversant $S$ par unité de temps.
> En multipliant par $nq$ les deux membres de l’équation différentielle en $\overrightarrow{v}$ établie au [[#^par1|§ 4.1.2.]] nous obtenons l’équation différentielle vérifiée par $\overrightarrow{j}$ en présence d’une force appliquée $\overrightarrow{F}$ : $\tau\dfrac{d\overrightarrow{j}}{dt} + \overrightarrow{j} = \frac{nq\tau}{m}\overrightarrow{F}$ (équation de transport).

> [!note] Les électrons de conduction d'un métal : Comportement d’ensemble en présence d’un champ électrique seul : La loi d’Ohm locale
> Dans ce qui suit, nous expliciterons les propriétés de notre modèle dans l’hypothèse d’un milieu homogène ($n$ est supposé uniforme), en présence d’un champ électrique $\overrightarrow{E}$ supposé localement uniforme et constant (donc $\overrightarrow{F} = q\overrightarrow{E}$), appliqué à compter de la date $t = 0$, pour laquelle on avait $\overrightarrow{v} = \overrightarrow{0}$ et donc $\overrightarrow{j} = \overrightarrow{0}$.
> Pour $t > 0$, une intégration immédiate de l’équation d’évolution de $\overrightarrow{v}$ et de l’équation de transport, donne : $\overrightarrow{v} = \frac{q\tau}{m}\overrightarrow{E}\left(1 - e^{-\frac{t}{\tau}}\right)$ et donc $\overrightarrow{j} = \frac{nq^{2}\tau}{m}\overrightarrow{E}\left(1 - e^{-\frac{t}{\tau}}\right)$.
> Le temps de relaxation de conduction $\tau$ est en général très faible ($\tau$ de l’ordre de $10^{-14}\,s$). Cela signifie que pour $t$ supérieur à $\tau$, donc en pratique pour $t > 0$, l’état permanent est atteint. D’où la **loi d’Ohm locale** : $\overrightarrow{v} = \frac{q\tau}{m}\overrightarrow{E}$ et $\overrightarrow{j} = \frac{nq^{2}\tau}{m}\overrightarrow{E}$.
> Ces relations sont en fait valables en régime quasi stationnaire, pour lequel les variations temporelles éventuelles de $\overrightarrow{E}$ sont lentes (durées typiques de variation nettement plus élevées que $\tau$).
> ==**La vitesse d’ensemble (ou de dérive) des particules $(q, m)$ participant à la conduction est donnée par $\overrightarrow{v} = \mu\overrightarrow{E}$ ; $\mu$ désigne la *mobilité* de ces particules $(\displaystyle\mu = q\frac{\tau}{m})$. Pour les électrons, $\displaystyle\mu = -e\frac{\tau}{m}$ est négatif.**==
> ==**Loi d’Ohm locale :**==
> ==**Le vecteur densité volumique de courants $\overrightarrow{j}$ (s’exprimant en $A\, . m^{-2}$) est proportionnel au champ électrique appliqué au conducteur : $\overrightarrow{j} = \gamma\overrightarrow{E}$, $\gamma$ désigne *la conductivité électrique* du milieu (dit ohmique), dont l’expression est donnée par $\displaystyle\gamma = nq^{2}\frac{\tau}{m}$ ($\tau$ voisin de $10^{-14}\,s$).**==
> ==**L’inverse de la conductivité $\displaystyle\rho = \frac{1}{\gamma}$ est la résistivité. La conductivité s’évalue en $S\,.m^{-1}$ et la résistivité en $\Omega\, . m$.**==

> [!note] Les électrons de conduction d'un métal : Comportement d’ensemble en présence d’un champ électrique seul : Résistance d’un conducteur filiforme cylindrique
> Considérons un conducteur filiforme cylindrique, homogène, de section $s$, de longueur $l$ et de conductivité $\gamma$ ([[#^figure6|fig. 6]]). Un courant continu d’intensité $I$ traverse ce conducteur dans le sens de l’axe $(Ox)$ quand une d.d.p. continue $U$ $(U > 0)$ est appliquée entre ses extrémités.
> Le déplacement des porteurs est « canalisé » par les parois du conducteur. Il s’en suit que le vecteur densité de courant $\overrightarrow{j}$ est en tout point parallèle à $(Ox)$.
> $\overrightarrow{E} = \frac{1}{\gamma}\overrightarrow{j}$ est un champ électrique dont les lignes de champ sont toutes parallèles à $(Ox)$ dans [[#^info2|une région globalement neutre]]. On en déduit (cf. [[#^app6|Application 9]]) que $\overrightarrow{E}$ et $\overrightarrow{j}$ sont uniformes dans le cylindre : $\overrightarrow{E} = E\,\overrightarrow{e}_x$ et $\overrightarrow{j} = j\,\overrightarrow{e}_x = \gamma E\,\overrightarrow{e}_x$.
> En régime permanent, l’intensité $I$ a la même valeur à travers toutes les sections du conducteur : $\displaystyle I = \iint_S\overrightarrow{j}\, . d\overrightarrow{S} = \gamma E\,s$.
> Exprimons $I$ à l’aide du potentiel $V(x)$ associé au champ $\overrightarrow{E}$ : $I = -\gamma s\dfrac{dV}{dx}$.
> $I$ étant indépendant de $x$, cette équation différentielle s’intègre simplement : $\displaystyle\int_{x_1}^{x_2}dV = -\frac{I}{\gamma s}\int_{x_1}^{x_2}dx$ d’où : $U = V_1 - V_2 = \frac{Il}{\gamma s}$.
> Nous en déduisons la valeur de la résistance du conducteur : $R = \frac{U}{I} = \frac{l}{\gamma s} = \rho\frac{l}{s}$.
 

# Définitions

# Diagrammes
Oscilloscope : ➀ : Fil chauffé. ➁ : Wehnelt. ➂ : Électrode de concentration ou de focalisation. ➃ : Électrode d’accélération. ➄ : Plaques de déviation verticale. ➅ : Plaques de déviation horizontale
![[electromagnetisme1/attachments-electromagnetisme1/figure166.png]]^figure1

Le cyclotron. a) vue latérale ; b) les dees vus du dessus
![[electromagnetisme1/attachments-electromagnetisme1/figure173.png]]^figure5

Conducteur cylindrique
![[electromagnetisme1/attachments-electromagnetisme1/figure174.png]]^figure6
# Graphiques
Mouvement d’une particule dans un champ magnétique
![[electromagnetisme1/attachments-electromagnetisme1/figure167.png]]^figure2

Projection de la trajectoire sur les plans de coordonnées dans le cas d’un proton
![[electromagnetisme1/attachments-electromagnetisme1/figure168.png]]^figure3

Trajectoire d’un électron et d’un proton dans un champ $\overrightarrow{B}$ uniforme
![[electromagnetisme1/attachments-electromagnetisme1/figure169.png]]^figure4
# Expériences

# Autres notes
> [!warning] Application 1 page 18
> ![[electromagnetisme1/attachments-electromagnetisme1/figure164.png]]
^app1

> [!warning] Application 3 page 179
> ![[electromagnetisme1/attachments-electromagnetisme1/figure165.png]]
^app2

> [!warning] Application 5 page 183
> ![[electromagnetisme1/attachments-electromagnetisme1/figure170.png]]
^app3

> [!warning] Application 6 page 184
> ![[electromagnetisme1/attachments-electromagnetisme1/figure171.png]]
^app4

> [!warning] Application 7 page 185
> ![[electromagnetisme1/attachments-electromagnetisme1/figure172.png]]
^app5

> [!warning] Comparaison entre vitesse d'agitation thermique et vitesse de dérive
> La vitesse instantanée, due à l’agitation thermique, est beaucoup plus grande que la vitesse de dérive (ou vitesse moyenne).
> Si nous adoptons le modèle des gaz monoatomiques, nous trouvons une vitesse d’agitation de l’ordre de : $u = \sqrt{\frac{3k_BT}{m}} \approx 10^{5} m\, . s^{-1}$.
> La vitesse de dérive est classiquement de l’ordre de $10^{-3} m\, . s^{-1}$.
^info1

> [!warning] Un milieu globalement neutre
> Un conducteur est un milieu globalement neutre à l’échelle mésoscopique.
> Pour un conducteur métallique, la charge des électrons de conduction est exactement compensée par la charge opposée des ions positifs immobiles.
> Pour une solution électrolytique, chaque élément mésoscopique contient des ions positifs et négatifs dont les charges s’équilibrent.
^info2

> [!warning] Application 9 page 190
> ![[electromagnetisme1/attachments-electromagnetisme1/figure175.png]]
^app6