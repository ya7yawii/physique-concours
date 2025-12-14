---
titre: "[[09-Machines à courant continu]]"
tags:
aliases:
crée: 13-12-2025, 14:01
---
# Formules

# Définitions
==**Machine à courant continu**== :
==**Une machine est dite à courant continu lorsque les grandeurs électriques (potentiels et courants) sont unidirectionnelles.**==
==**Une machine à courant continu est un convertisseur électromécanique rotatif « réversible » (ou « inversible ») permettant ([[#^figure1|fig. 1]]) :**==
- ==**une conversion d’énergie électrique en énergie mécanique : fonctionnement moteur ;**==
- ==**une conversion d’énergie mécanique en énergie électrique : fonctionnement génératrice.**==
==**Une machine à courant continu est un convertisseur électromécanique rotatif utilisant :**==
- ==**les forces de Laplace dans le dispositif mécanique ;**==
- ==**les phénomènes d’induction électromagnétique dans le dispositif électrique.**==
Ces transformations s’accompagnent inévitablement de pertes sous forme de chaleur ([[#^figure1|fig. 1]]) dont les causes sont de nature mécanique (frottements), électrique (effet Joule) et magnétique (courants de Foucault, hystérésis).

> [!note] Structure d'une machine à courant continu
> ==**Une machine à courant continu s’analyse en un circuit magnétique, deux circuits électriques et un dispositif de commutation.**==
> La [[#^figure2|figure 2]] présente un moteur à courant continu : un moteur d’essuie-glace fonctionnant sous une tension continue de 6 volts.
> - Circuit magnétique : Il est constitué ([[#^figure3|fig. 3a]]) d’une partie fixe, le **stator** ou **inducteur** (1 et 7), solidaire du **bâti** (2) de la machine dont l'arbre (3) porte la partie mobile, le **rotor** ou **induit** (4).
> Entre le stator et le rotor se trouve l'**entrefer** (5).
> Un champ magnétique intense est nécessaire pour obtenir une machine performante. Afin d’obtenir des champs magnétiques importants (de l'ordre du tesla), le stator et le noyau du rotor sont réalisés avec des matériaux ferromagnétiques.
> L'entrefer entre induit et inducteur doit être étroit pour limiter les pertes de flux, et obtenir ainsi un champ intense.
> Sur le moteur de [[#^figure2|figure 2]], le champ magnétique est créé grâce à un courant passant dans le bobinage visible sur la [[#^figure2|figure 2c]], Le circuit magnétique est feuilleté ([[#^figure2|fig. 2a]]) pour limiter les pertes dues aux courants de Foucault lors du démarrage du moteur.

> [!note] Structure d'une machine à courant continu : Circuits électriques
> - Circuit de l'inducteur : Il est formé ([[#^figure3|fig. 3a]]) de **bobines** (6) montées en série, alimentées, en courant continu et placées autour d’un nombre pair 2p de **pièces polaires** (7).
> La machine de [[#^figure3|figure 3a]] est bipolaire $(2p = 2)$ avec un pôle nord et un pôle sud. Les machines multipolaires $(2p > 2)$ possèdent $p$ pôles nord alternés avec $p$ pôles sud. Sur la [[#^figure3|figure 3b]], nous avons une machine tétrapolaire.
> Les **lignes de champ** (13) partent des pôles nord, traversent l’entrefer, puis le rotor où elles sont canalisées, ensuite elles franchissent à nouveau l’entrefer, aboutissent aux pôles sud et retournent par le stator aux pôles nord. Dans le cas d’une machine bipolaire ([[#^figure3|fig. 3a]]), l'axe des pôles $(x'Ox)$ (8) est un **axe de symétrie** du circuit magnétique et des lignes de champ magnétique. La ligne neutre $(y'Oy)$ (9) est un **axe d’antisymétrie** du circuit magnétique et des lignes de champ magnétique.
> Remarque : Les machines de faible puissance ne possèdent pas de circuit inducteur, Le champ magnétique, créé par des aimants permanents (ferrites, samarium, cobalt, ...), est permanent.
> - Circuit de l'induit : Il est réalisé par un enroulement, sous forme de spires ([[#^figure2|fig. 2]]) autour du rotor de forme cylindrique (cylindre de hauteur $h$ et de rayon $R$). Les parties de cet enroulement qui se trouvent dans le champ magnétique, à l’intérieur d’encoches (10) taillées le long des génératrices du rotor, forment les **conducteurs actifs**, par opposition aux **conducteurs passifs** ([[#^figure2|fig. 2]]) qui se trouvent, à l’extérieur du champ magnétique, sur les deux bases du rotor.

> [!note] Structure d'une machine à courant continu : Dispositif de commutation
> Les extrémités des spires sont soudées sur un ensemble de $2a$ lames de cuivre solidaires du rotor et isolées les unes des autres. L’ensemble de ces lames forme le **collecteur** (11) de la machine. Sur le collecteur frottent des **balais** (12) en graphite, solidaires du bâti, donc fixes. Le collecteur et les balais réalisent un dispositif de commutation.
> Celui-ci permet l'établissement de la liaison électrique entre le circuit d'induit et l'extérieur de la machine.

> [!note] Structure d'une machine à courant continu
> La représentation symbolique d'une machine à courant continu est donnée sur la [[#^figure4|figure 4]].
> Remarque :
> Les machines à courant continu étant des machines à deux circuits électriques, il existe plusieurs possibilités de branchement de ces circuits, ce qui conduit à autant de types de machines. Citons trois types ([[#^figure5|fig. 5]]) :
> - machine à excitation indépendante, dont le circuit inducteur est séparé du circuit de l’induit ;
> - machine à excitation série, dont le circuit inducteur est en série avec le circuit de l’induit ;
> - machine à excitation parallèle (ou shunt), dont le circuit inducteur est en parallèle sur le circuit de l’induit.
> 
> ==**Les machines les plus utilisées sont :**==
> - ==**les machines à excitation indépendante ;**==
> - ==**les machines à excitation série.**==
> 
> ==**En particulier, les moteurs universels (moteurs spécialement répandus) sont des moteurs à excitation série pouvant être alimentés en courant continu ou en courant alternatif.**==

> [!note] Structure d'une machine à courant continu : Principe de fonctionnement
> En première approximation, dans l’entrefer situé entre les deux cylindres ([[#^figure6|fig. 6a]] et [[#^figure6|b]]), le champ magnétique $\overrightarrow{B}$ est de type « radial ». Il existe une ligne neutre $(y'Oy)$ ; le champ $\overrightarrow{B}$ est quasiment de la forme :
> - à gauche $(0 < \theta <\pi)$ : $\overrightarrow{B} = -B_0\overrightarrow{e}_r$ ;
> - à droite $(\pi < \theta <2\pi)$ : $\overrightarrow{B} = B_0\overrightarrow{e}_r$ ;
> 
> Que cette machine soit utilisée en génératrice ou en moteur, un conducteur actif (de longueur $h$, parallèle aux génératrices du cylindre) se déplace dans cet entrefer en coupant des lignes de champ magnétique, d’où :
> - il est le siège d’une force électromotrice d’induction (qu’il soit ou non parcouru par un courant) ;
> - il est soumis à une force (magnétique) de Laplace s’il est parcouru par un courant.
> 
> Calculs :
> - Calcul de la f.e.m. d'induction pour un conducteur actif : Les conducteurs actifs sont des fils parallèles à l’axe $(Oz)$ du rotor et de longueur $h$. Ils se déplacent avec une vitesse $\overrightarrow{v} = \omega R\overrightarrow{e}_{\theta}$ en coupant les lignes de champ magnétique.
> Orientons, dans le sens de $\overrightarrow{e}_{z}$, les conducteurs actifs situés à gauche de la ligne neutre ($A'B'$ dans la [[#^figure7|figure 7]]), et dans le sens inverse, ceux qui sont situés à droite de la ligne neutre ($AB$ dans la [[#^figure7|figure 7]]).
> Notons $B(\theta) = -\overrightarrow{B} . \overrightarrow{e}_{r}$ le champ magnétique au niveau d'un conducteur actif. D'après nos conventions, $B(\theta) = +B_0$ à gauche de la ligne neutre et $B(\theta) = -B_0$ à droite.
> Chaque conducteur actif est le siège d'un champ électromoteur $\overrightarrow{E_m}$ de la forme : $\overrightarrow{E_m} = \overrightarrow{v} \wedge \overrightarrow{B} = \omega RB(\theta)\overrightarrow{e}_{z}$.
> La f.e.m. d'induction est donc :
> 	- $\displaystyle e_a = \int_{A'}^{B'}\overrightarrow{E_m} . d\overrightarrow{L} = \omega RhB_0$ à gauche de la ligne neutre ;
> 	- $\displaystyle e_a = \int_{A}^{B}\overrightarrow{E_m} . d\overrightarrow{L} = \omega RhB_0$ à droite de la ligne neutre.
> 
> 	==**Avec nos hypothèses et nos conventions d'orientation, la f.e.m. d'induction a la même valeur $e_a = \omega RhB_0$ pour tous les conducteurs actifs.**==
> - Calcul de la force de Laplace sur un conducteur actif : Les conducteurs actifs, orientés comme précédemment, sont parcourus par le même courant $I$.
> La force de Laplace appliquée à un conducteur actif est ([[#^figure8|fig. 8]]) :
> 	- $\displaystyle \overrightarrow{F} = I\int_{A'}^{B'}d\overrightarrow{L} \wedge \overrightarrow{B} = IB_0\int_{A'}^{B'}\overrightarrow{e}_{z} \wedge (-\overrightarrow{e}_{r})dz = -IB_0h\overrightarrow{e}_{\theta}$ à gauche de la ligne neutre ;
> 	- $\displaystyle \overrightarrow{F} = I\int_{A}^{B}d\overrightarrow{L} \wedge \overrightarrow{B} = IB_0\int_{A}^{B}(-\overrightarrow{e}_{z}) \wedge \overrightarrow{e}_{r}dz = -IB_0h\overrightarrow{e}_{\theta}$ à droite de la ligne neutre ;
> 	
> 	==**Avec nos hypothèses et nos conventions d'orientation, la force de Laplace a la même expression $\overrightarrow{F} = -IB_0h\overrightarrow{e}_{\theta}$ pour tous les conducteurs actifs.**==
> 
> Remarque : Nous pouvons vérifier sur cet exemple la relation générale établie au chapitre précédent : $\mathcal{P}_L = \overrightarrow{F} . \overrightarrow{v} = -\omega RIB_0h = -e_a I$.
^par1

> [!note] Fonctionnement d'une machine idéale : Machine à deux conducteurs actifs
> Considérons ([[#^figure9|fig. 9]] et [[#^figure10|10]]) une machine bipolaire à $N = 2$ conducteurs actifs en série, c'est-à-dire à une seule spire $MNPQ$. La position du rotor est repérée par l'angle $\theta$.
> - Dans la situation de [[#^figure9|figure 9]] ($\theta$ compris entre 0 et $\pi$), les deux conducteurs actifs $MN$ et $PQ$ sont orientés selon les conventions du paragraphe précédent. La f.e.m. induite dans la spire est donc : $e_{MNPQ} = 2e_a = 2\omega RhB_0$.
> Le circuit compris entre les balais $\mathcal{B}_1$ et $\mathcal{B}_2$ a la même orientation que la spire $MNPQ$. Sa f.e.m. (donc celle du moteur) est : $e = e_{MNPQ} = 2\omega RhB_0$.
> - Lorsque la spire traverse la ligne neutre, les collecteurs changent de balais ([[#^figure11|fig. 11]]). Pour conserver au circuit la même orientation (de $\mathcal{B}_1$ vers $\mathcal{B}_2$), il faut orienter la spire dans le sens $QPNM$. Les fils actifs ont alors toujours une orientation conforme à nos conventions, et la f.e.m. du moteur est : $e = e_{QPNM} = 2\omega RhB_0$.
> 
> Grâce à la commutation ([[#^figure2|fig. 2d]]), la f.e.m, entre les balais garde un signe constant. Nous pouvons même supposer qu’elle est constante (pour $\omega$ constant) si nous négligeons les zones de transition, situées près de la ligne neutre où $B(\theta)$ change de signe ([[#^figure12|fig. 12]]).
> Nous pouvons alors écrire : $e = \Phi_0\omega$ avec $\Phi_0 = 2RhB_0$.
> La constante $\Phi_0$ est homogène à un flux. Elle peut se mettre sous la forme : $\Phi_0 = k\Phi$ avec $\Phi = \pi RhB_0$ et $k = \frac{2}{\pi}$.
> $\Phi$, appelé **flux utile sous chacun des pôles**, représente le flux du champ $\overrightarrow{B}$ à travers les pôles de l'inducteur.
> **Attention** : $\Phi_0$ ne représente pas le flux du champ $\overrightarrow{B}$ à travers le circuit d'induit !

> [!note] Fonctionnement d'une machine idéale : Machine à $N$ conducteurs actifs
> Dans une machine réelle, le nombre $N$ de conducteurs actifs est élevé (de l'ordre de la centaine). Le choix du nombre de collecteurs et la méthode de branchement des différents conducteurs font que la f.e.m. aux bornes du moteur ne présente plus qu'une légère ondulation.
> Pour diminuer l’intensité qui les traverse, les conducteurs actifs sont répartis en $2a$ voies d’enroulement identiques assemblées en parallèle. Chaque voie comporte $\frac{N}{2a}$ conducteurs en série dont les f.e.m. s’ajoutent. Pour un courant $i$ débité, l’intensité à travers chaque conducteur vaut $\frac{i}{2a}$.
> Cela permet à une génératrice de débiter des courants importants sans risque d’échauffement excessif de son circuit d’induit.
> La f.e.m. de la machine, égale à la f.e.m. totale de chacune des voies, est proportionnelle à la vitesse de déplacement des conducteurs, donc à $\omega$. L’analogie avec le cas simple de la spire unique nous amène à poser $e = \Phi_0\omega$ avec $\Phi_0 = k\Phi$, constante positive homogène à un flux.
> - $\Phi_0$, *flux utile sous chacun des pôles*, est le flux du champ $\overrightarrow{B}$ à travers chaque pôle de l’inducteur. $k$, constante de construction de la machine, dépend, entre autres, du bobinage des conducteurs actifs.
> - La constante $\Phi_0$ est par convention positive ; il suffit pour cela de choisir en conséquence le sens positif d’orientation du circuit d’induit ou de la rotation.
> 
> ==**La f.e.m. $e$ d’une machine à courant continu est proportionnelle à sa vitesse de rotation : $e = \Phi_0\omega$, avec $\Phi_0 = k\Phi$ constante positive homogène à un flux.**==
> ==**$\Phi$, flux utile sous chacun des pôles, est proportionnel au champ créé par l’inducteur et k est la constante de construction de la machine.**==

> [!note] Fonctionnement d'une machine idéale : Expression du couple électromagnétique
> - Conventions d'orientation pour un moteur : L'effet des forces de Laplace sur les conducteurs actifs (cf. [[#^par1|paragraphe précédent]]) se traduit par un couple $\Gamma(t)$ appliqué au rotor, appelé **couple électromagnétique du moteur**. De l’analyse menée au [[#^par1|paragraphe précédent]], nous retenons que, lorsque le couple $\Gamma$ et la vitesse de rotation $\omega$ sont positifs, alors la f.e.m. $e$ est positive et le courant $I$ est négatif. Pour que les grandeurs $\Gamma, \omega, e, i)$ soient toutes positives lors du fonctionnement nominal, nous adoptons, pour les moteurs, une convention d'orientation spécifique où l'orientation du courant $i(t)$ est opposée à celle de la f.e.m. $\Phi_0\omega$. Le schéma équivalent d’un moteur idéal (d’inductance et de résistance négligeables) est représenté sur la [[#^figure13|figure 13]].
> 	- Bilan de puissance : Pour un conducteur filiforme siège d’une f.e.m. d’induction de déplacement $e_L$ orientée dans le sens du courant $i$ qui le traverse, la puissance des efforts de Laplace est : $\mathcal{P}_L = -e_Li$ (cf. [[08-Conversions électromagnétiques de puissance|chapitre 8]]).
> 		- Évaluons la puissance $\mathcal{P}_L$ des actions de Laplace pour une machine dont l’induit est constitué de $2a$ voies identiques en parallèle.
> 		Les $\frac{N}{2a}$ conducteurs d’une même voie, en série, forment un conducteur unique parcouru par un courant d’intensité $\frac{i}{2a}$ ; la f.e.m. totale de la voie (égale à celle du moteur), **orientée dans le sens de i** est, d’après nos conventions d’orientation ([[#^figure13|fig. 13]]) : $e_L = -\Phi_0\omega$. La puissance des efforts de Laplace sur les conducteurs d’une voie est donc égale à $-\frac{e_Li}{2a} = \frac{\Phi_0\omega i}{2a}$.
> 		Pour les $2a$ voies, la puissance totale est donc : $\mathcal{P}_L = 2a\times\frac{\Phi_0\omega i}{2a} = \Phi_0\omega i$.
> 		- Les conducteurs, solidaires du rotor, forment un solide en rotation de vitesse angulaire $\omega$ autour de l'axe fixe $(Oz)$. Les actions de Laplace, de moment $\Gamma$ ont donc une puissance $\mathcal{P}_L = \Gamma\omega$.
> 		- Identifions les deux expressions de $\mathcal{P}_L$, on obtient $\Gamma = \Phi_0 i$.
> 
> 	==**Le moment du couple électromagnétique $\Gamma$ d'une machine à courant continu est proportionnel au courant d’induit $i$ : $\Gamma = \Phi_0 i$.**==
> 	==**La même constante $\Phi_0$ intervient dans les deux termes du couplage électromécanique : $\Gamma = \Phi_0 i$ et $e = \Phi_0\omega$.**==

> [!note] Fonctionnement d'une machine idéale : Modes de fonctionnement de la machine
> Nous distinguerons alors les trois modes de fonctionnement :
> - $\Gamma\omega > 0$. La machine reçoit de l’énergie électrique et fournit de l’énergie mécanique : elle fonctionne en moteur ;
> - $\Gamma\omega < 0$. La machine reçoit de l’énergie mécanique et fournit de l’énergie électrique : elle fonctionne en génératrice ;
> - $\Gamma\omega = 0$. La machine fonctionne à vide, c’est-à-dire qu’elle n’entraîne aucune charge mécanique : elle n’est ni moteur ni génératrice. Ce mode de fonctionnement n’est possible que si les pertes sont négligées, Dans ces conditions, en régime permanent il n’est pas nécessaire de disposer d’un couple moteur pour maintenir la vitesse constante.

> [!note] Les machines réelles :
> Le comportement des machines réelles présente des écarts par rapport à celui des machines idéales. Nous allons en examiner succinctement les causes.
> - Notions sur un câblage de l'induit : La [[#^figure2|figure 2]] permet de visualiser la complexité du câblage de l’induit. Le nombre N de conducteurs actifs est généralement très grand de l’ordre de plusieurs centaines, Ce nombre N est souvent un multiple de 4, ceci afin de pouvoir faire participer le maximum de conducteurs actifs à chaque instant : nous ne justifierons pas cette affirmation.
> Lors du bobinage, les « spires » ne sont pas rigoureusement planes : supposons qu’il y ait $N = 2k$ encoches ($k$ étant pair), le fil sortant de l’encoche $p$ ne « repartira » pas par l’encoche $p + k$, mais par $p + k + 1$ ([[#^figure14|fig. 14]]).
> Sur la [[#^figure14|figure 14]], nous avons mis en traits pleins les fils placés devant l’induit, et en pointillé, ceux placés derrière. Un conducteur actif sur deux est relié aux lames du collecteur comme l'indique la [[#^figure15|figure 15]].
> Sur la [[#^figure16|figure 16]] nous avons mis en évidence le passage du courant en cas de fonctionnement « moteur ». Étudions ce qui se passe au cours d’une rotation de l’induit. Nous remarquons qu’avec ce bobinage, le moment des forces de Laplace est toujours moteur ; les variations de ce moment seront d’autant plus atténuées que le nombre N de conducteurs actifs est grand.
> Remarque : Le bobinage proposé n’est qu’un exemple ; chaque constructeur garde secrètement sa propre méthode de bobinage.


# Diagrammes
Conversions électromécaniques réalisées par une machine à courant continu
![[electronique2/attachments-electronique2/figure226.png]]^figure1

![[electronique2/attachments-electronique2/figure228.png]]
a. Structure d’une machine bipolaire à courant continu. b. Structure interne d’une machine tétrapolaire. (1) : culasse d’acier moulé ; (2) : socle ; (3) : axe de l’induit ; (4) : noyau de fer de l’induit ou rotor ; (5) : entrefer ; (6) : bobinage inducteur ou statorique ; (7) : pièces polaires du stator ; (8) : axe des pôles (axe de symétrie) ; (9) : ligne neutre (axe d’antisymétrie) ; (10) : encoches taillées le long des génératrices du rotor ; (11) : collecteur ; (12) : balai ; (13) : ligne de champ ; (14) : épanouissement polaire. ^figure3

Représentation d'une machine à courant continu. a. À circuit inducteur. b. À aimant permanent
![[electronique2/attachments-electronique2/figure229.png]]^figure4

Différents types de machines à courant continu. a. Machine à excitation indépendante. b. Machine à excitation série. c. Machine à excitation parallèle (ou shunt)
![[electronique2/attachments-electronique2/figure230.png]]^figure5

a. Orientation du champ magnétique dans l'entrefer. b. Champ magnétique dans l'entrefer
![[electronique2/attachments-electronique2/figure231.png]]^figure6

Mise en évidence du champ électromoteur de part et d'autre de la ligne neutre
![[electronique2/attachments-electronique2/figure232.png]]^figure7

Mise en évidence de la force de Laplace
![[electronique2/attachments-electronique2/figure233.png]]^figure8

Machine bipolaire à une seule spire
![[electronique2/attachments-electronique2/figure234.png]]^figure9

Vue "de dessus"
![[electronique2/attachments-electronique2/figure235.png]]^figure10

Situation pour $\theta$ compris entre $\pi$ et $2\pi$
![[electronique2/attachments-electronique2/figure236.png]]^figure11

Convention d'orientation de la f.e.m. pour une machine idéale à courant continu à caractère moteur
![[electronique2/attachments-electronique2/figure238.png]]^figure13

Bobinage de l'induit $(N = 12\, ; k = 6)$
![[electronique2/attachments-electronique2/figure239.png]]^figure14

Un conducteur actif sur deux est relié aux lames du collecteur
![[electronique2/attachments-electronique2/figure240.png]]^figure15

![[electronique2/attachments-electronique2/figure241.png]]^figure16
# Graphiques
![[electronique2/attachments-electronique2/figure227.png]]
Moteur à courant continu (moteur 6 volts d’essuie-glace de 2 CV Citroën)
a. Vue sur l’induit : bien remarquer la place des fils dans les encoches de l'induit.
Le circuit magnétique est feuilleté ; ce feuilletage limite les pertes par courants de Foucault au démarrage du moteur.
b. Vue sur le bobinage de l’induit avec le passage des fils dans les encoches de l'induit.
Les deux charbons ont été écartés pour mieux visualiser l’induit.
c. Vue sur le circuit électrique de l'inducteur. Le matériau ferromagnétique est feuilleté.
d. Vue sur le collecteur, avec les différents circuits de l’induit et l’espace du bobinage.
e. Visualisation du circuit de l’induit (avec le collecteur et les charbons ou balais) et de la forme des pièces polaires. ^figure2

Évolution du champ $B(\theta)$ vu par le fil $MN$ et de la f.e.m. $e$ du moteur
![[electronique2/attachments-electronique2/figure237.png]]^figure12
# Expériences

# Autres notes
