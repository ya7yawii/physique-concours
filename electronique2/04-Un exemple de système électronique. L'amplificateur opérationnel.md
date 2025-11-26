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
# Diagrammes
Quadripôle passif
![[electronique2/attachments-electronique2/figure43.png]]^figure1

Représentation de l'amplificateur opérationnel idéal. Les bornes d'alimentation $+V_{cc}$ et $-V_{cc}$ ne sont pas représentés
![[electronique2/attachments-electronique2/figure44.png]]^figure2
# Graphiques
Caractéristique de transfert de l'amplificateur opérationnel idéal
![[electronique2/attachments-electronique2/figure45.png]]^figure3

Caractéristique de transfert statique
![[electronique2/attachments-electronique2/figure46.png]]^figure4

Gain et déphasage du $\mu A741$ en fonction de la fréquence. Dans le domaine de fréquences usuelles (0 MHz à 1 MHz), le 741 se comporte comme un passe-bas du premier ordre
![[electronique2/attachments-electronique2/figure47.png]]^figure5
# Expériences

# Autres notes
