---
titre: "[[08-Fonctions de transfert des réseaux linéaires]]"
tags:
  - passe-bas
  - passe-haut
  - filtre-intégrateur
  - filtre-dérivateur
  - fonction-de-transfert
  - diagramme-de-Bode
  - ordre-un
crée: 14-11-2025, 14:38
---
# Formules
> [!note] Réponse d'un circuit (R, C) en régime harmonique
> Étudions le circuit (R, C ) représenté sur la [[#^figure1|figure 1]], alimenté par un générateur sinusoïdal. Nous définissons la tension d'entrée $u_1(t)$ et la tension de sortie $u_2(t)$. Nous l'étudions ici en régime forcé et en sortie ouverte : aucun dipôle n'est branché entre les bornes de sortie et donc $i_2 = 0$.
> Nous reconnaissons le diviseur de tension, ce qui permet d'écrire : $\displaystyle\underline{u}_{2m} = \frac{\frac{1}{jC\omega}}{R + \frac{1}{jC\omega}}\underline{u}_{1m}$.
> La [[#^info1|fonction de transfert]] est le rapport des amplitudes complexes de $u_2$ et $u_1$ : $\underline{H}(j\omega) = \frac{\underline{u}_{2m}}{\underline{u}_{1m}}$. Le module $H(\omega) = |\underline{H}(j\omega)|$ (grandeur positive) et le déphasage de $u_2(t)$ par rapport à $u_1(t)$, $\varphi(\omega)$ défini par $\underline{H}(j\omega) = H(\omega)e^{j\varphi(\omega)}$, sont fonction de la fréquence.
> Ce circuit est appelé filtre car il transmet différemment des signaux harmoniques de fréquences différentes.
> Forme réduite : Notons $x = \frac{\omega}{\omega_0} = RC\omega$ la pulsation réduite du filtre. Avec cette notation la fonction de transfert devient : $\underline{H}(jx) = \frac{1}{1 + jx}$.
> Définition du gain : Le rapport $H(\omega)$ des amplitudes est généralement exprimé dans une échelle logarithmique. Par définition, le gain en tension, exprimé en décibels, est : $G_{dB} = 20\log H$ ($\log X$ étant le logarithme décimal du nombre $X$). Pour le circuit étudié : $G(dB) = -10\log(1 + x^{2})$. L'utilisation de l'échelle logarithmique permet de traiter avec autant de précision les faibles et les fortes amplitudes : la multiplication par 10 de $H$ se traduit par un accroissement du gain de 20 dB, quelle que soit sa valeur initiale. Signalons enfin que l'œil et l'oreille ont une sensibilité beaucoup plus proche d'une échelle logarithmique que d'une échelle linéaire.
> 
> Remarque : La fonction de transfert étudiée correspond au circuit (R, C) de la [[#^figure1|figure 1]] lorsque la sortie est ouverte. Nous ne pouvons donc l'utiliser que si l'impédance du circuit d'utilisation est quasi infinie : oscilloscope, voltmètre numérique. Dans le cas contraire il faut modifier la fonction de transfert.
> Nous pouvons aussi nous affranchir de ce problème avec un suiveur en sortie ([[#^figure8|fig. 8]]). Les tensions $u_2$ et $u_3$ sont égales avec $i_+ = 0$.

> [!note] Diagramme de Bode
> Le diagramme de Bode ne se construit que si le système est stable.
> Un diagramme de Bode ([[#^figure3|fig. 3]]) est la représentation d'une fonction de transfert à l'aide des deux courbes suivantes :
> - courbe de réponse en gain donnant les variations du gain en fonction de la fréquence ou de la pulsation exprimée dans une échelle logarithmique $X = \log(\omega)$ ou $X = \log(f)$ ;
> - courbe de réponse en phase donnant les variations de déphasage $\varphi(\omega)$ en fonction de la même variable X.
> 
> Par définition, une décade est un intervalle de fréquences $[f_1 ; f_2]$ ou de pulsations $[\omega_1 ; \omega_2]$ tel que : $\frac{f_2}{f_1} = \frac{\omega_2}{\omega_1} = 10$ ou $\log(f_2) - \log(f_1) = 1$ et un octave un intervalle de fréquences $[f_1 ; f_2]$ ou de pulsations $[\omega_1 ; \omega_2]$ tel que : $\frac{f_2}{f_1} = \frac{\omega_2}{\omega_1} = 2$ ou $\log(f_2) - \log(f_1) = 0,3$.
> En électronique, l'intervalle de fréquences utilisé s'étend du continu à plusieurs gigahertz $(10^{9} Hertz)$. C'est un intervalle très étendu qui nécessite l'utilisation d'une échelle logarithmique pour conserver une lisibilité sur tout l'intervalle utilisé d'où l'usage du papier logarithmique pour les tracés de courbes de réponse en fonction de la fréquence. L'axe des fréquences (ou des pulsations) bien que gradué en fréquences (ou en pulsations) utilise comme abscisse $X = \log(f)$ \[ou $X = \log(\omega)$ ] ([[#^figure4|fig. 4]]).
> 
> - Courbe de fréquence de réponse en gain du filtre (R, C) : Aux très basses fréquences, la capacité $C$ se comporte comme un interrupteur ouvert. Il en résulte que $\underline{u}_{1m} = \underline{u}_{2m}$ et par suite $G = 0$. La courbe de réponse en gain admet l'asymptote $G = 0$ en basse fréquence ([[#^figure5|fig. 5]]). Aux très hautes fréquences, la capacité $C$ se comporte comme un court-circuit : $\underline{u}_{2m} = 0$ avec $\underline{u}_{1m} \neq 0$, d'où $G \rightarrow -\infty$. En haute fréquence, la courbe de réponse en gain admet une asymptote passant par l'origine et de pente $p = -20\, \text{dB/décade}$ ([[#^figure5|fig. 5]]).
> 	- Diagramme asymptotique : En limitant les asymptotes B.F. et H.F. à leur point de concours A, nous obtenons la représentation asymptotique du gain.
> 	Évaluons la qualité de cette représentation asymptotique. La courbe de réponse en gain, qui est confondue avec ses asymptotes lorsque $X \rightarrow \pm\infty$, s'en détache quand $X$ prend des valeurs finies. C'est au niveau du point anguleux $A(x = 1)$ que l'écart $\Delta G$ entre la courbe de réponse en gain et sa représentation asymptotique est maximal : $\Delta G = G_A - G(1) = 0 + 10\log(1+1) = 3\,dB$. Cet écart est faible et la représentation asymptotique du gain est considérée comme satisfaisante.
> 	- Identification du type de filtrage : La courbe de réponse en gain montre que les pulsations inférieures à $\omega_0(x < 1)$ sont transmises avec une atténuation inférieure à 3 dB , alors qu'au-delà de $\omega_0(x > 1)$, elles sont atténuées de 20 dB/décade. Un filtre pour lequel le gain est uniforme pour toutes les basses fréquences et qui coupe les hautes fréquences est appelé filtre passe-bas. La variable $j\omega$ n'intervient qu'à la puissance 1 (pas de terme en $\omega^{2}$, $\omega^{3}$ etc.) ; le filtre est dit du premier ordre.
> 	<mark style="color: red">Le quadripôle étudié (filtre (R, C )) est donc un filtre passe-bas du premier ordre.</mark>
> - Courbe de réponse en phase : Le déphasage de la tension de sortie par rapport à celle d'entrée est : $\varphi(x) = -\arctan(x)$, soit $-\frac{\pi}{2} < \varphi(x) < 0$ car $x > 0$. Si $X \rightarrow -\infty$ $(x \rightarrow 0)$, la valeur asymptotique du déphasage en basse fréquence est $\varphi = 0$ ([[#^figure6|fig. 6]]). La courbe de réponse en phase admet une asymptote d'équation $\varphi = 0$ en basse fréquence. Si $X \rightarrow +\infty$ $(x \rightarrow \infty)$, la valeur asymptotique du déphasage en haute fréquence est $\varphi = -\frac{\pi}{2}$.
> 	- Diagramme asymptotique : Le diagramme asymptotique formé des deux asymptotes $\varphi = 0$ et $\varphi = -\frac{\pi}{2}$ est insuffisant pour décrire les variations du déphasage$\varphi(\omega)$ lorsque la pulsation varie de zéro à l'infini. Il est généralement complété par le segment $A_1AA_2$ décrivant le déphasage qui s'effectue, pour l'essentiel, au voisinage de $X = 0$ ([[#^figure7|fig. 7]]). Dans un tel diagramme, la rotation de phase s'effectue sur deux décades autour de $X = 0$, avec une valeur de $-\frac{\pi}{4}$ rad/décade. L'écart maximal entre ce diagramme asymptotique et la réponse en phase est $|\Delta\varphi| < 6\degree$. Cette erreur est négligeable dans la pratique.

> [!note] Filtre intégrateur
> Nous cherchons un quadripôle qui réalise l'opération : $\displaystyle u_2(t) = u_2(0) + \frac{1}{\tau}\int_{0}^{\tau}u_1(\theta)d\theta$, ou, ce qui est équivalent : $u_1(t) = \tau\dfrac{du_2}{dt}$. En régime harmonique et en notation complexe : $\underline{u}_{1m} = j\omega\tau\underline{u}_{2m}$ soit : $\underline{H}(j\omega) = \frac{1}{j\omega\tau}$. Un intégrateur est donc un filtre du premier ordre.
> Diagramme de Bode : Nous définissons la pulsation réduite $x$ par : $x = \tau\omega$.
> - Courbe de réponse en gain : Le gain a pour expression : $G_{dB} = -20\log(x)$. La courbe de réponse en gain est donc une droite passant par l'origine et de pente égale à -20 dB/décade ([[#^figure9|fig. 9]]).
> - Courbe de réponse en phase : Le déphasage $\varphi$ de la tension de sortie par rapport à la tension d'entrée est : $\varphi = -\frac{\pi}{2}$.

> [!note] Réalisation d'un intégrateur
> Étudions le montage théorique de la [[#^figure10|figure 10a]].
> La loi des nœuds au niveau de l'entrée inverseuse de l'amplificateur opérationnel s'écrit : $\frac{v_e - v_-}{R} + C\dfrac{d(v_s - v_-)}{dt} = 0$. En régime linéaire, $v-$ est nulle, soit $\dfrac{dv_s}{dt} = -\frac{v_e}{RC}$. Le montage réalise bien une intégration quel que soit le signal d'entrée.
> - Réalisation du montage théorique : Réalisons le montage de la [[#^figure10|figure 10b]].
> L'interrupteur a été placé de façon à pouvoir décharger le condensateur. Prenons $v_e$ nul (entrée court-circuitée) et ouvrons l'interrupteur à l'instant $t = 0$. Nous observons soit une croissance linéaire de $v_s$ avec le temps jusqu'à la tension de saturation de l'A.O. $v_s = V_{sat}$, soit une décroissante linéaire jusqu'à $-V_{sat}$ .
> Cette dérive de la tension de sortie du montage est due aux défauts de l'amplificateur opérationnel.
> Ce montage théorique n'est pas utilisable dans la pratique. Un amplificateur opérationnel réel présente de petits défauts par rapport au modèle théorique appelés dérives : en régime linéaire, la tension $\epsilon = u_+ - u_-$ et le courant d'entrée ne sont pas rigoureusement nuls. Ces défauts, pratiquement sans incidence dans les montages amplificateurs étudiés au chapitre précédent, perturbent totalement le montage intégrateur qui n'est donc pas utilisable sous cette forme dans la pratique.
> - Montage amélioré : Pour éliminer le phénomène de dérive, il faudrait décharger régulièrement le condensateur. Remplaçons l'interrupteur par une résistance $R'$ ([[#^figure11|fig. 11]]).
> La fonction de transfert de ce nouveau montage se détermine simplement en appliquant la loi des nœuds en termes de potentiels à l'entrée inverseuse de l'amplificateur : $\underline{u} = 0 = \frac{\underline{u}_e}{R} + \underline{u}_s\left(\frac{1}{R'} + jC\omega\right)$ d'où $\underline{H} = -\frac{R'/R}{1 + jR'C\omega}$.
> Nous distinguons deux domaines de fonctionnement :
> 	- $R'C\omega \gg 1$ : Dans ce domaine de fréquence, le filtre se comporte comme un intégrateur de constante de temps $\tau = RC$.
> 	- $R'C\omega \ll 1$ : Alors $\underline{H} \approx -\frac{R'}{R}$. Admettons que les dérives sont équivalentes à une tension continue $e_d$ de l'ordre du millivolt ajoutée à la tension d'entrée. En régime forcé, une tension continue correspond au cas limite de la fréquence nulle.
> 	Si $u_e = 0$, les dérives seules créent, en régime forcé, une tension de sortie $u_{2}^{'} = -\frac{R'}{R}e_d$.
> 	Si les dérives sont nulles, la tension d'entrée sinusoïdale $u_1(t)$ crée en régime forcé une tension de sortie $u_{2}^{''}(t)$ telle que $\underline{u}_{2}^{''} = \underline{H}(j\omega)\underline{u}_{1}$.
> 	D'après le théorème de superposition : $u_{2}(t) = u_{2}^{'} + u_{2}^{''}(t)$.
> 
> 	Nous voulons fabriquer un circuit qui élimine les effets des dérives tout en se comportant comme un intégrateur acceptable pour $u_1(t)$. L'étude précédente nous fixe donc deux conditions :
> 	- Si nous nous fixons arbitrairement une valeur maximale de 0,1 V pour l'influence de ces dérives en sortie, nous en déduisons : $R' < 100R$ (environ) ;
> 	- Si nous considérons (arbitrairement) que le filtre se comporte comme un intégrateur pour $R'C\omega > 100$, nous obtenons : $R' > \frac{100}{C\omega}$ ou $R > \frac{1}{C\omega}$.
> 
> Remarques : 
> Expérimentalement, pour savoir si un intégrateur est perturbé par les dérives, il suffit de faire $u_1 = 0$ (en mettant l'entrée à la masse) et d'observer la sortie.
> Pour tester un intégrateur, il est recommandé d'utiliser à l'entrée une fonction en créneaux : l'intégrale d'une telle fonction est une fonction triangle facilement identifiable.

> [!note] Filtre passe-bas du premier ordre
> Nous avons vu un exemple de filtre passe-bas d'ordre un avec le circuit (R, C). Plus généralement : Un filtre est passe-bas d'ordre un si sa fonction de transfert est de la forme : $\displaystyle\underline{H}(j\omega) = \frac{A_0}{1 + j\frac{\omega}{\omega_0}} = \frac{A_0}{1 + jx}$ avec $A_0$ réel, $\omega_0$ est la pulsation propre ou pulsation de coupure et $x$ est la pulsation réduite.
> Le montage « intégrateur amélioré » vu précédemment est un exemple de passe-bas d'ordre un avec $A_0 = -\frac{R'}{R}$ et $\omega_0 = \frac{1}{R'C}$.
> Le diagramme de Bode est identique à celui du circuit ( R, C ), à une translation près, due à la constante $A_0$ ([[#^figure12|fig. 12]]).
> Remarque : Si $A_0 < 0$, il faut ajouter $\pi$ à l'expression de la phase $\varphi(\omega)$, car $e^{j\pi} = -1$.
> - Caractère pseudo-intégrateur : Réalisons le montage ([[#^figure13|fig. 13]]), avec une constante de temps $RC = 10^{-4} s$. Observons les courbes obtenues en régime forcé pour un signal d'entrée de type créneau d'amplitude $v_0 = 1 V$ et de période $T$.
> Si la période du signal est grande devant $RC$ $(T = 0,1 s)$, le signal de sortie est un créneau de même amplitude 1 V ([[#^figure14|fig. 14]]).
> Si la période du signal est petite devant $RC$ $(T = 10^{-5} s)$, le signal de sortie est un signal triangulaire d'amplitude 25 mV ([[#^figure18|fig. 18]]).
> Pour des valeurs intermédiaires de la période, le signal de sortie évolue d'une forme proche d'un créneau à une forme proche d'un triangle (fig. [[#^figure15|15]], [[#^figure16|16]] et [[#^figure17|17]]).
> Un signal créneau d'amplitude $v_0$ de période $T$ peut être décomposé en ses harmoniques, signaux sinusoïdaux de période $T$, $\frac{T}{3}$, $\frac{T}{5}$, $\frac{T}{7}$, $\ldots$, $\frac{T}{(2n + 1)}$ (le signal créneau ne contient que des harmoniques impairs) d'amplitudes : $a$, $\frac{a}{3}$, $\frac{a}{5}$, $\frac{a}{7}$, $\ldots$, $\frac{a}{(2n + 1)}$ avec $a = \frac{4v_0}{\pi}$ ([[#^figure19|fig. 19]]).
> Dans le cas où $T = 0,1 s$, les harmoniques d'amplitude importante vérifient $T \gg RC$ (ou $RC\omega \ll 1$). Le passe-bas (R, C) transmet sans déformation les harmoniques principaux : le signal de sortie est donc quasi identique au signal d'entrée. Dans le cas où $T = 10^{-5} s$ , tous les harmoniques vérifient $T \ll RC$ (ou $RC\omega \gg 1$). Le passe-bas atténue et intègre les harmoniques principaux : le signal de sortie est alors une primitive du signal d'entrée, donc un ensemble de segments de droite de pente $\pm\frac{v_0}{RC}$.
> En un quart de période, sa valeur passe de 0 à sa valeur extrémale : son amplitude est donc $\frac{v_0T}{4RC}$, soit 25 mV pour $\frac{T}{RC} = 10^{-1}$ et $v_0 = 1 V$.
> Dans les cas intermédiaires, seule une partie des harmoniques d'amplitude importante vérifie $T \gg RC$ ou $T \ll RC$. Nous ne pouvons rien déduire sur le signal de sortie.
> - Valeur moyenne d'une fonction périodique : Prenons l'exemple d'un signal : $u_1(t) = U_0 + U_1\cos(\omega t + \phi)$ envoyé à l'entrée d'un filtre passe-bas (R, C) tel que $\omega_0 = \frac{1}{RC} < \frac{\omega}{100}$ (soit $x = RC\omega > 100$).
> 	- Le filtre passe-bas laisse intégralement passer la fonction constante.
> 	- Le filtre passe-bas est utilisé dans sa zone asymptotique pour la partie variable. Son amplitude est divisée par 100 et elle est déphasée de $-\frac{\pi}{2}$.
> 	- En superposant les régimes forcés, nous obtenons : $u_2(t) = U_0 + \frac{U_1}{100}\sin(\omega t)$.
> 	Le signal de sortie est donc pratiquement égal à la valeur moyenne du signal d'entrée. Il ne subsiste qu'une faible ondulation, 100 fois plus faible que celle du signal d'entrée.
> 	Ce résultat est applicable à tout signal périodique de valeur moyenne non nulle.
> 
> ==**Un filtre passe-bas se comporte comme un opérateur « valeur moyenne » s'il est appliqué à un signal périodique de valeur moyenne non nulle et de fréquence $f \gg f_0$.**==

> [!note] Filtre dérivateur
> Nous cherchons un quadripôle qui réalise l'opération : $u_2(t) = \tau\dfrac{du_1}{dt}$. En régime harmonique et en notation complexe nous obtenons une fonction de transfert d'ordre un : $\underline{u}_{2m} = j\omega\tau\underline{u}_{1m}$ soit : $\underline{H}(j\omega) = j\omega\tau = jx$.
> La fonction de transfert est inverse de celle de l'intégrateur. Pour une même valeur de $x$, le gain en décibels et le déphasage sont donc opposés. Nous en déduisons le diagramme de Bode du dérivateur idéal ([[#^figure20|fig. 20]]).

> [!note] Réalisation d'un dérivateur
> Étudions le montage théorique de la [[#^figure21|figure 21]].
> Écrivons la loi des nœuds au niveau de l'entrée inverseuse de l'amplificateur opérationnel : $\frac{v_s - v_-}{R} + C\dfrac{d(v_e - v_-)}{dt} = 0$, soit en régime linéaire $(v_- = 0)$ : $v_s = -RC\dfrac{dv_e}{dt} = -\tau\dfrac{dv_e}{dt}$. Le montage réalise bien une dérivation quel que soit le signal d'entrée. Sa fonction de transfert est $\underline{H}(j\omega) = - jRC\omega$. Dans ce cas, nous avons $\varphi = -\frac{\pi}{2}$.
> - Réalisation à l'aide d'un amplificateur opérationnel réel :
> 	- Réalisation du montage théorique : Réalisons le montage théorique à l'aide d'un amplificateur opérationnel 741 avec $R = 10 kΩ$ et $C = 100 nF$ $(RC = 10^{-3} s)$. En choisissant comme signal d'entrée, un signal triangulaire d'amplitude 0,1 V, nous obtenons les résultats des figures [[#^figure22|22a]] et [[#^figure22|b]].
> 	Le montage présente un phénomène d'oscillations semblable à celui observé pour l'intensité dans un circuit (R, L, C). Il y a résonance.
> 	Le tracé du diagramme de Bode correspondant nous indique une résonance très aiguë pour une fréquence $f_c$ d'environ 13 kHz.
> 	Cette résonance est due à l'amplificateur opérationnel réel non idéal.
> 	Interprétons, à l'aide de la notion d'harmoniques, le fait que le montage ne soit pas dérivateur à basse fréquence.
> 	Sur la [[#^figure23|figure 23]] (signal d'entrée triangulaire de fréquence 100 Hz), nous remarquons que les harmoniques de rang 120 à 140 du signal de sortie ont une amplitude très grande. Leur fréquence est comprise entre 12 et 14 kHz , cela correspond au pic de résonance du montage. Cette amplification trop importante des harmoniques 120 à 140 explique les oscillations à une fréquence voisine de 13 kHz du signal de sortie. Le caractère dérivateur du montage est alors masqué par le phénomène de résonance.
> 	- Montage amélioré : L'idée est de diminuer l'acuité de la résonance du montage et donc de diminuer son facteur de qualité. Pour un circuit (R, L, C), il suffit d'augmenter $R$. Ici, nous ajouterons une résistance $R'$ en série avec le condensateur ([[#^figure24|fig. 24]]). La réponse est représentée sur les figures [[#^figure25a|25a]] et [[#^figure25b|b]].
>  - Étude expérimentale : Le montage expérimental est réalisé à l'aide d'une résistance $R'$ variable ([[#^figure26|fig. 26]]).
>  Nous choisissons un signal de sortie du générateur basse fréquence de type triangulaire de fréquence de l'ordre de 100 Hz et nous ajustons $R'$, de façon à obtenir en sortie de l'amplificateur opérationnel un signal aussi proche que possible du créneau (attention à la saturation en tension).
>  Réalisons l'expérience avec un générateur basse fréquence dont l'impédance de sortie est de 600 Ω. Nous trouvons une valeur optimale de $R'$ non nulle, de l'ordre de quelques centaines d'ohms.

> [!note] Filtre passe-haut d'ordre un
> Nous pouvons voir un exemple de filtre passe-haut d'ordre un avec le circuit (R, C), qui s'obtient en permutant dans le passe-bas (R, C) la position de $R$ et $C$. Nous obtenons le quadripôle représenté sur la [[#^figure27|figure 27]]. Sa fonction de transfert s'écrit : $\underline{H}(j\omega) = \frac{jx}{1 + jx}$. En déterminant les asymptotes de la courbe de réponse en gain ([[#^figure28|fig. 28]]), nous remarquons qu'aux très basses fréquences, la capacité $C$ se comporte comme un interrupteur ouvert. Alors qu'aux très hautes fréquences, la capacité $C$ se comporte comme un court-circuit. Nous observons que la courbe de réponse en phase d'un passe-haut d'ordre un, ainsi que son diagramme asymptotique ([[#^figure29|fig. 29]]) se déduisent de ceux d'un passe-bas du même ordre par une translation de $\frac{\pi}{2}$ le long de l'axe des déphasages. En fait la déphasage s'écrit : $\varphi(x) = \frac{\pi}{2} - \arctan(x)$, avec $0 < \varphi(x) < \frac{\pi}{2}$.
> Plus généralement : Un filtre est passe-haut d'ordre un si sa fonction de transfert est de la forme : $\displaystyle\underline{H}(j\omega) = \frac{jA_0\frac{\omega}{\omega_0}}{1 + j\frac{\omega}{\omega_0}} = A_0\frac{jx}{1 + jx} = A_0\frac{1}{1 - \frac{j}{x}}$ avec $A_0$ réel. Le diagramme de Bode est identique à celui du circuit (R, C) à une translation près, due à la constante $A_0$.
> 
> Caractère pseudo-dérivateur : Réalisons le montage de la [[#^figure30|figure 30]].
> Observons les courbes obtenues en régime forcé pour un signal d'entrée triangulaire d'amplitude $v_0 = 1 V$ réalisé avec une constante de temps $RC = 10_{-4} s$.
> Nous remarquons que si la période du signal est $T = 0,1 s$, donc grande devant $RC$, le signal de sortie est un signal créneau d'amplitude 4 mV ([[#^figure31|fig. 31]]).
> Si la période du signal est petite devant $RC(T = 10^{-5} s)$, le signal de sortie est un signal triangulaire d'amplitude 1 V ([[#^figure32|fig. 32]]).
> Pour des valeurs intermédiaires de la période, le signal de sortie évolue d'une forme proche d'un créneau à une forme proche d'un triangle.
> Nous dirons que ce montage est un pseudo-dérivateur, car le signal de sortie est la dérivée du signal d'entrée seulement quand ce dernier est périodique de période grande devant la constante de temps $RC$.
> La courbe de gain est alors confondue avec son asymptote basse fréquence de pente +20 dB/décade et sa réponse en phase a la valeur asymptotique $\frac{\pi}{2}$ ([[#^figure33|fig. 33]]).
> Nous pouvons généraliser ce résultat.
> 
> ==**Un filtre joue le rôle de dérivateur en basse fréquence si son diagramme de Bode présente une asymptote basse fréquence de pente +20 dB/décade et si le déphasage correspondant est de $\frac{\pi}{2}$ (ou $-\frac{\pi}{2}$ s'il y a inversion de signe).**==

> [!note] Produit de deux fonctions de transfert
> Étudions le circuit représenté sur la [[#^figure34|figure 34]].
> Nous reconnaissons deux filtres passe-bas séparés par un suiveur. Le suiveur permet d'assurer l'égalité $u_2 = u_3$ avec un courant $i_2$ nul.
> Comme le courant $i_2$ [[#^info2|est nul]] : $\underline{H}_1(j\omega) = \frac{\underline{u}_{2m}}{\underline{u}_{1m}} = \frac{1}{1 + j\frac{\omega}{\omega_1}}$ avec $\omega_1 = \frac{1}{R_1C_1}$.
> Comme la sortie est ouverte $(i_4 = 0)$ : $\underline{H}_2(j\omega) = \frac{\underline{u}_{4m}}{\underline{u}_{3m}} = \frac{1}{1 + j\frac{\omega}{\omega_2}}$ avec $\omega_2 = \frac{1}{R_2C_2}$.
> Nous en déduisons la fonction de transfert $\underline{H}(j\omega) = \frac{\underline{u}_{4m}}{\underline{u}_{1m}}$ du système complet : $\underline{H}(j\omega) = \underline{H}_1(j\omega)\underline{H}_2(j\omega) = \frac{1}{1 - \frac{\omega^{2}}{\omega_1\omega_2} + j\left(\frac{\omega}{\omega_1} + \frac{\omega}{\omega_2}\right)}$. Nous obtenons une fonction de transfert du second ordre.
> <mark style="color: red">Plus généralement : la fonction de transfert d'une association de deux filtres en cascade est égale au produit des fonctions de transfert.</mark>
> Construction du diagramme de Bode :
> - Diagramme de gain : La relation $\underline{H}(j\omega) = \underline{H}_1(j\omega)\underline{H}_2(j\omega)$ implique $20\log[H(\omega)] = 20\log[H_1(\omega)] + 20\log[H_2(\omega)]$ soit : $G_{dB} = G_{1\,dB} + G_{2\,dB}$.
> Il suffit donc d'additionner les deux courbes de gain. En particulier, nous déterminons très facilement les asymptotes ([[#^figure35|fig. 35]]).
> Le diagramme de gain nous indique que ce système est un filtre passe-bas d'ordre deux.
> - Diagramme de phase : La relation $\underline{H}(j\omega)$ implique également : $\arg[\underline{H}(j\omega)] = \arg[\underline{H}_1(j\omega)] + \arg[\underline{H}_2(j\omega)]$ soit : $\varphi = \varphi_1 +\varphi_2$. Il suffit donc d'additionner les deux courbes de phase, ce qui est particulièrement simple pour le diagramme asymptotique ([[#^figure35|fig. 35]]).

> [!note] Correspondance entre fonction de transfert et équation différentielle
> La fonction de transfert permet de déterminer $u_2(t)$ à partir de $u_1(t)$ en régime harmonique. Elle n'est en fait que la traduction pour le régime harmonique de l'équation différentielle qui relie les deux tensions.
> Inversement, nous pouvons en général retrouver cette équation différentielle à partir de la fonction de transfert en remplaçant $j\omega$ par une dérivation par rapport au temps.
> Pour un filtre du premier ordre : $\underline{H}(j\omega) = \frac{A + Bj\omega}{C + Dj\omega} \Rightarrow (C + Dj\omega)\underline{u}_{2} = (A + Bj\omega)\underline{u}_{1}$ d'où l'équation différentielle : $Cu_2 + D\dfrac{du_2}{dt} = Au_1 + B\dfrac{du_1}{dt}$.
> ==**Lorsqu'elles sont du même ordre, l'équation différentielle qui relie $u_2$ et $u_1$ et la fonction de transfert contiennent l'une et l'autre toutes les informations concernant le quadripôle. Les deux représentations sont équivalentes et on passe de l'une à l'autre par l'équivalence : $j\omega \rightarrow \dfrac{d}{dt}$.**==

> [!note] Stabilité d'un circuit
> Étudions la stabilité d'un filtre d'ordre un, de fonction de transfert : $\underline{H}(j\omega) = \frac{A + Bj\omega}{C + Dj\omega}$.
> - Condition concernant le régime libre : Le régime libre $u_{20}(t)$ est solution de l'équation homogène : $Cu_2 + D\frac{du_2}{dt} = 0$. Si $D = 0$ : $u_{20} = 0$. Si $C = 0$ : $\frac{du_{20}}{dt} = 0 \Rightarrow u_{20} = cte$. Si $C$ et $D$ non nuls : $u_{20} = U_0e^{-\frac{C}{D}t}$. Cette solution est bornée si $C$ et $D$ sont de même signe. La condition de stabilité qui résume ces trois cas est donc : $CD \geqslant 0$.
> Plutôt que d'appliquer mécaniquement un tel critère, il est préférable de retenir une formulation plus générale : <mark style="color: red">Le régime libre d'un système est stable si celui-ci converge vers 0.</mark>
> Le régime libre d'un système passif est généralement stable.
> Si le régime libre d'un système actif est instable, la sortie diverge et tend vers la saturation des amplificateurs. Cela se produit toujours, en raison des parasites aléatoires qui écartent le système de sa valeur d'équilibre.
> Remarque : L'étude du gain d'un filtre de fonction de transfert $\underline{H}(j\omega) = \frac{A_0}{1 - jx}$ devrait nous amener à la conclusion qu'il s'agit aussi d'un passe-bas d'ordre un. Mais son régime libre est instable (solution en $e^{+\omega_0 t}$) et il n'est pas utilisable en filtre ; il est donc inutile d'étudier le diagramme de Bode de cette fonction de transfert.
> - Condition concernant le régime forcé : Un système est instable en régime forcé s'il est possible de trouver une excitation $u_1(t)$ qui conduit à une réponse forcée $u_2(t)$ divergente.
> Pour les systèmes simples du premier ordre il est possible de raisonner directement en trouvant, lorsqu'elle existe, une excitation $u_1(t)$ qui conduit à une réponse $u_2(t)$ non bornée.
> En régime harmonique, la réponse est non bornée si le module $H(\omega)$ de la fonction de transfert est lui-même non borné. Nous admettrons la généralisation à tous les régimes forcés.
> ==**Un système est stable en régime forcé si le module $H(\omega)$ de la fonction de transfert est borné à toutes les fréquences (en particulier pour $\omega \rightarrow 0$ et pour $\omega \rightarrow \infty$).**==

> [!note] Composants à capacités commutées
> - Simulation d'une résistance par commutation d'une capacité : Considérons le circuit ([[#^figure36|fig. 36]]) où (K) est un commutateur dont le chronogramme des états est donné par la [[#^figure37|figure 37]]. Faisons d'abord l'hypothèse de tensions $U_1$ et $U_2$ continues avec $U_1 > U_2$. Lorsque le régime stationnaire est établi, les variations de $u(t)$ sont périodiques, de période $T_c$ entre les valeurs extrémales $U_{min}$ et $U_{max}$ ([[#^figure38|fig. 38]]). Prenons comme origine des temps, la date d'une commutation de $(K)$ de l'état ② à l'état ①. La capacité $C$ se charge alors sous $U_1$ à travers $R$ et nous pouvons écrire : $i_1 = \frac{U_1 - u(t)}{R} = C\dfrac{du(t)}{dt} \Rightarrow \dfrac{du(t)}{dt} +\frac{u(t)}{\tau} = \frac{U_1}{\tau}$. Par intégration, nous obtenons : $u(t) = (U_{min} - U_1)e^{-\frac{t}{\tau}} + U_1 \quad \left(0 \leqslant t < \frac{T_c}{2}\right)$.
> A la date $t = \frac{T_c}{2}$, la tension aux bornes de la capacité est : $u(\frac{T_c}{2}) = U_{max} = (U_{min} - U_1)e^{-\frac{T_c}{2\tau}} + U_1$ (équation 1).
> Par un raisonnement analogue à celui que nous venons de faire, nous établissons que : $u(t) = (U_{max} - U_2)e^{-\frac{t - \frac{T_c}{2}}{\tau}} + U_2 \quad \left(\frac{T_c}{2} \leqslant t < T_c\right)$.
> Donc, à la date $t = T_c$ la tension aux bornes du condensateur est : $u(T_c) = U_{min} = (U_{max} - U_2)e^{-\frac{T_c}{2\tau}} + U_2$ (équation 2).
> Les valeurs extrémales $U_{min}$ et $U_{max}$ sont les solutions du système formé par les équations 1 et 2 qu'il faut résoudre.
> Ainsi, pendant l'état ①, le condensateur reçoit la charge $q = C(U_{max} - U_{min})$ de la part de la source $U_1$ et restitue la même charge à la source $U_2$ pendant l'état ②.
> L'intensité moyenne du courant se dirigeant de $U_1$ vers $U_2$ est : $\langle i_1 \rangle = \langle i_2 \rangle = \frac{q}{T_c}$.
> La capacité commutée simule une résistance $R_{éq}$ de valeur : $R_{éq} = \frac{T_c}{C}\frac{\left(1 + e^{-\frac{T_c}{2\tau}}\right)}{\left(1 - e^{-\frac{T_c}{2\tau}}\right)}$ réglable par la fréquence de commutation $f_c = \frac{1}{T_c}$.
> Si la capacité est attaquée en tension ($R$ très faible), alors la constante de temps $\tau = RC$ est très faible devant la période de commutation $T_c$. L'expression de la résistance équivalente se simplifie en : $R_{éq} = \frac{T_c}{C} = \frac{1}{Cf_c}$.
> Les résultats précédents sont encore valables en régime variable si la période $T$ des signaux $u_1(t)$ et $u_2(t)$ est grande devant la période $T_c$ de commutation. Dans ces conditions, pendant la période $T_c$ de commutation les signaux $u_1(t)$ et $u_2(t)$ conservent quasiment les mêmes valeurs et les calculs précédents restent valables.
> 
> Par la suite, nous supposerons toujours satisfaire les inégalités $\tau \ll T_c \ll T$ de telle sorte que les capacités commutées soient utilisables en régime variable avec un comportement équivalent à celui d'une résistance $R_{éq} = \frac{1}{Cf_c}$. Dans ces hypothèses, les capacités commutées réalisent des résistances à valeurs contrôlées par une fréquence : nous leur attribuerons le symbole représenté dans la [[#^figure39|figure 39]].
> - Intégrateur inverseur à capacité commutée : Le principe utilisé pour réaliser un intégrateur inverseur à capacité commutée est donné sur la [[#^figure40|figure 40]]. La loi des nœuds écrite à l'entrée inverseuse donne : $i = \frac{u_1(t)}{R} = C\dfrac{du_2(t)}{dt} \Rightarrow \dfrac{du_2(t)}{dt} = -\frac{1}{RC}u_1(t) = -\frac{C_0}{C}f_cu_1(t)$.
> La constante de temps $\tau = \frac{C_0}{C}\frac{1}{f_c}$ de l'intégrateur peut être obtenue exactement, car, d'une part, la fréquence $f_c$ de commutation se contrôle facilement et, d'autre part, dans les circuits intégrés un rapport de deux capacités peut être réalisé avec précision.
> - Filtre universel d'ordre un à capacité commutée : La réalisation d'un tel filtre ([[#^figure41|fig. 41]]) nécessite un intégrateur inverseur et deux sommateurs. En régime harmonique, les signaux élaborés sont :
> 	- à la sortie du premier sommateur : $\underline{u}_{s\,1m} = \underline{u}_{em} + \underline{u}_{s\,2m}$ ;
> 	- à la sortie de l'intégrateur de constante de temps $\tau$ : $\underline{u}_{s\,2m} = -\frac{1}{j\omega\tau}\underline{u}_{s\,1m}$.
> 
> D'où, en éliminant $\underline{u}_{s\,2m}$, l'expression de la fonction de transfert d'un passe-haut d'ordre un entre l'entrée $E$ et la sortie $S_1$ : $\underline{H}_1 = \frac{\underline{u}_{s\,1m}}{\underline{u}_{em}}$.
> Entre l'entrée $E$ et la sortie $S_2$, la fonction de transfert réalisée est celle d'un passe-bas d'ordre un : $\underline{H}_2 = \frac{\underline{u}_{s\,2m}}{\underline{u}_{em}} = -\frac{1}{1 + j\omega\tau}$.
> À la sortie du second sommateur, nous trouvons le signal : $\underline{u}_{s\,3m} = \underline{u}_{s\,1m} + \underline{u}_{s\,2m}$ ce qui permet d'avoir, entre l'entrée $E$ et la sortie $S_3$, la fonction de transfert d'un déphaseur d'ordre un : $\underline{H}_3 = \frac{\underline{u}_{s\,3m}}{\underline{u}_{em}} = \frac{-1 + j\omega\tau}{1 + j\omega\tau}$ ;
> La pulsation de coupure $\omega_0 = \frac{1}{\tau}$ des filtres se règle au niveau de l'intégrateur par la fréquence de commutation $f_c$ de sa capacité commutée.
# Définitions
> [!note] Quadripôle
> Un quadripôle ([[#^figure2|fig. 2]]) est un ensemble qui présente deux bornes d'entrée et deux bornes de sortie.
> La fonction de transfert d'un quadripôle ne peut être définie que si le système est stable. A priori, tout quadripôle passif est stable (c'est-à-dire que les tensions ne divergent pas).
> Si nous étudions les tensions : $\underline{H}(j\omega) = \frac{\underline{u}_{2m}}{\underline{u}_{1m}}$.
> Un filtre est un quadripôle conçu pour transmettre sélectivement les diverses fréquences de la grandeur harmonique.
> Si le quadripôle est linéaire, $\underline{H}(j\omega)$ peut toujours s'écrire sous la forme : $\underline{H}(j\omega) = \frac{N(j\omega)}{D(j\omega)}$, $N$ et $D$ étant des polynômes à coefficients réels. L'ordre du filtre est égal au degré le plus élevé de ces deux polynômes.

==**Filtre passif et filtre actif**==
Un filtre est passif s'il n'est constitué que de dipôles passifs (résistances, bobines et condensateurs). Il est actif s'il contient un amplificateur alimenté par une source extérieure au circuit.

==**Réponse temporelle et réponse fréquentielle**== :
L'analyse temporelle d'un circuit est l'étude de sa réponse effectuée à partir de son équation différentielle et des conditions initiales. L'analyse fréquentielle en est l'étude effectuée à partir de sa fonction de transfert $\underline{H}(j\omega)$.
Les caractères instantanés de la réponse sont dégagés lors de l'analyse temporelle, tandis que les caractères permanents le sont lors de l'analyse fréquentielle.
Ces deux analyses d'un même phénomène physique (la réponse du circuit) sont intimement liées.

==**Définition de la stabilité**== :
Dans la théorie des circuits, le concept de stabilité est aussi fondamental que celui de linéarité. Nous conviendrons qu'un système est stable si sa réponse à toute excitation bornée, et quelles que soient les conditions initiales, reste bornée à tout instant.
# Diagrammes
Filtre (R, C)
![[electronique1/attachments-electronique1/figure172.png]]^figure1

Quadripôle : $u_1$ est la tension d'entrée ; $u_2$ est la tension de sortie ; $i_1$ est le courant d'entrée ; $i_2$ est le courant de sortie
![[electronique1/attachments-electronique1/figure173.png]]^figure2

Le courant $i_+$ étant nul la fonction de transfert du filtre est égale à $\frac{1}{1 + jRC\omega}$ quelque soit la valeur de $R_0$
![[electronique1/attachments-electronique1/figure179.png]]^figure8

 Intégrateurs à A.O. : montages théoriques
 ![[electronique1/attachments-electronique1/figure181.png]]^figure10

Intégrateur à A.O. : montage amélioré
![[electronique1/attachments-electronique1/figure182.png]]^figure11

Le suiveur impose au filtre (R, C) une impédance de charge infinie quelle que soit $R_u$
![[electronique1/attachments-electronique1/figure184.png]]^figure13

Dérivateur à A.O. : montage théorique
![[electronique1/attachments-electronique1/figure192.png]]^figure21

Dérivateur à A.O. : montage amélioré
![[electronique1/attachments-electronique1/figure195.png]]^figure24

Montage expérimental d'étude du dérivateur à A.O
![[electronique1/attachments-electronique1/figure198.png]]^figure26

Passe-haut (R, C) d'ordre un
![[electronique1/attachments-electronique1/figure199.png]]^figure27

Le suiveur impose au filtre passe-haut (R, C) une impédance de charge infinie quelle que soit $R_u$
![[electronique1/attachments-electronique1/figure202.png]]^figure30

Deux filtres d'ordre un en cascade
![[electronique1/attachments-electronique1/figure206.png]]^figure34

Principe de la simulation d'une résistance par commutation d'une capacité
![[electronique1/attachments-electronique1/figure208.png]]^figure36

Représentation d'une résistance à capacité commutée : $u(t) = Ri(t)$
![[electronique1/attachments-electronique1/figure211.png]]^figure39

Intégrateur inverseur à capacité commutée
![[electronique1/attachments-electronique1/figure212.png]]^figure40

Filtre universel d'ordre un
![[electronique1/attachments-electronique1/figure213.png]]^figure41
# Graphiques
Diagramme de Bode : a. courbe de réponse en gain ; b. courbe de réponse en phase
![[electronique1/attachments-electronique1/figure174.png]]^figure3

Principe d'une échelle logarithmique
![[electronique1/attachments-electronique1/figure175.png]]^figure4

Courbe de réponse en gain (en bleu) et diagramme asymptotique (en noir) d'un passe-bas d'ordre un
![[electronique1/attachments-electronique1/figure176.png]]^figure5

Le diagramme asymptotique formé des deux asymptotes $\varphi = 0$ et $\varphi = -\frac{\pi}{2}$ est insuffisant pour décrire la rotation de phase
![[electronique1/attachments-electronique1/figure177.png]]^figure6

Diagramme asymptotique de la courbe de réponse en phase d'un passe-bas d'ordre un
![[electronique1/attachments-electronique1/figure178.png]]^figure7

Diagramme de Bode d'un intégrateur théorique
![[electronique1/attachments-electronique1/figure180.png]]^figure9

Diagramme de Bode d'un filtre passe-bas d'ordre 1
![[electronique1/attachments-electronique1/figure183.png]]^figure12

Réponse du passe-bas de $RC = 10^{-4} s$ à une excitation en créneau de période $T = 10^{-1} s$
![[electronique1/attachments-electronique1/figure185.png]]^figure14

Réponse du passe-bas de $RC = 10^{-4} s$ à une excitation en créneau de période $T = 10^{-2} s$
![[electronique1/attachments-electronique1/figure186.png]]^figure15

Réponse du passe-bas de $RC = 10^{-4} s$ à une excitation en créneau de période $T = 10^{-3} s$
![[electronique1/attachments-electronique1/figure187.png]]^figure16

Réponse du passe-bas de $RC = 10^{-4} s$ à une excitation en créneau de période $T = 10^{-4} s$
![[electronique1/attachments-electronique1/figure188.png]]^figure17

Réponse du passe-bas de $RC = 10^{-4} s$ à une excitation en créneau de période $T = 10^{-5} s$
![[electronique1/attachments-electronique1/figure189.png]]^figure18

Harmoniques d'un signal créneau d'amplitude unité
![[electronique1/attachments-electronique1/figure190.png]]^figure19

Diagramme de Bode d'un dérivateur théorique
![[electronique1/attachments-electronique1/figure191.png]]^figure20

En basse fréquence, le montage n'a pas le caractère dérivateur attendu
![[electronique1/attachments-electronique1/figure193.png]]^figure22

Mise en évidence, dans le spectre de fréquence, d'une résonance de $v_s(t)$ au voisinage de 13 kHz
![[electronique1/attachments-electronique1/figure194.png]]^figure23

Réponse du dérivateur amélioré à un signal triangulaire
![[electronique1/attachments-electronique1/figure196.png]]^figure25a

Détail de la réponse précédente
![[electronique1/attachments-electronique1/figure197.png]]^figure25b

Courbe de réponse en gain et diagramme asymptotique d'un passe-haut d'ordre un
![[electronique1/attachments-electronique1/figure200.png]]^figure28

Courbe de réponse en phase et diagramme asymptotique d'un passe-haut d'ordre un
![[electronique1/attachments-electronique1/figure201.png]]^figure29

Réponse du passe-haut de $RC = 10^{-4} s$ à une excitation triangulaire de période $T = 10^{-1} s$
![[electronique1/attachments-electronique1/figure203.png]]^figure31

Réponse du passe-haut de $RC = 10^{-4} s$ à une excitation triangulaire de période $T = 10^{-5} s$
![[electronique1/attachments-electronique1/figure204.png]]^figure32

Diagramme de Bode du passe-haut (R, C) d'ordre un
![[electronique1/attachments-electronique1/figure205.png]]^figure33

Diagrammes asymptotiques pour le gain et pour la phase
![[electronique1/attachments-electronique1/figure207.png]]^figure35

Chronogramme des états du commutateur (K)
![[electronique1/attachments-electronique1/figure209.png]]^figure37

Variation de $u(t)$ en régime stationnaire établi
![[electronique1/attachments-electronique1/figure210.png]]^figure38
# Expériences
> [!warning]
> Voici des exemples de travaux pratiques qui abordent le sujet de ce chapitre : le [lien 1](https://telum.umc.edu.dz/pluginfile.php/235216/mod_resource/content/3/TP_01_papier.pdf), le [lien 2](https://ressources.unisciel.fr/sillages/physique/tp_electrocinetique_1a_pcsi/res/TP9.PDF), le [lien 3](https://www.studocu.com/row/document/universite-de-ain-temouchent-belhadj-bouchaib/comprehension-et-production-orale/tp-n-05-filtres-passifs-it-very-nice/93811369), le [lien 4](http://psi2.nantes.free.fr/TP/ENONCES-ET-CORRIGES-TP/TP-ELECTRONIQUE/ENONCE-TP-ELECTRONIQUE/TP-3-ENONCE.pdf), le [lien 5](https://www.lycee-champollion.fr/IMG/pdf/tp_phys_3_filtres_premier_ordre.pdf), le [lien 6](http://mpstar.lamartin.free.fr/fichiers/matieres-1128-1447320208.pdf), le [lien 7](https://www.f-legrand.fr/scidoc/srcdoc/sciphys/tpelectro/filtreactif/filtreactif-pdf.pdf), le [lien 8](https://ft.univ-tlemcen.dz/assets/uploads/pdf/departement/gee/Manuel-TP-ELN-L2-ST-S4-Electricite.pdf), le [lien 9](https://www.yumpu.com/fr/document/read/6395365/tp-electronique), le [lien 10](https://users.polytech.unice.fr/~pmasson/Enseignement/TP%20Elec%20analogique%20CIP1%202012-2013.pdf).
# Autres notes
> [!warning]
> L'usage le plus répandu consiste à noter la fonction de transfert comme une fonction complexe de la variable complexe $j\omega$ et non comme une fonction complexe de la variable réelle $\omega$.
^info1

> [!warning] A retenir
> - $\log 2 = 0,3$
> - $\log 3 = 0,48 \approx 0,5$ (à rapprocher de $3^{2} \approx 10$)
> - Diviser $H$ par $\sqrt{2}$ revient à retrancher 3 dB au gain : $20\log\frac{H}{\sqrt{2}} = 20\log(H) - 10\log2$
> - Diviser $H$ par 10 revient à retrancher 20 dB au gain : $20\log\frac{H}{10} = 20\log(H) - 20\log10$.

> [!warning]
> Nous n'avons pu écrire $\underline{H}_1(j\omega) = \frac{\underline{u}_{2m}}{\underline{u}_{1m}} = \frac{1}{1 + j\frac{\omega}{\omega_1}}$ que parce que $i_2$ est nul. Si nous n'avions pas intercalé de suiveur, le second filtre aurait « chargé » le premier et sa fonction de transfert en aurait été modifiée.
^info2