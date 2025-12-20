---
titre: "[[11-Conversion électronique statique]]"
tags:
aliases:
crée: 17-12-2025, 11:06
---
# Formules

# Définitions
==**Convertisseur statique**== :
Un convertisseur statique est un convertisseur utilisant des interrupteurs électroniques : il n'y a aucune conversion électromécanique.

> [!note] Conversion de puissance en continu
> - Puissance mises en jeu : L’électronique dite de puissance correspond à des puissances mises en jeu, de la centaine de watts à plusieurs centaines de kilowatts.
> 	- L'alimentation d’un micro-ordinateur ou d’une chaîne haute fidélité correspond à une puissance de 100 W à 500 W environ, celle d’un petit moteur (perceuse électrique, moteur de machine à laver) à une puissance de 500 W à 2 kW.
> 	- A l'autre extrémité de l’échelle des puissances, une motrice de T.G.V. consomme une puissance pouvant aller jusqu’à 8 MW sous 25 kV. Les moteurs utilisés dans l'industrie, les émetteurs de télédiffusion et les sonorisations de concerts correspondent couramment à des puissances de 100 kW.
> - Principe de la conversion de puissance : Imaginons un générateur continu et une charge adaptés. **Comment fournir à la charge une puissance réglable de zéro à sa valeur maximale avec un bon rendement ?**
> Ce problème est celui de la conversion de puissance en continu.
> Prenons le cas d’une charge résistive. Le plus simple est d’utiliser un rhéostat ([[#^figure1|fig. 1]]). Ce montage utilisable pour de faibles puissances n’est pas envisageable pour des puissances élevées : son rendement est très faible dès que la tension réglable est nettement inférieure à la tension d’alimentation.
> Une autre technique est de « hacher » la puissance délivrée par le générateur à la charge à l’aide d’un interrupteur ouvert et fermé de manière cyclique. La puissance est alors convertie sans pertes, car un interrupteur fonctionne en « tout ou rien » : soit la tension à ses bornes est nulle (interrupteur fermé), soit l’intensité le traversant est nulle (interrupteur ouvert).
> Dans les deux cas, la puissance qu’il dissipe est nulle.
^par1

> [!note] Conversion de puissance en continu
> - Principe du "hacheur" : Utilisons la technique envisagée au [[#^par1|paragraphe précédent]].
> L'interrupteur de [[#^figure2|figure 2]], appelé **hacheur**, « découpe » la tension continue. Il fonctionne à fréquence fixe avec une durée de conduction variable. Le rapport cyclique $\alpha$ est défini comme le rapport de cette durée sur la période du cycle ([[#^figure3|fig. 3]]).
> Quand l’interrupteur est fermé $u = E$ et $i = \frac{E}{R}$, quand il est ouvert $i = 0$ et $u = 0$. Calculons la puissance $p$ dissipée dans la résistance : $p = \frac{E^{2}}{R}$ quand l’interrupteur est fermé et $p = 0$ quand il est ouvert. Sa valeur moyenne est donc $\langle p \rangle = \frac{\alpha E^{2}}{R}$.
> Ce dispositif fournit une puissance réglable à la charge par une modification du rapport cyclique $\alpha$ avec un rendement égal à 1.
> Remarque : Les valeurs moyennes des grandeurs électriques $u(t)$ et $i(t)$ sont : $\langle u \rangle = \alpha E$ et $\langle i \rangle = \frac{\alpha E}{R}$.
> Nous pourrions penser que ce montage est effectivement équivalent en valeur moyenne à une source de f.e.m. $\alpha E$ alimentant la résistance $R$. Ce n'est pas le cas.
> En effet, la puissance moyenne dissipée dans la résistance est : $\langle p \rangle = \frac{\alpha E^{2}}{R} \neq \langle u \rangle \langle i \rangle$.
> La valeur moyenne d'un produit n'est pas égale au produit des valeurs moyennes.
> - Régime établi de commutation : L’analyse du fonctionnement des montages des figures [[#^figure3|3]] et [[#^figure4|4]] montre que l'interrupteur commandé permet de faire évoluer le système successivement suivant deux régimes différents de durées respectives $\alpha T$ et $(1 - \alpha)T$. Ces deux régimes se succèdent périodiquement puisque le hachage fonctionne à fréquence fixe.
> ==**Nous pouvons généraliser ce résultat aux dispositifs que nous allons étudier :**==
> ==**Les dispositifs de conversion de puissance fonctionnent en régime établi de commutation.**==
> ==**La période $T$ des cycles de fonctionnement est fixée.**==
> ==**La commutation sépare chaque cycle en régimes dont les durées sont régies par le rapport cyclique $\alpha$.**==
> Ainsi les grandeurs physiques, fonction du temps, des intensités et des tensions notamment, sont périodiques de période $T$. Cette propriété est très importante dans l'étude des régimes de commutation.

> [!note] Conversion électronique de puissance : Conversion électronique statique
> Il est impossible d’utiliser des interrupteurs mécaniques dans des hacheurs principalement à cause de leur inertie (ils ne peuvent pas fonctionner à des fréquences supérieures à une dizaine de hertz) et de leur durée de vie (quelques centaines de milliers de cycles au mieux).
> La conversion de puissance par hacheur a vu le jour grâce à la mise au point d'interrupteurs électroniques de puissance fiables dans les années 1960.
> Ceux-ci doivent présenter des caractéristiques adaptées aux circuits dans lesquels ils sont utilisés (tensions extrêmes admissibles de plusieurs kilovolts quand ils sont ouverts, courants extrêmes admissibles de plusieurs centaines d’ampères quand ils sont fermés pour les composants de puissance).
> Dans ce chapitre, nous étudierons le **convertisseur statique continu-continu** ([[#^figure5|fig. 5]]).
> ==**Un convertisseur utilisant des interrupteurs électroniques est appelé convertisseur statique, car il n’y a aucune conversion électromécanique. il est dit continu-continu si la source délivre une tension continue, et si la tension aux bornes de la charge est unidirectionnelle.**==
> D’autres dispositifs permettent une conversion électronique statique :
> - continu-alternatif (**onduleurs**) ;
> - alternatif-continu (**redresseurs**) ;
> - alternatif-alternatif (**gradateurs**).

> [!note] Conversion électronique de puissance : Interrupteurs idéaux
> Un interrupteur électronique idéal présente une caractéristique $u = 0$ quand il est fermé, et $i= 0$ quand il est ouvert. Son ouverture et sa fermeture peuvent être commandées ou naturelles ([[#^figure6|fig. 6]]).
> Le fonctionnement dans les quatre quadrants (($i \geqslant 0$, $u \geqslant 0$), ($i \geqslant 0$, $u \leqslant 0$), ($i \leqslant 0$, $u \geqslant 0$), ($i \leqslant 0$, $u \leqslant 0$)) n’est en général pas nécessaire.
> Un interrupteur, dont la caractéristique est tronquée, est dit unidirectionnel : sa caractéristique quand il est fermé se limite, par exemple, à $u = 0$ et $i > 0$ et quand il est ouvert à $i = 0$ et $u > 0$, soit un fonctionnement limité au domaine ($i \geqslant 0$, $u \geqslant 0$). Le fonctionnement en dehors de ce domaine n’est pas prévu ; s’il est imposé a l’interrupteur, il provoque souvent sa destruction.
> En majorité, les éléments de commutation sont unidirectionnels de caractéristique limitée à ($i \geqslant 0$, $u \geqslant 0$) ou ($i \geqslant 0$, $u$ quelconque).

> [!note] Conversion électronique de puissance : Interrupteurs usuels
> Présentons quelques composants usuels dans leur modélisation idéale.
> - La diode ([[#^figure7|fig. 7]]) :
> La diode est un interrupteur à commutation naturelle. Le passage de l’état interrupteur fermé à l'état interrupteur ouvert se produit dès que la tension $u_D$ à ses bornes devient négative. Son fonctionnement est limité à $i \geqslant 0$ et $u \leqslant 0$.
> Les diodes utilisées en commutation peuvent supporter une tension inverse pouvant aller jusqu’à 5000 V et un courant direct d’intensité 5000 A.
> - Le transistor (utilisé en commutation) ([[#^figure8|fig. 8]]) : C’est un interrupteur commandé à l'ouverture et à la fermeture, dont le fonctionnement est limité à $i \geqslant 0$ et $u \geqslant 0$.
> Les transistors sont utilisés pour des commutations à puissance relativement faible (inférieures à 10 kW) et à des fréquences pouvant atteindre 100 kHz. Les transistors I.G.B.T. (Insulated Gate Bipolar Transistor) ou transistors bipolaires à grille isolée ont été développés pour un usage en commutation de puissance (commutation allant jusqu’à des courants de 100 A sous 1000 V).
> - Le thyristor ([[#^figure9|fig. 9]]) : C’est un interrupteur commandé uniquement à la fermeture. L’ouverture se fait naturellement quand la tension à ses bornes devient négative ou l’intensité du courant qui le traverse devient nulle. Son fonctionnement est limité à $i \geqslant 0$, $u$ pouvant prendre un signe quelconque.
> Les thyristors sont utilisés pour des commutations de puissances élevées (100 kW) mais à des fréquences faibles (1 kHz) (commutation allant jusqu’à des courants de 5000 A sous 5000 V).
> Pour assurer un double fonctionnement du thyristor, il doit être accompagné d'un circuit assurant son blocage. Des thyristors particuliers, commandés aussi bien à l’ouverture qu’à la fermeture, ont été développés pour éviter cet inconvénient.
> Nous ne nous préoccuperons pas par la suite du type d’interrupteur commandé utilisé. Nous nous servirons d’un interrupteur unidirectionnel commandé à la fermeture et à l'ouverture utilisable pour $u \geqslant 0$ et $i \geqslant 0$. Son schéma est donné sur la [[#^figure10|figure 10]].
> La représentation de type diode indique le sens du courant en mode passant et le double trait vertical ou oblique signifie que cet interrupteur est commandé à l'ouverture et à la fermeture (H signifie hacheur).

> [!note] Source de courant et de tension en régime commuté
> Nous avons étudié le cas simple de transfert de puissance vers une résistance. Les convertisseurs de puissance sont principalement utilisés sur des moteurs dont le comportement électrocinétique est plus complexe en particulier pendant la commutation des interrupteurs.
> - Généralisation de la notion de source de tension ou de courant : Le fait d'utiliser les interrupteurs commandés fonctionnant à des fréquences de plusieurs kilohertz impose d’étendre les notions de source de courant ou de tension, car le comportement au niveau des commutations est plus important que celui vis-à-vis du régime continu qui n’est jamais atteint.
> Envisageons le montage suivant ([[#^figure11|fig. 11]]).
> Un générateur en créneau de période T et de rapport cyclique $\alpha$, de représentation de Thévenin (f.e.m. $e_g(t) = 0$ ou $E_0$, résistance $R_0$) ou de Norton (c.e.m. $\eta_g(t) = 0$ ou $I_0 = \frac{E_0}{R}$ résistance $R_0$), alimente un dipôle.
> Étudions la tension $u$ et l’intensité $i$ qui traversent le dipôle suivant son type dans quelques cas particuliers ([[#^figure12a|fig. 12a]] et [[#^figure12b|b]]).
> 	- Si le dipôle est une source de tension f.e.m. $E$, la tension $u = E$ est continue et l’intensité $i = \frac{e_g - E}{R}$ discontinue.
> 	- S'il est une source de courant de c.e.m. $\eta$, la tension $u = e_g - R_0\eta$ est discontinue et l’intensité $i = \eta$ continue.
> 	- Si le dipôle est une bobine d’inductance $L$, le flux et donc l'intensité $i$ sont continus.
> 	Le temps caractéristique d’évolution du courant est $\frac{L}{R_0}$.
> 	Si $\frac{L}{R_0} \gg T$, le courant traversant l’inductance est quasiment constant.
> 	- Si le dipôle est un condensateur de capacité $C$, la charge et donc la tension sont continues. Le temps caractéristique d’évolution de tension est $R_0C$.
> 	- Si $R_0C \gg T$, la tension aux bornes du condensateur est quasiment constante.
> 	
> 	Pour traiter de façon semblable des dipôles aux comportements voisins en régime commuté (inductance et source de courant) (condensateur et source de tension), nous choisissons de nouvelles définitions pour les sources.
> 	==**En présence de commutations :**==
> 	- ==**Un dipôle se comporte comme une source de tension si la tension à ses bornes est quasiment constante.**==
> 	- ==**Un dipôle se comporte comme une source de courant si l’intensité qui le traverse est quasiment constante.**==
> 	
> 	==**Une source de tension autorise des variations brusques de courant et, inversement, une source de courant autorise des variations brusques de tension.**==

> [!note] Source de courant et de tension en régime commuté : Lissage de la tension par un condensateur
> Envisageons la mise en parallèle d’un condensateur sur un dipôle dans un réseau siège d’une commutation périodique de période $T$ et de fréquence $f = \frac{1}{T}$ ([[#^figure13|fig. 13]]).
> **Quand le régime établi est atteint**, la tension $u(t)$ et les courants sont des fonctions périodiques du temps.
> - Variation de la tension : Considérons l’amplitude $\Delta u = u_{max} - u_{min}$ de la variation de $u(t)$ au cours d’une période ([[#^figure14|fig. 14]]). Nous pouvons majorer $\Delta u$ : $\Delta u < T\left|\dfrac{du}{dt}\right|_{max}$.
> Comme $i_C = C\dfrac{du}{dt}$ : $\Delta u < \frac{i_{C\,max}}{C}T$ ou $\Delta u < \frac{i_{C\,max}}{fC}$.
> La valeur de $i_{C\,max}$ dépend du dipôle $D$ et du reste du circuit.
> ==**En régime commuté établi, un condensateur atténue les variations de tension à ses bornes et tend à se comporter comme une source de tension. Cette propriété est d’autant mieux vérifiée que sa capacité est grande et que la fréquence de commutation est élevée.**==
> - Intensités : La valeur moyenne de l’intensité dans le condensateur est : $\displaystyle \langle i_C \rangle = \frac{1}{T}\int_{t}^{t+T}i_C(t')dt' = \frac{1}{T}\int_{t}^{t+T}C\dfrac{du}{dt'}dt' = C\frac{u(t+T) - u(t)}{T} = 0$.
> ==**En régime périodique, l’intensité moyenne entrant dans un condensateur est nulle.**==
> 	- La valeur moyenne de l’intensité à travers le dipôle $D$ est donc égale à celle de $i(t)$ : $\langle i_D(t) \rangle = \langle i(t) \rangle$.
> 	- Si le lissage de la tension est suffisant, la tension aux bornes du dipôle $D$ et donc l’intensité $i_D$ qui le traverse, sont pratiquement constantes. Les variations de l’intensité $i(t)$ sont « absorbées » par le condensateur.
> - Transformation ou amélioration d’une source : Examinons les cas où le dipôle $D$ est une source idéale de courant ([[#^figure15|fig. 15]]) ou une source non idéale de tension ([[#^figure16|fig. 16]]).
> Si la capacité $C$ et la fréquence de commutation $f$ sont suffisamment élevées, l'ensemble source et condensateur en parallèle peut être considéré comme une source de tension.
> ==**Si sa capacité est suffisamment grande, un condensateur en parallèle :**==
> 	- ==**transforme une source de courant en source de tension ;**==
> 	- ==**améliore une source de tension non idéale.**==
^par2

> [!note] Source de courant et de tension en régime commuté : Lissage du courant par une inductance
> Étudions maintenant la mise en série d’une inductance avec un dipôle quelconque en régime commuté de période $T$ et de fréquence $f$ ([[#^figure17|fig. 17]]).
> Quand le régime établi est atteint, les tensions $u(t)$, $u_L(t)$ et $i(t)$ sont des fonctions périodiques du temps. On retrouve des résultats analogues à ceux du [[#^par2|paragraphe précédent]].
> - Variation de l'intensité : L’amplitude $\Delta i = i_{max} - i_{min}$ de la variation de $i(t)$ au cours d’une période est majorée par: $\Delta i < T\left|\dfrac{di}{dt}\right|_{max}$ avec $u_L = L\dfrac{di}{dt}$, soit : $\Delta i < \frac{u_{L\,max}}{L}T$ ou $\Delta i < \frac{u_{L\,max}}{fL}$.
> ==**En *régime commuté établi*, une bobine atténue les variations de l'intensité du courant qui la traverse et tend à se comporter comme une source de courant.**==
> ==**Cette propriété est d’autant mieux vérifiée que son inductance est grande et que la fréquence de commutation est élevée.**==
> - Tensions : La valeur moyenne de la tension aux bornes de l'inductance (idéale) est : $\langle u_L \rangle = \frac{1}{T}\int_{t}^{t+T}u_L(t')dt' = \frac{1}{T}\int_{t}^{t+T}L\dfrac{di}{dt'}dt' = L\frac{i(t+T) - i(t)}{T} = 0$.
> ==**En *régime commuté établi*, la tension moyenne aux bornes d'une inductance parfaite est nulle.**==
> 	- La valeur moyenne de la tension aux bornes du dipôle $D$ est donc égale à celle de $u(t)$ : $\langle u_D(t) \rangle = \langle u(t) \rangle$.
> 	- Si le lissage du courant est suffisamment efficace, l'intensité $i$ et donc la tension $u_D$ aux bornes du dipôle $D$ sont pratiquement constantes. Les variations de la tension $u(t)$ sont pratiquement « absorbées » par l'inductance.
> - Transformation ou amélioration d’une source : Examinons les cas où le dipôle $D$ est une source idéale de tension ([[#^figure18a|fig. 18a]]) ou une source non idéale de courant ([[#^figure18b|fig. 18b]]).
> Si l'inductance $L$ et la fréquence de commutation $f$ sont suffisamment élevées, l'ensemble source et inductance en série peut être considéré comme une source de courant.
> ==**Si son inductance est suffisamment grande, une bobine en série :**==
> 	- ==**transforme une source de tension en source de courant ;**==
> 	- ==**améliore les caractéristiques d’une source de courant non idéale.**==

> [!note] Alimentation d'un électromoteur : Conversion de puissance entre une source idéale et un électromoteur
> Si nous négligeons la résistance en série d’un moteur à courant continu, celui-ci peut être considéré comme un électromoteur pur de f.e.m. $E'$. Cherchons comment il est possible de l’alimenter à partir d’une source idéale continue.
> - Le montage de [[#^figure19|figure 19a]] est impossible : à la fermeture de l'interrupteur, la tension à ses bornes, égale à $E - E'$ est non nulle et le courant devient donc infini.
> - Pour alimenter une source de courant, le montage de [[#^figure19|figure 19b]] est impossible : le courant $I_K$ étant toujours égal à $I + I'$, l'ouverture de l'interrupteur entraînerait sa destruction par surtension.
> - En revanche, rien n’interdit le montage sans interrupteur représenté sur la [[#^figure20|figure 20]]. Si les deux électromoteurs sont positifs, la source de courant transfère une puissance $\mathcal{P} = E'I$ vers la source de tension.
> 
> ==**La conversion de puissance ne peut se faire directement que d’une source de tension vers une source de courant et réciproquement.**==

> [!note] Alimentation d'un électromoteur : Alimentation d’une source
> Envisageons, dans un premier temps, le cas de l’alimentation d’une source de courant parfaite de c.e.m. $I$ par une source de tension de f.e.m. $E$ avec le montage de [[#^figure21|figure 21]].
> Le fait que le circuit électrique soit périodiquement ouvert est incompatible avec la présence de la source de courant. En effet, comment le courant $I$ peut-il parcourir un circuit ouvert ?
> Dans la réalité, une différence de potentiel très grande apparaît aux bornes de l’interrupteur et le détruit. Il est donc nécessaire de court-circuiter cette source pendant l'ouverture de l’interrupteur commandé.
> De façon symétrique, un court-circuit du générateur de tension endommagerait le circuit.
> ==**En régime de commutation établi :**==
> - ==**une source de tension ne doit jamais être court-circuitée ;**==
> - ==**une source de courant ne doit jamais être en circuit ouvert.**==
> 
> Considérons la structure à deux interrupteurs de [[#^figure22|figure 22]].
> Quand le premier interrupteur est fermé, le second est ouvert et inversement.
> De cette façon, la source de tension n’est jamais court-circuitée et la source de courant n’est jamais en circuit ouvert.
> À partir du chronogramme de [[#^figure23|figure 23]], nous remarquons que la tension moyenne aux bornes de la source de courant est $\langle u \rangle = \alpha E$ et que la puissance moyenne reçue par cette source est $\langle p \rangle = \alpha EI$. Ce dispositif permet donc de fournir une puissance variable à la source de courant en modifiant le rapport cyclique $\alpha$.
> Le transfert de puissance est réversible : il suffit d’inverser les bornes du générateur de courant pour que $\langle p \rangle$ soit négative. Dans ce cas, la puissance est transférée de la source de courant vers la source de tension.

> [!note] Alimentation d'un électromoteur : Choix des interrupteurs
> Quels interrupteurs pouvons-nous choisir dans le montage correspondant à l'alimentation d'une source de courant ?
> Envisageons un transfert de puissance du générateur vers le récepteur $(I > 0)$.
> Il existe deux points de fonctionnement pour chaque interrupteur ([[#^figure24|fig. 24]]).
> Les intensités traversant $K_1$ et $K_2$ étant toujours positives ou nulles, les interrupteurs choisis peuvent être unidirectionnels ([[#^figure25|fig. 25]]).
> Est-il nécessaire de choisir $K_1$ et $K_2$ commandés ?
> - Supposons que $K_2$ soit une diode orientée comme $i_{K_2}$.
> Sa conduction se produit dès que l’interrupteur $K_1$ est ouvert, car l’intensité $I$ est dans le sens passant de la diode. Son blocage se produit dès la fermeture de $K_1$, car elle est alors polarisée dans le sens bloqué.
> - Supposons que $K_1$ soit une diode orientée comme $i_{K_1}$.
> Si $i_{K_2}$. est fermé, elle est conductrice ; le générateur est en court-circuit et le montage est endommagé.
> Nous choisirons donc pour $K_1$ un interrupteur commande et pour $K_2$ une diode ([[#^figure26|fig. 26]]).
> ==**Le montage s’appelle hacheur série, car l'élément commandé est en série avec le générateur.**==
> ==**La diode est dite diode de roue libre, car elle est conductrice pendant la phase où la source débite une puissance nulle.**==

> [!note] Transfert entre deux sources de tension
> Ainsi que nous l’avons montré au paragraphes précédents ([[#^figure19|fig. 19]]), le transfert direct entre deux sources de même type est impossible.
> Nous allons étudier successivement, dans ce paragraphe, trois montages permettant le transfert unidirectionnel de puissance entre deux sources de tension.
> - Soit le récepteur est transformé en générateur de courant : le montage est le hacheur série. C’est le montage le plus utilisé.
> - Soit le générateur est transformé en générateur de courant : le montage est le hacheur parallèle.
> - Soit le transfert s’effectue par l’intermédiaire d’un élément de stockage de type source de courant : le montage est appelé hacheur à accumulation.

> [!note] Transfert entre deux sources de tension : Hacheur série
> Insérons une bobine en série avec le récepteur ([[#^figure27|fig. 27]]). L'ensemble récepteur-bobine est équivalent à une source de courant et peut être alimenté par une source de tension et la cellule à deux interrupteurs.
> Si le récepteur est un moteur, l’inductance de son circuit électrique peut être suffisante pour supprimer la bobine.
> - Tension aux bornes de l'ensemble bobine-charge : Nous pouvons résumer le cas, suivant l'état des interrupteurs ([[#^figure28|fig. 28]]). Remarquons d’abord que $i_L$ décroît pendant la phase $D$ passante $\left(\dfrac{di_L}{dt} = \frac{u_L}{L} = -\frac{E_R}{L} < 0\right)$. Comme $i_L$ ne peut pas décroître indéfiniment, $u_L$ doit être positif pendant la phase $D$ bloquée, $H$ fermé. $E_G$ est donc supérieur à $E_R$. Le hacheur est dit **dévolteur** ou **abaisseur**.
> Dans l’hypothèse où le courant dans l’inductance ne s’annule jamais, le cas $D$ bloquée et $H$ ouvert simultanément ne se produit pas.
> La tension $-u_D$ aux bornes d’ensemble bobine-charge prend donc uniquement les deux valeurs $E_G$ et $0$.
> Nous supposons par la suite que le courant ne s’annule pas dans la bobine.
> ==**Dans le cas usuel où l'intensité dans la bobine ne s’annule pas, la tension aux bornes de l’ensemble bobine-charge est un signal créneau variant entre $E_G$ et $0$, de rapport cyclique $\alpha$.**==
> ==**Ce résultat est faux si le courant dans la bobine s’annule.**==
> Nous pouvons alors envisager trois méthodes pour déterminer la tension aux bornes de la charge :
> 	- remplacer la source et le hacheur par une tension continue $\alpha E_G$ si l'intensité traversant la charge est quasiment constante ;
> 	- étudier la réponse du système bobine-charge en décomposant du signal créneau en série de Fourier si la charge est un dipôle linéaire ;
> 	- résoudre directement les équations différentielles du circuit.
> 
> 	Nous n’étudierons ici que la troisième méthode.

> [!note] Transfert entre deux sources de tension : Hacheur série
> - Chronogrammes : Utilisons la relation entre l'intensité et la tension aux bornes de la bobine $u_L = L\dfrac{di_L}{dt}$ ($i_L$ est aussi l'intensité $i_R$ dans le récepteur), et le fait que l'intensité dans une bobine est continue et que l'énergie emmagasinée dans la bobine est $W_L = \frac{1}{2}Li_{L}^{2}$.
> Nous pouvons bâtir le tableau suivant ([[#^figure29|fig. 29]]), où $t'$ représente la durée écoulée depuis le début de cycle.
> Comme nous étudions un régime établi de commutations périodiques, les intensités en début et fin de cycle sont égales $I_{L_m} = I_{L_M} - \frac{E_R}{L}(1 - \alpha)T$.
> En remplaçant $I_{L_M}$ par son expression en fonction de $I_{L_m}$ : $I_{L_m} = I_{L_m} + \frac{E_G - E_R}{L}\alpha T - \frac{E_R}{L}(1 - \alpha)T$, soit $E_R = \alpha E_G$.
> Nous pouvons alors bâtir le chronogramme de [[#^figure30|figure 30]].
> $\langle u_L \rangle = 0$ en régime permanent a pour conséquence l'égalité des aires colorées sur le chronogramme de $u_L$ ([[#^figure30|fig. 30]]). Cette égalité permet de retrouver la relation $E_R = \alpha E_G$.
> - Transferts d'énergie : Pendant la phase de conduction du hacheur, l’énergie de la bobine croît ($i_L$ augmente) et pendant la phase de roue libre, elle décroît ($i_L$ diminue).
> Cependant l'énergie reçue par la bobine pendant un cycle est : $\Delta W_L = \frac{1}{2}L(i(t + T)^{2} - i(t)^{2}) = 0$, car le régime est périodique établi: $i(t) = i(t + T)$.
> L’énergie reçue par la bobine pendant la première phase du cycle est égale à celle qu’elle cède pendant la deuxième phase : il y a égalité des aires sur le chronogramme des puissances ([[#^figure30|fig. 30]]).
> La totalité de l'énergie fournie en un cycle par le générateur est transférée sans pertes au récepteur.
> La puissance moyenne fournie à la charge est égale celle cédée par le générateur.
> ==**La bobine est un accumulateur d’énergie fonctionnant sans pertes dans le cas idéal. Elle absorbe une partie de l’énergie fournie par le générateur, qu’elle restitue au récepteur pendant la phase de roue libre.**==

> [!note] Transfert entre deux sources de tension : Hacheur série
> - Caractéristiques de transfert : L'intensité moyenne dans le générateur est : $\displaystyle I_G = \frac{1}{T}\int_{0}^{\alpha T}\left(I_{L_m} + \frac{E_G - E_R}{L}t\right)dt = \alpha\frac{I_{L_m} + I_{L_M}}{2}$, alors que l'intensité moyenne dans le récepteur est : $\displaystyle I_R = \frac{1}{T}\left[\int_{0}^{\alpha T}\left(I_{L_m} + \frac{E_G - E_R}{L}t\right)dt + \int_{\alpha T}^{T}\left(I_{L_M} - \frac{E_R}{L}(t - \alpha T)\right)dt\right] = \frac{I_{L_m} + I_{L_M}}{2}$.
> Ces deux résultats s’obtiennent facilement par des calculs d'aires sur les courbes $I_R(t)$ et $I_G(t)$ de [[#^figure30|figure 30]].
> Nous remarquons que $E_GI_G = E_RI_R$.
> Ce résultat traduit la conservation de l'énergie. En l’absence d’éléments résistifs, la puissance moyenne $\mathcal{P}_G$ fournie par le générateur doit être égale à la puissance moyenne $\mathcal{P}_R$ reçue par le récepteur. Or, $E_G$ et $E_R$ étant constantes, nous pouvons écrire : $\displaystyle \mathcal{P}_G = \frac{1}{T}\int_{0}^{T}E_Gi_G(t')dt' = E_GI_G$ et $\displaystyle \mathcal{P}_R = \frac{1}{T}\int_{0}^{T}E_Ri_R(t')dt' = E_RI_R$.
> ==**Les caractéristiques relatives aux grandeurs moyennes du montage sont alors $E_R = \alpha E_G$, $I_G = \alpha I_R$ et $\mathcal{P}_G = \mathcal{P}_R$. Ces relations sont identiques à celles du transformateur en alternatif avec un rapport de transformation de $\alpha$.**==
> $I_G$ et $I_R$ ne peuvent être déterminées qu’avec la connaissance d’une donnée supplémentaire : la puissance moyenne $\mathcal{P}_R$ fournie à la charge par exemple. Avec des éléments idéaux, cette indétermination est levée dés que l’on tient compte de la résistance du récepteur.
> - Ondulation en courant : L'ondulation en courant définie par $I_{L_M} - I_{L_m}$ vaut : $\Delta i = \frac{E_G - E_R}{L}\alpha T = \frac{E_G - E_R}{L}\frac{E_R}{E_G}T = \alpha(1 - \alpha)\frac{E_GT}{L}$. Elle est maximale, à $E_G$ donnée, pour $E_R = \frac{E_G}{2}$ et vaut alors : $\frac{E_GT}{4L}$.
> Pour la minimiser, il faut utiliser des bobines de coefficient d’inductance élevé et des fréquences de commutation élevées. L’utilisation de telles fréquences présente un autre avantage lorsque le récepteur est un moteur : les tôles de son circuit magnétique vibrent à la fréquence de commutation.
> Une fréquence supérieure à 20 kHz crée des vibrations dans le domaine des ultrasons donc inaudibles et assure un confort sonore appréciable.
> Remarques :
> 	- Pour que l'intensité dans la bobine soit toujours positive, il est nécessaire que $I_{L_m}$ soit positive. Comme $I_R = \frac{I_{L_m} + I_{L_M}}{2}$, cette condition est équivalente à $\Delta i < 2I_R$. La valeur de la bobine est donc calculée de telle façon que : $I_R > \frac{\alpha(1 - \alpha)}{2}\frac{E_GT}{L}$.
> 	- Le courant prélevé au générateur est discontinu. Cela peut être gênant si l'impédance du générateur n’est pas négligeable. Il est alors nécessaire de l'améliorer à l'aide d’un circuit $(L, C)$, permettant le lissage du courant dans le générateur et limitant les surtensions à l’entrée du hacheur lors des commutations ([[#^figure31|fig. 31]]).

> [!note] Transfert entre deux sources de tension : Hacheur parallèle
> Le hacheur dévolteur ne permet pas le passage de courant du générateur de f.e.m. la plus petite vers la plus grande. Son irréversibilité est due à l’unidirectionnalité des interrupteurs. Pour permettre un passage du courant en sens contraire, les interrupteurs doivent être « inversés ».
> Nous obtenons donc le montage ([[#^figure32|fig. 32]]) appelé hacheur parallèle, car l’élément commandé est en parallèle avec le générateur.
> Remarquons que dans ce cas le générateur source de tension est transformé par l’inductance en source de courant.
> Ce montage est dit **survolteur** ou **élévateur**.
> - Chronogrammes : Vérifions qu'il permet le transfert de la puissance d'un générateur de tension de f.e.m. $E_G$ vers un récepteur de tension de f.e.m. $E_R$ supérieure à $E_G$.
> Étudions le chronogramme correspondant aux paramètres du montage.
> Nous pouvons résumer les cas, suivant l'état des interrupteurs ([[#^figure33|fig. 33]]).
> Plaçons-nous dans l'hypothèse où le courant dans l'inductance ne s'annule jamais. Le cas $D$ bloquée et $H$ ouvert simultanément ne se produit pas.
> Le cycle comporte donc deux phases :
> 	- $H$ fermé, $D$ bloquée : $i_R = 0$, $u_L = E_G > 0$ et $\dfrac{di_L}{dt} = \frac{E_G}{L}$. En appelant $I_{L_m}$, l'intensité en début de cycle et $t'$ le temps écoulé depuis le début du cycle, $i_L = I_{L_m} + \frac{E_G}{L}t'$ et la valeur à l'instant de commutation $t = \alpha T$ de l'intensité est : $I_{L_M} = I_{L_m} + \frac{E_G}{L}\alpha T$. La bobine emmagasine alors de l'énergie, car $i_L$ croît.
> 	- $D$ passante, $H$ ouvert : $I_R = i_L$, $u_L = E_G - E_R$ et $\dfrac{di_L}{dt} = \frac{E_G - E_R}{L}$. ==**La valeur moyenne de $u_L$ étant nulle en régime établi, $u_L$ est négative durant cette phase. Nous en déduisons que $E_G < E_R$ (caractère élévateur du hacheur).**== $i_L = I_{L_M} + \frac{E_G - E_R}{L}(t' - \alpha T)$ et la valeur en fin de période $t' = T$ est : $I_{L_m}^{'} = I_{L_M} + \frac{E_G - E_R}{L}T(1 - \alpha)$. La bobine restitue de l'énergie, car $i_L$ décroît $(E_G < E_R)$.

> [!note] Transfert entre deux sources de tension : Hacheur parallèle
> - Caractéristique de transfert : Quand le régime permanent est établi, les intensités en début et fin de cycle dans la bobine sont égales $I_{L_m} = I_{L_m}^{'}$. En remplaçant $I_{L_M}$ par son expression en fonction de $I_{L_m}$ : $I_{L_m} = I_{L_m} + \frac{E_G}{L}\alpha T + \frac{E_G - E_R}{L}T(1 - \alpha)$, soit $E_G = (1 -\alpha) E_R$. L'intensité moyenne dans le générateur est : $\displaystyle I_G = \frac{1}{T}\left[\int_{0}^{\alpha T}\left(I_{L_m} + \frac{E_G}{L}t\right)dt + \int_{\alpha T}^{T}\left(I_{L_M} + \frac{E_G - E_R}{L}(t - \alpha T)\right)dt\right] = \frac{I_{L_m} + I_{L_M}}{2}$, alors que celle dans le récepteur est : $\displaystyle I_R = \frac{1}{T}\int_{\alpha T}^{T}\left(I_{L_M} + \frac{E_G - E_R}{L}(t - \alpha T)\right)dt = (1 - \alpha)\frac{I_{L_m} + I_{L_M}}{2}$.
> Ces trois résultats s’obtiennent avec un calcul d’aires grâce aux courbes de [[#^figure34|figure 34]].
> Comme dans le cas du hacheur série, l’énergie emmagasinée par la bobine pendant la fermeture de $H$ est restituée pendant son ouverture. La puissance moyenne $\mathcal{P}_R$ fournie au récepteur est égale à celle $\mathcal{P}_G$ fournie par le générateur.
> ==**Les caractéristiques du montage sont donc : $E_R = \frac{E_G}{1 - \alpha}$, $I_R = (1 - \alpha)I_G$ et $\mathcal{P}_G = \mathcal{P}_R$.**==
> ==**Ces relations sont identiques à celles du transformateur en alternatif avec un rapport de transformation de $\frac{1}{1 - \alpha}$.**==
> L'utilisation simultanée d’un hacheur dévolteur et d’un hacheur survolteur permet d’assurer les phases de traction et de freinage avec récupération d’un moteur ([[#^figure35|fig. 35]]). Il permet le fonctionnement d’un récepteur dans deux quadrants $(E_R > 0, I_R \geqslant 0)$ et $(E_R > 0, I_R \leqslant 0)$.

> [!note] Transfert entre deux sources de tension : Transfert à l'aide d'un élément de stockage
> Dans ce type de montage, le générateur de f.e.m. $E_G$ puis le récepteur de f.e.m. $E_R$ sont reliés successivement à une bobine qui accumule de l'énergie sous une tension $E_G$ et la restitue sous une tension $-E_R$. Cet élément de stockage est du type source de courant, ce qui est compatible avec une connexion à des sources de tension ([[#^figure36|fig. 36]]).
> - Chronogramme : Étudions le chronogramme du montage ([[#^figure37|fig. 37]]).
> Nous pouvons résumer les cas suivant l'état des interrupteurs ([[#^figure38|fig. 38]]).
> Pendant la phase de stockage, $i_L$ augmente donc $u_L$ est positive, alors que pendant la phase de restitution, $i_L$ diminue donc $u_L$ est négative. Il est donc nécessaire de brancher le générateur et le récepteur en sens inverse l’un de l’autre ; le **hacheur** est dit **inverseur**.
> Faisons l’hypothèse que le cas $H$ ouvert et $D$ bloquée ne se produit pas. Ceci est équivalent à supposer que l'intensité dans la bobine ne s’annule pas. Le cycle comprend deux phases :
> 	- $H$ fermé, $D$ bloquée : $i_R = 0$, $i_G = i_L$ et $\dfrac{di_L}{dt} = \frac{E_G}{L}$. En appelant $I_{L_m}$, l’intensité en début de cycle et $t'$ le temps écoulé depuis le début du cycle, $i_L = I_{L_m} + \frac{E_G}{L}t'$ ; et la valeur à l’instant de commutation $t = \alpha T$ de l'intensité $I_{L_M} = I_{L_m} + \frac{E_G}{L}\alpha T$. La bobine emmagasine alors de l'énergie, car $i_L$ croît .
> 	- $D$ passante, $H$ ouvert : $I_G = 0$, $i_R = i_L$ et $\dfrac{di_L}{dt} = -\frac{E_R}{L}$.
> 	$i_L = I_{L_M} - \frac{E_R}{L}(t' - \alpha T)$ et la valeur en fin de période $t' = T$ est $I_{L_m}^{'} = I_{L_M} - \frac{E_R}{L}T(1 - \alpha)$. La bobine restitue de l'énergie, car $i_L$ décroît.
> - Caractéristique de transfert : Quand le régime permanent est établi, les intensités en début et fin de cycle dans la bobine sont égales $I_{L_m} = I_{L_m}^{'}$. En remplaçant $I_{L_M}$ par son expression en fonction de $I_{L_m}$ : $I_{L_m} = I_{L_m} + \frac{E_G}{L}\alpha T - \frac{E_R}{L}T(1 - \alpha)$, soit $\alpha E_G = (1 -\alpha) E_R$. L'intensité moyenne dans le générateur est : $\displaystyle I_G = \frac{1}{T}\int_{0}^{\alpha T}\left(I_{L_m} + \frac{E_G}{L}t\right)dt = \alpha\frac{I_{L_m} + I_{L_M}}{2}$ ;
> alors que celle dans le récepteur est : $\displaystyle I_R = \frac{1}{T}\int_{\alpha T}^{T}\left(I_{L_M} - \frac{E_R}{L}(t - \alpha T)\right)dt = (1 - \alpha)\frac{I_{L_m} + I_{L_M}}{2}$.
> Comme dans le cas du hacheur série, l'énergie emmagasinée par la bobine pendant la fermeture de $H$ est restituée pendant son ouverture. La puissance moyenne $\mathcal{P}_R$ fournie au récepteur est égale à celle $\mathcal{P}_G$ fournie par le générateur.
> ==**Les caractéristiques du montage sont donc : $E_R = \frac{\alpha}{1 - \alpha}E_G$, $I_G = \frac{\alpha}{1 - \alpha}I_R$ et $\mathcal{P}_R = \mathcal{P}_G$.**==
> ==**Ces relations sont identiques à celles du transformateur en alternatif avec un rapport de transformation de $\frac{\alpha}{1 - \alpha}$.**==
> Ce montage présente l’intérêt d’être un hacheur dévolteur pour $\alpha < \frac{1}{2}$ et survolteur pour $\alpha > \frac{1}{2}$. Il reste cependant irréversible.
> Il présente l’inconvénient de courants discontinus dans le générateur et dans le récepteur. Il ne peut donc pas être utilisé pour l’alimentation d’un moteur à cause de l’inductance de ce type de récepteur incompatible avec des discontinuités de courant.

> [!note] Exemples d'applications : Régulation de vitesse d'un moteur
> Le but de la régulation de vitesse d’un moteur est :
> - de maintenir celle-ci à une valeur imposée (consigne) indépendamment du couple appliqué à l’axe du moteur ;
> - de s’assurer que le courant moteur ne dépasse pas une valeur maximale même en cas de couple important, ou au démarrage ;
> - de permettre un démarrage progressif du moteur pour éviter des efforts mécaniques excessifs.
> 
> Commentons le schéma fonctionnel d’un régulateur simple de vitesse d’un moteur à courant continu ([[#^figure39|fig. 39]]).
> - Le transducteur est une génératrice tachymétrique ou un capteur optoélectronique. Une génératrice délivre une tension proportionnelle à sa vitesse de rotation, alors que le capteur optoélectronique délivre une tension variable de fréquence proportionnelle à la vitesse de rotation. Ce dernier est donc associé à un convertisseur fréquence tension.
> - L'amplitude de la tension obtenue en sortie du transducteur est adaptée à l’entrée du comparateur par l’adaptateur d’échelle.
> - Le comparateur bâtit le signal d’erreur différence entre la consigne et le retour de vitesse adapté.
> - Ce signal mis en forme à l'aide d’un filtre sert à fabriquer le signal de commande du hacheur alimentant le moteur.
> 
> Une seconde boucle peut être mise en cascade pour effectuer une régulation en courant avec limitation.
> Comme la constante de temps électromécanique du moteur est en général grande devant la période du hacheur, le signal alternatif dû au hachage est en dehors de la bande passante du moteur et n’apparaît pas dans sa vitesse de rotation. Tout se passe comme si le moteur était alimenté par la tension moyenne délivrée par le hacheur. L’ensemble circuit de commande-hacheur est alors équivalent à un amplificateur de puissance.
> Si les éléments de la chaîne sont linéaires, nous retrouvons alors la structure bouclée classique de [[#^figure40|figure 40]].

> [!note] Exemples d'applications : Alimentation ou régulateur à découpage


# Diagrammes
Rhéostat. L'intensité est identique dans le générateur et le récepteur. Le rendement est donc égal au rapport $\frac{V_2}{V_1}$
![[electronique2/attachments-electronique2/figure280.png]]^figure1

Alimentation intermittente d'une résistance
![[electronique2/attachments-electronique2/figure281.png]]^figure2

Alimentation par une source de courant
![[electronique2/attachments-electronique2/figure284.png]]
La source de courant ne peut jamais être en circuit ouvert. Elle doit donc être périodiquement court-circuitée.
Quand l'interrupteur est fermé : $i = 0$, $u = 0$ et $p = 0$.
Quand l'interrupteur est ouvert : $i = I$, $u = RI$ et $p = RI^{2}$.
Les valeurs moyennes sont donc : $\langle i \rangle = (1 - \alpha)I$, $\langle u \rangle = (1 - \alpha)RI$ et $\langle p \rangle = (1 - \alpha)RI^{2}$.
Pendant la phase de court-circuit, le générateur ne fournit aucune puissance (la tension à ses bornes est nulle). Le rendement est donc égal à 1. ^figure4

Symbole d'un convertisseur continu-continu
![[electronique2/attachments-electronique2/figure285.png]]^figure5

Diode
![[electronique2/attachments-electronique2/figure287.png]]^figure7

Transistor
![[electronique2/attachments-electronique2/figure288.png]]^figure8

Thyristor (ouverture naturelle)
![[electronique2/attachments-electronique2/figure289.png]]^figure9

Schémas d'interrupteurs unidirectionnels commandés
![[electronique2/attachments-electronique2/figure290.png]]^figure10

a. Schéma de Thévenin du générateur. b. Schéma de Norton du générateur.
![[electronique2/attachments-electronique2/figure291.png]]^figure11

Le condensateur lisse la tension $u(t)$
![[electronique2/attachments-electronique2/figure294.png]]^figure13

En régime commuté, le condensateur en parallèle sur un générateur de courant le transforme en générateur de tension
![[electronique2/attachments-electronique2/figure296.png]]^figure15

En régime commuté, le condensateur en parallèle sur une source de tension l'améliore
![[electronique2/attachments-electronique2/figure297.png]]^figure16

L'inductance lisse le courant qui la traverse
![[electronique2/attachments-electronique2/figure298.png]]^figure17

En régime commuté, l'inductance en série avec un générateur de tension le transforme en générateur de courant
![[electronique2/attachments-electronique2/figure299.png]]^figure18a

En régime commuté, l'inductance en série avec un générateur non idéale de courant l'améliore
![[electronique2/attachments-electronique2/figure300.png]]^figure18b

Montages impossibles
![[electronique2/attachments-electronique2/figure301.png]]^figure19

Transfert de puissance entre deux sources de nature différente
![[electronique2/attachments-electronique2/figure302.png]]^figure20

Surtension à l'ouverture d'un interrupteur
![[electronique2/attachments-electronique2/figure303.png]]^figure21

Cellule à deux interrupteurs
![[electronique2/attachments-electronique2/figure304.png]]^figure22

Cellule à deux interrupteurs. Caractéristiques des interrupteurs
![[electronique2/attachments-electronique2/figure307.png]]^figure25

Hacheur série avec la diode de roue libre
![[electronique2/attachments-electronique2/figure308.png]]^figure26

Hacheur série ou dévolteur
![[electronique2/attachments-electronique2/figure309.png]]^figure27

Amélioration du générateur. L'inductance en série avec le générateur supprime les discontinuités de l'intensité qui le traverse. Le condensateur limite les surtensions aux bornes du hacheur
![[electronique2/attachments-electronique2/figure313.png]]^figure31

Montage hacheur parallèle ou survolteur
![[electronique2/attachments-electronique2/figure314.png]]^figure32

Hacheur réversible en courant
![[electronique2/attachments-electronique2/figure317.png]]^figure35

Hacheur inverseur
![[electronique2/attachments-electronique2/figure318.png]]^figure36

Régulation d'un moteur
![[electronique2/attachments-electronique2/figure321.png]]^figure39

Schéma fonctionnel de régulation d'un moteur
![[figure322.png]]^figure40
# Graphiques
Rapport cyclique $\alpha$
![[electronique2/attachments-electronique2/figure283.png]]^figure3

Caractéristiques d'interrupteurs. Interrupteur commandé quatre quadrants
![[electronique2/attachments-electronique2/figure286.png]]^figure6

Comportement de quelques dipôles
![[electronique2/attachments-electronique2/figure292.png]]^figure12a

Comportement de quelques dipôles
![[electronique2/attachments-electronique2/figure293.png]]^figure12b

Variation de $u(t)$
![[electronique2/attachments-electronique2/figure295.png]]^figure14

Chronogramme
![[electronique2/attachments-electronique2/figure305.png]]^figure23

Points de fonctionnement des interrupteurs
![[electronique2/attachments-electronique2/figure306.png]]^figure24

Points de fonctionnement des interrupteurs
![[electronique2/attachments-electronique2/figure310.png]]^figure28

Chronogrammes ($W_L$ est l'énergie de la bobine)
![[electronique2/attachments-electronique2/figure311.png]]^figure29

Chronogrammes du dévolteur. Cas où l'intensité ne s'annule pas. a est la puissance reçue par la bobine et b la puissance cédée par la bobine
![[electronique2/attachments-electronique2/figure312.png]]^figure30

Points de fonctionnement des interrupteurs
![[electronique2/attachments-electronique2/figure315.png]]^figure33

Chronogrammes du survolteur. a est la puissance reçue par la bobine et b la puissance fournie par la bobine
![[electronique2/attachments-electronique2/figure316.png]]^figure34

Chronogramme
![[electronique2/attachments-electronique2/figure319.png]]^figure37

Points de fonctionnement des interrupteurs
![[electronique2/attachments-electronique2/figure320.png]]^figure38
# Expériences

# Autres notes
