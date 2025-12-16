---
titre: "[[10-Amplificateur opérationnel. Bande passante, stabilité des montages bouclés et comparateurs]]"
tags:
  - amplificateur-opérationnel
  - comparateur-à-hystérésis
  - multivibrateur-astable
  - générateurs-de-fonctions
crée: 17-11-2025, 20:23
---
# Formules
> [!note] Étude dynamique du montage amplificateur non inverseur : Étude expérimentale du signal de sortie en fonction de la fréquence
> Réalisons un montage amplificateur non inverseur d'amplification statique $H_0 = 11$ ([[#^figure1|fig. 1]]) en prenant $R_1 = 1 k\Omega$ et $R_2 = 10 k\Omega$.
> Nous l'alimentons avec un GBF qui délivre une tension sinusoïdale dont la valeur de crête est de l'ordre de 1 V, de façon à ne pas saturer l'amplificateur opérationnel.
> Pour tracer le diagramme de Bode (courbes de réponse en gain et en phase), le montage doit fonctionner en régime linéaire.
> À chaque mesure, nous devons vérifier qu'il n'y a ni saturation, ni triangularisation et modifier l'amplitude du signal d'entrée si nécessaire. Nous ne pouvons donc pas nous contenter de mesures au multimètre : l'oscilloscope est obligatoire.
> Les diagrammes de Bode obtenus pour les différentes valeurs du rapport $\frac{R_2}{R_1}$ correspondent à des filtres passe-bas d'ordre un ([[#^figure2|fig.2]] et [[#^figure3|3]]).
> En basse fréquence, le gain est proche du gain théorique : $G_{dB} = 20\log\left(1 + \frac{R_2}{R_1}\right)$.
> Les courbes de réponse en gain présentent toutes la même asymptote haute fréquence : $G_{dB} = -20\log\left(\frac{f}{f_0}\right)$, de pente -20 dB/décade, avec $f_0 \approx 1 MHz$, fréquence de gain nul.
> Le déphasage en basse fréquence est nul, en haute fréquence il est voisin de $-\frac{\pi}{2}$. Le montage non inverseur peut donc être modélisé par un filtre passe-bas du premier ordre.
> La fréquence de coupure $f_c$ à -3 dB de ces montages est celle du point d'intersection des asymptotes basse fréquence et haute fréquence (filtres du premier ordre). Comme ils possèdent tous la même asymptote haute fréquence, le gain à basse fréquence vérifie $G_0 = -20\log\left(\frac{f}{f_0}\right)$, soit $H_0f_c = f_0$.
> Le produit « gain » × « bande passante à –3 dB » du montage est une constante caractéristique de l'amplificateur opérationnel. Le terme « gain » est un abus de langage, le terme correct est amplification.
^par1

> [!note] Étude dynamique du montage amplificateur non inverseur : Modélisation de l'amplificateur opérationnel réel
> Les caractéristiques passe-bas de l'amplificateur non inverseur étudié sont dues à l'A.O. La relation entre $v_s$ et $\epsilon$ est analogue à celle qui relie la tension $v_C$ aux bornes de la capacité à la tension totale $v$ dans un circuit (R, C) (filtre passe-bas élémentaire).
> 
> Considérons le modèle de l'amplificateur opérationnel réel dit « à bande passante limitée ». Nous pouvons donner deux représentations de la relation entre $v_s$ et $v_e$ :
> - une équation différentielle : $\tau\dfrac{dv_s}{dt}+ v_s = \mu_0\epsilon$, $\tau$ étant une constante homogène à un temps et $\mu_0$ une constante sans dimension ;
> - une relation entre grandeurs complexes en régime sinusoïdal : $\underline{v}_s = \underline{\mu}\underline{\epsilon}$, $\displaystyle \underline{\mu} = \frac{\mu_0}{1 + j\omega\tau}$.
> 
> Interprétons l'équation différentielle. L'amplificateur opérationnel est un amplificateur de différence $v_s = \mu(v_+ - v_-)$. Plus précisément, c'est un amplificateur différentiel intégré. Son amplification différentielle en régime continu est $\mu_0$ (notée aussi $A_d$) et son temps de relaxation est $\tau$.
>  Vérifions que la relation $\tau\dfrac{dv_s}{dt}+ v_s = \mu_0\epsilon$ conduit à des résultats compatibles avec ceux du [[#^par1|paragraphe 1]].
>  La formule du pont diviseur appliquée au niveau de l'entrée inverseuse $(i_- = 0)$ donne ([[#^figure4|fig. 4]]) : $v_- = v_e - \epsilon = \frac{R_1}{R_1 + R_2}v_s$, d'où $v_s + \tau\dfrac{dv_s}{dt} = \mu_0\left(v_e - \frac{R_1}{R_1 + R_2}v_s\right)$. En régime sinusoïdal, cette équation s'écrit en notation complexe : $\underline{v}_s\left(\frac{1}{\mu_0} + \frac{R_1}{R_1 + R_2} + j\omega\frac{\tau}{\mu_0}\right) = \underline{v}_e$, ce qui entraîne, pour l'amplificateur non inverseur, la fonction de transfert. Cette fonction de transfert est celle d'un filtre passe-bas.
>  Dans l'hypothèse $\frac{R_2}{R_1} \ll \mu_0$ , l'équation de l'asymptote basse fréquence est : $G = 20\log\left(1 + \frac{R_2}{R_1}\right)$ et à haute fréquence : $G = -20\log\left(\frac{f}{f_0}\right)$, avec $f_0 = \frac{\mu_0}{2\pi\tau}$.
>  La fréquence $f_0$ est la fréquence de gain nul pour l'amplificateur non inverseur et sa valeur est indépendante de $R_1$ et $R_2$.
>  Par ailleurs, calculons le gain de l'amplificateur opérationnel à la fréquence $f_0$ : $\underline{\mu} = \frac{\mu_0}{1 + j\mu_0}$, puisque $\omega_0\tau = \mu_0$, d'où : $20\log(|\underline{\mu}|) \approx 0$, car $\mu_0 \gg 1$.
>  La fréquence $f_0$ est aussi la fréquence de coupure à gain nul de l'amplificateur opérationnel.
>  
>  Les résultats expérimentaux sont compatibles avec le modèle que nous avons donné de l'amplificateur opérationnel réel (remarquons que $\tau$ est voisin de 2 ms pour le 741 puisque $\mu_0 \approx 10^{5}$ et $f_0 \approx 10^{6} Hz$).
>  Remarques : La mesure de $f_0$ est simple (intersection de l'asymptote haute fréquence avec la droite $G_{dB} = 0$), alors que la valeur importante de $\mu_0$ $(\approx 10^{5})$ rend sa mesure délicate.
^par2

> [!note] Étude dynamique du montage amplificateur non inverseur : Stabilité
> Nous avons constaté empiriquement que le montage est stable si la rétroaction s'effectue sur l'entrée inverseuse. Le modèle de fonction de transfert passe-bas adopté pour l'amplificateur opérationnel permet d'expliquer ce phénomène.
> Il suffit de reprendre l'équation différentielle obtenue au [[#^par2|paragraphe 2]], nous remarquons que le régime transitoire est du type $Ae^{-\frac{t}{\tau_0}}$, avec : $\tau_0 \approx \frac{\tau(R_1 + R_2)}{\mu_0R_1}$. La durée de ce régime est très brève (de l'ordre de la microseconde) pour le montage non inverseur.
> 
> Permuter les entrées + et – est équivalent à changer $\mu_0$ en $-\mu_0$. La solution transitoire est alors du type $Ae^{\frac{t}{\tau_0}}$. L'amplificateur opérationnel atteint théoriquement très rapidement la saturation (temps de l'ordre de la microseconde).
> En fait, la vitesse de balayage $\sigma$ de l'amplificateur opérationnel impose un temps de passage de 0 V à 15 V de l'ordre de 30 μs pour un 741.

> [!note] Comparateur non inverseur à hystérésis
> Le schéma de principe de ce type de comparateur est donné [[#^figure6|figure 6]]. La tension différentielle de ce comparateur est obtenue à l'aide du théorème de Millman : $v_{de} = v_+ - v_- = \frac{R_2v_e + R_1v_s}{R_1 + R_2} - V_{ref}$.
> Lorsque l'amplificateur opérationnel est saturé positivement, nous avons tout à la fois : $v_s = +V_{sat}$ et $v_{de} > 0$. Ce qui implique, en remplaçant $v_s$ par $+V_{sat}$ dans l'expression précédente de $v_{de}$ : $v_e > \frac{R_1 + R_2}{R_2}V_{ref} - \frac{R_1}{R_2}V_{sat} = V_{e_1}$.
> Le basculement de $v_s = +V_{sat}$ à $v_s = -V_{sat}$ se fait donc pour la tension de seuil $v_e = V_{e_1}$ au point de fonctionnement $B$.
> En revanche, lorsque l'amplificateur opérationnel est saturé négativement, nous avons : $v_s = -V_{sat}$ et $v_{de} < 0$. Ce qui entraîne, en remplaçant $v_s$ par $-V_{sat}$ dans l'expression précédente de $v_{de}$ : $v_e < \frac{R_1 + R_2}{R_2}V_{ref} + \frac{R_1}{R_2}V_{sat} = V_{e_2}$.
> Le basculement de $v_s = -V_{sat}$ à $v_s = +V_{sat}$ s'effectue à la tension de seuil $v_e = V_{e_2}$ au point de fonctionnement $B'$.
> Ces résultats conduisent à la caractéristique de transfert du [[#^figure7|figure 7]]. Le cycle d'hystérésis est centré en $V_{e_0} = \frac{R_1 + R_2}{R_2}V_{ref}$ et sa largeur est $\Delta V_e = 2\frac{R_1}{R_2}V_{sat}$.
> Remarque : La résistance d'entrée de ce comparateur est de l'ordre de $R_1$.

> [!note] Comparateur inverseur à hystérésis
> Le schéma de principe de ce type de comparateur est donné sur la [[#^figure8|figure 8]]. Par application de la relation de Millman à l'entrée non inverseuse de l'amplificateur opérationnel, nous obtenons : $v_+ = \frac{\frac{V_{ref}}{R_1} + \frac{v_s}{R_2}}{\frac{1}{R_1} + \frac{1}{R_2}}$, soit $v_{de} = v_+ - v_e = \frac{R_2V_{ref} + R_1v_s}{R_1 + R_2} - v_e$.
> Lorsque l'amplificateur opérationnel est saturé positivement, nous avons tout à la fois : $v_s = +V_{sat}$ et $v_{de} > 0$. Ce qui implique, en remplaçant $v_s$ par $+V_{sat}$ dans l'expression précédente de $v_{de}$ : $v_e < \frac{R_2}{R_1 + R_2}V_{ref} + \frac{R_1}{R_1 + R_2}V_{sat} = V_{e_2}$.
> Le basculement de $v_s = +V_{sat}$ à $v_s = -V_{sat}$ se fait donc pour la tension de seuil $v_e = V_{e_2}$ au point de fonctionnement $B$.
> En revanche, lorsque l'amplificateur opérationnel est saturé négativement, nous avons : $v_s = -V_{sat}$ et $v_{de} < 0$. D'où, en remplaçant $v_s$ par $-V_{sat}$ dans l'expression précédente de $v_{de}$ : $v_e > \frac{R_2}{R_1 + R_2}V_{ref} - \frac{R_1}{R_1 + R_2}V_{sat} = V_{e_1}$.
> Le basculement de $v_s = -V_{sat}$ à $v_s = +V_{sat}$ s'effectue à la tension de seuil $v_e = V_{e_1}$ au point de fonctionnement $B'$.
> Ces résultats permettent de tracer la caractéristique de transfert du [[#^figure9|figure 9]]. Le cycle d'hystérésis est centré en $V_{e_0} = \frac{R_2}{R_1 + R_2}V_{ref}$ et sa largeur est $\Delta V_e = 2\frac{R_1}{R_1 + R_2}V_{sat}$.
> Remarque : La résistance d'entrée de ce comparateur est très grande est son attaque par le générateur délivrant $v_e(t)$ se fait automatiquement en tension. C'est une qualité que ne possède pas son homologue non inverseur dont l'impédance d'entrée est $R_1$ et pour lequel il faut utiliser un générateur d'impédance interne faible devant $R_1$.

> [!note] Multivibrateur astable : Principe
> Le montage est constitué de deux éléments : un comparateur à hystérésis et un intégrateur, dont le rôle est de faire glisser le point de fonctionnement M du comparateur vers ses points de basculement B et B' ([[#^figure13|fig. 13]] et [[#^figure14|14]]).
> Plusieurs montages sont possibles selon que le comparateur est inverseur ou non et selon la nature du circuit associé.
> Considérons un comparateur inverseur à hystérésis pour lequel $V_{ref} = 0$. Quand $v_s = +V_{sat}$, le point de fonctionnement $M$ du comparateur doit se déplacer de $A$ vers $B$ qui est le point de basculement à saturation positive ([[#^figure14|fig. 14]]). En revanche, lorsque $v_s = -V_{sat}$, le point de fonctionnement $M'$ du comparateur doit se déplacer de A' vers B' qui est le point de basculement à saturation négative.
> Pour qu'il en soit ainsi, il faut et il suffit que : $v_s = +V_{sat}$ entraîne $\dfrac{dv_e}{dt} > 0$ et $v_s = -V_{sat}$ entraîne $\dfrac{dv_e}{dt} < 0$, c'est-à-dire que $\dfrac{dv_e}{dt}$ doit être du signe de $v_s$.
> Ces deux conditions sont simultanément réalisées par le circuit (R, C) (circuit pseudo-intégrateur) alimenté sous $v_s$ et délivrant $v_e$ ([[#^figure15|fig. 15]]). En effet, la loi des nœuds appliquée en $E$ donne : $\dfrac{dv_e}{dt} = \frac{v_s - v_e}{\tau}$ avec $\tau =RC$ constante de temps du circuit (R, C). La dérivée $\dfrac{dv_e}{dt}$ est bien du signe de $v_s$ puisque : $|v_s| = V_{sat} > |v_e|$.
> La tension de sortie $v_s$ du circuit bascule indéfiniment entre $+V_{sat}$ et $-V_{sat}$ : c'est un multivibrateur astable. Son chronogramme est donné [[#^figure16|figure 16]].
> Remarque : Bien qu'une rétroaction existe sur la borne - de l'A.O., ce montage est instable ; cette rétroaction est rendue inexistante par la présence de la capacité qui ne peut admettre de discontinuité de potentiel entre ses bornes : une variation brusque de potentiel de $S$ ne peut entraîner une variation brusque de celui de $E$.

> [!note] Multivibrateur astable : Calcul de la période et du rapport cyclique
> Pour ce calcul prenons comme nouvelle origine des temps la date d'un basculement, par exemple, de $+V_{sat}$ vers $-V_{sat}$. À $t = 0$, ce basculement s'est produit parce que $v_e(0) = V_{e_2} = \frac{R_1}{R_1 + R_2}V_{sat}$.
> À partir de cette date, le condensateur se charge à travers $R$ sous la tension constante $v_s = -V_{sat}$. La loi d'évolution de $v_e(t)$ est donnée par la relation : $\dfrac{dv_e}{dt} = \frac{v_s - v_e}{\tau}$ dans $v_s = -V_{sat}$. Ce qui conduit à une équation différentielle dont la solution est $v_e(t) = (V_{e_2} + V_{sat})e^{-\frac{t}{\tau}} - V_{sat}$.
> La tension $v_e(t)$ décroît à partir de $V_{e_2}$ pour tendre vers la tension $-V_{sat}$ qu'elle n'atteindra pas. En effet, à $t = t_1$, la tension $v_e(t)$ aura la valeur : $V_{e_1} = -\frac{R_1V_{sat}}{R_1 + R_2} \quad (< V_{e_2})$ et un nouveau basculement se produira amenant la tension de sortie de $-V_{sat}$ à $+V_{sat}$. La date $t = t_1$ se calcule en écrivant : $v_e(t_1) = V_{e_1} = (V_{e_2} + V_{sat})e^{-\frac{t_1}{\tau}} - V_{sat}$, d'où $t_1 = \tau\ln\left(\frac{V_{e_2} + V_{sat}}{V_{e_1} + V_{sat}}\right)$.
> Le condensateur se charge alors à travers $R$ sous la tension constante $v_s = V_{sat}$. La tension $v_e(t)$ croît à partir de $V_{e_1}$ pour tendre vers la tension $V_{sat}$ qu'elle n'atteindra pas. En effet, à $t = t_1 + t_2$ la tension $v_e(t)$ aura la valeur $V_{e_2} \quad (> V_{e_1})$ et un nouveau basculement se produira amenant la tension de sortie de $+V_{sat}$ à $-V_{sat}$. Le phénomène se poursuit ainsi indéfiniment.
> Le calcul de la durée $t_2$, qui se mène comme celui de la durée $t_1$, donne : $t_2 = \tau\ln\left(\frac{V_{e_1} - V_{sat}}{V_{e_2} - V_{sat}}\right)$.
> Posons $k = \frac{R_1}{R_1 + R_2}$, il vient $V_{e_1} = -kV_{sat}$ et $V_{e_2} = kV_{sat}$. Les expressions des durées $t_1$ et $t_2$ se simplifient et nous constatons qu'elles sont égales, ce qui était prévisible car le cycle est symétrique : $t_1 = t_2 = \tau\ln\left(\frac{1 + k}{1 - k}\right)$. La période de l'astable est $T = t_1 + t_2 = 2\tau\ln\left(\frac{1 + k}{1 - k}\right)$ et son rapport cyclique $\delta$, qui est, par définition, le rapport de la durée de l'état à saturation positive $t_2$ sur la période $T$, vaut $\delta = \frac{t_2}{T} = 0,5$.

> [!note] Multivibrateur astable : Contrôle de la période et du rapport cyclique
> La période est proportionnelle à la constante de temps $\tau = RC$. Nous pouvons contrôler la période en utilisant une résistance $R$ variable ou un condensateur $C$ variable. Nous utiliserons un condensateur $C$ variable, réservant la résistance $R$ pour le contrôle du rapport cyclique.
> Pour modifier le rapport cyclique sans modifier la fréquence, il suffit de faire varier de la même quantité et en sens opposé les deux constantes de temps $\tau_1$ et $\tau_2$ associées aux deux durées $t_1$ et $t_2$. Le montage réalisé est indiqué [[#^figure17|figure 17]]. Les résistances $r$ sont des résistances de protection lorsque $x$ prend une de ses valeurs extrêmes 0 ou 1. En fait, le courant maximum pouvant passer dans les diodes correspond au courant de saturation de l'amplificateur opérationnel (20 mA). Si les diodes supportent une intensité de l'ordre de 20 mA, il est inutile de mettre des résistances r de protection.
> Pendant la durée $t_2$ de l'état de saturation positive de l'A.O., la diode $D_1$ est bloquée tandis que la diode $D_2$ conduit. La constante de temps de charge du condensateur est : $\tau_2 = (xR + r)C$.
> En revanche, pendant la durée $t_1$ de l'état de saturation négative de l'A.O., c'est la diode $D_2$ qui est bloquée tandis que la diode $D_1$ conduit. La nouvelle constante de temps de charge du condensateur est : $\tau_1 = [(1 - x)R + r]C$. D'où l'expression de la période $T$ de l'astable : $T = t_1 + t_2 = (\tau_1 + \tau_2)\ln\left(\frac{1 + k}{1 - k}\right) = (R + 2r)C\ln\left(\frac{1 + k}{1 - k}\right)$, qui est indépendant de x.
> En revanche, la nouvelle expression du rapport cyclique $\delta = \frac{xR + r}{R + 2r}$ est une fonction affine de x, ce qui permet son contrôle.
^par3

> [!note] Principe des générateurs de fonctions : Système oscillateur
> Un générateur de fonctions est généralement constitué d'une boucle comprenant un comparateur à hystérésis et un intégrateur ([[#^figure22|fig. 22]]). Il est conçu de telle sorte que le point de fonctionnement du comparateur se déplace vers ses points de basculement B et B'.
> Il est possible d'utiliser les deux types de comparateurs à condition de lui associer le type d'intégrateur adéquat.
> Nous prenons l'exemple d'un comparateur non inverseur à hystérésis.
> La caractéristique d'un tel comparateur, avec $V_{ref} = 0$, est rappelée [[#^figure23|figure 23]]. Quand $v_s = V_{sat}$, le point de fonctionnement $M$ du comparateur doit se déplacer de $A$ vers $B$ qui est le point de basculement à saturation positive.
> En revanche, lorsque $v_s = -V_{sat}$, le point de fonctionnement $M'$ du comparateur doit se déplacer de A' vers B' qui est le point de basculement à saturation négative.
> Pour qu'il en soit ainsi, il faut et il suffit que : $v_s = +V_{sat}$ entraîne $\dfrac{dv_e}{dt} < 0$ et $v_s = -V_{sat}$ entraîne $\dfrac{dv_e}{dt} > 0$.
> Ces deux conditions sont simultanément réalisées par un intégrateur inverseur commandé par $v_s$ et délivrant $v_e$ : $\dfrac{dv_e}{dt} = -\frac{1}{\tau}v_s$, avec $\tau$ constante de temps de l'intégrateur.
> D'où la réalisation donnée [[#^figure24|figure 24]] et le chronogramme correspondant donné [[#^figure25|figure 25]].

> [!note] Principe des générateurs de fonctions : Calcul de la période
> Prenons pour origine des temps l'instant auquel se produit un basculement, par exemple, de $+V_{sat}$ vers $-V_{sat}$. À cette date, nous avons : $v_e(0) = V_{e_1} = -\frac{R_1}{R_2}V_{sat}$.
> À partir de ce moment, l'intégrateur est attaqué avec une tension constante $v_s = -V_{sat}$. La loi des nœuds appliquée à l'entrée inverseuse de l'intégrateur donne : $-\frac{V_{sat}}{R} + C\dfrac{dv_e}{dt} = 0$, soit $dv_e = \frac{V_{sat}}{RC}dt$.
> Ainsi, $v_e(t)$ croît avec le temps à partir de la valeur $V_{e_1}$ : $v_e(t) = V_{e_1} + \frac{V_{sat}}{RC}t$.
> À la date $t = t_1$, il atteindra la valeur $V_{e_2}$ et un basculement de $-V_{sat}$ vers $+V_{sat}$ se produira. La date $t_1$ de basculement se calcule à partir du résultat précédent : $t_1 = 2\frac{R_1}{R_2}RC$.
> Un nouveau basculement de $+V_{sat}$ vers $-V_{sat}$ se produira à $t = t_1 + t_2$, tel que : $t_1 = t_2 = \frac{T}{2}$, d'où $T = 4\frac{R_1}{R_2}RC$.
> La tension $v_s(t)$ à la sortie du comparateur est un signal carré de rapport cyclique $\delta = 0,5$ et, à la sortie de l'intégrateur, $v_e(t)$ est un signal triangulaire symétrique de même période.

> [!note] Principe des générateurs de fonctions : Contrôle de la période et du rapport cyclique
> C'est la même discussion que celle de la [[#^par3|paragraphe 3]]. Le montage réalisé est identique à celui utilisé pour l'astable ; il est donné [[#^figure26|figure 26]], où $0 \leqslant x \leqslant 1$. Les expressions de $\tau_1$, $\tau_2$ et $\delta$ restent les mêmes. Alors que les expressions de $t_1$ et $t_2$ et $T$ sont différents. En fait, $T = 2\frac{R_1}{R_2}(R + 2r)C$.
> Remarque : Le potentiomètre $(P_1)$ agit sur la largeur du cycle d'hystérésis, donc sur l'amplitude $|V_{e_1}| = V_{e_2}$ des signaux triangulaires. Les constantes de temps $\tau_1$ et $\tau_2$ ne sont pas affectées par les variations de $(P_1)$. Le rapport cyclique du signal carré est conservé, mais la période $T$ des signaux est modifiée. Si la capacité variable $C$ est réalisée avec un ensemble de capacités commutables, le potentiomètre $(P_1)$ permet un réglage de la fréquence à l'intérieur des différentes gammes de fréquences obtenues par commutation de $C$.
# Définitions
==**Principe des comparateurs à hystérésis**== :
- Montages instables : Les comparateurs sont des montages fonctionnant à saturation de la tension de sortie : $v_s = \pm V_{sat}$.  Nous avons étudié au [[07-L'amplificateur opérationnel. Le modèle idéal|chapitre 7]] le comparateur simple : idéalement, sa tension de sortie est égale à $\pm V_{sat}$ selon que la tension d'entrée est supérieure ou inférieure à une tension de référence. ==**Des montages à A.O. avec une boucle de rétroaction positive ([[#^figure6|fig. 6]] et [[#^figure8|8]]), pour lesquels le fonctionnement linéaire, instable, n'est pas observable, réalisent ce type de fonctionnement des comparateurs à hystérésis.**==
- Phénomène d'hystérésis : Pour ces montages, la commutation de $-V_{sat}$ à $+V_{sat}$ ne se fait pas pour la même tension d'entrée $v_e$ que la commutation de $+V_{sat}$ à $-V_{sat}$ ([[#^figure7|fig. 7]] et [[#^figure9|9]]) : l'état du système dépend non seulement de la valeur d'entrée $v_e$, mais aussi de ses états antérieurs. Le système garde la mémoire de son histoire : on appelle hystérésis le phénomène observé. Dans le plan ($v_e$, $v_s$), le système décrit un cycle d'hystérésis.

> [!note] Comparateur à hystérésis : Vérifications expérimentales
> Réalisons le comparateur inverseur à hystérésis décrit [[#^figure10|figure 10]], pour lequel : $V_{ref} = 0$.
> Réglons le G.B.F. pour qu'il délivre un signal sinusoïdal de fréquence $f = 50 Hz$ et d'amplitude $v_{e_m} = 5 V$. Observons les courbes données par l'oscillographe en mode bicourbe ([[#^figure11|fig. 11]]). Aucun défaut n'est perceptible. Commutons l'oscillographe en mode XY ([[#^figure12|fig. 12]]). La caractéristique est quasi idéale.
> Faisons varier le rapport $k = 2\frac{R_1}{R_1 + R_2}$ à l'aide du potentiomètre $(P_1)$. La caractéristique reste centrée en $V_{ref} = 0$, mais la largeur $\Delta V_e$ du cycle est fonction du rapport $k$. Nous vérifions à cette occasion sa formule.
> Diminuons la fréquence du signal délivré par le G.B.F. : un balayage assez lent de la tension d'entrée permet de percevoir le sens des basculements aux points de fonctionnement B et B' ([[#^figure9|fig. 9]]) afin d'en vérifier l'accord avec la théorie.

> [!note] Multivibrateur astable : Vérifications expérimentales
> Réalisons le montage du [[#^figure18|figure 18]], avec $C = 1 \mu F$ (boîte de condensateurs).
> Observons à l'oscilloscope, en mode bicourbe, la forme des signaux $v_e(t)$ et $v_s(t)$. Faisons varier le curseur du potentiomètre $(P)$ et examinons les modifications des signaux $v_e(t)$ et $v_s(t)$. Nous remarquons une modification du rapport cyclique sans modification de période.
> Plaçons le curseur du potentiomètre en position moyenne et faisons varier la valeur de la capacité $C$. Observons les modifications des signaux $v_e(t)$ et $v_s(t)$. Pour des valeurs connues de $C$, nous pouvons vérifier la proportionnalité de la période $T$ à $C$.
> Le curseur du potentiomètre $(P)$ étant toujours en position moyenne diminuons progressivement la valeur de la capacité $C$. Observons la déformation de plus en plus accentuée des signaux $v_e(t)$ et $v_s(t)$ ([[#^figure19|fig. 19]] et [[#^figure20|20]]). En utilisant le signal $v_s(t)$, évaluons la vitesse maximale de balayage $\sigma$ de l'A.O.
> - La déformation des signaux est due à la vitesse finie de balayage des tensions $v_e(t)$ et $v_s(t)$. Quand cette vitesse de balayage atteint sa valeur maximale, les flancs de $v_s(t)$ ne sont plus verticaux.
> Plaçons l'oscilloscope en mode $XY$ et observons la courbe $v_s = f(v_e)$ du comparateur.
> - On n'observe que la partie de la caractéristique utilisée durant le fonctionnement du comparateur ([[#^figure21|fig. 21]]).
# Diagrammes
Amplificateur non inverseur. Un oscilloscope bicourbe mesure simultanément $u_e(t)$ et $u_s(t)$
![[electronique1/attachments-electronique1/figure242.png]]^figure1

Amplificateur non inverseur
![[electronique1/attachments-electronique1/figure245.png]]^figure4

Comparateur non inverseur à hystérésis
![[electronique1/attachments-electronique1/figure246.png]]^figure6

Comparateur inverseur à hystérésis
![[electronique1/attachments-electronique1/figure248.png]]^figure8

Montage expérimental pour l'étude d'un comparateur à hystérésis
![[electronique1/attachments-electronique1/figure250.png]]^figure10

Multivibrateur astable à A.O
![[electronique1/attachments-electronique1/figure255.png]]^figure15

Astable à A.O. avec contrôle de la fréquence et du rapport cyclique. $R_1 = R_2 = 20 k\Omega$ ; $R = 10 k\Omega$ ; $r = 100 \Omega$ et $C$ boîte de condensateurs
![[electronique1/attachments-electronique1/figure257.png]]^figure17

Montage expérimental pour l'étude d'un multivibrateur astable
![[electronique1/attachments-electronique1/figure258.png]]^figure18

Principe d'un générateur de fonctions
![[electronique1/attachments-electronique1/figure262.png]]^figure22

Générateur de fonctions à intégrateur non inverseur à hystérésis
![[electronique1/attachments-electronique1/figure264.png]]^figure24

Générateur de fonctions avec contrôle de la fréquence et du rapport cyclique
![[electronique1/attachments-electronique1/figure266.png]]^figure26
# Graphiques
Diagramme de Bode obtenu pour $R_1 = 1 k\Omega$ et $R_2$ variant de $1 k\Omega$ à $100 k\Omega$
![[electronique1/attachments-electronique1/figure243.png]]^figure2

Déphasage $\varphi$ de $v_s$ par rapport à $v_e$. Phase mesurée pour $R_1 = 1 k\Omega$ et $R_2$ variant de $1 k\Omega$ à $100 k\Omega$
![[electronique1/attachments-electronique1/figure244.png]]^figure3

Caractéristique d'un comparateur non inverseur à hystérésis
![[electronique1/attachments-electronique1/figure247.png]]^figure7

Caractéristique d'un comparateur inverseur à hystérésis
![[electronique1/attachments-electronique1/figure249.png]]^figure9

Réponse d'un comparateur inverseur à l'hystérésis à une excitation sinusoïdale de fréquence 50 Hz et d'amplitude 5 V
![[electronique1/attachments-electronique1/figure251.png]]^figure11

Caractéristique d'un comparateur inverseur à hystérésis obtenue avec une excitation sinusoïdale de fréquence 50 Hz et d'amplitude 5 V
![[electronique1/attachments-electronique1/figure252.png]]^figure12

Pour réaliser un multivibrateur astable, le point de fonctionnement du comparateur non inverseur doit glisser de A vers B, puis de A' vers B'
![[electronique1/attachments-electronique1/figure253.png]]^figure13

Pour réaliser un multivibrateur astable, le point de fonctionnement du comparateur non inverseur doit glisser de A vers B, puis de A' vers B'
![[electronique1/attachments-electronique1/figure254.png]]^figure14

Chronogramme d'un multivibrateur astable
![[electronique1/attachments-electronique1/figure256.png]]^figure16

Multivibrateur astable $C = 1 \mu F$ : les signaux sont conformes à la théorie
![[electronique1/attachments-electronique1/figure259.png]]^figure19

Multivibrateur astable $C = 10 nF$ : les signaux sont déformés à cause de la vitesse de balayage de l'A.O
![[electronique1/attachments-electronique1/figure260.png]]^figure20

Le point de fonctionnement de l'astable décrit le cycle ABA'B'A $(C = 1 \mu F)$
![[electronique1/attachments-electronique1/figure261.png]]^figure21

Caractéristique d'un comparateur non inverseur à hystérésis. $V_{ref} = 0$ et $V_{e_2} = |V_{e_1}| = \frac{R_1}{R_2}V_{sat}$
![[electronique1/attachments-electronique1/figure263.png]]^figure23

Chronogrammes d'un générateur de fonctions à comparateur non inverseur à hystérésis
![[electronique1/attachments-electronique1/figure265.png]]^figure25
# Expériences
> [!warning]
> Voici des exemples de travaux pratiques qui abordent le sujet de ce chapitre : le [lien 1](https://www.technologuepro.com/cours-electronique-analogique-2/tp3-applications-non-lineaires-un-amplificateur-operationnel.pdf), le [lien 2](https://staff.univ-batna2.dz/sites/default/files/benacer-saddok/files/tpn02_eln-app_m1_as-aii.pdf), le [lien 3](https://www.etienne-thibierge.fr/tp_2025/tp05_comparateurs_eleve.pdf), le [lien 4](https://fr.scribd.com/document/716274662/tp-ali-comparateur-simple-et-hysteresis), le [lien 5](https://chamilo.grenoble-inp.fr/courses/PHELMA3PMKTET0/document/Docs_site/sujets_elec/1-AOP.pdf), le [lien 6](https://pdfcoffee.com/tp-comparateur-pdf-free.html), le [lien 7](https://ressources.unisciel.fr/sillages/physique/electronique_2a_pc/res/TP_sur_le_Multivibrateur_astable.pdf), le [lien 8](http://cr4ckt3am.free.fr/perso/TP%2011%20-%20Sujet%20(2012-05-10%20181941).pdf), le [lien 9](http://www.jeanpaulbiberian.net/Download/TP%20Electronique.pdf), le [lien 10](http://olivier.granier.free.fr/PC-Montesquieu445072/cariboost_files/Elec3-aop-1.pdf), le [lien 11](http://lionel.goub.free.fr/==COURS==/N3/Electronique/TP%20Elec/Osc%20Relax/tp_osc_relax.pdf), le [lien 12](http://benoit.decoux.free.fr/ENSEIGNEMENT/ELEC_P1P2/P1_ao.pdf), le [lien 13](https://fr.scribd.com/document/444638354/TP-les-comparateurs), le [lien 14](http://leroy.pe.free.fr/psi_new/tp/tp_oscillateurs.pdf), le [lien 15](https://www.yumpu.com/fr/document/read/27983712/tp-cours-amplificateur-opacrationnel-physique-en-sup-4), le [lien 16](http://fabrice.sincere.free.fr/cm_electronique/Travaux%20pratiques/tp_generateursignaux_v60/web_TPgenerateur_signaux_v60.pdf), le [lien 17](https://clemdelasalle.fr/media_in_docs/Pr%C3%A9pa+Physique+PT+TPs+%C3%89lectricit%C3%A9+05_Multivibrateur_astable.pdf/), le [lien 18](https://l2ep.univ-lille.fr/pagesperso/francois/files/L2_eni2_tp.pdf), le [lien 19](https://www.etienne-thibierge.fr/tp_2025/tp06_multivibrateur.pdf), le [lien 20](https://staff.univ-batna2.dz/sites/default/files/litim_moussa/files/3algb-tp-eg-06.pdf), le [lien 21](https://fr.scribd.com/document/709053332/TP2-MULTIVIBRATEUR-ASTABLE), le [lien 22](https://www.etienne-thibierge.fr/tp_2024/tp05_multivibrateur.pdf), le [lien 23](http://estelle.vh.free.fr/Physique_PC/Support_files/TP01_Cours_Multivibrateur_astable.pdf), le [lien 24](https://fr.scribd.com/document/815345163/TP03-multivibrateur), le [lien 25](http://elearning.univ-dbkm.dz/pluginfile.php/25487/mod_resource/content/1/TP_EApp_M%201_AII_1-converti.pdf), le [lien 26](http://psi2.nantes.free.fr/TP/ENONCES-ET-CORRIGES-TP/TP-ELECTRONIQUE/ENONCE-TP-ELECTRONIQUE/TP-7-ENONCE.pdf), le [lien 27](https://pdfcoffee.com/tp32020-pdf-free.html), le [lien 28](https://fr.scribd.com/document/722017087/1712443445441-TP5-preparation), le [lien 29](http://venturi.marc.free.fr/TP/TP_Fascicule_premiere_periode.pdf), le [lien 30](https://staff.univ-batna2.dz/sites/default/files/litim_moussa/files/3algb-tp-eg-05.pdf), le [lien 31](https://staff.univ-batna2.dz/sites/default/files/litim_moussa/files/tpn03_eln-app_m1_as-aii.pdf).
# Autres notes
