---
titre: "[[02-Champ électrostatique]]"
tags:
crée: 24-12-2025, 10:58
---
# Formules
> [!note] Loi de Coulomb
> - Force d'interaction entre charges statiques :
> Cette force est répulsive si les charges sont de même signe, attractive sinon.
> ==**La force de Coulomb exercée par la charge $q_1$ sur la charge $q_2$ (les deux charges étant dans le vide) est $\displaystyle \overrightarrow{f}_{1 \rightarrow 2} = \frac{q_1q_2}{4\pi\epsilon_0}\frac{\overrightarrow{e}_{1 \rightarrow 2}}{(M_1M_2)^{2}}$.**==
> $\overrightarrow{e}_{1 \rightarrow 2}$ désigne le vecteur unitaire dirigé de $M_1$ vers $M_2$ ([[#^figure1|fig. 1]]).
> Elle est opposée à la force exercée par $q_2$ sur $q_1$ : $\overrightarrow{f}_{1 \rightarrow 2} = -\overrightarrow{f}_{2 \rightarrow 1}$ ; elle obéit au principe de l'action et de la réaction.
> La constante $\epsilon_0$, permittivité électrique du vide, est voisine de $\displaystyle\frac{1}{36\pi 10^{9}}$ et se mesure en $F\,.\,m^{-1}$, $F$ désignant le farad (unité de capacité).
> La permittivité électrique $\epsilon$ de l'air étant très voisine de $\epsilon_0$ ($\epsilon = \epsilon_0\epsilon_r$, avec $\epsilon_r = 1,\!0006$), la loi de Coulomb reste valable dans l'air.
> - Champ d'une charge ponctuelle :
> La force exercée par $q_1$ sur $q_2$ se met sous la forme : $\displaystyle \overrightarrow{f}_{1 \rightarrow 2} = q_2\overrightarrow{E}_{1}(M_2)$, avec $\displaystyle \overrightarrow{E}_{1}(M_2) = \frac{q_1}{4\pi\epsilon_0}\frac{\overrightarrow{M_1M_2}}{(M_1M_2)^{3}}$.
> $\overrightarrow{E}_{1}(M_2)$ est le champ électrostatique créé par la charge $q_1$ (charge source) au point $M_2$ dans le vide (ou dans l'air).
> Le champ créé par $q_1$ caractérise l'influence de celle-ci sur l'espace qui l'entoure.
> Ainsi, le champ électrostatique créé dans l'espace par une particule de charge $q$, immobile au point origine $O$ du repère de coordonnées sphériques, a pour expression ([[#^figure2|fig. 2]]) : ==**$\displaystyle\overrightarrow{E}(\overrightarrow{r}) = \frac{q}{4\pi\epsilon_0}\frac{\overrightarrow{e}_r}{r^{2}} = \frac{q}{4\pi\epsilon_0}\frac{\overrightarrow{r}}{r^{3}} = \frac{q}{4\pi\epsilon_0}\frac{\overrightarrow{OM}}{OM^{3}}$.**==

> [!note] Champs créés par des distributions de charges ponctuelles
> Utilisant le principe de superposition, nous avons immédiatement :
> ==**Le champ électrostatique $\overrightarrow{E}$ créé en $M$ par diverses charges $q_i$ situées aux points $P_i$ est donné par : $\displaystyle\overrightarrow{E}_{(q_i,\, i\, = \,1,\, \cdots, \,N)}(M) = \frac{1}{4\pi\epsilon_0}\sum_{i=1}^{N}q_i\frac{\overrightarrow{P_iM}}{P_iM^{3}}$.**==

> [!note] Champs créés par des distributions de charges
> Nous appliquerons le principe de superposition à une distribution de charges $\mathcal{D}$ après l'avoir décomposée en un ensemble de fragments élémentaires chargés (mésoscopiques) assimilés à des charges ponctuelles ([[#^figure3|fig. 3]]).
> Notons $P$ un point décrivant l'espace occupé par la distribution. Une partie élémentaire de $\mathcal{D}$, située au voisinage de $P$, contient une charge $dq_P$ et crée un champ élémentaire $d\overrightarrow{E}$ au point d'observation $M$. Nous obtenons le champ total créé en $M$ par la distribution $\mathcal{D}$ par superposition des champs de chacune de ses parties élémentaires selon : ==**$\displaystyle\overrightarrow{E}_{\mathcal{D}}(M) = \frac{1}{4\pi\epsilon_0}\sum_{P \in \mathcal{D}}dq_P\frac{\overrightarrow{e}_{P \rightarrow M}}{PM^{2}} = \frac{1}{4\pi\epsilon_0}\sum_{P \in \mathcal{D}}dq_P\frac{\overrightarrow{PM}}{PM^{3}}$.**==
> On écrira cette expression plus rigoureusement sous la forme : $\displaystyle\overrightarrow{E}_{\mathcal{D}}(M) = \frac{1}{4\pi\epsilon_0}\iiint \limits_{\mathcal{D}}\frac{\overrightarrow{PM}}{PM^{3}}dq_P$.
> Il nous reste à préciser l'élément d'intégration $dq_P$ en fonction de la nature de la distribution considérée.
> - Distribution volumique : ==**$\displaystyle\overrightarrow{E}_{\mathcal{D}}(M) = \frac{1}{4\pi\epsilon_0}\iiint\limits_{\mathcal{D}}\rho(P)\frac{\overrightarrow{PM}}{PM^{3}}d\tau$.**==
> -  Distribution surfacique : ==**$\displaystyle\overrightarrow{E}_{\mathcal{D}}(M) = \frac{1}{4\pi\epsilon_0}\iint\limits_{\mathcal{D}}\sigma(P)\frac{\overrightarrow{PM}}{PM^{3}}dS$.**==
> - Distribution linéique : ==**$\displaystyle\overrightarrow{E}_{\mathcal{D}}(M) = \frac{1}{4\pi\epsilon_0}\int\limits_{\mathcal{D}}\lambda(P)\frac{\overrightarrow{PM}}{PM^{3}}dl$.**==

> [!note] Le champ électrostatique est-il toujours défini ?
> Les expressions précédentes ne sont *a priori* applicables qu'aux cas des distributions d'extension finie (distributions physiques), pour assurer la convergence des intégrales. Il existe toutefois des cas de distributions d'extension infinie pour lesquels ces intégrales convergent.
> Dans le cas d'une distribution volumique de charges $\rho(P)$ finie, d'extension quelconque, l'intégrale dans l'expression de $\overrightarrow{E}(M)$ converge toujours, quelque soit le point $M$.
> Il n'en est plus de même pour les distributions surfaciques et linéiques : le champ $\overrightarrow{E}(M)$ n'est pas défini *sur* ces distributions.
> Prenons l'exemple de l'[[#^app1|Application]] 2 page 21.
> Dans cette application, il est impossible de calculer le champ électrique en un point du segment $AA'$.
> Il en est de même lors d'une distribution surfacique de charges.
> Rappelons que ces modélisations linéiques et surfaciques n'existent que parce que localement la densité volumique de charge $\rho$ est très grande, voire « infinie ».
> C'est le caractère « infini » de $\rho$ qui nous interdit de définir le champ électrostatique en un point d'une distribution linéique ou surfacique.
> ==**Le champ électrostatique en un point des sources n'est pas défini lorsque ces sources sont modélisées par une densité surfacique ou linéique des charges.**==

> [!note] Topographie du champ
> - Lignes de champ :
> ==**Le champ est continuellement tangent à des courbes appelées lignes de champ ([[#^figure4|fig. 4]]). Ces lignes sont orientées par le sens du champ.**==
> La définition des lignes de champ nous permet d'affirmer qu'un élément de longueur $d\overrightarrow{M}$ le long d'une ligne de champ est parallèle au champ $\overrightarrow{E}$. L'équation différentielle (vectorielle) d'une ligne de champ est donc : $d\overrightarrow{M} \wedge \overrightarrow{E} = \overrightarrow{0}$.
> Nous obtiendrons la ligne de champ issue d'un point initial donné par intégration de cette équation différentielle.
> Par exemple, en coordonnées cartésiennes, nous écrirons : $\frac{dx}{E_x} = \frac{dy}{E_y} = \frac{dz}{E_z}$.
> - Tube de champ :
> ==**L'ensemble des lignes de champ s'appuyant sur une courbe fermée (ou contour) $C$  engendre une surface appelée tube de champ, représentée sur la [[#^figure5|figure 5]].**==
> - Points de champ nul, points singuliers :
> *Deux lignes de champ ne se coupent pas en un point $M$ où le champ électrostatique est défini et non nul* ([[#^figure6|fig. 6]]) ; sinon la direction du champ, donc le champ lui-même, ne serait pas défini en ce point.
> Deux lignes de champ peuvent se couper en $M$ si :
> 	- le champ est nul au point $M$ : $M$ est appelé *point de champ nul* (ou *point d'arrêt*) ;
> 	- le champ n'est pas défini au point $M$ : il y a une charge ponctuelle en $M$, ou bien $M$ appartient à une surface ou à une ligne chargée.
> 
> 	Quelques lignes de champ d'un système de deux charges ponctuelles $q$ et $Q$ sont représentées sur les figures [[#^figure7|7a]] (cas $Q = 2q > 0$) et [[#^figure7|7b]] (cas $Q = -2q < 0$).
> 	Nous pouvons observer que les lignes de champ divergent à partir des charges positives, convergent vers les charges négatives, ou « aboutissent » à l'infini. Elles se coupent au niveau des charges ainsi qu'aux points de champ nul $A$ et $A'$.
# Définitions
==**Principe de superposition**== :
L'expérience conduit à postuler que les interactions électrostatiques ont des effets linéaires.
Par exemple, la force subie par une charge $q$ de la part d'un ensemble de $N$ charges $q_1, q_2, \cdots, q_N$ est la somme des $N$ forces qu'exercent individuellement les charges $q_i\,(i = 1, \cdots, N)$ lorsqu'elles sont mises seules en présence de la charge $q$. Le champ créé par les $N$ charges est donc la somme des $N$ champs créés par chaque charge.
Nous postulons donc la *linéarité des effets*, ce qui constitue **le principe de superposition**.

==**Utilisation des symétries et antisymétries**== :
Le calcul du champ à partir des intégrales est souvent assez pénible. Il convient alors d'utiliser les symétries des distributions, quand elles existent, pour le simplifier.
Certaines simplifications (éliminations de certaines coordonnées du point de calcul $M$, annulation de composantes du champ...) peuvent alors être effectuées sans aucun calcul, à l'aide de considérations de symétries  ; c'est pourquoi nous étudions ici les propriétés de symétrie et d'antisymétrie du champ électrostatique.

> [!note] Propriétés de symétries du champ : Symétries élémentaires
> - Symétrie plane :
> ==**Sur un plan-miroir $\Pi$ d'une distribution de charge $\mathcal{D}$, le champ électrostatique créé est parallèle au plan $\Pi$ ([[#^figure8|fig. 8]]).**==
> ==**Aux points $M$ et $M'$ symétriques par rapport à un plan-miroir $\Pi$ d'une distribution de charges $\mathcal{D}$, les champs électrostatiques $\overrightarrow{E}$ et $\overrightarrow{E'}$ sont symétriques l'un de l'autre ([[#^figure9|fig. 9]]).**==
> Exemple de plan-miroir $\Pi$ :
> Sur la [[#^figure11a|figure 11a]], quatre charges ponctuelles sont placées dans le plan $(xOy)$ $-q$ en $(2, 2)$ et $(-2, 2)$, $2q$ en $(1, -1)$ et $(-1, -1)$. Le plan $(yOz)$ est plan-miroir de cette distribution. Quelques lignes de champ ont été tracées sur le plan $(xOy)$.
> Nous constatons que les lignes de champ qui approchent le plan $(yOz)$ lui sont en général tangentes : sur le plan-miroir, le champ électrostatique est tangent au plan. Notons qu'au point $A$, où se coupent quatre lignes de champ perpendiculaires, deux de ces lignes sont perpendiculaires au plan-miroir. Ceci ne contredit pas l'appartenance du champ à ce plan, car le point $A$ est un point de champ nul. Le point $A'$ est un autre point de champ nul.
> Comme nous l'avons vu précédemment, en deux points $M$ et $M'$ symétriques par rapport au plan $(yOz)$, les champs électrostatiques $\overrightarrow{E}$ et $\overrightarrow{E'}$ sont symétriques.
> - Antisymétrie plane :
> ==**Sur un plan-antimiroir $\Pi^{*}$ d'une distribution $\mathcal{D}$, le champ électrostatique créé est perpendiculaire au plan $\Pi^{*}$ ([[#^figure10|fig. 10a et b]]).**==
> ==**Au point $M'$ symétrique du point $M$ par rapport au plan-antimiroir $\Pi^{*}$ d'une distribution de charges $\mathcal{D}$, le champ électrostatique $\overrightarrow{E'}$ est l'opposé du symétrique du champ $\overrightarrow{E}$ créé par la distribution en $M$ ([[#^figure10|fig. 10c]]).**==
> Exemple de plan-antimiroir $\Pi^{*}$ :
> Sur la [[#^figure11b|figure 11b]], quatre charges ponctuelles sont placées dans le plan $(xOy)$ : $q$ en $(2, 2)$, $-q$ en $(-2, 2)$, $-2q$ en $(1, -1)$ et $2q$ en $(-1, -1)$. Le plan $(yOz)$ est plan-antimiroir de cette distribution. Quelques lignes de champ ont été tracées sur le plan $(xOy)$.
> Les lignes de champ coupent le plan $(yOz)$ perpendiculairement : sur le plan antimiroir, le champ électrostatique est orthogonal au plan.
> Notons qu'au point $A$ se coupent quatre lignes de champ non perpendiculaires à $(yOz)$. Le point $A$ est un point de champ nul, et le caractère orthogonal à $(yOz)$ du champ n'est pas mis en défaut.
> Plus généralement, au point $M'$ symétrique de $M$ par rapport au plan $(yOz)$, le champ électrostatique $\overrightarrow{E'}$ est l'opposé du symétrique du champ $\overrightarrow{E}$ en $M$.

> [!note] Propriétés de symétries du champ : Symétries élémentaires : Invariance par translation ou par rotation
> Lorsqu'une distribution $\mathcal{D}$ est invariante par une translation de $\Delta z$ parallèlement à l'axe $(Oz)$, un observateur percevra la même distribution s'il est au point de coordonnées cartésiennes $(x, y, z)$ ou en un point translaté du précédent de coordonnées $(x, y, z + n\Delta z)$, où $n$ est un entier. Le champ sera donc identique en ces deux points ([[#^figure12|fig. 12]]).
> Considérons maintenant une distribution $\mathcal{D}$ invariante par une rotation $\mathcal{R}$ d'angle $\alpha = \frac{2\pi}{n}$ (n entier) autour de l'axe $(Oz)$. Deux observateurs placés aux points $M$ et $M' = \mathcal{R}(M)$ percevront la même distribution (la [[#^figure13|figure 13]] a été tracé avec $n = 6$).
> Les champs électrostatiques détectés aux points $M$ et $M'$ ont les mêmes composantes dans les systèmes de coordonnées $(Ox, Oy, Oz)$ et $(\mathcal{R}(Ox), \mathcal{R}(Oy), \mathcal{R}(Oz))$ respectivement.
> Le champ au point $M'$ est ainsi le même qu'au point $M$, à une rotation d'angle $\alpha$ autour du vecteur $\overrightarrow{e}_z$ près.

> [!note] Propriétés de symétries du champ : Symétries élémentaires : Le champ électrostatique est un vecteur polaire
> Les études précédentes nous amènent à une conclusion simple : lors d'[[#^def1|opérations de symétrie]] (symétrie plane, translation, rotation autour d'un axe) appliquées à la distribution de charges $\mathcal{D}$, le champ électrostatique subit la même opération.
> Nous appelons *vecteur polaire* un vecteur dont le champ a les mêmes propriétés de symétrie que ses sources.
> Pour qualifier cette propriété, nous trouvons aussi le terme « *vrai vecteur* », par opposition à « *pseudo-vecteur* ».
> Nous reviendrons sur cette distinction lors de l'étude du champ magnétique.
> ==**Le champ électrostatique est un objet tridimensionnel ayant les propriétés de symétrie d'un *vecteur polaire* ou « *vecteur vrai* ».**==
> ==**Cela signifie qu'il a les mêmes propriétés de symétrie que la distribution des charges qui le créent.**==

> [!note] Propriétés de symétries du champ : Symétries multiples
> Ces cas correspondent à l'existence de plusieurs symétries élémentaires. Les cas de distributions invariantes par translation parallèlement à un axe ou de révolution autour d'un axe en font partie.
> Citons encore deux cas de symétrie élevée que nous traiterons comme application directe de l'utilisation des propriétés de symétrie élémentaires :
> - le champ d'une *distribution à symétrie cylindrique d'axe* $(Oz)$ (la répartition de charges n'est fonction que de la distance à l'axe $(Oz)$) est, en coordonnées cylindriques, de la forme $\overrightarrow{E}(r, \theta, z) = E(r)\overrightarrow{e}_r$  ;
> - le champ d'une *distribution à symétrie sphérique de centre* $O$ est, en coordonnées sphériques, de la forme $\overrightarrow{E}(r, \theta, \varphi) = E(r)\overrightarrow{e}_r$.

> [!note] Propriétés de symétries du champ : Discontinuités du champ à la traversée d'une distribution surfacique
> Nous avons déjà signalé que le champ électrostatique n'était pas défini sur les distributions surfaciques. En outre, *à la traversée d'une surface électrisée, de la face ➀ vers la face ➁, la composante normale du champ subit une discontinuité et la composante tangentielle est conservée ([[#^figure14|fig. 14]])*.
> Nous admettrons les résultats mis en évidence dans l'[[#^app2|Application]] 8 page 30 : $\displaystyle \overrightarrow{E}_{2\perp} - \overrightarrow{E}_{1\perp} = \frac{\sigma}{\epsilon_0}\overrightarrow{n}_{12}$ et $\overrightarrow{E}_{1\parallel} = \overrightarrow{E}_{2\parallel}$ ou encore $\displaystyle \overrightarrow{E}_{2} - \overrightarrow{E}_{1} = \frac{\sigma}{\epsilon_0}\overrightarrow{n}_{12}$.
# Diagrammes
Forces d'interaction électrostatique entre deux charges statiques $(q_1q_2 > 0)$
![[electromagnetisme1/attachments-electromagnetisme1/figure9.png]]^figure1

Champ d'une charge ponctuelle $(q > 0)$
![[electromagnetisme1/attachments-electromagnetisme1/figure10.png]]^figure2

Distribution de charges $\mathcal{D}$
![[electromagnetisme1/attachments-electromagnetisme1/figure11.png]]^figure3

Ligne de champ
![[electromagnetisme1/attachments-electromagnetisme1/figure13.png]]^figure4

Tube de champ
![[electromagnetisme1/attachments-electromagnetisme1/figure14.png]]^figure5

En $M$, le champ $\overrightarrow{E}$ est soit nul soit non défini
![[electromagnetisme1/attachments-electromagnetisme1/figure15.png]]^figure6

Symétrie plane. a. Contributions élémentaires de $P$ et $P'$. b. Champ total sur le plan-miroir
![[electromagnetisme1/attachments-electromagnetisme1/figure17.png]]^figure8

Symétrie plane et champ électrostatique
![[electromagnetisme1/attachments-electromagnetisme1/figure18.png]]^figure9

Antisymétrie plane
![[electromagnetisme1/attachments-electromagnetisme1/figure19.png]]^figure10

Distribution invariante par translation
![[electromagnetisme1/attachments-electromagnetisme1/figure22.png]]^figure12

Distribution invariante par rotation
![[electromagnetisme1/attachments-electromagnetisme1/figure23.png]]^figure13
# Graphiques
Lignes de champ d'un système de deux charges ponctuelles $q$ et $Q$. a. $Q = 2q$. b. $Q = -2q$
![[electromagnetisme1/attachments-electromagnetisme1/figure16.png]]^figure7

Symétrie des champs électrostatiques $\overrightarrow{E}$ et $\overrightarrow{E'}$ par rapport au plan de symétrie $\Pi = (y, O, z)$
![[electromagnetisme1/attachments-electromagnetisme1/figure20.png]]^figure11a

Le champ électrostatique $\overrightarrow{E'}$ est l'opposé du symétrique de $\overrightarrow{E}$ par rapport au plan d'antisymétrie $\Pi^{*} = (y, O, z)$
![[electromagnetisme1/attachments-electromagnetisme1/figure21.png]]^figure11b

Discontinuités du champ à la traversée d'une distribution surfacique
![[electromagnetisme1/attachments-electromagnetisme1/figure26.png]]^figure14
# Expériences

# Autres notes
> [!warning] Application 2 page 21
> ![[electromagnetisme1/attachments-electromagnetisme1/figure12.png]]
^app1

> [!warning] Application 5 page 27
> ![[electromagnetisme1/attachments-electromagnetisme1/figure24.png]]

> [!warning] Application 6 page 28
> ![[electromagnetisme1/attachments-electromagnetisme1/figure25.png]]

> [!warning] Opération de symétrie
> Le terme « opération de symétrie » désigne ici une **isométrie**, c'est-à-dire un déplacement qui laisse inchangées les distances.
^def1

> [!warning] Application 8 page 30
> ![[electromagnetisme1/attachments-electromagnetisme1/figure27.png]] 
^app2