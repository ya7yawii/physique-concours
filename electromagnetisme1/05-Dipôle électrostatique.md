---
titre: "[[05-Dipôle électrostatique]]"
tags:
aliases:
crée: 03-01-2026, 10:51
---
# Formules
> [!note] Moment dipolaire
> -  Moment dipolaire d’une distribution de charges globalement neutre :
> Considérons dans la distribution $\mathcal{D}$ l’ensemble des charges positives dont la somme est notée $+q$ et l’ensemble des charges négatives dont la somme vaut $-q$, $q$ étant supposée non nulle.
> Nous pouvons définir $A^{+}$, le barycentre des charges positives de $\mathcal{D}$, et $A^{-}$ le barycentre des charges négatives de $\mathcal{D}$.
> Le moment dipolaire de la distribution est par définition : $\overrightarrow{p} = q\overrightarrow{A^{-}A^{+}}$.
> Il s’évalue en coulomb . mètre $(C . m)$.
> - Doublet de charges :
> Le modèle le plus simple de dipôle est un doublet de charges opposées et séparées par une distance que nous noterons $d$ ([[#^figure1|fig. 1]]).
> ==**Un objet non chargé mais polarisé crée à grande distance un potentiel et un champ analogues (en première approximation) à ceux d’un doublet de charges de moment dipolaire $\overrightarrow{p}$ non nul $(q > 0)$ : $\overrightarrow{p} = q\overrightarrow{d}$ et $\overrightarrow{d} = \overrightarrow{A^{-}A^{+}}$.**==

> [!note] Potentiel et champ créés par un dipôle
> Nous nous limiterons au calcul et à la représentation de ces grandeurs pour le modèle du doublet.
> - Approximation dipolaire :
> Si nous nous intéressons aux effets produits par le dipôle, l’approximation dipolaire consiste à supposer *la distance à laquelle nous observons le champ créé par le dipôle très grande devant ses dimensions : $r \gg d$.*
> Dans ces conditions, nous mènerons les calculs en ne déterminant que les termes d’ordre le plus bas en $\left(\frac{d}{r}\right)$.

> [!note] Potentiel et champ créés par un dipôle : Potentiel du dipôle
> La distribution considérée (doublet) étant d’extension finie, nous pouvons *choisir le potentiel nul à l’infini*, et l’écrire, avec les notations de [[#^figure5|figure 5]] : $V(M) = \frac{q}{4\pi\epsilon_0}\left(\frac{1}{r_1} - \frac{1}{r_2}\right)$.
> Utilisant les coordonnées sphériques d’axe $(Oz)$ indiquées sur la [[#^figure5|figure 5]], nous avons $r_1 = \left[r^{2} - dr\cos\theta + \frac{d^{2}}{4}\right]^{\frac{1}{2}}$ et $r_2 = \left[r^{2} + dr\cos\theta + \frac{d^{2}}{4}\right]^{\frac{1}{2}}$.
> Dans l’approximation dipolaire, nous écrirons à l’ordre un en $\left(\frac{d}{r}\right)$ : $V(M) = \frac{q}{4\pi\epsilon_0 r}((1 + \frac{1}{2}\frac{d}{r}\cos\theta + \cdots) - (1 - \frac{1}{2}\frac{d}{r}\cos\theta + \cdots))$.
> *Remarque : Notons que pour ce modèle de dipôle, le second terme non nul est proportionnel à $\displaystyle \frac{1}{r^{4}}$.*
> La charge totale de ce système étant nulle, le terme en $\frac{1}{r}$ du potentiel s’annule ; le premier terme non nul du développement limité est proportionnel à $\frac{d}{r^{2}}$. Il décroît beaucoup plus vite à grande distance que le potentiel d’une charge seule : $V(M) = \frac{qd\cos\theta}{4\pi\epsilon_0r^{2}} = \frac{1}{4\pi\epsilon_0}\frac{\overrightarrow{p}.\overrightarrow{r}}{r^{3}}$.
> ==**En utilisant l’expression du moment dipolaire, le *potentiel électrostatique* créé par un dipôle placé au point $O$, à l’ordre le plus bas en puissances de $\frac{d}{r}$, est : $\displaystyle V(M) = \frac{p\cos\theta}{4\pi\epsilon_0r^{2}} = \frac{1}{4\pi\epsilon_0}\frac{\overrightarrow{p}\,.\overrightarrow{r}}{r^{3}}$.**==
> Du fait de la symétrie de révolution de la distribution autour de l’axe $(Oz)$, ce potentiel ne dépend pas de l’angle $\varphi$.
> Remarque :
> *Pour une distribution de charges quelconque existant dans une zone réduite de l’espace au voisinage d’un point $P$, étudions le potentiel créé en $M$ ($r = PM$ étant grand devant les dimensions de la zone des charges) par cette distribution.*
> - *Si la charge totale $q$ de cette distribution est non nulle, le terme prépondérant du potentiel est $\frac{1}{4\pi\epsilon_0}\frac{q}{r}$. Soit un potentiel en $\frac{1}{r}$.*
> - *Si la charge $q$ est nulle, le terme précédent n’existe pas : il faut s’intéresser au moment dipolaire $\overrightarrow{p}$ de cet ensemble de charges. Si $\overrightarrow{p}$ est non nul, le terme prépondérant du potentiel est $\frac{1}{4\pi\epsilon_0}\frac{\overrightarrow{p}\,.\overrightarrow{r}}{r^{3}}$. Soit un potentiel en $\frac{1}{r^{2}}$.*
> - *Si la charge $q$ et le moment dipolaire $\overrightarrow{p}$ sont nuls, les termes précédents n’existent pas : il faudrait alors pousser plus loin le développement du potentiel $V(M)$.*

> [!note] Potentiel et champ créés par un dipôle : Champ du dipôle
> - Expression en coordonnées sphériques :
> Le développement de l'expression $\overrightarrow{E}(M) = \frac{q}{4\pi\epsilon_0}\left(\frac{\overrightarrow{e}_1}{r_{1}^{2}} - \frac{\overrightarrow{e}_2}{r_{2}^{2}}\right)$ est délicat et nous déterminons le champ en calculant le gradient du potentiel qui vient d’être obtenu. En coordonnées sphériques :
> $$
> \begin{cases}
> \displaystyle E_r =-\dfrac{\partial V}{\partial r} = \frac{1}{4\pi\epsilon_0}\frac{2p\cos\theta}{r^{3}}\\
> \displaystyle E_{\theta} =-\frac{1}{r}\dfrac{\partial V}{\partial \theta} = \frac{1}{4\pi\epsilon_0}\frac{p\sin\theta}{r^{3}}\\
> \displaystyle E_{\varphi} = -\frac{1}{r\sin\theta}\dfrac{\partial V}{\partial \varphi} = 0
> \end{cases}
> $$
> Le plan contenant $OM$ et l’axe $(Oz)$ est un *plan de symétrie* de la distribution, il est naturel de trouver $\overrightarrow{E} . \overrightarrow{e}_{\varphi} = 0$ ([[#^figure6|fig. 6]]).
> ==**L’expression du champ du dipôle est : $\displaystyle\overrightarrow{E}(M) = \frac{1}{4\pi\epsilon_0}\frac{2p\cos\theta . \overrightarrow{e}_r + p\sin\theta . \overrightarrow{e}_{\theta}}{r^{3}}$.**==
> - Expression intrinsèque :
> Le moment dipolaire $\overrightarrow{p}$ peut s’écrire $\overrightarrow{p} = p(cos\theta . \overrightarrow{e}_r - \sin\theta . \overrightarrow{e}_{\theta})$.
> Nous pouvons alors donner de $\overrightarrow{E}(M)$ une expression sous une forme intrinsèque (pour un dipôle en $O$, sans référence à un choix d’axes particulier).
> ==**Sous forme intrinsèque, le champ du dipôle est : $\displaystyle\overrightarrow{E}(M) = \frac{1}{4\pi\epsilon_0}\frac{(3(\overrightarrow{p}\,.\overrightarrow{e}_r)\overrightarrow{e}_r - \overrightarrow{p})}{r^{3}}$. Ou bien : $\displaystyle\overrightarrow{E}(M) = \frac{1}{4\pi\epsilon_0}\frac{(3(\overrightarrow{p}\,.\overrightarrow{r})\overrightarrow{r} - \overrightarrow{p}r^{2})}{r^{5}}$.**==
> Remarques :
> 	- *Le champ d’un dipôle $\displaystyle\left(\text{en}\,\frac{1}{r^{3}}\right)$ décroît plus vite que celui d’une charge ponctuelle $\displaystyle\left(\text{en}\,\frac{1}{r^{2}}\right)$.*
> 	- *La seule caractéristique du dipôle qui apparaît dans les expressions du potentiel $V(M)$ et dans celle du champ $\overrightarrow{E}(M)$ est son moment dipolaire $\overrightarrow{p}$.*
> 	***Un dipôle est entièrement caractérisé par son moment dipolaire.***

> [!note] Topographie de E et V
> - Équation et description qualitative :
> La distribution de charges d’un dipôle, dont le moment dipolaire $\overrightarrow{p}$ est sur l’axe $(Oz)$, admet cet axe comme *axe de révolution*. De ce fait, l’équation du potentiel $V(M)$ ne dépend pas de la coordonnée $\varphi$ et les surfaces équipotentielles sont de révolution autour de $(Oz)$. Une représentation graphique de leurs traces dans un plan de symétrie $(\varphi = cte)$ contenant l’axe $(Oz)$ est dès lors suffisante ([[#^figure7|fig. 7]]).
> La ligne équipotentielle $V = V_0$ a pour équation polaire : $r^{2} = \frac{p}{4\pi\epsilon_0V_0}\cos\theta$.
> C’est l’équation d’une courbe fermée, symétrique par rapport à l’axe $(Oz)$ et passant par l’origine.
> Le signe de $\cos\theta$ reste constant sur la ligne équipotentielle. Si $V_0 > 0$, cette ligne équipotentielle se situe dans le demi-plan $z > 0$, du côté de la charge positive.
> Le plan médiateur $(xOy)$ du doublet correspond à l’équipotentielle $V = 0$. Ce plan médiateur est un plan d’*antisymétrie* de la distribution de charges, donc la ligne équipotentielle $V = -V_0$ est symétrique de la ligne $V = V_0$ par rapport au plan médiateur.
> Sur les lignes équipotentielles, la distance au point $O$ est maximale sur l’axe $(Oz)$. À l’inverse, cette distance s’annule lorsque $\theta$ tend vers $\frac{\pi}{2}$. Les lignes équipotentielles sont tangentes au plan médiateur $(xOy)$ du dipôle.
> Cette dernière constatation n’a cependant pas de réalité physique : au voisinage de l’origine, l’approximation dipolaire ne s’applique plus, et l’équipotentielle $V = V_0$ passe « quelque part » entre le point $O$ et la charge $+q$ ([[#^figure8|fig. 8]]).
> - Représentation :
> Sur la [[#^figure8|figure 8]] sont représentées les traces de quelques équipotentielles du système de deux charges dans un plan contenant l’axe $(Oz)$. La [[#^figure9|figure 9]] reprend ce tracé en utilisant la formule du potentiel dipolaire. Nous constatons que les deux figures sont semblables, sauf au voisinage du dipôle où l’approximation dipolaire n’est pas valable : la différence entre le doublet de charges et l’entité idéale apparaît nettement à courte distance.
> Les figures [[#^figure10|10]] et [[#^figure11|11]] montrent la visualisation du potentiel d'un doublet et du dipôle respectivement.
# Définitions
> [!note] Objets polaires
> - Molécules polaires :
> Ces molécules présentent au repos une séparation de charges.
> Une molécule diatomique telle que le chlorure d’hydrogène $HCl$ possède *une liaison polaire* ([[#^figure2|fig. 2]]). Son nuage électronique est asymétrique, les électrons se trouvant préférentiellement au voisinage de l’atome de chlore.
> Des édifices moléculaires plus complexes présenteront de même une polarité permanente : la molécule d’eau $H_2O$, triangulaire, possède un moment dipolaire résultant de la polarité des liaisons $OH$. De même la molécule d’ammoniac $NH_3$, pyramidale, possède trois liaisons $NH$ polarisées ([[#^figure3|fig. 3]]). Dans les molécules polyatomiques, la présence de doublets libres sur certains atomes doit parfois être prise en compte.
> - Polarisation due à un champ appliqué :
> Un atome et une molécule peuvent aussi être polarisés par l’action d’un champ appliqué : en effet, celui-ci déplace en sens opposé les charges positives et négatives. Les nuages électroniques sont déformés par ce champ appliqué, les longueurs et les angles des liaisons chimiques peuvent être modifiés. Ces modifications, généralement faibles, correspondent à une apparition ou à un changement de la polarité ([[#^figure4|fig. 4]]). On parle d’atomes ou de molécules *polarisables*.
> Remarques :
> *Les atomes, les ions, les molécules (polaires ou non au repos) et plus généralement les milieux matériels sont susceptibles d’être polarisés par un champ appliqué.*
> *Ainsi un certain nombre de phénomènes liés à la polarisation peuvent être observés dans la matière.*
> 	- *Les ions d’un cristal ionique se trouvent déplacés par l’action d’un champ appliqué par rapport à leur position au repos (en sens opposé pour des charges de signes opposés), ce qui fait apparaître de nouveaux moments dipolaires. Ce phénomène porte le nom de polarisation ionique.*
> 	- *Nous verrons aussi qu’un dipôle tend à s’orienter parallèlement au champ qui lui est appliqué. Un matériau contenant des entités polaires susceptibles de s’orienter peut ainsi être polarisé lorsqu’un champ lui est appliqué (une compétition s’engage entre l’effet d’orientation du champ appliqué et la tendance au désordre liée à l’agitation thermique). On parle alors de polarisation d’orientation.*
> - Unité de moment dipolaire en chimie :
> Les entités chimiques ont des charges de l’ordre de $q = 10^{-19} C$ et des dimensions de l’ordre de $l = 10^{-10} m$. Une unité de moment dipolaire adaptée aux besoins des chimistes doit être de l’ordre de $p = ql = 10^{-29} C.m$. C’est pour cette raison que les chimistes utilisent le **debye** (symbole : $D$), bien que cette unité de moment dipolaire appartienne à un système d’unités actuellement abandonné. ==**$1D = \frac{1}{3}.10^{-29} C.m$**==.
# Diagrammes
Doublet de charges
![[electromagnetisme1/attachments-electromagnetisme1/figure54.png]]^figure1

Molécule diatomique
![[electromagnetisme1/attachments-electromagnetisme1/figure55.png]]^figure2

Moments dipolaires des molécules $H_2O$ et $NH_3$
![[electromagnetisme1/attachments-electromagnetisme1/figure56.png]]^figure3

Polarisation d’un atome placé dans un champ $\overrightarrow{E}$ : $\overrightarrow{p} = \alpha\overrightarrow{E}$, avec $\alpha > 0$
![[electromagnetisme1/attachments-electromagnetisme1/figure57.png]]^figure4

Le point $M$ est repéré par son vecteur position $\overrightarrow{r} = \overrightarrow{OM}$ ou par ses coordonnées sphériques : $(r, \theta, \varphi)$
![[electromagnetisme1/attachments-electromagnetisme1/figure58.png]]^figure5

Orientation de $\overrightarrow{E}$ créé un dipôle $\overrightarrow{p}$
![[electromagnetisme1/attachments-electromagnetisme1/figure59.png]]^figure6
# Graphiques
Équipotentielles $\pm V_0$ du dipôle
![[electromagnetisme1/attachments-electromagnetisme1/figure60.png]]^figure7

Équipotentielles d’un doublet ($-q$ , $+q$)
![[electromagnetisme1/attachments-electromagnetisme1/figure61.png]]^figure8

Équipotentielles d’un dipôle
![[electromagnetisme1/attachments-electromagnetisme1/figure62.png]]^figure9

Visualisation du potentiel créé par deux charges $-q$ et $+q$ (en noir $V > 0$, en bleu $V < 0$)
![[electromagnetisme1/attachments-electromagnetisme1/figure63.png]]^figure10

Visualisation du potentiel du dipôle dans l’espace (en noir $V > 0$, en bleu $V < 0$)
![[electromagnetisme1/attachments-electromagnetisme1/figure64.png]]^figure11
# Expériences

# Autres notes
