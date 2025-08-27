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


# Définitions

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
# Expériences

# Autres notes
