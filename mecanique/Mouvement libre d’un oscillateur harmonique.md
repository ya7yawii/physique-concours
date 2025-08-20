---
titre: "[[Mouvement libre d’un oscillateur harmonique]]"
tags:
aliases:
crée: 20-08-2025, 10:43
---
# Formules
> [!note] Oscillateur harmonique
> L'oscillateur harmonique à un degré de liberté évolue dans un puits de potentiel parabolique : $\mathcal{E}_{P}(x) = \mathcal{E}_{P}(0) + \frac{1}{2}kx^{2}$
> Il est soumis à une force de rappel linéaire : $F(x) = -kx$
> Son équation du mouvement est : $\dfrac{d^{2}x}{dt^{2}} + \omega_{0}^{2}x = 0$, avec $\omega_{0} = \sqrt{\frac{k}{m}}$. 
> La solution générale de cet équation est : $x(t) = A_1\cos(\omega_0t) + A_2\sin(\omega_0t)$ où $A_1$ et $A_2$ sont des constantes d’intégration que l’on déterminera à partir des conditions initiales : $x(0) = x_0$ et $\left(\dfrac{dx}{dt}\right)_{t = 0} = v_0$
> Ainsi, $x(t) = x_0\cos(\omega_0t) + \frac{v_0}{\omega_0}\sin(\omega_0t)$
> qui peut encore s'écrire : $x(t) = x_m\cos(\omega_0t + \phi)$ avec $x_m = \sqrt{x_{0}^{2} + \left(\frac{v_0}{\omega_0}\right)^{2}}$ et $\tan\phi = -\frac{v_0}{\omega_0x_0}$
> La période, appelée période propre des oscillations de l’oscillateur est : $T_0 = \frac{2\pi}{\omega_0}$. Cette période est indépendante de l’amplitude des oscillations. Il y a isochronisme des oscillations.
> La trajectoire de phase de l’oscillateur harmonique décrit une ellipse d’équation : $\left(\frac{x}{x_m}\right)^{2} + \left(\frac{v}{\omega_0x_m}\right)^{2} = 1$. Celle-ci peut même se ramener à un cercle de rayon $x_m$ si nous portons la variable $\frac{v}{\omega_0}$ sur l'axe des ordonnées ([[#^figure1]]).
> Le caractère circulaire de la trajectoire de phase tracée dans les axes $\left(O\hspace{0.4em};\hspace{0.4em} x,\hspace{0.4em}\frac{v}{\omega_0}\right)$ permet un test visuel simple du caractère harmonique d'un oscillateur.
> La trajectoire de phase limite séparant les états liés (oscillations plus ou moins harmoniques) et les états de diffusion est appelée <mark style="color: red">séparatrice</mark>.
> L'énergie mécanique de l'oscillateur est constante : $\mathcal{E}_M = \mathcal{E}_K + \mathcal{E}_P = \frac{1}{2}kx_{m}^{2}$ 

>[!note] Équipartition de l’énergie potentielle et de l’énergie cinétique
> Durant le mouvement, il y a échange permanent des formes cinétique et potentielle de l’énergie. Donc, il y a équipartition, en moyenne, de l’énergie potentielle et de l’énergie cinétique : $\langle\mathcal{E}_P\rangle = \langle\mathcal{E}_K\rangle = \frac{\mathcal{E}_M}{2}$.

Énergie potentielle pour un oscillateur harmonique spatial : $\mathcal{E}_P(x,y,z) = \frac{1}{2}k_xx^{2} + \frac{1}{2}k_yy^{2} + \frac{1}{2}k_zz^{2}$

La force subie par l'oscillateur harmonique spatial est alors, à l’approximation linéaire : $\overrightarrow{F} = -k_xx\overrightarrow{e}_x - k_yy\overrightarrow{e}_y - k_zz\overrightarrow{e}_z$

 L’équation du mouvement du mobile en référentiel galiléen devient, en projection sur les axes $(Ox)$, $(Oy)$ et $(Oz)$ : $\dfrac{d^{2}x}{dt^{2}} + \omega_{0x}^{2}x = 0$ ; $\dfrac{d^{2}y}{dt^{2}} + \omega_{0y}^{2}y = 0$ ; $\dfrac{d^{2}z}{dt^{2}} + \omega_{0z}^{2}z = 0$.

L’énergie mécanique de l’oscillateur spatial : $\mathcal{E}_M = \mathcal{E}_K + \mathcal{E}_P = \left[\frac{1}{2}m\dot{x}^{2} + \frac{1}{2}k_xx^{2}\right] + \left[\frac{1}{2}m\dot{y}^{2} + \frac{1}{2}k_yy^{2}\right] + \left[\frac{1}{2}m\dot{z}^{2} + \frac{1}{2}k_zz^{2}\right]$


# Définitions

# Diagrammes

# Graphiques
Trajectoires de  phase de l’oscillateur réel :
![[figure15.png]]^figure1

Mouvement de l’oscillateur harmonique spatial :
![[figure16.png]]^figure2

<ol style="list-style-type: lower-alpha">
<li>Anisotrope, à trajectoire ouverte.</li>
<li>Anisotrope, à trajectoire fermée. Les trois pulsations sont dans des rapports rationnels.</li>
<li>Isotrope, à trajectoire plane, elliptique. Les trois pulsations sont égales à &#969;<sub>0</sub></li>.
</ol>

# Expériences

# Autres notes
