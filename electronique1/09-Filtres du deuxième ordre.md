---
titre: "[[09-Filtres du deuxième ordre]]"
tags:
aliases:
crée: 16-11-2025, 13:38
---
# Formules
> [!note] Exemple de filtre d'ordre deux
> Étudions le circuit représenté sur la [[#^figure1|figure 1]].
> Nous reconnaissons un filtre passe-bas et un filtre passe-haut d’ordre un séparés par un suiveur.
> Le suiveur permet d’assurer l’égalité $u_2 = u_3$ avec un courant $i_2$ nul.
> Comme le courant $i_2$ est nul : $\underline{H}_1(j\omega) = \frac{\underline{u}_{2m}}{\underline{u}_{1m}} = \frac{1}{1 + j\frac{\omega}{\omega_1}}$ avec $\omega_1 = \frac{1}{R_1C_1}$.
> Comme la sortie est ouverte $(i_4 = 0)$ : $\underline{H}_2(j\omega) = \frac{\underline{u}_{4m}}{\underline{u}_{3m}} = \frac{j\frac{\omega}{\omega_2}}{1 + j\frac{\omega}{\omega_2}}$ avec $\omega_2 = \frac{1}{R_2C_2}$.
> Nous en déduisons la fonction de transfert $\underline{H}(j\omega) = \frac{\underline{u}_{4m}}{\underline{u}_{1m}}$ du système complet : $\underline{H}(j\omega) = \underline{H}_1(j\omega)\underline{H}_2(j\omega) = \frac{j\frac{\omega}{\omega_2}}{\left(1 + j\frac{\omega}{\omega_1}\right)\left(1 + j\frac{\omega}{\omega_2}\right)}$. Nous obtenons une fonction de transfert du second ordre. Le tracé asymptotique de la courbe de gain se déduit de ceux de chaque filtre d’ordre un ([[#^figure2|fig. 2]]).
> Nous sommes donc en présence d’un filtre qui élimine à la fois les hautes et les basses fréquences. Il s’agit d’un type de filtre, appelé passe-bande.
> Nous pourrons rencontrer des réalisations variées de filtre d’ordre deux. L’association de deux filtres d’ordre un semble naturelle, mais ne permet pas de réaliser tous les transferts d’ordre deux. En utilisant un circuit de type (R, L, C), dont le facteur de qualité est ajustable, nous accéderons à une présentation plus générale de ces filtres.
> Remarque : le circuit (R, L, C) est facile à aborder mais assez peu utilisé en pratique. Dans les circuits électriques, on préfère généralement employer des résistances et capacités, composants peu encombrants et bon marché, plutôt que des bobines, qui peuvent éventuellement être simulées.

> [!note] Filtre passe-bas d'ordre deux
> La réponse en charge du circuit (R, L, C) série à une excitation sinusoïdale en tension a été étudiée au [[06-Régime sinusoïdal forcé|chapitre 6]]. Reprenons celle-ci en utilisant les impédances complexes des composants, et interprétons-la en terme de filtrage.
> - Exemple de fonction de transfert passe-bas d’ordre deux : Le filtre étudié est représenté sur la [[#^figure3|figure 3]]. Fonctionnant à vide $(\underline{i}_2(t) = 0)$, il réalise un diviseur de tension : $\underline{H} = \frac{\underline{u}_{2m}}{\underline{u}_{1m}} = \frac{\frac{1}{jC\omega}}{R + jL\omega + \frac{1}{jC\omega}}$. Notons par $\omega_0 = \frac{1}{\sqrt{LC}}$ la pulsation propre, par $x = \frac{\omega}{\omega_0}$ la pulsation réduite et par $2\sigma = RC\omega_0 = \frac{R}{L\omega_0} = \frac{1}{Q}$ l'inverse du facteur de qualité du circuit (R, L, C) série. Avec ces notations, la fonction de transfert s'écrit : $\underline{H}(jx) = \frac{1}{1 + 2\sigma(jx) + (jx)^{2}} = \frac{1}{1 - x^{2} + j\frac{x}{Q}}$.
> - Courbe de réponse en gain : Le gain du filtre est : $G(x) = -10\log[(1 - x^{2})^{2} + 4\sigma^{2}x^{2}]$.
> 	- Asymptote basse fréquence : En très basse fréquence, l’inductance $L$ se comporte comme un interrupteur fermé et la capacité $C$ comme un interrupteur ouvert. Le circuit étant ouvert en sortie, aucun courant ne traverse la résistance $R$, donc $\underline{u}_{1m} = \underline{u}_{2m}$ et $G = 0$. La courbe de réponse en gain admet, en basse fréquence, une asymptote horizontale à $G = 0$ dB.
> 	- Asymptote haute fréquence : En haute fréquence, la capacité se comporte comme un interrupteur fermé, donc $\underline{u}_{2m} = 0$, alors $\underline{u}_{1m} \neq 0$. Donc $G(x) \rightarrow -\infty$. Lorsque $x \gg 1$, la valeur asymptotique du gain est $G = -10\log(x^{4}) = -40X$. La courbe de réponse en gain admet, en haute fréquence, une asymptote passant par l’origine de pente -40 dB/décade ([[#^figure4|fig. 4]]).
> 	- Diagramme asymptotique :
> 	Le diagramme asymptotique est la réunion des deux asymptotes basses fréquences et hautes fréquences limitées à leur point de concours. Évaluons la qualité de cette représentation asymptotique en calculant, pour $x = 1$, l’écart entre le graphe de la réponse en gain et sa représentation asymptotique : $\Delta G = G(1) - G_A = -20\log(2\sigma) = 20\log(Q)$. Cet écart peut être considérable si le facteur d’amortissement $2\sigma$ est faible (ou le facteur de qualité $Q$ élevé) ([[#^figure5|fig. 5]]). Le diagramme asymptotique est généralement insuffisant pour décrire la réponse en gain d’un filtre du second ordre. Nous sommes conduits à préciser les variations de la courbe de réponse en gain.
> 	Posons : $y = (1 - x^{2})^{2} + 4\sigma^{2}x^{2}$. Cette fonction bicarrée passe par un maximum pour : $x_s = \sqrt{1 - 2\sigma^{2}}$, lorsque $\sigma < \frac{\sqrt{2}}{2} \Leftrightarrow Q > \frac{\sqrt{2}}{2} \approx 0,707$.
> 	Pour la fonction de filtrage, l’existence d’un extremum, surtout accentué, est un défaut. Le gain d’un filtre ne doit avoir que de faibles variations en bande passante. En conséquence, un filtre passe-bas d’ordre deux est réalisé généralement avec des valeurs du facteur de qualité $Q$ de l’ordre de $\frac{\sqrt{2}}{2}$.
> - [[#^info1|Courbe de réponse en phase]] : Le déphasage de $\underline{u}_{2m}$ par rapport à $\underline{u}_{1m}$ est $\varphi(x) = \arg[\underline{H}(jx)]$, dont les valeurs asymptotiques sont $\varphi = 0$ en basse fréquence et $\varphi = -\pi$ en haute fréquence. Par ailleurs, quelle que soit la valeur de $\sigma$, la courbe de réponse en phase passe par le point $A\left(0 ; -\frac{\pi}{2}\right)$ ([[#^figure6|fig. 6]]).
> Le diagramme asymptotique de la réponse en phase constitué des deux asymptotes B.F. $(\phi = 0)$ et H.F. $(\phi = -\pi)$, ne décrit pas la rotation de phase au voisinage de $X = 0$. Il peut être complété comme indiqué en [[#^figure7|figure 7]] par le segment $A_1AA_2$. La rotation de phase s’effectue pour l’essentiel au voisinage de $X = 0$ et elle est d’autant plus rapide que $\sigma$ est petit (ou $Q$ élevé) ([[#^figure8|fig. 8]]).

> [!note] Filtre passe-bas d'ordre deux : Généralisation
> La fonction de transfert d’un filtre passe-bas d’ordre deux peut se mettre sous la forme : $\displaystyle\underline{H}(j\omega) = \frac{A_0}{1 - \frac{\omega^{2}}{\omega_{0}^{2}} + \frac{j}{Q}\frac{\omega}{\omega_0}} = \frac{A_0}{1 - x^{2} + j\frac{x}{Q}}$.
> Son diagramme de Bode est caractérisé par :
> -  une asymptote basse fréquence d’ordonnée : $G_{(dB)} = 20\log A_0$ ;
> - une asymptote haute fréquence de pente -40 dB/décade ;
> - une résonance pour $\omega < \omega_0$ si $Q > \frac{1}{\sqrt{2}}$.
> - $\underline{H}(j\omega_0) = QA_0$.
> 
> Remarques :
> - Si le facteur $A_0$ n’est pas réel positif, cela revient simplement à ajouter un déphasage constant au signal de sortie correspondant à ces écritures ;
> - On notera qu’il faut deux paramètres ($A_0$ et $\omega_0$) pour définir complètement un passe-bas d’ordre un et qu’il en faut trois ($A_0$, $Q$ et $\omega_0$) pour définir un passe-bas d’ordre deux.
> 
> Comportement à haute fréquence : À haute fréquence, c’est-à-dire lorsque la courbe de réponse en gain se confond avec l’asymptote haute fréquence, la partie principale du dénominateur est $- \frac{\omega^{2}}{\omega_{0}^{2}}$ et la fonction de transfert est équivalente à : $\underline{H}(j\omega) \approx A_0\omega_{0}^{2}\left(\frac{1}{j\omega}\right)^{2}$. Or, en notation complexe, multiplier par $\left(\frac{1}{j\omega}\right)^{2}$ revient à intégrer deux fois.
> <mark style="color: red">Lorsque la courbe de réponse en gain se confond avec l’asymptote haute fréquence, l’effet du filtre est pratiquement équivalent à une double intégration du signal d’entrée.</mark>
> Lorsque l’on affirme qu’un filtre est intégrateur, il est sous-entendu qu’en régime forcé, la tension de sortie $u_2(t)$ est proportionnelle à la primitive de $u_1(t)$ <mark style="color: red">dont la valeur moyenne est nulle</mark>. La tension de sortie est, en effet, égale à la somme de fonctions sinusoïdales de valeur moyenne nulle.

> [!note] Filtre passe-haut d'ordre deux
> - Exemple : Comme pour l’ordre un, le filtre passe-haut d’ordre deux est complémentaire du filtre passe-bas du même ordre. Le filtre réalisé est représenté sur la [[#^figure9|figure 9]]. Avec le même raisonnement que celui du passe-bas d'ordre 2, on obtient la fonction de transfert suivante : $\underline{H} = \frac{(jx)^{2}}{1 + 2\sigma(jx) + (jx)^{2}}$. La fonction de transfert $\underline{H}$, d’ordre deux, peut être considérée comme le produit de la fonction de transfert d’un double dérivateur $\underline{H}_1 = (jx)^{2}$ par celle d'un passe-bas d'ordre deux : $\underline{H}_2 = \frac{1}{1 + 2\sigma(jx) + (jx)^{2}}$. Il en résulte que son diagramme asymptotique de gain et de phase est la somme des diagrammes asymptotiques correspondant de $\underline{H}_1$ et de $\underline{H}_2$ comme il est indiqué ([[#^figure10|fig. 10]]) et que son diagramme de Bode est la somme des diagrammes de Bode de $\underline{H}_1$ et de $\underline{H}_2$ ([[#^figure11|fig. 11]]).
> L’examen du diagramme asymptotique de gain montre que le filtre étudié est un passe-haut. Par ailleurs, il est possible de démontrer que la courbe de réponse en gain du passe-haut réalisé est symétrique, par rapport à l’axe des gains, de celle du passe-bas de même facteur d’amortissement $2\sigma$.
> - Généralisation : La fonction de transfert d’un filtre passe-haut d’ordre deux peut se mettre sous la forme : $\displaystyle\underline{H}(j\omega) = \frac{-A_0\frac{\omega^{2}}{\omega_{0}^{2}}}{1 - \frac{\omega^{2}}{\omega_{0}^{2}} + \frac{j\omega}{Q\omega_0}} = +A_0\frac{-x^{2}}{1 - x^{2} + j\frac{x}{Q}}$. Son diagramme de Bode, symétrique de celui du filtre passe-haut se caractérise par :
> 	- une asymptote haute fréquence d’ordonnée égale à $20\log A_0$ ;
> 	- une asymptote basse fréquence de pente 40 dB/décade ;
> 	- l’intersection des asymptotes pour $\omega = \omega_0$ ;
> 	- une résonance pour $\omega > \omega_0$ si $Q > \frac{1}{\sqrt{2}}$ ;
> 	- $\underline{H}(j\omega_0) = jQA_0$.
> - Comportement à basse fréquence : À basse fréquence, c’est-à-dire lorsque la courbe de réponse en gain se confond avec l’asymptote basse fréquence la fonction de transfert est équivalente à : $\underline{H}(j\omega) \approx \frac{A_0}{\omega_{0}^{2}}(j\omega)^{2}$. Or, en notation complexe, multiplier par $(j\omega)^{2}$ revient à dériver deux fois.
> <mark style="color: red">Lorsque la courbe de réponse en gain se confond avec l’asymptote basse fréquence, l’effet du filtre est pratiquement équivalent à une double dérivation du signal d’entrée.</mark>
> La dérivation pose en général plus de problèmes que l’intégration. Si le signal d’entrée n’est pas sinusoïdal, il possède des harmoniques dont la fréquence est voisine de la fréquence caractéristique. Si le filtre est résonant $(Q > 1)$, ceux-ci sont amplifiés et la dérivation n’est plus observée.

# Définitions

# Diagrammes
Deux filtres d’ordre un en cascade
![[figure214.png]]^figure1

Filtre (R, L, C) passe-bas d’ordre deux
![[figure216.png]]^figure3

Filtre (R, L, C) passe-haut d’ordre deux
![[figure222.png]]^figure9
# Graphiques
Tracé asymptotique de la courbe de gain
![[figure215.png]]^figure2

Diagramme asymptotique de la réponse en gain d’un filtre passe-bas d’ordre deux : pente -40 dB/décade
![[figure217.png]]^figure4

Courbes de réponse en gain d’un filtre passe-bas d’ordre deux $\left(Q = 5, 1, \frac{\sqrt{2}}{2}, \frac{1}{2}\right)$
![[figure218.png]]^figure5

Courbes de réponse en phase d’un filtre passe-bas d’ordre deux $\left(Q = 5, 1, \frac{\sqrt{2}}{2}, \frac{1}{2}\right)$
![[figure219.png]]^figure6

Diagramme asymptotique de la réponse en phase d’un passe-bas d’ordre deux
![[figure220.png]]^figure7

La rotation de phase est d’autant plus rapide que $Q$ est grand (ou $\sigma$ petit)
![[figure221.png]]^figure8

Diagrammes asymptotiques de gain a. et de phase b. d’un passe-haut d’ordre deux
![[figure223.png]]^figure10

Diagramme de Bode d’un passe-haut d’ordre deux
![[figure224.png]]^figure11
# Expériences

# Autres notes
> [!warning]
> Une faute courante est d'écrire $\varphi = -\phi = -\arctan\left(\frac{2\sigma x}{1 - x^{2}}\right)$, où $\phi$ est présumé représenter l'argument du dénominateur de $\underline{H}(jx)$. En effet, la tangente d'un angle ne le détermine qu'à $\pi$ près et il est nécessaire d'examiner le signe de son cosinus ou de son sinus pour le définir complètement. Ici, $\sin(\phi)$ est toujours positif et $\cos(\phi)$ est du signe de $(1 - x^{2})$, donc $\varphi = -\arctan\left(\frac{2\sigma x}{1 - x^{2}}\right)$ si $(1 - x^{2}) > 0$, $\varphi = \frac{\pi}{2}$ si $(1 - x^{2}) = 0$ et $\varphi = \pi + \arctan\left(\frac{2\sigma x}{1 - x^{2}}\right)$ si $(1 - x^{2}) < 0$.
^info1
