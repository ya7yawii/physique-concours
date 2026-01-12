---
titre: "[[10-La force de Lorentz]]"
tags:
aliases:
crée: 12-01-2026, 11:13
---
# Formules
> [!note] L'interaction électromagnétique : La force de Lorentz : Formulation
> C’est Lorentz qui, le premier, a décrit la force électromagnétique $\overrightarrow{F}$ agissant sur une particule chargée.
> ==**La force électromagnétique subie par une particule de charge $q$ et de masse $m$, se trouvant, à la date $t$, au point $M$ du référentiel galiléen $\mathcal{R}$, en présence d’un champ électrique $\overrightarrow{E}(M, t)$ et d’un champ magnétique $\overrightarrow{B}(M, t)$, et se déplaçant à la vitesse $\overrightarrow{v}(M, t)_{\!/\mathcal{R}}$  est donnée par : $\overrightarrow{F}_{Lo} = q[\overrightarrow{E}(M, t) + \overrightarrow{v}(M, t)_{\!/\mathcal{R}}\wedge\overrightarrow{B}(M, t)]$.**==
> ==**Dans le cas de champs permanents et indépendants du temps nous avons : $\overrightarrow{F}_{Lo} = q(\overrightarrow{E} + \overrightarrow{v}\wedge\overrightarrow{B})$.**==
> Cette force de Lorentz traduit l’une des interactions fondamentales de la physique ; son domaine de validité n’est pas limité dans le cadre de nos connaissances actuelles.
> Les champs $\overrightarrow{E}$ et $\overrightarrow{B}$ introduits ici sont créés par des sources (charges et courants) et définis relativement au référentiel $\mathcal{R}$.
> Comme toute force d’interaction, $\overrightarrow{F}_{Lo}$ ne dépend pas du référentiel alors que la vitesse en dépend. Les champs $\overrightarrow{E}$ et $\overrightarrow{B}$ peuvent donc dépendre du référentiel.
> Remarquons que les champs $\overrightarrow{E}$ et $\overrightarrow{B}$ sont de natures différentes ; le rapport $\frac{E}{B}$ est homogène à une vitesse. Dans le Système International d’unités, $E$ s’exprime en volts par mètre $(V . m^{-1})$ et $B$ en testa $(T)$.
> La charge $q$ est une propriété intrinsèque de la particule : elle est indépendante du temps et du référentiel.

> [!note] L'interaction électromagnétique : La force de Lorentz
> - Comparaison avec la force gravitationnelle :
> La comparaison des forces électrostatique et gravitationnelle a été mentionnée dans le chapitre 2, [[#^app1|Application 1]] : le rapport colossal obtenu justifie que nous négligions par la suite les forces de gravitation (et donc de pesanteur).
> - Puissance :
> La puissance de la force de Lorentz est : $\mathcal{P}_{Lo} = \overrightarrow{F}_{Lo}\,.\overrightarrow{v} = q\,\overrightarrow{E}\,.\overrightarrow{v}$.
> Elle est nulle si le champ électrique est nul.
> - Hypothèses d’étude :
> Considérons le mouvement de particules dans des champs $\overrightarrow{E}$ et (ou) $\overrightarrow{B}$ indépendants du temps (ou très exceptionnellement à variation temporelle suffisamment lente pour que l'approximation du régime quasi permanent soit applicable (cf. [[07-Champ magnétique|chapitre 7]]).
> Nous utiliserons une propriété des champs électriques indépendants du temps, à savoir l'existence d'un potentiel scalaire $V(M)$ tel que : $\overrightarrow{E} = -\overrightarrow{grad}\,V$.
> *Remarque :*
> *La plupart des expériences et des exercices étudiés ci-dessous supposent la réalisation d’un vide poussé (pression inférieure à un pascal), ce qui élimine tout frottement lors du déplacement des particules.*
> La relation fondamentale de la mécanique appliquée à une particule de masse $m$ et de charge $q$ s’écrit alors : $m\dfrac{d\overrightarrow{v}}{dt} = q(\overrightarrow{E} + \overrightarrow{v}\wedge\overrightarrow{B})$.
> La masse $m$ et la charge $q$ interviennent par leur rapport $\frac{q}{m}$. Il est donc inutile de chercher à déterminer séparément $q$ et $m$ par l’étude du mouvement.

> [!note] Mouvement d'une particule chargée dans les champs $\overrightarrow{E}$ et (ou) $\overrightarrow{B}$ : Champ $\overrightarrow{E}$ seul
> - Rôle accélérateur d’un champ électrique :
> Lorsqu’une charge $q$ se déplace dans un champ électrostatique $\overrightarrow{E} = -\overrightarrow{grad}\,V$, elle subit la force : $\overrightarrow{F} = q\overrightarrow{E} = -\overrightarrow{grad}(qV)$, qui dérive de l’énergie potentielle $\mathcal{E}_P = qV$.
> L’énergie mécanique $\mathcal{E}_M = \frac{1}{2}mv^{2} + qV$ se conserve et en deux positions $M_1$ et $M_2$ de la particule, il vient : $v^{2}(M_2) = v^{2}(M_1) + 2\frac{q}{m}(V_1 - V_2)$.
> En supposant que la particule parte d’un point $O$ de potentiel nul (potentiel de référence) avec une vitesse nulle, son énergie cinétique en un point $M$ est : $\mathcal{E}_K(M) = -qV(M)$.
> Cette particule possède une énergie cinétique exprimable naturellement en électron-volt (*symbole* : $eV$).
> Remarquons que pour un *électron* $(q = -e)$ , il faut que $V(M) > 0$ pour qu’il puisse acquérir une vitesse.
> - Mouvement dans un champ électrique $\overrightarrow{E}$ uniforme et indépendant du temps :
> Une particule passant à l’intérieur d’un condensateur plan subit une déviation proportionnelle à la différence de potentiel entre les plaques du condensateur (cf. l’[[#^app2|Application 3]]) ; ce principe est utilisé dans un oscilloscope analogique.
> Limitons-nous à rappeler succinctement la description du tube cathodique d’un oscilloscope ([[#^figure1|fig. 1]]).
> Dans le tube règne un vide poussé $(p < 10^{-4} Pa)$. Le pinceau électronique est produit par un canon à électron comportant un fil chauffé ($1000\,K$ environ) à fort pouvoir émissif en électrons, une électrode appelée wehnelt permettant de régler l’intensité du courant électronique, et des électrodes de concentration et d’accélération (lentilles électroniques).
> Les électrons traversent ensuite les plaques de déviations verticales et horizontales. Quand les électrons traversent les plaques horizontales soumises à une différence de potentiel $U_V$, ils sont déviés verticalement ; cette déviation était proportionnelle à $U_V$ (cf. l’[[#^app2|Application 3]]).
> Il en est de même pour la traversée des plaques verticales, la déviation horizontale associée étant proportionnelle à la tension $U_H$ appliquée entre ces plaques.
> Sur l’écran la trace de l’électron (spot) traduit ces déviations : $X = K_1U_H$ et $Y = K_2U_V$.
> Nous nous reporterons aux travaux pratiques pour l’utilisation de cette propriété.

> [!note] Mouvement d'une particule chargée dans les champs $\overrightarrow{E}$ et (ou) $\overrightarrow{B}$ : Champ $\overrightarrow{B}$ seul : Propriétés du mouvement dans un champ $\overrightarrow{B}$ stationnaire
> Un électron mobile dans un champ magnétique $\overrightarrow{B}$ indépendant du temps (stationnaire) est uniquement soumis à la force magnétique $\overrightarrow{F} = q\overrightarrow{v}\wedge\overrightarrow{B}$ (souvent appelée également force de Lorentz).
> La puissance de cette force est nulle, car : $\overrightarrow{F}\, . \overrightarrow{v} = (q\overrightarrow{v}\wedge\overrightarrow{B}) . \overrightarrow{v} = 0$, (produit mixte avec deux vecteurs colinéaires).
> Le travail de la force magnétique $\overrightarrow{F} = q\overrightarrow{v}\wedge\overrightarrow{B}$ qui s’exerce sur une particule est nul.
> L’énergie cinétique de cette particule est constante (théorème de la puissance cinétique). La norme de sa vitesse au cours du mouvement est constante : $\dfrac{d\mathcal{E}_K}{dt} = \overrightarrow{F}\, . \overrightarrow{v} = 0$, donc $\mathcal{E}_K = cte$ et $v = cte$.
> *Remarques :*
> - *Si $\overrightarrow{B}$ dépend du temps selon $\overrightarrow{B} = \overrightarrow{B}(M, t)$, la force magnétique ne travaille toujours pas, mais il apparaît (phénomène d’induction) un champ électrique dont la puissance est en général non nulle. Une telle situation est exclue de nos hypothèses d’étude.*
> - *La puissance de la force magnétique est nulle mais ses effets ne le sont pas ; la force magnétique dévie les particules chargées en mouvement et cela d'autant fortement que leur vitesse est élevée.*

> [!note] Mouvement d'une particule chargée dans les champs $\overrightarrow{E}$ et (ou) $\overrightarrow{B}$ : Champ $\overrightarrow{B}$ seul : Mouvement dans un champ $\overrightarrow{B}$ uniforme et indépendant du temps
> - Cas général d’une vitesse initiale quelconque :
> Étudions le mouvement d’une particule $(q, m)$ placée à l’origine $O$ du trièdre trirectangulaire $(O ; x, y, z)$ à l’instant initial $t = 0$ (vitesse initiale $\overrightarrow{v}_0$) dans un champ magnétostatique $\overrightarrow{B} = B\,\overrightarrow{e}_z$ $(B > 0)$ uniforme dans un domaine donné ([[#^figure2|fig. 2]]).
> Posons $\overrightarrow{v}_0 = v_0(\sin\alpha\, . \overrightarrow{e}_x + \cos\alpha\, . \overrightarrow{e}_z)$.
> La relation fondamentale de la dynamique appliquée au point matériel donne : $m\dfrac{d\overrightarrow{v}}{dt} = q\,\overrightarrow{v}\wedge B\,\overrightarrow{e}_z$.
> Posons $q = \epsilon e$ ($\epsilon = +1$ pour un proton, et $\epsilon = -1$ pour un électron).
> Introduisons la grandeur $\omega_c = \frac{eB}{m}$ homogène à l’inverse d’un temps et que nous appellerons **pulsation cyclotron**.
> Nous obtenons : $\dfrac{dv_x}{dt} = \epsilon\omega_cv_y$, $\dfrac{dv_y}{dt} = -\epsilon\omega_cv_x$ et $\dfrac{dv_z}{dt} = 0$.
> 	- Mouvement projeté sur le plan $(xOy)$ :
> 	En intégrant les deux premières équations par rapport au temps, nous obtenons : $v_x = \epsilon\omega_cy + v_0\sin\alpha$ et $v_y = -\epsilon\omega_cx$. Il est possible de reporter $v_x$ et $v_y$ dans les équations précédentes et d’intégrer à nouveau, mais il est aussi efficace d’introduire la variable $\xi = x + i y$ qui représente *l’affixe* de la projection orthogonale du vecteur $\overrightarrow{OM}$ (vecteur position de la particule) dans le plan $(xOy)$.
> 	Comme $\dfrac{d\xi}{dt} = v_x + i v_y$, nous avons $\dfrac{d\xi}{dt} = -\epsilon i \omega_c\xi + v_0\sin\alpha$, dont la solution est : $\xi = -i\frac{\epsilon v_0}{\omega_c}\sin\alpha + A\exp(-i\epsilon\omega_ct)$.
> 	À $t = 0$, $\xi = 0$, donc $A = i\frac{\epsilon v_0}{\omega_c}\sin\alpha$ et $\xi = i\frac{\epsilon v_0}{\omega_c}\sin\alpha[\exp(-i\epsilon\omega_ct) - 1]$.
> 	Les lois horaires sont donc : $x(t) = -\frac{\epsilon v_0}{\omega_c}\sin\alpha\sin(-\epsilon\omega_ct)$ et $y(t) = -\frac{\epsilon v_0}{\omega_c}\sin\alpha[1 - \cos(-\epsilon\omega_ct)]$.
> 	$x$ et $y$ vérifient $x^{2} + \left(\frac{\epsilon v_0}{\omega_c}\sin\alpha + y\right)^{2} = \left(\frac{v_0}{\omega_c}\sin\alpha\right)^{2}$ : le mouvement projeté dans le plan $(xOy)$ est un cercle de centre $C$ ($x_C = 0$ et $y_C = -\frac{\epsilon v_0}{\omega_c}\sin\alpha$) et de rayon $\rho = \frac{v_0}{\omega_c}\sin\alpha$ ([[#^figure3|fig. 3a]]). Ce cercle est décrit avec la vitesse angulaire $-\epsilon\omega_c$ égale en valeur absolue à la pulsation cyclotron.
> 	- Mouvement suivant $(Oz)$ :
> 	La troisième équation fournit : $v_z = cte = v_0\cos\alpha$, soit $z = v_0\cos\alpha t$ (mouvement uniforme parallèlement à $(Oz)$). La particule décrit donc une hélice circulaire ([[#^figure4|fig. 4]]).
> 	*Remarque : Le pas de l'hélice ([[#^figure3|fig. 3b et c]]) est $h = v_0\cos\alpha T$, où $T = \frac{2\pi}{\omega_c} = 2\pi\frac{m}{eB}$, donc : $h = 2\pi\frac{mv_0}{eB}\cos\alpha$.*
> - Le cas particulier d’une vitesse initiale normale au champ magnétique :
> Si la vitesse initiale $\overrightarrow{v}_0$ de la particule est normale au champ magnétique $\overrightarrow{B}$, $\left(\alpha = \frac{\pi}{2}\right)$, cette particule décrit une trajectoire circulaire dans un plan orthogonal à $\overrightarrow{B}$, et contenant $\overrightarrow{v}_0$. 
# Définitions

# Diagrammes
Oscilloscope : ➀ : Fil chauffé. ➁ : Wehnelt. ➂ : Électrode de concentration ou de focalisation. ➃ : Électrode d’accélération. ➄ : Plaques de déviation verticale. ➅ : Plaques de déviation horizontale
![[electromagnetisme1/attachments-electromagnetisme1/figure166.png]]^figure1
# Graphiques
Mouvement d’une particule dans un champ magnétique
![[electromagnetisme1/attachments-electromagnetisme1/figure167.png]]^figure2

Projection de la trajectoire sur les plans de coordonnées dans le cas d’un proton
![[electromagnetisme1/attachments-electromagnetisme1/figure168.png]]^figure3

Trajectoire d’un électron et d’un proton dans un champ $\overrightarrow{B}$ uniforme
![[electromagnetisme1/attachments-electromagnetisme1/figure169.png]]^figure4
# Expériences

# Autres notes
> [!warning] Application 1 page 18
> ![[electromagnetisme1/attachments-electromagnetisme1/figure164.png]]
^app1

> [!warning] Application 3 page 179
> ![[electromagnetisme1/attachments-electromagnetisme1/figure165.png]]
^app2