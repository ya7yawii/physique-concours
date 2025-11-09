---
titre: "[[04-Principe des appareils de mesure]]"
tags:
aliases:
crée: 09-11-2025, 08:38
---
# Formules

# Définitions
> [!note] Utilisation d’un multimètre : Utilisation en voltmètre DC
> La mesure de la différence de potentiel entre deux points A et B d’un circuit s’effectue en plaçant le multimètre en parallèle entre ces deux points.
> Un multimètre numérique utilisé en voltmètre perturbe peu le circuit sur lequel s’effectue la mesure.
> Choix du calibre : (Exemple : Application 2 page 72) : Un multimètre à 2000 points de mesure et de précision 0,5 % + 1 [[#^demo1|digit]] en voltmètre DC possède les calibres 200 mV, 2 V et 20 V. Quel est l’ordre de grandeur de l’erreur pour une mesure de tension de 150 mV sur ces trois calibres ?
> L'erreur relative de conversion (0,5 %) conduit toujours à la même erreur $\delta_1 = 150\frac{0,5}{100} = 0,75\, mV$.
> L’[[#^demo1|erreur de quantification]] $\delta_2$ s’y ajoute. Pour évaluer cette dernière erreur, examinons l’affichage de la grandeur mesurée avec le calibre : ![[electronique1/attachments-electronique1/figure58.png]]
> Nous remarquons que les erreurs $\delta = \delta_1 + \delta_2$ sur les calibres 200 mV et 2 V sont voisines. Ces deux calibres pourront être indifféremment utilisés.
> Pour bénéficier du maximum de précision, nous devons utiliser le plus petit calibre permettant d’effectuer la mesure. Sur le calibre 200 mV, le dernier chiffre ne sera pas significatif.

> [!note] Utilisation d’un multimètre : Utilisation en ampèremètre DC
> Le convertisseur analogique-numérique d’un multimètre ne peut mesurer directement qu’une tension. Il est donc nécessaire d’utiliser la chute de potentiel aux bornes d’un résistor $R_m$ connu au sein de multimètre pour mesurer une intensité. La valeur maximale de cette chute de tension est donnée dans la notice constructeur.
> La mesure de l’intensité dans une branche de circuit s’effectue en plaçant le multimètre en série avec les éléments de la branche étudiée.
> La perturbation introduite par la mesure d’une intensité n’est négligeable que si une chute de potentiel aux bornes de l’appareil de mesure est sans importance pour le circuit étudié.
> Le [[#^demo2|calibre utilisé]] doit être le fruit d’un compromis entre un maximum de chiffres affichés et un minimum de perturbation du circuit. La meilleure façon de procéder consiste souvent à diminuer le calibre jusqu’à ce que la valeur affichée ne soit plus compatible avec celle du calibre suivant.

> [!note] Mesure de grandeurs variables
> Nous ne pouvons pas mesurer de grandeurs variant rapidement, car le temps mis pour effectuer une mesure n’est pas négligeable $(\approx 1 s)$.
> Il est tout de même possible de mesurer des grandeurs ([[#^figure1|fig. 1]]) indépendantes du temps caractéristiques de signaux périodiques.
> Quels sont les « appareils » disponibles pour effectuer ces mesures ? : Nous disposons d’appareils à cadre mobile (avec choix des entrées « DC » et « AC »), des appareils « RMS » (avec choix des entrées « DC » et « AC »), et des appareils « TRMS » (avec choix des entrées « DC », « AC » et « AC + DC »). Nous trouvons les propriétés de ces appareils dans la [[#^figure2a|figure 2a]] pour une signal de valeur moyenne nulle et dans la [[#^figure2b|figure 2b]] pour une signal de valeur moyenne non nulle.
> Nous devons veiller à trois points pour apprécier l’indication d’un multimètre :
> - le multimètre perturbe la grandeur mesurée de la même manière qu’en continu : erreur d’insertion ;
> - si le signal étudié n’est pas sinusoïdal, le résultat donné par un multimètre non « efficace vrai » sera faux ;
> - un multimètre a une bande passante limitée : nous devons l’utiliser dans le domaine de fréquences prévu par le constructeur. D’où l’intérêt de lire la notice du multimètre.

> [!note] Utilisation d’un multimètre : Utilisation en ohmmètre
> Le convertisseur analogique-numérique d’un multimètre ne peut mesurer directement qu’une tension. Il nous suffit de disposer d’un générateur de courant d’intensité η connue au sein de multimètre et de mesurer la différence de potentiel $u$ aux bornes du dipôle. Nous aurons alors $R = \frac{u}{\eta}$.
> L’ohmmètre, appliqué aux bornes d’un dipôle, injecte un courant dans le circuit auquel le dipôle appartient. De ce fait, l’ohmmètre perturbe le circuit. En outre, la différence de potentiel, qui existe aux bornes du dipôle, est fonction de tout le circuit et non seulement de la résistance du dipôle.
> Il est impossible de mesurer la résistance d’un dipôle branché dans un circuit !

> [!note] Mesure d’impédances à l’aide d’un multimètre
> Par définition, l’impédance $Z$ d’un dipôle linéaire passif est égale au rapport de la tension maximale et du courant maximal en régime sinusoïdal : $Z = \frac{u_m}{i_m}$.
> Il s’agit de mesurer l’impédance $Z$ d’un dipôle pour une tension sinusoïdale de fréquence compatible avec la bande passante du multimètre.
> Nous devons simultanément mesurer l’intensité qui traverse le dipôle ainsi que la différence de potentiel à ses bornes. Nous utiliserons donc deux multimètres l’un en ampèremètre, l’autre en voltmètre. Deux montages sont possibles :
> - Montage courte dérivation : Le courant mesuré effectivement par l’ampèremètre est la somme des courants traversant le dipôle et le voltmètre ([[#^figure3a|fig. 3a]]).
> - Montage longue dérivation : La différence de potentiel effectivement mesurée par le voltmètre est la somme des différences de potentiel aux bornes du dipôle et de l’ampèremètre ([[#^figure3b|fig. 3b]]).
> 
> Le courant qui traverse un voltmètre numérique est très faible (résistance interne de 10 MΩ), alors que la chute de potentiel aux bornes d’un ampèremètre n’est souvent pas négligeable.
> <mark style="color: red">Pour la mesure d’une impédance, seul le montage courte dérivation est à employer avec des multimètres numériques.</mark>

==**Principe d’un oscilloscope analogique**== :
Un appareil de mesure est dit « analogique » lorsque la grandeur à mesurer est repérée par une autre grandeur qui varie de façon continue.
Un voltmètre à aiguille est un appareil analogique : le déplacement de l’aiguille est une fonction continue de la tension.
Par opposition, un appareil numérique convertit la grandeur à mesurer en un nombre qui est stocké dans une mémoire numérique.
L’élément principal d’un oscilloscope analogique est le tube cathodique, dans lequel la déviation électrostatique des électrons est réalisée par deux paires de plaques : les plaques de déviation horizontale et verticale ([[#^figure4|fig. 4]]).
# Diagrammes
Montage courte dérivation
![[electronique1/attachments-electronique1/figure62.png]]^figure3a

Montage longue dérivation
![[electronique1/attachments-electronique1/figure63.png]]^figure3b
# Graphiques
Définition des grandeurs mesurables
![[electronique1/attachments-electronique1/figure59.png]]
Dans les expressions, $T_m$ représente la durée (caractéristique de l’appareil de mesure) sur laquelle est traité le signal. ^figure1

Signal $u(t)$ de valeur moyenne nulle
![[electronique1/attachments-electronique1/figure60.png]]^figure2a

Signal $u(t)$ de valeur moyenne non nulle
![[electronique1/attachments-electronique1/figure61.png]]^figure2b

Tube cathodique
![[electronique1/attachments-electronique1/figure64.png]]^figure4
# Expériences

# Autres notes
> [!warning] Évaluer l’incertitude d’une mesure
> ![[electronique1/attachments-electronique1/figure57.png]]
^demo1

> [!warning] Choix de la calibre
> Chaque calibre est la valeur maximale qui peut être mesurée pour la position choisie du curseur.
> Exemples :
> - si le curseur est en position 20mA, l’intensité maximale que peut mesurer l’ampèremètre est moins de 20mA.
> - si le curseur est en position 20V, la tension maximale que peut mesurer le voltmètre est moins de 20V.
> 
> Attention : si la valeur est supérieure au calibre utilisé, le multimètre risque d’être endommagé.
> Choix du calibre de l’ampèremètre :
> - Lors de la première mesure dans un circuit quelconque, on utilise le plus gros calibre : Par exemple pour le calibre le plus gros 10A, on obtient I = 0.09 A.
> - Après cette première mesure, la meilleure précision sera obtenue en adoptant le calibre immédiatement supérieur à la valeur mesurée. Comme 0.09 A = 90 mA, le calibre immédiatement supérieur et le calibre 200mA. On obtient avec ce calibre I = 94.3 mA (cette mesure est plus précise que la précédente car elle comporte plus de chiffres).
^demo2
