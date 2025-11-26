---
titre: "[[04-Un exemple de système électronique. L'amplificateur opérationnel]]"
tags:
aliases:
crée: 26-11-2025, 15:28
---
# Formules

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
# Diagrammes
Quadripôle passif
![[electronique2/attachments-electronique2/figure43.png]]^figure1
# Graphiques

# Expériences

# Autres notes
