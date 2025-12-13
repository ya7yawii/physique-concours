---
titre: "[[09-Filtres du deuxième ordre]]"
tags:
  - passe-bas
  - passe-haut
  - ordre-deux
  - passe-bande
  - pont-de-Wien
  - oscillateur-quasisinusoïdal
  - filtre-sélectif
crée: 16-11-2025, 13:38
---
# Formules
> [!note] Exemple de filtre d'ordre deux
> Étudions le circuit représenté sur la [[#^figure1|figure 1]].
> Nous reconnaissons un filtre passe-bas et un filtre passe-haut d'ordre un séparés par un suiveur.
> Le suiveur permet d'assurer l'égalité $u_2 = u_3$ avec un courant $i_2$ nul.
> Comme le courant $i_2$ est nul : $\underline{H}_1(j\omega) = \frac{\underline{u}_{2m}}{\underline{u}_{1m}} = \frac{1}{1 + j\frac{\omega}{\omega_1}}$ avec $\omega_1 = \frac{1}{R_1C_1}$.
> Comme la sortie est ouverte $(i_4 = 0)$ : $\underline{H}_2(j\omega) = \frac{\underline{u}_{4m}}{\underline{u}_{3m}} = \frac{j\frac{\omega}{\omega_2}}{1 + j\frac{\omega}{\omega_2}}$ avec $\omega_2 = \frac{1}{R_2C_2}$.
> Nous en déduisons la fonction de transfert $\underline{H}(j\omega) = \frac{\underline{u}_{4m}}{\underline{u}_{1m}}$ du système complet : $\underline{H}(j\omega) = \underline{H}_1(j\omega)\underline{H}_2(j\omega) = \frac{j\frac{\omega}{\omega_2}}{\left(1 + j\frac{\omega}{\omega_1}\right)\left(1 + j\frac{\omega}{\omega_2}\right)}$. Nous obtenons une fonction de transfert du second ordre. Le tracé asymptotique de la courbe de gain se déduit de ceux de chaque filtre d'ordre un ([[#^figure2|fig. 2]]).
> Nous sommes donc en présence d'un filtre qui élimine à la fois les hautes et les basses fréquences. Il s'agit d'un type de filtre, appelé passe-bande.
> Nous pourrons rencontrer des réalisations variées de filtre d'ordre deux. L'association de deux filtres d'ordre un semble naturelle, mais ne permet pas de réaliser tous les transferts d'ordre deux. En utilisant un circuit de type (R, L, C), dont le facteur de qualité est ajustable, nous accéderons à une présentation plus générale de ces filtres.
> Remarque : le circuit (R, L, C) est facile à aborder mais assez peu utilisé en pratique. Dans les circuits électriques, on préfère généralement employer des résistances et capacités, composants peu encombrants et bon marché, plutôt que des bobines, qui peuvent éventuellement être simulées.
^par1

> [!note] Filtre passe-bas d'ordre deux
> La réponse en charge du circuit (R, L, C) série à une excitation sinusoïdale en tension a été étudiée au [[06-Régime sinusoïdal forcé|chapitre 6]]. Reprenons celle-ci en utilisant les impédances complexes des composants, et interprétons-la en terme de filtrage.
> - Exemple de fonction de transfert passe-bas d'ordre deux : Le filtre étudié est représenté sur la [[#^figure3|figure 3]]. Fonctionnant à vide $(\underline{i}_2(t) = 0)$, il réalise un diviseur de tension : $\underline{H} = \frac{\underline{u}_{2m}}{\underline{u}_{1m}} = \frac{\frac{1}{jC\omega}}{R + jL\omega + \frac{1}{jC\omega}}$. Notons par $\omega_0 = \frac{1}{\sqrt{LC}}$ la pulsation propre, par $x = \frac{\omega}{\omega_0}$ la pulsation réduite et par $2\sigma = RC\omega_0 = \frac{R}{L\omega_0} = \frac{1}{Q}$ l'inverse du facteur de qualité du circuit (R, L, C) série. Avec ces notations, la fonction de transfert s'écrit : $\underline{H}(jx) = \frac{1}{1 + 2\sigma(jx) + (jx)^{2}} = \frac{1}{1 - x^{2} + j\frac{x}{Q}}$.
> - Courbe de réponse en gain : Le gain du filtre est : $G(x) = -10\log[(1 - x^{2})^{2} + 4\sigma^{2}x^{2}]$.
> 	- Asymptote basse fréquence : En très basse fréquence, l'inductance $L$ se comporte comme un interrupteur fermé et la capacité $C$ comme un interrupteur ouvert. Le circuit étant ouvert en sortie, aucun courant ne traverse la résistance $R$, donc $\underline{u}_{1m} = \underline{u}_{2m}$ et $G = 0$. La courbe de réponse en gain admet, en basse fréquence, une asymptote horizontale à $G = 0$ dB.
> 	- Asymptote haute fréquence : En haute fréquence, la capacité se comporte comme un interrupteur fermé, donc $\underline{u}_{2m} = 0$, alors $\underline{u}_{1m} \neq 0$. Donc $G(x) \rightarrow -\infty$. Lorsque $x \gg 1$, la valeur asymptotique du gain est $G = -10\log(x^{4}) = -40X$. La courbe de réponse en gain admet, en haute fréquence, une asymptote passant par l'origine de pente -40 dB/décade ([[#^figure4|fig. 4]]).
> 	- Diagramme asymptotique :
> 	Le diagramme asymptotique est la réunion des deux asymptotes basses fréquences et hautes fréquences limitées à leur point de concours. Évaluons la qualité de cette représentation asymptotique en calculant, pour $x = 1$, l'écart entre le graphe de la réponse en gain et sa représentation asymptotique : $\Delta G = G(1) - G_A = -20\log(2\sigma) = 20\log(Q)$. Cet écart peut être considérable si le facteur d'amortissement $2\sigma$ est faible (ou le facteur de qualité $Q$ élevé) ([[#^figure5|fig. 5]]). Le diagramme asymptotique est généralement insuffisant pour décrire la réponse en gain d'un filtre du second ordre. Nous sommes conduits à préciser les variations de la courbe de réponse en gain.
> 	Posons : $y = (1 - x^{2})^{2} + 4\sigma^{2}x^{2}$. Cette fonction bicarrée passe par un maximum pour : $x_s = \sqrt{1 - 2\sigma^{2}}$, lorsque $\sigma < \frac{\sqrt{2}}{2} \Leftrightarrow Q > \frac{\sqrt{2}}{2} \approx 0,707$.
> 	Pour la fonction de filtrage, l'existence d'un extremum, surtout accentué, est un défaut. Le gain d'un filtre ne doit avoir que de faibles variations en bande passante. En conséquence, un filtre passe-bas d'ordre deux est réalisé généralement avec des valeurs du facteur de qualité $Q$ de l'ordre de $\frac{\sqrt{2}}{2}$.
> - [[#^info1|Courbe de réponse en phase]] : Le déphasage de $\underline{u}_{2m}$ par rapport à $\underline{u}_{1m}$ est $\varphi(x) = \arg[\underline{H}(jx)]$, dont les valeurs asymptotiques sont $\varphi = 0$ en basse fréquence et $\varphi = -\pi$ en haute fréquence. Par ailleurs, quelle que soit la valeur de $\sigma$, la courbe de réponse en phase passe par le point $A\left(0 ; -\frac{\pi}{2}\right)$ ([[#^figure6|fig. 6]]).
> Le diagramme asymptotique de la réponse en phase constitué des deux asymptotes B.F. $(\phi = 0)$ et H.F. $(\phi = -\pi)$, ne décrit pas la rotation de phase au voisinage de $X = 0$. Il peut être complété comme indiqué en [[#^figure7|figure 7]] par le segment $A_1AA_2$. La rotation de phase s'effectue pour l'essentiel au voisinage de $X = 0$ et elle est d'autant plus rapide que $\sigma$ est petit (ou $Q$ élevé) ([[#^figure8|fig. 8]]).

> [!note] Filtre passe-bas d'ordre deux : Généralisation
> La fonction de transfert d'un filtre passe-bas d'ordre deux peut se mettre sous la forme : $\displaystyle\underline{H}(j\omega) = \frac{A_0}{1 - \frac{\omega^{2}}{\omega_{0}^{2}} + \frac{j}{Q}\frac{\omega}{\omega_0}} = \frac{A_0}{1 - x^{2} + j\frac{x}{Q}}$.
> Son diagramme de Bode est caractérisé par :
> -  une asymptote basse fréquence d'ordonnée : $G_{(dB)} = 20\log A_0$ ;
> - une asymptote haute fréquence de pente -40 dB/décade ;
> - une résonance pour $\omega < \omega_0$ si $Q > \frac{1}{\sqrt{2}}$.
> - $\underline{H}(j\omega_0) = QA_0$.
> 
> Remarques :
> - Si le facteur $A_0$ n'est pas réel positif, cela revient simplement à ajouter un déphasage constant au signal de sortie correspondant à ces écritures ;
> - On notera qu'il faut deux paramètres ($A_0$ et $\omega_0$) pour définir complètement un passe-bas d'ordre un et qu'il en faut trois ($A_0$, $Q$ et $\omega_0$) pour définir un passe-bas d'ordre deux.
> 
> Comportement à haute fréquence : À haute fréquence, c'est-à-dire lorsque la courbe de réponse en gain se confond avec l'asymptote haute fréquence, la partie principale du dénominateur est $- \frac{\omega^{2}}{\omega_{0}^{2}}$ et la fonction de transfert est équivalente à : $\underline{H}(j\omega) \approx A_0\omega_{0}^{2}\left(\frac{1}{j\omega}\right)^{2}$. Or, en notation complexe, multiplier par $\left(\frac{1}{j\omega}\right)^{2}$ revient à intégrer deux fois.
> <mark style="color: red">Lorsque la courbe de réponse en gain se confond avec l'asymptote haute fréquence, l'effet du filtre est pratiquement équivalent à une double intégration du signal d'entrée.</mark>
> Lorsque l'on affirme qu'un filtre est intégrateur, il est sous-entendu qu'en régime forcé, la tension de sortie $u_2(t)$ est proportionnelle à la primitive de $u_1(t)$ <mark style="color: red">dont la valeur moyenne est nulle</mark>. La tension de sortie est, en effet, égale à la somme de fonctions sinusoïdales de valeur moyenne nulle.

> [!note] Filtre passe-haut d'ordre deux
> - Exemple : Comme pour l'ordre un, le filtre passe-haut d'ordre deux est complémentaire du filtre passe-bas du même ordre. Le filtre réalisé est représenté sur la [[#^figure9|figure 9]]. Avec le même raisonnement que celui du passe-bas d'ordre 2, on obtient la fonction de transfert suivante : $\underline{H} = \frac{(jx)^{2}}{1 + 2\sigma(jx) + (jx)^{2}}$. La fonction de transfert $\underline{H}$, d'ordre deux, peut être considérée comme le produit de la fonction de transfert d'un double dérivateur $\underline{H}_1 = (jx)^{2}$ par celle d'un passe-bas d'ordre deux : $\underline{H}_2 = \frac{1}{1 + 2\sigma(jx) + (jx)^{2}}$. Il en résulte que son diagramme asymptotique de gain et de phase est la somme des diagrammes asymptotiques correspondant de $\underline{H}_1$ et de $\underline{H}_2$ comme il est indiqué ([[#^figure10|fig. 10]]) et que son diagramme de Bode est la somme des diagrammes de Bode de $\underline{H}_1$ et de $\underline{H}_2$ ([[#^figure11|fig. 11]]).
> L'examen du diagramme asymptotique de gain montre que le filtre étudié est un passe-haut. Par ailleurs, il est possible de démontrer que la courbe de réponse en gain du passe-haut réalisé est symétrique, par rapport à l'axe des gains, de celle du passe-bas de même facteur d'amortissement $2\sigma$.
> - Généralisation : La fonction de transfert d'un filtre passe-haut d'ordre deux peut se mettre sous la forme : $\displaystyle\underline{H}(j\omega) = \frac{-A_0\frac{\omega^{2}}{\omega_{0}^{2}}}{1 - \frac{\omega^{2}}{\omega_{0}^{2}} + \frac{j\omega}{Q\omega_0}} = +A_0\frac{-x^{2}}{1 - x^{2} + j\frac{x}{Q}}$. Son diagramme de Bode, symétrique de celui du filtre passe-haut se caractérise par :
> 	- une asymptote haute fréquence d'ordonnée égale à $20\log A_0$ ;
> 	- une asymptote basse fréquence de pente 40 dB/décade ;
> 	- l'intersection des asymptotes pour $\omega = \omega_0$ ;
> 	- une résonance pour $\omega > \omega_0$ si $Q > \frac{1}{\sqrt{2}}$ ;
> 	- $\underline{H}(j\omega_0) = jQA_0$.
> - Comportement à basse fréquence : À basse fréquence, c'est-à-dire lorsque la courbe de réponse en gain se confond avec l'asymptote basse fréquence la fonction de transfert est équivalente à : $\underline{H}(j\omega) \approx \frac{A_0}{\omega_{0}^{2}}(j\omega)^{2}$. Or, en notation complexe, multiplier par $(j\omega)^{2}$ revient à dériver deux fois.
> <mark style="color: red">Lorsque la courbe de réponse en gain se confond avec l'asymptote basse fréquence, l'effet du filtre est pratiquement équivalent à une double dérivation du signal d'entrée.</mark>
> La dérivation pose en général plus de problèmes que l'intégration. Si le signal d'entrée n'est pas sinusoïdal, il possède des harmoniques dont la fréquence est voisine de la fréquence caractéristique. Si le filtre est résonant $(Q > 1)$, ceux-ci sont amplifiés et la dérivation n'est plus observée.

> [!note] Filtre passe-bande d'ordre deux
> Nous avons vu au [[#^par1|paragraphe 1]] un exemple de filtre passe-bande. Nous allons étudier ce type de filtre à partir d'un autre exemple, celui du (R, L, C) série.
> Nous reprenons donc la réponse en courant (tension aux bornes de la résistance) du circuit (R, L, C) soumis à une tension sinusoïdale, étudiée au [[06-Régime sinusoïdal forcé|chapitre 6]].
> Le filtre étudié est représenté sur la [[#^figure12|figure 12]]. En utilisant le diviseur de tension et les mêmes notations que précédemment, l'expression de la fonction de transfert est : $\underline{H} = \frac{1}{1 + jQ\left(x - \frac{1}{x}\right)} = \frac{2\sigma(jx)}{1 + 2\sigma(jx) + (jx)^{2}}$.
> - Courbe de réponse en gain :
> 	- Asymptote basse fréquence : Aux très basses fréquences, la capacité $C$ se comporte comme un interrupteur ouvert et la résistance $R$ n'est pas alimentée. Donc $\underline{u}_2 = 0$, alors que $\underline{u}_1 \neq 0$ ce qui entraîne $G = -\infty$. En effet, lorsque $X \rightarrow -\infty$ $(x \ll 1)$, la valeur asymptotique du gain est : $G = 20X - 20\log(Q)$. La courbe de réponse en gain admet, en basse fréquence, une asymptote de pente 20 dB/décade ([[#^figure13|fig. 13]]).
> 	- Asymptote haute fréquence : En hautes fréquences, l'inductance $L$ se comporte comme un interrupteur ouvert et la résistance $R$ est, de nouveau, non alimentée, d'où la valeur asymptotique du gain $G = -\infty$. Si $X \rightarrow -\infty$ $(x \gg 1)$, alors : $G = -20X - 20\log(Q)$. La courbe de réponse en gain admet, en haute fréquence, une asymptote de pente –20 dB/décade ([[#^figure13|fig. 13]]).
> 	- Diagramme asymptotique : C'est au niveau du point de concours $A$ $[x = 1 ; G = -20\log(Q)]$ des deux demi-asymptotes que l'écart entre le diagramme asymptotique et la courbe de réponse en gain est le plus prononcé. Évaluons cet écart $\Delta G$ en remarquant que, quel que soit $Q$ (ou $2\sigma$), la courbe passe par le même maximum $S$ $(x = 1 \,\text{et}\, G(1) = 0)$. En conséquence : $\Delta G = G_S - G_A = 0 + 20\log(Q)$. Cet écart peut être considérable lorsque $Q$ (ou $2\sigma$) est très différent de 1 ([[#^figure14|fig. 14]]). L'examen de la réponse en gain montre que le filtre étudié est un passe-bande.
> 	- Bande passante : Calculons la bande passante à 3 dB du filtre. Les pulsations de coupure satisfont à l'équation : $|\underline{H}(x)| = \frac{1}{\sqrt{2}} \Rightarrow Q\left(x - \frac{1}{x}\right) = \pm 1$. Ce qui conduit à un ensemble de deux équations du second degré dont les quatre racines sont réelles. Ne retenant que les racines positives, il vient : $x_1 = -\frac{1}{2Q} + \sqrt{\left(\frac{1}{2Q}\right)^{2} + 1}$ et $x_2 = \frac{1}{2Q} + \sqrt{\left(\frac{1}{2Q}\right)^{2} + 1}$, d'où $x_2 - x_1 = \frac{\Delta\omega}{\omega_0} = \frac{1}{Q} =2\sigma$. La bande passante est inversement proportionnelle au facteur de qualité $Q$.
> - Courbe de réponse en phase : L'argument du dénominateur de la fonction de transfert $\underline{H} = \frac{1}{1 + jQ\left(x - \frac{1}{x}\right)}$ est donné par $\phi = \arctan(Q\left(x - \frac{1}{x}\right))$ car son cosinus est positif. Donc le déphasage est $\varphi = -\phi$, avec $-\frac{\pi}{2} < \varphi < \frac{\pi}{2}$ ([[#^figure15|fig 15]]). Nous aurions pu aussi remarquer que la réponse en phase d'un passe-bande se déduit de celle d'un passe-bas d'ordre deux par une translation de $\frac{\pi}{2}$ le long de l'axe des déphasages ([[#^figure13|fig. 13b]]).

> [!note] Filtre passe-bande d'ordre deux : Généralisation
> La fonction de transfert d'un filtre passe-bande d'ordre deux est de la forme : $\displaystyle\underline{H}(j\omega) = \frac{A_0\frac{j\omega}{Q\omega_0}}{1 - \frac{\omega^{2}}{\omega_{0}^{2}} + \frac{j}{Q}\frac{\omega}{\omega_0}} = \frac{A_0}{1 + jQ\left(\frac{\omega}{\omega_0} - \frac{\omega_0}{\omega}\right)} = A_0\frac{1}{1 + jQ\left(x - \frac{1}{x}\right)}$.
> Son diagramme de Bode se caractérise par :
> - une asymptote basse fréquence de pente 20 dB/décade ;
> - une asymptote haute fréquence de pente -20 dB/décade ;
> - une intersection pour $\omega = \omega_0$ au point d'ordonnée : $G = 20\log A_0 - 20\log Q$ ;
> - un gain maximal, égal à $20\log A_0$ obtenu pour $\omega = \omega_0$ ;
> - un déphasage nul pour $\omega = \omega_0$ ;
> - un pic de résonance de largeur (mesurée 3 dB au-dessous du maximum) $\Delta\omega =\frac{\omega_0}{Q}$. Cette largeur est encore appelée bande passante à –3 dB.

> [!note] Comportements intégrateur et dérivateur
> Comportement intégrateur : Pour les pulsations grandes devant $\omega_0$, la fonction de transfert peut se mettre sous la forme approchée : $\underline{H}(j\omega) \approx \frac{A_0\omega_0}{Q}\frac{1}{j\omega}$. Nous retrouvons la fonction de transfert d'un intégrateur. En régime sinusoïdal forcé et si $\omega \gg \omega_0$, la tension de sortie $u_2(t)$ est pratiquement proportionnelle à la primitive de valeur moyenne nulle de la tension d'entrée $u_1(t)$.
> <mark style="color: red">Lorsque la courbe de réponse en gain se confond avec son asymptote de pente -20 dB/décade, le filtre passe-bande d'ordre deux a un comportement intégrateur.</mark>
> Le filtre est intégrateur pour tout signal périodique de fréquence grande devant la fréquence caractéristique $f_0$. En effet, s'il est intégrateur pour le fondamental de fréquence $f_0$, il l'est a fortiori pour tous les harmoniques de fréquences $nf_0$.
> 
> Comportement dérivateur :
> - Signal d'entrée sinusoïdal : Pour les pulsations faibles devant $\omega_0$, la fonction de transfert peut se mettre sous la forme approchée : $\underline{H}(j\omega) \approx \frac{A_0}{Q\omega_0}(j\omega)$. Nous retrouvons la fonction de transfert d'un dérivateur. En régime sinusoïdal forcé et si $\omega \ll \omega_0$, la tension de sortie $u_2(t)$ est pratiquement proportionnelle à la dérivée de la tension d'entrée $u_1(t)$.
> - Signal d'entrée périodique quelconque : Si le signal d'entrée est périodique mais non harmonique, le filtre n'a pas nécessairement un effet dérivateur. En effet, il existe des harmoniques de rang élevé qui ne vérifient pas la condition $f \ll f_0$. En particulier, si la résonance est aiguë $(Q \gg 1)$, un harmonique de fréquence voisine de $f_0$ pourra être fortement amplifié. La [[#^figure16|figure 16]] donne les réponses d'un filtre passe-haut à un signal d'entrée triangulaire de fréquence $\frac{f_0}{20}$ pour $Q = 0,5$ et pour $Q = 10$.
> 
> <mark style="color: red">Lorsque la courbe de réponse en gain se confond avec son asymptote de pente +20 dB/décade et si le facteur de qualité Q est suffisamment faible, le filtre passe-bande d'ordre deux a un comportement dérivateur.</mark>

> [!note] Application à la réalisation d'un oscillateur quasisinusoïdal
> - Schéma de l'oscillateur : Considérons le montage représenté sur la [[#^figure17|figure 17]]. Remarquons qu'il n'y figure pas de source et que nous étudions donc son régime libre.
> Nous pouvons identifier deux blocs :
> 	- un amplificateur non inverseur qui impose : $v_1 = Kv_2$ avec $K = \frac{R_1 + R_2}{R_1}$ ;
> 	- un filtre passif du second ordre, nommé « pont de Wien » ([[#^figure18|fig. 18]]). Le courant $i_2$ étant nul, nous pouvons utiliser la relation du diviseur de tension pour calculer la fonction de transfert : $\underline{H}(j\omega)  = \frac{\underline{v}_2}{\underline{v}_1} = \frac{\left(jC\omega + \frac{1}{R}\right)^{-1}}{\left(jC\omega + \frac{1}{R}\right)^{-1} + R + \frac{1}{jC\omega}} = \frac{j\frac{\omega}{\omega_0}}{1 - \frac{\omega^{2}}{\omega_{0}^{2}} + 3j\frac{\omega}{\omega_0}}$ avec $\omega_0 = \frac{1}{RC}$. Il s'agit d'un passe-bande d'ordre deux peu sélectif avec $Q = \frac{1}{3}$ et $A_0 = \frac{1}{3}$.
> - Équation différentielle : La fonction de transfert permet en principe de remonter à l'équation différentielle à condition de l'expliciter sous la forme de polynômes en $(j\omega)$ : $\dfrac{d^{2}v_2}{dt^{2}} + 3\omega_0\dfrac{dv_2}{dt} + \omega_{0}^{2}v_2 = \omega_0\dfrac{dv_1}{dt}$. Cette équation pourrait être retrouvée par un calcul direct utilisant les dérivées temporelles des tensions. Comme $v_1 = Kv_3 = Kv_2$ : $\dfrac{d^{2}v_2}{dt^{2}} + (3 - K)\omega_0\dfrac{dv_2}{dt} + \omega_{0}^{2}v_2 = 0$. Ceci n'est bien entendu applicable que si, aux fréquences auxquelles sera utilisé le montage, la fonction de transfert du montage amplificateur non inverseur est bien assimilable au facteur multiplicatif K (en pratique, sa bande passante est effectivement beaucoup plus grande que la fréquence à laquelle le montage va osciller).
> - Stabilité du régime libre : ==**La condition nécessaire et suffisante de stabilité du régime libre régi par l'équation d'évolution $a\dfrac{d^{2}s(t)}{dt^{2}} + b\dfrac{ds(t)}{dt} + cs(t) = 0$, où a, b et c sont des constantes réelles, est a, b et c de même signe.**==
> Nous en déduisons que : ==**Pour une équation d'évolution de la forme : $\dfrac{d^{2}s(t)}{dt^{2}} + \frac{\omega_0}{Q}\dfrac{ds(t)}{dt} + \omega_{0}^{2}s(t) = 0$, la stabilité du régime libre est assurée par la condition $Q > 0$.**== La [[#^figure19|figure 19]] illustre cette conclusion.
> - Régimes de fonctionnement du montage oscillateur : Pour le montage, la limite de stabilité correspond à $K = 3$. Discutons le comportement observé au voisinage de cette valeur :
> 	- $K < 3$ ou $R_2 < 2R_1$ : le régime libre est stable car $v_2(t)$ tend vers 0. En l'absence de source, la tension $v_2$ reste nulle.
> 	- $K > 3$ ou $R_2 > 2R_1$ : le régime libre est instable car $|v_2(t)|$ tend vers l'infini. Les petites perturbations (les défauts de l'amplificateur, par exemple) sont amplifiées jusqu'à la saturation de l'amplificateur opérationnel.
> 	- $K = 3$ ou $R_2 = 2R_1$ : dans ce cas limite, inaccessible rigoureusement, $v_2(t)$ est une fonction sinusoïdale d'amplitude constante. En fait, le régime libre ne « démarre » spontanément que pour $K$ légèrement supérieur à 3, et $v_2(t)$ se stabilise comme une fonction presque sinusoïdale de pulsation $\omega_0$, du fait d'une limitation de l'amplitude par les non-linéarités du montage (saturation de la sortie de l'A.O.), ce qui engendre des harmoniques (le signal est quasi sinusoïdal).
> 	La réalisation expérimentale doit tenir compte des limitations de l'amplificateur opérationnel, notamment sa vitesse de balayage. Il ne faut donc pas que $\omega_0$ soit trop grande.

> [!note] Filtres sélectifs
> On prend le montage de la [[#^figure20|figure 20]].
> Soit $A$ le nœud commun aux deux résistances $R$ et à la capacité $C$.
> - Nous reconnaissons un amplificateur non inverseur qui impose : $\underline{v}_s = k\underline{v}_+$ ;
> - Le diviseur de tension nous donne la relation : $\underline{v}_+ = \underline{v}_A\frac{\left(\frac{1}{R} + jC\omega\right)^{-1}}{\frac{1}{jC\omega} + \left(\frac{1}{R} + jC\omega\right)^{-1}}$ ;
> - De la loi des nœuds appliquée en $A$ il découle : $\underline{v}_A = \frac{\underline{v}_e + \underline{v}_s + jRC\omega\underline{v}_+}{2 + jRC\omega}$.
> 
> Nous éliminons $\underline{v}_A$ et $\underline{v}_+$ dans la dernière équation et nous obtenons la fonction de transfert du filtre : $\underline{H}(j\omega) = \frac{A_0\frac{j\omega}{Q\omega_0}}{1 - \frac{\omega^{2}}{\omega_{0}^{2}} + \frac{j}{Q}\frac{\omega}{\omega_0}}$ avec $A_0 = \frac{k}{5 - k}$, $Q = \frac{\sqrt{2}}{5 - k}$ et $\omega_0 = \frac{\sqrt{2}}{RC}$.
> De la fonction de transfert nous déduisons l'équation différentielle liant $v_s(t)$ à $v_e(t)$ : $\dfrac{d^{2}v_2}{dt^{2}} + \frac{\omega_0}{Q}\dfrac{dv_2}{dt} + \omega_{0}^{2}v_2 = \frac{A_0\omega_0}{Q}\dfrac{dv_e}{dt}$.
> Le régime libre est stable si ses solutions convergent vers 0, c'est-à-dire si $Q$ est positif, soit $k < 5$.
> La sélectivité est maximale à la limite de l'instabilité. Cette considération est importante sur le plan expériemental : il faudra ajuster la valeur de $k$ de façon à conserver un fonctionnement stable tout en ayant une grande sélectivité.
> La condition de stabilité $k < 5$ est sans rapport avec la condition de stabilité liée à la permutation des entrées de l'amplificateur opérationnel.
# Définitions
==**Sélectivité d'un filtre passe-bande**== :
Un filtre passe-bande est sélectif s'il ne transmet effectivement que des tensions sinusoïdales de fréquence voisine de sa fréquence de résonance.
==**La sélectivité d'un filtre est d'autant plus forte que la bande passante est étroite, ou que le facteur de qualité $Q$ est élevé.**==

> [!note] Filtres sélectifs : Exemple de réalisation
> Le filtre sélectif étudié est le filtre passe-bande de Sallen et Key ([[#^figure20|fig. 20]]) pour lequel nous supposerons que l'amplificateur opérationnel utilisé est idéal.
> Bien qu'il y ait deux boucles de rétroaction, l'une sur l'entrée inverseuse (rétroaction stabilisante) et l'autre sur l'entrée non inverseuse (rétroaction déstabilisante), nous admettrons qu'il existe un régime linéaire dont nous déterminerons ultérieurement les conditions d'existence.
> En basse fréquence, les condensateurs sont équivalents à des interrupteurs ouverts. Le comportement du filtre correspond à celui du montage représenté dans la [[#^figure21|figure 21]]. Nous remarquons que $v_+ = 0$, donc, en régime linéaire, $v_-$ et $v_s$ sont nuls. Le montage ne laisse pas passer les basses fréquences.
> En haute fréquence, les condensateurs sont équivalents à des interrupteurs fermés. Le circuit équivalent au filtre est donné par la [[#^figure22|figure 22]]. L'entrée non inverseuse est à la masse : $v_+ = 0$, donc, en régime linéaire, $v_- = v_s = 0$. Le montage ne laisse pas passer les hautes fréquences.
> En conclusion, le comportement du circuit étudié est bien celui d'un filtre passe-bande.

> [!note] Filtres sélectifs : Réalisation expérimentale
> Le montage expérimental est dans la [[#^figure23|figure 23]].
> Les valeurs des résistances sont choisies dans le domaine $[1 k\Omega ; 1 M\Omega]$ et la valeur de $C$ est fixée de façon à avoir une fréquence de résonance $(f_0 = 225 Hz)$ suffisamment basse pour que les défauts de triangularisation et de bande passante limitée de l'amplificateur opérationnel soient négligeables.
> La résistance ajustable de 100 kΩ permet de modifier la valeur du facteur $k$.
> - Mesures : Mesurons l'amplitude de $v_s$ et $v_e$ et leur déphasage $\varphi$ en fonction de la fréquence pour $r' = 0$ $(k = 1)$, $r' = 10 k\Omega$ $(k = 2)$, $r' = 20 k\Omega$ $(k = 3)$, $r' = 30 k\Omega$ $(k = 4)$, $r' = 38 k\Omega$ $(k = 4,8)$.
> L'amplitude de $v_e$ sera choisie de façon à avoir un fonctionnement linéaire de l'A.O. (ni saturation en tension, ni triangularisation). Une amplitude de $v_e$ de 1 V ou 2 V convient, saut pour $k = 4,8$, car les amplifications théoriques $A_0$ à la résonance sont respectivement 0,2 ; 0,67 ; 1,5 ; 4 et 24.
> Nous effectuerons plusieurs mesures au voisinage de la fréquence de $f_0 = 225 Hz$ pour évaluer la bande passante $\Delta f$ du montage.
> Les résultats expérimentaux correspondent aux résultats théoriques, compte tenu des écarts entre les valeurs réelles et nominales des composants ([[#^figure24|fig. 24]]). Le montage est très sensible à la modification de la valeur d'un composant au voisinage de la résonance.
> - Réponse du filtre à des signaux non sinusoïdaux : Un filtre sélectif permet l'analyse spectrale d'un signal non sinusoïdal. En effet, la réponse d'un tel filtre n'est notable que si la fréquence $f_n$ d'un harmonique est égale ou, tout au moins, voisine de sa fréquence $f_0$ de résonance.
> Plus le facteur de qualité $Q$ du filtre est élevé, plus sa bande passante $\Delta f$ est étroite et plus la détermination de la fréquence $f$ est précise ([[#^figure25|fig. 25]]).
> En outre, lorsque $f_n = f_0$, l'amplitude de la réponse du filtre $V_{s_n} = A_0 V_{e_n}$ en est proportionnelle à l'amplitude de l'harmonique du signal d'entrée.
> Ainsi, si nous réalisons notre filtre sélectif avec une valeur de $Q$ élevée, nous pourrons effectuer l'analyse harmonique des signaux d'entrée.
> En effet, ajustons $r'$, de façon à obtenir un montage stable et de grand facteur de qualité. Choisissons un signal d'entrée de type créneaux symétriques d'amplitude 0,1 V et diminuons sa fréquence $f$ à partir de 250 Hz. Observons la forme du signal de sortie $v_s$ et mesurons sa valeur efficace $V_s$. Pour $f_1 = 225 Hz$, $f_3 = 75 Hz$, $f_5 = 45 Hz$, $f_7 = 32 Hz$ et $f_9 = 25 Hz$, la tension de sortie $v_s$ prend des valeurs importantes et est quasiment sinusoïdale, de fréquence $f_0 = 225 Hz$. Si sa valeur efficace est $V_{s_1} = 10 V$ à $f_1 = 225 Hz$, elle n'est plus que de $V_{s_3} = 3,3 V$ à $f_3 = 75 Hz$, $V_{s_5} = 2 V$ à $f_5 = 45 Hz$, $V_{s_7} = 1,4 V$ à $f_7 = 32 Hz$ et $V_{s_9} = 1,1 V$ à $f_9 = 25 Hz$ ([[#^figure26|fig. 26]]).
> Nous vérifions ainsi qu'un signal de type créneaux symétriques est composé uniquement d'harmoniques impairs $f_1$, $f_3 = \frac{f_1}{3}$, $f_5 = \frac{f_1}{5}$, $f_7 = \frac{f_1}{7}$, $f_9 = \frac{f_1}{9}$, d'amplitudes inversement proportionnelles à leur rang.
> La comparaison entre les figures [[#^figure26|26]] et [[#^figure27|27]] ($Q = 20$ et $Q = 7$), d'une part, et la [[#^figure28|figure 28]], d'autre part, nous montre la nécessité d'un facteur de qualité important pour l'étude des harmoniques d'un signal périodique.
> 
> ==**Un filtre sélectif permet d'extraire d'un signal les composantes sinusoïdales de fréquences voisines de sa fréquence de résonance $f_0$.**==
# Diagrammes
Deux filtres d'ordre un en cascade
![[electronique1/attachments-electronique1/figure214.png]]^figure1

Filtre (R, L, C) passe-bas d'ordre deux
![[electronique1/attachments-electronique1/figure216.png]]^figure3

Filtre (R, L, C) passe-haut d'ordre deux
![[electronique1/attachments-electronique1/figure222.png]]^figure9

Filtre (R, L, C) passe-bande d'ordre deux
![[electronique1/attachments-electronique1/figure225.png]]^figure12

Oscillateur à pont de Wien
![[electronique1/attachments-electronique1/figure230.png]]^figure17

Pont de Wien
![[electronique1/attachments-electronique1/figure231.png]]^figure18

Filtre passe-bande de Sallen et Key
![[figure233.png]]^figure20

Schéma équivalent au filtre passe-bande de Sallen et Key en basse fréquence
![[figure234.png]]^figure21

Schéma équivalent au filtre passe-bande de Sallen et Key en haute fréquence
![[figure235.png]]^figure22

Montage expérimental. $r' = (k - 1)r$ et $r = 10 k\Omega$
![[figure237.png]]^figure23
# Graphiques
Tracé asymptotique de la courbe de gain
![[electronique1/attachments-electronique1/figure215.png]]^figure2

Diagramme asymptotique de la réponse en gain d'un filtre passe-bas d'ordre deux : pente -40 dB/décade
![[electronique1/attachments-electronique1/figure217.png]]^figure4

Courbes de réponse en gain d'un filtre passe-bas d'ordre deux $\left(Q = 5, 1, \frac{\sqrt{2}}{2}, \frac{1}{2}\right)$
![[electronique1/attachments-electronique1/figure218.png]]^figure5

Courbes de réponse en phase d'un filtre passe-bas d'ordre deux $\left(Q = 5, 1, \frac{\sqrt{2}}{2}, \frac{1}{2}\right)$
![[electronique1/attachments-electronique1/figure219.png]]^figure6

Diagramme asymptotique de la réponse en phase d'un passe-bas d'ordre deux
![[electronique1/attachments-electronique1/figure220.png]]^figure7

La rotation de phase est d'autant plus rapide que $Q$ est grand (ou $\sigma$ petit)
![[electronique1/attachments-electronique1/figure221.png]]^figure8

Diagrammes asymptotiques de gain a. et de phase b. d'un passe-haut d'ordre deux
![[electronique1/attachments-electronique1/figure223.png]]^figure10

Diagramme de Bode d'un passe-haut d'ordre deux
![[electronique1/attachments-electronique1/figure224.png]]^figure11

Diagrammes asymptotiques de gain a. et de phase b. d'un passe-bande d'ordre deux
![[electronique1/attachments-electronique1/figure226.png]]^figure13

Courbe de réponse en gain d'un passe-bande d'ordre deux
![[electronique1/attachments-electronique1/figure227.png]]^figure14

Courbe de réponse en phase d'un passe-bande d'ordre deux
![[electronique1/attachments-electronique1/figure228.png]]^figure15

Réponse d'un filtre passe-bande du deuxième ordre à un signal triangulaire de fréquence $\frac{f_0}{20}$ d'amplitude 1 V : a. pour un facteur de qualité de 0,5 ; b. pour un facteur de qualité de 10
![[electronique1/attachments-electronique1/figure229.png]]^figure16

Régimes libres décrits par $s''(t) + \frac{\omega_0}{Q}s'(t) + \omega_{0}^{2}s(t) = 0$
![[figure232.png]]^figure19

Simulation de l'influence du non appariement des condensateurs (le rapport des capacités $\frac{C_4}{C_2} = 1 + \epsilon$ varie de 0,90 à 1.10) pour $k = 4,8$
![[figure236.png]]^figure24

Un filtre très sélectif permet d'extraire la composante sinusoïdale de fréquence égale à sa fréquence $f_0$ de résonance contrairement au filtre peu sélectif
![[figure238.png]]^figure25

Valeur efficace du signal de sortie en fonction de la fréquence $(Q = 20)$. Le signal de sortie est approximativement sinusoïdal à chaque maximum
![[figure239.png]]^figure26

Valeur efficace du signal de sortie en fonction de la fréquence $(Q = 7)$. Le signal de sortie est très approximativement sinusoïdal à chaque maximum. Les maxima sont moins marqués que pour $Q = 20$ et ne sont plus séparés à basse fréquence
![[figure240.png]]^figure27

Signal de sortie pour un signal d'entrée 45 Hz. Le signal est encore proche d'une sinusoïde pour $Q = 20$, mais pas pour $Q = 7$
![[figure241.png]]^figure28
# Expériences
> [!warning]
> Voici des exemples de travaux pratiques qui abordent le sujet de ce chapitre : le [lien 1](https://ressources.unisciel.fr/sillages/physique/tp_electrocinetique_1a_pcsi/res/TP16.PDF), le [lien 2](https://fr.scribd.com/document/800805810/TP1-Filtre-passe-bas-2ordre), le [lien 3](https://ressources.unisciel.fr/sillages/physique/tp_electrocinetique_1a_pcsi/res/TP10.PDF), le [lien 4](https://www.f-legrand.fr/scidoc/srcdoc/sciphys/tpelectro/passebande2/passebande2-pdf.pdf), le [lien 5](http://mp2carnot.free.fr/TP/TP_03_filtre.pdf), le [lien 6](http://remy.duperray.free.fr/downloads-7/files/TP-Filtre-RLC-ordre2.pdf), le [lien 7](http://psi2.nantes.free.fr/TP/ENONCES-ET-CORRIGES-TP/TP-ELECTRONIQUE/ENONCE-TP-ELECTRONIQUE/TP-3-ENONCE.pdf), le [lien 8](https://cahier-de-prepa.fr/mp-charlemagne/download?id=1273), le [lien 9](https://cahier-de-prepa.fr/pc-lavoisier/download?id=1702), le [lien 10](https://www.alloschool.com/assets/documents/course-248/tp-e4-filtres-du-second-ordre.pdf), le [lien 11](https://pcjoffre.fr/Data/tp/TP20_Wien.pdf), le [lien 12](http://talbourdel.yves.free.fr/resources/TP/TP4oscillateurpontdeWien2023.pdf), le [lien 13](http://mpetoilemartiniere.free.fr/wp-content/uploads/tp-oscillateur.pdf), le [lien 14](https://fr.scribd.com/document/732118159/Tp03-Oscillateur-a-Pont-de-Wien-Berrouachedi-n), le [lien 15](http://colinherve.free.fr/Physique_en_PC/TP_files/Oscillateur%20de%20Wien.pdf), le [lien 16](https://fr.scribd.com/document/923751845/TP-2-Oscillateur-A-pont-de-Wien-Ver-2022), le [lien 17](https://ressources.unisciel.fr/sillages/physique/electronique_2a_pc/res/osciquasisinus.pdf), le [lien 18](http://prfphy1.fr/lycee/ATS/TP/TP18Transmissiondinformation_creation_oscillateur_pont_Wien.pdf), le [lien 19](http://mp2carnot.free.fr/TP/TP_08_ALI.pdf), le [lien 20](http://thierryperisse.free.fr/documents/electronique-analogique/cesi/OSCILLATEURS_TP.pdf), le [lien 21](http://leroy.pe.free.fr/psi_new/tp/tp_oscillateurs.pdf), le [lien 22](http://venturi.marc.free.fr/TP/TP_Fascicule_premiere_periode.pdf), le [lien 23](https://fr.scribd.com/document/853086542/TP-elec-4-oscillateurs-quasi-sinusoidaux), le [lien 24](http://psi2.nantes.free.fr/TP/ENONCES-ET-CORRIGES-TP/TP-ELECTRONIQUE/ENONCE-TP-ELECTRONIQUE/TP-6-ENONCE.pdf), le [lien 25](http://psi2.nantes.free.fr/TP/ENONCES-ET-CORRIGES-TP/TP-ELECTRONIQUE/ENONCE-TP-ELECTRONIQUE/TP-6-ENONCE.pdf), le [lien 26](https://www.technologuepro.com/cours-electronique-analogique-2/tp4-les-oscillateurs-sinusoidaux.pdf), le [lien 27](https://www.alloschool.com/assets/documents/course-248/tp-e9-oscillateur-quasi-sinusoidal-a-resistance-negative.pdf), le [lien 28](https://www.etienne-thibierge.fr/tp_2024/tp06_osc-wien.pdf), le [lien 29](http://maths.sup.free.fr/modules/Page/html/TP/16_TPE10_Oscillateurquasisinusoidal.pdf), le [lien 30](https://fr.scribd.com/document/833272236/TP2-Oscillateurs-quasi-sinusuidaux), le [lien 31](https://fr.scribd.com/document/720721286/TP-Wien-1), le [lien 32](https://ressources.unisciel.fr/sillages/physique/electronique_1a_pcsi/res/TP29.PDF), le [lien 33](https://sites.google.com/view/jphoremans/tp), le [lien 34](https://fr.scribd.com/document/802128503/TP-Filtres-passifs).
# Autres notes
> [!warning]
> Une faute courante est d'écrire $\varphi = -\phi = -\arctan\left(\frac{2\sigma x}{1 - x^{2}}\right)$, où $\phi$ est présumé représenter l'argument du dénominateur de $\underline{H}(jx)$. En effet, la tangente d'un angle ne le détermine qu'à $\pi$ près et il est nécessaire d'examiner le signe de son cosinus ou de son sinus pour le définir complètement. Ici, $\sin(\phi)$ est toujours positif et $\cos(\phi)$ est du signe de $(1 - x^{2})$, donc $\varphi = -\arctan\left(\frac{2\sigma x}{1 - x^{2}}\right)$ si $(1 - x^{2}) > 0$, $\varphi = \frac{\pi}{2}$ si $(1 - x^{2}) = 0$ et $\varphi = \pi + \arctan\left(\frac{2\sigma x}{1 - x^{2}}\right)$ si $(1 - x^{2}) < 0$.
^info1

> [!warning] Forme canonique
> La forme canonique d'une fonction de transfert est celle qui fait apparaître les paramètres $A_0$, $\omega_0$ et $Q$.
