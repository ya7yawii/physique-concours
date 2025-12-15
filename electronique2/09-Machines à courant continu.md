---
titre: "[[09-Machines à courant continu]]"
tags:
  - machine-à-courant-continu
  - inducteur
  - induit
  - dispositif-de-commutation
  - conducteur-actif
  - couple-électromagnétique
  - moteur-à-excitation-indépendante
  - génératrice
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

> [!note] Les machines réelles : Notions sur les pertes
> - Les pertes électriques : Elles se produisent par effet Joule dans les circuits électriques de l’inducteur et de l’induit ainsi qu’au niveau des contacts collecteur-balais.
> L’échauffement qui en résulte est réduit par ventilation forcée. Dans ces conditions, la résistance des circuits n’augmente que de 15 % à 30 %.
> - Les pertes fer : Le rotor est en rotation dans le champ magnétique intense de l’inducteur. Le champ magnétique en un point de celui-ci varie au cours du temps à la fréquence de rotation du moteur.
> Le moteur présente donc des pertes semblables à celles dans la carcasse d’un transformateur, dues aux pertes par hystérésis et par courants de Foucault.
> On réduit les pertes par hystérésis en utilisant des matériaux à cycle d’hystérésis étroit et celles par courants de Foucault en utilisant des matériaux de forte résistivité (tôles de silicium, ...), feuilletés ([[#^figure2|fig. 2a]]). (cf. H-Prépa, Électromagnétisme, $2^{e}$ année, chapitres 7 et 8).
> - Les pertes de commutation : Lors de la commutation d’une spire, le courant qui la traverse subit une brusque variation.
> Une f.e.m. d’induction apparaît dans la spire et provoque une étincelle entre le balai et la lame du collecteur ([[#^figure2|fig. 2b]]) qu’il vient de quitter. Cette étincelle détruit les contacts et dissipe de l’énergie.
> Ce phénomène est atténué à l’aide de dispositifs de commutation auxiliaire.
> - Les pertes mécaniques : Elles sont principalement dues au contact des balais sur le collecteur (sensiblement proportionnelles à la vitesse de rotation) et à la liaison rotor-bâti. Le rendement d’une machine réelle à courant continu est de l’ordre de 80 % à 95 %, ce qui est excellent comparativement aux rendements des machines thermiques (de l'ordre de 30 % à 40 % pour une centrale thermique).

> [!note] Moteur à excitation indépendante : Généralités
> Ce type de moteur nécessite deux alimentations indépendantes ($u_e$, $i_e$) et $(u, i)$ ([[#^figure17|fig. 17]]), Cet inconvénient est compensé par la possibilité de choisir le sens de rotation du moteur en inversant simplement le sens des branchements d’une de ses deux alimentations afin d’inverser l'un des deux courants $i_e$ ou $i$.
> Pour les autres moteurs (série ou parallèle), l’inversion du sens de rotation nécessite de modifier le sens des connexions entre inducteur et induit ([[#^figure18|fig. 18]]).

> [!note] Moteur à excitation indépendante : Équations d'un moteur à flux constant
> Le flux inducteur $\Phi$ ne dépend que du courant dans l'inducteur, Pour travailler à flux constant, il suffit de fixer l’intensité $I_e$ dans l’inducteur. Soit $L$ et $R$ respectivement l’inductance et la résistance de l’induit du moteur ([[#^figure19|fig. 19]]).
> ==**À flux constant, lorsque l’induit est alimenté sous la tension $u(t)$, le courant d’induit $i(t)$ est donné par l’équation électrique : $u(t) = L\dfrac{di(t)}{dt} + Ri(t) + \Phi_0\omega(t)$.**==
> Notons par $J$ le moment d’inertie du rotor et de la charge mécanique et par $\Gamma_r$ le moment résistant opposé par les frottements et la charge mécanique. Nous considérerons ici que $\Gamma_r$ est une fonction de la seule variable $\omega$ notée $\Gamma_r(\omega)$.
> ==**La vitesse du rotor est donnée par l'équation mécanique : $J\dfrac{d\omega(t)}{dt} = \Phi_0i(t) - \Gamma_r(\omega)$.**==
> Éliminons $i(t)$ entre les deux équations précédentes. De l’équation mécanique, il vient : $i(t) = \frac{1}{\Phi_0}\left[J\dfrac{d\omega}{dt} + \Gamma_r(\omega)\right]$, ce qui, porté dans l'équation électrique, donne, après multiplication par $\Phi_0$, l'équation différentielle du moteur : $LJ\dfrac{d^{2}\omega(t)}{dt^{2}} + \left[RJ + L\dfrac{d\Gamma_r(\omega)}{d\omega}\right]\dfrac{d\omega}{dt} + \Phi_{0}^{2}\omega + R\Gamma_r(\omega) = \Phi_0u(t)$.
> ==**Un moteur à excitation indépendante et à flux constant est un système d'ordre 2.**==
> Ce système n'est linéaire que si le moment du couple résistant est une fonction affine de la vitesse : $\dfrac{d\Gamma_r(\omega)}{d\omega} = K_r$.
> Lorsque les phénomènes d'induction propres au circuit d'induit sont négligeables, il est pertinent de négliger l'inductance du circuit d'induit $(L \approx 0)$.
> L'équation du moteur devient alors : $RJ\dfrac{d\omega}{dt} + \Phi_{0}^{2}\omega + R\Gamma_r(\omega) = \Phi_0u(t)$.
> ==**Le moteur à excitation indépendante et à flux constant se comporte souvent comme un système linéaire d'ordre 1.**==

> [!note] Moteur à excitation indépendante : Démarrage du moteur
> C'est le terme de moment $\Gamma_r(0)$ qui s'oppose au démarrage du moteur. Pour que ce dernier puisse démarrer, il faut que : $\Phi_0u(0) - R\Gamma_r(0) > 0$, c'est-à-dire qu'à l'instant initial, la relation d'induit doit être supérieure à la tension de démarrage $U_d$ : $u(0) > \frac{R\Gamma_r(0)}{\Phi_0} = U_d$.
> Le fonctionnement avec une tension d’alimentation au voisinage de la valeur de démarrage est utilisé dans les engins de levage.
> Si l’induit est alimenté, dès le démarrage, sous sa tension nominale $U_n$ (qui est très supérieure à la tension de démarrage $U_d$), une intensité $i(t)$, très supérieure à la valeur nominale $I_n$ du courant d’induit, traverse le moteur lors de sa mise en vitesse.
> Cette surintensité provoque un choc mécanique sur le rotor et un échauffement excessif, souvent destructeur, dans le circuit d’induit.
> ==**La mise en vitesse du moteur doit se faire sous tension d’induit $u(t)$ réduite en limitant le courant $i(t)$ qui le traverse.**==
> Pour cela, on peut brancher, en série avec le circuit d’induit, un rhéostat dont on diminue ensuite la résistance pour la mise en vitesse du moteur.
> Ce procédé n’est envisageable que pour des moteurs de faible puissance dont la phase de démarrage est courte. En outre, il est peu économique à cause de la puissance perdue par effet Joule dans le rhéostat.
> Une solution plus satisfaisante se fait en appliquant à l’induit une tension $u(t)$ croissante en utilisant un générateur de rampe de tension.

> [!note] Moteur à excitation indépendante : Point de fonctionnement du moteur
> Le point de fonctionnement d’un moteur concerne un régime établi. À flux constant et en régime permanent (tension $u$ d’induit et vitesse $\omega$ du rotor constantes), l’induit est un dipôle linéaire qui satisfait à la relation : $U = E + RI$ avec $E = \Phi_0\omega$ et $\Gamma = \Phi_0I$.
> Remplaçons $E$ et $I$ dans la première relation : $U = \Phi_0\omega + \frac{R}{\Phi_0}\Gamma$, d'où l'expression du moment des forces magnétiques en fonction de $\omega$ : $\Gamma(\omega) = \frac{\Phi_0}{R}(U - \Phi_0\omega)$ et sa représentation est donnée sur la [[#^figure20|figure 20]].
> En régime établi, le moment du couple électromagnétique $\Gamma(\omega)$ est opposé à celui du couple résistant $-\Gamma_r(\omega)$ dû à la charge mécanique et aux frottements. La vitesse $\omega$ du moteur est solution de : $\Gamma_r(\omega) = \frac{\Phi_0}{R}(U - \Phi_0\omega)$.
> ==**Le point de fonctionnement d’un moteur en régime établi se trouve à l'intersection de la caractéristique de son couple électromagnétique $\Gamma(\omega) = \frac{\Phi_0}{R}(U - \Phi_0\omega)$ et celle $\Gamma_r(\omega)$ de sa charge mécanique et des frottements.**==
> **En charge et en régime établi**, la relation entre le couple résistant $-\Gamma_r$ et la vitesse du moteur peut s'écrire : $\omega = \frac{1}{\Phi_0}\left(U - \frac{R}{\Phi_0}\Gamma_r\right)$.
> Il apparaît ainsi que :
> - la vitesse $\omega$ du moteur, en régime établi, est une fonction décroissante du moment $\Gamma_r$ du couple résistant.
> Lorsque $\Gamma_r$ augmente, la vitesse décroit jusqu’à s’annuler lorsque le moment du couple résistant vaut $\Gamma_{r\,max} = \frac{\Phi_0U}{R}$.
> Remarquons que la valeur de $\Gamma_{r\,max}$ est celle **du moment du couple de démarrage** $\Gamma_d = \Gamma(0)$. Le moment du couple de démarrage est maximum et égal à $\Gamma_d = \Gamma_{r\,max} = \frac{\Phi_0U}{R}$.
> ==**La valeur de $\Gamma_{r\,max}$ est celle du moment du couple de démarrage $\Gamma_d$. Un moteur à excitation indépendante peut donc démarrer avec sa charge nominale puisque le moment résistant exercée par celle-ci est nécessairement inférieur à $\Gamma_d$.**==
> - $U$ et $\Gamma_r$ étant constants, $\omega$ en régime établi dépend de $\Phi_0$ et sa valeur passe par un maximum $\omega_M = \frac{U^{2}}{4R\Gamma_r}$ pour $\Phi_0 = \Phi_{0M} = \frac{2R\Gamma_r}{U}$.
> En fonction de la puissance mécanique nominale $\mathcal{P}_N = \omega_N\Gamma_r$ : $\frac{\omega_M}{\omega_N} = \frac{U^{2}}{4R\mathcal{P}_N}$.
> Ce rapport est en général très supérieur à 1.
> Si, à partir des conditions nominales d'utilisation, nous diminuons le flux inducteur $\Phi$, la vitesse angulaire $\omega$ commence par augmenter et passe par un maximum qui peut être très largement supérieur à la vitesse nominale ([[#^figure21|fig. 21]]).
> ==**Il ne faut jamais supprimer l'alimentation de l’inducteur lorsque l'induit est sous tension, car le moteur en s’emballant risque d’être détruit.**==

> [!note] Moteur à excitation indépendante : Bilan de puissance
> Pour l'état de charge considéré, le moteur reçoit la puissance électrique des alimentations de l’inducteur et de l’induit $\mathcal{P}_a = U_eI_e + UI$ et fournit la puissance mécanique $\mathcal{P}_M = \Gamma_M\omega$, où $\Gamma_M$ est le couple utile (ou couple moteur disponible sur l'arbre moteur ([[#^figure22|fig. 22]])).
> Son rendement est $\eta = \frac{\mathcal{P}_M}{\mathcal{P}_a}$.
> Les phénomènes d’induction dans l’inducteur peuvent être négligés. Toute la puissance qui lui est fournie est alors dissipée par effet Joule.
> Les pertes s’analysent en :
> - pertes par effet Joule dans l’inducteur et dans l’induit: $\mathcal{P}_J = U_eI_e + RI^{2}$, où $R$ est la résistance de l’induit dans les conditions d’utilisation. Ces pertes sont souvent appelées pertes cuivre ;
> - pertes collectives $\mathcal{P}_c$ de nature magnétique (hystérésis et courants de Foucault dites encore pertes fer) et mécanique (frottements).
> L'expression de la puissance mécanique du moteur s’établit à : $\mathcal{P}_M = \mathcal{P}_a - \mathcal{P}_J - \mathcal{P}_c = UI - (RI^{2} + \mathcal{P}_c)$ et celle du rendement à $\eta = \frac{\mathcal{P}_M}{\mathcal{P}_a} = \frac{UI - RI^{2} - \mathcal{P}_c}{U_eI_e + UI}$.
> 
> Une méthode de mesure utilisée est celle dites des pertes séparées.
> La puissance des pertes par effet Joule est déterminée à partir de la connaissance de la résistance des circuits et de l’intensité qui les traverse.
> La puissance des pertes collectives est déterminée par un **essai à vide** (sans charge mécanique) avec les mêmes valeurs de flux $\Phi$ de vitesse $\omega$ que lors du fonctionnement en charge, afin d’avoir les mêmes pertes magnétiques et mécaniques. Lors de cet essai, on démontre que la puissance des pertes collectives est donnée par la relation: $\mathcal{P}_c = U_vI_v$, où $U_v$ et $I_v$ sont respectivement la tension et le courant à vide de l’induit.

> [!note] Modélisation d'un moteur à excitation indépendante
> Pour étudier le comportement d'un moteur, ainsi que pour l'asservir ou pour le réguler, il est indispensable de le modéliser.
> Le moteur à excitation indépendante sera analysé comme un opérateur linéaire : $\Omega(p) = f(U(p), \Gamma_m(p))$, où $\Omega(p)$, $U(p)$ et $\Gamma_m(p)$ sont les notations fonctionnelles de sa vitesse, de sa tension d’induit et du couple qu’il exerce sur la charge mécanique.
> Déterminons le schéma fonctionnel d'un moteur à excitation indépendante pour lequel :
> - $\Phi_0$ est la constante de couplage électromécanique ;
> - $R$ la résistance de l’induit, $L$ l'inductance de l'induit ;
> - $J$ le moment d’inertie du rotor et de la charge mécanique entraînée ;
> - $\Gamma_f$ le moment du couple résistant dû aux fonctionnements internes au moteur supposé de la forme $\Gamma_f = -h\omega$.
> 
> Pour ce faire, notons par $E(p)$ la f.e.m. de l’induit, $I(p)$ son courant et $U(p)$ sa tension d’alimentation. L’équation électrique du moteur est : $U(p) = LpI(p) + RI(p) + E(p)$.
> Il en résulte que le courant d’induit est : $I(p) = \frac{1}{R + Lp}[U(p) - E(p)] = K_e(p)[U(p) - E(p)]$.
> Cette relation peut être traduite par un comparateur recevant sur ses entrées inverseuse et non inverseuse respectivement les signaux $E(p)$ et $U(p)$, et un bloc fonctionnel de transmittance $K_e(p) = \frac{1}{R + Lp}$ délivrant le signal $I(p)$ ([[#^figure23|fig. 23]]).
> $K_e(p)$ correspond à un passe-bas d’ordre 1 de constante de temps $\tau_e = \frac{L}{R}$. Ce courant d’induit crée un moment moteur $\Gamma(p) = \Phi_0I(p)$, d'où le bloc fonctionnel de transmittance $\Phi_0$.
> L'équation mécanique du moteur est $Jp\Omega(p) = \Gamma(p) - \Gamma_m(p) - h\Omega(p)$.
> La vitesse du moteur est donnée par : $\Omega(p) = \frac{1}{h + Jp}[\Gamma(p) - \Gamma_m(p)] = K_m(p)[\Gamma(p) - \Gamma_m(p)]$.
> Cette équation mécanique du moteur se représente à l’aide d’un comparateur et d’un bloc fonctionnel de transmittance $K_m(p) = \frac{1}{h + Jp}$.
> $K_m(p)$ correspond à un passe-bas d’ordre 1 de constante de temps $\tau_m = \frac{J}{h}$.
> La vitesse crée une f.e.m. $E(p) = \Phi_0\Omega(p)$ qui est réinjectée sur l’entée inverseuse du comparateur. Cela est représenté par la chaîne de retour de transmittance $\Phi_0$ ([[#^figure23|fig. 23]]).
> ==**Le moteur est un système électrique passe-bas d'ordre 1, de constante de temps $\tau_e = \frac{L}{R}$, associé à un système mécanique passe-bas d’ordre 1, de constante de temps $\tau_m = \frac{J}{h}$.**==
> Lorsque les effets d’induction propres au circuit de l’induit sont négligés $(L = 0)$, $\tau_e$ est très inférieur à $\tau_m$.
> La fonction de transfert $K_e(p) = \frac{I(p)}{U(p) - E(p)} = \frac{1}{R}$ devient constante ([[#^figure24|fig. 24]]).

> [!note] Génératrice
> - Caractère inversible (ou « réversible ») d’une machine à courant continu : Le caractère réversible d’une machine à courant continu peut être utilisé dans deux cas :
> 	- le freinage du moteur avec ou sans récupération d'énergie ;
> 	- l’obtention d’une tension continue à l'aide d’une génératrice.
> - Freinage d’une machine : Si la tension $u$ devient inférieure à la f.e.m. $e = \Phi_0\omega$, le courant $i$ change de sens. Le couple $\Gamma$ est alors opposé à la vitesse et le moteur se comporte donc comme un frein.
> Le freinage par inversion du sens du courant dans un moteur est souvent utilisé.
> En général, le moteur est branché sur une résistance capable de dissiper une forte puissance pendant la phase de freinage (cas des moteurs de machine à laver en fin d’essorage,..., des motrices de T.G.V.).
> La récupération nécessite que la f.e.m. moteur soit supérieure à la tension du réseau, Ceci peut être obtenu soit en jouant sur le couplage des induits de plusieurs moteurs, soit en utilisant des hacheurs survolteurs pour transmettre de l'énergie au réseau électrique. Elle n’est donc intéressante que si les phases de freinage se reproduisent souvent (cas du métro, mais pas des T.G.V.).
> - Génératrices tachymétriques : Les génératrices à excitation indépendante ne sont plus guère utilisées, sauf en capteurs linéaires de vitesses angulaires, c’est-à-dire en génératrices tachymétriques. Ces génératrices sont des machines de faible puissance à aimants permanents qui fonctionnent, par construction, à flux constant.
> Le rotor de la génératrice ([[#^figure25|fig. 25]]) étant entraîné à la vitesse $\omega(t)$, la tension $u(t)$ délivrée par la machine est une image exacte de la vitesse de rotation de son rotor si l’induit est en circuit ouvert $(i(t) = 0)$.
> En effet, dans ces conditions, on a : $u(t) = e(t) = \Phi_0\omega(t)$.
> La charge électrique d'une génératrice doit être aussi élevée que possible, sinon infinie. Ce faisant, le couple électromagnétique opposé à la rotation par la génératrice $((\Gamma(t) = \Phi_0i(t)) \approx O)$ est quasiment nul : le capteur ne perturbe que faiblement (uniquement par le couple de ses forces de frottement) le système auquel il est associé.
> ==**À flux constant et à charge électrique élevée $(i = 0)$, la fonction de transfert d’une génératrice tachymétrique est : $H(p) = \frac{E(p)}{\Omega(p)} = \Phi_0$.**==
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

Pour inverser le sens de rotation d'un moteur à excitation indépendante, il suffit d'inverser le sens d'une de ses deux alimentations
![[electronique2/attachments-electronique2/figure242.png]]^figure17

Pour inverser le sens de rotation d'un moteur série, il faut modifier le sens des connexions entre inducteur et induit
![[electronique2/attachments-electronique2/figure243.png]]^figure18

Schéma équivalent et conventions d'orientation d'un moteur à courant continu vu entre les bornes de l'induit : $u(t) = L\dfrac{di(t)}{dt} + Ri(t) + \Phi_0\omega(t)$
![[electronique2/attachments-electronique2/figure244.png]]^figure19

Diagramme des puissances dans un moteur
![[electronique2/attachments-electronique2/figure247.png]]^figure22

Schéma fonctionnel d'un moteur à excitation indépendante
![[electronique2/attachments-electronique2/figure248.png]]^figure23

Schéma fonctionnel d'un moteur à excitation indépendante dont les effets d'induction propres au circuit de l'induit sont négligés
![[electronique2/attachments-electronique2/figure249.png]]^figure24

Utilisation d'une machine à courant continu en génératrice et son schéma électrique équivalent
![[electronique2/attachments-electronique2/figure250.png]]^figure25
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

Caractéristique mécanique d'un moteur à courant continu à flux inducteur constant
![[electronique2/attachments-electronique2/figure245.png]]^figure20

Vitesse de rotation en fonction du flux $\Phi_0$, à $U$ et $\Gamma_r$ constants. $\omega_M = \frac{U^{2}}{4R\Gamma_r}$ est en général très grand devant $\omega_N$
![[electronique2/attachments-electronique2/figure246.png]]^figure21
# Expériences
> [!warning]
> Voici des exemples de travaux pratiques qui abordent le sujet de ce chapitre : [lien 1](https://fr.scribd.com/document/463923841/TP2-1), [lien 2](https://www.espacetechnologue.com/wp-content/uploads/2017/03/tp-electrotechnique.pdf), [lien 3](https://staff.univ-batna2.dz/sites/default/files/rebbouh_sonia/files/tp_ndeg1.pdf), [lien 4](https://lycee-champollion.fr/IMG/pdf/tp_no20_moteur_a_courant_continu.pdf), [lien 5](https://fr.scribd.com/document/435882840/TP-N-5-Moteur-a-exc-independante-GE-Inge-uas), [lien 6](https://www.studocu.com/row/document/universite-batna-2/tp-machines-electriques-approfondies/tp-n03-moteur-a-courant-continu-elm-s5-20-21-1-1/53255893), [lien 7](http://archive.univ-biskra.dz/moodle2023/pluginfile.php/661620/mod_resource/content/1/TP%20generatrice%20%20a%20courant%20continu%20a%20excitation%20separee.pdf), [lien 8](https://fr.scribd.com/document/832698386/tp01elt), [lien 9](https://fr.scribd.com/document/645584111/TP-N-02-GENERATRICE-A-COURANT-CONTINU).
# Autres notes
