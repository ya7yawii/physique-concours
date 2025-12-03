---
titre: "[[06-Multiplication de signaux]]"
tags:
  - multiplieur-analogique
  - modulation-d-amplitude
  - détection-synchrone
  - mesure-d-impédance
crée: 01-12-2025, 20:42
---
# Formules
> [!note] Multiplieur analogique
> La multiplication de deux signaux est très utilisée en électronique. De nombreux circuits intégrés ont été conçus dans ce but. L'AD633 fait partie des multiplieurs analogiques capables de réaliser la multiplication de deux tensions.
> - Présentation de l'AD633 : Étudions son schéma fonctionnel ([[#^figure1|fig. 1]]). Il comporte :
> 	- deux entrées différentielles $X_1$, $X_2$ et $Y_1$, $Y_2$ à haute impédance d'entrée $(> 10 M\Omega)$ ;
> 	- un circuit multiplieur réalisant l'opération $\frac{x(t)y(t)}{E_0}$, où $E_0$ est une tension de référence fixée à 10 V par le constructeur ;
> 	- un sommateur ajoutant la tension $z(t)$ au résultat ;
> 	- un suiveur de faible impédance de sortie, protégé en courant $(I_{max} = 30 mA)$ contre les courts-circuits ;
> 	- deux bornes pour une alimentation symétrique de $\pm 8 V$ à $\pm 18 V$, la valeur typique étant de $\pm 15 V$.
> 
> 	L'opération réalisée par le circuit est donc : $w(t) = \frac{x(t)y(t)}{E_0} + z(t)$ avec $E_0 = 10 V$.
> 	Le montage multiplieur que nous utiliserons est donné sur la [[#^figure2|figure 2]].
> 	Les condensateurs de $0,1 \mu F$ permettent le découplage des alimentations (suppression des composantes haute fréquence parasites). Les tensions d'entrée doivent être inférieures aux tensions d'alimentation. Nous nous limiterons à $\pm 12 V$ pour $|x|_{max}$ et $|y|_{max}$.
> 	==**Un multiplieur analogique réalise l'opération : $\displaystyle w(t) = \frac{x(t)y(t)}{E_0} + z(t)$.**==
> - Multiplication d'un signal par une constante : Appliquons $y(t) = U_1$ la tension constante délivrée par une alimentation stabilisée et $x(t) = u_2(t)$ la tension variable délivrée par un générateur basse fréquence. Étudions le signal de sortie $w(t)$ pour $u_2(t)$ sinusoïdal de fréquence 1 kHz et d'amplitude 5 V avec différentes valeurs de $U_1$. Nous remarquons sur la [[#^figure3|figure 3]] que $w(t)$ est proportionnel à $u_2(t)$.
> En utilisant l'oscilloscope en mode $XY$ avec $X$ pour $u_2(t)$ et $Y$ pour $w(t)$, nous obtenons les caractéristiques de transfert du montage pour différentes valeurs de $U_1$ ([[#^figure4|fig. 4]]).
> Ce sont des segments de droite de pente proportionnelle à $U_1$.
> ==**Si le signal $y(t)$ est constant, le montage est linéaire.**==
> Le montage est un amplificateur de tension dont le gain est commandé par une tension.
> Choisissons un signal $u_2(t)$ non sinusoïdal (signal créneau, par exemple) et analysons les spectres de $u_2(t)$ et $w(t)$. Ils sont identiques à une constante multiplicative prés ([[#^figure5|fig. 5]]).
> ==**La multiplication d'un signal par une constante s'effectue sans enrichissement du spectre : c'est une opération linéaire.**==

> [!note] Multiplieur analogique : Mise en évidence des défauts
> L'AD633 est un multiplieur performant. Ses défauts sont donc peu visibles.
> - Bande passante : Comme pour tout amplificateur, la bande passante de l'AD633 est limitée et sa vitesse de balayage est finie. Gardons le montage précédent avec un signal d'entrée $u_2(t)$ sinusoïdal. Ajustons son amplitude pour obtenir un signal de sortie d'amplitude faible (< 1 V). Nous observons que le gain chute de 3 dB vers 1 MHz (la bande passante typique de l'AD633 est de 1 MHz) ([[#^figure6|fig. 6]]). Pour un signal de sortie d'amplitude importante (10 V par exemple), nous remarquons qu'à haute fréquence le signal de sortie devient triangulaire. Ceci est dû à la vitesse de balayage finie du circuit intégré. En mesurant la pente de $w(t)$ à haute fréquence, nous trouvons une valeur de $20 V.\mu s^{-1}$ environ ([[#^figure7|fig. 7]]).
> - Tension de décalage en entrée : Les étages différentiels d'entrée $X$ ou $Y$ présentent le même défaut que celui des amplificateurs opérationnels. Une tension différentielle d'entrée nulle ne donne pas un signal de sortie nul.
> La relation entre la sortie et les différentes entrées est : $w(t) = \frac{(x(t) + X_0)(y(t) + Y_0)}{E_0} + z(t) + Z_0$, où $X_0$, $Y_0$ et $Z_0$ représentent les différentes tensions de décalage.
> La tension de décalage $Z_0$ a pour effet d'introduire une composante continue au signal de sortie. Les tensions de décalage $X_0$ et $Y_0$ sont plus gênantes, car elles interviennent dans le terme produit en y ajoutant des termes proportionnels au signal sur l'autre entrée tels que : $\frac{X_0y(t)}{E_0}$ ou $\frac{Y_0x(t)}{E_0}$.
> Le constructeur prend un soin particulier à limiter ces défauts. Nous ne pourrons donc que mesurer un ordre de grandeur des tensions de décalage, car leurs effets sont noyés dans le bruit du multiplieur.
> Utilisons le même montage en prenant $U_1$ nulle (les entrées $Y_1$ et $Y_2$ sont reliées à la masse) et $u_2(t)$ sinusoïdal de fréquence 1 kHz et d'amplitude 10 V. La relation entre l'entrée et la sortie est : $w(t) = \frac{Y_0}{E_0}u_2(t) + Z_0 + \frac{X_0Y_0}{E_0}$.
> Nous observons une tension de sortie non exactement nulle ([[#^figure8|fig. 8]]) qui s'analyse en une superposition d'un signal de bruit, d'une sinusoïde d'amplitude $\frac{Y_0U_{2\,max}}{E_0} \approx 5 mV$ et d'une composante continue de valeur $Z_0 + \frac{X_0Y_0}{E_0}$ du même ordre de grandeur.
> Nous déduisons que $Y_0$ et $Z_0$ sont de l'ordre de grandeur de 5 mV, car le produit $\frac{X_0Y_0}{E_0}$ est négligeable devant $Z_0$.
> En permutant les entrées $X$ et $Y$ du multiplieur, nous pouvons mesurer $X_0$.
> Les défauts liés aux tensions de décalage sont négligeables dés que le signal de sortie est supérieur à 100 mV.
> ==**Les défauts du multiplieur peuvent généralement être négligés.**==

> [!note] Multiplication d'un signal par lui-même
> - Cas d'un signal sinusoïdal : Réalisons le montage de [[#^figure9|figure 9]] et observons le signal de sortie pour un signal d'entrée sinusoïdal de fréquence $f_0 = 1 kHz$ et d'amplitude 8 V ([[#^figure10|fig. 10]]). A la sortie, nous obtenons un signal $w(t)$ sinusoïdal de fréquence double, d'amplitude 3,2 V superposé à une composante continue de 3,2 V.
> Le résultat est en accord avec la relation $w(t) = \frac{u(t)^{2}}{E_0}$.
> En effet si $u = u_m\cos\omega t$ : $w(t) = \frac{u_{m}^{2}}{2E_0} + \frac{u_{m}^{2}}{2E_0}\cos 2\omega t$ avec $\frac{u_{m}^{2}}{2E_0} = 3,2 V$.
> Le spectre de $w(t)$ est différent de celui de $u(t)$ ([[#^figure11|fig. 11]]) : nous observons deux raies, l'une à fréquence nulle et l'autre de fréquence $2f_0$.
> ==**Cette opération est non linéaire : les spectres du signal et de son carré sont différents.**==
> - Moyenne quadratique : Le calcul de la puissance moyenne associée à un signal $s(t)$ nécessite la connaissance de sa valeur quadratique moyenne $\langle s^{2}(t)\rangle$. Cette grandeur est donc très importante.
> La valeur efficace vraie (R.M.S. : root mean square) $S = \sqrt{\langle s^{2}(t)\rangle}$ est proportionnelle à l'amplitude du signal.
> Cependant, la constante de proportionnalité dépend de la forme du signal.
> La relation $U_{eff} = \frac{U_m}{\sqrt{2}}$ utilisée pour les signaux sinusoïdaux n'est pas généralisable.
> Comment obtenir $\langle \frac{u(t)^{2}}{E_0}\rangle$ à partir de $\frac{u(t)^{2}}{E_0}$ ?
> Il n'est pas garanti qu'un voltmètre continu indique la composante continue, donc la moyenne de $\frac{u(t)^{2}}{E_0}$.
> ==**L'utilisation d'un filtre passe-bas permet d'accéder à la valeur quadratique moyenne du signal.**==
> En effet, un filtre passe-bas ne laisse passer que la composante continue d'un signal de fréquence $f_0$ très supérieure à sa fréquence de coupure haute $f_H$ (cf. [[02-Étude fréquentielle des systèmes linéaires|chapitre 2]]). En réalisant un montage dont le diagramme fonctionnel est donné sur la [[#^figure12|figure 12]], nous observons $s(t) = \langle \frac{u(t)^{2}}{E_0}\rangle$ à condition que la fréquence $f_0$ de $u(t)$ soit très supérieure à $f_H$.

> [!note] Modulation d'amplitude : Produit de deux signaux sinusoïdaux
> Réalisons le montage de [[#^figure13|figure 13]], où les deux sources $s(t)$ (signal) et $p(t)$ (porteuse) sont sinusoïdales et de fréquences différentes $f_p > f_s$ : $s(t) = s_m\cos(2\pi f_st + \varphi_s)$ et $p(t) = p_m\cos(2\pi f_pt)$. Le signal $w(t)$ est proportionnel à : $s_mp_m\cos(2\pi f_st + \varphi_s)\cos(2\pi f_pt)$ et s'écrit : $w(t) = \frac{1}{2E_0}s_mp_m[\cos(2\pi(f_p - f_s)t - \varphi_s) + \cos(2\pi(f_p + f_s)t + \varphi_s)]$.
> ==**Le spectre produit signal sinusoïdal-porteuse présente donc deux raies symétriques par rapport à $f_p$, d'amplitude égale et de fréquences $f_p + f_s$ et $f_p - f_s$ ([[#^figure14|fig. 14]]).**==
> Observons le signal de sortie du multiplieur $w(t)$ suivant les valeurs de $f_s$.
> - Si $f_s \ll f_p$, nous observons un signal sinusoïdal de fréquence $f_p$, présentant un phénomène de battements à la fréquence $f_s$ ([[#^figure15|fig. 15]]). $w(t)$ peut s'interpréter comme un signal de fréquence $f_p$ dont l'amplitude varie sinusoïdalement à la fréquence $f_s$ : modulation en amplitude de $p(t)$ par $s(t)$.
> - Dans le cas où $f_p$ et $f_s$ sont voisines, la fréquence $f_p - f_s$ est très inférieure à $f_p + f_s$. Nous voyons donc la somme d'un signal de fréquence voisine de $2f_p$ (ou $2f_s$) et d'un signal basse fréquence de fréquence $f_p - f_s$ ([[#^figure16|fig. 16]]).

> [!note] Modulation d'amplitude : Modulation d'une porteuse sinusoïdale par un signal quelconque
> Généralisons les résultats précédents au cas d'un signal quelconque.
> - Bande spectrale utile d'un signal quelconque : Le signal $s(t)$ est décomposable en une somme de signaux sinusoïdaux :
> 	- si $s(t)$ est périodique de fréquence $f_0$, nous pouvons l'exprimer par son développement en série de Fourier : $\displaystyle s(t) = \sum_{n}a_n\cos(2\pi nf_0t + \varphi_n)$ ;
> 	- si $s(t)$ n'est pas périodique, il est possible de l'écrire sous la forme d'une intégrale de Fourier : $\displaystyle s(t) = \int_{0}^{\infty}S(f)\cos[2\pi ft + \varphi(f)]df$.
> 	
> 	Dans les deux cas, le spectre théorique peut s'étendre jusqu'aux valeurs infinies de la fréquence. En pratique, ce spectre est limité à une bande de fréquences pour deux raisons :
> 	- les amplitudes $a_n$ des composantes du développement en série de Fourier ou l'amplitude $S(f)$ tendent généralement vers 0 pour les hautes fréquences ;
> 	- les composantes utiles sont limitées par les instruments de mesure. Par exemple, le spectre utile d'un signal audio est limité par le domaine de sensibilité de l'oreille humaine qui s'étend approximativement de 20 Hz à 20 kHz.
> 
> 	==**Un signal quelconque physiquement réalisable peut se décomposer en une somme de fonctions sinusoïdales dont le spectre utile constitue une bande de fréquences comprise entre une fréquence minimale $f_1$ et une fréquence maximale $f_2$.**==
> - Analyse fréquentielle du signal modulé : Le spectre de $s(t)$ s'étend entre les fréquences $f_1$ et $f_2$ ; le spectre de chaque composante de fréquence $f$ crée deux raies dans le spectre produit, l'une de fréquence $f_p + f$ (spectre somme), l'autre de fréquence $|f_p - f|$ (spectre différence).
> 	- Si $f_2 < f_p$, les deux raies sont symétriques par rapport à $f_p$. Donc, si le spectre de $s(t)$ est limité à des fréquences inférieures à $f_p$ $(f_2 < f_p)$, le spectre de $w(t)$ est composé de deux parties :
> 		- un **spectre somme** identique a celui de $s(t)$ mais translaté de $f_p$, appelé bande latérale supérieure (upper side bande) ;
> 		- un spectre différence, ou **spectre miroir**, symétrique du spectre somme par rapport à $f_p$ appelé bande latérale inférieure (lower side bande) ([[#^figure17|fig. 17]]).
> 	- Si $f_2 > f_p$, la raie différence a pour fréquence $(f - f_p)$ pour $f_p < f < f_2$. Elle n'est plus symétrique de la raie somme $(f + f_p)$. Les harmoniques de $s(t)$ de fréquence supérieure à $f_p$ donnent un spectre miroir replié ([[#^figure18|fig. 18]]).
> 	
> 	==**Le produit d'un signal $s(t)$ par une porteuse $p(t)$ est composé de deux parties : un spectre somme identique à celui de $s(t)$ mais translaté de $f_p$ et un spectre différence, ou spectre miroir, symétrique du spectre somme par rapport à $f_p$.**==
> 	==**Si le spectre signal modulant $s(t)$ s'étend au-delà de $f_p$, le spectre miroir est replié.**==

> [!note] Modulation d'amplitude : Modulation d'amplitude d'une porteuse
> Le produit porteuse-signal de modulation ne présente pas de raie à la fréquence $f_p$ si le signal de modulation $s(t)$ n'a pas de composante continue. En particulier, si $s(t)$ est nul, le signal obtenu l'est aussi.
> Pour cette raison, le montage de [[#^figure13|figure 13]] est appelé **modulateur équilibré**.
> L'absence de composante de porteuse dans le signal modulé ne permet pas une récupération simple de l'information. En outre, l'amplitude du signal reçu $w(t) = ks(t)p(t)$ est égale à celle du signal émis à une constante multiplicative inconnue près $k$. L'amplitude du signal modulant n'est donc accessible que de façon relative.
> En revanche, la présence de porteuse permet d'obtenir une valeur de référence d'amplitude.
> ==**Un signal est dit modulé en amplitude lorsqu'il est la somme de la porteuse et du produit porteuse-signal modulant.**==
> Un signal modulé sinusoïdalement en amplitude s'écrit : $s(t) = s_0(1 + m\cos(2\pi f_st))\cos(2\pi f_pt)$, où $m$ est le taux de modulation en général inférieur à 1 ([[#^figure19|fig. 19]]).
> Remarquons que, dans un signal modulé en amplitude, l'information est redondante à cause de la présence de deux spectres symétriques ([[#^figure20|fig. 20]]).
> Il est possible d'éliminer, par exemple, le spectre différence et la porteuse pour ne conserver que le spectre somme des fréquences.
> Ce principe est utilisé en modulation dite B.L.U. (bande latérale unique) ([[#^figure21|fig. 21]]). Il présente deux avantages :
> - la division par deux de la largeur du domaine de fréquences utilisées ;
> - la diminution de la puissance nécessaire à l'émetteur.
> 
> Ce type de modulation B.L.U est utilisé, entre autre, par les radioamateurs.

> [!note] Détection synchrone
> La démodulation d'un signal consiste à reconstituer le signal modulant à partir du signal modulé.
> - Principe de la détection synchrone : Comment récupérer le signal modulant $s(t)$ quel que soit le taux de modulation m ? Supposons que nous disposons d'un signal synchrone avec la porteuse : $p(t) = p_m\cos(2\pi f_pt)$ et du signal modulé sinusoïdalement en amplitude : $s(t) = s_0[1 + m\cos(2\pi f_st)]\cos(2\pi f_pt)$. Le produit de deux signaux s'écrit après linéarisation : 
> $$
> \begin{multline*}
> p(t)s(t) = p_ms_0\left[\frac{1}{2} + \frac{1}{2}\cos(4\pi f_pt) + \frac{m}{2}\cos(2\pi f_st) \right. \\ \left. + \frac{m}{4}\cos(2\pi(2f_p + f_s)t) + \frac{m}{4}\cos(2\pi(2f_p - f_s)t)\right].
> \end{multline*}
> $$
> Son spectre comprend une composante continue, une raie de fréquence $2f_p$ et les raies de fréquences $f_s$, $2f_p - f_s$, $2f_p + f_s$, d'amplitude proportionnelle à m.
> Ce résultat peut être généralisé à un signal modulant dont le spectre est limité à des fréquences inférieures à $f_p$.
> Nous observons une composante continue, une composante de fréquence $2f_p$ et trois spectres : l'un identique à celui du signal modulant, l'autre identique mais translaté de $2f_p$ et le troisième miroir du précédent par rapport à $2f_p$ ([[#^figure22|fig. 22]]).
> Revenons au signal $p(t)s(t)$. Il suffit de le filtrer avec un filtre passe-bas de fréquence de coupure $f_H$, très supérieure à $f_s$ et très inférieure à ($2f_p - f_s$) pour éliminer la porteuse et les deux spectres inutiles. Un passe-haut de fréquence très inférieure à $f_s$, élimine ensuite la composante continue pour récupérer le signal modulant.
> Un exemple de réalisation expérimentale est donné sur la [[#^figure23|figure 23]].
> Le produit d'un signal modulé par un signal synchrone de la porteuse donne un signal proportionnel au signal modulant après un filtrage passe-bas : $(f_s \ll f_H \ll 2f_p - f_s)$ et élimination de la composante continue.
> - Boucle à verrouillage de phase : La démodulation synchrone nécessite de disposer du même oscillateur de fréquence $f_p$ à la réception et à l'émission. Ceci n'est pas toujours réalisable.
> Supposons que l'oscillateur de démodulation présente un déphasage $\varphi(t)$ évoluant lentement au cours du temps par rapport à l'oscillateur de modulation : $p'(t) = p_{m}^{'}\cos(2\pi f_pt + \varphi(t))$.
> Pour un signal modulé du type : $s(t) = s_0[1 + m\cos(2\pi f_st)]\cos(2\pi f_pt)$, le signal à la sortie du multiplieur est : $w(t) = kp_{m}^{'}s_0\cos(2\pi f_pt)\cos(2\pi f_pt + \varphi(t))[1 + m\cos(2\pi f_st)]$, soit après linéarisation : 
> $$
> \begin{multline*}
> kp_{m}^{'}s_0\left(\frac{1}{2}\cos\varphi + \frac{1}{2}m\cos\varphi\cos(2\pi f_st) + \frac{1}{4}m\cos[2\pi(2f_p - f_s)t + \varphi(t)]\right.\\
> \left. + \frac{1}{2}\cos(4\pi f_pt + \varphi(t)) + \frac{1}{4}m\cos[2\pi(2f_p + f_s)t + \varphi(t)]\right).
> \end{multline*}
> $$
> Après un filtrage passe-bas et une élimination de la composante continue, il reste : $\frac{1}{2}ks_0p_{m}^{'}m\cos(\varphi(t))\cos(2\pi f_st)$ dont l'amplitude dépend de $\varphi(t)$. Ce déphasage varie au cours du temps, donc l'amplitude du signal de sortie n'est pas constante.
> Ce défaut, appelé "**fading**", est inacceptable.
> ==**Une boucle à verrouillage de phase permet de conserver un déphasage nul entre les oscillateurs d'émission et de réception donc de les synchroniser. Elle permet ainsi de recréer la porteuse.**==

> [!note] Détection synchrone : Signal bruité et détection synchrone
> Le principe de la détection synchrone peut être appliqué à l'étude de tout phénoméne périodique.
> Imaginons un signal comprenant une partie utile sinusoïdale $s_u(t)$ : $s_u(t) = s_0\sin(\omega t + \varphi)$ noyé dans un bruit $b(t)$ aléatoire : $s(t) = s_u(t) + b(t)$.
> On le multiplie par un signal d'extraction $a\sin\omega t$, ou $a\cos\omega t$.
> Dans le produit, le terme : $ab(t)\sin\omega t$ prend des valeurs aléatoires ; il est donc de valeur moyenne nulle, alors que le terme : $as_0\sin\omega t\sin(\omega t + \varphi)$ a pour valeur moyenne : $\frac{as_0}{2}\cos\varphi$.
> ==**Cette méthode permet de détecter un signal noyé dans un bruit d'amplitude plusieurs milliers de fois supérieure à celle du signal.**==
> La détection synchrone est aussi utilisée pour mesurer la différence de fréquence entre deux signaux.

> [!note] Mesure d'impédance
> La mesure classique d'impédance avec un voltmètre et un ampèremètre alternatifs ne donne accès ni à la résistance, ni à la réactance d'un dipôle ([[#^figure24|fig. 24]]).
> L'utilisation d'un oscilloscope permet de mesurer la valeur du déphasage entre l'intensité et la tension, et pose des problèmes de masse ([[#^figure25|fig. 25]]).
> - Mesure de la résistance d'une impédance : Considérons un dipôle alimenté par une source de courant sinusoïdale de fréquence $f$ et de pulsation $\omega$ : $i(t) = i_m\cos(\omega t)$. La tension à ses bornes est : $u(t) = u_m\cos(\omega t + \varphi) = Zi_m\cos(\omega t + \varphi)$ où $Z$ est le module de son impédance complexe $\underline{Z}(j\omega)$ et $\varphi$ son argument.
> Le produit de $u(t)$ par une tension $u_i(t) = u_{im}\cos(\omega t)$ synchrone de $i(t)$ peut être linéarisé : $u(t)u_i(t) = \frac{1}{2}u_mu_{im}(\cos\varphi + \cos(2\omega t + \varphi))$.
> Nous pouvons obtenir sa composante continue par un filtrage passe-bas de fréquence de coupure très inférieure à $2f$. Son expression est : $\frac{1}{2}u_mu_{im}\cos\varphi = \frac{1}{2}Zu_{im}i_m\cos\varphi$, soit aussi $U_iI\mathcal{R}e[\underline{Z}(j\omega)]$, où $U_i$ et $I$ sont les valeurs efficaces et $\mathcal{R}e$ la partie réelle.
> ==**La valeur moyenne du produit de la tension aux bornes d'un dipôle par une tension synchrone de son intensité est proportionnelle à la partie réelle de son impédance complexe.**==
> Pour que le principe de la mesure de la partie réelle de $Z(p)$ soit utilisable, il est nécessaire de fixer les valeurs de $i_m$ et de $u_{im}$ de façon à connaître la constante de proportionnalité. La méthode la plus simple est d'utiliser un convertisseur tension-courant tel que $i(t) = gu_i(t)$, où $g$ représente la transconductance du convertisseur.
> Nous obtenons donc le schéma fonctionnel de [[#^figure26|figure 26]]. Comme le multiplieur réalise l'opération $\frac{xy}{E_0}$, la valeur mesurée en sortie du filtre est : $W_0 = \frac{U_iI}{E_0}\mathcal{R}e[\underline{Z}(j\omega)]$.
> La résistance $\mathcal{R}e[\underline{Z}(j\omega)]$ peut donc être calculée à partir des valeurs mesurées de $U_i$ et $W_0$ : $\mathcal{R}e[\underline{Z}(j\omega)] = \frac{E_0W_0}{gU_{i}^{2}}$.
> - Mesure de la réactance d'une impédance : Le produit $u(t)$ par une tension $u_{i}^{'}(t)$, en avance de $\frac{\pi}{2}$ par rapport à $i(t)$ : $u_{i}^{'}(t) = u_{im}^{'}\cos\left(\omega t + \frac{\pi}{2}\right)$ peut être linéarisé : $u(t)u_{i}^{'}(t) = \frac{1}{2}u_{m}u_{im}^{'}\left(\cos\left(\varphi - \frac{\pi}{2}\right) + \cos\left(2\omega t + \varphi + \frac{\pi}{2}\right)\right)$.
> Le même type de filtrage que précédemment permet d'en extraire la composante continue : $\frac{1}{2}u_{m}u_{im}^{'}\left(\cos\left(\varphi - \frac{\pi}{2}\right)\right) = \frac{1}{2}u_{m}u_{im}^{'}\sin(\varphi) = \frac{1}{2}u_{im}^{'}i_{m}\sin(\varphi)$, soit $U_iI\mathcal{I}m[\underline{Z}(j\omega)]$ avec $\mathcal{I}m$ la partie imaginaire.
> ==**La valeur moyenne du produit de la tension aux bornes d'un dipôle par une tension en avance de $\frac{\pi}{2}$ par rapport à son intensité est proportionnelle à la partie imaginaire de son impédance complexe.**==
> Il « suffit » donc de déphaser de $\frac{\pi}{2}$ le signal $u_i(t)$ avant d'en faire le produit avec $u(t)$, d'où le diagramme fonctionnel ([[#^figure27|fig. 27]]).
> La valeur mesurée en sortie du filtre est $W_0 = \frac{U_iI}{E_0}\mathcal{I}m[\underline{Z}(j\omega)]$.
> La réactance $\mathcal{I}m[\underline{Z}(j\omega)]$ peut être donc calculée à partir des valeurs mesurées de $U_i$ et $W_0$ : $\mathcal{I}m[\underline{Z}(j\omega)] = \frac{E_0W_0}{gU_{i}^{2}}$.

> [!note] Mesure d'impédance : Réalisation expérimentale
> - Convertisseur tension-courant : Si le dipôle $Z$ n'a pas de borne à la masse, nous pouvons utiliser le montage de [[#^figure28|figure 28]], En régime linéaire, l'entrée - de l'amplificateur opérationnel est au potentiel 0, donc $u_i(t) = Ri(t)$. La tension de sortie de l'amplificateur opérationnel est alors $-u(t)$.
> Si le dipôle a une borne à la masse, nous devons utiliser un convertisseur tension-courant plus complexe ([[#^figure29|fig. 29]]), qui nécessite l'utilisation de résistances appariées $(i(t) = gu_i(t))$.
> - Déphaseur : Le circuit déphaseur ([[#^figure30|fig. 30]]) est réalisé à l'aide d'un filtre déphaseur (cf. [[04-Un exemple de système électronique. L'amplificateur opérationnel|chapitre 4]]). Sa fonction de transfert est $H(p) = \frac{1 - RCp}{1 + RCp}$. Il présente l'inconvénient de ne déphaser de $-\frac{\pi}{2}$ qu'à la fréquence particulière $f = \left(\frac{1}{2\pi}RC\right)$. Les mesures de réactance ne pourront être effectuées qu'à cette fréquence, qui peut être ajustée en modifiant $R$.
> - Montage complet : Le montage expérimental est représenté sur la [[#^figure31|figure 31]]. Le choix de $R$ et $C$ dépend de la fréquence du G.B.F. Avec ce montage, la partie réelle de l'impédance du dipôle vaut : $\mathcal{R}e[\underline{Z}(j\omega)] = \frac{10^{3}W_0}{U_{i}^{2}}$ (ohm).
> Si un circuit déphaseur, du type indiqué sur la [[#^figure30|figure 30]], adapté à la fréquence utilisée est inséré entre A et B, la partie imaginaire de l'impédance du dipôle vaut : $\mathcal{I}m[\underline{Z}(j\omega)] = \frac{10^{3}W_0}{U_{i}^{2}}$ (ohm).
> Le fait que le filtre déphase de $-\frac{\pi}{2}$ (et non de $\frac{\pi}{2}$) compense l'inversion de signe due au convertisseur tension-courant.
> ==**L'association d'un convertisseur tension-courant, d'un multiplieur et d'un filtre passe-bas permet de mesurer la résistance d'un dipôle. Sa réactance se mesure en introduisant un déphaseur de $\frac{\pi}{2}$ avant le multiplieur.**==
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

Exemple de réalisation d'un détecteur synchrone
![[electronique2/attachments-electronique2/figure153.png]]^figure23

Avec un voltmètre et un ampèremètre, nous ne pouvons mesurer que le module $Z$ de l'impédance
![[electronique2/attachments-electronique2/figure154.png]]^figure24

Un transformateur d'isolement est nécessaire pour la mesure du déphasage à l'aide d'un oscilloscope
![[electronique2/attachments-electronique2/figure155.png]]^figure25

Principe de la mesure de la résistance d'une impédance
![[electronique2/attachments-electronique2/figure156.png]]^figure26

Principe de la mesure de la réactance d'une impédance
![[electronique2/attachments-electronique2/figure157.png]]^figure27

Obtention des tensions $u(t)$ et $u_i(t)$ pour la mesure de la résistance du dipôle $Z(j\omega)$ quand ce dernier n'a pas de borne à la masse $(s(t) = -u(t))$
![[electronique2/attachments-electronique2/figure158.png]]^figure28

Obtention des tensions $u(t)$ et $u_i(t)$ pour la mesure de la résistance du dipôle $Z(j\omega)$ quand ce dernier a une borne à la masse
![[electronique2/attachments-electronique2/figure159.png]]^figure29

Circuit déphaseur
![[electronique2/attachments-electronique2/figure160.png]]^figure30

Réalisation expérimentale d'un circuit de mesure de la résistance et de la réactance (en insérant un déphaseur entre A et B) d'une impédance $\underline{Z}(j\omega)$ d'un dipôle
![[electronique2/attachments-electronique2/figure161.png]]^figure31
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

Spectre du signal produit porteuse-signal modulé en amplitude
![[electronique2/attachments-electronique2/figure152.png]]^figure22
# Expériences
> [!warning]
> Voici des exemples de travaux pratiques qui abordent le sujet de ce chapitre : [lien 1](https://fr.scribd.com/document/227382583/tp10multiplieur), [lien 2](http://thierryperisse.free.fr/documents/TPs-Telecoms-AM-FM-TNT/TP-mod-demod-AM/sujettpmoddemodam.pdf), [lien 3](https://pdfcoffee.com/tpn1am229-pdf-free.html), [lien 4](https://fr.scribd.com/document/697812963/TP3-AM), [lien 5](http://gensdelalune.free.fr/mp/Travaux%20pratiques/TP%20Modulation%20et%20demodulation.pdf), [lien 6](https://cpgemaroc.com/agregation/tp/TP-2-AGP/elec2-TP8.pdf), [lien 7](https://www.alloschool.com/assets/documents/course-423/modulation-d-amplitude-cours-4-1.pdf), [lien 8](https://www.f-legrand.fr/scidoc/srcdoc/sciphys/tpelectro/modamp/modamp-pdf.pdf), [lien 9](http://psi2.nantes.free.fr/TP/ENONCES-ET-CORRIGES-TP/TP-ELECTRONIQUE/ENONCE-TP-ELECTRONIQUE/TP-8-ENONCE.pdf), [lien 10](https://fr.scribd.com/document/731222848/mod), [lien 11](https://cahier-de-prepa.fr/pc-rabelais/download?id=905), [lien 12](https://fr.scribd.com/document/123605854/Detection-Synchrone), [lien 13](https://psi1montaigne.com/tp/), [lien 14](https://fr.scribd.com/document/833272250/TP4-Multiplication-des-signaux-Application-a-la-modulation-et-la-detection-synchrone).
# Autres notes
