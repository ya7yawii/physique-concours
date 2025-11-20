---
titre: "[[12-Analyse harmonique]]"
tags:
aliases:
crée: 20-11-2025, 11:09
---
# Formules
> [!note] Théorème de Fourier
> Soit un signal $s(t)$ physiquement réalisable et périodique de période $T = \frac{2\pi}{\omega}$. À toute date $t$ où le signal est continu, il est développable, de façon unique, en série de Fourier : $\displaystyle s(t) = \frac{A_0}{2} + \sum_{n = 1}^{\infty}[A_n\cos(n\omega t) + B_n\sin(n\omega t)]$.
> Les coefficients de la série de Fourier sont donnés par les formules : $\displaystyle A_n = \frac{2}{T}\int_{t_0}^{t_0 + T}s(t)\cos(n\omega t)dt$ et $\displaystyle B_n = \frac{2}{T}\int_{t_0}^{t_0 + T}s(t)\sin(n\omega t)dt$, où $t_0$ est une date arbitraire.
> Les pulsations $\omega, 2\omega, \ldots, n\omega$, sont appelés harmoniques et constituent l'ondulation $s_{ond}(t)$ du signal : $\displaystyle s(t) = s_0 + s_{ond}(t) = \frac{A_0}{2} + \sum_{n = 1}^{\infty} s_n(t)$.
> Le signal constant est la valeur moyenne de $s(t)$ sur une période : $s_0 = \langle s(t) \rangle$.
> L’harmonique de rang n $(n \geqslant 1)$ est le signal $s_n(t)$ et l'harmonique de rang 1, de même période que le signal $s(t)$, est le fondamental $s_1(t)$.
> Remarque : Les coefficients de Fourier d’un signal périodique sont indépendants du choix particulier de l’intervalle $[t_0, t_0 + T]$ utilisé pour leur calcul. Seule importe l’extension de cet intervalle qui doit être égale à la période $T$ du signal.

> [!note] Autre forme du développement en série de Fourier
> Le développement en série de Fourier d’un signal périodique $s(t)$ peut être mis sous la forme : $\displaystyle s(t) = C_0 + \sum_{n=1}^{\infty}C_n\cos(n\omega t + \phi_n)$, avec :
> - $C_0 = \frac{A_0}{2}$ : amplitude de la composante continue ;
> - $C_n = \sqrt{A_{n}^{2} + B_{n}^{2}}$ : amplitude de l’harmonique de rang n ;
> - $\phi_n$ : phase à l’origine des temps telle que $\tan\phi_n = -\frac{B_n}{A_n}$.

> [!note] Série de Fourier : Propriétés
> - Pour un signal physique, l’amplitude $C_n$ des harmoniques tend vers zéro quand leur rang $n$ tend vers l’infini : $\displaystyle \lim_{n \rightarrow \infty} C_n = 0$ ;
> - Lorsque la fonction périodique $s(t)$ est paire, son développement en série de Fourier est aussi pair, ce qui entraîne $B_n = 0$ quel que soit $n$, d’où : $\displaystyle s(t) = \frac{A_0}{2} + \sum_{n = 1}^{\infty}A_n\cos(n\omega t)$ ;
> - Lorsque la fonction périodique $s(t)$ est impaire, son développement en série de Fourier est aussi impair, ce qui entraîne $A_n = 0$ quel que soit $n$, d’où : $\displaystyle s(t) = \sum_{n = 1}^{\infty}B_n\sin(n\omega t)$.

> [!note] Quelques séries de Fourier
> Notre but n’est pas de nous concentrer sur la technique de calcul des coefficients $A_n$ et $B_n$, mais sur l’utilisation de cette notion riche en application. Mais, il est conseillé de vérifier à titre d'entraînement les développements de signaux fréquemment rencontrés comme :
> - Signal en créneau impair et de rapport cyclique $\frac{1}{2}$ : Le rapport cyclique est égal au rapport de la durée de la partie positive et de la période ([[#^figure1|fig. 1]]) ;
> - Signal en créneau pair et de rapport cyclique $\frac{1}{2}$ : Le développement se déduit du précédent par un changement de l’origine des temps ([[#^figure2|fig. 2]]) ;
> - Signal en triangle, pair et de rapport cyclique $\frac{1}{2}$ : Pour le signal triangulaire ([[#^figure3|fig. 3]]), nous définissons le rapport cyclique comme le rapport entre l’intervalle de temps sur lequel le signal est croissant et sa période. Nous pouvons remarquer que si nous dérivons tous les termes, nous obtenons le développement d’une fonction en créneau, c'est-à-dire la dérivée de la fonction $s(t)$ ;
> - Signal sinusoïdal redressé double alternance ([[#^figure4|fig. 4]]).

> [!note] Spectre de fréquence
> Considérons un signal périodique dont la décomposition en série de Fourier est écrite sous la forme : $\displaystyle s(t) = C_0 + \sum_{n=1}^{\infty}C_n\cos(n\omega t + \phi_n)$.
> L’ensemble des amplitudes $C_n$ $(n \in \mathbb{N})$ forme le spectre de fréquence du signal $s(t)$. Il est représenté par un diagramme en bâtons, spectre de raies, obtenu en représentant les amplitudes $C_n$ en fonction des pulsations $n\omega$ ou, plus simplement, en fonction des rangs $n$ ([[#^figure5|fig. 5]]).
> Remarque : Le spectre de fréquence d’un signal est invariant lors des changements de l’origine des temps. Un tel changement affecte les $\varphi_n$ et non les $C_n$.

> [!note] Synthèse de Fourier
> - Signal continu : Notons $s_{F_n}(t)$ la série de Fourier d’un signal périodique continu $s(t)$, limitée à ses $n$ premiers termes. Lorsque $n$ tend vers l’infini, $s_{F_n}(t)$ tend vers $s(t)$ : $\displaystyle \lim_{n \rightarrow \infty}s_{F_n}(t) = s(t)$. Lors de la synthèse d’un tel signal, la somme des premiers harmoniques $s_{F_n}(t)$ suffit pour le représenter de façon satisfaisante, comme nous pouvons le constater sur les figures [[#^figure6|6]] et [[#^figure7|7]] où les signaux présentent, cependant, une discontinuité de pente.
> Lorsqu’un signal périodique ne présente que des discontinuités de pente, l’amplitude $C_n$ des raies de son spectre de fréquence décroît rapidement (au moins en $\frac{1}{n^{2}}$).
> Une bande passante limitée suffira généralement à la transmission d’un signal périodique continu.
> - Signal discontinu : Soit $s(t)$ un signal développable en série de Fourier et présentant une discontinuité en $t = t_0$. La série de Fourier $s_F(t)$ est continue et tend vers : $s_F(t) = \frac{1}{2}[s(t_{0^-}) + s(t_{0^+})]$ quand $t$ tend vers $t_0$. Au voisinage de $t_0$, le graphe de $s_F(t)$ varie rapidement et continûment pour dépasser, de part et d’autre, la discontinuité.
> En un point de discontinuité, l’écart entre les graphes de $s_{F_n}(t_0)$ et $s(t_0)$ est irréductible, quel que soit le nombre $n$ d’harmoniques considéré. Cet effet, connu sous le nom de phénomène de Gibbs, est illustré [[#^figure8|figure 8]] pour un signal carré $s(t)$, et [[#^figure9|figure 9]] pour une rampe périodique. Le dépassement peut être important. Il est ainsi possible de démontrer qu’il est environ de 17 % pour le signal carré.
> D’un point de vue pratique, nous retiendrons qu’un signal discontinu exige une bande passante très large pour sa transmission.
> Lorsqu’un signal périodique présente des discontinuités, l’amplitude $C_n$ des raies de son spectre de fréquence décroît lentement (généralement en $\frac{1}{n}$).

> [!note] Valeurs efficaces et coefficients de Fourier
> - Formule de Parseval : Soit $S$ la valeur efficace d’un signal $s(t)$ périodique développable en série de Fourier : $\displaystyle S^{2} = \langle s^{2}(t) \rangle = \frac{1}{T}\int_{t_0}^{t_0 +T}s^{2}(t)dt$. $S^2$ s’obtient par la formule de Parseval : $\displaystyle S^{2} = \langle s^{2}(t) \rangle = C_{0}^{2} + \frac{1}{2}\sum_{n=1}^{\infty}C_{n}^{2}$.
> La formule de Parseval peut s’interpréter physiquement en constatant que l’énergie est souvent une fonction quadratique du signal (par exemple $\mathcal{E} = \frac{1}{2}Cu^{2}$ dans un condensateur, $\mathcal{E}_K = \frac{1}{2}mv^{2}$ pour un point matériel...). Elle signifie alors que l’énergie moyenne contenue dans le signal périodique est la somme des énergies moyennes associées à chacun de ses harmoniques.
> - Taux de distorsion : Appliquons un signal sinusoïdal $v_e(t) = v_{e_m}\cos (\omega t)$ à l’entrée d’un amplificateur. Si ce dernier est linéaire, il délivre en sortie un signal sinusoïdal de même pulsation $\omega$.
> Ainsi, le fondamental du signal de sortie correspond à l’amplification linéaire et les autres harmoniques sont dus à la non-linéarité.
> Il en résulte que la linéarité d’un amplificateur peut s’apprécier avec le taux de distorsion harmonique $\delta_h$, rapport de la valeur efficace $S_h$ des harmoniques $(n > 1)$ créés par la distorsion à la valeur efficace $S_f$ du fondamental : $\displaystyle \delta_h = \frac{S_h}{S_f} = \frac{\displaystyle\sqrt{\sum_{n=2}^{\infty}C_{n}^{2}}}{C_1}$.
> Un amplificateur est d’autant plus linéaire que son taux de distorsion harmonique est voisin de zéro.
# Définitions

# Diagrammes

# Graphiques
Créneau impair et de rapport cyclique $\frac{1}{2}$
![[figure298.png]]^figure1

Créneau pair et de rapport cyclique $\frac{1}{2}$
![[figure299.png]]^figure2

Triangle pair et de rapport cyclique $\frac{1}{2}$
![[figure300.png]]^figure3

Sinusoïde redressée double alternance
![[figure301.png]]^figure4

Spectre de fréquence d’un signal périodique
![[figure302.png]]^figure5

Synthèse d’un signal triangulaire
![[figure303.png]]^figure6

Synthèse d’un signal redressé simple alternance
![[figure304.png]]^figure7

 Mise en évidence du phénomène de Gibbs sur un signal carré
 ![[figure305.png]]^figure8

Mise en évidence du phénomène de Gibbs sur une rampe périodique
![[figure306.png]]^figure9
# Expériences

# Autres notes
