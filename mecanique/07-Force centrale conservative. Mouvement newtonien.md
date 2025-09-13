---
titre: "[[07-Force centrale conservative. Mouvement newtonien]]"
tags:
  - centrale
  - newtonien
  - gravitation
  - kepler
crée: 07-09-2025, 17:04
---
# Formules
Champ de forces centrales : $\overrightarrow{F} = F\overrightarrow{e_r}$  ; le support de la force $\overrightarrow{F}$ passe par le point fixe O.
> [!note] Champ de force centrale conservative
> Un champ de force centrale conservative est de la forme $\overrightarrow{F} = F(r)\overrightarrow{e_r}$ avec $F(r) = -\dfrac{\mathcal{E}_P(r)}{dr}$, $\mathcal{E}_P(r)$ désignant l'énergie potentielle (définie à une constante près) associée à ce champ de force.
> Il existe des champs de forces centrales non conservatifs ; c'est le cas de certaines forces de contact.
> La force est attractive lorsqu'elle est dirigée vers O, soit :$F(r) < 0$. L'énergie potentielle est alors une fonction croissante de la distance r au centre de force O.
> Elle est au contraire répulsive si $F(r) > 0$, donc lorsque l'énergie potentielle est une  fonction décroissante de la distance.

Loi de gravitation : $\displaystyle \overrightarrow{F}_{M_1 \rightarrow M_2} = -G\frac{m_1m_2}{r^{2}}\overrightarrow{e_{12}}$ avec $\overrightarrow{F}_{M_1\rightarrow M_2}$ force de gravitation qui est attractive, $G = 6,\!672\hspace{0.3em} . 10^{-11} N . m^{2} . kg^{-2}$ est une constante universelle et $\overrightarrow{e_{12}}$  est le vecteur unitaire de l'axe $M_1M_2$ orienté de $M_1$ vers $M_2$.
> [!note]
> Cette loi, dite de gravitation universelle, a été formulée par Newton pour expliquer les orbites planétaires.
> La <mark style="color: red">masse pesante</mark> qui intervient dans l'expression de la force de gravitation est identique à la <mark style="color: red">masse inerte</mark> de la relation fondamentale de la dynamique. Il s'agit là d'un postulat supplémentaire, dont la validité est confirmée par toutes les expériences.

Le champ de gravitation engendré par un astre de masse $M_{astre}$, de centre d'inertie O, en un point M situé à l'extérieur de l'astre est : $\displaystyle \overrightarrow{\mathcal{G}}(M) = -GM_{astre}\frac{\overrightarrow{OM}}{OM^{3}} = -GM_{astre}\frac{\overrightarrow{e_r}}{r^{2}}$.
> [!note]
> Cette expression est exacte dans le cas d'un astre à symétrie sphérique, et constitue une bonne approximation du champ de gravitation si l'astre est quasi sphérique ou bien à distance r suffisamment grande par rapport à la dimension caractéristique R d'un astre peu régulier.

Champ de force centrale newtonien : $\displaystyle\overrightarrow{F} = -\alpha\frac{\overrightarrow{e_r}}{r^{2}}$.
Énergie potentielle associée au champ newtonien : $\mathcal{E}_P(r) = -\frac{\alpha}{r} + cte$.
> [!note]
> Le champ de force newtonien est attractif lorsque la constante d'interaction $\alpha$ est positive, répulsif au contraire.

> [!note] Mouvement à force centrale conservative
> Nous savons que lors d'un mouvement où il est soumis à un champ de force centrale, de centre O fixe, dans un référentiel galiléen, la trajectoire d'un point matériel est en général dans un plan (passant par O et perpendiculaire au moment cinétique constant $\overrightarrow{L_O}$).
> Pour repérer le mouvement du point matériel dans ce plan, il nous suffit de deux coordonnées. La force étant constamment radiale, nous ferons le choix des coordonnées polaires $(r, \theta)$ de centre O ([[#^figure1]]).
> En écrivant la relation fondamentale de la dynamique, en projection sur les deux vecteurs de la base locale, nous obtenons donc :
>$$  
\begin{cases}  
\displaystyle \ddot{r} - r\dot{\theta}^{2} = \frac{F(r)}{m} = -\frac{1}{m}\dfrac{d\mathcal{E}_P(r)}{dr} & \text{équation radiale}\\  
\displaystyle 2\dot{r}\dot{\theta} + r\ddot{\theta} = 0 & \text{équation orthoradiale}
\end{cases}  
>$$ 
> En remarquant que : $\displaystyle 2\dot{r}\dot{\theta} + r\ddot{\theta} = \frac{1}{r}\dfrac{d}{dt}(r^{2}\dot{\theta}$). En utilisant la loi des aires, nous pouvons ramener le système précédent aux équations suivantes :
>$$  
\begin{cases}  
\displaystyle \ddot{r} - \frac{C^{2}}{r^{3}} = \frac{F(r)}{m} = -\frac{1}{m}\dfrac{d\mathcal{E}_P(r)}{dr} \\  
\displaystyle \dot{\theta} = \frac{C}{r^{2}} 
\end{cases}  
>$$
>En multipliant les deux membres de l'équation radiale par $\dot{r}$, ce qui nous donne : $\displaystyle \dfrac{d}{dt}\left(\frac{1}{2}\dot{r}^{2} + \frac{1}{2}\frac{C^{2}}{r^{2}}\right) = \dfrac{d}{dt}\left(-\frac{1}{m}\mathcal{E}_P(r)\right)$ qui s'intègre par rapport au temps en : $\displaystyle \frac{1}{2}m\left(\dot{r}^{2} + \frac{C^{2}}{r^{2}}\right) + \mathcal{E}_P(r) = cte$ qui n'est rien d'autre que la traduction de la conservation de l'énergie mécanique $\mathcal{E}_M$ du mobile donc : $\displaystyle \dot{r} = \pm \sqrt{\mathcal{E}_M - \frac{mC^{2}}{2r^{2}} - \mathcal{E}_P(r)}$.
>Cette expression fait apparaître une équation différentielle d'ordre un, qui peut se prêter assez aisément à un calcul numérique (en utilisant la méthode de résolution d'Euler, par exemple). Ensuite, il suffirait de reporter $r(t)$ dans la seconde équation pour obtenir $\theta(t)$ par intégration par rapport au temps.
>Énergie potentielle effective : $\displaystyle \mathcal{E}_{P_{eff}}(r) = \frac{mC^{2}}{2r^{2}} - \mathcal{E}_P(r)$
>Domaine accessible à la trajectoire : $\mathcal{E}_{P_{eff}}(r) \leqslant \mathcal{E}_M$
>Pour le mouvement à force centrale, l'énergie cinétique ne peut s'annuler car la composante orthoradiale $\displaystyle \frac{mC^{2}}{2r^{2}}$ ne s'annule pas puisque la constante des aires n'est, en général, pas nulle.
>Considérons une énergie potentielle d'expression simple, par exemple : $\displaystyle \mathcal{E}_P(r) = -\frac{K}{r^{n}}$, soit $\displaystyle F(r) = -\frac{nK}{r^{n+1}}$. Le champ de forces est attracteur si nK est positif, répulsif le cas échéant.
>Cas d'un champ répulsif (n et K de signes opposées) : On peut trouver le graphe de $\mathcal{E}_{P_{eff}}(r)$ dans la [[#^figure2]]. Dans tous les cas, il est clair que nous avons affaire à un état de diffusion, le point matériel finissant toujours par s'éloigner indéfiniment du centre O ([[#^figure3]]).
>Cas d'un champ attractif (n et K de même signe) :
>- Cas n° 1 : $n < 0$ (et $K < 0$) : On peut trouver le graphe de $\mathcal{E}_{P_{eff}}(r)$ dans la [[#^figure4]]. La simulation du mouvement fait apparaître une trajectoire qui n'est en général pas fermée, pour laquelle la distance au centre de force O oscille entre $r_{min}$ et $r_{max}$ ([[#^figure5]]). Le cas $n = -2$ est particulier, puisqu'il s'agit alors d'un oscillateur harmonique spatial et nous savons que dans ce cas la trajectoire est fermée : c'est une ellipse.
>- Cas n° 2 : $0 < n < 2$ (et $K > 0$) : On peut trouver le graphe de $\mathcal{E}_{P_{eff}}(r)$ dans la [[#^figure6]]. Nous pouvons alors observer un état lié si $\mathcal{E}_M < 0$ ([[#^figure7]]), ou un état de diffusion si $\mathcal{E}_M > 0$ ([[#^figure8]]). Le cas du champ newtonien correspond ici à n = 1. Nous verrons plus loin que pour ce champ très particulier, les trajectoires des états liés sont fermées : ce sont des ellipses.
>- Cas n° 3 : $n > 2$ (et $K > 0$) : On peut trouver le graphe de $\mathcal{E}_{P_{eff}}(r)$ dans la [[#^figure9]]. Pour $\mathcal{E}_M = \mathcal{E}_{M_a}$ (sur la [[#^figure9]]), nous pouvons observer un état de diffusion (cas de l'état a.1.), pour lequel la distance r ne peut descendre en deçà d'un minimum $r_{min}$ ([[#^figure10]]). Pour une même valeur de l'énergie mécanique, nous pouvons aussi rencontrer un cas (état a.2.) où la distance r possède une borne supérieure $r_{max}$ , mais pas de borne inférieure non nulle : concrètement, cela signifie que la force attractive est trop forte à courte distance, et que le point matériel vient s'écraser sur le centre attracteur O ! Pour l'état b. sur la [[#^figure9]], cette collision survient encore si le point matériel se dirige initialement vers le centre de force O ([[#^figure11]]).

Énergie mécanique dans un mouvement dans un champ newtonien : $\displaystyle \mathcal{E}_M= \frac{1}{2}mv^{2} + \mathcal{E}_P(r) = \frac{1}{2}m\dot{r}^{2} + \frac{mC^{2}}{2r^{2}} - \frac{\alpha}{r} = cte$ avec $\alpha = GmM$ quand l'interaction newtonienne correspond à l'attraction gravitationnelle subie par un satellite de masse m évoluant dans le champ de gravitation d'un astre de masse M.

Vitesse d'un satellite en trajectoire circulaire de rayon $r_c$ : $\displaystyle v_c = \sqrt{\frac{\alpha}{mr_c}} = \sqrt{\frac{GM}{r_c}}$ où M est la masse de l'astre.

Énergie associée à une trajectoire circulaire de rayon $r_c$ : $\displaystyle \mathcal{E}_M = -\frac{\alpha}{2r_c}$ 
> [!note] Troisième loi de Kepler
> Dans le système solaire, les planètes de masse $M_{\odot}$ en trajectoire circulaire autour du Soleil ont une période liée à leur rayon de giration par : $\displaystyle \frac{T^{2}}{r_{c}^{3}} = \frac{4\pi^{2}}{GM_{\odot}}$
> Pour une trajectoire elliptique, il faut remplacer le rayon $r_c$ de la trajectoire circulaire par le demi-grand axe a de l'ellipse dans ce résultat.

> [!note]
> Un mouvement newtonien est un mouvement à force centrale, où la force est conservative, et proportionnelle à $\frac{1}{r^{2}}$ : $\displaystyle \overrightarrow{F}_{M \rightarrow m} = -\frac{\alpha}{r^{2}}\overrightarrow{e_r}$ ; le moment cinétique : $\overrightarrow{L_O} = mr^{2}\dot{\theta}\overrightarrow{e_z} = mC\overrightarrow{e_z}$, l'énergie : $\displaystyle \mathcal{E}_M = \frac{1}{2}m\dot{r}^{2} + \frac{mC^{2}}{2r^{2}} - \frac{\alpha}{r}$, et le vecteur de Runge-Lenz : $\displaystyle \overrightarrow{A} = \frac{\overrightarrow{v} \wedge \overrightarrow{L_O}}{\alpha} - \overrightarrow{e_r}$ sont des constantes du mouvement.

> [!note] Les trajectoires sont des coniques
> En exprimant les composantes du vecteur de Runge-Lenz dans la base locale des coordonnées polaires, on obtient : $\displaystyle \overrightarrow{A} = \left(\frac{mC^{2}}{\alpha r} - 1\right)\overrightarrow{e_r} - \frac{mC}{\alpha}\dot{r}\overrightarrow{e_{\theta}}$ en particulier, on a : $\displaystyle \overrightarrow{A} \hspace{0.2em} . \overrightarrow{r} = \frac{mC^{2}}{\alpha} - r$ et $\overrightarrow{A} \hspace{0.2em} . \overrightarrow{r} = \left\Vert\overrightarrow{A}\right\Vert r\cos\theta = er\cos\theta$ et en comparant ces deux expressions, on identifie l'équation polaire de la trajectoire : $\displaystyle r(\theta) = \frac{p}{1 + e\cos\theta}$. Il s'agit de l'équation d'une courbe conique, d'excentricité $e = \left\Vert\overrightarrow{A}\right\Vert$ et de paramètre $\displaystyle p = \frac{mC^{2}}{\alpha}$. On déduit ainsi :
> - une trajectoire elliptique, si l'excentricité est inférieure à 1 (un cercle, si e = 0) ;
> - une trajectoire parabolique, si l'excentricité vaut 1 ;
> - une trajectoire hyperbolique, si l'excentricité est plus grande que 1.
> 
> A partir de calcul de la norme de $\overrightarrow{A}$ au carré, on peut conclure que : $\displaystyle \mathcal{E}_M = \frac{\alpha}{2mC^{2}}(e^{2} - 1)$. On voit qu'on peut encore classer la nature des trajectoires à l'aide du signe de l'énergie :
> - la trajectoire est elliptique si l'énergie est négative (c'est le cas pour les trajectoires circulaires) ;
> - la trajectoire est parabolique si l'énergie est nulle ;
> - la trajectoire est hyperbolique si l'énergie est positive.

> [!note] Représentation du mouvement newtonien
> Domaine accessible aux variations de r : $\displaystyle \mathcal{E}_{P_{eff}}(r) = \frac{mC^{2}}{2r^{2}} - \frac{\alpha}{r} \leqslant \mathcal{E}_M$.
> Force newtonienne répulsive : états de diffusion $(\alpha < 0)$ : On peut trouver le graphe de $\mathcal{E}_{P_{eff}}(r)$ dans la [[#^figure2]]. La trajectoire est hyperbolique : la distance $r_{min}$ est atteinte au sommet S de la branche d'hyperbole décrite par le point matériel. En ce point, la dérivée $\dot{r}$ est nulle et le vecteur de Lenz est colinéaire au rayon vecteur ([[#^figure12]]).
> Force newtonienne attractive : états liés et états de diffusion $(\alpha > 0)$ : On peut trouver le graphe de $\mathcal{E}_{P_{eff}}(r)$ dans la [[#^figure13]] :
> - Si l'énergie est négative ($e < 1$, trajectoire elliptique) : La distance r évolue entre une valeur maximale $r_{max}$ et une valeur minimale $r_{min}$ : nous avons affaire à un état lié. Ces distances correspondent respectivement à l'apogée A et au périgée P de la trajectoire elliptique ([[#^figure14]]).
> - Si l'énergie est nulle ($e = 1$, trajectoire parabolique) : L'apogée de la trajectoire est renvoyé à l'infini ([[#^figure15]]).
> - Si l'énergie est positive ($e > 1$, trajectoire hyperbolique) : Comme dans le cas répulsif, nous obtenons un état de diffusion. Attention cependant, car la branche d'hyperbole décrite par le point matériel diffère dans les deux cas : pour une force répulsive, nous avons observé une trajectoire où le point matériel fuyait le centre de force ([[#^figure12]]). Ici, il est attiré vers O, mais finit quand même par s'échapper ([[#^figure16]]).
# Définitions
==**Mouvement keplerien**== :
Un mouvement est dit keplerien lorsqu'il s'effectue sous l'action d'une force centrale en $\displaystyle \frac{1}{r^{2}}$, de centre de force fixe dans le référentiel galiléen d'étude, c'est-à-dire dans un champ de forces newtonien.

==**Trois lois de Kepler**== :
- Première loi (1605) : chaque planète décrit, dans le sens direct, une trajectoire elliptique dont le Soleil est un foyer.
- Deuxième loi (1604) : l'aire balayée par le rayon Soleil-planète est proportionnelle au temps mis pour la décrire.
- Troisième loi (1618) : le carré du temps de révolution sidérale d'une planète est proportionnel au cube du grand axe de l'ellipse qu'elle décrit.

==**Satellites**== :
Les satellites correspondent à des mobiles en état lié évoluant dans le champ de gravitation, attractif, de l'astre autour duquel ils gravitent : leur énergie mécanique est négative.

==**Première vitesse cosmique**== :
Dans le cas d'un satellite terrestre, $M = M_T$ masse de la Terre, et la vitesse minimale correspond au cas $r = R_T$. Cette vitesse est la vitesse en orbite circulaire basse, encore appelée première vitesse cosmique : $v_1 \approx 7,\!92 \hspace{0.3em} km \hspace{0.3em}.\hspace{0.1em} s^{-1}$.

==**Deuxième vitesse cosmique**== :
Le satellite pourrait totalement échapper à l'attraction terrestre si son énergie mécanique devenait juste nulle : la distance r peut devenir infinie.
La vitesse nécessaire $v_2$, deuxième vitesse cosmique, est donnée par : $\displaystyle \mathcal{E}_M = -\frac{1}{2}mv_{2}^{2} - \frac{GmM}{R_T} = 0$ soit $v_2 \approx 11,\!2 \hspace{0.3em} km \hspace{0.3em}.\hspace{0.1em} s^{-1}$.  
# Diagrammes

# Graphiques
Coordonnées polaires dans le plan de la trajectoire :
![[figure52.png]]^figure1

Énergie potentielle effective dans un cas répulsif $(n = 1, k < 0)$ :
![[figure53.png]]^figure2

État de diffusion, avec passage par la distance d'approche minimale $r_{min}$ :
![[figure54.png]]^figure3

Énergie potentielle effective pour $n < 0$ (ici n = –1,2) et $k < 0$ :
![[figure55.png]]^figure4

Mouvement pour $n < 0$ (ici n = –1,5), oscillations de la distance au centre de force :
![[figure56.png]]^figure5

Énergie potentielle effective pour $0 < n < 2$ ici (n = 1,2) :
![[figure57.png]]^figure6

État lié (n = 1,2) :
![[figure58.png]]^figure7

État de diffusion (n = 1,2) :
![[figure59.png]]^figure8

Énergie potentielle effective pour $n > 2$ ici $(n = 3)$ :
![[figure60.png]]^figure9

Le point matériel s'échappe ! :
![[figure61.png]]^figure10

Il va s'écraser sur le centre attracteur :
![[figure62.png]]^figure11

Branche d'hyperbole du mouvement répulsif :
![[figure63.png]]^figure12

Énergie potentielle effective du cas attractif :
![[figure64.png]]^figure13

Mouvement elliptique :
![[figure65.png]]^figure14

Mouvement parabolique :
![[figure66.png]]^figure15

Branche d'hyperbole du mouvement attractif :
![[figure67.png]]^figure16
# Expériences
## Mobiles autoporteurs sur coussin d'air
> [!warning]
> Ce TP n'est pas dans le livre mais se trouve [en ligne](https://perso.ens-lyon.fr/nicolas.barros/agreg/MP/Polys/Divers.pdf) et le schéma de l'expérience se trouve dans ce [lien](https://books.google.tn/books?redir_esc=y&hl=fr&id=iKEnXengxq4C&q=Mobiles+autoporteurs+sur+coussin+d%E2%80%99air#v=onepage&q=Mobiles%20autoporteurs%20sur%20coussin%20d%E2%80%99air&f=true). Pour faire ce TP, on est besoin de logiciel Latis-Pro donc ce n'est pas l'exemple des travaux pratique qui est possible de faire dans les universités tunisiennes.
# Autres notes
> [!note] Énergie mécanique pour un mouvement elliptique dans un champ newtonien
> Il faut retenir que $\displaystyle \mathcal{E}_M = \frac{-\alpha}{2a}$ pour un mouvement elliptique dans un champ newtonien. Pour plus des détails, consulter l'exercice commenté page 164.

> [!note] Direction de vecteur de Runge Lenz $\overrightarrow{A}$
> Dans tous les cas des courbes coniques, $\overrightarrow{A}$ est colinéaire à l'axe de symétrie de la conique et est dirigé du centre de force vers le periapside, point de plus courte approche (d'après [wiki](https://fr.wikipedia.org/wiki/Vecteur_de_Runge-Lenz)) ou pointant dans la concavité de la branche d’hyperbole pour un trajectoire hyperbolique (d'après corrigé exercice n° 8 page 171).