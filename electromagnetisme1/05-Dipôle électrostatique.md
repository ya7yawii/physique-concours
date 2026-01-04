---
titre: "[[05-Dipôle électrostatique]]"
tags:
aliases:
crée: 03-01-2026, 10:51
---
# Formules
> [!note] Moment dipolaire
> -  Moment dipolaire d'une distribution de charges globalement neutre :
> Considérons dans la distribution $\mathcal{D}$ l'ensemble des charges positives dont la somme est notée $+q$ et l'ensemble des charges négatives dont la somme vaut $-q$, $q$ étant supposée non nulle.
> Nous pouvons définir $A^{+}$, le barycentre des charges positives de $\mathcal{D}$, et $A^{-}$ le barycentre des charges négatives de $\mathcal{D}$.
> Le moment dipolaire de la distribution est par définition : $\overrightarrow{p} = q\overrightarrow{A^{-}A^{+}}$.
> Il s'évalue en coulomb . mètre $(C . m)$.
> - Doublet de charges :
> Le modèle le plus simple de dipôle est un doublet de charges opposées et séparées par une distance que nous noterons $d$ ([[#^figure1|fig. 1]]).
> ==**Un objet non chargé mais polarisé crée à grande distance un potentiel et un champ analogues (en première approximation) à ceux d'un doublet de charges de moment dipolaire $\overrightarrow{p}$ non nul $(q > 0)$ : $\overrightarrow{p} = q\overrightarrow{d}$ et $\overrightarrow{d} = \overrightarrow{A^{-}A^{+}}$.**==

> [!note] Potentiel et champ créés par un dipôle
> Nous nous limiterons au calcul et à la représentation de ces grandeurs pour le modèle du doublet.
> - Approximation dipolaire :
> Si nous nous intéressons aux effets produits par le dipôle, l'approximation dipolaire consiste à supposer *la distance à laquelle nous observons le champ créé par le dipôle très grande devant ses dimensions : $r \gg d$.*
> Dans ces conditions, nous mènerons les calculs en ne déterminant que les termes d'ordre le plus bas en $\left(\frac{d}{r}\right)$.

> [!note] Potentiel et champ créés par un dipôle : Potentiel du dipôle
> La distribution considérée (doublet) étant d'extension finie, nous pouvons *choisir le potentiel nul à l'infini*, et l'écrire, avec les notations de [[#^figure5|figure 5]] : $V(M) = \frac{q}{4\pi\epsilon_0}\left(\frac{1}{r_1} - \frac{1}{r_2}\right)$.
> Utilisant les coordonnées sphériques d'axe $(Oz)$ indiquées sur la [[#^figure5|figure 5]], nous avons $r_1 = \left[r^{2} - dr\cos\theta + \frac{d^{2}}{4}\right]^{\frac{1}{2}}$ et $r_2 = \left[r^{2} + dr\cos\theta + \frac{d^{2}}{4}\right]^{\frac{1}{2}}$.
> Dans l'approximation dipolaire, nous écrirons à l'ordre un en $\left(\frac{d}{r}\right)$ : $V(M) = \frac{q}{4\pi\epsilon_0 r}((1 + \frac{1}{2}\frac{d}{r}\cos\theta + \ldots) - (1 - \frac{1}{2}\frac{d}{r}\cos\theta + \ldots))$.
> *Remarque : Notons que pour ce modèle de dipôle, le second terme non nul est proportionnel à $\displaystyle \frac{1}{r^{4}}$.*
> La charge totale de ce système étant nulle, le terme en $\frac{1}{r}$ du potentiel s'annule ; le premier terme non nul du développement limité est proportionnel à $\frac{d}{r^{2}}$. Il décroît beaucoup plus vite à grande distance que le potentiel d'une charge seule : $V(M) = \frac{qd\cos\theta}{4\pi\epsilon_0r^{2}} = \frac{1}{4\pi\epsilon_0}\frac{\overrightarrow{p}.\overrightarrow{r}}{r^{3}}$.
> ==**En utilisant l'expression du moment dipolaire, le *potentiel électrostatique* créé par un dipôle placé au point $O$, à l'ordre le plus bas en puissances de $\frac{d}{r}$, est : $\displaystyle V(M) = \frac{p\cos\theta}{4\pi\epsilon_0r^{2}} = \frac{1}{4\pi\epsilon_0}\frac{\overrightarrow{p}\,.\overrightarrow{r}}{r^{3}}$.**==
> Du fait de la symétrie de révolution de la distribution autour de l'axe $(Oz)$, ce potentiel ne dépend pas de l'angle $\varphi$.
> Remarque :
> *Pour une distribution de charges quelconque existant dans une zone réduite de l'espace au voisinage d'un point $P$, étudions le potentiel créé en $M$ ($r = PM$ étant grand devant les dimensions de la zone des charges) par cette distribution.*
> - *Si la charge totale $q$ de cette distribution est non nulle, le terme prépondérant du potentiel est $\frac{1}{4\pi\epsilon_0}\frac{q}{r}$. Soit un potentiel en $\frac{1}{r}$.*
> - *Si la charge $q$ est nulle, le terme précédent n'existe pas : il faut s'intéresser au moment dipolaire $\overrightarrow{p}$ de cet ensemble de charges. Si $\overrightarrow{p}$ est non nul, le terme prépondérant du potentiel est $\frac{1}{4\pi\epsilon_0}\frac{\overrightarrow{p}\,.\overrightarrow{r}}{r^{3}}$. Soit un potentiel en $\frac{1}{r^{2}}$.*
> - *Si la charge $q$ et le moment dipolaire $\overrightarrow{p}$ sont nuls, les termes précédents n'existent pas : il faudrait alors pousser plus loin le développement du potentiel $V(M)$.*

> [!note] Potentiel et champ créés par un dipôle : Champ du dipôle
> - Expression en coordonnées sphériques :
> Le développement de l'expression $\overrightarrow{E}(M) = \frac{q}{4\pi\epsilon_0}\left(\frac{\overrightarrow{e}_1}{r_{1}^{2}} - \frac{\overrightarrow{e}_2}{r_{2}^{2}}\right)$ est délicat et nous déterminons le champ en calculant le gradient du potentiel qui vient d'être obtenu. En coordonnées sphériques :
> $$
> \begin{cases}
> \displaystyle E_r =-\dfrac{\partial V}{\partial r} = \frac{1}{4\pi\epsilon_0}\frac{2p\cos\theta}{r^{3}}\\
> \displaystyle E_{\theta} =-\frac{1}{r}\dfrac{\partial V}{\partial \theta} = \frac{1}{4\pi\epsilon_0}\frac{p\sin\theta}{r^{3}}\\
> \displaystyle E_{\varphi} = -\frac{1}{r\sin\theta}\dfrac{\partial V}{\partial \varphi} = 0
> \end{cases}
> $$
> Le plan contenant $OM$ et l'axe $(Oz)$ est un *plan de symétrie* de la distribution, il est naturel de trouver $\overrightarrow{E} . \overrightarrow{e}_{\varphi} = 0$ ([[#^figure6|fig. 6]]).
> ==**L'expression du champ du dipôle est : $\displaystyle\overrightarrow{E}(M) = \frac{1}{4\pi\epsilon_0}\frac{2p\cos\theta . \overrightarrow{e}_r + p\sin\theta . \overrightarrow{e}_{\theta}}{r^{3}}$.**==
> - Expression intrinsèque :
> Le moment dipolaire $\overrightarrow{p}$ peut s'écrire $\overrightarrow{p} = p(cos\theta . \overrightarrow{e}_r - \sin\theta . \overrightarrow{e}_{\theta})$.
> Nous pouvons alors donner de $\overrightarrow{E}(M)$ une expression sous une forme intrinsèque (pour un dipôle en $O$, sans référence à un choix d'axes particulier).
> ==**Sous forme intrinsèque, le champ du dipôle est : $\displaystyle\overrightarrow{E}(M) = \frac{1}{4\pi\epsilon_0}\frac{(3(\overrightarrow{p}\,.\overrightarrow{e}_r)\overrightarrow{e}_r - \overrightarrow{p})}{r^{3}}$. Ou bien : $\displaystyle\overrightarrow{E}(M) = \frac{1}{4\pi\epsilon_0}\frac{(3(\overrightarrow{p}\,.\overrightarrow{r})\overrightarrow{r} - \overrightarrow{p}r^{2})}{r^{5}}$.**==
> Remarques :
> 	- *Le champ d'un dipôle $\displaystyle\left(\text{en}\,\frac{1}{r^{3}}\right)$ décroît plus vite que celui d'une charge ponctuelle $\displaystyle\left(\text{en}\,\frac{1}{r^{2}}\right)$.*
> 	- *La seule caractéristique du dipôle qui apparaît dans les expressions du potentiel $V(M)$ et dans celle du champ $\overrightarrow{E}(M)$ est son moment dipolaire $\overrightarrow{p}$.*
> 	***Un dipôle est entièrement caractérisé par son moment dipolaire.***

> [!note] Potentiel et champ créés par un dipôle : Topographie de E et V
> - Équation et description qualitative :
> La distribution de charges d'un dipôle, dont le moment dipolaire $\overrightarrow{p}$ est sur l'axe $(Oz)$, admet cet axe comme *axe de révolution*. De ce fait, l'équation du potentiel $V(M)$ ne dépend pas de la coordonnée $\varphi$ et les surfaces équipotentielles sont de révolution autour de $(Oz)$. Une représentation graphique de leurs traces dans un plan de symétrie $(\varphi = cte)$ contenant l'axe $(Oz)$ est dès lors suffisante ([[#^figure7|fig. 7]]).
> La ligne équipotentielle $V = V_0$ a pour équation polaire : $r^{2} = \frac{p}{4\pi\epsilon_0V_0}\cos\theta$.
> C'est l'équation d'une courbe fermée, symétrique par rapport à l'axe $(Oz)$ et passant par l'origine.
> Le signe de $\cos\theta$ reste constant sur la ligne équipotentielle. Si $V_0 > 0$, cette ligne équipotentielle se situe dans le demi-plan $z > 0$, du côté de la charge positive.
> Le plan médiateur $(xOy)$ du doublet correspond à l'équipotentielle $V = 0$. Ce plan médiateur est un plan d'*antisymétrie* de la distribution de charges, donc la ligne équipotentielle $V = -V_0$ est symétrique de la ligne $V = V_0$ par rapport au plan médiateur.
> Sur les lignes équipotentielles, la distance au point $O$ est maximale sur l'axe $(Oz)$. À l'inverse, cette distance s'annule lorsque $\theta$ tend vers $\frac{\pi}{2}$. Les lignes équipotentielles sont tangentes au plan médiateur $(xOy)$ du dipôle.
> Cette dernière constatation n'a cependant pas de réalité physique : au voisinage de l'origine, l'approximation dipolaire ne s'applique plus, et l'équipotentielle $V = V_0$ passe « quelque part » entre le point $O$ et la charge $+q$ ([[#^figure8|fig. 8]]).
> - Représentation :
> Sur la [[#^figure8|figure 8]] sont représentées les traces de quelques équipotentielles du système de deux charges dans un plan contenant l'axe $(Oz)$. La [[#^figure9|figure 9]] reprend ce tracé en utilisant la formule du potentiel dipolaire. Nous constatons que les deux figures sont semblables, sauf au voisinage du dipôle où l'approximation dipolaire n'est pas valable : la différence entre le doublet de charges et l'entité idéale apparaît nettement à courte distance.
> Les figures [[#^figure10|10]] et [[#^figure11|11]] montrent la visualisation du potentiel d'un doublet et du dipôle respectivement.

> [!note] Potentiel et champ créés par un dipôle : Topographie de E et V : Lignes de champ
> - Équation :
> Par définition, pour un déplacement élémentaire $d\overrightarrow{r}$ le long d'une ligne de champ, nous aurons $d\overrightarrow{r} \wedge \overrightarrow{E} = \overrightarrow{0}$. Utilisant les coordonnées sphériques du champ et l'expression $d\overrightarrow{r} = dr\,\overrightarrow{e}_r + rd\theta\,\overrightarrow{e}_{\theta} + r\sin\theta d\varphi\,\overrightarrow{e}_{\varphi}$ d'un déplacement élémentaire, nous obtenons : $$ \begin{cases} r\sin\theta d\varphi . E_{\theta} = 0\\ r\sin\theta d\varphi . E_{r} = 0\\ dr . E_{\theta} - rd\theta . E_{r} = 0\,. \end{cases}$$
> Hors les lignes de champ situées sur l'axe $(Oz)$ ($\theta = 0$ ou $\theta =\pi$), les deux premières équations imposent $\varphi = cte$. En effet, le système est de révolution autour de l'axe $(Oz)$ et les lignes de champ sont tracées dans les *plans de symétrie* passant par cet axe.
> La dernière équation s'explicite en $\sin\theta . dr = 2r . \cos\theta . d\theta$, ce qui donne, par intégration, l'équation des lignes de champ : $r = \text{cte}\,\sin^{2}\theta$.
> - Description qualitative et représentation :
> Les lignes de champ sont donc des courbes planes tracées dans des plans contenant l'axe de révolution $(Oz)$. Elles sont, en outre, symétriques par rapport au plan médiateur $(xOy)$, qui est un *plan d'antisymétrie* qu'elles coupent orthogonalement. Enfin, sur les lignes de champ, la distance au point $O$ est maximale sur le plan médiateur. Les lignes de champ sont tangentes à l'axe $(Oz)$. Cette dernière caractéristique géométrique est sans réalité physique car, au voisinage du point $O$, l'approximation dipolaire n'est plus vérifiée.
> Sur les figures [[#^figure12|12]] et [[#^figure13|13]], on trouve les cartes des lignes de champ et des lignes équipotentielles respectivement pour un doublet de deux charges opposées et pour un dipôle. On vérifie que les deux cartes sont équivalentes lorsque la distance d'observation est grande devant la taille du dipôle.

> [!note] Potentiel et champ créés par un dipôle : Généralisation
> Le modèle du dipôle s'applique en fait à toute distribution de charges de charge totale nulle.
> Considérons un ensemble de $N$ particules chargées, de position $P_i$ et de charges $q_i$ $(i \in (1\ldots N))$ telles que $\displaystyle\sum_{i=1}^{N}q_i = 0$ ([[#^figure14|fig. 14]]).
> Notons $\overrightarrow{a}_i = \overrightarrow{OP_i}$ le vecteur-position du point $P_i$.
> $\overrightarrow{OM} = r\overrightarrow{e}_r$ est le vecteur-position du point $M$ et nous effectuons les calculs dans l'approximation dipolaire : $r \gg a_i$ pour tout $i$.
> Le potentiel en un point $M$ est : $\displaystyle V = \sum_{i=1}^{N}V_i = \frac{1}{4\pi\epsilon_0}\sum_{i=1}^{N}\frac{q_i}{P_iM}$ et $\overrightarrow{P_iM} = r\overrightarrow{e}_r - \overrightarrow{a}_i$ soit : $P_iM^{2} = r^{2} - 2r\overrightarrow{e}_r\,.\,\overrightarrow{a}_i + a_{i}^{2}$ et $\displaystyle\frac{1}{P_iM} = \frac{1}{r}\left[1 + \left(\frac{a_{i}^{2}}{r^{2}} - 2\frac{\overrightarrow{e}_r\,.\,\overrightarrow{a}_i}{r}\right)\right]^{-\frac{1}{2}}$.
> En se limitant au premier ordre en $\displaystyle\frac{a_{i}}{r}$ : $\displaystyle\frac{1}{r_i} = \frac{1}{r}\left[1 + \frac{\overrightarrow{e}_r\,.\,\overrightarrow{a}_i}{r}\right]$ et $\displaystyle V = \frac{1}{4\pi\epsilon_0}\Bigg[\frac{\sum\limits_{i=1}^{N}q_i}{r} + \frac{\left(\sum\limits_{i=1}^{N}q_i\overrightarrow{a}_i\right).\overrightarrow{e}_r}{r^{2}}\Bigg]$.
> Si nous définissons le moment dipolaire de la distribution par : $\overrightarrow{p} = \sum\limits_{i=1}^{N}q_i\overrightarrow{OP_i}$, alors, le potentiel en $M$ se met sous la même forme que celui d'un doublet de charges : $\displaystyle V(M) = \frac{\overrightarrow{p}\,.\overrightarrow{e}_r}{4\pi\epsilon_0r^{2}}$.
> Nous avons montré que le modèle élémentaire du doublet peut en fait s'appliquer à toute distribution globalement neutre et de moment dipolaire $\overrightarrow{p} = \sum\limits_{i=1}^{N}q_i\overrightarrow{OP_i}$ non nul.

> [!note] Actions d'un champ électrostatique sur un dipôle
> Nous supposons dans un premier temps que le dipôle est rigide, c'est-à-dire que la distance $AB$ reste fixe et les charges constantes.
> Les actions mécaniques exercées sur le dipôle seront caractérisées par leur résultante $\overrightarrow{F}$ et leur moment $\overrightarrow{\Gamma}_O$ calculé par rapport à un point $O$ donné.
> - Champ uniforme :
> 
> Force : Les forces exercées sur les charges $+q$ et $-q$ par le champ uniforme sont opposées. Par conséquent :
> ==**La résultante des forces qui s'exercent sur un dipôle placé dans un champ uniforme est nulle : $\overrightarrow{F} = \overrightarrow{0}$.**==
> Le dipôle est donc soumis à un *couple* de forces.
> 
> Moment : Calculons par exemple ce moment par rapport au point $O$, milieu des deux charges : $\overrightarrow{\Gamma}_O = \left(\frac{\overrightarrow{d}}{2}\right)\wedge(q\overrightarrow{E}_0) + \left(-\frac{\overrightarrow{d}}{2}\right)\wedge(-q\overrightarrow{E}_0) = q\overrightarrow{d}\wedge\overrightarrow{E}_0$.
> Pour un couple (force résultante nulle), le moment est indépendant du point où il est évalué. Il vaut donc en tout point $\overrightarrow{\Gamma} = \overrightarrow{p}\wedge\overrightarrow{E}_0$.
> En observant la [[#^figure15|figure 15]], nous pouvons résumer l'influence du champ appliqué en disant que :
> ==**Dans un champ uniforme, le dipôle subit un couple de moment $\overrightarrow{\Gamma} = \overrightarrow{p}\wedge\overrightarrow{E}_0$ qui tend à l'aligner parallèlement au champ appliqué dans le même sens que celui-ci.**==

> [!note] Actions d'un champ électrostatique sur un dipôle : Cas d'un champ non uniforme
> Soit une zone de l'espace où existe un champ électrique $\overrightarrow{E}(M)$ : plaçons dans ce champ un dipôle, et cherchons l'action de ce champ.
> Le dipôle de moment dipolaire $\overrightarrow{p} = q\overrightarrow{NP}$ est constitué d'une charge $-q$ en $N$ où existe initialement un champ $\overrightarrow{E}(N)$, et une charge $+q$ en $P$ où existe le champ $\overrightarrow{E}(P)$. Appelons $O$ le centre du vecteur $\overrightarrow{NP}$ de composantes $\overrightarrow{NP} = (\delta x, \delta y, \delta z)$ ([[#^figure16|fig. 16]]). Les composantes du moment dipolaire sont donc $\overrightarrow{p} : (q\delta x, q\delta y, q\delta z)$.
> - Approximation du calcul :
> Dans le cas d'actions subies par le dipôle, l'approximation dipolaire consiste à supposer la taille $d = \left\Vert\overrightarrow{NP}\right\Vert$ du dipôle faible devant la distance $L_c$, longueur caractéristique de variation du champ électrostatique appliqué ; on supposera, par exemple, que le champ électrostatique varie de $\left\Vert\overrightarrow{E}(M_1)\right\Vert$ à $\left\Vert\overrightarrow{E}(M_2)\right\Vert \approx 2\left\Vert\overrightarrow{E}(M_1)\right\Vert$ sur une distance de l'ordre de $L_c$ ([[#^figure16|fig. 16]]).
> Calculons ainsi un ordre de grandeur de : $\frac{\left\Vert\overrightarrow{E}(P) - \overrightarrow{E}(N)\right\Vert}{\left\Vert\overrightarrow{E}(O)\right\Vert} = \frac{\left\Vert\delta\overrightarrow{E}\right\Vert}{\left\Vert\overrightarrow{E}(O)\right\Vert}$ ;
> la composante suivant $x$ de $\delta\overrightarrow{E}$ peut s'écrire : $\delta E_x \approx \left(\dfrac{\partial E_x}{\partial x}\right)_{\!O}\delta x + \left(\dfrac{\partial E_x}{\partial y}\right)_{\!O}\delta y + \left(\dfrac{\partial E_x}{\partial z}\right)_{\!O}\delta z = \overrightarrow{NP} . \overrightarrow{grad_O}(E_x)$.
> La quantité $\left\Vert\overrightarrow{grad_O}(E_x)\right\Vert$ étant de l'ordre de grandeur de $\left|\frac{E_{O_x}}{L_c}\right|$, nous pouvons écrire :
> ==**Dans l'approximation dipolaire, les variations relatives du champ extérieur appliqué sur un dipôle sont négligeables, de l'ordre de $\displaystyle\frac{d}{L_c}$, rapport entre la taille du dipôle et la distance caractéristique de variation du champ : $\displaystyle\frac{\left\Vert\overrightarrow{E}(M) - \overrightarrow{E}(O)\right\Vert}{\left\Vert\overrightarrow{E}(O)\right\Vert} \approx \frac{d}{L_c} \ll 1$, pour $\left\Vert\overrightarrow{OM}\right\Vert \approx d$.**==
> Cherchons les effets de ce champ légèrement non uniforme à l'échelle du dipôle.

> [!note] Actions d'un champ électrostatique sur un dipôle : Cas d'un champ non uniforme : Moment en $O$ des forces s'exerçant sur le dipôle
> Le moment $\overrightarrow{\Gamma}_O$ en $O$ des forces s'exerçant sur le dipôle est égal à : $\overrightarrow{\Gamma}_O = q\bigg(\overrightarrow{OP}\wedge\overrightarrow{E}(P) - \overrightarrow{ON}\wedge\overrightarrow{E}(N)\bigg)$ avec $\overrightarrow{OP} = -\overrightarrow{ON} = \frac{\overrightarrow{NP}}{2}$, on obtient en notant $\overrightarrow{\delta E}(P) = \overrightarrow{E}(P) - \overrightarrow{E}(O)$ et $\overrightarrow{\delta E}(N) = \overrightarrow{E}(N) - \overrightarrow{E}(O)$ :
> $$
> \begin{align}
> \overrightarrow{\Gamma}_O &= q\bigg(\overrightarrow{OP}\wedge\bigg(\overrightarrow{E}(O) + \overrightarrow{\delta E}(P)\bigg) - \overrightarrow{ON}\wedge\bigg(\overrightarrow{E}(O) + \overrightarrow{\delta E}(N)\bigg)\bigg)\\
> &= q\overrightarrow{NP}\wedge\overrightarrow{E}(O) + q\frac{\overrightarrow{NP}}{2}\wedge\bigg(\overrightarrow{\delta E}(P) + \overrightarrow{\delta E}(N)\bigg)\\
> &= \overrightarrow{p}\wedge\overrightarrow{E}(O) + \overrightarrow{p}\wedge\frac{\overrightarrow{\delta E}(P) + \overrightarrow{\delta E}(N)}{2}
> \end{align}
> $$
> Les calculs précédents ont montré que les normes de $\overrightarrow{\delta E}(P)$ et $\overrightarrow{\delta E}(N)$ sont négligeables devant celle de $\overrightarrow{E}(O)$, donc nous écrivons :
> ==**Dans un champ non uniforme, le moment en $O$ des forces s'exerçant sur un dipôle est égal à : $\overrightarrow{\Gamma}_O = \overrightarrow{p}\wedge\overrightarrow{E}(O)$. Dans un champ électrique, le dipôle s'aligne sur la ligne de champ qui passe par son centre.**==

> [!note] Actions d'un champ électrostatique sur un dipôle : Cas d'un champ non uniforme : Force
> - La force est-elle nulle ? :
> La force s'exerçant sur le dipôle est : $\overrightarrow{F} = -q\overrightarrow{E}(N) + q\overrightarrow{E}(P) = q\bigg(\overrightarrow{E}(P) - \overrightarrow{E}(N)\bigg)$.
> Comme le champ est non uniforme, cette quantité est non nulle :
> ==**En présence d'un champ non uniforme, une force non nulle s'exerce sur le dipôle.**==
> - Mise en évidence de l'orientation de cette force :
> S'il n'y a pas de contraintes extérieures l'empêchant d'évoluer, le dipôle s'aligne sur la ligne de champ passant par son centre ([[#^figure17|fig. 17]]) ($\overrightarrow{p}$ et $\overrightarrow{E}$ sont alors parallèles et de même sens). Examinons les diverses situations où nous avons fait apparaître les lignes de champs, avec les orientations du champ : le dipôle, orienté parallèlement à $\overrightarrow{E}$ et dans le même sens, est toujours attiré par les champs forts.
> - Cas général :
> La composante $F_x$ (par exemple) de la force $\overrightarrow{F} = q\bigg(\overrightarrow{E}(P) - \overrightarrow{E}(N)\bigg)$ s'exerçant sur le dipôle est donnée par : $F_x = q(E_x(P) - E_x(N)) = q\left(\dfrac{\partial E_x}{\partial x}\delta x + \dfrac{\partial E_x}{\partial y}\delta y + \dfrac{\partial E_x}{\partial z}\delta z\right)$.
> Les composantes du moment dipolaire étant $q\delta x$, $q\delta y$ et $q\delta z$, cela donne : $F_x = p_x\dfrac{\partial E_x}{\partial x} + p_y\dfrac{\partial E_x}{\partial y} + p_z\dfrac{\partial E_x}{\partial z}$.
> Nous avons vu dans l'Application 2 du chapitre 3 que : $\dfrac{\partial E_x}{\partial y} = \dfrac{\partial E_y}{\partial x}$ et $\dfrac{\partial E_z}{\partial x} = \dfrac{\partial E_x}{\partial z}$ on obtient donc : $F_x = p_x\dfrac{\partial E_x}{\partial x} + p_y\dfrac{\partial E_y}{\partial x} + p_z\dfrac{\partial E_z}{\partial x}$ relation qui s'écrit : $F_x = \overrightarrow{p}\,\,\dfrac{\partial \overrightarrow{E}}{\partial x}$.
> On a donc : $\overrightarrow{F} = \left(\overrightarrow{p}\,\,\,.\,\dfrac{\partial \overrightarrow{E}}{\partial x}\right)\overrightarrow{e}_x + \left(\overrightarrow{p}\,\,\,.\,\dfrac{\partial \overrightarrow{E}}{\partial y}\right)\overrightarrow{e}_y + \left(\overrightarrow{p}\,\,\,.\,\dfrac{\partial \overrightarrow{E}}{\partial z}\right)\overrightarrow{e}_z$.

> [!note] Actions d'un champ électrostatique sur un dipôle : Cas d'un champ non uniforme : Interprétation
> Retrouve-t-on l'orientation de la force précédente, c'est-à-dire que les dipôles, une fois alignés sur le champ local, sont attirés par les champs forts ?
> Examinons la [[#^figure18|figure 18]] sur lequel nous avons repris les quatre cas de [[#^figure17|figure 17]]. Les forces obéissent bien, en orientation, à l'expression précédente en considérant les diverses orientations des champs et des gradients de champ.
> ==**Dans un champ électrique uniforme ou non, un dipôle a tendance à s'aligner sur la ligne de champ qui passe par son centre ; le dipôle, orienté parallèlement au champ local et dans le même sens, est alors attiré par les champs forts.**==

> [!note] Actions d'un champ électrostatique sur un dipôle : Cas d'un dipôle non rigide
> Si le dipôle n'est pas rigide, ses caractéristiques dépendent du champ appliqué. Sous l'action du champ, les répartitions de charges (de l'atome ou de la molécule par exemple) sont modifiées. Le moment dipolaire dépend du champ électrostatique : $\overrightarrow{p} = \overrightarrow{p}(\overrightarrow{E})$.
> Une fois le champ établi, les caractéristiques du dipôle sont bien déterminées et son moment dipolaire connu. Les calculs précédents sont donc applicables en considérant pour $\overrightarrow{p}$, la valeur du moment dipolaire en présence du champ $\overrightarrow{p}(\overrightarrow{E})$. Pour le calcul de la force, nous pouvons raisonner avec ce moment dipolaire comme s'il était rigide.
> *Remarque : La matière, sous l'action d'un champ appliqué, acquiert généralement une polarisation (densité volumique de dipôles) de même sens que le champ appliqué, de sorte que la matière dévie vers les zones de champ fort.*

> [!note] Énergie potentielle d'interaction : Énergie potentielle d'interaction entre un dipôle rigide et un champ extérieur
> Dans une distribution de charges ponctuelles, si les interactions entre les charges sont neutralisées par des contraintes, l'énergie potentielle de la distribution dans un champ électrostatique extérieur est la somme des énergies potentielles de chacune des charges de la distribution.
> Dans le cas d'un dipôle *rigide*, l'interaction électrostatique entre les deux charges est neutralisée par la structure du dipôle qui maintient ces deux charges à une distance $d$ constante.
> L'énergie potentielle d'un tel dipôle est donc due uniquement à l'interaction entre les deux charges $\pm q$ et le champ extérieur.
> Nous avons vu ([[02-Champ électrostatique|chapitre 2]]) que l'énergie potentielle d'une charge $q$ dans un champ créant le potentiel $V$ est : $\mathcal{E}_p = qV$. Cela étant, l'énergie potentielle du dipôle *rigide* est : $\mathcal{E}_p = qV\left(\overrightarrow{r} + \frac{\overrightarrow{d}}{2}\right) - qV\left(\overrightarrow{r} - \frac{\overrightarrow{d}}{2}\right)$.
> Comme nous sommes fondés à écrire : $V\left(\overrightarrow{r} \pm \frac{\overrightarrow{d}}{2}\right) = V(\overrightarrow{r}) \pm \overrightarrow{grad}(V(\overrightarrow{r}))\,\,.\frac{\overrightarrow{d}}{2}$ il vient : $\mathcal{E}_p = q\,\overrightarrow{grad}(V(\overrightarrow{r}))\,\,.d = p\,\,.\overrightarrow{grad}(V(\overrightarrow{r})) = -\overrightarrow{p}\,\,.\overrightarrow{E}(\overrightarrow{r})$.
> ==**L'énergie potentielle d'interaction entre un dipôle rigide et le champ appliqué est : $\mathcal{E}_p = -\overrightarrow{p}\,\,.\overrightarrow{E}$.**==
> Notons que le travail fournit par un opérateur lors d'un déplacement élémentaire du dipôle rigide s'écrit : $\delta W_{op} = d\mathcal{E}_p = d(-\overrightarrow{p}\,\,.\overrightarrow{E}) = -\overrightarrow{p}\,\,.d\overrightarrow{E} - d\overrightarrow{p}\,\,.\overrightarrow{E}$. Il serait possible, à partir de cette expression, de retrouver la force et le moment s'exerçant sur un dipôle.
> *Remarque : Dipôle rigide signifie $\left\Vert\,\,\overrightarrow{p}\,\,\right\Vert = cte$. Nous n'aurons $\overrightarrow{p} = \overrightarrow{cte}$ que si le dipôle subit une translation.*
# Définitions
> [!note] Objets polaires
> - Molécules polaires :
> Ces molécules présentent au repos une séparation de charges.
> Une molécule diatomique telle que le chlorure d'hydrogène $HCl$ possède *une liaison polaire* ([[#^figure2|fig. 2]]). Son nuage électronique est asymétrique, les électrons se trouvant préférentiellement au voisinage de l'atome de chlore.
> Des édifices moléculaires plus complexes présenteront de même une polarité permanente : la molécule d'eau $H_2O$, triangulaire, possède un moment dipolaire résultant de la polarité des liaisons $OH$. De même la molécule d'ammoniac $NH_3$, pyramidale, possède trois liaisons $NH$ polarisées ([[#^figure3|fig. 3]]). Dans les molécules polyatomiques, la présence de doublets libres sur certains atomes doit parfois être prise en compte.
> - Polarisation due à un champ appliqué :
> Un atome et une molécule peuvent aussi être polarisés par l'action d'un champ appliqué : en effet, celui-ci déplace en sens opposé les charges positives et négatives. Les nuages électroniques sont déformés par ce champ appliqué, les longueurs et les angles des liaisons chimiques peuvent être modifiés. Ces modifications, généralement faibles, correspondent à une apparition ou à un changement de la polarité ([[#^figure4|fig. 4]]). On parle d'atomes ou de molécules *polarisables*.
> Remarques :
> *Les atomes, les ions, les molécules (polaires ou non au repos) et plus généralement les milieux matériels sont susceptibles d'être polarisés par un champ appliqué.*
> *Ainsi un certain nombre de phénomènes liés à la polarisation peuvent être observés dans la matière.*
> 	- *Les ions d'un cristal ionique se trouvent déplacés par l'action d'un champ appliqué par rapport à leur position au repos (en sens opposé pour des charges de signes opposés), ce qui fait apparaître de nouveaux moments dipolaires. Ce phénomène porte le nom de polarisation ionique.*
> 	- *Nous verrons aussi qu'un dipôle tend à s'orienter parallèlement au champ qui lui est appliqué. Un matériau contenant des entités polaires susceptibles de s'orienter peut ainsi être polarisé lorsqu'un champ lui est appliqué (une compétition s'engage entre l'effet d'orientation du champ appliqué et la tendance au désordre liée à l'agitation thermique). On parle alors de polarisation d'orientation.*
> - Unité de moment dipolaire en chimie :
> Les entités chimiques ont des charges de l'ordre de $q = 10^{-19} C$ et des dimensions de l'ordre de $l = 10^{-10} m$. Une unité de moment dipolaire adaptée aux besoins des chimistes doit être de l'ordre de $p = ql = 10^{-29} C.m$. C'est pour cette raison que les chimistes utilisent le **debye** (symbole : $D$), bien que cette unité de moment dipolaire appartienne à un système d'unités actuellement abandonné. ==**$1D = \frac{1}{3}.10^{-29} C.m$**==.
# Diagrammes
Doublet de charges
![[electromagnetisme1/attachments-electromagnetisme1/figure54.png]]^figure1

Molécule diatomique
![[electromagnetisme1/attachments-electromagnetisme1/figure55.png]]^figure2

Moments dipolaires des molécules $H_2O$ et $NH_3$
![[electromagnetisme1/attachments-electromagnetisme1/figure56.png]]^figure3

Polarisation d'un atome placé dans un champ $\overrightarrow{E}$ : $\overrightarrow{p} = \alpha\overrightarrow{E}$, avec $\alpha > 0$
![[electromagnetisme1/attachments-electromagnetisme1/figure57.png]]^figure4

Le point $M$ est repéré par son vecteur position $\overrightarrow{r} = \overrightarrow{OM}$ ou par ses coordonnées sphériques : $(r, \theta, \varphi)$
![[electromagnetisme1/attachments-electromagnetisme1/figure58.png]]^figure5

Orientation de $\overrightarrow{E}$ créé un dipôle $\overrightarrow{p}$
![[electromagnetisme1/attachments-electromagnetisme1/figure59.png]]^figure6

Distribution de charges
![[electromagnetisme1/attachments-electromagnetisme1/figure67.png]]^figure14

Dipôle dans un champ uniforme
![[electromagnetisme1/attachments-electromagnetisme1/figure68.png]]^figure15

Dans l'approximation dipolaire, $d \ll L_c$
![[electromagnetisme1/attachments-electromagnetisme1/figure69.png]]^figure16

Sur ces divers documents $a$, $b$, $c$ et $d$, le dipôle, orienté parallèlement à $\overrightarrow{E}$ et dans le même sens, est toujours attiré par les champs forts
![[electromagnetisme1/attachments-electromagnetisme1/figure70.png]]
![[electromagnetisme1/attachments-electromagnetisme1/figure71.png]]^figure17

Sur ces divers documents $a$, $b$, $c$ et $d$, le dipôle orienté parallèlement à $\overrightarrow{E}$ et dans le même sens est toujours attiré par les champs forts, conforme à l'expression de la force en $\overrightarrow{F} = \left(\overrightarrow{p}\,\,\,.\,\dfrac{\partial \overrightarrow{E}}{\partial x}\right)\overrightarrow{e}_x$
![[electromagnetisme1/attachments-electromagnetisme1/figure72.png]]![[electromagnetisme1/attachments-electromagnetisme1/figure73.png]]^figure18
# Graphiques
Équipotentielles $\pm V_0$ du dipôle
![[electromagnetisme1/attachments-electromagnetisme1/figure60.png]]^figure7

Équipotentielles d'un doublet ($-q$ , $+q$)
![[electromagnetisme1/attachments-electromagnetisme1/figure61.png]]^figure8

Équipotentielles d'un dipôle
![[electromagnetisme1/attachments-electromagnetisme1/figure62.png]]^figure9

Visualisation du potentiel créé par deux charges $-q$ et $+q$ (en noir $V > 0$, en bleu $V < 0$)
![[electromagnetisme1/attachments-electromagnetisme1/figure63.png]]^figure10

Visualisation du potentiel du dipôle dans l'espace (en noir $V > 0$, en bleu $V < 0$)
![[electromagnetisme1/attachments-electromagnetisme1/figure64.png]]^figure11

Équipotentielles et lignes de champ d'un doublet
![[electromagnetisme1/attachments-electromagnetisme1/figure65.png]]^figure12

Équipotentielles et lignes de champ d'un dipôle
![[electromagnetisme1/attachments-electromagnetisme1/figure66.png]]^figure13
# Expériences

# Autres notes
