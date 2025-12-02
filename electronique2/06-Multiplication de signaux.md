---
titre: "[[06-Multiplication de signaux]]"
tags:
aliases:
crée: 01-12-2025, 20:42
---
# Formules
> [!note] Multiplieur analogique
> La multiplication de deux signaux est très utilisée en électronique. De nombreux circuits intégrés ont été conçus dans ce but. L’AD633 fait partie des multiplieurs analogiques capables de réaliser la multiplication de deux tensions.
> - Présentation de l'AD633 : Étudions son schéma fonctionnel ([[#^figure1|fig. 1]]). Il comporte :
> 	- deux entrées différentielles $X_1$, $X_2$ et $Y_1$, $Y_2$ à haute impédance d’entrée $(> 10 M\Omega)$ ;
> 	- un circuit multiplieur réalisant l'opération $\frac{x(t)y(t)}{E_0}$, où $E_0$ est une tension de référence fixée à 10 V par le constructeur ;
> 	- un sommateur ajoutant la tension $z(t)$ au résultat ;
> 	- un suiveur de faible impédance de sortie, protégé en courant $(I_{max} = 30 mA)$ contre les courts-circuits ;
> 	- deux bornes pour une alimentation symétrique de $\pm 8 V$ à $\pm 18 V$, la valeur typique étant de $\pm 15 V$.
> 
> 	L’opération réalisée par le circuit est donc : $w(t) = \frac{x(t)y(t)}{E_0} + z(t)$ avec $E_0 = 10 V$.
> 	Le montage multiplieur que nous utiliserons est donné sur la [[#^figure2|figure 2]].
> 	Les condensateurs de $0,1 \mu F$ permettent le découplage des alimentations (suppression des composantes haute fréquence parasites). Les tensions d'entrée doivent être inférieures aux tensions d'alimentation. Nous nous limiterons à $\pm 12 V$ pour $|x|_{max}$ et $|y|_{max}$.
> 	==**Un multiplieur analogique réalise l'opération : $\displaystyle w(t) = \frac{x(t)y(t)}{E_0} + z(t)$.**==
> - Multiplication d'un signal par une constante : Appliquons $y(t) = U_1$ la tension constante délivrée par une alimentation stabilisée et $x(t) = u_2(t)$ la tension variable délivrée par un générateur basse fréquence. Étudions le signal de sortie $w(t)$ pour $u_2(t)$ sinusoïdal de fréquence 1 kHz et d’amplitude 5 V avec différentes valeurs de $U_1$. Nous remarquons sur la [[#^figure3|figure 3]] que $w(t)$ est proportionnel à $u_2(t)$.
> En utilisant l'oscilloscope en mode $XY$ avec $X$ pour $u_2(t)$ et $Y$ pour $w(t)$, nous obtenons les caractéristiques de transfert du montage pour différentes valeurs de $U_1$ ([[#^figure4|fig. 4]]).
> Ce sont des segments de droite de pente proportionnelle à $U_1$.
> ==**Si le signal $y(t)$ est constant, le montage est linéaire.**==
> Le montage est un amplificateur de tension dont le gain est commandé par une tension.
> Choisissons un signal $u_2(t)$ non sinusoïdal (signal créneau, par exemple) et analysons les spectres de $u_2(t)$ et $w(t)$. Ils sont identiques à une constante multiplicative prés ([[#^figure5|fig. 5]]).
> ==**La multiplication d’un signal par une constante s’effectue sans enrichissement du spectre : c’est une opération linéaire.**==

> [!note] Multiplieur analogique : Mise en évidence des défauts
> L’AD633 est un multiplieur performant. Ses défauts sont donc peu visibles.
> - Bande passante : Comme pour tout amplificateur, la bande passante de l'AD633 est limitée et sa vitesse de balayage est finie. Gardons le montage précédent avec un signal d’entrée $u_2(t)$ sinusoïdal. Ajustons son amplitude pour obtenir un signal de sortie d’amplitude faible (< 1 V). Nous observons que le gain chute de 3 dB vers 1 MHz (la bande passante typique de l'AD633 est de 1 MHz) ([[#^figure6|fig. 6]]). Pour un signal de sortie d’amplitude importante (10 V par exemple), nous remarquons qu’à haute fréquence le signal de sortie devient triangulaire. Ceci est dû à la vitesse de balayage finie du circuit intégré. En mesurant la pente de $w(t)$ à haute fréquence, nous trouvons une valeur de $20 V.\mu s^{-1}$ environ ([[#^figure7|fig. 7]]).
> - Tension de décalage en entrée : Les étages différentiels d’entrée $X$ ou $Y$ présentent le même défaut que celui des amplificateurs opérationnels. Une tension différentielle d’entrée nulle ne donne pas un signal de sortie nul.
> La relation entre la sortie et les différentes entrées est : $w(t) = \frac{(x(t) + X_0)(y(t) + Y_0)}{E_0} + z(t) + Z_0$, où $X_0$, $Y_0$ et $Z_0$ représentent les différentes tensions de décalage.
> La tension de décalage $Z_0$ a pour effet d’introduire une composante continue au signal de sortie. Les tensions de décalage $X_0$ et $Y_0$ sont plus gênantes, car elles interviennent dans le terme produit en y ajoutant des termes proportionnels au signal sur l'autre entrée tels que : $\frac{X_0y(t)}{E_0}$ ou $\frac{Y_0x(t)}{E_0}$.
> Le constructeur prend un soin particulier à limiter ces défauts. Nous ne pourrons donc que mesurer un ordre de grandeur des tensions de décalage, car leurs effets sont noyés dans le bruit du multiplieur.
> Utilisons le même montage en prenant $U_1$ nulle (les entrées $Y_1$ et $Y_2$ sont reliées à la masse) et $u_2(t)$ sinusoïdal de fréquence 1 kHz et d’amplitude 10 V. La relation entre l'entrée et la sortie est : $w(t) = \frac{Y_0}{E_0}u_2(t) + Z_0 + \frac{X_0Y_0}{E_0}$.
> Nous observons une tension de sortie non exactement nulle ([[#^figure8|fig. 8]]) qui s’analyse en une superposition d’un signal de bruit, d’une sinusoïde d’amplitude $\frac{Y_0U_{2\,max}}{E_0} \approx 5 mV$ et d’une composante continue de valeur $Z_0 + \frac{X_0Y_0}{E_0}$ du même ordre de grandeur.
> Nous déduisons que $Y_0$ et $Z_0$ sont de l'ordre de grandeur de 5 mV, car le produit $\frac{X_0Y_0}{E_0}$ est négligeable devant $Z_0$.
> En permutant les entrées $X$ et $Y$ du multiplieur, nous pouvons mesurer $X_0$.
> Les défauts liés aux tensions de décalage sont négligeables dés que le signal de sortie est supérieur à 100 mV.
> ==**Les défauts du multiplieur peuvent généralement être négligés.**==

> [!note] Multiplication d'un signal par lui-même
> - Cas d'un signal sinusoïdal : Réalisons le montage de [[#^figure9|figure 9]] et observons le signal de sortie pour un signal d’entrée sinusoïdal de fréquence $f_0 = 1 kHz$ et d’amplitude 8 V ([[#^figure10|fig. 10]]). A la sortie, nous obtenons un signal $w(t)$ sinusoïdal de fréquence double, d’amplitude 3,2 V superposé à une composante continue de 3,2 V.
> Le résultat est en accord avec la relation $w(t) = \frac{u(t)^{2}}{E_0}$.
> En effet si $u = u_m\cos\omega t$ : $w(t) = \frac{u_{m}^{2}}{2E_0} + \frac{u_{m}^{2}}{2E_0}\cos 2\omega t$ avec $\frac{u_{m}^{2}}{2E_0} = 3,2 V$.
> Le spectre de $w(t)$ est différent de celui de $u(t)$ ([[#^figure11|fig. 11]]) : nous observons deux raies, l'une à fréquence nulle et l'autre de fréquence $2f_0$.
> ==**Cette opération est non linéaire : les spectres du signal et de son carré sont différents.**==
> - Moyenne quadratique : Le calcul de la puissance moyenne associée à un signal $s(t)$ nécessite la connaissance de sa valeur quadratique moyenne $\langle s^{2}(t)\rangle$. Cette grandeur est donc très importante.
> La valeur efficace vraie (R.M.S. : root mean square) $S = \sqrt{\langle s^{2}(t)\rangle}$ est proportionnelle à l'amplitude du signal.
> Cependant, la constante de proportionnalité dépend de la forme du signal.
> La relation $U_{eff} = \frac{U_m}{\sqrt{2}}$ utilisée pour les signaux sinusoïdaux n’est pas généralisable.
> Comment obtenir $\langle \frac{u(t)^{2}}{E_0}\rangle$ à partir de $\frac{u(t)^{2}}{E_0}$ ?
> Il n’est pas garanti qu’un voltmètre continu indique la composante continue, donc la moyenne de $\frac{u(t)^{2}}{E_0}$.
> ==**L'utilisation d’un filtre passe-bas permet d’accéder à la valeur quadratique moyenne du signal.**==
> En effet, un filtre passe-bas ne laisse passer que la composante continue d’un signal de fréquence $f_0$ très supérieure à sa fréquence de coupure haute $f_H$ (cf. [[02-Étude fréquentielle des systèmes linéaires|chapitre 2]]). En réalisant un montage dont le diagramme fonctionnel est donné sur la [[#^figure12|figure 12]], nous observons $s(t) = \langle \frac{u(t)^{2}}{E_0}\rangle$ à condition que la fréquence $f_0$ de $u(t)$ soit très supérieure à $f_H$.

> [!note] Modulation d'amplitude : Produit de deux signaux sinusoïdaux
> Réalisons le montage de [[#^figure13|figure 13]], où les deux sources $s(t)$ (signal) et $p(t)$ (porteuse) sont sinusoïdales et de fréquences différentes $f_p > f_s$ : $s(t) = s_m\cos(2\pi f_st + \varphi_s)$ et $p(t) = p_m\cos(2\pi f_pt)$. Le signal $w(t)$ est proportionnel à : $s_mp_m\cos(2\pi f_st + \varphi_s)\cos(2\pi f_pt)$ et s'écrit : $w(t) = \frac{1}{2E_0}s_mp_m[\cos(2\pi(f_p - f_s)t - \varphi_s) + \cos(2\pi(f_p + f_s)t + \varphi_s)]$.
> ==**Le spectre produit signal sinusoïdal-porteuse présente donc deux raies symétriques par rapport à $f_p$, d’amplitude égale et de fréquences $f_p + f_s$ et $f_p - f_s$ ([[#^figure14|fig. 14]]).**==
> Observons le signal de sortie du multiplieur $w(t)$ suivant les valeurs de $f_s$.
> - Si $f_s \ll f_p$, nous observons un signal sinusoïdal de fréquence $f_p$, présentant un phénomène de battements à la fréquence $f_s$ ([[#^figure15|fig. 15]]). $w(t)$ peut s’interpréter comme un signal de fréquence $f_p$ dont l'amplitude varie sinusoïdalement à la fréquence $f_s$ : modulation en amplitude de $p(t)$ par $s(t)$.
> - Dans le cas où $f_p$ et $f_s$ sont voisines, la fréquence $f_p - f_s$ est très inférieure à $f_p + f_s$. Nous voyons donc la somme d'un signal de fréquence voisine de $2f_p$ (ou $2f_s$) et d'un signal basse fréquence de fréquence $f_p - f_s$ ([[#^figure16|fig. 16]]).

> [!note] Modulation d'amplitude : Modulation d'une porteuse sinusoïdale par un signal quelconque
> Généralisons les résultats précédents au cas d'un signal quelconque.
> - Bande spectrale utile d'un signal quelconque : Le signal $s(t)$ est décomposable en une somme de signaux sinusoïdaux :
> 	- si $s(t)$ est périodique de fréquence $f_0$, nous pouvons l'exprimer par son développement en série de Fourier : $\displaystyle s(t) = \sum_{n}a_n\cos(2\pi nf_0t + \varphi_n)$ ;
> 	- si $s(t)$ n'est pas périodique, il est possible de l'écrire sous la forme d'une intégrale de Fourier : $\displaystyle s(t) = \int_{0}^{\infty}S(f)\cos[2\pi ft + \varphi(f)]df$.
> 	
> 	Dans les deux cas, le spectre théorique peut s’étendre jusqu’aux valeurs infinies de la fréquence. En pratique, ce spectre est limité à une bande de fréquences pour deux raisons :
> 	- les amplitudes $a_n$ des composantes du développement en série de Fourier ou l’amplitude $S(f)$ tendent généralement vers 0 pour les hautes fréquences ;
> 	- les composantes utiles sont limitées par les instruments de mesure. Par exemple, le spectre utile d’un signal audio est limité par le domaine de sensibilité de l’oreille humaine qui s’étend approximativement de 20 Hz à 20 kHz.
> 
> 	==**Un signal quelconque physiquement réalisable peut se décomposer en une somme de fonctions sinusoïdales dont le spectre utile constitue une bande de fréquences comprise entre une fréquence minimale $f_1$ et une fréquence maximale $f_2$.**==
> - Analyse fréquentielle du signal modulé : Le spectre de $s(t)$ s’étend entre les fréquences $f_1$ et $f_2$ ; le spectre de chaque composante de fréquence $f$ crée deux raies dans le spectre produit, l’une de fréquence $f_p + f$ (spectre somme), l’autre de fréquence $|f_p - f|$ (spectre différence).
> 	- Si $f_2 < f_p$, les deux raies sont symétriques par rapport à $f_p$. Donc, si le spectre de $s(t)$ est limité à des fréquences inférieures à $f_p$ $(f_2 < f_p)$, le spectre de $w(t)$ est composé de deux parties :
> 		- un **spectre somme** identique a celui de $s(t)$ mais translaté de $f_p$, appelé bande latérale supérieure (upper side bande) ;
> 		- un spectre différence, ou **spectre miroir**, symétrique du spectre somme par rapport à $f_p$ appelé bande latérale inférieure (lower side bande) ([[#^figure17|fig. 17]]).
> 	- Si $f_2 > f_p$, la raie différence a pour fréquence $(f - f_p)$ pour $f_p < f < f_2$. Elle n'est plus symétrique de la raie somme $(f + f_p)$. Les harmoniques de $s(t)$ de fréquence supérieure à $f_p$ donnent un spectre miroir replié ([[#^figure18|fig. 18]]).
> 	
> 	==**Le produit d’un signal $s(t)$ par une porteuse $p(t)$ est composé de deux parties : un spectre somme identique à celui de $s(t)$ mais translaté de $f_p$ et un spectre différence, ou spectre miroir, symétrique du spectre somme par rapport à $f_p$.**==
> 	==**Si le spectre signal modulant $s(t)$ s’étend au-delà de $f_p$, le spectre miroir est replié.**==

> [!note] Modulation d'amplitude : Modulation d'amplitude d'une porteuse
> Le produit porteuse-signal de modulation ne présente pas de raie à la fréquence $f_p$ si le signal de modulation $s(t)$ n’a pas de composante continue. En particulier, si $s(t)$ est nul, le signal obtenu l’est aussi.
> Pour cette raison, le montage de [[#^figure13|figure 13]] est appelé **modulateur équilibré**.
> L’absence de composante de porteuse dans le signal modulé ne permet pas une récupération simple de l’information. En outre, l’amplitude du signal reçu $w(t) = ks(t)p(t)$ est égale à celle du signal émis à une constante multiplicative inconnue près $k$. L’amplitude du signal modulant n’est donc accessible que de façon relative.
> En revanche, la présence de porteuse permet d’obtenir une valeur de référence d’amplitude.
> ==**Un signal est dit modulé en amplitude lorsqu’il est la somme de la porteuse et du produit porteuse-signal modulant.**==
> Un signal modulé sinusoïdalement en amplitude s’écrit : $s(t) = s_0(1 + m\cos(2\pi f_st))\cos(2\pi f_pt)$, où $m$ est le taux de modulation en général inférieur à 1 ([[#^figure19|fig. 19]]).
> Remarquons que, dans un signal modulé en amplitude, l'information est redondante à cause de la présence de deux spectres symétriques ([[#^figure20|fig. 20]]).
> Il est possible d’éliminer, par exemple, le spectre différence et la porteuse pour ne conserver que le spectre somme des fréquences.
> Ce principe est utilisé en modulation dite B.L.U. (bande latérale unique) ([[#^figure21|fig. 21]]). Il présente deux avantages :
> - la division par deux de la largeur du domaine de fréquences utilisées ;
> - la diminution de la puissance nécessaire à l'émetteur.
> 
> Ce type de modulation B.L.U est utilisé, entre autre, par les radioamateurs.


# Définitions

# Diagrammes
Schéma fonctionnel du multiplieur analogique AD633
![[electronique2/attachments-electronique2/figure131.png]]^figure1

Montage d'utilisation du multiplieur AD633
![[electronique2/attachments-electronique2/figure132.png]]^figure2

Montage réalisant la multiplication d'un signal sinusoïdal par lui-même
![[electronique2/attachments-electronique2/figure139.png]]^figure9

La valeur moyenne de $u_2(t)$ s'obtient par filtrage passe-bas
![[electronique2/attachments-electronique2/figure142.png]]^figure12

Montage réalisant le produit de deux signaux
![[electronique2/attachments-electronique2/figure143.png]]^figure13
# Graphiques
Réponses temporelles du multiplieur utilisé avec des tensions d'entrée $U_1$ constantes
![[electronique2/attachments-electronique2/figure133.png]]^figure3

Caractéristiques de transfert du multiplieur utilisé avec une tension d'entrée $U_1$ constante
![[electronique2/attachments-electronique2/figure134.png]]^figure4

La multiplication d'un signal par une constante s'effectue sans enrichissement du spectre
![[electronique2/attachments-electronique2/figure135.png]]^figure5

La bande passante du multiplieur AD633 est de l'ordre du mégahertz
![[electronique2/attachments-electronique2/figure136.png]]^figure6

En haute fréquence, la vitesse de balayage finie du multiplieur triangularise les signaux de sortie $w(t)$
![[electronique2/attachments-electronique2/figure137.png]]^figure7

Quand l'une des entrées du multiplieur est à la masse, le signal de sortie est particulièrement bruité
![[electronique2/attachments-electronique2/figure138.png]]^figure8

Signal sinusoïdal $u(t)$ et celui de son carré : $w(t) = \frac{u^{2}(t)}{E_0}$
![[electronique2/attachments-electronique2/figure140.png]]^figure10

Le spectre d'un signal sinusoïdal et celui de son carré sont différents
![[electronique2/attachments-electronique2/figure141.png]]^figure11

Le produit de deux signaux sinusoïdaux de fréquence $f_p$ et $f_s$ donne un signal dont le spectre contient les raies $(f_p - f_s)$ et $(f_p + f_s)$
![[electronique2/attachments-electronique2/figure144.png]]^figure14

Signal produit de deux signaux de fréquences très différentes : battements ou modulation d'amplitude
![[electronique2/attachments-electronique2/figure145.png]]^figure15

Signal produit de deux signaux de fréquences voisines
![[electronique2/attachments-electronique2/figure146.png]]^figure16

Si $f_2 < f_p$, le spectre produit comprend une bande latérale supérieure et une bande latérale inférieure symétriques par rapport à $f_p$
![[electronique2/attachments-electronique2/figure147.png]]^figure17

Si $f_2 > f_p$, il y a recouvrement des spectres somme et différence et repliement du spectre différence
![[electronique2/attachments-electronique2/figure148.png]]^figure18

a. Modulation d'amplitude : $m < 1$ $(m = 0,5)$. b. Surmodulation $m > 1$ $(m = 2)$
![[electronique2/attachments-electronique2/figure149.png]]^figure19

L'information contenue dans le spectre somme est redondante avec celle contenue dans le spectre différence
![[electronique2/attachments-electronique2/figure150.png]]^figure20

Principe de la modulation B.L.U.
![[electronique2/attachments-electronique2/figure151.png]]^figure21
# Expériences

# Autres notes
