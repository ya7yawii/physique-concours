---
titre: "[[05-Réponse d'un réseau linéaire. Exemple du circuit (R, L, C) série]]"
tags:
aliases:
crée: 10-11-2025, 08:24
---
Dans ce chapitre, nous assimilerons les condensateurs et les bobines à leurs modèles idéalisés et nous noterons par $0_-$ et $0_+$ les instants juste avant et juste après l’instant initial $t = 0$.
==**Le régime libre, ou régime propre, d’un circuit est le régime que nous observons lorsque ses sources libres sont éteintes.**==
# Formules
> [!note] Régime libre du circuit (R, C)
> Considérons le montage de la [[#^figure1|figure 1]].
> Équations différentielles : $\dfrac{du}{dt} + \frac{u}{RC} = 0$ ou $\dfrac{di}{dt} + \frac{i}{RC} = 0$.
> - Le temps caractéristique du circuit (R, C) est le temps de relaxation $\tau = RC$.
> - Le circuit (R, C) est un circuit du premier ordre de constante de temps $RC$, car les équations différentielles vérifiées par l’intensité et la différence de potentiel sont linéaires du premier ordre.
> 
> La solution générale de l’équation différentielle vérifiée par $u$ est : $u(t) = Ae^{-\frac{t}{\tau}}$, pour $t > 0$. La continuité de $u$ aux bornes du condensateur nous permet d’affirmer que la constante $A$ vaut $u_0$.
> Finalement, $u(t) = u_0$ pour $t < 0$ et $u(t) = u_0e^{-\frac{t}{RC}}$ pour $t > 0$.
> Sur le tracé $\frac{u}{u_0}$ en fonction de $\frac{t}{\tau}$, nous remarquons que la tangente à l’origine coupe l’axe horizontal en $\frac{t}{\tau} = 1$. Dans le tracé u en fonction de t, elle couperait l’axe des $t$ en $\tau$. Ce résultat est utilisé pour mesurer expérimentalement $\tau$.
> La propriété est vraie à un instant $t_0$ quelconque : la tangente à la courbe $u(t)$ à l’instant $t_0$ coupe l’axe des $t$, c’est-à-dire l’asymptote, en $t_0 + \tau$.
> Dès que $t$ est de l’ordre de quelques $\tau$, $\frac{u}{u_0}$ prend des valeurs négligeables ([[#^figure2|fig. 2]]).
> En utilisant $i(t) = C\dfrac{du}{dt}$, nous obtenons : $i(t) = 0$ pour $t < 0$ et $i(t) = -\frac{u_0}{R}e^{-\frac{t}{RC}}$ pour $t > 0$ ([[#^figure3|fig. 3]]).
> Nous remarquons que $i$ est discontinue à l’instant $t = 0$.
> Cette discontinuité est liée à la modélisation du circuit par un résistor et une capacité idéale. Dans un circuit réel, la résistance et le condensateur possèdent des coefficients d’inductance non nuls. La présence de ces inductances élimine la discontinuité de $i$. De ce fait, la relation $i(t) = -\frac{u_0}{R}e^{-\frac{t}{RC}}$ n'est pas rigoureusement valable au voisinage immédiat de $t = 0$.
> Nous pouvons faire les mêmes remarques sur la tangente à l’origine et le temps de décroissance sur le tracé $\frac{i}{i_0}$ que celles qui ont été faites sur le tracé de $\frac{u}{u_0}$.
> Calculons l’énergie $\mathcal{E}$ dissipée par effet Joule dans le résistor $R$ : $\displaystyle \mathcal{E} = \int_{0}^{+\infty} Ri^{2}dt = \frac{1}{2}Cu_0^{2}$.
> Cette énergie est l’énergie du condensateur à l’instant initial.
> L’énergie emmagasinée à l’instant initial dans le condensateur est intégralement dissipée par effet Joule dans le résistor.
 
> [!note] Régime libre du circuit (R, L)
> Considérons le montage théorique de la [[#^figure4|figure 4]].
> Équations différentielles : $\dfrac{di}{dt} + \frac{R}{L}i = 0$ ou $\dfrac{du}{dt} + \frac{R}{L}u = 0$.
> Le temps caractéristique du circuit (R, L) est le temps de relaxation : $\tau = \frac{L}{R}$. Ce circuit est un circuit du premier ordre de constante de temps $\frac{L}{R}$.
> La solution générale de l’équation différentielle vérifiée par $i$ est : $i(t) = Ae^{-\frac{t}{\tau}}$ pour $t > 0$. La continuité de $i$ nous permet d’affirmer que la constante $A$ vaut $i_0$.
> Finalement, $i(t) = i_0$ pour $t < 0$ et $i(t) = i_0e^{-\frac{Rt}{L}}$ pour $t > 0$.
> En utilisant $u(t) = L\dfrac{di}{dt}$, nous obtenons : $u(t) = 0$ pour $t < 0$ et $u(t) = -Ri_0e^{-\frac{R}{L}t}$ pour $t > 0$. 
> Les tracés $\frac{i}{i_0}$ et $\frac{u}{Ri_0}$ en fonction de $\frac{t}{\tau}$ sont presque les mêmes que celle du circuit (R, C) ainsi que les remarques sur la tangente à l'origine et la décroissance de $i$.
> Nous remarquons que $u$ est discontinue à l’instant $t = 0$.
> Dans un montage expérimental, cette discontinuité de $u$ n’apparaît pas principalement à cause des capacités parasites de la bobine et de l’interrupteur. De ce fait, la relation $u(t) = -Ri_0e^{-\frac{R}{L}t}$ n'est pas valable au voisinage immédiat de $t = 0$.
> Calculons l’énergie $\mathcal{E}$ dissipée par effet Joule dans le résistor $R$ : $\displaystyle \mathcal{E} = \int_{0}^{+\infty} Ri^{2}dt = \frac{1}{2}Li_0^{2}$.
> Cette énergie est l’énergie de la bobine à l’instant initial.
> L’énergie emmagasinée à l’instant initial dans la bobine est intégralement dissipée par effet Joule dans le résistor.

> [!note] Régime libre du circuit (R, L, C) série
> Considérons le circuit représenté sur la [[#^figure5|figure 5]].
> Équations différentielles : $\dfrac{d^{2}q}{dt^{2}} + \frac{\omega_0}{Q}\dfrac{dq}{dt} + \omega_{0}^{2}q = 0$, $\dfrac{d^{2}u}{dt^{2}} + \frac{\omega_0}{Q}\dfrac{du}{dt} + \omega_{0}^{2}u = 0$ et $\dfrac{d^{2}i}{dt^{2}} + \frac{\omega_0}{Q}\dfrac{di}{dt} + \omega_{0}^{2}i = 0$.
> Le circuit (R, L, C) série est un circuit du second ordre ; il est caractérisé par deux grandeurs caractéristiques :
> - sa pulsation propre $\omega_0 = \frac{1}{\sqrt{LC}}$ ;
> - son facteur de qualité $Q = \frac{L\omega_0}{R} = \frac{1}{RC\omega_0}$ qui est un nombre sans dimension.
> 
> La solution générale d’une équation différentielle d’ordre deux fait intervenir deux constantes arbitraires, que l’on détermine à partir des conditions initiales. Il faut donc connaître la valeur de la fonction cherchée et celle de sa dérivée à l’instant $0_+$.
> Pour cela, nous exprimons que la tension aux bornes du condensateur ainsi que l’intensité qui traverse la bobine sont des fonctions continues du temps. Par la suite, nous noterons : $u_0 = u_0 = \frac{q_0}{C}$ et $i_{0} = i_0$.
> Exemple de détermination des conditions initiales : Considérons le montage théorique de la [[#^figure6|figure 6]], où l’interrupteur est fermé depuis un temps infini. On a atteint un régime continu où les dérivées par rapport au temps sont nulles. Le condensateur est équivalent à un interrupteur ouvert et la bobine idéale à un fil sans résistance ([[#^figure7|fig. 7]]). On en déduit les valeurs : $i = -\frac{e_0}{R}$ et $u_c = e_0$.
> Ouvrons l’interrupteur à l’instant $t = 0$. L’intensité $i(t)$ et la tension $u_C(t)$ étant des fonctions continues, nous pouvons écrire : $u_C(0_+) = u_C(0_-) = e_0$ et $i(0_+) = i(0_-) = -\frac{e_0}{R}$.
> Maintenant que l’interrupteur est ouvert, le courant i passe dans la branche du condensateur ; nous pouvons donc écrire en faisant attention aux orientations, les deux conditions initiales recherchées : $u_0 = e_0$ et $i_0 = C\left(\dfrac{du_C}{dt}\right)_{0_+} = \frac{-e_0}{R}$.

> [!note] Étude du régime libre du circuit (R, L, C)
> L’étude du régime libre fait intervenir le coefficient de qualité $Q$. Nous parlerons aussi d’amortissement : un circuit est très amorti quand sa résistance est grande (soit $Q \approx 0$) et est peu amorti quand sa résistance est faible (soit $Q \gg 1$).
> Résolvons l'équation différentielle en $q(t)$. Nous savons que sauf cas particulier, la solution de cette équation différentielle est de la forme $q(t) = A_1e^{r_1t} + A_2e^{r_2t}$, où $A_1$ et $A_2$ sont des constantes pouvant être complexes et $r_1$ et $r_2$ sont les racines de l'équation caractéristique associée à l'équation différentielle $r^{2} + \frac{\omega_0}{Q}r + \omega_{0}^{2} = 0$.
> Dans le cas particulier où $r_1 = r_2 = r$, la solution est de la forme : $q(t) = (At + B)e^{rt}$. Les constantes réelles $A$ et $B$ sont fixées par les deux conditions initiales.
> Nous pouvons donc envisager trois cas suivant le signe du discriminant réduit de l’équation caractéristique $\Delta' = \omega_{0}^{2}\left(\frac{1}{4Q^{2}} - 1\right)$ :
> - $\Delta > 0$ ou $Q < 1/2$ : régime apériodique :


# Définitions

# Diagrammes
Circuit (R, C)
![[electronique1/attachments-electronique1/figure74.png]]^figure1

Montage d’étude du circuit (R, L)
![[electronique1/attachments-electronique1/figure77.png]]^figure4

Circuit (R, L, C)
![[electronique1/attachments-electronique1/figure78.png]]^figure5

Circuit R, L, C
![[electronique1/attachments-electronique1/figure79.png]]^figure6

Schéma équivalent pour $t < 0$
![[electronique1/attachments-electronique1/figure80.png]]^figure7
# Graphiques
Différence de potentiel aux bornes du condensateur
![[electronique1/attachments-electronique1/figure75.png]]^figure2

Intensité dans le circuit
![[electronique1/attachments-electronique1/figure76.png]]^figure3
# Expériences

# Autres notes
