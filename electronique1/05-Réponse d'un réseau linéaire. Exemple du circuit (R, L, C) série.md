---
titre: "[[05-Réponse d'un réseau linéaire. Exemple du circuit (R, L, C) série]]"
tags:
  - régime-libre
  - circuit-R-C
  - circuit-R-L
  - circuit-R-L-C
  - réponse-à-un-échelon-de-tension
crée: 10-11-2025, 08:24
---
Dans ce chapitre, nous assimilerons les condensateurs et les bobines à leurs modèles idéalisés et nous noterons par $0_-$ et $0_+$ les instants juste avant et juste après l'instant initial $t = 0$.
==**Le régime libre, ou régime propre, d'un circuit est le régime que nous observons lorsque ses sources libres sont éteintes.**==
# Formules
> [!note] Régime libre du circuit (R, C)
> Considérons le montage de la [[#^figure1|figure 1]].
> Équations différentielles : $\dfrac{du}{dt} + \frac{u}{RC} = 0$ ou $\dfrac{di}{dt} + \frac{i}{RC} = 0$.
> - Le temps caractéristique du circuit (R, C) est le temps de relaxation $\tau = RC$.
> - Le circuit (R, C) est un circuit du premier ordre de constante de temps $RC$, car les équations différentielles vérifiées par l'intensité et la différence de potentiel sont linéaires du premier ordre.
> 
> La solution générale de l'équation différentielle vérifiée par $u$ est : $u(t) = Ae^{-\frac{t}{\tau}}$, pour $t > 0$. La continuité de $u$ aux bornes du condensateur nous permet d'affirmer que la constante $A$ vaut $u_0$.
> Finalement, $u(t) = u_0$ pour $t < 0$ et $u(t) = u_0e^{-\frac{t}{RC}}$ pour $t > 0$.
> Sur le tracé $\frac{u}{u_0}$ en fonction de $\frac{t}{\tau}$, nous remarquons que la tangente à l'origine coupe l'axe horizontal en $\frac{t}{\tau} = 1$. Dans le tracé u en fonction de t, elle couperait l'axe des $t$ en $\tau$. Ce résultat est utilisé pour mesurer expérimentalement $\tau$.
> La propriété est vraie à un instant $t_0$ quelconque : la tangente à la courbe $u(t)$ à l'instant $t_0$ coupe l'axe des $t$, c'est-à-dire l'asymptote, en $t_0 + \tau$.
> Dès que $t$ est de l'ordre de quelques $\tau$, $\frac{u}{u_0}$ prend des valeurs négligeables ([[#^figure2|fig. 2]]).
> En utilisant $i(t) = C\dfrac{du}{dt}$, nous obtenons : $i(t) = 0$ pour $t < 0$ et $i(t) = -\frac{u_0}{R}e^{-\frac{t}{RC}}$ pour $t > 0$ ([[#^figure3|fig. 3]]).
> Nous remarquons que $i$ est discontinue à l'instant $t = 0$.
> Cette discontinuité est liée à la modélisation du circuit par un résistor et une capacité idéale. Dans un circuit réel, la résistance et le condensateur possèdent des coefficients d'inductance non nuls. La présence de ces inductances élimine la discontinuité de $i$. De ce fait, la relation $i(t) = -\frac{u_0}{R}e^{-\frac{t}{RC}}$ n'est pas rigoureusement valable au voisinage immédiat de $t = 0$.
> Nous pouvons faire les mêmes remarques sur la tangente à l'origine et le temps de décroissance sur le tracé $\frac{i}{i_0}$ que celles qui ont été faites sur le tracé de $\frac{u}{u_0}$.
> Calculons l'énergie $\mathcal{E}$ dissipée par effet Joule dans le résistor $R$ : $\displaystyle \mathcal{E} = \int_{0}^{+\infty} Ri^{2}dt = \frac{1}{2}Cu_0^{2}$.
> Cette énergie est l'énergie du condensateur à l'instant initial.
> L'énergie emmagasinée à l'instant initial dans le condensateur est intégralement dissipée par effet Joule dans le résistor.
 
> [!note] Régime libre du circuit (R, L)
> Considérons le montage théorique de la [[#^figure4|figure 4]].
> Équations différentielles : $\dfrac{di}{dt} + \frac{R}{L}i = 0$ ou $\dfrac{du}{dt} + \frac{R}{L}u = 0$.
> Le temps caractéristique du circuit (R, L) est le temps de relaxation : $\tau = \frac{L}{R}$. Ce circuit est un circuit du premier ordre de constante de temps $\frac{L}{R}$.
> La solution générale de l'équation différentielle vérifiée par $i$ est : $i(t) = Ae^{-\frac{t}{\tau}}$ pour $t > 0$. La continuité de $i$ nous permet d'affirmer que la constante $A$ vaut $i_0$.
> Finalement, $i(t) = i_0$ pour $t < 0$ et $i(t) = i_0e^{-\frac{Rt}{L}}$ pour $t > 0$.
> En utilisant $u(t) = L\dfrac{di}{dt}$, nous obtenons : $u(t) = 0$ pour $t < 0$ et $u(t) = -Ri_0e^{-\frac{R}{L}t}$ pour $t > 0$. 
> Les tracés $\frac{i}{i_0}$ et $\frac{u}{Ri_0}$ en fonction de $\frac{t}{\tau}$ sont presque les mêmes que celle du circuit (R, C) ainsi que les remarques sur la tangente à l'origine et la décroissance de $i$.
> Nous remarquons que $u$ est discontinue à l'instant $t = 0$.
> Dans un montage expérimental, cette discontinuité de $u$ n'apparaît pas principalement à cause des capacités parasites de la bobine et de l'interrupteur. De ce fait, la relation $u(t) = -Ri_0e^{-\frac{R}{L}t}$ n'est pas valable au voisinage immédiat de $t = 0$.
> Calculons l'énergie $\mathcal{E}$ dissipée par effet Joule dans le résistor $R$ : $\displaystyle \mathcal{E} = \int_{0}^{+\infty} Ri^{2}dt = \frac{1}{2}Li_0^{2}$.
> Cette énergie est l'énergie de la bobine à l'instant initial.
> L'énergie emmagasinée à l'instant initial dans la bobine est intégralement dissipée par effet Joule dans le résistor.

> [!note] Régime libre du circuit (R, L, C) série
> Considérons le circuit représenté sur la [[#^figure5|figure 5]].
> Équations différentielles : $\dfrac{d^{2}q}{dt^{2}} + \frac{\omega_0}{Q}\dfrac{dq}{dt} + \omega_{0}^{2}q = 0$, $\dfrac{d^{2}u}{dt^{2}} + \frac{\omega_0}{Q}\dfrac{du}{dt} + \omega_{0}^{2}u = 0$ et $\dfrac{d^{2}i}{dt^{2}} + \frac{\omega_0}{Q}\dfrac{di}{dt} + \omega_{0}^{2}i = 0$.
> Le circuit (R, L, C) série est un circuit du second ordre ; il est caractérisé par deux grandeurs caractéristiques :
> - sa pulsation propre $\omega_0 = \frac{1}{\sqrt{LC}}$ ;
> - son facteur de qualité $Q = \frac{L\omega_0}{R} = \frac{1}{RC\omega_0}$ qui est un nombre sans dimension.
> 
> La solution générale d'une équation différentielle d'ordre deux fait intervenir deux constantes arbitraires, que l'on détermine à partir des conditions initiales. Il faut donc connaître la valeur de la fonction cherchée et celle de sa dérivée à l'instant $0_+$.
> Pour cela, nous exprimons que la tension aux bornes du condensateur ainsi que l'intensité qui traverse la bobine sont des fonctions continues du temps. Par la suite, nous noterons : $u_0 = u_0 = \frac{q_0}{C}$ et $i_{0} = i_0$.
> Exemple de détermination des conditions initiales : Considérons le montage théorique de la [[#^figure6|figure 6]], où l'interrupteur est fermé depuis un temps infini. On a atteint un régime continu où les dérivées par rapport au temps sont nulles. Le condensateur est équivalent à un interrupteur ouvert et la bobine idéale à un fil sans résistance ([[#^figure7|fig. 7]]). On en déduit les valeurs : $i = -\frac{e_0}{R}$ et $u_c = e_0$.
> Ouvrons l'interrupteur à l'instant $t = 0$. L'intensité $i(t)$ et la tension $u_C(t)$ étant des fonctions continues, nous pouvons écrire : $u_C(0_+) = u_C(0_-) = e_0$ et $i(0_+) = i(0_-) = -\frac{e_0}{R}$.
> Maintenant que l'interrupteur est ouvert, le courant i passe dans la branche du condensateur ; nous pouvons donc écrire en faisant attention aux orientations, les deux conditions initiales recherchées : $u_0 = e_0$ et $i_0 = C\left(\dfrac{du_C}{dt}\right)_{0_+} = \frac{-e_0}{R}$.

> [!note] Étude du régime libre du circuit (R, L, C)
> L'étude du régime libre fait intervenir le coefficient de qualité $Q$. Nous parlerons aussi d'amortissement : un circuit est très amorti quand sa résistance est grande (soit $Q \approx 0$) et est peu amorti quand sa résistance est faible (soit $Q \gg 1$).
> Résolvons l'équation différentielle en $q(t)$. Nous savons que sauf cas particulier, la solution de cette équation différentielle est de la forme $q(t) = A_1e^{r_1t} + A_2e^{r_2t}$, où $A_1$ et $A_2$ sont des constantes pouvant être complexes et $r_1$ et $r_2$ sont les racines de l'équation caractéristique associée à l'équation différentielle $r^{2} + \frac{\omega_0}{Q}r + \omega_{0}^{2} = 0$.
> Dans le cas particulier où $r_1 = r_2 = r$, la solution est de la forme : $q(t) = (At + B)e^{rt}$. Les constantes réelles $A$ et $B$ sont fixées par les deux conditions initiales.
> Nous pouvons donc envisager trois cas suivant le signe du discriminant réduit de l'équation caractéristique $\Delta' = \omega_{0}^{2}\left(\frac{1}{4Q^{2}} - 1\right)$ :
> - $\Delta > 0$ ou $Q < 1/2$ : régime apériodique : Les deux racines $r_1$ et $r_2$ sont réelles négatives. Une étude mathématique de la solution donnerait les résultats suivants ([[#^figure8|fig. 8]]) :
> 	- $q(t)$ ne peut pas s'annuler plus d'une fois ;
> 	- $q(t)$ ne peut pas prendre plus de deux fois la même valeur et ne présente qu'un extremum au plus ;
> 	- quand $t$ tend vers l'infini, $q(t)$ tend vers 0.
> 	Il en est de même pour les grandeurs $i(t)$, $u_L(t)$, $u_C(t)$ et $u_R(t)$.
> Nous remarquons que la « durée » du régime apériodique (temps pendant lequel $q$ prend des valeurs non négligeables) est d'autant plus grande que $Q$ est proche de 0 ([[#^figure8|fig. 8]] et [[#^figure9|9]]).
> - $\Delta = 0$ ou $Q = 1/2$ : régime critique : Dans ce cas purement théorique (physiquement il est impossible de fixer $Q$ exactement à la valeur 0,5), la solution de l'équation différentielle est de la forme : $q(t) = (At + B)e^{-\omega_0 t}$. $q(t)$ tend vers 0 quand $t$ tend vers l'infini avec une constante de temps $\tau = \frac{1}{\omega_0}$. Le régime critique correspond au régime apériodique de « durée » minimale. L'allure des courbes correspondant à ce régime est voisine de celle des régimes apériodiques ([[#^figure8|fig. 8]]).
> - $\Delta < 0$ ou $Q > 1/2$ : régime pseudo-périodique : Les racines de l'équation caractéristique sont complexes et conjuguées. La solution générale de l'équation différentielle peut s'écrire sous les formes suivantes : $q(t) = e^{-\frac{t}{\tau}}(\alpha e^{i\omega t} + \beta e^{-i\omega t})$, $q(t) = e^{-\frac{t}{\tau}}(A\cos\omega t + B\sin\omega t)$ ou $q(t) = ae^{-\frac{t}{\tau}}\cos(\omega t + \varphi)$. $q(t)$ se présente donc sous la forme d'une fonction oscillante modulée par une enveloppe exponentielle décroissante ([[#^figure10|fig. 10]] et [[#^figure11|11]]). Le régime libre est un régime transitoire de temps caractéristique $\tau = \frac{2Q}{\omega_0}$. Il en est de même pour les grandeurs $i(t)$, $u_L(t)$, $u_C(t)$ et $u_R(t)$. La période $T = \frac{2\pi}{\omega} = \frac{2\pi}{\omega_0 \sqrt{1 - \frac{1}{4Q^{2}}}}$ de la fonction sinusoïdale est appelée pseudo-période du régime libre. Elle est telle que $q(t + T) = q(t)e^{-\frac{T}{\tau}}$.
> Remarque : Le rapport $\frac{q(t + T)}{q(t)}$ est constant et nous appellerons décrément logarithmique la quantité : $\delta = \ln\left(\frac{q(t)}{q(t + T)}\right) = \frac{T}{\tau} = \frac{2\pi}{\sqrt{4Q^{2} - 1}}$. La mesure de cette grandeur permet de calculer le coefficient de qualité du circuit.
> Nous remarquons sur les tracés ([[#^figure12|fig. 12]] et [[#^figure13|13]])que le retour vers l'état d'équilibre $q = 0$ est d'autant plus lent que $Q$ est grand et que la pseudo-période diminue quand $Q$ augmente.
> Dès que $Q > 4$, elle est voisine de $\frac{2\pi}{\omega_0}$ avec un écart relatif de moins de 1 %.
> 
> En conclusion, nous pouvons affirmer que : Le régime libre est un régime transitoire dont le temps caractéristique est minimal pour le régime critique $\left(Q = \frac{1}{2}\right)$ et est très grand pour des circuits très amortis $(Q \approx 0)$ ou des circuits peu amortis $(Q \gg 1)$.

> [!note] Étude énergétique du régime libre du circuit (R, L, C)
> Si nous multiplions par i l'équation différentielle vérifiée par $q(t)$ , nous obtenons : $\dfrac{d}{dt}\left(\frac{1}{2}Li^{2} + \frac{1}{2}\frac{q^{2}}{C}\right) = -Ri^{2}$. Nous pouvons interpréter cette relation de la façon suivante : $\mathcal{E} = \frac{1}{2}Li^{2} + \frac{1}{2}\frac{q^{2}}{C}$ représente l'énergie emmagasinée dans la bobine et le condensateur, et constitue une fonction positive décroissante du temps. Cette énergie est dissipée par effet Joule dans le résistor et le bilan énergétique du circuit s'écrit $\dfrac{d\mathcal{E}}{dt} = -P_{Joule}$.
> - Cas du régime non amorti : L'équation différentielle vérifiée par $q(t)$ est alors : $\dfrac{d^{2}q}{dt^{2}} + \omega_{0}^{2}q = 0$. La solution générale est : $q(t) = q_0\cos(\omega_0 t + \varphi)$ et $i(t) = -\omega_0q_0\sin(\omega_0 t + \varphi)$. L'énergie emmagasinée dans le condensateur vaut $\mathcal{E}_C = \frac{1}{2}\frac{q_{0}^{2}}{C}\cos^{2}(\omega_0 t + \varphi)$ et celle dans la bobine $\mathcal{E}_L = \frac{1}{2}\frac{q_{0}^{2}}{C}\sin^{2}(\omega_0 t + \varphi)$. Nous remarquons que $\mathcal{E}_C + \mathcal{E}_L$ est constante et que l'énergie « oscille » entre le condensateur et la bobine, sans pertes.
> - Cas du régime pseudo-périodique faiblement amorti : Pour un circuit peu amorti $(Q \gg 1)$ : $\omega \approx \omega_0$ et $\frac{1}{\tau} \ll \omega_0$. On a alors $q(t) \approx ae^{-\frac{t}{\tau}}\cos(\omega_0 t + \varphi)$ et $i(t) \approx ae^{-\frac{t}{\tau}}\omega_0\sin(\omega_0 t + \varphi)$. L'énergie emmagasinée dans le condensateur et dans la bobine vaut : $\mathcal{E}(t) \approx \frac{1}{2}\frac{a^{2}}{C}e^{-\frac{2t}{\tau}}$. En une pseudo-période $T$, l'énergie décroît de la quantité : $\Delta\mathcal{E} = \frac{1}{2}\frac{a^{2}}{C}e^{-\frac{2t}{\tau}}\left(1 - e^{-\frac{2T}{\tau}}\right)$, soit, comme $T \approx \frac{2\pi}{\omega_0} \ll \tau$, $\frac{\Delta\mathcal{E}}{\mathcal{E}} \approx \frac{2T}{\tau} = \frac{2\pi}{Q}$, ou encore $Q = 2\pi\frac{\mathcal{E}}{\Delta\mathcal{E}}$.
> Nous en déduisons une interprétation énergétique du facteur de qualité $Q$ (quand il est grand devant 1). Le facteur de qualité est égal à $2\pi$ fois l'énergie emmagasinée dans le circuit divisée par l'énergie dissipée pendant une pseudo-période : cette définition peut s'appliquer à tout système physique (oscillateur mécanique, cavité résonante...).
> Sur les courbes tracées ([[#figure14|fig. 14]] et [[#^figure15|15]]), nous remarquons que pour $Q = 10$, l'énergie a une décroissance sensiblement exponentielle, ce qui n'est pas le cas pour $Q = 2$.

> [!note] Réponse à un échelon de tension
> Nous supposons dans ce paragraphe que le générateur du circuit délivre une f.e.m. de valeur nulle pour les temps négatifs et de valeur non nulle et égale à $e_0$ pour les temps positifs. Il délivre un échelon de tension ([[#^figure16|fig. 16]]).
> Un échelon de tension peut être réalisé à l'aide d'une source de tension constante et d'un interrupteur à deux positions que l'on bascule à l'instant $t = 0$ ([[#^figure17|fig. 17]]).
> - Charge d'un condensateur : L'application de la loi des mailles dans le circuit de la [[#^figure18|figure 18]] donne : $u(t) + RC\dfrac{du}{dt} = e(t)$. La solution générale de l'équation est alors $u(t) = e_0 + Ae^{-\frac{t}{RC}}$ pour $t > 0$. Nous savons que la différence de potentiel aux bornes d'un condensateur est continue. Donc si initialement le condensateur est non chargé, $u(0_+) = 0$. Nous en déduisons : $u(t) = 0$ pour $t < 0$ ; $u(t) = e_0\left(1 - e^{-\frac{t}{RC}}\right)$ pour $t \geqslant 0$ ([[#^figure19|fig. 19]]). Du coup, $i(t) = 0$ pour $t < 0$ et $i(t) = \frac{e_0}{R}e^{-\frac{t}{RC}}$ pour $t \geqslant 0$ ([[#^figure20|fig. 20]]).
> Nous remarquons qu'après un temps de l'ordre de quelques $\tau = RC$ , la tension aux bornes de $C$ est pratiquement constante et correspond à la valeur du régime établi (le condensateur est un circuit ouvert en régime indépendant du temps). Corrélativement, le courant dans le circuit décroît et s'annule.
> <mark style="color: red">Après un régime transitoire d'une durée de l'ordre de $\tau$, l'état du circuit correspond au régime établi indépendant du temps. La durée du régime transitoire chiffre le retard à l'établissement de la différence de potentiel aux bornes de la capacité.</mark>
> Reprenons l'équation d'évolution sous la forme : $e(t) = Ri(t) + \frac{q(t)}{C}$ et multiplions-la membre à membre par $i(t)$ où nous pouvons identifier : $\mathcal{P}_{\begin{subarray}{l} \text{fournie par } \\ \text{le générateur}\end{subarray}} = \mathcal{P}_{\begin{subarray}{l} \text{dissipée dans} \\ \text{la résistance} \\ \text{par effet Joule}\end{subarray}} + \mathcal{P}_{\begin{subarray}{l} \text{emmagasinée} \\ \text{dans le condensateur}\end{subarray}}$. Dans le cas de la charge envisagée, l'énergie totale fournie par le générateur est : $\displaystyle \mathcal{E}_{gén} = \int_{0}^{\infty} \mathcal{P}_{gén} dt = e_0 \int_{0}^{\infty} i dt = e_0 . q_{finale} = Ce_{0}^{2}$. C'est le double de l'énergie accumulée dans le condensateur. La moitié de l'énergie fournie par le générateur est donc dissipée par effet Joule dans la résistance.
> - Établissement du courant dans un circuit inductif : L'application de la loi des mailles dans le circuit de la [[#^figure21|figure 21]] donne : $i(t) + \frac{L}{R}\dfrac{di}{dt} = \frac{e(t)}{R}$. La solution générale de l'équation est alors $i(t) = \frac{e_0}{R} + Ae^{-\frac{R}{L}t}$ pour $t \geqslant 0$. Nous savons que l'intensité traversant une bobine est continue. Comme initialement le courant traversant $L$ est nul, $i(0_+) = 0$. Nous en déduisons $i(t) = 0$ pour $t < 0$, $i(t) = \frac{e_0}{R}\left(1 - e^{-\frac{R}{L}t}\right)$ pour $t \geqslant 0$ ([[#^figure22|fig. 22]]). Donc $u(t) = e_0e^{-\frac{R}{L}t}$ ([[#^figure23|fig. 23]]).
> Nous remarquons qu'après un temps de l'ordre de quelques $\tau = \frac{L}{R}$, l'intensité dans le circuit est pratiquement constante et correspond à la valeur du régime établi (la bobine est un court-circuit en régime indépendant du temps). Corrélativement, la différence de potentiel aux bornes de la bobine décroît et s'annule.
> <mark style="color: red">Après un régime transitoire d'une durée de l'ordre de $\tau$, l'état du circuit correspond au régime établi indépendant du temps. La durée du régime transitoire chiffre le retard à l'établissement du courant dans la bobine.</mark>
> - Cas du circuit (R, L, C) série : L'application de la loi des mailles dans le circuit de la figure 24 donne : $\dfrac{d^{2}q}{dt^{2}} + \frac{\omega_0}{Q}\dfrac{dq}{dt} + \omega_{0}^{2}q = \frac{e(t)}{L} = C\omega_{0}^{2}e(t)$. Dans le cas d'un échelon de tension, $q(t) = Ce_0$ est une solution particulière de l'équation différentielle. Sa superposition à la solution générale de l'équation sans second membre donne les courbes suivantes compte tenu des conditions initiales.
> Interprétons les courbes des figures [[#^figure24a|24a]], [[#^figure24b|b]], [[#^figure24c|c]] et [[#^figure25a|25a]], [[#^figure25b|b]], [[#^figure25c|c]].
> À $t = 0$, $q(t)$ est nulle et présente une tangente horizontale. Nous vérifions ainsi la continuité de $q(t)$ (caractéristique du condensateur) et de $i(t)$ (caractéristique de la bobine).
> À $t = 0$, $u_C(t)$ est continue et présente une tangente horizontale, $u_R(t)$ est continue et $u_L(t)$ est discontinue. En effet, $u_C(t) = \frac{q}{C}$ et $u_R(t) = Ri(t)$ présentent les mêmes propriétés de continuité que $q(t)$ et $i(t)$ respectivement.
> Quand $t$ est grand, $q(t)$ tend vers $Ce_0$ solution particulière de l'équation.
> C'est le régime établi indépendant du temps.

> [!note] Réalisation expérimentale : réglage de l'oscilloscope
> Le phénomène à étudier n'étant pas périodique, il ne peut être étudié en temps réel.
> Nous devons utiliser un oscilloscope numérique pour étudier une des tensions du circuit : $u_R(t)$, $u_C(t)$ ou $u_L(t)$.
> Il faut tout d'abord régler correctement l'oscilloscope.
> - Sensibilité verticale : la courbe doit occuper une part notable de l'écran sans déborder.
> - Vitesse de balayage : il faut afficher $u(t)$ entre 0 et $t_{max}$, qui est de l'ordre de quelques $\tau$. Connaissant la valeur approximative de $\tau$, on choisit la vitesse de balayage. Si par exemple $\tau \approx 1\, ms$, on choisira $500\, \mu s$ par division.
> - Niveau et pente de synchronisation : l'affichage se déclenche lorsque le signal $u(t)$ passe par le niveau (ou level) avec la pente (slope) positive ou négative selon le signe choisi. Il faut donc fixer le niveau à une valeur comprise entre $u_{min}$ et $u_{max}$ avec une pente de même signe que celle de $u(t)$. Par exemple, si $u$ passe de 0 à -2 V, il faut choisir un niveau compris entre 0 V et -2 V, avec une pente négative.
> Un niveau trop faible est à éviter, car l'enregistrement risque d'être déclenché par un signal parasite. Une fois les réglages choisis, passer en mode monocoup (single) et lancer une acquisition (run). La courbe $u(t)$ s'affiche dès que l'interrupteur est fermé.

> [!note] Réalisation expérimentale : Circuit (R , C)
> Les condensateurs de qualité (les condensateurs électrochimiques de forte capacité ne permettent pas d'effectuer des mesures fiables) ont des capacités d'au plus quelques microfarads.
> L'impédance d'entrée des appareils de mesure (oscilloscope, table traçante, multimètre) est de l'ordre du mégaohm.
> Nous ne pouvons donc pas espérer observer des temps de relaxation supérieurs à la seconde. La solution la meilleure est d'utiliser un oscilloscope à mémoire numérique car ni la table traçante ni le multimètre ne sont adaptés à des mesures pendant des temps courts ([[#^figure26|fig. 26]] et [[#^figure27|27]]).

> [!note] Réalisation expérimentale : Circuit (R , L)
> Les bobines de faible résistance interne ont des inductances de l'ordre de 100 mH au plus. Leur résistance interne est de l'ordre de l'ohm.
> Nous ne pouvons donc pas espérer observer des temps de relaxations supérieurs au dixième de seconde. Nous utiliserons à nouveau un oscilloscope à mémoire numérique. Le réglage du mode de déclenchement de l'oscilloscope est identique à celui du circuit (R , C) ([[#^figure28|fig. 28]] et [[#^figure29|29]]).

> [!note] Réalisation expérimentale : Circuit (R , L, C)
> Les remarques concernant le circuit (R, C) et (R, L) sont toujours valables. Nous réalisons en conséquence le montage de la [[#^figure30|figure 30]]. Les réponses du circuit sont affichées aux figures [[#^figure31a|31a]] et [[#^figure31b|b]].
# Définitions

# Diagrammes
Circuit (R, C)
![[electronique1/attachments-electronique1/figure74.png]]^figure1

Montage d'étude du circuit (R, L)
![[electronique1/attachments-electronique1/figure77.png]]^figure4

Circuit (R, L, C)
![[electronique1/attachments-electronique1/figure78.png]]^figure5

Circuit R, L, C
![[electronique1/attachments-electronique1/figure79.png]]^figure6

Schéma équivalent pour $t < 0$
![[electronique1/attachments-electronique1/figure80.png]]^figure7

Réalisation d'un échelon de tension
![[figure90.png]]^figure17

Circuit d'étude de la charge d'un condensateur à travers une résistance
![[figure91.png]]^figure18

Circuit d'étude de l'établissement du courant à travers une bobine
![[figure94.png]]^figure21

Montage d'étude du circuit (R , C)
![[figure104.png]]^figure27

Montage d'étude du circuit (R , L)
![[figure106.png]]^figure29

Montage d'étude du circuit (R, L, C)
![[figure107.png]]^figure30
# Graphiques
Différence de potentiel aux bornes du condensateur
![[electronique1/attachments-electronique1/figure75.png]]^figure2

Intensité dans le circuit
![[electronique1/attachments-electronique1/figure76.png]]^figure3

Régimes apériodique $(Q < 0,5)$ et critique $(Q = 0,5)$
![[electronique1/attachments-electronique1/figure81.png]]^figure8

d.d.p. aux bornes des trois dipôles : régimes apériodiques $Q = 0,4$
![[electronique1/attachments-electronique1/figure82.png]]^figure9

Régime pseudo-périodique. $Q = 10$ ; $q(0) = q_0$ et $i(0) = 0$
![[electronique1/attachments-electronique1/figure83.png]]^figure10

Régime pseudo-périodique. $Q = 10$ ; $q(0) = 0$ et $i(0) = i_0$
![[electronique1/attachments-electronique1/figure84.png]]^figure11

Régimes pseudo-périodique et critique. Condensateur initialement chargé $i(0) = 0$
![[electronique1/attachments-electronique1/figure85.png]]^figure12

Régimes pseudo-périodique et critique. Intensité initiale $i_0$ dans le circuit
![[electronique1/attachments-electronique1/figure86.png]]^figure13

Énergie dans le circuit (R, L, C) $Q = 2$, $q(0) = q_0$, $i(0) = 0$, $\mathcal{E}_0 = \frac{1}{2}\frac{q_{0}^{2}}{C}$
![[electronique1/attachments-electronique1/figure87.png]]^figure14

Énergie dans le circuit (R , L , C) $Q = 10$, $Q = 2$, $q(0) = q_0$, $i(0) = 0$, $\mathcal{E}_0 = \frac{1}{2}\frac{q_{0}^{2}}{C}$
![[electronique1/attachments-electronique1/figure88.png]]^figure15

Échelon de tension débutant à $t = 0$
![[figure89.png]]^figure16

Différence de potentiel aux bornes de C
![[figure92.png]]^figure19

Intensité dans le circuit
![[figure93.png]]^figure20

Intensité dans le circuit
![[figure95.png]]^figure22

Différence de potentiel aux bornes de la bobine
![[figure96.png]]^figure23

Réponse à un échelon de tension. Régimes apériodiques
![[figure97.png]]^figure24a

Réponse à un échelon de tension. Régimes apériodiques très amortis
![[figure98.png]]^figure24b

Réponse à un échelon de tension. $Q = 0,3$
![[figure99.png]]^figure24c

Réponse à un échelon de tension. Régimes pseudo-périodiques
![[figure100.png]]^figure25a

Réponse à un échelon de tension. Régimes pseudo-périodiques peu amortis
![[figure101.png]]^figure25b

Réponse à un échelon de tension. $Q = 2$
![[figure102.png]]^figure25c

Réponse du circuit (R , C). Balayage horizontal : 2 ms/div ; voie $Y_1$ : 5 V/div ; voie $Y_2$ : 10 V/div
![[figure103.png]]^figure26

Réponse du circuit (R , L). Balayage horizontal : 0,5 ms/div ; voie $Y_1$ : 5 V/div ; voie $Y_2$ : 10 V/div
![[figure105.png]]^figure28

Réponse du circuit (R , L, C). Balayage horizontal : 0,2 ms/div ; voie $Y_1$ : 5 V/div ; voie $Y_2$ : 0,5 V/div ; mode : alt-CH2 ; synchronisation LF
![[figure108.png]]^figure31a

Réponse du circuit (R , L, C) en mode XY. Balayage horizontal : 0,2 ms/div ; voie $Y_1$ : 5 V/div ; voie $Y_2$ : 0,5 V/div ; mode : XY ; synchronisation LF
![[figure109.png]]^figure31b
# Expériences

# Autres notes
