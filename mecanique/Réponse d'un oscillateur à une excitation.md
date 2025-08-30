---
titre: "[[Réponse d'un oscillateur à une excitation]]"
tags:
aliases:
crée: 27-08-2025, 09:31
---
# Formules
Équation du mouvement : $\dfrac{d^{2}x(t)}{dt^{2}} + \frac{\omega_0}{\mathcal{Q}}\dfrac{dx(t)}{dt} + \omega_{0}^{2}x(t) = \omega_{0}^{2}x_A(t)$ avec $x(t)$ est le déplacement de la bille par rapport à sa position d'équilibre (exemple dans la [[#^figure1]]), et $x_A(t)$ celui du point A par rapport à $O$. En notant $\omega_0 = \sqrt{\frac{k}{m}}$  la pulsation propre de l'oscillateur et $\mathcal{Q} = \frac{m\omega_0}{h} = \frac{\omega_0}{2\alpha} = \omega_0\tau$ son facteur de qualité.

> [!warning] Solutions de l'équation d'évolution
> Il faut savoir comment résoudre une équation différentielle linéaire  d'ordre deux à coefficients constants avec un second membre fonction du temps.

> [!note] Régimes libre, transitoire, et forcé
> La solution générale $x(t)$ s'analyse en la somme de :
> - $x_0(t)$ : solution générale de l'équation différentielle homogène ;
> - $x_1(t)$ : solution particulière de l'équation différentielle avec second membre, soit : $x(t) = x_0(t) + x_1(t)$.
> 
> Quand l'oscillateur est amorti, son régime libre, décrit par $x_0(t)$, disparaît avec le temps, comme il a été vu au chapitre [[Mouvement libre d'un oscillateur harmonique]]. Seul persiste ensuite le régime forcé décrit par $x_1(t)$.
> On appelle régime transitoire le régime représenté par $x(t)$ tant que $x_0(t)$ n'est pas négligeable devant $x_1(t)$.

> [!note] Additivité des réponses (ou principe de superposition)
> La linéarité de l'équation du mouvement d'un oscillateur harmonique entraîne l'additivité de ses réponses.
> Il en sera ainsi, par exemple, lorsque l'oscillateur est soumis à une excitation périodique décomposable en série de Fourier : sa réponse est la superposition de l'ensemble des réponses harmoniques.

> [!note] Réponse à un échelon
> L'équation du mouvement s'écrit : $\dfrac{d^{2}x(t)}{dt^{2}} + \frac{\omega_0}{\mathcal{Q}}\dfrac{dx(t)}{dt} + \omega_{0}^{2}x(t) = \omega_{0}^{2}X_0$ où $x_A(t) = X_0H(t)$, $X_0$ est l'amplitude de cet échelon, et $H(t)$ désigne la fonction de Heaviside ([[#^figure2]]).
> La solution générale est : $x(t) = X_0 + A_1e^{r_1t} + A_2e^{r_2t}$ avec $r_1$ et $r_2$ sont les racines de l'équation caractéristique ; $A_1$ et $A_2$ sont deux constantes fixées par les conditions initiales.
> À l'instant initial, il n'y a pas discontinuité de vitesse ou déplacement donc $x(0^{+}) = 0$ et $v(0^{+}) = 0$.
> Pour une excitation permanente imposée, la réponse de l'oscillateur amorti tend vers une réponse limite qui est la réponse à cette excitation permanente. Cette limite devrait en principe être atteinte en un temps de l'ordre de quelques $\tau = \frac{\mathcal{Q}}{\omega_0} = \frac{1}{2\alpha}$.
> La valeur du facteur de qualité $\mathcal{Q}$ nous indique si la limite sera atteinte après  un régime transitoire pseudo-périodique, critique, ou apériodique, comme nous pouvons l'observer sur la [[#^figure3]].
> Déplacer l'extrémité revient à décaler la position d'équilibre de l'oscillateur. Dans le plan de phase ([[#^figure4]]), nous pouvons observer la modification de la position du centre attracteur : l'oscillateur qui était au repos se déplace pour rejoindre la nouvelle position d'équilibre représentée par le nouvel attracteur $A(X_0, 0)$.

> [!note] Réponse à une excitation sinusoïdale
> L'excitation sinusoïdale de pulsation $\omega$ : $x_A(t) = x_{A_m}\cos(\omega t)$.
> La réponse de l'oscillateur est sous la forme : $x(t) = x_1(t) + x_0(t)$ avec le terme $x_0(t)$ de régime transitoire est une solution de l'équation du mouvement sans second membre, qui tend vers zéro lorsque le temps s'écoule, puisque l'oscillateur est amorti. Par conséquent, la réponse oscillante qui se stabilise peu à peu n'est autre que la fonction $x_1(t)$.
> Lorsque ce régime permanent sinusoïdal établi est atteint, nous avons : $x(t) = x_1(t) = x_m\cos(\omega t + \phi)$ où les amplitudes $x_m$ et la phase $\phi$ sont des fonctions de $\omega$ que nous obtiendrons en résolvant l'équation ci-dessous. En fait, $x_m = |\underline{X}|$ et $\phi = arg(\underline{X})$.
> Pour le modèle de l'oscillateur harmonique parfait $(\mathcal{Q} = ∞)$, le régime permanent sinusoïdal ne pourrait pas s'établir, des oscillations à la pulsation propre $\omega_0$ subsistant indéfiniment.
> L'équation du mouvement s'écrit : $\dfrac{d^{2}x(t)}{dt^{2}}+ \frac{\omega_0}{\mathcal{Q}}\dfrac{dx(t)}{dt} + \omega_{0}^{2}x(t) = \omega_{0}^{2}x_{A_m}\cos(\omega t)$
> La meilleure méthode pour résoudre cette équation est celle de la variable complexe qui suit ces étapes :
> - l'équation différentielle s'écrit en notation complexe : $\dfrac{d^{2}\underline{x}(t)}{dt^{2}} + \frac{\omega_0}{\mathcal{Q}}\dfrac{d\underline{x}(t)}{dt} + \omega_{0}^{2}\underline{x}(t) = \omega_{0}^{2}x_{A_m}e^{j\omega t}$
> - on note $\underline{x}(t) = \underline{X}e^{j\omega t} \Rightarrow \dfrac{d\underline{x}(t)}{dt} = j\omega\underline{X}e^{j\omega t} = j\omega\underline{x} \Rightarrow \dfrac{d^{2}\underline{x}(t)}{dt^{2}} = -\omega^{2}\underline{X}e^{j\omega t} = -\omega^{2}\underline{x}$
> - l'équation différentielle se transforme ensuite : $-\omega^{2}\underline{x}(t) + j\omega\frac{\omega_0}{\mathcal{Q}}\underline{x}(t) + \omega_{0}^{2}\underline{x}(t) = \omega_{0}^{2}x_{A_m}e^{j\omega t}$
> - qui nous donne l'amplitude complexe $\underline{X} = \frac{\omega_{0}^{2}x_{A_m}}{\omega_{0}^{2} + j\omega\frac{\omega_0}{\mathcal{Q}} - \omega^{2}}$ 

> [!note] Réponse harmonique en élongation
> Amplitude de la réponse en élongation : $x_m(u) = x_{A_m} \frac{1}{\sqrt{(1 - u^{2})^{2} + \left(\frac{u}{\mathcal{Q}}\right)^{2}}}$ avec $u = \frac{\omega}{\omega_0}$.
> En étudiant les comportements asymptotiques (à très basses et très hautes fréquences), on déduit que l’oscillateur harmonique amorti effectue un filtrage passe-bas ([[#^figure5]]).
> Pour détailler ce qui se produit entre les deux comportements limites précédents, on calcule la dérivée de $x_m$ par rapport à $u$ :
> - Si $\mathcal{Q} \leqslant \frac{1}{\sqrt{2}}$, l’élongation est strictement décroissante.
> - En revanche, pour $\mathcal{Q} > \frac{1}{\sqrt{2}}$, elle passe par un maximum. L’oscillateur présente alors une résonance en élongation. Celle-ci survient à une pulsation $\omega_r$ un peu inférieure à la pulsation propre $\omega_0$ de l’oscillateur. Si $\mathcal{Q} \gg 1 : x_m = \mathcal{Q} x_{A_m}$. Cette amplitude peut devenir très grande et causer la détérioration du résonateur. Pour de fortes amplitudes, le modèle du rappel linéaire serait aussi remis en cause.
> 
> Déphasage de la réponse en élongation : $\phi(\omega) = arg(\underline{X}) = -\frac{\pi}{2} + \arctan\left(\frac{1 - u^{2}}{\frac{u}{\mathcal{Q}}}\right)$
> Pour trouver l'allure de $\phi(\omega)$ ([[#^figure6]]), on étudie d'abord les comportement asymptotiques de $\tan(\phi)$ qui peut être déduite de l'expression de $\underline{X}$ sans calculer $arg(\underline{X})$.

> [!note] Réponse harmonique en vitesse
> Amplitude de la réponse en vitesse : dans la mesure où $\underline{v} = j\omega\underline{x}$, nous avons : $v_m = \mathcal{Q}\omega_0x_{A_m}\frac{1}{\sqrt{1 + \mathcal{Q}^{2}\left(u -\frac{1}{u}\right)^{2}}}$ avec $u = \frac{\omega}{\omega_0}$.
> Celle-ci tend vers zéro à très basse ou très haute fréquence, et passe par un maximum en $u = 1$. Pour la réponse en vitesse, l’oscillateur harmonique amorti effectue un filtrage passe-bande ([[#^figure7]]), avec une résonance lorsque la fréquence excitatrice coïncide avec la fréquence propre de l’oscillateur.  À la résonance, pour $\omega = \omega_0$ , la valeur maximale $v_{m,r} = \mathcal{Q}\omega_0x_{A_m}$ peut devenir très importante, associée à une résonance aiguë, lorsque l’amortissement est faible.
> Déphasage de la réponse en vitesse : considérant la relation $\underline{v} = j\omega\underline{x}$, nous obtenons : $\psi(\omega) = \frac{\pi}{2} + \phi(\omega) = \arctan\left[\mathcal{Q}\left(\frac{1}{u} - u\right)\right]$ dont le graphe est représenté sur la [[#^figure8]].

# Définitions
==**Analyse harmonique**== :
Faire l’analyse harmonique du système, c’est étudier sa réponse fréquentielle, autrement dit analyser les variations de l’amplitude $A(w)$ et du déphasage $\phi(w)$ avec la pulsation $\omega$ ($\omega = 2\pi f$, où $f$ est la fréquence de l’excitation).
# Diagrammes
Modèle d'oscillateur mécanique linéaire amorti soumis à une excitation $x_A(t)$ :
![[figure38.png]]^figure1
En agitant l'extrémité A du ressort, nous pouvons exciter le mouvement de cet oscillateur amorti. Ce fait est traduit par le second membre, non nul et pouvant dépendre du temps, de l'équation d'évolution.
# Graphiques
Fonction échelon (ou de Heaviside) :
![[figure39.png]]^figure2

Régimes transitoires d'un oscillateur en réponse à une excitation en échelon (Évolutions temporelles):
![[figure40.png]]^figure3

Régimes transitoires d'un oscillateur en réponse à une excitation en échelon (Trajectoires de phase):
![[figure41.png]]^figure4

Variation de l’amplitude normalisée de la réponse en élongation en fonction de u pulsation normalisée de l’excitation pour différents amortissements:
![[figure42.png]]^figure5

Variation de déphasage de la réponse en élongation par rapport à l’excitation pour différents amortissements:
![[figure43.png]]^figure6

Variation de l’amplitude de la réponse en vitesse en fonction de la pulsation normalisée de l’excitation, pour différents amortissements :
![[figure44.png]]^figure7

Variation de $\psi$ en fonction de pulsation normalisée, pour différents amortissements :
![[figure45.png]]^figure8
# Expériences

# Autres notes
