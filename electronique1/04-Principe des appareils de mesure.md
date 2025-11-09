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

> [!note] Utilisation d'un oscilloscope : Signaux d'entrée
> Le signal d’entrée (voie 1 ou 2) est calibré par un amplificateur (de 5 mV à 20 V par division) d’impédance d’entrée souvent équivalente à une résistance de 1 MΩ en parallèle avec un condensateur de 30 à 50 pF.
> Le branchement d’un oscilloscope pour mesurer une différence de potentiel perturbe le circuit de la même façon qu’un multimètre utilisé en voltmètre. Cette perturbation doit être prise en compte dans certains montages.
> Remarque : La composante continue d’un signal peut masquer sa composante variable. Que dire d’un signal variable d’amplitude 10 mV « noyé » sous une composante continue de 10 V ?
> La touche AC/DC de la voie étudiée permet de résoudre ce type de problème ; la composante continue du signal est éliminée en mode AC. Attention, en mode AC le signal est filtré par un filtre passe-haut, dont la fréquence de coupure est d’une dizaine de hertz. <mark style="color: red">Ce mode ne doit être utilisé qu’exceptionnellement</mark>.
> Remarque : Le bouton de positionnement de la voie ajoute une composante continue à la valeur appliquée aux plaques de déviation. Lors des mesures, la position du zéro de la voie doit être connue. Pour la visualiser, il suffit d’utiliser la touche GRND (ground ou masse) de la voie (une tension nulle est alors appliquée).

> [!note] Utilisation d'un oscilloscope : Base de temps et synchronisation
> Dans le mode balayage, une tension en dents de scie est appliquée sur les plaques de déviation horizontale. Le spot se déplace à vitesse constante de la gauche vers la droite. Cette vitesse est choisie en utilisant le bouton « base de temps » qui permet le contrôle de la vitesse de balayage en seconde par division. Pendant son retour (rapide), le faisceau électronique est éteint.
> Un signal périodique ne peut être visualisé de façon stable que si la période de la dent de scie est asservie à celle du signal. C’est le but de la synchronisation. Le spot attend que le signal servant à la synchronisation passe par zéro ou par une valeur fixée par le réglage du seuil avec une pente déterminée positive ou négative (bouton +/– de la base de temps) pour effectuer son trajet de gauche à droite ([[#^figure5a|figs. 5a]] et [[#^figure5b|b]]).
> Plusieurs modes de synchronisation existent. En voici quelques-uns :
> - mode DC (direct current) : le signal est prélevé, puis directement mis en forme pour la synchronisation ;
> - mode AC (alternative current) : seule la composante variable du signal est conservée ;
> - mode LF (low frequency) ou basse fréquence : seule la composante basse fréquence du signal est conservée ;
> - mode HF (high frequency) ou haute fréquence : seule la composante haute fréquence est conservée.
> 
> Dans la plupart des montages utilisés le mode LF donne les meilleurs résultats.
> Le signal servant à la synchronisation peut être soit :
> - le signal de la voie 1 ;
> - le signal de la voie 2 ;
> - un signal extérieur.
> 
> <mark style="color: red">Si nous utilisons le mode balayage, nous devons synchroniser la base de temps sur le signal de plus grande amplitude.</mark>
> En particulier, il est souvent intéressant de se placer en mode synchronisation extérieure avec comme signal celui de la sortie « synchro » du générateur basse fréquence.

> [!note] Utilisation d'un oscilloscope : Fonctionnement bicourbe d’un oscilloscope
> Seuls les oscilloscopes bicourbes haut de gamme possèdent un double canon à électrons et un double système de déviation. Les oscilloscopes classiques utilisent deux méthodes pour tracer « simultanément » deux courbes ([[#^figure6|fig. 6]]).
> - Le mode alterné : Après chaque retour de balayage, la voie tracée à l’écran est changée. Ce mode n’est possible que si la durée du balayage est petite (moins de 0,1 s) pour éviter le clignotement. Le signal 1 est décrit, puis 2, puis 1, etc. mais trop lentement et l’œil perçoit ces basculements de l’un à l’autre.
> - Le mode découpé (chopped) : Le changement de voie se fait plusieurs fois par période de balayage à une fréquence de 500 kHz environ. Ce mode n’est possible que si la période du signal est grande devant celle de découpage.
> 
> L’oscilloscope choisit souvent automatiquement le mode en fonction de la base de temps.

> [!note] Utilisation d'un oscilloscope : Mesures en mode balayage
> Le mode balayage permet d’observer et de mesurer l’amplitude et la fréquence d’un signal périodique en utilisant les calibres de la voie et de la base de temps.
> Le mode bicourbe permet aussi de mesurer le déphasage entre deux signaux ([[#^figure7|fig. 7]]). Si $L$ est la longueur correspondant à une période et $l$ celle qui correspond au déphasage $\varphi$, alors $\varphi = 360\frac{l}{L}$ en degré ou $\varphi = 2\pi\frac{l}{L}$ en radian. Cette mesure peut être améliorée dans le cas des petits déphasages en utilisant une demi-période.
> Remarque : En pratique, il est commode de jouer sur la calibration de la base de temps de façon à amener la longueur d’une demi-période à 9 carreaux.
> De cette façon on mesure directement un déphasage de 20° par carreau de décalage entre ces deux signaux.
> Cette méthode n’est applicable que si la base de temps est réglable de manière continue, ce qui n’est pas le cas pour tous les appareils, en particulier les numériques. Dans ce cas, le déphasage est directement affiché à l’écran.


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

Synchronisation de la base de temps
![[electronique1/attachments-electronique1/figure65.png]]^figure5a

Aspect du signal observé sur l’écran
![[electronique1/attachments-electronique1/figure66.png]]^figure5b

Affichage de deux courbes simultanément
![[electronique1/attachments-electronique1/figure67.png]]^figure6

Mesure d’un déphasage en mode base de temps. $l \approx 0,8\, div$, $L \approx 4,5\, div$ et $\varphi = 65\degree$ (retard de 2 par rapport à 1)
![[electronique1/attachments-electronique1/figure68.png]]^figure7
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
