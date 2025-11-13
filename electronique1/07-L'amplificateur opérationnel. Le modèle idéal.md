---
titre: "[[07-L'amplificateur opérationnel. Le modèle idéal]]"
tags:
aliases:
crée: 12-11-2025, 19:41
---
# Formules
> [!note] Étude théorique d'un amplificateur non inverseur
> Considérons le montage représenté sur la [[#^figure6|figure 6]] avec un A.O. supposé idéal $(i_+ = i_- = 0)$. Faisons l’hypothèse du régime linéaire $(\epsilon = 0)$ que nous justifierons ultérieurement. Comme $i_-$ est nul, le potentiel de l’entrée inverseuse est donné par la formule du pont diviseur, soit : $v_- = \frac{R_1}{R_1 + R_2}v_s$. D'où $v_s = (1 + \frac{R_2}{R_1})v_e$, puisque'en régime linéaire $v_e = v_+ = v_-$. Le montage étudié est un amplificateur de tension non inverseur ($v_s$ et $v_e$ sont de mêmes signes) d’amplification : $H = 1 + \frac{R_2}{R_1}$. Son impédance d’entrée est infinie $(i_e = 0)$ et son impédance de sortie est nulle ($v_s$ indépendant de $i_s$).
> Remarque : Même si le courant de sortie $i_s$ de l’amplificateur non inverseur est nul, un courant non nul $i$ sort de l’amplificateur opérationnel.
^theo1
# Définitions
==**Amplificateur opérationnel idéal**== :
L’amplificateur opérationnel (A.O.) idéal est un composant théorique possédant trois bornes : l’entrée inverseuse, notée -, l’entrée non inverseuse, notée + et la sortie. Il est représenté symboliquement par la [[#^figure1|figure 1]].
Aucun courant n’arrive par les entrées : $i_+ = i_- = 0$. En revanche, un courant $i_s$ qui dépend des circuits extérieurs peut sortir (ou entrer) par la sortie.
Un amplificateur opérationnel idéal peut fonctionner suivant deux régimes :
- un régime linéaire pour lequel $\epsilon = 0$ et $v_s$ fixé par le reste du circuit, compte tenu de la relation $\epsilon = 0$ et dans la limite où $v_s$ ne dépasse pas des valeurs fixées par les alimentations $V_{sat}^- < v_s < V_{sat}^+$ ;
- un régime non linéaire pour lequel la tension de sortie $v_s$ de l’amplificateur prend une des valeurs limites $V_{sat}^+$ ou $V_{sat}^-$. Ainsi, lorsque $\epsilon > 0$, $v_s = V_{sat}^+$ tension de saturation positive et lorsque $\epsilon < 0$, $v_s = V_{sat}^-$ tension de saturation négative. En général, $V_{sat}^- = -V_{sat}^+$, si bien que si $\epsilon > 0$, alors $v_s = V_{sat}$ et si $\epsilon < 0$, alors $v_s = -V_{sat}$.
==**Un A.O. idéal est caractérisé par des courants d’entrée nuls et par une différence de potentiel $\epsilon$ nulle entre ses deux entrées en régime linéaire. Sa caractéristique de transfert est donnée par la [[#^figure2|figure 2]].**==
Remarques :
- Le qualificatif linéaire signifie que nous pourrons appliquer les lois de l’électrocinétique linéaire à un circuit ne contenant que des composants linéaires et des amplificateurs opérationnels idéaux en régime linéaire.
- Les alimentations ne sont pas représentées sur la [[#^figure1|figure 1]]. Des courants, qui ne figurent pas sur le schéma, arrivent et partent de la masse par les alimentations. Il ne faut pas écrire : « $i_+ + i_- = i_s$ » pour un amplificateur opérationnel ainsi représenté.

==**Amplificateur opérationnel réel**== :
Les amplificateurs opérationnels rassemblent sur une surface de quelques millimètres carrés de silicium une dizaine de transistors, de résistors et de condensateurs.
==**L’amplificateur opérationnel réel est un composant dont les caractéristiques sont proches de celles de l’amplificateur opérationnel idéal.**==
Un amplificateur opérationnel est présenté généralement sous la forme d’un boîtier à huit broches ([[#^figure3|fig. 3]]). ==**Seules cinq d’entre elles nous intéressent : l’alimentation positive, notée $+V_{cc}$, l’alimentation négative, notée $-V_{cc}$, les deux entrées inverseuse et non inverseuse, notées - et + et la sortie.**==
==**Remarquons qu’il n’y a aucune borne prévue pour une masse éventuelle sur ce boîtier.**==

==**Montage amplificateur linéaire**== :
Un montage amplificateur linéaire (réalisé, par exemple, avec un A.O.) peut être représenté, en régime sinusoïdal forcé, par une « boîte noire » possédant deux bornes d’entrée et deux bornes de sortie. Vu du générateur d’entrée, il est équivalent à une impédance $\underline{Z}_e$ (impédance d’entrée) et vu de la sortie à un générateur de f.e.m. $\underline{H}\,\underline{v}_e$ ($\underline{H}$ fonction de transfert de l’amplificateur) et d’impédance $\underline{Z}_s$ (impédance de sortie) ([[#^figure4|fig. 4]]).
==**Le cas idéal correspond à $\underline{H}$ réel indépendant de la fréquence, $\underline{Z}_e$ infini et $\underline{Z}_s$ nul**== ([[#^figure5|fig. 5]]). Dans ces conditions, le circuit ne déforme pas les signaux quelles que soient leurs fréquences. En outre, il ne consomme pas de puissance en entrée et fournit une puissance arbitraire en sortie.

> [!note] Étude expérimentale d'un amplificateur non inverseur
> Réalisons le montage d’un amplificateur non inverseur représenté sur la [[#^figure7|figure 7]]. Le générateur de fréquence émet des signaux sinusoïdaux de fréquence $f$.
> D’après l’étude théorique [[#^theo1|précédente]], le montage réalisé est un amplificateur non inverseur d’amplification $A_v = 11$, d’impédance d’entrée infinie d’impédance et de sortie nulle.
> Premières observations :
> Nous remarquons sur la [[#^figure8|figure 8]] que le signal de sortie est sensiblement sinusoïdal, de même fréquence que le signal d’entrée et d’amplitude 5,5 V. Le tracé en mode $XY$ ([[#^figure9|fig. 9]]) est un segment de droite dont la pente est de l’ordre de 11.
> Les tensions $v_s$ et $v_e$ sont donc proportionnelles. Le montage réalise effectivement une amplification $A_v \approx 11$.
> Les remarques précédentes ne s’appliquent plus à la totalité du signal sur les figures [[#^figure10|10]] et [[#^figure11|11]].
> Nous observons un phénomène de saturation de la tension de sortie de l’amplificateur opérationnel à des tensions voisines des tensions d’alimentation +15 V et –15 V.
> Le fonctionnement du montage est alors non linéaire.
> Pour des fréquences d'entrée plus élevées, les choses sont différentes :
> À 10 kHz ([[#^figure12|fig. 12]]), le signal de sortie est toujours sinusoïdal, d’amplitude de 5,5 V, mais il est en léger retard par rapport au signal d’entrée. Le déphasage est surtout visible en mode XY, où la courbe est une ellipse ([[#^figure13|fig. 13]]).
> À 100 kHz ([[#^figure14|fig. 14]]), le signal de sortie a une forme proche d’un signal triangulaire. Ce phénomène s’appelle la triangularisation. Le fonctionnement du montage est non linéaire. La courbe en mode $XY$ ([[#^figure15|fig. 15]]), qui est très différente d’une ellipse, confirme cette analyse. Cette non linéarité (triangularisation) est liée à la vitesse de balayage (en anglais : slew rate) $\sigma$ de l’amplificateur opérationnel : la tension de sortie $v_s$ ne peut plus suivre les variations trop rapides de $v_e$ : $\left|\dfrac{dv_s}{dt}\right| < \sigma$, de l'ordre de $0,5 V.\mu s^{-1}$.

> [!note] Amplificateur non inverseur : Caractéristique statique de transfert
> En remplaçant le G.B.F. par une alimentation continue, traçons point par point la courbe $V_s$ fonction de $V_e$ en régime indépendant du temps ([[#^figure16|fig. 16]]). Elle peut aussi être visualisée sur un oscilloscope utilisé en mode $XY$ à l’aide d’un générateur basse fréquence à une fréquence faible $(< 100 Hz)$. Nous vérifions ainsi la proportionnalité entre $V_s$ et $V_e$ dans le domaine linéaire.
> En fait, $V_s$ ne s’annule pas exactement pour $V_e = 0$. La valeur effective de $v_e$ (de l’ordre de la dizaine de millivolts) qui annule $V_s$ s’appelle tension de décalage en entrée (input offset voltage) ([[#^figure17|fig. 17]]) ; elle est notée $V_d$.

> [!note] Amplificateur non inverseur : Impédances d’entrée et de sortie
> Pour mesurer l’impédance d’entrée du circuit étudié, réalisons le montage représenté sur la [[#^figure18|figure 18]].
> Nous ne devons pas placer le multimètre, ou l’oscilloscope, au niveau de l’entrée de l’amplificateur non inverseur, car l’impédance d’entrée de ce dernier est a priori très grande, même devant l’impédance d’entrée de ces deux appareils (infinie si l’amplificateur opérationnel était idéal) ([[#^figure19|fig. 19]]).
> <mark style="color: red">L’impédance d’entrée de ce montage amplificateur non inverseur peut être considérée comme infinie.</mark>


# Diagrammes
Représentation symbolique d’un amplificateur opérationnel idéal
![[figure131.png]]^figure1

Identification des broches d’un amplificateur opérationnel réel (TL081 ou μA741)
![[figure133.png]]^figure3

Modélisation d’un amplificateur de tension
![[figure134.png]]^figure4

Amplificateur de tension idéal
![[figure135.png]]^figure5

Amplificateur non inverseur
![[figure136.png]]
Le symbole (triangle avec ∞) sur la figure signifie que l’amplificateur opérationnel est considéré comme idéal. La tension de sortie $v_s$ étant non nulle pour une tension d’entrée $\epsilon$ nulle, le gain $H$ d’un tel amplificateur est bien infini. ^figure6

Circuit d’étude d’un amplificateur non inverseur $(R_c \approx \infty)$
![[figure137.png]]
==**Les tensions d’alimentation (+15 V et –15 V) sont définies par rapport à la masse.**== Concrètement, l’alimentation stabilisée comporte trois bornes :
- Une borne 15 V à relier à la broche 7.
- Une borne 0 V à relier à la masse de l’oscilloscope, et donc à celle du G.B.F.
- Une borne –15 V à relier à la broche 4.
==**Attention, il n’y a pas de bornes de masse sur un amplificateur opérationnel.**== ^figure7

 Principe de la mesure de l’impédance d’entrée d’un amplificateur non inverseur
 ![[figure148.png]]
 ^figure18

Montage à proscrire
![[figure149.png]]^figure19
# Graphiques
Caractéristique d’un amplificateur opérationnel idéal. Lorsque $\epsilon = 0$, $v_s$ est imposée par le circuit extérieur
![[figure132.png]]^figure2

Fréquence de travail $f = 500 Hz$, tension en entrée $v_e = 0,5 V$ et oscillographe en mode DC bicourbe
![[figure138.png]]^figure8

Fréquence de travail $f = 500 Hz$, tension en entrée $v_e = 0,5 V$ et oscillographe en mode $XY$
![[figure139.png]]^figure9

Fréquence de travail $f = 500 Hz$, tension en entrée $v_e = 2 V$ et oscillographe en mode DC bicourbe
![[figure140.png]]^figure10

Fréquence de travail $f = 500 Hz$, tension en entrée $v_e = 2 V$ et oscillographe en mode $XY$
![[figure141.png]]^figure11

Fréquence de travail $f = 10 kHz$, tension en entrée $v_e = 0,5 V$ et oscillographe en mode DC bicourbe
![[figure142.png]]^figure12

Fréquence de travail $f = 10 kHz$, tension en entrée $v_e = 0,5 V$ et oscillographe en mode $XY$
![[figure143.png]]^figure13

Fréquence de travail $f = 100 kHz$, tension en entrée $v_e = 0,5 V$ et oscillographe en mode DC bicourbe
![[figure144.png]]^figure14

Fréquence de travail $f = 100 kHz$, tension en entrée $v_e = 0,5 V$ et oscillographe en mode $XY$
![[figure145.png]]^figure15

Montage non inverseur. Caractéristique de transfert statique
![[figure146.png]]^figure16

Mise en évidence de la tension de décalage en entrée d’un amplificateur non inverseur
![[figure147.png]]^figure17
# Expériences

# Autres notes
