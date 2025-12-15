---
titre: "[[10-Champs tournants, machines synchrones et asynchrones]]"
tags:
aliases:
crée: 15-12-2025, 14:23
---
# Formules

# Définitions
> [!note] Champs magnétiques tournants
> - Définitions : ==**Un champ tournant est un champ magnétique $\overrightarrow{B}$, de norme constante, tournant dans l’espace avec une vitesse angulaire $\omega_0$ constante et contrôlable.**==
> - Production de champs tournants : Plusieurs méthodes sont utilisées pour produire des champs tournants. Trois d’entre elles sont citées ci-dessous.
> 	- Rotation d’un électro-aimant ou d’un aimant permanent : L'aimant dans sa rotation entraîne le champ magnétique $\overrightarrow{B}$ qu'il crée. Ce champ tournant peut être mis en évidence par une petite aiguille aimantée montée sur un pivot ([[#^figure1|fig. 1]]).
> 	Lorsque l’aimant est au repos, l’aiguille s’oriente dans le champ magnétique $\overrightarrow{B}$ de l'aimant de telle sorte que son moment magnétique $\overrightarrow{M}$ soit parallèle et de même sens que $\overrightarrow{B}$. Dès que l’aimant tourne, l'aiguille se met à tourner dans le même sens et à la même vitesse que lui. Le mouvement de rotation de l'aiguille est *synchrone* de celui du champ tournant.
> 	- Utilisation de champs magnétiques sinusoïdaux en quadrature spatiale et temporelle : Le dispositif réalisé est représenté sur la [[#^figure2|figure 2]]. Les deux bobines ($B_1$) et ($B_2$) identiques ont leurs axes orthogonaux (quadrature spatiale) et sont alimentées par des courants sinusoïdaux de pulsation $\omega_0$ déphasés de $\frac{\pi}{2}$ (quadrature temporelle). Par un choix convenable de l’origine des temps, les champs magnétiques créés en $O$ s’écrivent respectivement : $B_x = B_0\cos(\omega_0 t)$ et $B_y = B_0\sin(\omega_0 t)$.
> 	Le champ résultant $\overrightarrow{B}(t) = B_0[\cos(\omega_0 t)\overrightarrow{e_x} + \sin(\omega_0 t)\overrightarrow{e_y}]$ est un champ de norme $B_0$ constante tournant dans le plan $(xOy)$ a la vitesse angulaire constante $\omega_0$ autour de l’axe $(Oz)$.
> 	« Lançons » une petite aiguille aimantée placée en $O$ : elle « s’accroche » au champ magnétique et finit par être entraînée à la même vitesse angulaire $\omega_0$ que le champ tournant.
> 	En agissant sur la fréquence des courants alimentant les bobines, on contrôle la vitesse de rotation du champ tournant $\overrightarrow{B}$.
> 	Le dispositif précédent peut être rendu plus efficace en associant aux deux bobines ($B_1$) et ($B_2$) deux nouvelles bobines ($B_{1}^{'}$) et ($B_{2}^{'}$) identiques, placées en séries avec leurs homologues et disposées symétriquement par rapport au point $O$ où l’on désire obtenir le champ tournant ([[#^figure3|fig. 3]]).
> 	- Utilisation d'un champ magnétique sinusoïdal : La bobine $B$, alimentée en courant sinusoïdal, crée en $O$ ([[#^figure4|fig. 4]]) un champ alternatif (supposé sinusoïdal) de direction constante $\overrightarrow{e_x}$ qui s'écrit, par un choix convenable de l'origine des temps : $\overrightarrow{B} = B_0\cos(\omega_0 t)\overrightarrow{e_x}$.
> 	Ce champ peut être analysé ([[#^figure5|fig. 5]]) comme la résultante de deux champs d’amplitudes $\frac{B_0}{2}$ tournants en sens opposés avec respectivement les vitesses angulaires $\omega_0$ et $-\omega_0$ : $\overrightarrow{B} = \frac{B_0}{2}([\cos(\omega_0 t)\overrightarrow{e_x} + \sin(\omega_0 t)\overrightarrow{e_y}] + [\cos(-\omega_0 t)\overrightarrow{e_x} + \sin(-\omega_0 t)\overrightarrow{e_y}])$.
> 	Ce résultat est connu en électrotechnique sous le nom de *théorème de Leblanc*. Cette décomposition est utilisée lors de l’étude des machines fonctionnant en courant alternatif monophasé.
> 	Il est possible de vérifier expérimentalement l’existence des deux champs tournants. En effet, disposons dans l’axe des deux bobines une petite aiguille aimantée. Elle reste immobile, car elle est sollicitée simultanément par deux champs tournants en sens inverse l’un de l’autre.
> 	« Lançons » l’aiguille dans un sens arbitraire : elle « s’accroche » sur la pulsation $\omega_0$, et finit par se mettre à tourner en **synchronisme** avec la composante de $\overrightarrow{B}(t)$ tournant dans le même sens. Arrêtons l'aiguille et lançons-la dans l’autre sens : elle finira alors par tourner en synchronisme avec l’autre composante tournante de $\overrightarrow{B}(t)$.
> 	
> 	Retenons, pour conclure :
> 	==**Des enroulements fixes, régulièrement distribués autour d'un point $O$ et parcourus par un système de courants polyphasés équilibrés produisent en $O$ un champ magnétique tournant.**==

**mettre l'application 1 dans la section autres notes**
# Diagrammes
L'aimant dans sa rotation crée un champ magnétique tournant qui entraîne l'aiguille à la même vitesse $\omega_0$
![[electronique2/attachments-electronique2/figure251.png]]^figure1

Deux champs magnétiques en quadrature spatiale et temporelle créent un champ tournant $\overrightarrow{B}$
![[electronique2/attachments-electronique2/figure252.png]]^figure2

En doublant les champs magnétiques en quadrature spatiale et temporelle, on double l'amplitude du champ tournant ; la vitesse de rotation angulaire du champ est inchangée
![[electronique2/attachments-electronique2/figure253.png]]^figure3

Création d'un champ sinusoïdal
![[electronique2/attachments-electronique2/figure254.png]]^figure4

Un champ sinusoïdal $\overrightarrow{B}(t)$ est la résultante de deux champs $\overrightarrow{B_1}(t)$ et $\overrightarrow{B_2}(t)$ de mêmes amplitudes et tournant en sens inverse
![[electronique2/attachments-electronique2/figure255.png]]^figure5
# Graphiques

# Expériences

# Autres notes
