---
titre: "[[04-Un exemple de système électronique. L'amplificateur opérationnel]]"
tags:
aliases:
crée: 26-11-2025, 15:28
---
# Formules
> [!note] Le modèle linéaire de l'amplificateur opérationnel : Modélisation
> Nous n’examinerons ici que le problème de la modélisation des amplificateurs opérationnels en régime linéaire.
> Dans le modèle de l'amplificateur opérationnel réel dit "à bande passante limitée", nous pouvons donner deux représentations de la relation entre $v_s$ et $v_e$ :
> - la première sous la forme d’une équation différentielle : $v_s + \tau\dfrac{dv_s}{dt} = \mu_0\epsilon$ ($\tau$ homogène à un temps et $\mu_0$ sans dimension) ;
> - la seconde sous la forme d'une fonction de transfert : $V_s(p) = \mu(p)\epsilon(p)$ avec $\mu(p) = \frac{1}{1 + \tau p}$ ;
> - ces lois linéaires sont valides tant que $v_s$ reste comprise entre les deux tensions de saturation $V_{sat}^{+}$ et $V_{sat}^{-}$. Dans le cas contraire, l’amplificateur est en régime saturé (non linéaire) avec $v_s = V_{sat}^{+}$ (pour $\epsilon > 0$) ou $v_s = V_{sat}^{-}$ (pour $\epsilon < 0$).
> 
> La [[#^figure4|figure 4]] représente la caractéristique de transfert statique (c’est-à-dire en régime indépendant du temps).
> Interprétons l'équation différentielle :
> En régime permanent, l’amplificateur opérationnel est un amplificateur de différence $v_s = \mu_0(v_+ - v_-)$, d’où son nom d'amplificateur différentiel intégré. Le coefficient $\mu_0$ noté aussi $A_d$, est son amplification différentielle statique et $\tau$ correspond au temps de relaxation de l'amplificateur opérationnel (temps caractéristique de la solution de l'équation différentielle sans second membre).
> Interprétons la fonction de transfert :
> Le diagramme de Bode ([[#^figure5|fig. 5]]) pour les gains positifs correspond à celui d’un filtre passe-bas du premier ordre de gain statique $G_0 = 20\log\mu_0$ dont la fréquence de coupure à -3 dB est $f_H = \frac{1}{2\pi\tau}$.
> La fréquence de gain nul est la fréquence $f_0 \approx \frac{\mu_0}{2\pi\tau}$, car $\mu_0 \gg 1$.
> Au-delà de $f_0$, l’affaiblissement n’est plus de -20 dB par décade et le déphasage n’est plus de $-\frac{\pi}{2}$ : le modèle « à bande passante limitée » n’est pas valable au-delà de $f_0$ : une modélisation par une fonction de transfert d’ordre supérieur serait nécessaire.
> La fréquence $f_H$ est trés faible (de l'ordre de 10 Hz). Pour des signaux de fréquence supérieure à 100 Hz, la fonction de transfert peut être approchée par sa valeur asymptotique $\mu(p) \approx \frac{\mu_0}{\tau p}$. La grandeur la plus importante pour l’utilisateur est donc $\frac{\mu_0}{\tau}$ ou $f_0$. Cette dernière fréquence est celle donnée par le constructeur sous le nom de « Unity Gain Bandwith ».
# Définitions
==**Système actif et système passif**== :
Un système actif est un système dont le fonctionnement nécessite une source d’énergie. Par opposition, un système passif ne reçoit de l'énergie que par l'intermédiaire de son signal d’entrée ou de sortie.

==**Limitation des systèmes passifs**== :
Les performances des systèmes passifs sont fondamentalement imitées par les lois de la thermodynamique. Pour simplifier, nous raisonnons sur un quadripôle électrique dont la charge est passive et qui est alimenté en entrée par une source représentée par un générateur de Thévenin ([[#^figure1|fig. 1]]).
- Limitation du gain en puissance :
L'énergie cédée à la charge ne peut provenir que de la source. Une partie de l'énergie fournie étant dissipée dans le système, le gain en puissance moyenne est inférieur à 1 : $\mathcal{P}_{sortie} < \mathcal{P}_{entrée}$.
Remarque : Cette inégalité concerne les puissances moyennes (ou puissances actives). Si le système contient des bobines ou des condensateurs, ceux-ci peuvent temporairement restituer de l’énergie préalablement stockée.
Un amplificateur est donc nécessairement un système actif.
- Perturbation de la grandeur d'entrée :
Le quadripôle et la charge consommant de l'énergie (par effet Joule), la puissance fournie par la source est non nulle, donc $u_e$ **et** $i_e$ sont non nuls.
La tension d’entrée $u_e = E - Ri_e$ est différente de $E$ et dépend de la charge du quadripôle.
En revanche, nous pouvons envisager qu’un système actif fournisse la totalité de la puissance dissipée dans le quadripôle et de la puissance cédée à la charge. Dans ce cas, il est possible d’avoir $i_e = 0$ pour $u_e \neq 0$ (ou $u_e = 0$ pour $i_e \neq 0$) ce qui correspond à une impédance d’entrée infinie (ou nulle). Plus généralement :
Un quadripôle d’impédance d’entrée nulle ou infinie doit être actif.
- Sélectivité d'un filtre passe-bande passif :
Nous avons vu au [[02-Étude fréquentielle des systèmes linéaires|chapitre 2]] que la sélectivité d'un filtre passe-bande est une fonction croissante de son facteur de qualité $Q$.
Par ailleurs, l'étude du régime libre d'un tel filtre (s'il est peu amorti) montre que son facteur de qualité est proportionnel au rapport entre l’énergie accumulée et l'énergie dissipée pendant une pseudo-période (voir H-Prépa, Électrocinétique - Électronique, 1re année, page 106).
Un système actif, qui apporte de l'énergie, permet de compenser partiellement l’énergie dissipée dans les résistances et donc d’obtenir des valeurs plus importantes du facteur $Q$.
La réalisation d’un filtre passe-bande très sélectif est plus aisée avec un système actif.
- Conclusion : De ce rapide survol nous retenons que les systèmes actifs permettent de réaliser :
	- des opérateurs de même nature que ceux que l’on sait réaliser avec un système passif, mais plus performants ;
	- des opérateurs impossibles à obtenir avec des systèmes passifs.

==**Amplificateur opérationnel idéal**== : 
L’amplificateur opérationnel idéal est un composant théorique actif possédant trois bornes : l'entrée inverseuse notée -, entrée non inverseuse notée + et la sortie, Aucun courant n’entre par les entrées : $i_+ = i_- = 0$.
L’A.O idéal est représenté sur la [[#^figure2|figure 2]].
Un courant quelconque peut sortir (ou entrer) par la sortie.
Un amplificateur opérationnel peut fonctionner suivant deux régimes :
- un régime dit « linéaire » : $\epsilon = 0$ et $v_s$ est fixée par le reste du circuit compte tenu de la relation $\epsilon = 0$, dans la limite où $v_s$ ne dépasse pas des valeurs fixées par les alimentations $V_{sat}^{-} < v_s < V_{sat}^{+}$ ;
- un régime dit «non linéaire » : la tension de sortie de l’amplificateur prend alors une des valeurs limite $V_{sat}^{+}$ ou $V_{sat}^{-}$ :
	- si $\epsilon > 0$, $v_s = V_{sat}^{+}$ la tension de saturation est positive ;
	- si $\epsilon < 0$, $v_s = V_{sat}^{-}$ la tension de saturation est négative.
En général, $V_{sat}^{-} = -V_{sat}^{+}$
La caractéristique de transfert d’un amplificateur opérationnel idéal est représentée sur la [[#^figure3|figure 3]].
Remarques :
- Le terme « linéaire » vient du fait que nous pourrons appliquer les lois de l'électrocinétique linéaire à un circuit ne contenant que des composants linéaires et des amplificateurs opérationnels idéaux en régime linéaire.
- Les alimentations continues $+V_{cc}$ et $-V_{cc}$ de l'amplificateur opérationnel ne sont généralement pas représentées : des courants non visibles sur les schémas arrivent et partent de la masse. Il est impossible d’écrire la loi des nœuds en ce dernier point avec les courants figurant sur ces schémas.

==**Limitations non linéaires**== :
Le modèle linéaire à bande passante limitée est une très bonne approximation des caractéristiques de l’A.O. à condition que le signal de sortie reste dans ces limites bien définies.
- Saturation en tension : Cet aspect a déjà été traité : la tension de sortie est comprise entre $-V_{sat}$ et $+V_{sat}$.
- Saturation en courant : Une surintensité en sortie détériorerait l'amplificateur. Pour l’éviter, le courant de sortie est limité par construction : $|i_s| < I_{sat}$ avec $I_{sat}$ de l'ordre de 20 mA. Cet effet non linéaire se manifeste lorsque l’impédance de la charge est faible.
- Vitesse de balayage : Les effets capacitifs internes a l’amplificateur opérationnel imposent à la tension de sortie $v_s(t)$ une vitesse maximale d’évolution appelée vitesse de balayage (ou slewrate) notée $\sigma$. $\left(\dfrac{dv_s(t)}{dt}\right) \leqslant \sigma$. Le système sort donc de son mode de fonctionnement linéaire dés que la dérivée de la tension de sortie $v_s(t)$ atteint cette valeur. Cet effet non linéaire se manifeste principalement à haute fréquence : on peut dire qu’alors le composant ne « suit » plus le signal d’entrée.

==**Dérives**== :
Du fait du fonctionnement interne de l’amplificateur en régime linéaire, les courants d’entrée et la tension différentielle ne sont pas rigoureusement nuls. Pour rendre compte de ces perturbations (négligeables dans la plupart des applications), nous ajoutons des sources fictives de courant et de tension au modèle linéaire.
Un modèle de l’A.O. est donné sur la [[#^figure6|figure 6]].
La tension de décalage $V_d$ vérifie $|V_d| < V_{10}$ avec $V_{10}$ est la tension de décalage à l'entrée (input offset voltage). Elle peut être diminuée en utilisant le réglage d’« offset » ([[#^figure7|fig. 7]]).
Le courant de polarisation est défini par $I_{IB} = \frac{|i_0 + i_1|}{2}$ et le courant de décalage par $I_{10} = \frac{|i_0 - i_1|}{2}$.

> [!note] Amplification
> Un montage amplificateur réalise pour tous les types de signaux l'opération $v_s = kv_e$ avec $k$ constante réelle. Il est dit non inverseur si $k$ est positive et inverseur si $k$ est négative.
> - Amplificateur non inverseur : Tous ce qui est dit dans ce chapitre sur son montage théorique, sa réalisation expérimentale et sa comparaison au modèle théorique ont été résumé dans les chapitres [[07-L'amplificateur opérationnel. Le modèle idéal|7]] et [[10-Amplificateur opérationnel. Bande passante, stabilité des montages bouclés et comparateurs|10]] de l'ouvrage H-Prépa, Électronique-Électrocinétique, 1re année.
> - Suiveur : Le montage suiveur correspond au cas particulier $R_1$ infinie et $R_2$ nulle du montage de non inverseur ([[#^figure8|fig. 8]]) donc $H_0 = 1$ et $f_H = f_0$.
> Nous avons alors $v_s \approx v_e$ dans la bande passante $[0 ; f_0]$ du suiveur, c’est-à-dire jusqu'à la fréquence de gain nul de l’A.O. (soit $f < 1$ MHz pour le 741 par exemple), à condition que son fonctionnement soit linéaire.
> Ce montage est un adaptateur d’impédance : son impédance d’entrée est quasiment infinie et son impédance de sortie est nulle.
> Nous l’utiliserons dans tous les montages nécessitant une grande impédance de charge. C’est aussi un amplificateur de courant donc de puissance.
> - Amplificateur inverseur :
> Étude théorique : Considérons le montage de la [[#^figure9|figure 9]] où l'amplificateur opérationnel est supposé idéal. Comme $i_+$ est nulle, $v_+$ est nulle, la résistance $R$ n'intervient pas quand l'A.O. est idéal. En théorie $R$ est quelconque et peut être nulle. Une étude plus complète montre que les défauts liés aux courants de polarisation de l'A.O. sont minimisés si $R = R_1 \parallel R_2 = \frac{R_1R_2}{R_1 + R_2}$. En régime linéaire $\epsilon = 0$, donc $v_- = 0$. En outre, $i_-$ est nulle ; il en résulte que $v_e = R_1i_e$ et $v_s = -R_2i_e$. Nous obtenons : $v_s = -\frac{R_2}{R_1}v_e$.
> Ce montage est un amplificateur de tension inverseur ($v_s$ et $v_e$ sont de signes opposés) d'amplification $H = -\frac{R_2}{R_1}$.
> Son impédance d'entrée est $R_1$ et son impédance de sortie est nulle ($v_s$ est indépendante de $i_s$).
> Réalisation expérimentale : Les résultats de l’étude fréquentielle pour différentes valeurs de $R_2$ sont donnés sur les figures [[#^figure10|10]] et [[#^figure11|11]] : le montage est un filtre passe-bas. Le déphasage $\varphi$ qu’il introduit varie de 180° (montage inverseur) à 90°. Les asymptotes haute fréquence de la réponse en gain sont voisines mais distinctes de l’asymptote haute fréquence du montage non inverseur : $G = -\log\frac{f}{f_0}$.
> Le [[#^demo1|produit]] « gain x bande passante » n’est pas constant pour l’amplificateur inverseur.
> 
> Conclusion : A.O. réel et A.O. idéal : Nous pouvons déduire deux résultats des études précédentes, que nous généraliserons à la majorité des montages à amplificateur opérationnel.
> - La « boucle de réaction (ou de rétroaction) » doit être reliée à l'entrée inverseuse pour que le montage soit stable.
> - Les limitations dues au gain fini de l’A.O. réel sont visibles si le gain théorique du montage n’est pas petit devant celui $(20\log|\mu(j\omega)|)$ de l’A.O. en boucle ouverte. 

> [!note] Addition et soustraction
> - Sommateur : Tous ce qui est dit dans ce chapitre sur ce montage a été résumé dans le chapitre [[07-L'amplificateur opérationnel. Le modèle idéal|7]] de l'ouvrage H-Prépa, Électronique-Électrocinétique, 1re année.
> - Amplificateur différentiel : Comment obtenir la différence de deux tensions ?
> Il suffit d’utiliser simultanément un amplificateur opérationnel en amplificateur inverseur et non inverseur.
> Le montage le plus simple qui réalise cette opération est donné sur la [[#^figure12|figure 12]].
> Utilisons le théorème de superposition :
> 	- si la source $v_1$ est éteinte, le montage est équivalent à un amplificateur inverseur d'amplification $-\frac{R_2}{R_1}$ : $v_s = -\frac{R_2}{R_1}v_2$ ;
> 	- si la source $v_2$ est éteinte, le montage est équivalent à un pont diviseur de tension de rapport $\frac{R_4}{R_3 + R_4}$ suivi d’un amplificateur non inverseur d’amplification $\frac{R_2 + R_1}{R_1}$ : $v_s = \frac{R_4}{R_3 + R_4}\frac{R_2 + R_1}{R_1}v_1$,
> 
> 	d'où : $v_s = \frac{R_4}{R_3 + R_4}\frac{R_2 + R_1}{R_1}v_1 - \frac{R_2}{R_1}v_2$ Si $R_1R_4 = R_2R_3$, alors $vs = \frac{R_2}{R_1}(v_1 - v_2)$.
> 	Le montage de la [[#^figure12|figure 12]] présente l'inconvénient d’avoir des impédances d'entrées finies et dissymétriques. On peut y remédier en intercalant des suiveurs.

> [!note] Intégration et dérivation
> Nous avons constaté au [[02-Étude fréquentielle des systèmes linéaires|chapitre 2]] qu'un filtre du premier ordre peut, dans un certain domaine de fréquences, se comporter approximativement comme un dérivateur ou comme un intégrateur. Les systèmes présentés ci-dessous sont plus performants et, contrairement aux systèmes passifs, ont des caractéristiques qui ne dépendent pratiquement pas de la charge.
> 
> - Exemple de montage intégrateur performant :
> 
> Montage théorique : Étudions le montage théorique de [[#^figure13|figure 13]].
> Écrivons la loi des nœuds au niveau de l'entrée inverseuse de l'A.O. : $\frac{v_e - v_-}{R} + C\dfrac{d(v_s - v_-)}{dt} = 0$. En régime linéaire, $v_-$ est nulle, soit $\dfrac{dv_s}{dt} = -\frac{v_e}{RC}$.
> Le montage réalise bien une intégration quel que soit le signal d'entrée et pour toute charge branchée en sortie.
> 
> Réalisation à l'aide d’un amplificateur opérationnel réel : Réalisons le montage de [[#^figure14a|figure 14a]].
> L'interrupteur a été placé de façon à pouvoir décharger le condensateur.
> Prenons $v_e$ nulle (entrée court-circuitée) et ouvrons l’interrupteur à l’instant $t = 0$. Nous observons que $v_s$ varie linéairement au cours du temps pendant quelques secondes jusqu’à atteindre $v_s = \pm V_{sat}$, tension de saturation de l’amplificateur opérationnel ([[#^figure14b|fig. 14b]]).
> Cette dérive de la tension de sortie du montage est due aux défauts de l’A.O. : tension de décalage et courants de polarisation. Ce montage théorique n’est pas utilisable dans la pratique.
> Pour éliminer le phénomène de dérive, il faudrait décharger régulièrement le condensateur. Remplaçons l'interrupteur par une résistance $R'$ ([[#^figure15|fig. 15]]) et cherchons la fonction de transfert du montage en considérant l'amplificateur opérationnel comme idéal.
> La loi des nœuds appliquée a l’entrée inverseuse donne : $v_s(p)\left(Cp + \frac{1}{R'}\right) + \frac{v_e(p)}{R} = 0$, d'où la fonction de transfert $H(p) = \frac{-\frac{R'}{R}}{1 + R'Cp}$.
> Le filtre est un passe-bas du premier ordre de pulsation de coupure $\frac{1}{R'C}$ et d’asymptote haute fréquence $G_{dB} = -20\log(RC\omega)$ et $\varphi = \frac{\pi}{2}$.
> Donc pour un signal d’entrée périodique de période $T' \ll R'C$, le signal de sortie vaut $v_s = -\frac{1}{RC}\int v_edt$ (la constante d’intégration est telle que le signal est de valeur moyenne nulle). La partie continue du signal subit une amplification égale à $-\frac{R'}{R}$.
> 
> - Exemple de montage dérivateur performant :
> Le montage pseudo-dérivateur $RC$ présente des inconvénients semblables à ceux du pseudo-intégrateur $RC$ : limitation aux basses fréquences, amplitude de signal faible et perturbation par la charge.
> Étudions un montage à amplificateur opérationnel éliminant ces défauts.
> 
> Montage théorique : Étudions le montage théorique de [[#^figure16|figure 16]].
> Écrivons la loi des nœuds au niveau de l’entrée inverseuse de l’A.O. : $\frac{v_s - v_-}{R} + C\dfrac{d(v_e - v_-)}{dt} = 0$, soit en régime linéaire : $v_s = -RC\dfrac{dv_e}{dt}$.
> Le montage réalise bien une dérivation quel que soit le signal d’entrée. Sa fonction de transfert est $H(p) = RCp$ pour toute charge.
> 
> Réalisation à l'aide d'un amplificateur opérationnel réel : Réalisons le montage théorique à l'aide d'un amplificateur opérationnel "741" avec $R = 10 k\Omega$ et $C = 100 nF$.
> En choisissant comme signal d'entrée, un signal triangulaire d'amplitude 1 V, nous obtenons les résultats de [[#^figure17|figure 17]].
> Le montage présente un phénomène d'oscillations semblable à celui observé pour le filtre passe-bande de coefficient de qualité important. Il y a résonance. Le tracé du diagramme de Bode correspondant nous indique une résonance très aiguë pour une fréquence $f_0$ d’environ 13 kHz ([[#^figure18|fig. 18]]).
> Cette résonance est due à la bande passante limitée de l’A.O.
> Le caractère dérivateur du montage est alors masqué par le phénomène de résonance.
> Il faut diminuer l’acuité de la résonance du montage et donc diminuer le facteur de qualité du circuit.
> Pour un circuit (R, L, C), il suffit d’augmenter $R$. Ici, nous ajoutons une résistance en série avec le condensateur ([[#^figure19|fig. 19]]).
> Le choix optimal peut être réalisé en observant la réponse à un signal triangulaire. Il se fait en ajustant la valeur de $R'$ ([[#^figure20|fig. 20]]) : la réponse la plus proche du créneau est obtenue pour $250 \Omega$ dans le cas des valeurs de $R$ et $C$ choisies pour un $\mu A741$.

> [!note] Comparateur : Comparateur simple
> La définition et la réalisation données dans ce chapitre est la même que celles résumées dans le chapitre [[07-L'amplificateur opérationnel. Le modèle idéal|7]] de l'ouvrage H-Prépa, Électronique-Électrocinétique, 1re année.
> 
> Écarts entre les caractéristiques réelles et idéales : Les comparateurs à amplificateurs opérationnels réels possèdent des caractéristiques qui différent notablement de celles données dans la définition et la réalisation.
> Mettons en évidence les influences des divers « défauts » d’un A.O. réel, à savoir : son gain fini, sa fréquence de coupure en boucle ouverte finie, sa vitesse de balayage finie et sa tension de décalage éventuelle, en supposant, pour chacun des cas considérés, que c’est le défaut étudié qui est le seul présent.

> [!note] Comparateur : Comparateur simple : Conséquence d'un gain statique fini
> En statique, l'amplification en tension $A_0$ d’un A.O. réel en boucle ouverte est finie. La caractéristique du comparateur ([[#^figure21|fig. 21]]) possède un flanc incliné à la différence de celle d’un comparateur à A.O. idéal qui possède un flanc vertical (de pente infinie). L’amplificateur opérationnel ne sera saturé que si : $|v_{de}| = |v_e - V_{ref}| \geqslant \frac{V_{sat}}{A_0}$.
> Il en résulte que la tension d’entrée doit varier de $\delta v_e = \frac{2V_{sat}}{A_0}$, entre : $v_{e1} = V_{ref} - \frac{V_{sat}}{A_0}$ et $v_{e2} = V_{ref} + \frac{V_{sat}}{A_0}$, pour que la tension de sortie $v_s$ bascule de $-V_{sat}$ à $+V_{sat}$.
> Cet intervalle $\delta v_e = \frac{2V_{sat}}{A_0} = v_{e2} - v_{e1}$ est l'intervalle de résolution du comparateur (0,28 mV pour un type 741).
> La [[#^figure22|figure 22]] représente l’évolution des tensions d’entrée $v_e(t)$ (nous avons choisi un signal d’entrée sinusoïdal basse fréquence) et de sortie $v_s(t)$.
> Les signaux $v_s(t)$ et $v_e(t)$ s’annulent simultanément $(V_{ref} = 0)$ en ne considérant que ce défaut de l’amplificateur.

> [!note] Comparateur : Comparateur simple : Conséquence d'une fréquence de coupure en boucle ouverte finie
> Considérons un comparateur non inverseur réalisé avec un A.O. dont l’équation différentielle d’évolution en régime linéaire est donnée par : $\tau\dfrac{dv_s}{dt} + v_s = A_0v_{de}$ avec $v_{de} = v_e(t)$, $\tau = 10^{-2} s$ et $A_0 = 10^{5}$.
> Remarquons que nous sortons du régime linéaire dès que la solution $v_s(t)$ de l’équation précédente est telle que $|v_s(t)| \geqslant V_{sat}$.
> Les stimulations des solutions $v_s(t)$ ([[#^figure23|fig. 23]]), lorsque $v_e(t)$ est sinusoïdal $(v_e(t) = v_{em}\sin(2\pi ft))$, en ne considérant que ce « défaut », nous montrent une augmentation significative de l’intervalle de résolution avec la fréquence $f$ et l'amplitude $v_{em}$ du signal $v_e(t)$.
> L'intervalle de résolution, faible en « statique » (de l'ordre de 0,30 mV avec un A.O.) augmente avec la fréquence du signal. Cet intervalle de résolution peut être très gênant si la tension de commande est voisine de la tension de référence dans le cas où il existe un bruit, dont l’amplitude est de l’ordre de cet intervalle.

> [!note] Comparateur : Comparateur simple : Conséquence d'une vitesse de balayage finie
> Rappelons que la vitesse d'évolution de la tension de sortie est limitée : $\left|\dfrac{dv_s(t)}{dt}\right| \leqslant \sigma$.
> Soit un comparateur non inverseur dont l’amplificateur opérationnel a pour unique défaut la valeur finie de sa vitesse de balayage. Choisissons $V_{ref} = 0$ et appliquons à l'entrée du comparateur un signal sinusoïdal $v_e(t)$.
> A $t = t_0$ la tension d’entrée s’annule et à $t > t_0$, elle est négative ([[#^figure24|fig. 24]]).
> Pour un comparateur parfait, un basculement de $V_{sat}$ à $-V_{sat}$ se produirait à $t = t_0$.
> Pour le comparateur étudié, $v_s(t)$ ne s’annule qu’à $t = t_{0}^{'}$ tel que : $t_{0}^{'} - t_0 = \frac{V_{sat}}{\sigma}$, c’est-à-dire que nous observons un décalage temporel $\Delta t = t_{0}^{'} - t_0$ qui est le temps nécessaire à $v_s(t)$ pour passer de $V_{sat}$ à zéro.
> A $t_{0}^{''}$, tel que $t_{0}^{''} - t_{0}^{'} = \frac{V_{sat}}{\sigma}$, la tension $v_s(t)$ atteint sa valeur de saturation $-V_{sat}$ et la tension $v_e(t)$ prend alors la valeur $-\frac{\Delta V_e}{2}$ ([[#^figure24|fig. 24]]).
> Lorsqu’à $t = t_1$, la tension d’entrée s'annule par valeurs croissantes, nous observerons le même décalage temporel entre $v_e$ et $v_s$. La tension de sortie s'annule à $t_{1}^{'}$ tel que $t_{1}^{'} = t_1 + \frac{V_{sat}}{\sigma}$, et elle prend sa valeur de saturation à $t_{1}^{''} = t_1 + \frac{V_{sat}}{\sigma}$ lorsque $v_e$ à la valeur $\frac{\Delta V_e}{2}$.
> La caractéristique $v_s = f(v_e)$ à cette fréquence est donnée sur la [[#^figure25|figure 25]]. Elle possède des flancs obliques et fait apparaître un phénomène d'hystérésis, c’est-à-dire que le point figuratif de l’état du comparateur ne suit pas le même chemin suivant que $v_e$ croît ou décroît. La largeur du cycle d’hystérésis est $\Delta V_e$. Lorsque la fréquence croît, la vitesse de balayage déforme la caractéristique du circuit ([[#^figure26|fig. 26]]) jusqu’à le rendre inutilisable en comparateur.
> 
> ==**La valeur finie de la vitesse de balayage est le plus important facteur de limitation des performances d'un comparateur simple à A.O.**==

> [!note] Comparateur : Comparateur simple : Conclusion
> Les caractéristiques de commutation d’un comparateur simple à A.O. sont médiocres. Ce type de comparateur doit être réservé pour les traitements de signaux en basse fréquence (inférieures à 1 kHz pour les $\mu A 741$ et inférieures à 10 kHz pour le TL 801), au-delà il est nécessaire d’utiliser des circuits intégrés spécialisés. Parmi les applications des comparateurs simples, signalons :
> - la détection d’un niveau de tension de référence $V_{ref}$ ;
> - la transformation d’un signal analogique variable en un signal numérique à deux niveaux $v_H = V_{sat}$ et $v_B = -V_{sat}$, permettant son traitement logique.

> [!note] Comparateurs à hystérésis
> - Nécessité et principe des comparateurs à hystérésis :
> Les comparateurs simples sont sensibles au bruit. En effet, lorsque la tension d’entrée $v_e$ est voisine de la tension de référence $V_{ref}$, une tension de bruit peut provoquer intempestivement et aléatoirement le basculement du comparateur d'une saturation à l’autre. La [[#^figure27|figure 27]] illustre ce phénomène. Pour palier ce défaut, il est nécessaire de disposer de comparateurs à cycle d’hystérésis permanent et de largeur suffisante pour neutraliser cette sensibilité au bruit. En outre, il est souhaitable que les caractéristiques soient indépendantes de la fréquence et que les fronts de commutation soient verticaux. Une solution consiste à munir l’amplificateur opérationnel utilisé d’une boucle de rétroaction positive.
> Un comparateur hystérésis est réalisé à l'aide d’un amplificateur opérationnel possédant une boucle de rétroaction aboutissant sur l’entrée non inverseuse.
> Comme pour les comparateurs simples, il existe deux types de comparateurs à hystérésis selon que le signal d’entrée est introduit sur l’entrée non inverseuse (comparateur non inverseur à hystérésis) ([[#^figure28|fig. 28a]]) ou sur l’entrée inverseuse (comparateur inverseur à hystérésis) ([[#^figure28|fig. 28b]]).
> ==**Comme pour les comparateurs simples, c’est la vitesse de balayage qui limite les performances des comparateurs à hystérésis.**==
> - Caractéristiques d'un comparateur à hystérésis :
> 	- Comparateur non inverseur : Tout ce qui est donné dans ce chapitre est le même que celui résumé dans le chapitre [[10-Amplificateur opérationnel. Bande passante, stabilité des montages bouclés et comparateurs|10]] de l'ouvrage H-Prépa, Électronique-Électrocinétique, 1re année.
> 	- Comparateur inverseur : Tout ce qui est donné dans ce chapitre est le même que celui résumé dans le chapitre [[10-Amplificateur opérationnel. Bande passante, stabilité des montages bouclés et comparateurs|10]] de l'ouvrage H-Prépa, Électronique-Électrocinétique, 1re année.
> 	- Influence de la fréquence : En régime dynamique se manifestent les limitations liées à la vitesse de balayage $\sigma$ finie et au temps de désaturation non nul des A.O. Ces effets s’observent sur les deux types de comparateurs (inverseurs et non inverseurs) et sont d’autant plus marqués que l’A.O. est moins performant : pour un $\mu A 741$ ([[#^figure29|fig. 29]]) et pour un TL 081.

> [!note] Générateur d'oscillations périodiques
> L'association en boucle fermée de deux opérateurs permet d'obtenir des oscillations périodiques réglables en fréquence. Nous étudions ici les oscillations de relaxation obtenus en associant un comparateur à hystérésis et un intégrateur.
> - Multivibrateur astable : Son principe, le calcul et le contrôle de sa période et du son rapport cyclique et son vérification expérimentale, qui sont donnés dans ce chapitre, sont les mêmes que ceux résumés dans le chapitre [[10-Amplificateur opérationnel. Bande passante, stabilité des montages bouclés et comparateurs|10]] de l'ouvrage H-Prépa, Électronique-Électrocinétique, 1re année.
> - Principe du générateur de fonction :
# Diagrammes
Quadripôle passif
![[electronique2/attachments-electronique2/figure43.png]]^figure1

Représentation de l'amplificateur opérationnel idéal. Les bornes d'alimentation $+V_{cc}$ et $-V_{cc}$ ne sont pas représentés
![[electronique2/attachments-electronique2/figure44.png]]^figure2

Schéma équivalent d'un A.O. $i_0$ et $i_1$ sont positifs pour un 741 et négatifs pour un TL 081
![[electronique2/attachments-electronique2/figure48.png]]^figure6

Réglage de la tension de décalage pour un "741" en boîtier huit broches. 1 : réglage offset ; 2 : entrée - ; 3 : entrée + ; 4 : $-V_{cc}$ ; 5 : réglage offset ; 6 : sortie ; 7 : $+V_{cc}$
![[electronique2/attachments-electronique2/figure49.png]]^figure7

Montage suiveur à amplificateur
![[electronique2/attachments-electronique2/figure50.png]]^figure8

Montage amplificateur inverseur
![[electronique2/attachments-electronique2/figure51.png]]^figure9

Amplificateur différentiel à A.O.
![[electronique2/attachments-electronique2/figure56.png]]^figure12

Intégrateur à A.O.
![[electronique2/attachments-electronique2/figure57.png]]^figure13

Montage intégrateur à A.O. réel avec interrupteur pour décharge $C$
![[electronique2/attachments-electronique2/figure58.png]]^figure14a

Intégrateur à A.O. ne présentant pas de dérive
![[electronique2/attachments-electronique2/figure60.png]]^figure15

Dérivateur à A.O.
![[electronique2/attachments-electronique2/figure61.png]]^figure16

Dérivateur à A.O. corrigé. La résistance $R'$ sert à diminuer l'acuité à la résonance due à la bande passante limitée de l'A.O. ($R = 10 k\Omega$, $C = 100 nF$ et $R' = 250 \Omega$)
![[electronique2/attachments-electronique2/figure64.png]]^figure19

Comparateur à hystérésis : a. non inverseur ; b. inverseur
![[electronique2/attachments-electronique2/figure73.png]]^figure28
# Graphiques
Caractéristique de transfert de l'amplificateur opérationnel idéal
![[electronique2/attachments-electronique2/figure45.png]]^figure3

Caractéristique de transfert statique
![[electronique2/attachments-electronique2/figure46.png]]^figure4

Gain et déphasage du $\mu A741$ en fonction de la fréquence. Dans le domaine de fréquences usuelles (0 MHz à 1 MHz), le 741 se comporte comme un passe-bas du premier ordre
![[electronique2/attachments-electronique2/figure47.png]]^figure5

Diagramme de Bode pour différentes valeurs de $R_2$ $(R_1 = 10 k\Omega)$ ; les asymptotes haute fréquence ont toutes la même pente de -20 dB par décade mais ne sont pas confondues
![[electronique2/attachments-electronique2/figure52.png]]^figure10

Phase mesurée pour $R_2$ variant de $10 k\Omega$ à $100 k\Omega$
![[electronique2/attachments-electronique2/figure53.png]]^figure11

Tension de sortie pour $v_e = 0$
![[electronique2/attachments-electronique2/figure59.png]]^figure14b

Réponse du montage dérivateur à A.O. à un signal triangulaire de fréquence 100 Hz
![[electronique2/attachments-electronique2/figure62.png]]^figure17

Diagramme de Bode du montage dérivateur
![[electronique2/attachments-electronique2/figure63.png]]^figure18

Réponse du dérivateur à A.O. à un signal triangulaire de fréquence 100 Hz d'amplitude 1 V pour $R' = 50\, \Omega$, $250\, \Omega$ et $450\, \Omega$. La réponse la plus proche du créneau correspond à $R' = 250\, \Omega$ pour l'A.O. $\mu A741$
![[electronique2/attachments-electronique2/figure65.png]]^figure20

Caractéristique d'un comparateur simple ayant pour unique défaut un gain statique
![[electronique2/attachments-electronique2/figure66.png]]^figure21

Le comparateur bascule d'un état de saturation à l'autre dès que : $|v_e(t)| = \frac{V_{sat}}{A_0}$
![[electronique2/attachments-electronique2/figure67.png]]^figure22

Évolution de l'intervalle de résolution $\delta v_e$ pour diverses fréquences et diverses amplitudes du signal d'entrée. a. $V_{em} = 5 V$ ; $f = 100 Hz$ ; $dv_e = 236 mV$. b. $V_{em} = 5 V$ ; $f = 10000 Hz$ ; $dv_e = 2627 mV$. c. $V_{em} = 10 V$ ; $f = 10000 Hz$ ; $dv_e = 3730 mV$
![[electronique2/attachments-electronique2/figure68.png]]^figure23

Réponse d'un comparateur simple non inverseur à A.O. (type 741) soumis à une commande sinusoïdale de fréquence $f = 1 kHz$
![[electronique2/attachments-electronique2/figure69.png]]^figure24

Caractéristique d'un comparateur simple non inverseur à A.O. (type 741) soumis à un signal triangulaire de fréquence $f = 1 kHz$
![[electronique2/attachments-electronique2/figure70.png]]^figure25

Caractéristique d'un comparateur simple non inverseur à A.O. (type 741) soumis à un signal sinusoïdal de fréquence $f = 5 kHz$
![[electronique2/attachments-electronique2/figure71.png]]^figure26

a. Signal bruité. b. Réponse d'un comparateur simple à ce signal
![[electronique2/attachments-electronique2/figure72.png]]^figure27

Caractéristiques d'un comparateur inverseur à A.O. du type $\mu A 741$ soumis à un signal sinusoïdal d'amplitude $v_{em} = 10 V$. a. $f = 1 kHz$. b. $f = 5 kHz$
![[electronique2/attachments-electronique2/figure74.png]]^figure29
# Expériences

# Autres notes
> [!warning] Application 1 page 118
> Le document 18 dans l'énoncé correspond à la [[#^figure9|figure 9]] ici.
> ![[electronique2/attachments-electronique2/figure54.png]] ![[electronique2/attachments-electronique2/figure55.png]]
^demo1
