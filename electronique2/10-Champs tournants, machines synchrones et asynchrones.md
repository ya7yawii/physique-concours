---
titre: "[[10-Champs tournants, machines synchrones et asynchrones]]"
tags:
aliases:
crée: 15-12-2025, 14:23
---
# Formules

# Définitions
> [!note] Champs magnétiques tournants
> - Définitions : ==**Un champ tournant est un champ magnétique $\overrightarrow{B}$, de norme constante, tournant dans l’espace avec une vitesse angulaire $\omega_0$ constante et contrôlable.**==
> - Production de champs tournants : Plusieurs méthodes sont utilisées pour produire des champs tournants. Trois d’entre elles sont citées ci-dessous.
> 	- Rotation d’un électro-aimant ou d’un aimant permanent : L'aimant dans sa rotation entraîne le champ magnétique $\overrightarrow{B}$ qu'il crée. Ce champ tournant peut être mis en évidence par une petite aiguille aimantée montée sur un pivot ([[#^figure1|fig. 1]]).
> 	Lorsque l’aimant est au repos, l’aiguille s’oriente dans le champ magnétique $\overrightarrow{B}$ de l'aimant de telle sorte que son moment magnétique $\overrightarrow{M}$ soit parallèle et de même sens que $\overrightarrow{B}$. Dès que l’aimant tourne, l'aiguille se met à tourner dans le même sens et à la même vitesse que lui. Le mouvement de rotation de l'aiguille est *synchrone* de celui du champ tournant.
> 	- Utilisation de champs magnétiques sinusoïdaux en quadrature spatiale et temporelle : Le dispositif réalisé est représenté sur la [[#^figure2|figure 2]]. Les deux bobines ($B_1$) et ($B_2$) identiques ont leurs axes orthogonaux (quadrature spatiale) et sont alimentées par des courants sinusoïdaux de pulsation $\omega_0$ déphasés de $\frac{\pi}{2}$ (quadrature temporelle). Par un choix convenable de l’origine des temps, les champs magnétiques créés en $O$ s’écrivent respectivement : $B_x = B_0\cos(\omega_0 t)$ et $B_y = B_0\sin(\omega_0 t)$.
> 	Le champ résultant $\overrightarrow{B}(t) = B_0[\cos(\omega_0 t)\overrightarrow{e_x} + \sin(\omega_0 t)\overrightarrow{e_y}]$ est un champ de norme $B_0$ constante tournant dans le plan $(xOy)$ a la vitesse angulaire constante $\omega_0$ autour de l’axe $(Oz)$.
> 	« Lançons » une petite aiguille aimantée placée en $O$ : elle « s’accroche » au champ magnétique et finit par être entraînée à la même vitesse angulaire $\omega_0$ que le champ tournant.
> 	En agissant sur la fréquence des courants alimentant les bobines, on contrôle la vitesse de rotation du champ tournant $\overrightarrow{B}$.
> 	Le dispositif précédent peut être rendu plus efficace en associant aux deux bobines ($B_1$) et ($B_2$) deux nouvelles bobines ($B_{1}^{'}$) et ($B_{2}^{'}$) identiques, placées en séries avec leurs homologues et disposées symétriquement par rapport au point $O$ où l’on désire obtenir le champ tournant ([[#^figure3|fig. 3]]).
> 	- Utilisation d'un champ magnétique sinusoïdal : La bobine $B$, alimentée en courant sinusoïdal, crée en $O$ ([[#^figure4|fig. 4]]) un champ alternatif (supposé sinusoïdal) de direction constante $\overrightarrow{e_x}$ qui s'écrit, par un choix convenable de l'origine des temps : $\overrightarrow{B} = B_0\cos(\omega_0 t)\overrightarrow{e_x}$.
> 	Ce champ peut être analysé ([[#^figure5|fig. 5]]) comme la résultante de deux champs d’amplitudes $\frac{B_0}{2}$ tournants en sens opposés avec respectivement les vitesses angulaires $\omega_0$ et $-\omega_0$ : $\overrightarrow{B} = \frac{B_0}{2}([\cos(\omega_0 t)\overrightarrow{e_x} + \sin(\omega_0 t)\overrightarrow{e_y}] + [\cos(-\omega_0 t)\overrightarrow{e_x} + \sin(-\omega_0 t)\overrightarrow{e_y}])$.
> 	Ce résultat est connu en électrotechnique sous le nom de *théorème de Leblanc*. Cette décomposition est utilisée lors de l’étude des machines fonctionnant en courant alternatif monophasé.
> 	Il est possible de vérifier expérimentalement l’existence des deux champs tournants. En effet, disposons dans l’axe des deux bobines une petite aiguille aimantée. Elle reste immobile, car elle est sollicitée simultanément par deux champs tournants en sens inverse l’un de l’autre.
> 	« Lançons » l’aiguille dans un sens arbitraire : elle « s’accroche » sur la pulsation $\omega_0$, et finit par se mettre à tourner en **synchronisme** avec la composante de $\overrightarrow{B}(t)$ tournant dans le même sens. Arrêtons l'aiguille et lançons-la dans l’autre sens : elle finira alors par tourner en synchronisme avec l’autre composante tournante de $\overrightarrow{B}(t)$.
> 	
> 	Retenons, pour conclure :
> 	==**Des enroulements fixes, régulièrement distribués autour d'un point $O$ et parcourus par un système de [[#^demo1|courants polyphasés équilibrés]] produisent en $O$ un champ magnétique tournant.**==

> [!note] Principe de machines synchrones : Action d'un champ tournant sur un aimant
> Lors de la mise en évidence des champs tournants, nous avons utilisé une petite aiguille aimantée pour vérifier la rotation du champ.
> Nous nous proposons d’étudier l’action d’un champ tournant $\overrightarrow{B}(t)$ tournant à $\omega_0$ sur un aimant de moment magnétique $\overrightarrow{M}$ constant en norme mais en mouvement de rotation à la vitesse angulaire $\omega$ : $\overrightarrow{M}(t)$ avec $\left\Vert\overrightarrow{M}\right\Vert = M_0$.
> Le champ et le moment magnétique tournent donc respectivement à la vitesse $\omega_0$ et $\omega$ autour du même axe $(O, \overrightarrow{e_z})$.
> Soit $\overrightarrow{B}(0)$ et $\overrightarrow{M}(0)$ les positions initiales de $\overrightarrow{B}(t)$ et de $\overrightarrow{M}(t)$, et $\theta_0 = (\overrightarrow{M}(0), \overrightarrow{B}(0))$ le décalage angulaire initial $(t = 0)$ du champ par rapport à l’aimant repéré par son moment magnétique ([[#^figure6|fig. 6]]).
> A la date $t$, le champ tournant $\overrightarrow{B}(t)$ et le moment magnétique $\overrightarrow{M}(t)$ forment entre eux un angle $\theta(t)$ tel que : $\theta(t) = (\omega_0 t + \theta_0) - \omega t = (\omega_0 - \omega)t + \theta_0$.
> L'action du champ tournant sur l'aimant se traduit par un couple dont le moment par rapport à l’axe de rotation est $(\overrightarrow{\Gamma} = \overrightarrow{M} \wedge \overrightarrow{B})$ : $\Gamma_z(t) = M_0B\sin[\theta(t)] = M_0B\sin[(\omega_0 - \omega)t + \theta_0]$.
> - Si $\omega_0 \neq \omega$, ce couple a un moment de valeur moyenne nulle et il fournit un travail moyen nul.
> ==**Un aimant (moment magnétique $M_0$), lancé à une vitesse $\omega$ différente de celle $\omega_0$ du champ tournant, ne peut pas maintenir cette vitesse de rotation à cause de l’action des frottements.**==
> - Si $\omega = \omega_0$, le décalage angulaire de l'aimant par rapport au champ tournant est constant: $\theta = \theta_0$. Le moment $\Gamma_z(t)$ du couple des forces magnétiques a la valeur constante : $\Gamma(\theta) = M_0B\sin(\theta)$.
> ==**Lorsqu’un aimant est lancé à la vitesse $\omega_0$ du champ tournant (vitesse de synchronisme), l’action du champ tournant sur l'aimant se traduit par un couple de moment : $\Gamma(\theta) = M_0B\sin(\theta)$.**==
> ==**Ce couple est moteur lorsque $0 < \theta < \pi$ et il est résistant lorsque $-\pi < \theta < 0$ ([[#^figure7|fig. 7]]).**==
> La machine synchrone est basée sur ce principe.
> 
> Une machine synchrone est conçue sur l'interaction entre un champ magnétique tournant et un **aimant** (dipôle magnétique de module constant en norme).

> [!note] Principe de machines synchrones : Structure d'une machine synchrone
> Une machine synchrone est un convertisseur de puissance utilisant l’interaction de deux champs magnétiques, dont le premier est un champ tournant créé par une armature fixe appelée **stator** et dont le second est créé soit par un aimant, soit par un électro-aimant alimenté par un courant continu, constituant l’élément mobile appelé **rotor**.
> Dans une machine synchrone *polyphasée*, le champ tournant est créé par un système de courants polyphasés équilibrés circulant dans des circuits statoriques appelés **phases**. Dans une machine *monophasée*, le champ magnétique tournant correspond à une des composantes du champ sinusoïdal de direction fixe créé par un courant monophasé.
> La plupart des machines sont *triphasées*, c’ est-à-dire qu’elles utilisent des systèmes de courants triphasés équilibrés.
> Cependant, conformément au programme, nous limiterons notre étude aux machines diphasées dont le champ tournant $\overrightarrow{B}(t)$ est produit par un système de courants diphasés équilibrés et aux machines monophasées dont le stator est alimenté par un courant monophasé sinusoïdal.
> Le rotor d’une machine synchrone est constitué de bobinages alimentés en courant continu (ou d’aimants permanents pour les machines de faible puissance). Les bobinages, logés dans des encoches du rotor, ont leurs extrémités soudées à des bagues solidaires de l'arbre de rotation. C’est par l’intermédiaire de balais frottant sur ces bagues qu’il est possible d’accéder aux circuits rotoriques et ainsi de les alimenter.
> L'alimentation du rotor est faite sans commutation (par opposition aux moteurs continus, cf. [[09-Machines à courant continu|chapitre 9]]).
> Nous limiterons notre étude aux machines bipolaires pour lesquelles le rotor ne comporte qu’une paire de pôles nord-sud.
> En définitive, les seules machines synchrones que nous examinerons sont soit des machines diphasées bipolaires ([[#^figure8|fig. 8]]), soit des machines monophasées bipolaires ([[#^figure9|fig. 9]]).
> La représentation symbolique de ces moteurs synchrones est donnée sur la [[#^figure10|figure 10]].

> [!note] Principe de machines synchrones : Propriétés des moteurs synchrones
> - Couple moteur : Lorsque le rotor d’un moteur synchrone est lancé dans le champ tournant statorique $\overrightarrow{B}(t)$, à la vitesse de synchronisme $\omega_0$, il est soumis à un couple électromagnétique moteur dont le moment est : $\Gamma(\theta) = M_0B\cos(\theta)$ avec $0 < \theta < \pi$.
> Le couple moteur maximal $\Gamma_{r\,max} = M_0B$ est appelé couple de décrochage. Si le rotor est lancé à une vitesse angulaire différente, le couple électromagnétique moyen est nul et les actions extérieures exercées sur le rotor modifient sa vitesse de rotation.
> ==**Les moteurs synchrones ne peuvent tourner, comme leur nom l’indique, qu’à la vitesse de synchronisme.**==
> Pour contrôler la vitesse d’un moteur synchrone, il faut contrôler la fréquence de rotation de son champ tournant, c’est-à-dire la fréquence des courants polyphasés utilisés. On se sert pour cela du système de courants polyphasés produits par un **onduleur**.
> Les moteurs synchrones ne peuvent pas démarrer par eux-mêmes, ce qui est un sérieux inconvénient. Pour les mettre en synchronisme, c’est-à-dire pour les « accrocher » au champ tournant, il faut soit les lancer à l'aide d’un petit moteur auxiliaire, soit munir leurs rotors d’un dispositif appelé « **cage d'écureuil** » afin qu’ils puissent démarrer en moteur asynchrone. Lorsqu’une charge mécanique impose au moteur un couple résistant $-\Gamma_r$ avec $\Gamma_r$ inférieur au couple de décrochage $\Gamma_{r\,max} = M_0B$, le moment magnétique $\overrightarrow{M}(t)$ du rotor se décale d’un angle $\theta$ par rapport au champ tournant $\overrightarrow{B}(t)$ afin d’obtenir, en régime établi, l’égalité $\Gamma_r = M_0B\sin(\theta)$. Il existe deux valeurs pour le décalage angulaire $\theta$ permettant au moteur d’entraîner sa charge mécanique ([[#^figure11|fig. 11]]).
> La première valeur $\theta_1$ $\left(0 < \theta_1 < \frac{\pi}{2}\right)$ correspond à un régime **de fonctionnement stable**.
> En effet, si pour une cause quelconque le rotor ralentit, ce qui augmente son décalage angulaire $\theta$, le couple moteur $\Gamma = M_0B\sin(\theta)$ augmente aussi : ce qui accélère le rotor et rétablit le décalage à sa valeur initiale.
> Si, pour une cause quelconque, le rotor accélère et diminue son décalage angulaire $\theta$, le couple moteur diminue aussi ; ce qui freine le rotor et rétablit, à nouveau, le décalage à sa valeur initiale.
> La seconde valeur $\theta_2$ $\left(\frac{\pi}{2} < \theta_2 < \pi\right)$ correspond à un régime de fonctionnement instable pour des raisons symétriques de celles examinées dans le cas précédent.
> ==**Dans un moteur synchrone polyphasé bipolaire en régime de fonctionnement stable, le décalage angulaire $\theta$ (retard) du rotor par rapport au champ tournant est : $\left(0 < \theta < \frac{\pi}{2}\right)$.**==
> - Bilan de puissance : Un moteur synchrone polyphasé reçoit dans son stator une puissance électrique $\mathcal{P}_e$ somme des puissances reçues par chacune de ses phases : $\displaystyle \mathcal{P}_e = \sum_k U_kI_k\cos\varphi_k$, avec $I_k$ la valeur efficace du courant à travers l’enroulement de la phase $k$ et $U_k$ la valeur efficace de la tension aux bornes de cet enroulement dont le facteur de puissance est $\cos(\varphi_k)$.
> Si les $p$ phases sont équilibrées, les tensions, courants et déphasages sont identiques pour chacune d’entre elles et $\mathcal{P}_e = pUI\cos\varphi$. En régime établi, le flux à travers les bobinages du rotor est constant. Si nous négligeons les pertes par effet Joule, nous pouvons donc considérer qu’aucune puissance électrique ne lui est fournie.
> Alors, la puissance électrique fournie aux circuits statoriques est intégralement convertie en puissance mécanique $\mathcal{P}_m = \Gamma\omega_0$ : $\Gamma\omega_0 = pUI\cos\varphi$.
> - f.e.m. d'induction dans les circuits statoriques et schéma électrique équivalent : Quand le moteur tourne, le rotor envoie à travers chacune des bobines $B_k$ du stator un flux $\Phi_k(t)$ variable. Dans chacune de ces bobines, c’est-à-dire dans chacun des circuits de phase, apparaît une f.e.m. d’induction : $e_k = -\dfrac{d\Phi_k}{dt}$.
> Cette f.e.m. est périodique et les constructeurs s’attachent à la rendre aussi sinusoïdale que possible. Elle est une fonction croissante du *courant d’excitation $I_e$* qui alimente le rotor ([[#^figure12|fig. 12]]). Ce courant, très facilement contrôlable, sert aux réglages du moteur.
> Le schéma équivalent d’une machine synchrone pour chacune de ses phases $k$ est donné sur la [[#^figure13|figure 13]].
> L’impédance du stator est $\underline{Z} = R + jL\omega_0$ avec très souvent $R \ll L\omega_0$.
> La valeur efficace $E_k$ de la f.e.m. $e_k$ de la machine est proportionnelle au flux maximal $\Phi_0$ à travers chacune des spires statoriques et à la pulsation de synchronisme $\omega_0$ : $E_k = K\omega_0\Phi_0$, où K est un facteur de bobinage. La loi d’Ohm, en termes complexes, appliquée à la phase $k$ de la machine s’écrit : $\underline{U}_k = \underline{E}_k + \underline{Z}\,\underline{I}_k$.

> [!note] Principe de machines synchrones : Utilisation des moteurs synchrones
> Pour clore cette étude des synchrones, citons les qualités, les défauts et les utilisations de ce type de moteurs.
> - Qualités :
> 	- Excellent rendement (comparable à celui des alternateurs : de 85 % à 95 %).
> 	- Facteur de puissance facilement réglable au moyen du courant d’excitation $I_e$ alimentant le rotor.
> 	- Vitesse fixée par la fréquence du courant d’alimentation créant le champ tournant et permettant l'*autopilotage* du moteur.
> - Défauts :
> 	- Démarrage difficile et non autonome.
> 	- Risque de décrochage en cas de surcharge mécanique.
> - Utilisations :
> 	- Moteurs devant entraîner, à la vitesse constante, des charges mécaniques soumises à des couples variables.
> 	- Moteurs devant fonctionner en permanence ou subissant peu de démarrages.
> 	- Moteurs pouvant être autopilotés et se prêtant alors à de multiples usages dont la traction électrique : le T.G.V. Atlantique est équipé de moteurs synchrones autopilotés.

> [!note] Principe de machines synchrones : Alternateurs
> - Principe des alternateurs : Dans un moteur synchrone, les flux $\Phi_k(t)$, envoyés par le rotor à travers les bobines du stator, varient dans le temps. Ces flux créent, dans les enroulements des différentes phases du moteur, un système de f.e.m. $e_k(t)$ d’induction polyphasés.
> Supprimons les courants polyphasés qui alimentent le moteur et faisons tourner le rotor à la vitesse angulaire de synchronisme $\omega_0$. Les valeurs efficaces des f.e.m, induites $e_k(t)$ dans les bobines ne sont pas modifiées et la machine fonctionne maintenant en générateur synchrone, c’est-à-dire en **alternateur**.
> ==**Un alternateur et un moteur synchrone sont une seule et même machine électrique.**==
> Si ces bobines sont fermées sur des circuits extérieurs identiques, un système de courants polyphasés équilibré s’établit dans ces circuits.
> Les bobines alimentées par ces courants créent à leur tour un champ tournant $\overrightarrow{B}(t)$ dans la machine.
> Ce champ engendre, sur le rotor, un couple résistant $\Gamma = MB\sin(\theta) < 0$ qui tend à s’opposer à sa rotation.
> Cette fois, le décalage $\theta = (\overrightarrow{M}, \overrightarrow{B})$ entre le moment magnétique $\overrightarrow{M}(t)$ du rotor et le champ tournant $\overrightarrow{B}(t)$ est négatif et c’est le moment magnétique du rotor qui se trouve en avance sur le champ tournant qu’il crée ([[#^figure14|fig. 14]]).
> ==**Dans un alternateur, le moment magnétique $\overrightarrow{M}(t)$ du rotor est en avance sur le champ tournant statorique $\overrightarrow{B}(t)$ qu’il crée et la rotation du rotor est freinée par le couple électromagnétique résistant : $\Gamma(\theta) = M_0B\sin(\theta) < 0$ avec $-\pi < \theta < 0$.**==
> Dans un alternateur, le rotor est l’inducteur et les bobines du stator constituent l'induit : **l'inducteur est mobile et l’induit est fixe.**
> **Alternateur** : Un aimant (dipôle de moment magnétique constant en norme) en rotation donne naissance à des courants induits dans les bobines fixes du stator. Dans un alternateur, le rotor est l'inducteur et les bobines du stator constituent l'induit : l'inducteur est mobile et l'induit est fixe.
> - Performances des alternateurs : La conversion d’énergie mécanique en énergie électrique est majoritairement réalisée à l'aide d’alternateurs : de l’alternateur de bicyclette ([[#^figure15|fig. 15]]) de quelques watts à celui de centrale nucléaire ([[#^figure16|fig. 16]]) de plus d’un gigawatt ! La puissance apparente des machines triphasées les plus performantes atteint 1 500 MVA, avec des tensions efficaces comprises entre $10^{4} kV$ et $2 \,. 10^{4} kV$, et le rendement des alternateurs les plus modernes est voisin de 99 %.

> [!note] Principe des machines asynchrones : Action d'un champ tournant sur un circuit inductif
> Plaçons dans un champ tournant $\overrightarrow{B}(t)$, non plus un aimant, mais un circuit plan sans source, de vecteur surface $\overrightarrow{S}$, de résistance $R$ et d’inductance $L$. Supposons que ce circuit puisse tourner autour du même axe $(O, \overrightarrow{e_z}$ que le champ tournant $\overrightarrow{B}(t)$. Notons par $\omega_0$ la vitesse de rotation du champ $\overrightarrow{B}(t)$ et par $\omega$ celle du circuit ([[#^figure17|fig. 17]]). Remarquons que nous ne sommes donc plus en présence d'un moment magnétique de module constant en rotation.
> La loi de Lenz affirme que les effets des phénomènes d’induction s’opposent à leur cause. Nous pouvons en déduire le résultat qualitatif suivant : la spire a tendance à tourner à la même vitesse que le champ magnétique.
> - Si $\omega < \omega_0$, le couple électromagnétique a tendance à accélérer la spire. Le couple est moteur.
> - Si $\omega = \omega_0$, il n’y a aucun couple exercé sur la spire.
> - Si $\omega > \omega_0$, le couple électromagnétique a tendance à freiner la spire. Le couple est résistant.
> 
> ==**Dans un champ magnétique tournant à la vitesse $\omega_0$, un circuit sans source est soumis à un couple électromagnétique moteur $(\Gamma > 0)$ ou résistant $(\Gamma < 0)$ selon que sa vitesse $\omega$ de rotation est inférieure ou supérieure à la vitesse de synchronisme $\omega_0$. À la vitesse de synchronisme, ce couple est de valeur nulle.**==
> ==**Le moteur asynchrone est basé sur ce principe.**==

> [!note] Principe des machines asynchrones : Structure d'une machine asynchrone
> Une machine *asynchrone* est un convertisseur de puissance utilisant, comme les machines synchrones, l’interaction de deux champs magnétiques. Si le premier champ est, comme dans les machines synchrones, créé par une armature fixe appelée **stator**, le second, quand à lui, est créé par un circuit mobile *sans source* appelé **rotor** (et non plus par un aimant ou un électroaimant).
> Nous distinguerons encore les machines asynchrones *polyphasées*, dont les enroulements statoriques sont alimentés par un système de courants polyphasés équilibrés créant un *champ tournant*, des machines *monophasés* dont les enroulements sont alimentés par un courant sinusoïdal créant un champ sinusoïdal de direction fixe.
> Le stator d’une machine asynchrone est analogue à celui d’une machine synchrone. Par opposition avec les moteurs à courants continus et synchrones, le rotor ne nécessite pas d’alimentation. Les courants qui le traversent sont uniquement dus aux phénomènes d’induction.
> Il en existe deux types.
> - Rotor en cage d’écureuil : Des barres métalliques parallèles sont reliées à deux anneaux conducteurs ([[#^figure18|fig. 18]]), Les moteurs à cage sont caractérisés par leur simplicité de construction, leur facilité d’entretien, leur robustesse et leur faible coût de revient. Ce sont les moteurs électriques les plus utilisés, mais ils sont de faible puissance (jusqu’à 10 kW).
> - Rotor bobiné : Les conducteurs, logés dans des encoches du rotor, forment un circuit dont les extrémités sont soudées à des bagues solidaires de l’arbre de rotation. Par l'intermédiaire de balais frottant sur ces bagues, il est possible d’accéder au rotor et de modifier, à l’aide d’un rhéostat, la résistance du circuit rotorique. La représentation symbolique d’un moteur asynchrone est donnée sur la [[#^figure19|figure 19]].
> 
> Machine asynchrone : Une machine asynchrone est conçue sur l'interaction entre un champ magnétique tournant et un **circuit fermé sans source**.

> [!note] Principe des machines asynchrones : Propriétés des moteurs asynchrones
> D’après l'étude de l’[[#^appli1|application ci-dessous]], le couple de démarrage est non nul. Un moteur asynchrone peut démarrer en charge.
> Lorsque le rotor est bobiné, il est possible de régler, à l'aide d’un rhéostat, la résistance $R$ du circuit rotorique. Après avoir donné à $R$ la valeur $R_{opt} = L\omega_0$ (cf. [[#^appli1|Application ci-dessous]]) pour le démarrage, on diminue la valeur de la résistance pour la mise en vitesse de telle sorte que le moteur soit utilisé au voisinage de son couple et de son rendement maximum.
> ==**En charge, la vitesse $\omega$ d'un moteur asynchrone est inférieure à celle $\omega_0$ du champ tournant et cette vitesse est d'autant plus faible que la charge est plus importante. Lorsque cette dernière introduit un couple résistant supérieur à $\Gamma_{max} = \frac{\Phi_{0}^{2}}{4L}$ (couple de décrochage), le moteur décroche et s'arrête.**==
> ==**Le fonctionnement d’un moteur asynchrone est caractérisé par son glissement $g = \frac{\omega_0 - \omega}{\omega_0}$ qui est l’écart relatif entre la vitesse de rotation $\omega_0$ du champ tournant et la vitesse $\omega$ de rotation. Au point de fonctionnement nominal, ce glissement est faible (< 5 % en général).**==
> Le couple d’une machine asynchrone est moteur $(\Gamma > 0)$ pour $g > 0$. Plus précisément, pour $0 < g < 1$, la machine fonctionne effectivement en moteur, pour $g = 1$ elle est à l’arrêt, et pour $g > 1$ le moteur fonctionne en frein (cf. [[#^appli1|Application ci-dessous]]).


# Diagrammes
L'aimant dans sa rotation crée un champ magnétique tournant qui entraîne l'aiguille à la même vitesse $\omega_0$
![[electronique2/attachments-electronique2/figure251.png]]^figure1

Deux champs magnétiques en quadrature spatiale et temporelle créent un champ tournant $\overrightarrow{B}$
![[electronique2/attachments-electronique2/figure252.png]]^figure2

En doublant les champs magnétiques en quadrature spatiale et temporelle, on double l'amplitude du champ tournant ; la vitesse de rotation angulaire du champ est inchangée
![[electronique2/attachments-electronique2/figure253.png]]^figure3

Création d'un champ sinusoïdal
![[electronique2/attachments-electronique2/figure254.png]]^figure4

Un champ sinusoïdal $\overrightarrow{B}(t)$ est la résultante de deux champs $\overrightarrow{B_1}(t)$ et $\overrightarrow{B_2}(t)$ de mêmes amplitudes et tournant en sens inverse
![[electronique2/attachments-electronique2/figure255.png]]^figure5

Disposition relative du champ tournant $\overrightarrow{B}(t)$ et du moment magnétique $\overrightarrow{M}(t)$ de l'aimant à $t = 0$ et à $t \neq 0$ ($\left\Vert\overrightarrow{M}(0)\right\Vert = \left\Vert\overrightarrow{M}(t)\right\Vert$ et $\left\Vert\overrightarrow{B}(0)\right\Vert = \left\Vert\overrightarrow{B}(t)\right\Vert$)
![[electronique2/attachments-electronique2/figure258.png]]^figure6

Principe d'une machine synchrone diphasée bipolaire
![[electronique2/attachments-electronique2/figure260.png]]^figure8

Principe d'une machine synchrone monophasée bipolaire
![[electronique2/attachments-electronique2/figure261.png]]^figure9

Représentation symbolique des moteurs synchrones. a. Monophasé. b. Diphasé
![[electronique2/attachments-electronique2/figure262.png]]^figure10

Schéma équivalent d'une phase d'une machine synchrone
![[electronique2/attachments-electronique2/figure265.png]]^figure13

Alternateur diphasé bipolaire
![[electronique2/attachments-electronique2/figure266.png]]^figure14

Positions relatives du circuit et du champ tournant à $t = 0$ et à un instant ultérieur $t$
![[electronique2/attachments-electronique2/figure269.png]]^figure17

Représentation symbolique des moteurs asynchrones monophasés. a. À rotor bobiné. b. En cage d'écureuil
![[electronique2/attachments-electronique2/figure271.png]]^figure19
# Graphiques
Variation du couple des forces électromagnétiques s'exerçant sur un aimant en fonction de son décalage angulaire $\theta$ par rapport au champ tournant
![[electronique2/attachments-electronique2/figure259.png]]^figure7

Pour une charge mécanique donnée, il existe, en général, deux points de fonctionnement $M_1$ et $M_2$ pour un moteur synchrone. Le régime de fonctionnement est stable en $M_1$ et instable en $M_2$
![[electronique2/attachments-electronique2/figure263.png]]^figure11

$\Phi_0$ et $E_k$ sont des fonctions croissantes du courant d'excitation $I_e$ qui alimente le rotor. La zone utile de fonctionnement est au voisinage du coude de saturation (point $A_N$)
![[electronique2/attachments-electronique2/figure264.png]]^figure12

Alternateur de bicyclette
![[electronique2/attachments-electronique2/figure267.png]]^figure15

Alternateur à pôles saillants des centrales hydrauliques entraîné à faible vitesse par des chutes d'eau
![[electronique2/attachments-electronique2/figure268.png]]^figure16

Rotor en cage d'écureuil
![[electronique2/attachments-electronique2/figure270.png]]^figure18
# Expériences

# Autres notes
> [!warning] Application 1 page 312
> ![[electronique2/attachments-electronique2/figure256.png]]![[electronique2/attachments-electronique2/figure257.png]]
^demo1

> [!warning] Application
> ![[electronique2/attachments-electronique2/figure272.png]]![[electronique2/attachments-electronique2/figure273.png]]![[electronique2/attachments-electronique2/figure274.png]]![[electronique2/attachments-electronique2/figure275.png]]![[electronique2/attachments-electronique2/figure276.png]]
^appli1