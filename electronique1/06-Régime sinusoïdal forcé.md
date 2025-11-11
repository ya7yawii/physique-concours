---
titre: "[[06-Régime sinusoïdal forcé]]"
tags:
aliases:
crée: 11-11-2025, 09:50
---
# Formules
> [!note] Représentation complexe du signal
> - Représentation complexe : À un signal sinusoïdal : $s(t) = s_m\cos(\omega t + \phi)$ d'amplitude réelle $s_m$ (positive) et de phase $\phi$ est associée la représentation complexe : $\underline{s}(t) = \underline{s}_m e^{j\omega t}$ d'amplitude complexe : $\underline{s}_m = s_me^{j\phi}$.
> - Représentation de Fresnel : La représentation de Fresnel de $s(t) = s_m\cos(\omega t + \phi)$ est la représentation géométrique de son amplitude complexe $\underline{s}_m$ dans le plan complexe ([[#^figure1|fig. 1]]).

> [!note]
> La notation complexe d’un signal peut être utilisée lorsqu’on effectue des OPÉRATIONS LINÉAIRES sur celui-ci : addition, soustraction, multiplication par un réel, dérivation, intégration (avec une constante nulle). Les opérations de dérivation et intégration de la représentation complexe d’un signal sont très simples puisqu’il suffit de multiplier ou diviser, respectivement, le signal complexe par le facteur $j\omega$.

> [!note] Circuit (R, L, C) série en régime sinusoïdal
> Considérons un circuit (R, L, C ) série soumis à l’excitation sinusoïdale $e(t)$ délivrée par un générateur basse fréquence. Nous supposerons, par exemple, que le générateur délivre, à partir de l’instant $t = 0$, la tension $e(t) = e_m\cos\omega t$ ([[#^figure2|fig. 2]]).
> L’équation d’évolution du courant dans le circuit : $\dfrac{d^{2}i(t)}{dt^{2}} + \frac{\omega_0}{Q}\dfrac{di(t)}{dt} + \omega_{0}^{2}i(t) = \frac{-\omega e_m}{L}\sin(\omega t)$ avec $\omega_0 = \frac{1}{\sqrt{LC}}$ et $Q = \frac{L\omega_0}{R}$.
> Ainsi, la solution cherchée $i(t)$ doit pouvoir s'écrire $i(t) = i_0(t) + i_1(t)$ où :
> - $i_1(t)$ est une solution particulière de l’équation d’évolution ;
> - $i_0(t)$ solution de l’équation sans second membre.
> 
> Dans le cas du circuit (R, L, C ) nous savons que la résistance entraîne un amortissement des solutions du type $i_0(t)$ : lorsque le second membre de l’équation d’évolution est nul, le signal tend vers zéro, et la fonction $i_0(t)$ est pratiquement nulle au-delà de $t = \tau$ , temps de relaxation du circuit.
> Dans ces conditions, nous pouvons dire que le signal $i(t)$ tend vers la solution particulière $i_1(t)$ : après un <mark style="color: red">régime transitoire</mark> dont la durée est indiquée par le temps de relaxation $\tau$ du circuit (R, L, C ) série, seule la solution particulière subsiste.
> Lorsqu’un circuit (R, L, C) est soumis à une excitation sinusoïdale de pulsation $\omega$, un <mark style="color: red">régime permanent sinusoïdal</mark>, de même pulsation que l’excitation imposée, s'établit après un régime transitoire qui dépend du facteur de qualité du circuit. Ne dépendant que de l’excitation imposée, ce régime permanent (limite) est de plus indépendant des conditions initiales.

> [!note] Détermination du régime permanent sinusoïdal
> Lorsque nous observons les signaux électriques d’un circuit (R, L, C ) alimenté par une tension excitatrice sinusoïdale $e(t) = e_m\cos(\omega t)$, nous ne voyons pas apparaître le régime transitoire, qui a disparu depuis longtemps ; nous ne nous intéresserons donc ici qu’au signal $i_1(t)$ qui seul subsiste : il est sinusoïdal, de même pulsation que l’excitation : $i_1(t) = i_{1m}\cos(\omega t + \phi)$. Cherchons à déterminer les paramètres de ce signal.
> - Une méthode fastidieuse (à proscrire) : Reportons l'expression de $i_1(t)$ dans l'équation d’évolution du courant, ce qui donne : $(-\omega^{2} + \omega_{0}^{2})i_{1m}\cos(\omega t +\phi) - \frac{\omega\omega_0}{Q}i_{1m}\sin(\omega t +\phi) = \frac{-\omega e_m}{L}\sin(\omega t)$. Développons cette expression de façon à ne garder que des termes en $\cos(\omega t)$ et $\sin (\omega t)$ : $\left[(-\omega^{2} + \omega_{0}^{2})\cos\phi - \frac{\omega\omega_0}{Q}\sin\phi\right]\cos(\omega t) + \left[(\omega^{2} - \omega_{0}^{2})\sin\phi - \frac{\omega\omega_0}{Q}\cos\phi\right]\sin(\omega t) = \frac{-\omega e_m}{Li_{1m}}\sin(\omega t)$. En identifiant les termes en $\cos(\omega t)$ et en $\sin(\omega t)$, on obtient un système d'équation en $\cos\phi$ et $\sin\phi$. En résolvant ce système, on trouve les expressions de $\cos\phi$ et $\sin\phi$ en fonction de $i_{1m}$. Donc, pour éliminer $\phi$ et trouver l'expression de l'amplitude $i_{1m}$, écrivons que $\cos^{2}\phi + \sin^{2}\phi = 1$. Enfin la réponse $i_1(t)$ est déterminée après avoir trouver l'expression de l'amplitude et la phase.
> - Obtention de la solution particulière avec la notation complexe :


# Définitions

# Diagrammes
Étude d’un circuit (R, L, C) série
![[figure111.png]]^figure2
# Graphiques
Représentation de Fresnel de la grandeur sinusoïdale $s(t) = s_m\cos(\omega t + \phi)$
![[figure110.png]]^figure1
# Expériences

# Autres notes
> [!warning] Point mathématique
> La représentation complexe ne permet pas de déterminer le produit de deux fonctions sinusoïdales.
> Considérons en effet deux signaux sinusoïdaux : $s_1(t) = s_{1m}\cos(\omega t + \phi_1)$ et $s_2(t) = s_{2m}\cos(\omega t + \phi_2)$.
> - $s_1(t)s_2(t) = \frac{1}{2}s_{1m}s_{2m}\cos(\phi_1 - \phi_2)\cos(2\omega t + \phi_1 + \phi_2)$.
> - $\underline{s}_1\underline{s}_2 = s_{1m}s_{2m}e^{j(2\omega t + \phi_1 + \phi_2)}$.
> 
> Il est clair que : $\mathcal{R}e(\underline{s}_1\underline{s}_2) \neq s_1(t)s_2(t)$.