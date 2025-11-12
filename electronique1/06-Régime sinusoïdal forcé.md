---
titre: "[[06-Régime sinusoïdal forcé]]"
tags:
  - circuit-R-L-C
  - régime-sinusoïdal-permanent
  - impédance-complexe
  - puissance
aliases:
  - régime sinusoïdal permanent
  - régime sinusoïdal établi
  - régime harmonique
crée: 11-11-2025, 09:50
---
# Formules
> [!note] Représentation complexe du signal
> - Représentation complexe : À un signal sinusoïdal : $s(t) = s_m\cos(\omega t + \phi)$ d'amplitude réelle $s_m$ (positive) et de phase $\phi$ est associée la représentation complexe : $\underline{s}(t) = \underline{s}_m e^{j\omega t}$ d'amplitude complexe : $\underline{s}_m = s_me^{j\phi}$.
> - Représentation de Fresnel : La représentation de Fresnel de $s(t) = s_m\cos(\omega t + \phi)$ est la représentation géométrique de son amplitude complexe $\underline{s}_m$ dans le plan complexe ([[#^figure1|fig. 1]]).

> [!note]
> La notation complexe d'un signal peut être utilisée lorsqu'on effectue des OPÉRATIONS LINÉAIRES sur celui-ci : addition, soustraction, multiplication par un réel, dérivation, intégration (avec une constante nulle). Les opérations de dérivation et intégration de la représentation complexe d'un signal sont très simples puisqu'il suffit de multiplier ou diviser, respectivement, le signal complexe par le facteur $j\omega$.

> [!note] Circuit (R, L, C) série en régime sinusoïdal
> Considérons un circuit (R, L, C ) série soumis à l'excitation sinusoïdale $e(t)$ délivrée par un générateur basse fréquence. Nous supposerons, par exemple, que le générateur délivre, à partir de l'instant $t = 0$, la tension $e(t) = e_m\cos\omega t$ ([[#^figure2|fig. 2]]).
> L'équation d'évolution du courant dans le circuit : $\dfrac{d^{2}i(t)}{dt^{2}} + \frac{\omega_0}{Q}\dfrac{di(t)}{dt} + \omega_{0}^{2}i(t) = \frac{-\omega e_m}{L}\sin(\omega t)$ avec $\omega_0 = \frac{1}{\sqrt{LC}}$ et $Q = \frac{L\omega_0}{R}$.
> Ainsi, la solution cherchée $i(t)$ doit pouvoir s'écrire $i(t) = i_0(t) + i_1(t)$ où :
> - $i_1(t)$ est une solution particulière de l'équation d'évolution ;
> - $i_0(t)$ solution de l'équation sans second membre.
> 
> Dans le cas du circuit (R, L, C ) nous savons que la résistance entraîne un amortissement des solutions du type $i_0(t)$ : lorsque le second membre de l'équation d'évolution est nul, le signal tend vers zéro, et la fonction $i_0(t)$ est pratiquement nulle au-delà de $t = \tau$ , temps de relaxation du circuit.
> Dans ces conditions, nous pouvons dire que le signal $i(t)$ tend vers la solution particulière $i_1(t)$ : après un <mark style="color: red">régime transitoire</mark> dont la durée est indiquée par le temps de relaxation $\tau$ du circuit (R, L, C ) série, seule la solution particulière subsiste.
> Lorsqu'un circuit (R, L, C) est soumis à une excitation sinusoïdale de pulsation $\omega$, un <mark style="color: red">régime permanent sinusoïdal</mark>, de même pulsation que l'excitation imposée, s'établit après un régime transitoire qui dépend du facteur de qualité du circuit. Ne dépendant que de l'excitation imposée, ce régime permanent (limite) est de plus indépendant des conditions initiales.

> [!note] Détermination du régime permanent sinusoïdal
> Lorsque nous observons les signaux électriques d'un circuit (R, L, C ) alimenté par une tension excitatrice sinusoïdale $e(t) = e_m\cos(\omega t)$, nous ne voyons pas apparaître le régime transitoire, qui a disparu depuis longtemps ; nous ne nous intéresserons donc ici qu'au signal $i_1(t)$ qui seul subsiste : il est sinusoïdal, de même pulsation que l'excitation : $i_1(t) = i_{1m}\cos(\omega t + \phi)$. Cherchons à déterminer les paramètres de ce signal.
> - Une méthode fastidieuse (à proscrire) : Reportons l'expression de $i_1(t)$ dans l'équation d'évolution du courant, ce qui donne : $(-\omega^{2} + \omega_{0}^{2})i_{1m}\cos(\omega t +\phi) - \frac{\omega\omega_0}{Q}i_{1m}\sin(\omega t +\phi) = \frac{-\omega e_m}{L}\sin(\omega t)$. Développons cette expression de façon à ne garder que des termes en $\cos(\omega t)$ et $\sin (\omega t)$ : $\left[(-\omega^{2} + \omega_{0}^{2})\cos\phi - \frac{\omega\omega_0}{Q}\sin\phi\right]\cos(\omega t) + \left[(\omega^{2} - \omega_{0}^{2})\sin\phi - \frac{\omega\omega_0}{Q}\cos\phi\right]\sin(\omega t) = \frac{-\omega e_m}{Li_{1m}}\sin(\omega t)$. En identifiant les termes en $\cos(\omega t)$ et en $\sin(\omega t)$, on obtient un système d'équation en $\cos\phi$ et $\sin\phi$. En résolvant ce système, on trouve les expressions de $\cos\phi$ et $\sin\phi$ en fonction de $i_{1m}$. Donc, pour éliminer $\phi$ et trouver l'expression de l'amplitude $i_{1m}$, écrivons que $\cos^{2}\phi + \sin^{2}\phi = 1$. Enfin la réponse $i_1(t)$ est déterminée après avoir trouver l'expression de l'amplitude et la phase.
> - Obtention de la solution particulière avec la notation complexe : La tension excitatrice et la solution sinusoïdale recherchée s'écrivent en notation complexe : $\underline{e}(t) = e_me^{j\omega t}$ et $\underline{i}_1(t) = \underline{i}_{1m}e^{j\omega t}$ avec $\underline{i}_{1m} = {i}_{1m}e^{j\phi}$. Les fonctions $\underline{e}(t)$ et $\underline{i}_1(t)$ sont liées par l'équation différentielle : $L\dfrac{d^{2}\underline{i}_1(t)}{dt^{2}} + R\dfrac{d\underline{i}_1(t)}{dt} + \frac{\underline{i}_1(t)}{C} = \dfrac{d\underline{e}(t)}{dt}$. La dérivation temporelle se résume ici à la multiplication par $j\omega$, donc : $\left(-L\omega^{2} + j\omega R + \frac{1}{C}\right)\underline{i}_{1m}e^{j\omega t} = j\omega \underline{e}_{m}e^{j\omega t}$. À partir de cette expression (en introduisant $\omega_0$ et $Q$), nous retrouvons les valeurs $i_{1m}$ et $\phi$ précédentes : la solution particulière $i_1(t)$ est identifiée.

> [!note] Réponses en courant et charge du circuit (R, L, C )
> - la réponse en charge, indiquée par la tension $u_C(t) = \frac{q(t)}{C}$ aux bornes du condensateur ([[#^figure3a|fig. 3a]]) ;
> - la réponse en courant, indiquée par la tension $u_R(t) = Ri(t)$ aux bornes de la résistance ([[#^figure3b|fig. 3b]]).
> 
> Reportons l'expression de $\underline{q}(t)$ dans l'équation d'évolution de la charge, nous identifions les paramètres de signal de $\underline{q}(t)$. Dans la mesure où $\underline{i}(t) = j\omega\underline{q}(t)$, nous retrouvons tout aussi rapidement les paramètres de signal de $\underline{i}(t)$.
> - Étude de la réponse en courant : Notons $x = \frac{\omega}{\omega_0}$ la pulsation réduite, l'amplitude du courant peut s'écrire : $\displaystyle i_m = \frac{QC\omega_0e_m}{\sqrt{1 + Q^{2}\left(x - \frac{1}{x}\right)^{2}}}$.
> 	- Elle est nulle en $x = 0$ (limite basse fréquence) : le condensateur bloque le courant en régime continu. À fréquence nulle, il se comporte comme un interrupteur ouvert ([[#^figure4a|fig. 4a]]).
> 	- Elle est nulle pour $x \rightarrow \infty$ (limite haute fréquence) : l'inductance s'oppose aux variations très rapides du courant, elle se comporte à son tour comme un interrupteur ouvert ([[#^figure4b|fig. 4b]]).
> 	Elle passe par un maximum pour $x = 1$ : le circuit (R, L, C) série présente une résonance en courant lorsque la pulsation coïncide avec sa pulsation propre $\omega_0$ ([[#^figure5|fig. 5]]).
> À la résonance, l'amplitude maximale est : $i_{m,\,max} = i_m(\omega_0) = \frac{e_m}{R}$. Nous définirons la bande passante de la réponse par la plage de pulsations $[\omega_1, \omega_2]$ dans laquelle l'amplitude vérifie : $i_m \geqslant \frac{i_{m,\,max}}{\sqrt{2}}$. En résolvant cette inégalité, nous obtenons les valeurs de $\omega_1$ et $\omega_2$. Donc la bande passante en courant a une largeur $\Delta\omega = \frac{\omega_0}{Q}$. Elle est d'autant plus étroite que le facteur de qualité $Q$ du circuit est grand.
> La phase $\phi$ du courant est définie par : $\phi = -\arctan[Q(x - \frac{1}{x})]$. La rotation de phase au voisinage de $x = 1$ est d'autant plus rapide que le facteur de qualité $Q$ est élevé ([[#^figure6|fig. 6]]).
> Dans le circuit (R, L , C ) série (pulsation propre $\omega_0$, facteur de qualité $Q$), le courant est nul à très haute $(\omega \gg \omega_0)$ et très basse $(\omega \ll \omega_0)$ fréquence. Une résonance en courant est observée lorsque le circuit est excité exactement à sa pulsation propre $\omega_0$. Le courant est alors en phase avec la tension excitatrice. L'acuité de la résonance augmente avec le facteur de qualité du circuit.
> - Étude de la réponse en charge : L'amplitude de la charge peut s'écrire : $\displaystyle q_m = \frac{Ce_m}{\sqrt{\frac{x^{2}}{Q^{2}} + (1 - x^{2})^{2}}}$. Elle est non nulle en $x = 0$ : le condensateur est chargé en régime continu avec $q_m(0) = Ce_m$. Elle est nulle pour $x \rightarrow \infty$. Pour $x = 1$, nous obtenons $u_C = Qe_m$ : si $Q$ est supérieur à l'unité il y a une surtension aux bornes de la capacité ([[#^figure7|fig. 7]]). Un éventuel maximum de $q_m$ correspond au minimum de : $f(x) = x^{2} + Q^{2}(1 - x^{2})^{2} = g(X)$, où $X = x^{2}$. La dérivée $\dfrac{dg(X)}{dX} = 1 - 2Q^{2}(1 - X)$ s'annule en $X = 1 - \frac{1}{2Q^{2}}$. Cette solution est positive si $Q > \frac{1}{\sqrt{2}}$. Une résonance en tension est donc observable si cette condition est vérifiée. La pulsation de résonance, lorsqu'elle existe correspond à : $\omega_r = \omega_0\sqrt{1 - \frac{1}{2Q^{2}}}$.
> Dans un circuit (R, L, C) série (pulsation propre $\omega_0$, facteur de qualité $Q$) excité par un générateur sinusoïdal de tension, l'amplitude de la tension aux bornes de la capacité passe par un maximum si $Q > \frac{1}{\sqrt{2}}$. Dans ce cas, la résonance est obtenue pour une pulsation $\omega_r$ inférieure à $\omega_0$. Si $Q \gg 1$, $\omega_r$ est voisin de $\omega_0$.
> Sachant que $\underline{q}_m = \frac{\underline{i}_m}{j\omega}$, nous en déduisons que la phase de la charge du condensateur vaut : $\varphi = -\frac{\pi}{2} - \arctan[Q(x - \frac{1}{x})]$. Lorsque le circuit est excité à sa pulsation propre, la charge du condensateur est en phase avec la tension excitatrice. La rotation de phase au voisinage de $x = 1$ est ici encore accélérée pour les valeurs plus élevées de $Q$ ([[#^figure8|fig. 8]]).

> [!note] Étude du régime sinusoïdal forcé
> Chaque branche du circuit est régie par une équation d'évolution qui est une équation différentielle linéaire à coefficients constants. Pour étudier le régime sinusoïdal permanent établi, nous savons qu'il est très commode d'utiliser la notation complexe. L'équation différentielle se ramène alors à une relation entre amplitudes complexes où interviennent des polynômes de la variable $(j\omega)$. Par exemple, pour un circuit dont l'évolution est régie par l'équation ([[#^figure9|fig. 9]]) : $D_2\dfrac{d^{2}s(t)}{dt^{2}} + D_1\dfrac{ds(t)}{dt} + D_0s(t) = N_2\dfrac{d^{2}e(t)}{dt^{2}} + N_1\dfrac{de(t)}{dt} + N_0e(t)$ liant sa réponse $s(t)$ à l'excitation $e(t)$, nous obtenons immédiatement le rapport des amplitudes complexes de l'excitation et de la réponse sous la forme d'un rapport de deux polynômes de la variable $(j\omega)$. Nous trouvons ensuite l'amplitude et la phase de la réponse $s(t)$.
> Faire l'analyse harmonique du comportement du circuit, c'est étudier l'évolution de l'amplitude complexe (c'est-à-dire de l'amplitude et de la phase des oscillations sinusoïdales réelles) des grandeurs physiques (intensité, tension) dans le circuit en fonction de la pulsation de l'excitation.
> Comme pour le circuit (R, L, C) série, nous pourrons, par exemple, observer une (ou plusieurs) résonance(s) du circuit en faisant varier la fréquence d'utilisation.

> [!note] Lois de Kirchhoff en notation complexe
> - en un noeud du circuit : $\displaystyle \sum_{k}\epsilon_k\underline{i}_k = 0$ ;
> - sur une maille : $\displaystyle \sum_{k}\epsilon_k\underline{u}_k = 0$.

> [!note] Définition d'une impédance complexe
> L'impédance complexe du dipôle est la grandeur complexe : $\displaystyle\underline{Z}(j\omega) = \frac{\underline{u}_m}{\underline{i}_m}$.
> Le module de l'impédance complexe est l'impédance du dipôle. Les impédances se mesurent en ohm (symbole : Ω). Son argument $\varphi(\omega) = \phi_u - \phi_i$ est le déphasage de la tension par rapport au courant.
> La partie réelle de l'impédance complexe d'un dipôle est la résistance de ce dipôle et la partie imaginaire en est la réactance et les deux se mesurent en ohm.
> L'admittance complexe du dipôle est l'inverse de son impédance complexe. Le module de l'admittance complexe d'un dipôle est son admittance ; elle se mesure en siemens (symbole : S).
> La partie réelle de l'admittance complexe est la conductance du dipôle et la partie imaginaire en est la susceptance et les deux se mesurent en siemens.

> [!note] Exemples d'impédances
> - Conducteur ohmique : En régime harmonique l'impédance complexe du conducteur ohmique est : $\underline{Z} = R$. Pour un conducteur ohmique donné, son impédance est réelle et constante ([[#^figure10|fig. 10]]) : la tension et le courant sont en phase ([[#^figure11|fig. 11]]).
> - Inductance : L'impédance complexe $\underline{Z}(j\omega) = jL\omega$ d'une inductance est imaginaire pure ([[#^figure12|fig. 12]]). Le module $L\omega$ de cette impédance est d'autant plus élevé que la fréquence est élevée. Une inductance s'oppose aux variations de l'intensité. En haute fréquence, elle se comporte comme un interrupteur ouvert. En revanche, en très basse fréquence, elle se comporte comme un interrupteur fermé. La tension est en avance de $\frac{\pi}{2}$ sur le courant ([[#^figure13|fig. 13]]).
> - Capacité : L'[[#^info1|impédance complexe]] $\underline{Z}(j\omega) = \frac{1}{jC\omega}$ d'une capacité est imaginaire pure ([[#^figure14|fig. 14]]). Le module $\frac{1}{C\omega}$ de cette impédance est d'autant plus faible que la fréquence est élevée : la coupure du circuit par un condensateur est d'autant moins marquée que la fréquence est élevée. À haute fréquence, une capacité se comporte comme un interrupteur fermé. En revanche, à très basse fréquence elle se comporte comme un interrupteur ouvert. La tension est en retard de $\frac{\pi}{2}$ par rapport à l'intensité ([[#^figure15|fig. 15]]).

> [!note] Associations d'impédances en notation complexe
> - en série : $\displaystyle \underline{Z} = \sum_{k} \underline{Z}_k$ ;
> - en parallèle : $\displaystyle \underline{Y} = \sum_{k} \underline{Y}_k$.

> [!note] Diviseurs de tension et de courant
> - Pour le diviseur de tension : $\displaystyle \underline{u}_{2m} = \frac{\underline{Z}_2}{\underline{Z}_1 + \underline{Z}_2}\underline{u}_m$ ;
> - Pour le diviseur de courant : $\displaystyle \underline{i}_{2m} = \frac{\underline{Y}_2}{\underline{Y}_1 + \underline{Y}_2}\underline{i}_m = \frac{\underline{Z}_1}{\underline{Z}_1 + \underline{Z}_2}\underline{i}_m$.

> [!note] Représentation de Thévenin et Norton des électromoteurs
> En régime harmonique, un électromoteur (le plus souvent un générateur) peut se représenter par deux modèles dont les effets sont équivalents pour le circuit extérieur : modèle de Thévenin $(\underline{e}, \underline{Z}_i)$ ou modèle de Norton $(\underline{\eta}, \underline{Z}_i)$.
> L'impédance interne $\underline{Z}_i$ de l'électromoteur a la même valeur pour les deux modèles qui sont liés par : $\underline{e}_m = \underline{Z}_i\underline{\eta}$ ([[#^figure16|fig. 16]]).

> [!note] Loi des nœuds en termes de potentiels
> En régime sinusoïdal forcé, les branches qui aboutissent à un nœud $A$ peuvent être classées en deux catégories ([[#^figure17|fig. 17]]) :
> - celles qui contiennent des générateurs de courant imposant des courants de branche de valeur complexe $\underline{\eta}_j$ ;
> - celles d'admittance $\underline{Y}_k$, sans générateur de courant, dont le potentiel à leur extrémité $B_k$ a une valeur complexe $\underline{v}_k$.
> 
> La loi des nœuds, exprimée en termes de potentiel, appliquée en $A$ s'écrit : $\displaystyle \sum_{j}\epsilon_j\underline{\eta}_j + \sum_{k}\underline{Y}_k(\underline{v}_k - \underline{v}_A) = 0$. En l'absence de générateurs de courant, la loi des nœuds prend la forme simple mais usuelle (relation de Milleman) : $\underline{v}_A = \frac{\displaystyle\sum_{k}\underline{Y}_k\underline{v}_k}{\displaystyle\sum_{k}\underline{Y}_k}$.

> [!note] Théorème de superposition
> Dans un réseau linéaire contenant des sources sinusoïdales indépendantes, la valeur complexe $s(t)$ d'une grandeur quelconque (courant ou tension) est égale à la somme des valeurs complexes de cette même grandeur obtenues lorsque toutes les sources sont éteintes à l'exception d'une seule.

Puissance instantanée en régime sinusoïdal reçue par le dipôle (en convention récepteur) est la fonction réelle du temps : $p(t) = u(t)i(t)$.

En régime harmonique, la puissance moyenne est appelée puissance active : $\mathcal{P} = \frac{u_mi_m}{2}\cos\varphi$ avec $u_m$ et $i_m$ sont les amplitudes de la tension et de l'intensité et $\varphi$ est le déphasage de la tension par rapport au courant. Le produit $\mathscr{S} = \frac{u_mi_m}{2}$, appelé puissance apparente, s'exprime en volt-ampère $(V.A)$. Le facteur, sans dimension, $\cos\varphi$ est le facteur de puissance. 

Si $s(t)$ est une grandeur sinusoïdale d'amplitude $s_m$ alors sa valeur efficace est : $\displaystyle S_{eff} = \frac{s_m}{\sqrt{2}}$.
La puissance moyenne absorbée par un dipôle est ainsi : $\mathcal{P} = U_{eff}I_{eff}\cos\varphi$.

> [!warning] Puissance et notation complexe
> La puissance est le produit de la tension par le courant : ce n'est pas une grandeur linéaire.
> Il faut manipuler la notation complexe avec précaution : $p(t) = u(t)i(t)$ ne s'identifie pas à $\mathcal{R}e[\underline{u}(t)\underline{i}(t)]$ (cf. [[#^info2]]).
> La puissance moyenne absorbée par un dipôle en régime sinusoïdal est, en convention récepteur : $\mathcal{P} = \frac{1}{2}\mathcal{R}e[\underline{u}(t)\underline{i}^*(t)]$.

> [!note] Autres expressions de la puissance active
> Utilisons la définition de l'impédance d'un dipôle linéaire : $\underline{Z}(\omega) = R + jX$ avec $Z = \left| \underline{Z} \right|$ : $u_m = Z(\omega) i_m$ et l'expression de $\cos\varphi = \frac{R}{Z}$ pour établir une nouvelle expression de la puissance active. Il vient : $\mathcal{P} = \frac{Zi_{m}^{2}}{2}\frac{R}{Z} = RI_{eff}^{2}$.
> De façon analogue, la définition de l'admittance du dipôle : $\underline{Y}(\omega) = \frac{1}{\underline{Z}(\omega)} = G + jB$ nous donne : $\mathcal{P} = GU_{eff}^{2}$.
> Conséquences :
> - Si le dipôle est passif, il se comporte toujours en récepteur et sa puissance active est positive, $\mathcal{P} > 0$, ce qui implique $R(\omega) > 0$ et $G(\omega) > 0$. <mark style="color: red">Les parties réelles de l'impédance et de l'admittance complexes d'un dipôle linéaire passif sont toujours positives.</mark>
> - Pour une inductance pure $L$ ou une capacité $C$ idéale, la partie réelle de l'impédance est nulle. En conséquence, $\mathcal{P} = 0$. Une inductance pure et une capacité idéale ne consomment pas, en moyenne, d'énergie. Ces éléments échangent réversiblement de l'énergie avec le circuit. Ainsi, en régime harmonique, ils restituent, en moyenne, autant d'énergie qu'ils en reçoivent.
> - Une résistance absorbe de l'énergie et n'en restitue jamais. Elle transforme irréversiblement l'énergie qu'elle absorbe : c'est un élément dissipatif.

> [!note] Adaptation d'impédances
> Cherchons à quelles conditions un générateur sinusoïdal de f.e.m. $e(t) = e_m\cos(\omega t)$ et d'impédance interne $\underline{Z}_g = R_g + jX_g$ fournit le maximum de puissance à un réseau d'utilisation d'impédance $\underline{Z}_u = R_u + jX_u$ ([[#^figure18|fig. 18]]).
> Supposons que les caractéristiques du générateur soient fixées et que celles de l'utilisation soient à déterminer. Nous avons d'abord $\underline{i}_m = \frac{\underline{e}_m}{\underline{Z}_g + \underline{Z}_u}$, puis $i_m^{2} = \underline{i}_m\underline{i}_m^*$. Nous trouvons ainsi la puissance active fournie à l'utilisation : $\mathcal{P}_u = R_u\frac{i_m^{2}}{2} = \frac{R_u}{(R_g + R_u)^{2} + (X_g + X_u)^{2}}\frac{e_m^{2}}{2}$.
> Dans l'hypothèse d'une f.e.m. $\underline{e}_m$ fixée, nous augmentons la valeur de $\mathcal{P}_u$ en choisissant $\underline{Z}_u$ avec une réactance opposée à celle de $\underline{Z}_g$ : $X_g + X_u = 0$. Dans ces conditions, la puissance transmise à l'utilisation est : $\mathcal{P}_u = \frac{R_u}{(R_g + R_u)^{2}}\frac{e_m^{2}}{2}$. Cette puissance transmise peut encore être augmentée en déterminant la valeur de la résistance $R_u$ qui rend le facteur $y = \frac{R_u}{(R_g + R_u)^{2}}$ maximal c-à-d $\dfrac{dy}{dR_u} = 0$ d'où $R_u = R_g$.
> Les deux conditions à satisfaire sont $R_u = R_g$ et $X_u = -X_g$ : les deux impédances complexes $\underline{Z}_u$ et $\underline{Z}_g$ sont donc conjuguées.
> La puissance transmise par un générateur à une utilisation est maximale quand les impédances du générateur et de l'utilisation sont adaptées, c'est-à-dire conjuguées : $\underline{Z}_u = \underline{Z}_g^*$. Cette puissance maximale vaut : $\mathcal{P}_{u_{max}} = \frac{e_m^{2}}{8R_g}$.
> Remarque : Lorsque les caractéristiques $(e_m, \underline{Z}_g)$ du générateur sinusoïdal et celle $\underline{Z}_u$ de l'utilisation sont imposées, le problème de l'adaptation d'impédances ne peut être résolu qu'en intercalant un quadripôle entre le générateur et l'utilisation ([[#^figure19|fig. 19]]). Le quadripôle, fermé sur l'impédance d'utilisation, doit présenter en entrée une impédance conjuguée de celle du générateur. On réalise ainsi le transfert maximal de puissance entre le générateur et le quadripôle. Pour que cette puissance maximale se retrouve ensuite sur l'utilisation, il faut réaliser le quadripôle avec des éléments non dissipatifs (inductances et capacités). On peut aussi utiliser comme quadripôle un transformateur.
# Définitions
==**Régime transitoire et régime permanent sinusoïdal**== :
L'étude effectuée pour le circuit (R, L, C) série peut être généralisée aux réseaux linéaires, lorsqu'ils sont soumis à une excitation sinusoïdale : la réponse du circuit à une excitation sinusoïdale est la superposition de la réponse permanente sinusoïdale (qui ne dépend pas des conditions initiales) et d'un régime transitoire (déterminé par les conditions initiales).
Nous supposerons que le régime libre du circuit est caractérisé par un régime transitoire qui tend vers zéro au cours du temps : le circuit est supposé stable, suffisamment amorti.
==**Pour un réseau linéaire stable, soumis à une excitation sinusoïdale, un régime permanent sinusoïdal s'établit après un régime transitoire qui tend vers zéro. En régime sinusoïdal forcé, tous les courants et tensions du circuit de même pulsation, seront caractérisés par leurs amplitude et phase.**==

==**Représentations des éléments du circuit en régime permanent sinusoïdal**== :
Dans le cas d'un réseau linéaire en régime harmonique permanent (ou régime sinusoïdal forcé), nous pouvons transposer les lois et modèles développés en régime constant, et utiliser :
- les lois de Kirchhoff ;
	- la loi des nœuds pour les intensités complexes ;
	- la loi des mailles pour les tensions complexes ;
- la décomposition du réseau en dipôles élémentaires :
	- dipôles passifs caractérisés par leur impédance complexe ($\underline{u} = \underline{Z}\,\underline{i}$ en convention récepteur) ;
	- générateurs de tension sinusoïdale de f.e.m complexe $\underline{e} = \underline{e}_m . e^{j\omega t}$, de courant sinusoïdal de c.e.m. $\underline{\eta} = \underline{\eta}_m . e^{j\omega t}$ d'impédance interne $\underline{Z}_i$ s'ils ne sont pas idéaux.

==**Intérêt de l'analyse harmonique**== :
La place particulière accordée aux régimes harmoniques a plusieurs justifications :
- Si l'excitation est harmonique, la réponse forcée l'est également. Le régime harmonique forcé est aisément calculable, en utilisant la notation complexe.
- Les sources sont assez souvent sinusoïdales : tension du secteur, tension délivrée par un alternateur, tensions délivrées par les générateurs utilisés en TP.
- On peut montrer que tout signal physiquement réalisable peut se mettre sous la forme d'une somme infinie de signaux sinusoïdaux (décomposition de Fourier) : la réponse du circuit linéaire au signal complet est la superposition des réponses à chaque terme de la décomposition pris individuellement.
# Diagrammes
Étude d'un circuit (R, L, C) série
![[figure111.png]]^figure2

Réponse en charge
![[figure112.png]]^figure3a

Réponse en courant
![[figure113.png]]^figure3b

Équivalent basse fréquence
![[figure114.png]]^figure4a

Équivalent haute fréquence
![[figure115.png]]^figure4b

Soumis à l'excitation $e(t)$, le dipôle linéaire délivre la réponse $s(t)$
![[figure120.png]]^figure9

Représentations de Thévenin et de Norton d'un générateur sinusoïdal en notation complexe
![[figure127.png]]^figure16

Nœud $A$ avec les deux types de branches qui y aboutissent
![[figure128.png]]^figure17

La puissance transmise par le générateur à l'utilisation est maximale lorsque $\underline{Z}_u = \underline{Z}_g^*$
![[figure129.png]]^figure18

Le quadripôle $Q$ adapte les impédances du générateur et de la charge pour une transmission maximale de la puissance moyenne
![[figure130.png]]^figure19
# Graphiques
Représentation de Fresnel de la grandeur sinusoïdale $s(t) = s_m\cos(\omega t + \phi)$
![[figure110.png]]^figure1

Variations de $\frac{i_m(x)}{e_m/R}$ en fonction de $x$ pour $Q = \frac{1}{2}$, $Q = 1$ et $Q = 5$
![[figure116.png]]^figure5

Variations du déphasage $\phi(x)$ de la réponse $i(t)$ par rapport à l'excitation $e(t)$ en fonction de $x$ pour $Q = \frac{1}{2}$, $Q = 1$ et $Q = 5$
![[figure117.png]]^figure6

Variations de $\frac{u_{C_m}}{e_m}$ en fonction de $x$ pour $Q = \frac{1}{2}$, $1$ et $5$
![[figure118.png]]^figure7

Variations du déphasage $\varphi(x)$ et $u_c(t)$ par rapport à $e(t)$ en fonction de $Q = \frac{1}{2}$, $1$ et $5$
![[figure119.png]]^figure8

L'impédance complexe $Z = R$ d'un conducteur ohmique est réelle et constante
![[figure121.png]]^figure10

La tension $u(t)$ aux bornes d'un conducteur ohmique est en phase avec l'intensité $i(t)$ qui le traverse
![[figure122.png]]^figure11

L'impédance complexe $\underline{Z} = jL\omega$ d'une inductance est imaginaire pure
![[figure123.png]]^figure12

La tension $u(t)$ aux bornes d'une inductance est en avance de $\frac{\pi}{2}$ sur l'intensité $i(t)$ qui la traverse
![[figure124.png]]^figure13

L'impédance complexe $\underline{Z} = \frac{1}{jC\omega}$ d'une capacité est imaginaire pure
![[figure125.png]]^figure14

La tension $u(t)$ aux bornes d'une capacité est en retard de $\frac{\pi}{2}$ sur le courant $i(t)$ qui la traverse
![[figure126.png]]^figure15
# Expériences
> [!warning]
> Voici des exemples de travaux pratiques qui abordent le sujet de ce chapitre : le [lien 1](https://www.romainplanques.fr/TP/TP12_circuitRLC_force.pdf), le [lien 2](http://prepa.blois.free.fr/SITEMPSI/PhyMPSI/wa_files/EnonceTP15.pdf), le [lien 3](https://drive.google.com/file/d/1aAOOKnAfIe40M_2iZbtqpViXAy_iM8HV/view).
# Autres notes
> [!warning] Détermination de la phase
> De façon générale, la donnée de $\sin\phi$ ou $\cos\phi$ ou $\tan\phi$ ne suffit pas à déterminer $\phi$ entre $-\pi$ et $+\pi$.
> Il faut préciser le signe d'une seconde fonction trigonométrique de $\phi$ ou indiquer un domaine plus restreint.
> En particulier ici :
> - Si $\tan\phi = X$ et $\cos\phi > 0$, alors : $\phi = \arctan X$ ;
> - Si $\tan\phi = X$ et $\cos\phi < 0$, alors : $\phi = \arctan X \pm \pi$.

> [!warning] Impédance d'un condensateur
> Il faut se souvenir que $\underline{Z}$ N'EST PAS ÉGALE À $jC\omega$.
^info1

> [!warning] Point mathématique (Calcul de la puissance et la notation complexe)
> La représentation complexe ne permet pas de déterminer le produit de deux fonctions sinusoïdales.
> Considérons en effet deux signaux sinusoïdaux : $s_1(t) = s_{1m}\cos(\omega t + \phi_1)$ et $s_2(t) = s_{2m}\cos(\omega t + \phi_2)$.
> - $s_1(t)s_2(t) = \frac{1}{2}s_{1m}s_{2m}\cos(\phi_1 - \phi_2)\cos(2\omega t + \phi_1 + \phi_2)$.
> - $\underline{s}_1\underline{s}_2 = s_{1m}s_{2m}e^{j(2\omega t + \phi_1 + \phi_2)}$.
> 
> Il est clair que : $\mathcal{R}e(\underline{s}_1\underline{s}_2) \neq s_1(t)s_2(t)$.
^info2

> [!note] Calcul de la moyenne temporelle et de la valeur efficace
> Considérons une grandeur $s(t)$ fonction du temps et de nature physique quelconque. La valeur moyenne de $s(t)$ au cours du temps ou moyenne temporelle est la grandeur notée $\langle s(t) \rangle$ ou $S$, définie par : $\displaystyle\langle s(t) \rangle = S = \lim_{\tau \rightarrow +\infty} \frac{1}{\tau} \int_{0}^{\tau} s(t) dt$.
> Si $s(t)$ est périodique de période $T$, la moyenne peut se calculer sur une période : $\displaystyle\langle s(t) \rangle = S = \frac{1}{T}\int_{\tau}^{\tau + T} s(t) dt$.
> La valeur efficace d'une grandeur périodique $s(t)$ est : $S_{eff} = \sqrt{\langle s^{2}(t) \rangle}$.