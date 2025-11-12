---
titre: "[[07-L'amplificateur opérationnel. Le modèle idéal]]"
tags:
aliases:
crée: 12-11-2025, 19:41
---
# Formules

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
# Diagrammes
Représentation symbolique d’un amplificateur opérationnel idéal
![[figure131.png]]^figure1

Identification des broches d’un amplificateur opérationnel réel (TL081 ou μA741)
![[figure133.png]]^figure3

Modélisation d’un amplificateur de tension
![[figure134.png]]^figure4

Amplificateur de tension idéal
![[figure135.png]]^figure5
# Graphiques
Caractéristique d’un amplificateur opérationnel idéal. Lorsque $\epsilon = 0$, $v_s$ est imposée par le circuit extérieur
![[figure132.png]]^figure2
# Expériences

# Autres notes
