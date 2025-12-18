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
> Comme $i_C = C\dfrac{du}{dt}$ : $\Delta u < \frac{i_{C\,max}}{C}T$ ou $\Delta u < \frac{i_{C\,max}}{fC}$
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
# Expériences

# Autres notes
