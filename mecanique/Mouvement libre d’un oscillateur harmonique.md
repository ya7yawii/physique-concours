---
titre: "[[Mouvement libre d'un oscillateur harmonique]]"
tags:
  - oscillateur
  - harmonique
  - amorti
crée: 20-08-2025, 10:43
---
# Formules
> [!note] Oscillateur harmonique
> L'oscillateur harmonique à un degré de liberté évolue dans un puits de potentiel parabolique : $\mathcal{E}_{P}(x) = \mathcal{E}_{P}(0) + \frac{1}{2}kx^{2}$
> Il est soumis à une force de rappel linéaire : $F(x) = -kx$
> Son équation du mouvement est : $\dfrac{d^{2}x}{dt^{2}} + \omega_{0}^{2}x = 0$, avec $\omega_{0} = \sqrt{\frac{k}{m}}$. 
> La solution générale de cet équation est : $x(t) = A_1\cos(\omega_0t) + A_2\sin(\omega_0t)$ où $A_1$ et $A_2$ sont des constantes d'intégration que l'on déterminera à partir des conditions initiales : $x(0) = x_0$ et $\left(\dfrac{dx}{dt}\right)_{t = 0} = v_0$
> Ainsi, $x(t) = x_0\cos(\omega_0t) + \frac{v_0}{\omega_0}\sin(\omega_0t)$
> qui peut encore s'écrire : $x(t) = x_m\cos(\omega_0t + \phi)$ avec $x_m = \sqrt{x_{0}^{2} + \left(\frac{v_0}{\omega_0}\right)^{2}}$ et $\tan\phi = -\frac{v_0}{\omega_0x_0}$
> La période, appelée période propre des oscillations de l'oscillateur est : $T_0 = \frac{2\pi}{\omega_0}$. Cette période est indépendante de l'amplitude des oscillations. Il y a isochronisme des oscillations.
> La trajectoire de phase de l'oscillateur harmonique décrit une ellipse d'équation : $\left(\frac{x}{x_m}\right)^{2} + \left(\frac{v}{\omega_0x_m}\right)^{2} = 1$. Celle-ci peut même se ramener à un cercle de rayon $x_m$ si nous portons la variable $\frac{v}{\omega_0}$ sur l'axe des ordonnées ([[#^figure1]]).
> Le caractère circulaire de la trajectoire de phase tracée dans les axes $\left(O\hspace{0.4em};\hspace{0.4em} x,\hspace{0.4em}\frac{v}{\omega_0}\right)$ permet un test visuel simple du caractère harmonique d'un oscillateur.
> La trajectoire de phase limite séparant les états liés (oscillations plus ou moins harmoniques) et les états de diffusion est appelée <mark style="color: red">séparatrice</mark>.
> L'énergie mécanique de l'oscillateur est constante : $\mathcal{E}_M = \mathcal{E}_K + \mathcal{E}_P = \frac{1}{2}kx_{m}^{2}$ 

>[!note] Équipartition de l'énergie potentielle et de l'énergie cinétique
> Durant le mouvement, il y a échange permanent des formes cinétique et potentielle de l'énergie. Donc, il y a équipartition, en moyenne, de l'énergie potentielle et de l'énergie cinétique : $\langle\mathcal{E}_P\rangle = \langle\mathcal{E}_K\rangle = \frac{\mathcal{E}_M}{2}$.

Énergie potentielle pour un oscillateur harmonique spatial : $\mathcal{E}_P(x,y,z) = \frac{1}{2}k_xx^{2} + \frac{1}{2}k_yy^{2} + \frac{1}{2}k_zz^{2}$

La force subie par l'oscillateur harmonique spatial est alors, à l'approximation linéaire : $\overrightarrow{F} = -k_xx\overrightarrow{e}_x - k_yy\overrightarrow{e}_y - k_zz\overrightarrow{e}_z$

 L'équation du mouvement du mobile en référentiel galiléen devient, en projection sur les axes $(Ox)$, $(Oy)$ et $(Oz)$ : $\dfrac{d^{2}x}{dt^{2}} + \omega_{0x}^{2}x = 0$ ; $\dfrac{d^{2}y}{dt^{2}} + \omega_{0y}^{2}y = 0$ ; $\dfrac{d^{2}z}{dt^{2}} + \omega_{0z}^{2}z = 0$.

L'énergie mécanique de l'oscillateur spatial : $\mathcal{E}_M = \mathcal{E}_K + \mathcal{E}_P = \left[\frac{1}{2}m\dot{x}^{2} + \frac{1}{2}k_xx^{2}\right] + \left[\frac{1}{2}m\dot{y}^{2} + \frac{1}{2}k_yy^{2}\right] + \left[\frac{1}{2}m\dot{z}^{2} + \frac{1}{2}k_zz^{2}\right]$

La force de rappel d'un oscillateur isotrope : $\overrightarrow{F} = -k\overrightarrow{r}$.
> [!note]
> Nous pouvons remarquer que la force de rappel est colinéaire au vecteur position : c'est une force centrale (voir chapitre [[Force centrale conservative. Mouvement newtonien]]).

L'équation du mouvement d'un oscillateur isotrope : $\dfrac{d^{2}\overrightarrow{r}}{dt^{2}} + \omega_{0}^{2}\overrightarrow{r} = \overrightarrow{0}$.

La solution de cet équation : $\overrightarrow{r} = \overrightarrow{r}_0\cos\omega_0t + \frac{\overrightarrow{v}_0}{\omega_0}\sin\omega_0t$.

Équation du mouvement d'oscillateur amorti par frottement fluide : $m\ddot{x} = -kx - h\dot{x}$
> [!note]
> Cet équation peut s'écrire : $\ddot{x} + \frac{1}{\tau}\dot{x} + \omega_{0}^{2}x = 0$ où $\omega_{0} = \sqrt{\frac{k}{m}}$ est la pulsation propre, ou pulsation de l'oscillateur non amorti, et $\tau = \frac{m}{h}$ est le temps de relaxation de l'énergie de l'oscillateur.
> $\frac{1}{\tau}$ peut être remplacer par $2\alpha$ où $\alpha$ est le facteur d'amortissement de l'oscillateur ou bien par $\frac{\omega_0}{\mathcal{Q}}$ avec $\mathcal{Q}$ est une grandeur sans dimension appelée facteur de qualité de l'oscillateur.

> [!warning] Solutions de l'équation d'évolution
> Il faut savoir comment résoudre une équation différentielle d'ordre deux.

> [!note] Régime pseudo-périodique : $\mathcal{Q} > \frac{1}{2}$
> La solution de l'équation du mouvement est de la forme : $x(t) = e^{-\alpha t}(A_1e^{-j\omega t} + A_2e^{j\omega t})$
> Le terme entre parenthèses est un facteur oscillant, de pulsation $\omega = \sqrt{\omega_{0}^{2} - \alpha^{2}}$. Le facteur $e^{-\alpha t}$ cause une décroissance de l'amplitude d'oscillation (donc de l'énergie), caractérisée par le temps d'amortissement $\tau = \frac{1}{\alpha}$.
> L'évolution est caractérisée par des oscillations d'amplitude exponentiellement décroissante ([[#^figure2]]).
> La pseudo-période du mouvement est : $T = \frac{2\pi}{\omega} = \frac{T_0}{\sqrt{1 - \left(\frac{\alpha}{\omega_0}\right)^{2}}} = \frac{T_0}{\sqrt{1 - \left(\frac{1}{2\mathcal{Q}}\right)^{2}}}$. Elle est une fonction croissante de $\alpha$, c'est-à-dire de l'amortissement. Les frottements augmentent la pseudo-période T des oscillations et la rendent supérieure à la période propre $T_0$.

> [!note] Régime critique : $\mathcal{Q} = \frac{1}{2}$
> La solution de l'équation du mouvement est de la forme : $x(t) = (a + bt)e^{-\omega_0t}$. Cette solution correspond à un retour vers l'équilibre $x = 0$ qui est juste non oscillant : son évolution est semblable à celle du régime oscillant précédent, mais avec des oscillations qui s'essoufflent dès la première ! La stabilisation à $x = 0$ est donc plus rapide que dans le cas précédent ([[#^figure3]]).


> [!note] Régime apériodique : $\mathcal{Q} < \frac{1}{2}$
> La solution de l'équation du mouvement est de la forme : $x(t) = e^{-\alpha t}(A_1e^{-\omega t} + A_2e^{\omega t})$ avec $\omega = \sqrt{\alpha^{2} - \omega_{0}^{2}}$.
> L'évolution est à présent purement exponentielle. Comme dans le cas critique, le retour à $x = 0$ se fait sans oscillation, mais dure ici plus longtemps ([[#^figure4]]).


> [!note]
> En multipliant l'équation différentielle de l'oscillateur amorti $m\dot{v} + hv + kx = 0$ par $v = \dot{x}$, on obtient : $\dfrac{d\mathcal{E}_M}{dt} = -hv^{2}$.


Le décrément logarithmique d'un oscillateur en régime pseudo-périodique : $\delta = \ln\left[\frac{x(t)}{x(t + T)}\right] = \alpha T = \frac{2\pi\alpha}{\sqrt{\omega_{0}^{2} - \alpha^{2}}} = \frac{\pi}{\sqrt{\mathcal{Q}^{2} - \left(\frac{1}{2}\right)^{2}}}$.
> [!note]
> La détermination expérimentale du décrément logarithmique $\delta$ permet d'atteindre le facteur de qualité $\mathcal{Q}$ de l'oscillateur amorti.
> Entre deux élongations extrémales successives $x(t_0)$ et $x(t_0 + T)$, pour lesquelles la vitesse est nulle, l'énergie mécanique passe de $\mathcal{E}_M$ à $\mathcal{E}_M + \Delta \mathcal{E}_M$ avec : $\frac{\Delta \mathcal{E}_M}{\mathcal{E}_M} = (e^{-2\delta} - 1)$.
> Pour de faibles amortissements $(\delta\ll1 \hspace{0.5em}\text{ou}\hspace{0.5em} \mathcal{Q}\gg1)$, $\delta \approx \frac{\pi}{\mathcal{Q}}$ puisque $T \approx T_0$.
> L'expression précédente se simplifie en : $\frac{\Delta \mathcal{E}_M}{\mathcal{E}_M} = -2\delta = -\frac{2\pi}{\mathcal{Q}} =-\frac{T_0}{\tau}$ ou encore $\mathcal{Q} = -2\pi\frac{\mathcal{E}_M}{\Delta \mathcal{E}_M}$.
# Définitions
==**Temps de réponse d'un système physique**== :
Partant des conditions initiales $x(t = 0) = x_0$ et $x(t = 0) = 0$, il existe un temps $t_p$ tel que pour $t > t_p$ nous avons $|x_{(t > t_p)}| < px_0$ (avec p positif ; $p < 1$).
Ce temps $t_p$ correspond souvent à un temps de mesure ou de réponse pour un système physique ; nous cherchons alors à le minimiser.
Ce temps $t_p$, fonction du facteur d'amortissement $2\alpha$ pour un $\omega_0$ donné, admet un minimum pour une valeur particulière $2\alpha_p$ de ce facteur. Il est possible d'obtenir, par des méthodes numériques ou expérimentales, cette valeur de $\alpha_p$ en fonction de p.
> [!note]
> Souvent une « précision » de 5 % est suffisante ; ainsi si nous voulons que $t_{0,05}$ soit minimal $(p = 0,05)$, il faut que $\alpha = 0,\!7\omega_0$ (régime pseudo-périodique) [[#^note]]. Mais si nous désirons une précision supérieure $(p \approx 0)$, il faut tendre vers le régime critique $(\alpha = \omega_0)$.
# Diagrammes

# Graphiques
Trajectoires de  phase de l'oscillateur réel :
![[figure25.png]]^figure1

Mouvement de l'oscillateur harmonique spatial :
![[figure26.png]]
<ol style="list-style-type: lower-alpha">
<li>Anisotrope, à trajectoire ouverte.</li>
<li>Anisotrope, à trajectoire fermée. Les trois pulsations sont dans des rapports rationnels.</li>
<li>Isotrope, à trajectoire plane, elliptique. Les trois pulsations sont égales à &#969;<sub>0</sub></li>
</ol>

L'évolution en régime pseudo-périodique :
![[figure27.png]]^figure2
Le mobile est lâché en $x = x_0$ avec une vitesse $v_0$ positive, nulle ou négative pour les trois cas apparaissant sur la figure.
> [!note]
> Le signal oscille entre les deux enveloppes exponentielles $±Ce^{-\alpha t}$. Notons que les dates des extrema de x ne coïncident pas vraiment avec les dates de contact avec l'enveloppe.


Portrait de phase d'un oscillateur en régime pseudo-périodique $(\mathcal{Q} = 3)$ :
![[figure28.png]]
Le mobile est lâché sans vitesse initiale, pour diverses valeurs de $x_0$.
> [!note]
> Contrairement au cas de l'oscillateur sans frottement, les trajectoires obtenues ne sont pas symétriques par rapport à l'axe $(Ox)$. Cette dissymétrie correspond à un changement de signe du coefficient de la vitesse lors d'un renversement du temps. Du fait de la présence de ce terme de frottement fluide, l'équation du mouvement n'est plus invariante vis-à-vis du changement de variable t → – t : le processus n'est pas réversible.


L'évolution en régime critique :
![[figure29.png]]^figure3
Les conditions initiales sont les mêmes que celles du mouvement pseudo-périodique ([[#^figure2]]).

Portrait de phase d'un oscillateur en régime critique $(\mathcal{Q} = \frac{1}{2})$ :
![[figure30.png]]
Le système tente encore de contourner l'origine (point attracteur) dans le sens horaire, mais ne peut y parvenir : il échoue rapidement au point $O$.

L'évolution en régime apériodique :
![[figure31.png]]^figure4
Suivant les conditions initiales, l'élongation passe par un extremum ou tend uniformément vers zéro.

Portrait de phase d'un oscillateur en régime apériodique $(\mathcal{Q} = 0,\!2)$ :
![[figure32.png]]
Les trajectoires de phase montrent un retour sans oscillation vers le point attracteur à l'origine.
# Expériences
## Etude du pendule pesant ou pendule simple
> [!warning]
> Ce TP n'est pas dans le livre mais se trouve [en ligne](https://prepanouar.wordpress.com/wp-content/uploads/2020/03/pendule-simple.pdf).

![[figure33.png]]
On mesurera la durée de 10 oscillations et on enclenchera le chronomètre lorsque le pendule passera par sa position d'équilibre.

### Influence de l'amplitude
- Déterminer la période T pour des différentes amplitudes initiales en remplissant le tableau suivant : 
![[figure34.png]]
- Conclure et donner le nom du phénomène ainsi observé.
- pour $\theta_0 \geq 40^\circ$ vérifier la formule de Borda $T =T_0 \left(1 + \frac{\theta_{0}^{2}}{16}\right)$ qui est obtenue en utilisant un développement limité de la fonction sinus dans l'équation de mouvement.

### Influence de la masse
- Déterminer la période T pour des différentes masses en remplissant le tableau suivant :
![[figure35.png]]
- Conclure.

### Influence de la longueur du fil L
- Déterminer la période T pour des différentes longueurs en remplissant le tableau suivant :
![[figure36.png]]
- Tracer le graphe représentant T en fonction de L puis faire modéliser.
- Conclure

### Expression de T
- L'expression de la période propre d'un pendule simple non-amorti est : $T_0 = 2\pi\sqrt{\frac{L}{g}}$. Vérifier, à l'aide des résultats expérimentaux, cette expression.
# Autres notes
==**Oscillateur harmonique**== : 
On appelle oscillateur harmonique tout système dont l'évolution (de la position, de la vitesse ou de l'accélération) est fonction sinusoïdale du temps (sinus ou cosinus). on peut citer les exemples suivants à titre non exhaustif de l'oscillateur harmonique : le pendule simple, oscillateur masse-ressort, circuit LC, atomes dans un solide,...

==**Mouvement du pendule simple pour les très petits angles**== : (Application 2 page 79)
![[figure37.png]]
On a $m\overrightarrow{a} = m\overrightarrow{g} + \overrightarrow{T}$ signifie $T\overrightarrow{e}_r = \frac{mv^{2}}{L_0}\overrightarrow{e}_r + mg\cos\theta\overrightarrow{e}_r$ 
Si $\theta$ est petit, on n'a plus de mouvement significatif sur $Oz$, donc $z = L_0$, $z' = 0$, $z'' = 0$ et $\cos\theta = 1 - \frac{\theta^{2}}{2} = 1$
De plus d'après la conservation de l'énergie mécanique, $\frac{v^{2}}{L_0} = 2g(\cos\theta - \cos\theta_m) = g(\theta_{m}^{2} - \theta^{2}) \ll g$ donc $T \simeq mg$
La force $\overrightarrow{T}$ s'exprime comme suit dans les coordonnées de la base mobile : $-T\frac{\overrightarrow{r}}{\lVert \overrightarrow{r} \rVert} = -T\frac{x}{L_0}\overrightarrow{e_x} - T\frac{y}{L_0}\overrightarrow{e_y} - T\frac{z}{L_0}\overrightarrow{e_z}$ 
Alors $x'' = -\frac{T}{m} \frac{x}{L_0} \simeq -g\frac{x}{L_0} = -\omega_{0}^{2}x$, $x'' = -\frac{T}{m} \frac{y}{L_0} \simeq -g\frac{y}{L_0} = -\omega_{0}^{2}y$  et $z'' \simeq 0$ en posant $\omega_{0}^{2} = g/L_0$.

> [!warning] Pourquoi pour que le temps de réponse soit minimal, il faut que $\alpha = 0,\!7\omega_0$^note
> Avant tout on appelle un temps de réponse (généralement pour un oscillateur forcé), le temps pour lequel la position x de l'oscillateur atteint son amplitude maximale à l'intérieur d'un intervalle d'erreur donné (la largeur de la bande d'erreur peut-être 5% ou 2%) et reste à l'intérieur de cet intervalle.
> J'ai rien trouvé sur la minimisation du temps de réponse pour l'oscillateur harmonique amorti libre, tout ce qui existe ce sont des formules pour l'oscillateur forcé et en plus pas de minimisation juste un simple calcul de temps de réponse.
> Par exemple pour un oscillateur forcé en échelon voir ce [lien](https://tttapa.github.io/Pages/Arduino/Audio-and-Signal-Processing/VU-Meters/Damped-Harmonic-Oscillator.html).

