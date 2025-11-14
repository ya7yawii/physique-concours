---
titre: "[[08-Fonctions de transfert des réseaux linéaires]]"
tags:
aliases:
crée: 14-11-2025, 14:38
---
# Formules
> [!note] Réponse d'un circuit (R, C) en régime harmonique
> Étudions le circuit (R, C ) représenté sur la [[#^figure1|figure 1]], alimenté par un générateur sinusoïdal. Nous définissons la tension d’entrée $u_1(t)$ et la tension de sortie $u_2(t)$. Nous l’étudions ici en régime forcé et en sortie ouverte : aucun dipôle n’est branché entre les bornes de sortie et donc $i_2 = 0$.
> Nous reconnaissons le diviseur de tension, ce qui permet d’écrire : $\displaystyle\underline{u}_{2m} = \frac{\frac{1}{jC\omega}}{R + \frac{1}{jC\omega}}\underline{u}_{1m}$.
> La [[#^info1|fonction de transfert]] est le rapport des amplitudes complexes de $u_2$ et $u_1$ : $\underline{H}(j\omega) = \frac{\underline{u}_{2m}}{\underline{u}_{1m}}$. Le module $H(\omega) = |\underline{H}(j\omega)|$ (grandeur positive) et le déphasage de $u_2(t)$ par rapport à $u_1(t)$, $\varphi(\omega)$ défini par $\underline{H}(j\omega) = H(\omega)e^{j\varphi(\omega)}$, sont fonction de la fréquence.
> Ce circuit est appelé filtre car il transmet différemment des signaux harmoniques de fréquences différentes.
> Forme réduite : Notons $x = \frac{\omega}{\omega_0} = RC\omega$ la pulsation réduite du filtre. Avec cette notation la fonction de transfert devient : $\underline{H}(jx) = \frac{1}{1 + jx}$.
> Définition du gain : Le rapport $H(\omega)$ des amplitudes est généralement exprimé dans une échelle logarithmique. Par définition, le gain en tension, exprimé en décibels, est : $G_{dB} = 20\log H$ ($\log X$ étant le logarithme décimal du nombre $X$). Pour le circuit étudié : $G(dB) = -10\log(1 + x^{2})$. L’utilisation de l’échelle logarithmique permet de traiter avec autant de précision les faibles et les fortes amplitudes : la multiplication par 10 de $H$ se traduit par un accroissement du gain de 20 dB, quelle que soit sa valeur initiale. Signalons enfin que l’œil et l’oreille ont une sensibilité beaucoup plus proche d’une échelle logarithmique que d’une échelle linéaire.
> 
> Remarque : La fonction de transfert étudiée correspond au circuit (R, C) de la [[#^figure1|figure 1]] lorsque la sortie est ouverte. Nous ne pouvons donc l’utiliser que si l’impédance du circuit d’utilisation est quasi infinie : oscilloscope, voltmètre numérique. Dans le cas contraire il faut modifier la fonction de transfert.
> Nous pouvons aussi nous affranchir de ce problème avec un suiveur en sortie ([[#^figure8|fig. 8]]). Les tensions $u_2$ et $u_3$ sont égales avec $i_+ = 0$.

> [!note] Diagramme de Bode
> Le diagramme de Bode ne se construit que si le système est stable.
> Un diagramme de Bode ([[#^figure3|fig. 3]]) est la représentation d’une fonction de transfert à l'aide des deux courbes suivantes :
> - courbe de réponse en gain donnant les variations du gain en fonction de la fréquence ou de la pulsation exprimée dans une échelle logarithmique $X = \log(\omega)$ ou $X = \log(f)$ ;
> - courbe de réponse en phase donnant les variations de déphasage $\varphi(\omega)$ en fonction de la même variable X.
> 
> Par définition, une décade est un intervalle de fréquences $[f_1 ; f_2]$ ou de pulsations $[\omega_1 ; \omega_2]$ tel que : $\frac{f_2}{f_1} = \frac{\omega_2}{\omega_1} = 10$ ou $\log(f_2) - \log(f_1) = 1$ et un octave un intervalle de fréquences $[f_1 ; f_2]$ ou de pulsations $[\omega_1 ; \omega_2]$ tel que : $\frac{f_2}{f_1} = \frac{\omega_2}{\omega_1} = 2$ ou $\log(f_2) - \log(f_1) = 0,3$.
> En électronique, l’intervalle de fréquences utilisé s’étend du continu à plusieurs gigahertz $(10^{9} Hertz)$. C’est un intervalle très étendu qui nécessite l’utilisation d’une échelle logarithmique pour conserver une lisibilité sur tout l’intervalle utilisé d’où l’usage du papier logarithmique pour les tracés de courbes de réponse en fonction de la fréquence. L’axe des fréquences (ou des pulsations) bien que gradué en fréquences (ou en pulsations) utilise comme abscisse $X = \log(f)$ \[ou $X = \log(\omega)$ ] ([[#^figure4|fig. 4]]).
> 
> - Courbe de fréquence de réponse en gain du filtre (R, C) : Aux très basses fréquences, la capacité $C$ se comporte comme un interrupteur ouvert. Il en résulte que $\underline{u}_{1m} = \underline{u}_{2m}$ et par suite $G = 0$. La courbe de réponse en gain admet l’asymptote $G = 0$ en basse fréquence ([[#^figure5|fig. 5]]). Aux très hautes fréquences, la capacité $C$ se comporte comme un court-circuit : $\underline{u}_{2m} = 0$ avec $\underline{u}_{1m} \neq 0$, d’où $G \rightarrow -\infty$. En haute fréquence, la courbe de réponse en gain admet une asymptote passant par l’origine et de pente $p = -20\, \text{dB/décade}$ ([[#^figure5|fig. 5]]).
> 	- Diagramme asymptotique : En limitant les asymptotes B.F. et H.F. à leur point de concours A, nous obtenons la représentation asymptotique du gain.
> 	Évaluons la qualité de cette représentation asymptotique. La courbe de réponse en gain, qui est confondue avec ses asymptotes lorsque $X \rightarrow \pm\infty$, s’en détache quand $X$ prend des valeurs finies. C’est au niveau du point anguleux $A(x = 1)$ que l’écart $\Delta G$ entre la courbe de réponse en gain et sa représentation asymptotique est maximal : $\Delta G = G_A - G(1) = 0 + 10\log(1+1) = 3\,dB$. Cet écart est faible et la représentation asymptotique du gain est considérée comme satisfaisante.
> 	- Identification du type de filtrage : La courbe de réponse en gain montre que les pulsations inférieures à $\omega_0(x < 1)$ sont transmises avec une atténuation inférieure à 3 dB , alors qu’au-delà de $\omega_0(x > 1)$, elles sont atténuées de 20 dB/décade. Un filtre pour lequel le gain est uniforme pour toutes les basses fréquences et qui coupe les hautes fréquences est appelé filtre passe-bas. La variable $j\omega$ n’intervient qu’à la puissance 1 (pas de terme en $\omega^{2}$, $\omega^{3}$ etc.) ; le filtre est dit du premier ordre.
> 	<mark style="color: red">Le quadripôle étudié (filtre (R, C )) est donc un filtre passe-bas du premier ordre.</mark>
> - Courbe de réponse en phase : Le déphasage de la tension de sortie par rapport à celle d’entrée est : $\varphi(x) = -\arctan(x)$, soit $-\frac{\pi}{2} < \varphi(x) < 0$ car $x > 0$. Si $X \rightarrow -\infty$ $(x \rightarrow 0)$, la valeur asymptotique du déphasage en basse fréquence est $\varphi = 0$ ([[#^figure6|fig. 6]]). La courbe de réponse en phase admet une asymptote d’équation $\varphi = 0$ en basse fréquence. Si $X \rightarrow +\infty$ $(x \rightarrow \infty)$, la valeur asymptotique du déphasage en haute fréquence est $\varphi = -\frac{\pi}{2}$.
> 	- Diagramme asymptotique : Le diagramme asymptotique formé des deux asymptotes $\varphi = 0$ et $\varphi = -\frac{\pi}{2}$ est insuffisant pour décrire les variations du déphasage$\varphi(\omega)$ lorsque la pulsation varie de zéro à l’infini. Il est généralement complété par le segment $A_1AA_2$ décrivant le déphasage qui s’effectue, pour l’essentiel, au voisinage de $X = 0$ ([[#^figure7|fig. 7]]). Dans un tel diagramme, la rotation de phase s’effectue sur deux décades autour de $X = 0$, avec une valeur de $-\frac{\pi}{4}$ rad/décade. L’écart maximal entre ce diagramme asymptotique et la réponse en phase est $|\Delta\varphi| < 6\degree$. Cette erreur est négligeable dans la pratique.


# Définitions
> [!note] Quadripôle
> Un quadripôle ([[#^figure2|fig. 2]]) est un ensemble qui présente deux bornes d’entrée et deux bornes de sortie.
> La fonction de transfert d’un quadripôle ne peut être définie que si le système est stable. A priori, tout quadripôle passif est stable (c’est-à-dire que les tensions ne divergent pas).
> Si nous étudions les tensions : $\underline{H}(j\omega) = \frac{\underline{u}_{2m}}{\underline{u}_{1m}}$.
> Un filtre est un quadripôle conçu pour transmettre sélectivement les diverses fréquences de la grandeur harmonique.
> Si le quadripôle est linéaire, $\underline{H}(j\omega)$ peut toujours s’écrire sous la forme : $\underline{H}(j\omega) = \frac{N(j\omega)}{D(j\omega)}$, $N$ et $D$ étant des polynômes à coefficients réels. L'ordre du filtre est égal au degré le plus élevé de ces deux polynômes.

==**Filtre passif et filtre actif**==
Un filtre est passif s’il n’est constitué que de dipôles passifs (résistances, bobines et condensateurs). Il est actif s’il contient un amplificateur alimenté par une source extérieure au circuit.
# Diagrammes
Filtre (R, C)
![[figure172.png]]^figure1

Quadripôle : $u_1$ est la tension d’entrée ; $u_2$ est la tension de sortie ; $i_1$ est le courant d’entrée ; $i_2$ est le courant de sortie
![[figure173.png]]^figure2

Le courant $i_+$ étant nul la fonction de transfert du filtre est égale à $\frac{1}{1 + jRC\omega}$ quelque soit la valeur de $R_0$
![[figure179.png]]^figure8
# Graphiques
Diagramme de Bode : a. courbe de réponse en gain ; b. courbe de réponse en phase
![[figure174.png]]^figure3

Principe d’une échelle logarithmique
![[figure175.png]]^figure4

Courbe de réponse en gain (en bleu) et diagramme asymptotique (en noir) d’un passe-bas d’ordre un
![[figure176.png]]^figure5

Le diagramme asymptotique formé des deux asymptotes $\varphi = 0$ et $\varphi = -\frac{\pi}{2}$ est insuffisant pour décrire la rotation de phase
![[figure177.png]]^figure6

Diagramme asymptotique de la courbe de réponse en phase d’un passe-bas d’ordre un
![[figure178.png]]^figure7
# Expériences

# Autres notes
> [!warning]
> L’usage le plus répandu consiste à noter la fonction de transfert comme une fonction complexe de la variable complexe $j\omega$ et non comme une fonction complexe de la variable réelle $\omega$.
^info1

> [!warning] A retenir
> - $\log 2 = 0,3$
> - $\log 3 = 0,48 \approx 0,5$ (à rapprocher de $3^{2} \approx 10$)
> - Diviser $H$ par $\sqrt{2}$ revient à retrancher 3 dB au gain : $20\log\frac{H}{\sqrt{2}} = 20\log(H) - 10\log2$
> - Diviser $H$ par 10 revient à retrancher 20 dB au gain : $20\log\frac{H}{10} = 20\log(H) - 20\log10$.