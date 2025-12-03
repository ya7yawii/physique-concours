---
titre: "[[07-L'amplificateur opérationnel. Le modèle idéal]]"
tags:
  - amplificateur-opérationnel
  - inverseur
  - non-inverseur
  - comparateur-de-tension
crée: 12-11-2025, 19:41
---
# Formules
> [!note] Étude théorique d'un amplificateur non inverseur
> Considérons le montage représenté sur la [[#^figure6|figure 6]] avec un A.O. supposé idéal $(i_+ = i_- = 0)$. Faisons l'hypothèse du régime linéaire $(\epsilon = 0)$ que nous justifierons ultérieurement. Comme $i_-$ est nul, le potentiel de l'entrée inverseuse est donné par la formule du pont diviseur, soit : $v_- = \frac{R_1}{R_1 + R_2}v_s$. D'où $v_s = (1 + \frac{R_2}{R_1})v_e$, puisque'en régime linéaire $v_e = v_+ = v_-$. Le montage étudié est un amplificateur de tension non inverseur ($v_s$ et $v_e$ sont de mêmes signes) d'amplification : $H = 1 + \frac{R_2}{R_1}$. Son impédance d'entrée est infinie $(i_e = 0)$ et son impédance de sortie est nulle ($v_s$ indépendant de $i_s$).
> Remarque : Même si le courant de sortie $i_s$ de l'amplificateur non inverseur est nul, un courant non nul $i$ sort de l'amplificateur opérationnel.
^theo1

> [!note] Étude théorique d'un amplificateur inverseur
> Considérons le montage de la [[#^figure25|figure 25]] où l'amplificateur opérationnel est supposé idéal.
> Comme $i_+$ est nulle, $v_+$ est nulle. En régime linéaire $\epsilon = 0$, donc $v_- = 0$. En outre, $i_-$ est nulle ; il en résulte que $v_e = R_1i_e$ et $v_s = -R_2i_e$. Nous obtenons : $v_s = -\frac{R_2}{R_1}v_e$.
> Ce montage est un amplificateur de tension inverseur ([[#^figure26|fig. 26]]) ($v_s$ et $v_e$ sont de signes opposés) d'amplification $H = -\frac{R_2}{R_1}$.
> Son impédance d'entrée est $R_1$ et son impédance de sortie est nulle ($v_s$ est indépendante de $i_s$).
^theo2

> [!note] Étude théorique d'un sommateur de tensions
> En reliant les fils parcourus par deux courants $i_1$ et $i_2$, il est simple d'obtenir la somme $i_1 + i_2$ des intensités dans un troisième fil. Remarquons qu'il est impossible d'obtenir directement une somme de tensions $u_1 + u_2$ si les deux sources de tension ont une de leurs bornes reliées à la masse.
> Considérons le montage de la [[#^figure28|figure 28]] ($R$ est quelconque, à la limite $R = 0$). L'amplificateur opérationnel est en régime linéaire à cause de la résistance $R_3$ qui introduit une rétroaction sur l'entrée inverseuse, donc $\epsilon = 0$. Comme $i_+ = 0$, il en résulte $v_+ = 0$ et $v_- = 0$. L'intensité $i$ est la somme $i_1 + i_2$. Cette loi des nœuds traduite en termes de potentiels s'écrit : $\frac{v_1}{R_1} + \frac{v_2}{R_2} = -\frac{v_s}{R_3}$, soit encore $v_s = -\left(\frac{R_3}{R_1}v_1 + \frac{R_3}{R_2}v_2\right)$.
> Nous avons donc réalisé, par l'intermédiaire d'une somme de courants, une somme pondérée des tensions $v_1$ et $v_2$. Si $R_1 = R_2 = R_3$, la tension de sortie est l'opposée de la somme des tensions d'entrée : $v_s = -(v_1 + v_2)$.
^theo3

> [!note] Réalisation d'un dipôle de résistance négative
> Un composant actif comme l'amplificateur opérationnel permet de fabriquer des dipôles dont la caractéristique est impossible à obtenir avec des composants passifs. Nous étudions ici l'exemple de la résistance négative.
> Imaginons un dipôle qui, en convention récepteur, a pour caractéristique : $u = Ri$ avec $R < 0$.
> Dans ce cas, la puissance $\mathcal{P} = Ri^{2}$ <mark style="color: red">dissipée</mark> par le dipôle est toujours négative. Cela signifierait que le dipôle convertit de l'énergie thermique en énergie électrique, ce qui est impossible pour un dipôle passif.
> En revanche, si le dipôle inclut un composant actif, l'énergie apportée au circuit peut provenir de l'alimentation du composant.
> Étudions le circuit représenté sur la [[#^figure32|figure 32]]. Nous pouvons le décomposer en deux blocs : la source de f.e.m. $E$ et de résistance interne $R_i$ et le circuit situé à droite des bornes $A$ et $B$. La résistance équivalente de ce circuit est : $R_e = \frac{u}{i}$.
> Nous supposons que l'amplificateur opérationnel est en régime linéaire. Ce n'est pas, a priori, évident du fait qu'il y a une rétroaction à la fois sur l'entrée non inverseuse et sur l'entrée inverseuse, mais nous l'admettons et nous pouvons le constater expérimentalement si la condition $R_1R_i > RR_2$ est satisfaite.
> Écrivons la loi des nœuds au point $A$ : $i = \frac{u - u_s}{R}$.
> L'amplificateur étant idéal, la tension $u_+$ se déduit de $u_s$ par un diviseur de tension.
> En régime linéaire : $u = u_+ = u_s\frac{R_2}{R_1 + R_2}$. Nous en déduisons : $Ri = -u\frac{R_1}{R_2}$ et donc $R_e = -R\frac{R_2}{R_1}$.
# Définitions
==**Amplificateur opérationnel idéal**== :
L'amplificateur opérationnel (A.O.) idéal est un composant théorique possédant trois bornes : l'entrée inverseuse, notée -, l'entrée non inverseuse, notée + et la sortie. Il est représenté symboliquement par la [[#^figure1|figure 1]].
Aucun courant n'arrive par les entrées : $i_+ = i_- = 0$. En revanche, un courant $i_s$ qui dépend des circuits extérieurs peut sortir (ou entrer) par la sortie.
Un amplificateur opérationnel idéal peut fonctionner suivant deux régimes :
- un régime linéaire pour lequel $\epsilon = 0$ et $v_s$ fixé par le reste du circuit, compte tenu de la relation $\epsilon = 0$ et dans la limite où $v_s$ ne dépasse pas des valeurs fixées par les alimentations $V_{sat}^- < v_s < V_{sat}^+$ ;
- un régime non linéaire pour lequel la tension de sortie $v_s$ de l'amplificateur prend une des valeurs limites $V_{sat}^+$ ou $V_{sat}^-$. Ainsi, lorsque $\epsilon > 0$, $v_s = V_{sat}^+$ tension de saturation positive et lorsque $\epsilon < 0$, $v_s = V_{sat}^-$ tension de saturation négative. En général, $V_{sat}^- = -V_{sat}^+$, si bien que si $\epsilon > 0$, alors $v_s = V_{sat}$ et si $\epsilon < 0$, alors $v_s = -V_{sat}$.
==**Un A.O. idéal est caractérisé par des courants d'entrée nuls et par une différence de potentiel $\epsilon$ nulle entre ses deux entrées en régime linéaire. Sa caractéristique de transfert est donnée par la [[#^figure2|figure 2]].**==
Remarques :
- Le qualificatif linéaire signifie que nous pourrons appliquer les lois de l'électrocinétique linéaire à un circuit ne contenant que des composants linéaires et des amplificateurs opérationnels idéaux en régime linéaire.
- Les alimentations ne sont pas représentées sur la [[#^figure1|figure 1]]. Des courants, qui ne figurent pas sur le schéma, arrivent et partent de la masse par les alimentations. Il ne faut pas écrire : « $i_+ + i_- = i_s$ » pour un amplificateur opérationnel ainsi représenté.

==**Amplificateur opérationnel réel**== :
Les amplificateurs opérationnels rassemblent sur une surface de quelques millimètres carrés de silicium une dizaine de transistors, de résistors et de condensateurs.
==**L'amplificateur opérationnel réel est un composant dont les caractéristiques sont proches de celles de l'amplificateur opérationnel idéal.**==
Un amplificateur opérationnel est présenté généralement sous la forme d'un boîtier à huit broches ([[#^figure3|fig. 3]]). ==**Seules cinq d'entre elles nous intéressent : l'alimentation positive, notée $+V_{cc}$, l'alimentation négative, notée $-V_{cc}$, les deux entrées inverseuse et non inverseuse, notées - et + et la sortie.**==
==**Remarquons qu'il n'y a aucune borne prévue pour une masse éventuelle sur ce boîtier.**==

==**Montage amplificateur linéaire**== :
Un montage amplificateur linéaire (réalisé, par exemple, avec un A.O.) peut être représenté, en régime sinusoïdal forcé, par une « boîte noire » possédant deux bornes d'entrée et deux bornes de sortie. Vu du générateur d'entrée, il est équivalent à une impédance $\underline{Z}_e$ (impédance d'entrée) et vu de la sortie à un générateur de f.e.m. $\underline{H}\,\underline{v}_e$ ($\underline{H}$ fonction de transfert de l'amplificateur) et d'impédance $\underline{Z}_s$ (impédance de sortie) ([[#^figure4|fig. 4]]).
==**Le cas idéal correspond à $\underline{H}$ réel indépendant de la fréquence, $\underline{Z}_e$ infini et $\underline{Z}_s$ nul**== ([[#^figure5|fig. 5]]). Dans ces conditions, le circuit ne déforme pas les signaux quelles que soient leurs fréquences. En outre, il ne consomme pas de puissance en entrée et fournit une puissance arbitraire en sortie.

> [!note] Étude expérimentale d'un amplificateur non inverseur
> Réalisons le montage d'un amplificateur non inverseur représenté sur la [[#^figure7|figure 7]]. Le générateur de fréquence émet des signaux sinusoïdaux de fréquence $f$.
> D'après l'étude théorique [[#^theo1|précédente]], le montage réalisé est un amplificateur non inverseur d'amplification $A_v = 11$, d'impédance d'entrée infinie d'impédance et de sortie nulle.
> Premières observations :
> Nous remarquons sur la [[#^figure8|figure 8]] que le signal de sortie est sensiblement sinusoïdal, de même fréquence que le signal d'entrée et d'amplitude 5,5 V. Le tracé en mode $XY$ ([[#^figure9|fig. 9]]) est un segment de droite dont la pente est de l'ordre de 11.
> Les tensions $v_s$ et $v_e$ sont donc proportionnelles. Le montage réalise effectivement une amplification $A_v \approx 11$.
> Les remarques précédentes ne s'appliquent plus à la totalité du signal sur les figures [[#^figure10|10]] et [[#^figure11|11]].
> Nous observons un phénomène de saturation de la tension de sortie de l'amplificateur opérationnel à des tensions voisines des tensions d'alimentation +15 V et –15 V.
> Le fonctionnement du montage est alors non linéaire.
> Pour des fréquences d'entrée plus élevées, les choses sont différentes :
> À 10 kHz ([[#^figure12|fig. 12]]), le signal de sortie est toujours sinusoïdal, d'amplitude de 5,5 V, mais il est en léger retard par rapport au signal d'entrée. Le déphasage est surtout visible en mode XY, où la courbe est une ellipse ([[#^figure13|fig. 13]]).
> À 100 kHz ([[#^figure14|fig. 14]]), le signal de sortie a une forme proche d'un signal triangulaire. Ce phénomène s'appelle la triangularisation. Le fonctionnement du montage est non linéaire. La courbe en mode $XY$ ([[#^figure15|fig. 15]]), qui est très différente d'une ellipse, confirme cette analyse. Cette non linéarité (triangularisation) est liée à la vitesse de balayage (en anglais : slew rate) $\sigma$ de l'amplificateur opérationnel : la tension de sortie $v_s$ ne peut plus suivre les variations trop rapides de $v_e$ : $\left|\dfrac{dv_s}{dt}\right| < \sigma$, de l'ordre de $0,5 V.\mu s^{-1}$.

> [!note] Amplificateur non inverseur : Caractéristique statique de transfert
> En remplaçant le G.B.F. par une alimentation continue, traçons point par point la courbe $V_s$ fonction de $V_e$ en régime indépendant du temps ([[#^figure16|fig. 16]]). Elle peut aussi être visualisée sur un oscilloscope utilisé en mode $XY$ à l'aide d'un générateur basse fréquence à une fréquence faible $(< 100 Hz)$. Nous vérifions ainsi la proportionnalité entre $V_s$ et $V_e$ dans le domaine linéaire.
> En fait, $V_s$ ne s'annule pas exactement pour $V_e = 0$. La valeur effective de $v_e$ (de l'ordre de la dizaine de millivolts) qui annule $V_s$ s'appelle tension de décalage en entrée (input offset voltage) ([[#^figure17|fig. 17]]) ; elle est notée $V_d$.

> [!note] Amplificateur non inverseur : Impédances d'entrée et de sortie
> Pour mesurer l'impédance d'entrée du circuit étudié, réalisons le montage représenté sur la [[#^figure18|figure 18]].
> Nous ne devons pas placer le multimètre, ou l'oscilloscope, au niveau de l'entrée de l'amplificateur non inverseur, car l'impédance d'entrée de ce dernier est a priori très grande, même devant l'impédance d'entrée de ces deux appareils (infinie si l'amplificateur opérationnel était idéal) ([[#^figure19|fig. 19]]).
> <mark style="color: red">L'impédance d'entrée de ce montage amplificateur non inverseur peut être considérée comme infinie.</mark>
> Pour mesurer l'impédance de sortie du circuit étudié, réalisons le montage représenté sur la [[#^figure20|figure 20]]. Observons les résultats de la [[#^figure21|figure 21]].
> Pour une résistance de charge $R$ suffisante, le signal sinusoïdal de sortie ne subit aucune modification visible. L'impédance de sortie du montage est très faible devant $R$. Cette impédance de sortie est inférieure à l'ohm.
> En revanche, lorsque la résistance de charge $R$ est faible, la saturation de sortie étant proportionnelle à la résistance R, nous mettons en évidence une saturation du courant de sortie de l'amplificateur opérationnel, égale ici à environ 17 mA $(|i_s| < I_{sat} \approx 17 mA)$. (Cette limitation est souvent de l'ordre de $I_{sat} = 20 mA$.)
> La saturation en courant est voulue par le constructeur pour limiter la dissipation thermique dans l'amplificateur opérationnel et éviter sa destruction lors d'un court-circuit en sortie.
> Lorsque l'A.O. n'est pas saturé en courant, l'amplificateur non inverseur fonctionne en régime linéaire avec une résistance de sortie très faible, inférieure à l'ohm.

> [!note] Amplificateur non inverseur : Conclusion sur les limites de linéarité du montage
> Nous avons observé trois causes de non-linéarité des montages à amplificateur opérationnel :
> - la saturation en tension : $|v_s| \leqslant V_{sat}$ (voisine de 15 V, pour une alimentation –15 V, +15 V) ;
> - la saturation en courant : $|i_s| \leqslant I_{sat}$ (voisine de 20 mA) ;
> - la vitesse de balayage : $\left|\dfrac{dv_s}{dt}\right| \leqslant \sigma$ (voisine de $0,5 V.\mu s^{-1}$).
> 
> L'amplitude de la tension délivrée par les générateurs basse fréquence et les valeurs des composants utilisés doivent être choisies de façon à minimiser les défauts de linéarité dans les montages amplificateurs ou les filtres que nous réaliserons. En particulier, les résistances doivent être choisies dans l'intervalle 1 kΩ, 1 MΩ.

> [!note] Amplificateur non inverseur : Stabilité du montage
> En régime linéaire, les entrées inverseuse et non inverseuse d'un amplificateur idéal semblent équivalentes.
> Observons le résultat obtenu en permutant les entrées + et – de l'amplificateur opérationnel du circuit initial ([[#^figure7|fig. 7]]) représenté ci-dessous ([[#^figure22|fig. 22]]).
> Pour une tension d'entrée sinusoïdale d'amplitude 0,5 V, la tension de sortie est constante et égale à environ +15 V ou –15 V. Pour une tension d'entrée de 5 V, nous observons la [[#^figure23|figure 23]].
> Les résultats sont totalement différents de ceux qui avaient été obtenus avec le circuit initial : la tension de sortie $v_s$ prend successivement les valeurs $+V_{sat}$ et $-V_{sat}$, et passe d'une valeur à l'autre avec une pente constante égale à la vitesse de balayage.
> <mark style="color: red">Les entrées inverseuse et non inverseuse d'un amplificateur opérationnel ne sont pas équivalentes.</mark>
> Pour que le montage soit stable, il est nécessaire que le nœud intermédiaire du pont de résistances soit relié à l'entrée inverseuse.
> Cette condition est très générale :
> <mark style="color: red">La boucle de retour, ou boucle de rétroaction (purement résistive), doit revenir sur l'entrée inverseuse pour qu'un montage à amplificateur opérationnel soit stable.</mark>

> [!note] Amplificateur non inverseur : Montage suiveur
> Le montage suiveur correspond au cas particulier où $R_1$ infinie et $R_2$ nulle ([[#^figure24|fig. 24]]).
> Nous avons alors $v_s \approx v_e$ dans le domaine de la bande passante à gain nul de l'amplificateur opérationnel (soit $f < f_0 = 1 MHz$ pour le 741) à condition que son fonctionnement soit linéaire.
> Ce montage est un adaptateur d'impédance : son impédance d'entrée est quasiment infinie et son impédance de sortie est quasiment nulle.
> Nous l'utiliserons dans tous les montages nécessitant une grande impédance de charge.
> C'est aussi un amplificateur de puissance, d'amplification en puissance très élevée, puisque sa puissance d'entrée est pratiquement nulle $(i_+ \approx 0)$ alors que sa puissance de sortie est finie et non nulle. Avec $V_e = 10 V$ (tension continue) et une résistance de charge de $R_c = 1 k\Omega$ (valeur minimale de résistance avec laquelle il est conseillé de travailler pour éviter une saturation en courant de sortie), cette puissance est égale 100 mW.
> Pour des signaux sinusoïdaux de fréquences variant de 0 Hz à $10^5$ Hz et d'amplitudes comprises entre 0 V et 10 V, le fonctionnement de ce montage est toujours linéaire : $V_s = V_e$. Aucune des saturations précédentes ($V_{sat}$, $I_{sat}$ et $\sigma$) n'est atteinte.

> [!note] Étude expérimentale d'un amplificateur inverseur
> Réalisons le circuit représenté sur la [[#^figure27|figure 27]] ($R$ est quelconque, à la limite $R = 0$).
> D'après l'étude [[#^theo2|précédente]], le montage doit être un amplificateur inverseur d'amplification $H = -2,2$ et d'impédance d'entrée $R_e = 10 k\Omega$.
> Nous pouvons successivement, en suivant le même protocole opératoire que pour l'amplificateur non inverseur :
> - tracer la caractéristique de transfert statique ([[#^figure26|fig. 26]]) à basse fréquence ;
> - constater que l'amplification n'a plus la valeur prévue au-delà d'une certaine fréquence ;
> - mesurer les impédances d'entrée et de sortie ($R_e \approx 10 k\Omega$, $R_s$ non mesurable) ;
> - chercher les limites de linéarité ;
> - vérifier que le montage obtenu en permutant les entrées + et – est instable.
> Les résultats sont en bon accord avec la théorie.

> [!note] Sommateur de tensions à impédances d'entrée infinies
> Le défaut principal du montage [[#^figure28|précédent]] est dû à ses impédances d'entrée finies : $R_1$ pour le signal $v_1$ et $R_2$ pour le signal $v_2$. Si les sources nécessitent une impédance de charge élevée, nous devons intercaler un montage suiveur de façon à adapter les impédances du sommateur d'entrée ([[#^figure29|fig. 29]] ; $R$ étant toujours quelconque).

> [!note] Étude expérimentale d'un sommateur de tensions
> Réalisons le montage de la [[#^figure30|figure 30]].
> Si deux générateurs délivrent des signaux sinusoïdaux de fréquences $f_1$ et $f_2$ voisines, nous observons un phénomène de battements : le signal de sortie oscille avec la fréquence $f_1 + f_2$, et son amplitude est modulée à la fréquence $\frac{|f_1 - f_2|}{2}$ ([[#^figure31|fig. 31]]).
> Ce phénomène peut être utilisé pour comparer un signal de fréquence inconnue à un signal de fréquence connue de valeur voisine.
> Remarque : La synchronisation de la base de temps de l'oscilloscope sur le phénomène de battements nécessite souvent de modifier le seuil de déclenchement.

==**Comparateur de tension**== :
==**Un comparateur de tension est un composant à deux entrées et une sortie, dont la fonction est de fournir une tension de sortie $v_s$ fonction du signe de la tension différentielle d'entrée $v_{de} = v_2 – v_1$.**==
La représentation symbolique d'un comparateur de tension est donnée sur la [[#^figure33|figure 33]].
Parce que la tension de sortie $v_s$ d'un comparateur ne dépend que du signe de la tension différentielle d'entrée $v_{de}$, la relation entre $v_s$ et $v_{de}$ est une relation non linéaire.

> [!note] Comparateurs simples à amplificateurs opérationnels
> ==**Un comparateur simple est réalisable à l'aide d'un amplificateur opérationnel en boucle ouverte.
> La tension de référence $V_{ref}$ est appliquée sur l'une des entrées de l'amplificateur opérationnel et la tension d'entrée $v_e$ sur l'autre.**==
> Rappelons que la tension différentielle d'entrée de l'amplificateur opérationnel est : $v_{de} = v_+ - v_-$.
> Nous disposons de deux types de comparateurs simples selon que le signal d'entrée est introduit sur l'entrée non inverseuse (comparateur simple non inverseur) ou sur l'entrée inverseuse (comparateur simple inverseur) de l'amplificateur opérationnel ([[#^figure34|fig. 34]]).
> Pour les deux types de comparateurs, les tensions de sortie sont les tensions de saturation $V_H = +V_{sat}$ et $V_B = -V_{sat}$ de l'amplificateur opérationnel.
> Leurs caractéristiques $v_s = f(v_e)$ ([[#^figure35|fig. 35]]) ne sont que les traductions graphiques des implications suivantes : $v_{de} > 0$ entraîne $v_s = +V_{sat}$ et $v_{de} < 0$ entraîne $v_s = -V_{sat}$.
> Pour un même signal d'entrée $v_e(t)$, la tension de sortie $v_s(t)$ d'un comparateur simple non inverseur et celle d'un comparateur simple inverseur sont données [[#^figure36|figure 36]] (Chronogrammes).

> [!note] Étude expérimentale d'un comparateur de tension
> Réalisons le comparateur non inverseur représenté sur la [[#^figure37|figure 37]]. La tension de référence $V_{ref}$ est obtenue par l'intermédiaire d'un diviseur de tension utilisant le potentiomètre (P).
> Traçons alors la caractéristique de transfert statique $V_s = f(V_e)$ du montage à l'aide d'une alimentation stabilisée. La courbe obtenue est bien conforme à l'étude théorique ([[#^figure35|fig. 35a]]).
> Remplaçons l'alimentation stabilisée par un G.B.F. et réglons-le pour qu'il délivre une tension sinusoïdale basse fréquence $(f < 200 Hz)$ et d'amplitude $V_e$ inférieure à $|V_{ref}|$ . L'oscilloscope étant utilisé en bicourbe et en mode DC, observons les courbes obtenues ([[#^figure38|fig. 38]]). Commutons ensuite l'oscilloscope en mode XY. Nous observons un segment de droite horizontal.
> La tension différentielle d'entrée $v_{de}$ est, dans ces conditions, toujours négative. En conséquence, l'amplificateur opérationnel reste saturé négativement à : $v_s = -V_{sat}$.
> Faisons croître l'amplitude $v_{e_m}$ de la tension d'entrée et observons les modifications en utilisant l'oscilloscope en bicourbe. Faisons ensuite varier $V_{ref}$ et observons les modifications des courbes obtenues.
> Quand $v_{e_m} \geqslant |V_{ref}|$, l'amplificateur opérationnel commute de $-V_{sat}$ et $+V_{sat}$, quand $v_e(t)$ prend la valeur $V_{ref}$ par valeurs croissantes et commute de $+V_{sat}$ et $-V_{sat}$, quand $v_e(t)$ prend la valeur $V_{ref}$ par valeurs décroissantes ([[#^figure39|fig. 39]]).

> [!note] Défauts du comparateur réel
> Les capacités qui se trouvent à l'intérieur de l'amplificateur opérationnel imposent à la tension de sortie une vitesse de balayage finie $\left|\dfrac{du_s}{dt}\right| \leqslant \sigma$.
> La valeur maximale $\sigma$ de cette vitesse de balayage est appelée slew rate.
> Comme le montrent les courbes des figures [[#^figure40|40]] et [[#^figure41|41]], ce phénomène perturbe le fonctionnement du comparateur dès que la période n'est plus grande devant le temps de montée. Sur la figure 41, nous pouvons estimer $\sigma \approx \frac{30 V}{0,3 ms}$ soit : $\sigma \approx 10^{5}\, V . s^{-1}$.
> Il existe d'autres imperfections, visibles essentiellement pour un signal d'entrée de faible amplitude. Pour les faibles valeurs de $\epsilon$ (typiquement inférieures à 0,1 mV en valeur absolue), un amplificateur opérationnel a un fonctionnement linéaire.
> ==**La valeur finie de la vitesse de balayage $\sigma$ est le plus important facteur de limitation des performances du comparateur simple à amplificateur opérationnel réel.**==

> [!note] Application des comparateurs simples
> Parmi les applications possibles des comparateurs simples, signalons :
> - la détection d'un niveau de tension de référence ;
> - la transformation d'un signal analogique variable en un signal numérique à deux niveaux $v_H$ et $v_B$ permettant son traitement logique.
> 
> Les caractéristiques de commutation d'un comparateur simple à A.O. sont médiocres. Ce type de comparateur doit être réservé pour les traitements de signaux en basse fréquence, au-delà il est nécessaire d'utiliser des circuits intégrés spécialisés.
# Diagrammes
Représentation symbolique d'un amplificateur opérationnel idéal
![[electronique1/attachments-electronique1/figure131.png]]^figure1

Identification des broches d'un amplificateur opérationnel réel (TL081 ou μA741)
![[electronique1/attachments-electronique1/figure133.png]]^figure3

Modélisation d'un amplificateur de tension
![[electronique1/attachments-electronique1/figure134.png]]^figure4

Amplificateur de tension idéal
![[electronique1/attachments-electronique1/figure135.png]]^figure5

Amplificateur non inverseur
![[electronique1/attachments-electronique1/figure136.png]]
Le symbole (triangle avec ∞) sur la figure signifie que l'amplificateur opérationnel est considéré comme idéal. La tension de sortie $v_s$ étant non nulle pour une tension d'entrée $\epsilon$ nulle, le gain $H$ d'un tel amplificateur est bien infini. ^figure6

Circuit d'étude d'un amplificateur non inverseur $(R_c \approx \infty)$
![[electronique1/attachments-electronique1/figure137.png]]
==**Les tensions d'alimentation (+15 V et –15 V) sont définies par rapport à la masse.**== Concrètement, l'alimentation stabilisée comporte trois bornes :
- Une borne 15 V à relier à la broche 7.
- Une borne 0 V à relier à la masse de l'oscilloscope, et donc à celle du G.B.F.
- Une borne –15 V à relier à la broche 4.
==**Attention, il n'y a pas de bornes de masse sur un amplificateur opérationnel.**== ^figure7

 Principe de la mesure de l'impédance d'entrée d'un amplificateur non inverseur
 ![[electronique1/attachments-electronique1/figure148.png]]
 ^figure18

Montage à proscrire
![[electronique1/attachments-electronique1/figure149.png]]^figure19

Principe de la mesure de l'impédance de sortie d'un amplificateur non inverseur
![[electronique1/attachments-electronique1/figure150.png]]^figure20

Les entrées + et – ont été permutées par rapport à la [[#^figure7|figure 7]]
![[electronique1/attachments-electronique1/figure152.png]]^figure22

Montage suiveur
![[electronique1/attachments-electronique1/figure154.png]]^figure24

Amplificateur inverseur
![[electronique1/attachments-electronique1/figure155.png]]^figure25

Montage d'étude de l'amplificateur inverseur
![[electronique1/attachments-electronique1/figure157.png]]^figure27

Sommateur pondéré de tensions
![[electronique1/attachments-electronique1/figure158.png]]^figure28

Sommateur à impédances d'entrée infinies et à impédance de sortie nulle
![[electronique1/attachments-electronique1/figure159.png]]^figure29

Réalisation expérimentale d'un sommateur de tensions
![[electronique1/attachments-electronique1/figure160.png]]^figure30

Le générateur alimente une résistance négative : $u = R_ei$ avec $R_e < 0$
![[electronique1/attachments-electronique1/figure162.png]]^figure32

Représentation symbolique d'un comparateur
![[electronique1/attachments-electronique1/figure163.png]]^figure33

Les deux types de comparateurs simples à A.O. idéal. a. Comparateur non inverseur. b. Comparateur inverseur.
![[electronique1/attachments-electronique1/figure164.png]]^figure34

Montage d'étude d'un comparateur simple non inverseur
![[figure167.png]]^figure37
# Graphiques
Caractéristique d'un amplificateur opérationnel idéal. Lorsque $\epsilon = 0$, $v_s$ est imposée par le circuit extérieur
![[electronique1/attachments-electronique1/figure132.png]]^figure2

Fréquence de travail $f = 500 Hz$, tension en entrée $v_e = 0,5 V$ et oscillographe en mode DC bicourbe
![[electronique1/attachments-electronique1/figure138.png]]^figure8

Fréquence de travail $f = 500 Hz$, tension en entrée $v_e = 0,5 V$ et oscillographe en mode $XY$
![[electronique1/attachments-electronique1/figure139.png]]^figure9

Fréquence de travail $f = 500 Hz$, tension en entrée $v_e = 2 V$ et oscillographe en mode DC bicourbe
![[electronique1/attachments-electronique1/figure140.png]]^figure10

Fréquence de travail $f = 500 Hz$, tension en entrée $v_e = 2 V$ et oscillographe en mode $XY$
![[electronique1/attachments-electronique1/figure141.png]]^figure11

Fréquence de travail $f = 10 kHz$, tension en entrée $v_e = 0,5 V$ et oscillographe en mode DC bicourbe
![[electronique1/attachments-electronique1/figure142.png]]^figure12

Fréquence de travail $f = 10 kHz$, tension en entrée $v_e = 0,5 V$ et oscillographe en mode $XY$
![[electronique1/attachments-electronique1/figure143.png]]^figure13

Fréquence de travail $f = 100 kHz$, tension en entrée $v_e = 0,5 V$ et oscillographe en mode DC bicourbe
![[electronique1/attachments-electronique1/figure144.png]]^figure14

Fréquence de travail $f = 100 kHz$, tension en entrée $v_e = 0,5 V$ et oscillographe en mode $XY$
![[electronique1/attachments-electronique1/figure145.png]]^figure15

Montage non inverseur. Caractéristique de transfert statique
![[electronique1/attachments-electronique1/figure146.png]]^figure16

Mise en évidence de la tension de décalage en entrée d'un amplificateur non inverseur
![[electronique1/attachments-electronique1/figure147.png]]^figure17

Montage non inverseur. Influence de la résistance de charge. Signal d'entrée (0,5 V, 500 Hz)
![[electronique1/attachments-electronique1/figure151.png]]^figure21

Le montage de la [[#^figure22|fig. 22]] est instable. Signal d'entrée (5 V, 500 Hz), entrées + et – inversées
![[electronique1/attachments-electronique1/figure153.png]]^figure23

Montage inverseur. Caractéristique de transfert statique
![[electronique1/attachments-electronique1/figure156.png]]^figure26

Montage sommateur inverseur, somme d'un signal d'amplitude 1 V de fréquence 510 Hz et d'un signal d'amplitude 1,5 V et de fréquence 500 Hz. Remarquons un phénomène de battements de fréquence 10 Hz
![[electronique1/attachments-electronique1/figure161.png]]^figure31

Caractéristiques des deux types de comparateurs simples à A.O. idéal. a. Comparateur non inverseur. b. Comparateur inverseur.
![[electronique1/attachments-electronique1/figure165.png]]^figure35

Réponse $v_s(t)$ d'un comparateur simple à A.O. idéal à une excitation sinusoïdale $v_e(t)$
![[electronique1/attachments-electronique1/figure166.png]]^figure36

L'amplitude de la tension d'entrée $v_e(t)$ est insuffisante pour provoquer le basculement du comparateur
![[figure168.png]]^figure38

Attaqué par une tension sinusoïdale, un comparateur simple non inverseur délivre une tension en créneaux
![[figure169.png]]^figure39

Réponse d'un comparateur simple non inverseur à une excitation sinusoïdale de fréquence 50 Hz et d'amplitude 5 V
![[figure170.png]]^figure40

Réponse d'un comparateur simple non inverseur à une excitation sinusoïdale de fréquence 5 kHz et d'amplitude 5 V
![[figure171.png]]^figure41
# Expériences
> [!warning]
> Voici des exemples de travaux pratiques qui abordent le sujet de ce chapitre : le [lien 1](https://dpnc.unige.ch/tp/elect/doc/TP4.pdf), le [lien 2](https://www.emse.fr/~dutertre/documents/7_TP_AOp_MCP6022_ismin_1A.pdf), le [lien 3](https://geossc.ma/wp-content/uploads/2021/11/TP1_AOP_AZ.pdf), le [lien 4](https://prepanouar.wordpress.com/wp-content/uploads/2020/03/montages-acc80-a.o-2.pdf), le [lien 5](http://olivier.granier.free.fr/PC-Montesquieu445072/cariboost_files/Elec3-aop-1.pdf), le [lien 6](https://fr.scribd.com/document/857262859/TP-3), le [lien 7](http://physiqueensti.free.fr/IMG/pdf/TP24.pdf), le [lien 8](https://staff.univ-batna2.dz/sites/default/files/benacer-saddok/files/tpn02_eln-app_m1_as-aii.pdf), le [lien 9](http://www.matthieurigaut.net/public/sup/tp/tp07_ao.pdf), le [lien 10](http://elearning.univ-dbkm.dz/pluginfile.php/25487/mod_resource/content/1/TP_EApp_M%201_AII_1-converti.pdf), le [lien 11](http://cdelacourphysique.chez.com/TP/AO%20en%20regime%20lineaire3.pdf), le [lien 12](http://agregation.capes.free.fr/tp/25_Aop_lineaire2006.pdf), le [lien 13](http://compilonet.free.fr/ptsi/Cours%20de%20physique/Relec8.pdf), le [lien 14](https://www.yumpu.com/fr/document/read/27983712/tp-cours-amplificateur-opacrationnel-physique-en-sup-4), le [lien 15](http://stephbill.free.fr/tp%20mpi/tp%20steph/tpn11mpinew.pdf), le [lien 16](https://lycee-champollion.fr/IMG/pdf/tp_no1_et_2_-_montages_non_inverseur-_et_suiveur.pdf).
# Autres notes
