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
# Expériences

# Autres notes
