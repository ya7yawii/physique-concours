---
titre: "[[08-Fonctions de transfert des réseaux linéaires]]"
tags:
aliases:
crée: 14-11-2025, 14:38
---
# Formules
> [!note] Réponse d'un circuit (R, C) en régime harmonique
> Étudions le circuit (R, C ) représenté sur la [[#^figure1|figure 1]], alimenté par un générateur sinusoïdal. Nous définissons la tension d’entrée $u_1(t)$ et la tension de sortie $u_2(t)$. Nous l’étudions ici en régime forcé et en sortie ouverte : aucun dipôle n’est branché entre les bornes de sortie et donc $i_2 = 0$.
> Nous reconnaissons le diviseur de tension, ce qui permet d’écrire : $\displaystyle\underline{u}_{2m} = \frac{\frac{1}{jC\omega}}{R + \frac{1}{jC\omega}}\underline{u}_{1m}$.
> La [[#^info1|fonction de transfert]] est le rapport des amplitudes complexes de $u_2$ et $u_1$ : $\underline{H}(j\omega) = \frac{\underline{u}_{2m}}{\underline{u}_{1m}}$. Le module $H(\omega) = |\underline{H}(j\omega)|$ (grandeur positive) et le déphasage de $u_2(t)$ par rapport à $u_1(t)$, $\varphi(\omega)$ défini par $\underline{H}(j\omega) = H(\omega)e^{j\varphi(\omega)}$, sont fonction de la fréquence.
> Ce circuit est appelé filtre car il transmet différemment des signaux harmoniques de fréquences différentes.
> Forme réduite : Notons $x = \frac{\omega}{\omega_0} = RC\omega$ la pulsation réduite du filtre. Avec cette notation la fonction de transfert devient : $\underline{H}(jx) = \frac{1}{1 + jx}$.
> Définition du gain : Le rapport $H(\omega)$ des amplitudes est généralement exprimé dans une échelle logarithmique. Par définition, le gain en tension, exprimé en décibels, est : $G_{dB} = 20\log H$ ($\log X$ étant le logarithme décimal du nombre $X$). Pour le circuit étudié : $G(dB) = -10\log(1 + x^{2})$. L’utilisation de l’échelle logarithmique permet de traiter avec autant de précision les faibles et les fortes amplitudes : la multiplication par 10 de $H$ se traduit par un accroissement du gain de 20 dB, quelle que soit sa valeur initiale. Signalons enfin que l’œil et l’oreille ont une sensibilité beaucoup plus proche d’une échelle logarithmique que d’une échelle linéaire.

# Définitions
> [!note] Quadripôle
> Un quadripôle ([[#^figure2|fig. 2]]) est un ensemble qui présente deux bornes d’entrée et deux bornes de sortie.
> La fonction de transfert d’un quadripôle ne peut être définie que si le système est stable. A priori, tout quadripôle passif est stable (c’est-à-dire que les tensions ne divergent pas).
> Si nous étudions les tensions : $\underline{H}(j\omega) = \frac{\underline{u}_{2m}}{\underline{u}_{1m}}$.
> Un filtre est un quadripôle conçu pour transmettre sélectivement les diverses fréquences de la grandeur harmonique.
> Si le quadripôle est linéaire, $\underline{H}(j\omega)$ peut toujours s’écrire sous la forme : $\underline{H}(j\omega) = \frac{N(j\omega)}{D(j\omega)}$, $N$ et $D$ étant des polynômes à coefficients réels. L'ordre du filtre est égal au degré le plus élevé de ces deux polynômes.

==**Filtre passif et filtre actif**==
Un filtre est passif s’il n’est constitué que de dipôles passifs (résistances, bobines et condensateurs). Il est actif s’il contient un amplificateur alimenté par une source extérieure au circuit.
# Diagrammes
Filtre (R, C)
![[figure172.png]]^figure1

Quadripôle : $u_1$ est la tension d’entrée ; $u_2$ est la tension de sortie ; $i_1$ est le courant d’entrée ; $i_2$ est le courant de sortie
![[figure173.png]]^figure2
# Graphiques

# Expériences

# Autres notes
> [!warning]
> L’usage le plus répandu consiste à noter la fonction de transfert comme une fonction complexe de la variable complexe $j\omega$ et non comme une fonction complexe de la variable réelle $\omega$.
^info1

> [!warning] A retenir
> - $\log 2 = 0,3$
> - $\log 3 = 0,48 \approx 0,5$ (à rapprocher de $3^{2} \approx 10$)
> - Diviser $H$ par $\sqrt{2}$ revient à retrancher 3 dB au gain : $20\log\frac{H}{\sqrt{2}} = 20\log(H) - 10\log2$
> - Diviser $H$ par 10 revient à retrancher 20 dB au gain : $20\log\frac{H}{10} = 20\log(H) - 20\log10$.