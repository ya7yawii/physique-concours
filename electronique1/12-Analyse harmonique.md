---
titre: "[[12-Analyse harmonique]]"
tags:
  - série-de-Fourier
  - spectre-de-fréquence
  - filtre
  - passe-bas
  - passe-haut
  - passe-bande
crée: 20-11-2025, 11:09
---
# Formules
> [!note] Théorème de Fourier
> Soit un signal $s(t)$ physiquement réalisable et périodique de période $T = \frac{2\pi}{\omega}$. À toute date $t$ où le signal est continu, il est développable, de façon unique, en série de Fourier : $\displaystyle s(t) = \frac{A_0}{2} + \sum_{n = 1}^{\infty}[A_n\cos(n\omega t) + B_n\sin(n\omega t)]$.
> Les coefficients de la série de Fourier sont donnés par les formules : $\displaystyle A_n = \frac{2}{T}\int_{t_0}^{t_0 + T}s(t)\cos(n\omega t)dt$ et $\displaystyle B_n = \frac{2}{T}\int_{t_0}^{t_0 + T}s(t)\sin(n\omega t)dt$, où $t_0$ est une date arbitraire.
> Les pulsations $\omega, 2\omega, \ldots, n\omega$, sont appelés harmoniques et constituent l'ondulation $s_{ond}(t)$ du signal : $\displaystyle s(t) = s_0 + s_{ond}(t) = \frac{A_0}{2} + \sum_{n = 1}^{\infty} s_n(t)$.
> Le signal constant est la valeur moyenne de $s(t)$ sur une période : $s_0 = \langle s(t) \rangle$.
> L'harmonique de rang n $(n \geqslant 1)$ est le signal $s_n(t)$ et l'harmonique de rang 1, de même période que le signal $s(t)$, est le fondamental $s_1(t)$.
> Remarque : Les coefficients de Fourier d'un signal périodique sont indépendants du choix particulier de l'intervalle $[t_0, t_0 + T]$ utilisé pour leur calcul. Seule importe l'extension de cet intervalle qui doit être égale à la période $T$ du signal.

> [!note] Autre forme du développement en série de Fourier
> Le développement en série de Fourier d'un signal périodique $s(t)$ peut être mis sous la forme : $\displaystyle s(t) = C_0 + \sum_{n=1}^{\infty}C_n\cos(n\omega t + \phi_n)$, avec :
> - $C_0 = \frac{A_0}{2}$ : amplitude de la composante continue ;
> - $C_n = \sqrt{A_{n}^{2} + B_{n}^{2}}$ : amplitude de l'harmonique de rang n ;
> - $\phi_n$ : phase à l'origine des temps telle que $\tan\phi_n = -\frac{B_n}{A_n}$.

> [!note] Série de Fourier : Propriétés
> - Pour un signal physique, l'amplitude $C_n$ des harmoniques tend vers zéro quand leur rang $n$ tend vers l'infini : $\displaystyle \lim_{n \rightarrow \infty} C_n = 0$ ;
> - Lorsque la fonction périodique $s(t)$ est paire, son développement en série de Fourier est aussi pair, ce qui entraîne $B_n = 0$ quel que soit $n$, d'où : $\displaystyle s(t) = \frac{A_0}{2} + \sum_{n = 1}^{\infty}A_n\cos(n\omega t)$ ;
> - Lorsque la fonction périodique $s(t)$ est impaire, son développement en série de Fourier est aussi impair, ce qui entraîne $A_n = 0$ quel que soit $n$, d'où : $\displaystyle s(t) = \sum_{n = 1}^{\infty}B_n\sin(n\omega t)$.

> [!note] Quelques séries de Fourier
> Notre but n'est pas de nous concentrer sur la technique de calcul des coefficients $A_n$ et $B_n$, mais sur l'utilisation de cette notion riche en application. Mais, il est conseillé de déterminer à titre d'entraînement les développements de signaux fréquemment rencontrés comme :
> - Signal en créneau impair et de rapport cyclique $\frac{1}{2}$ : Le rapport cyclique est égal au rapport de la durée de la partie positive et de la période ([[#^figure1|fig. 1]]) ;
> - Signal en créneau pair et de rapport cyclique $\frac{1}{2}$ : Le développement se déduit du précédent par un changement de l'origine des temps ([[#^figure2|fig. 2]]) ;
> - Signal en triangle, pair et de rapport cyclique $\frac{1}{2}$ : Pour le signal triangulaire ([[#^figure3|fig. 3]]), nous définissons le rapport cyclique comme le rapport entre l'intervalle de temps sur lequel le signal est croissant et sa période. Nous pouvons remarquer que si nous dérivons tous les termes, nous obtenons le développement d'une fonction en créneau, c'est-à-dire la dérivée de la fonction $s(t)$ ;
> - Signal sinusoïdal redressé double alternance ([[#^figure4|fig. 4]]).

> [!note] Spectre de fréquence
> Considérons un signal périodique dont la décomposition en série de Fourier est écrite sous la forme : $\displaystyle s(t) = C_0 + \sum_{n=1}^{\infty}C_n\cos(n\omega t + \phi_n)$.
> L'ensemble des amplitudes $C_n$ $(n \in \mathbb{N})$ forme le spectre de fréquence du signal $s(t)$. Il est représenté par un diagramme en bâtons, spectre de raies, obtenu en représentant les amplitudes $C_n$ en fonction des pulsations $n\omega$ ou, plus simplement, en fonction des rangs $n$ ([[#^figure5|fig. 5]]).
> Remarque : Le spectre de fréquence d'un signal est invariant lors des changements de l'origine des temps. Un tel changement affecte les $\varphi_n$ et non les $C_n$.

> [!note] Synthèse de Fourier
> - Signal continu : Notons $s_{F_n}(t)$ la série de Fourier d'un signal périodique continu $s(t)$, limitée à ses $n$ premiers termes. Lorsque $n$ tend vers l'infini, $s_{F_n}(t)$ tend vers $s(t)$ : $\displaystyle \lim_{n \rightarrow \infty}s_{F_n}(t) = s(t)$. Lors de la synthèse d'un tel signal, la somme des premiers harmoniques $s_{F_n}(t)$ suffit pour le représenter de façon satisfaisante, comme nous pouvons le constater sur les figures [[#^figure6|6]] et [[#^figure7|7]] où les signaux présentent, cependant, une discontinuité de pente.
> Lorsqu'un signal périodique ne présente que des discontinuités de pente, l'amplitude $C_n$ des raies de son spectre de fréquence décroît rapidement (au moins en $\frac{1}{n^{2}}$).
> Une bande passante limitée suffira généralement à la transmission d'un signal périodique continu.
> - Signal discontinu : Soit $s(t)$ un signal développable en série de Fourier et présentant une discontinuité en $t = t_0$. La série de Fourier $s_F(t)$ est continue et tend vers : $s_F(t) = \frac{1}{2}[s(t_{0^-}) + s(t_{0^+})]$ quand $t$ tend vers $t_0$. Au voisinage de $t_0$, le graphe de $s_F(t)$ varie rapidement et continûment pour dépasser, de part et d'autre, la discontinuité.
> En un point de discontinuité, l'écart entre les graphes de $s_{F_n}(t_0)$ et $s(t_0)$ est irréductible, quel que soit le nombre $n$ d'harmoniques considéré. Cet effet, connu sous le nom de phénomène de Gibbs, est illustré [[#^figure8|figure 8]] pour un signal carré $s(t)$, et [[#^figure9|figure 9]] pour une rampe périodique. Le dépassement peut être important. Il est ainsi possible de démontrer qu'il est environ de 17 % pour le signal carré.
> D'un point de vue pratique, nous retiendrons qu'un signal discontinu exige une bande passante très large pour sa transmission.
> Lorsqu'un signal périodique présente des discontinuités, l'amplitude $C_n$ des raies de son spectre de fréquence décroît lentement (généralement en $\frac{1}{n}$).

> [!note] Valeurs efficaces et coefficients de Fourier
> - Formule de Parseval : Soit $S$ la valeur efficace d'un signal $s(t)$ périodique développable en série de Fourier : $\displaystyle S^{2} = \langle s^{2}(t) \rangle = \frac{1}{T}\int_{t_0}^{t_0 +T}s^{2}(t)dt$. $S^2$ s'obtient par la formule de Parseval : $\displaystyle S^{2} = \langle s^{2}(t) \rangle = C_{0}^{2} + \frac{1}{2}\sum_{n=1}^{\infty}C_{n}^{2}$.
> La formule de Parseval peut s'interpréter physiquement en constatant que l'énergie est souvent une fonction quadratique du signal (par exemple $\mathcal{E} = \frac{1}{2}Cu^{2}$ dans un condensateur, $\mathcal{E}_K = \frac{1}{2}mv^{2}$ pour un point matériel...). Elle signifie alors que l'énergie moyenne contenue dans le signal périodique est la somme des énergies moyennes associées à chacun de ses harmoniques.
> - Taux de distorsion : Appliquons un signal sinusoïdal $v_e(t) = v_{e_m}\cos (\omega t)$ à l'entrée d'un amplificateur. Si ce dernier est linéaire, il délivre en sortie un signal sinusoïdal de même pulsation $\omega$.
> Ainsi, le fondamental du signal de sortie correspond à l'amplification linéaire et les autres harmoniques sont dus à la non-linéarité.
> Il en résulte que la linéarité d'un amplificateur peut s'apprécier avec le taux de distorsion harmonique $\delta_h$, rapport de la valeur efficace $S_h$ des harmoniques $(n > 1)$ créés par la distorsion à la valeur efficace $S_f$ du fondamental : $\displaystyle \delta_h = \frac{S_h}{S_f} = \frac{\displaystyle\sqrt{\sum_{n=2}^{\infty}C_{n}^{2}}}{C_1}$.
> Un amplificateur est d'autant plus linéaire que son taux de distorsion harmonique est voisin de zéro.

> [!note] Calcul de la tension de sortie pour un filtre linéaire
> Étudions comme exemple l'effet d'un filtre passe-bas d'ordre un de fréquence caractéristique $f_0$ sur un signal créneau pair, de rapport cyclique $\frac{1}{2}$, de fréquence $f = \frac{1}{2}f_0$ et d'amplitude $V_0$ ([[#^figure10|fig. 10]] et [[#^figure11|11]]).
> - Détermination de $v_s(t)$ par décomposition en série de Fourier : Déterminons tout d'abord l'effet du filtre sur un signal harmonique de fréquence quelconque $f = \frac{\omega}{2\pi}$ : $\underline{H}(j\omega) = H(\omega)e^{j\varphi}$ avec $H(\omega) = \frac{1}{\sqrt{1 + \left(\frac{f}{f_0}\right)^{2}}}$ et $\varphi(\omega) = -\arctan\frac{f}{f_0}$.
> Si $v_e(t) = v_{e_m}\cos\frac{2\pi t}{f}$ alors en régime permanent : $v_s(t) = \frac{v_{e_m}}{\sqrt{1 + \left(\frac{f}{f_0}\right)^{2}}}\cos\left(2\pi ft - \arctan\frac{f}{f_0}\right)$.
> Décomposons le signal d'entrée en série de Fourier : $\displaystyle v_e(t) = \frac{4V_0}{\pi}\sum_{p=0}^{\infty}\frac{\sin[(2p+1)2\pi ft]}{2p+1}$ avec $p \in \mathbb{N}$. Comme $f = \frac{1}{2} f_0$ et le filtre étant linéaire, nous pouvons appliquer la superposition des régimes forcés. La réponse à la somme des $u_{en}(t)$ est égale à la somme des $u_{sn}(t)$ : $\displaystyle v_s(t) = \frac{4V_0}{\pi}\sum_{p=0}^{\infty}\frac{1}{\sqrt{1 + \left(\frac{2p+1}{2}\right)^{2}}}\frac{\sin\left[(2p+1)2\pi f_0t - \arctan\frac{(2p+1)}{2}\right]}{2p+1}$ avec $p \in \mathbb{N}$.
> L'expression de $v_s(t)$ n'est pas particulièrement simple, mais un logiciel de calcul peut en donner une valeur approchée en calculant la somme d'un nombre fini d'harmoniques : $\displaystyle v_s(t) \approx \sum_{p=0}^{p_{max}} v_{sn}(t)$ ([[#^figure12|fig. 12]] et [[#^figure13|13]]).
> L'approximation est d'autant meilleure que $p_{max}$ est grand. Dans le cas étudié, on constate que la courbe donnée par le logiciel de calcul n'évolue pratiquement plus à partir de $p_{max} = 20$. Nous pouvons donc restituer le signal de façon satisfaisante en sommant une vingtaine d'harmoniques.
> - Vérification par une autre méthode : Dans ce cas simple, nous pouvons déterminer une expression exacte de $u_s(t)$ en régime forcé. Fixons l'origine des temps à l'instant où $v_e$ bascule de $-V_0$ à $+V_0$ ([[#^figure11|fig. 11]]).
> Lorsque $v_e = +V_0$, $v_s(t)$ est solution de l'équation différentielle du premier ordre à coefficients constants : $\dfrac{dv_s}{dt} + \omega_0v_s = \omega_0V_0$ dont la solution générale est : $v_s(t) = V_0 + Ae^{-\omega_0t}$.
> Lorsque $v_e = -V_0$, en changeant le second membre de l'équation précédente, la solution générale devient : $v_s(t) = -V_0 + Be^{-\omega_0t}$.
> La continuité de $v_s(t)$ à l'instant $t = \frac{T}{2}$ implique : $V_0 + Ae^{-\frac{\omega_0T}{2}} = -V_0 + Be^{-\frac{\omega_0T}{2}}$ (eq. 1).
> En régime établi, nous avons aussi : $v_s(0) = v_s(T)$, soit $V_0 + A = -V_0 + Be^{-\omega_0T}$ (eq. 2).
> D'après les équations eq. 1 et eq. 2, nous obtenons un système d'équations en A et B, que nous pouvons résoudre pour trouver les expressions de A et B, tout en sachant que $\omega_0T = 4\pi$ (puisque $f = \frac{1}{2}f_0$).
> 
> La première méthode est applicable à tout signal périodique et tout filtre linéaire. Elle est récapitulée dans le tableau de [[#^figure14|figure 14]]. 
# Définitions
> [!note] Effet d'un filtre passe-bas sur un signal périodique
> Nous étudions l'effet d'un passe-bas d'ordre un. L'effet d'un passe-bas d'ordre deux peut être étudié selon les mêmes méthodes (rappelons que la coupure à haute fréquence est alors plus brutale, et qu'il peut même y avoir une résonance).
> Nous pouvons envisager trois cas :
> - la fréquence $f$ du signal est très inférieure à la fréquence de coupure $f_H$ ;
> - $f$ est de l'ordre de $f_H$ ;
> - $f$ est très supérieure à $f_H$.
> 
> Ces trois cas sont représentés sur la [[#^figure15|figure 15]] pour un signal triangulaire et sur la [[#^figure16|figure 16]] pour un signal créneau, d'amplitude crête-crête de 1 V et de composante continue 0,1 V.
> Nous remarquons que, dans tous les cas :
> ==**La composante continue du signal est intégralement transmise avec une amplification unité. Le signal de sortie ne présente jamais de discontinuité.**==
> Observons la composante variable.
> Dans le cas où $f < f_H$, le signal triangulaire est transmis avec une légère déformation au niveau de la rupture de pente alors que le signal créneau est transmis avec une déformation plus sensible au niveau de la discontinuité.
> Dans le cas où $f$ est de l'ordre de $f_H$, les signaux transmis sont très déformés.
> Si $f$ est grand devant $f_H$, l'amplitude du signal variable est très faible.
> - Interprétation : Un signal périodique peut être décomposé en série de Fourier en une composante continue représentant sa valeur moyenne et des harmoniques de fréquence $nf$ ($n$ entier). Un filtre passe-bas n'atténue pas la composante continue et les signaux sinusoïdaux de fréquence inférieure à $f_H$.
> 	- Si $f \ll f_H$, une grande partie des harmoniques du signal est transmise sans modification. Le signal de sortie est voisin du signal d'entrée. La déformation du signal de sortie au niveau des discontinuités provient de l'élimination des harmoniques de rang élevé $\left(n > \frac{f_H}{f}\right).
> 	- Si $f$ est de l'ordre de $f_H$, le fondamental et quelques harmoniques sont transmis, les autres harmoniques sont éliminés ([[#^figure17|fig. 17]]). Le signal de sortie ne ressemble pas au signal d'entrée.
> 	- Si $f \gg f_H$, seule la composante continue du signal est transmise sans atténuation. Les différents harmoniques sont très atténués ([[#^figure18|fig. 18]]).
> 
> Remarque : $f \gg f_0$, nous pouvons vérifier que, avec un signal d'entrée en créneau, le spectre du signal de sortie est équivalent au spectre d'un signal triangulaire avec des harmoniques en $\frac{1}{n^{2}}$. On retrouve ainsi le caractère intégrateur du filtre passe-bas d'ordre un.

> [!note] Effet d'un filtre passe-haut sur un signal périodique
> Nous étudions l'effet d'un passe-haut d'ordre un. L'effet d'un passe-haut d'ordre deux peut être étudié selon les mêmes méthodes.
> Envisageons les trois cas suivants :
> - la fréquence $f$ du signal est très inférieure à la fréquence de coupure $f_B$ ;
> - $f$ est de l'ordre de $f_B$ ;
> - $f$ est très supérieure à $f_B$.
> 
> Ces trois cas sont représentés sur les figures [[#^figure19|19]] et [[#^figure20|20]].
> Nous remarquons que, dans les trois cas, la composante continue du signal est éliminée. La réponse à un signal créneau présente une discontinuité d'amplitude 1 V identique à celle du signal d'entrée.
> ==**Le filtre passe-haut transmet sans atténuation les discontinuités de signal et élimine sa composante continue.**==
> - Si $f \ll f_B$, le signal de sortie est d'amplitude faible dans le cas d'un signal triangulaire. En revanche, pour le signal créneau, il présente deux pics d'amplitude 1 V à chaque discontinuité du signal d'entrée.
> - Dans le cas où $f$ est de l'ordre de $f_B$, les signaux transmis sont très déformés.
> - Si $f$ est grand devant $f_B$, les signaux de sortie sont proches du signal d'entrée sans sa composante continue.
> 
> Remarque : Un filtre passe-haut du premier ordre est utilisé dans les oscilloscopes en mode AC (Alternative Current).
> Dans ce mode, le signal visualisé est déformé si sa fréquence n'est pas très supérieure à la fréquence de coupure basse du filtre (de l'ordre de 10 Hz).
> Le mode AC doit être utilisé avec précaution et pour des signaux de fréquence supérieure à 100 Hz.
> - Interprétation : Un filtre passe-haut élimine la composante continue et atténue de façon sensible les signaux sinusoïdaux de fréquence inférieure à $f_B$, les signaux de fréquence supérieure à $f_B$ sont transmis. La discontinuité de signal est due à la présence d'harmoniques de rang élevé et d'amplitude en $\frac{1}{n}$. Leur transmission sans atténuation explique donc la discontinuité du signal de sortie.
> 	- Si $f \ll f_B$, une grande partie des harmoniques du signal est atténuée ([[#^figure21|fig. 21]]). Seuls les harmoniques de rang $n$ élevé sont transmis : ceux du signal triangulaire sont en $\frac{1}{n^{2}}$, donc d'amplitude très faible, le signal de sortie est très faible, ceux du signal créneau en $\frac{1}{n}$ créent la discontinuité d'amplitude 1 V.
> 	- Si $f$ est de l'ordre de $f_B$, le continu et le fondamental sont éliminés, les autres harmoniques sont transmis ([[#^figure22|fig. 22]]). Le signal de sortie ne ressemble pas au signal d'entrée.
> 	- Si $f \gg f_B$, seule la composante continue du signal est éliminée. Les différents harmoniques sont transmis par le filtre.
> 
> Remarque : $f \ll f_B$, nous pouvons vérifier que, avec un signal d'entrée en triangle, le spectre du signal de sortie est équivalent au spectre d'un signal créneau, avec des harmoniques en $\frac{1}{n}$.
> On retrouve ainsi le caractère dérivateur du filtre passe-haut d'ordre un.

> [!note] Effet d'un filtre passe-bande sur un signal périodique
> Étudions l'effet d'un filtre passe-bande à bande étroite (Q = 10) dans trois cas particuliers de signal périodique :
> - $f < f_0$ : fréquence inférieure à la fréquence caractéristique du filtre ;
> - $f = f_0$ : fréquence égale à la fréquence caractéristique ;
> - $f > f_0$ : signal de fréquence supérieure à la fréquence caractéristique du filtre ;
> 
> Dans tous les cas, le signal ne présente pas de discontinuité et sa composante continue est éliminée ([[#^figure23|fig. 23]] et [[#^figure24|24]]).
> Le signal de sortie est soit d'amplitude très faible (si $f$ est très différent de $f_0$), soit pratiquement sinusoïdal (si $f$ est voisin de $f_0$).
> ==**Un filtre passe-bande à bande étroite ne transmet que les composantes sinusoïdales de fréquence voisine de la fréquence de résonance $f_0$ du filtre. Il élimine la composante continue et les discontinuités.**==
> Remarque : Il faut tenir compte de la modification d'échelle pour apprécier l'atténuation du signal de sortie.
> 
> Interprétation : Un filtre passe-bande atténue les composantes sinusoïdales en dehors de sa bande passante comprise entre les fréquences $f_B$ et $f_H$ ; rappelons que $f_H - f_B = \frac{f_0}{Q}$. L'harmonique de rang $n$ du signal sera transmis sans atténuation importante si : $\frac{f_B}{f} < n < \frac{f_H}{f}$. Le nombre d'harmoniques transmis est de l'ordre de : $\frac{f_H - f_B}{f} = \frac{\Delta f}{f} = \frac{f_0}{Qf}$ ($\Delta f$ largeur de bande passante du filtre et $Q$ coefficient de qualité).
> Trois cas se présentent suivant la valeur de $\frac{\Delta f}{f} = \frac{f_0}{Qf}$ :
> - $\frac{f_0}{Qf} \gg 1$ : de nombreux harmoniques sont dans la bande passante du filtre ;
> - $\frac{f_0}{Qf} \approx 1$ : peu d'harmoniques sont dans la bande passante du filtre ;
> - $\frac{f_0}{Qf} \ll 1$ : un ou aucun harmonique est dans la bande passante du filtre ;
> 
> Remarque : La résonance aiguë (Q = 10) masque le caractère dérivateur du filtre passe-bande pour $f \ll f_0$ en amplifiant les harmoniques 19 et 21.
> - Si $f = \frac{f_0}{20}$ : Les harmoniques de rang voisin de 20 sont transmis. Leur superposition donne dans le cas d'une excitation en créneau un signal de type pseudo-périodique de fréquence $f_0$.
> - Si $f = f_0$ : Seul le fondamental est transmis. Le signal de sortie est quasi sinusoïdal.
> - Si $f = 20f_0$ : Le signal de sortie, très atténué, est une fonction triangle pour une attaque en créneau. On retrouve le caractère intégrateur d'un passe-bande d'ordre deux pour $f \gg f_0$.
# Diagrammes
Filtre passe-bas d'ordre un
![[figure307.png]]^figure10

Détermination du signal de sortie d'un filtre linéaire
![[figure311.png]]^figure14
# Graphiques
Créneau impair et de rapport cyclique $\frac{1}{2}$
![[figure298.png]]^figure1

Créneau pair et de rapport cyclique $\frac{1}{2}$
![[figure299.png]]^figure2

Triangle pair et de rapport cyclique $\frac{1}{2}$
![[figure300.png]]^figure3

Sinusoïde redressée double alternance
![[figure301.png]]^figure4

Spectre de fréquence d'un signal périodique
![[figure302.png]]^figure5

Synthèse d'un signal triangulaire
![[figure303.png]]^figure6

Synthèse d'un signal redressé simple alternance
![[figure304.png]]^figure7

 Mise en évidence du phénomène de Gibbs sur un signal carré
 ![[figure305.png]]^figure8

Mise en évidence du phénomène de Gibbs sur une rampe périodique
![[figure306.png]]^figure9

$u_e(t)$
![[figure308.png]]^figure11

Valeur approchée de $v_s(t)$ pour $p_{max} = 5$
![[figure309.png]]^figure12

Valeur approchée de $v_s(t)$ pour $p_{max} = 20$
![[figure310.png]]^figure13

Filtre passe-bas du premier ordre. Réponse d'un signal triangulaire d'amplitude crête-crête 1 V, de fréquence $f$ égale à $\frac{f_H}{20}$, $f_H$ et $20f_H$, superposé à une composante continue de 0,1 V
![[figure312.png]]^figure15

Filtre passe-bas du premier ordre. Réponse d'un signal en créneaux d'amplitude crête-crête 1 V, de fréquence $f$ égale à $\frac{f_H}{20}$, $f_H$ et $20f_H$, superposé à une composante continue de 0,1 V
![[figure313.png]]^figure16

Filtre passe-bas du premier ordre. Réponse d'un signal en créneaux d'amplitude crête-crête 1 V, de fréquence $f_H$, superposé à une composante continue de 0,1 V
![[figure314.png]]^figure17

Filtre passe-bas du premier ordre. Réponse d'un signal en créneaux d'amplitude crête-crête 1 V, de fréquence $f = 20f_H$, superposé à une composante continue de 0,1 V
![[figure315.png]]^figure18

Filtre passe-haut du premier ordre. Réponse d'un signal triangulaire d'amplitude crête-crête 1 V, de fréquence $\frac{f_B}{20}$, $f_B$ et $20f_B$, superposé à une composante continue de 0,1 V
![[figure316.png]]^figure19

Filtre passe-haut du premier ordre. Réponse d'un signal créneau d'amplitude crête-crête 1 V, de fréquence $\frac{f_B}{20}$, $f_B$ et $20f_B$, superposé à une composante continue de 0,1 V
![[figure317.png]]^figure20

Filtre passe-haut du premier ordre. Réponse d'un signal en créneaux d'amplitude crête-crête 1 V, de fréquence $\frac{f_B}{20}$, superposé à une composante continue de 0,1 V. Analyse des harmoniques du signal d'entrée et du signal de sortie.
![[figure318.png]]^figure21

Filtre passe-haut du premier ordre. Réponse d'un signal en créneaux d'amplitude crête-crête 1 V, de fréquence $f_B$, superposé à une composante continue de 0,1 V. Analyse des harmoniques du signal d'entrée et du signal de sortie.
![[figure319.png]]^figure22

Filtre passe-bande de coefficient de qualité $Q = 10$. Réponse d'un signal triangulaire d'amplitude crête-crête 1 V, de fréquence $\frac{f_0}{20}$, $f_0$ et $20f_0$, superposé à une composante continue de 0,1 V
![[figure320.png]]^figure23

Filtre passe-bande de coefficient de qualité $Q = 10$. Réponse d'un signal en créneau d'amplitude crête-crête 1 V, de fréquence $\frac{f_0}{20}$, $f_0$ et $20f_0$, superposé à une composante continue de 0,1 V
![[figure321.png]]^figure24
# Expériences
> [!warning]
> Voici des exemples de travaux pratiques qui abordent le sujet de ce chapitre : le [lien 1](https://ressources.unisciel.fr/sillages/physique/electronique_2a_pc/res/TP_Analyse_de_Fourier.pdf), le [lien 2](https://www.physagreg.fr/tp/TP4_filtres.pdf), le [lien 3](https://fr.scribd.com/document/833271293/TP1-Analyseur-de-spectre-correction), le [lien 4](https://chamilo.grenoble-inp.fr/courses/PHELMA3PMKTET0/document/Docs_site/sujets-TP-Techniques-experimentales-et-mesures/TP4-Associations_d_etages.pdf), le [lien 5](http://www.seigne.free.fr/TP/TPOscilloFilt2.pdf), le [lien 6](https://fr.scribd.com/document/148515491/TP-Analyse-de-Fourier), le [lien 7](https://www.lias-lab.fr/perso/fredericlaunay/Cours/T1/T1_TP1&2_Fourier.pdf).
# Autres notes
