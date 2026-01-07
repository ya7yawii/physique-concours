---
titre: "[[07-Champ magnétique]]"
tags:
aliases:
crée: 06-01-2026, 13:08
---
# Formules
> [!note] Force de Lorentz et champ magnétique
> - Force de Lorentz :
> Nous savons qu’un aimant ou une bobine de spires conductrices parcourues par un courant électrique sont sources de champs magnétiques $\overrightarrow{B}$. Ces champs se manifestent par la force de Lorentz que subit une particule mobile de charge $q$ et de vitesse $\overrightarrow{v}$ : $\overrightarrow{F} = q\overrightarrow{v} \wedge \overrightarrow{B}$, ou par la force de Laplace que subit un élément $d\overrightarrow{l}$ de circuit parcouru par un courant d’intensité $I$ : $d\overrightarrow{F} = Id\overrightarrow{l} \wedge \overrightarrow{B}$.
> Nous n’étudierons dans ce cours que le champ magnétique créé par des courants.
> *Remarque : Rappelons qu’il existe un champ magnétique terrestre (cf. chapitre 9) dont la composante horizontale, en France, est de l’ordre de $2\,.10^{-5}$ tesla.*
> - [[#^app1|Cadre d’étude]] :
> Les lois à venir sont rigoureusement valables dans le cas de la magnétostatique, c’est-à-dire pour des régimes indépendants du temps (courants constants, pas d’accumulation de charges). Nous emploierons souvent l’expression « champ magnétique » au sens de « champ magnétostatique » par la suite.
> Ces lois sont encore applicables à des dispositifs expérimentaux de dimension caractéristique $L$, dans le cas des régimes variables de temps caractéristique $T$, tant que $L \ll cT$ où $c$ est la vitesse de la lumière dans le vide.
> - Mesure du champ :
> *La force de Laplace*, subie par un élément $d\overrightarrow{l}$ de circuit parcouru par un courant d’intensité $i$ : $d\overrightarrow{F} = Id\overrightarrow{l} \wedge \overrightarrow{B}$, est mesurable.
> Le champ magnétique $\overrightarrow{B}$ appliqué à un circuit parcouru par un courant $i$ peut donc être mesuré à partir de la mesure de la force $\overrightarrow{F}$ subie par celui-ci ([[#^figure1|fig. 1]]).
> En fait une sonde à effet Hall, moins encombrante et plus précise, sera généralement préférée pour la mesure des champs magnétiques.

> [!note] Loi de Biot et Savart : Vecteur élément de courant
> - Considérons un circuit filiforme parcouru par un courant d’intensité $I$ et notons $d\overrightarrow{l}$ un déplacement élémentaire le long de ce circuit, dans le sens que du courant ([[#^figure2|fig. 2]]).
> Par définition, on appelle *élément de courant* le vecteur polaire : $d\overrightarrow{C} = Id\overrightarrow{l}$.
> La norme d’un élément de courant s’évalue en A.m.
> - Lorsque la section du circuit n’est plus petite à l’échelle macroscopique, il est pertinent, sinon indispensable, de s’interroger sur la répartition du courant dans le circuit. Pour cela nous serons obligés d’introduire une modélisation continue. Nous analyserons alors le circuit comme un ensemble de tubes de courants mésoscopiques, filiformes, jointifs, d’intensité $dI$, placés à l’intérieur de la surface externe du circuit ([[#^figure3a|fig. 3a]]). À un élément de longueur $d\overrightarrow{l}$ d’un tube de courant mésoscopique, sera associé le vecteur de courant : $d\overrightarrow{C} = dI\,d\overrightarrow{l}$. Notons $s$ la section de ce tube de courant et $\overrightarrow{j}$ le vecteur densité volumique de courant à travers la section considérée, il vient : $d\overrightarrow{C} = dI\,d\overrightarrow{l} = jsd\overrightarrow{l} = \overrightarrow{j}d\tau$ puisque $\overrightarrow{j}$ et $d\overrightarrow{l}$ sont colinéaires et de même sens.
> *Une distribution volumique de courants peut s’analyser en une distribution continue de courants filiformes mésoscopiques.*
> Cette équivalence est fréquemment utilisée. En effet, dans la pratique, nombre de circuits filiformes se présentent sous la forme de bobinages multicouches avec des spires jointives de faible section. La structure d’une telle bobine, avec ses spires filiformes, rappelle en tous points celle du courant précédent lorsqu’il est analysé en tubes de courant mésoscopiques. Pour calculer les champs créés par de tels circuits, il sera alors très commode d’avoir recours à une modélisation volumique, continue, nivelant le caractère discret du bobinage.
> - Une démarche analogue peut être adoptée pour une distribution de courants surfaciques. Tout courant surfacique peut être analysé comme une distribution continue de rubans mésoscopiques, filiformes, jointifs, d’intensité $dI$ ([[#^figure3b|fig. 3b]]). À un élément de longueur $d\overrightarrow{l}$ d’un ruban de courant mésoscopique, sera associé le vecteur de courant : $d\overrightarrow{C} = dI\,d\overrightarrow{l}$. Notons $a$ la section d’un ruban de courant et $j_s$ le vecteur densité surfacique de courant à travers la section considérée, il vient : $d\overrightarrow{C} = dI\,d\overrightarrow{l} = j_s\,a\,d\overrightarrow{l} = \overrightarrow{j_s}dS$ puisque $\overrightarrow{j_s}$ et $d\overrightarrow{l}$ sont colinéaires et de même sens.
> Cette équivalence pourra être utilement exploitée quand il s’agira, par exemple, de calculer le champ créé par une bobine monocouche à spires jointives de faible section.
> *Une distribution surfacique de courant peut s’analyser en une distribution continue de courants filiformes mésoscopiques.*
> - En conclusion, nous retiendrons que :
> ==**Toute distribution de courants peut s’analyser comme une distribution de courants filiformes dont la caractéristique locale est l’élément de courant $d\overrightarrow{C}$.**==
> 
> Par la suite, cette analyse ne sera pas toujours explicitement faite sur les distributions de courants étudiés, mais il ne tient qu’au lecteur de s’en convaincre en l’effectuant.

> [!note] Loi de Biot et Savart : Champ attribué à un élément de courant
> Alors que les charges sont les sources du champ électrostatique, les éléments de courant sont les sources du champ magnétique.
> ==**Nous *postulons* que l’expression de la contribution d’un élément de courant $d\overrightarrow{C}$, situé au point $P$, au champ total $\overrightarrow{B}(M)$ créé en $M$ par une distribution de courants est donnée par la loi de Biot et Savart : $\displaystyle d\overrightarrow{B}(M) = \frac{\mu_0}{4\pi} d\overrightarrow{C}\wedge\frac{\overrightarrow{e}_{P\rightarrow M}}{\left\Vert PM \right\Vert^{2}} = \frac{\mu_0}{4\pi}d\overrightarrow{C}\wedge\frac{\overrightarrow{PM}}{\left\Vert PM \right\Vert^{3}}$.**==
> ==**Le champ $\overrightarrow{B}(M)$ étant la somme des contributions élémentaires, avec $d\overrightarrow{C} = \overrightarrow{j}d\tau$ ou $d\overrightarrow{C} = \overrightarrow{j}_SdS$ ou $d\overrightarrow{C} = I\,d\overrightarrow{l}$ selon les cas.**==
> Comme il est impossible d’isoler un élément de courant, nous ne pouvons pas vérifier directement ce postulat : la seule grandeur ayant une signification physique (en tant que grandeur mesurable) est le champ résultant $\overrightarrow{B}$ créé par toute la distribution de courants $\mathcal{D}$.
> ==**Le coefficient $\mu_0$, dimensionné, vaut exactement $\mu_0 = 4\pi\, . 10^{-7}\, H\, . m^{-1}$ ($H$ désigne le henry, unité d’inductance).**==
> ==**L’unité de champ magnétique est le tesla (symbole : $T$).**==
> - Nous pouvons aussi attribuer un élément de courant à chaque particule chargée en mouvement. Imaginons que sur une longueur $\delta l$ d’un fil conducteur, il y ait $N$ particules mobiles de charge $q$ et de vitesse $v$. Ces $N$ particules traversent une section du fil pendant la durée $\delta t = \frac{\delta l}{v}$, d’où la valeur de l’intensité : $I = \frac{Nqv}{\delta l}$ et donc pour l’élément de fil : $\delta \overrightarrow{C} = N q \overrightarrow{v}$.
> Nous pouvons associer à chaque particule en mouvement un élément de courant : $\overrightarrow{C} = q \overrightarrow{v}$.

> [!note] Loi de Biot et Savart : Expression du champ magnétique par la loi de Biot et Savart
> La loi Biot et Savart postule que le champ créé en un point $M$ par une distribution $\mathcal{D}$ ([[#^figure4|fig. 4]]) s’obtient par superposition des contributions élémentaires $d\overrightarrow{B}$ des éléments de courant de la distribution : $\displaystyle\overrightarrow{B}(M) = \int_{\mathcal{D}}\frac{\mu_0}{4\pi}d\overrightarrow{C}\wedge\frac{\overrightarrow{e}_{P\rightarrow M}}{\left\Vert PM \right\Vert^{2}}$.
> Suivant le type de distribution, nous écrirons ce champ sous l’une des formes suivantes.
> - Distribution volumique : ==**$\displaystyle\overrightarrow{B}(M) = \frac{\mu_0}{4\pi}\iiint_{\mathcal{D}}\overrightarrow{j}(P)d\tau\wedge\frac{\overrightarrow{e}_{P\rightarrow M}}{PM^{2}}$**==.
> - Distribution surfacique : ==**$\displaystyle\overrightarrow{B}(M) = \frac{\mu_0}{4\pi}\iint_{\mathcal{D}}\overrightarrow{j}_S(P)dS\wedge\frac{\overrightarrow{e}_{P\rightarrow M}}{PM^{2}}$**==.
> - Distribution filiforme : ==**$\displaystyle\overrightarrow{B}(M) = \frac{\mu_0}{4\pi}\int_{\mathcal{D}}Id\overrightarrow{P}\wedge\frac{\overrightarrow{e}_{P\rightarrow M}}{PM^{2}}$**==.
> Le régime permanent imposant au courant d’être « bouclé sur lui-même », cette dernière distribution a la forme d’un contour $C$, et nous pourrons aussi écrire : $\displaystyle\overrightarrow{B}(M) = \frac{\mu_0}{4\pi}\oint_{C}Id\overrightarrow{P}\wedge\frac{\overrightarrow{e}_{P\rightarrow M}}{PM^{2}}$.
> 
> *Remarques :*
> - *L’analogie de ces expressions avec celles donnant le champ électrostatique d’une distribution est remarquable : il suffit de transposer $\frac{1}{4\pi\epsilon_0}$ en $\frac{\mu_0}{4\pi}$ et $[dq_P]$ en $[d\overrightarrow{C}\,\wedge]$ dans les expressions donnant le champ. Les champs électrostatique et magnétique sont deux facettes d’un même objet, le champ électromagnétique.*
> - *Pour une distribution volumique de courants, l’intégrale de Biot et Savart permet le calcul du champ magnétique en tout point de l’espace.*
> - *Dans le cas d’une distribution surfacique, cette intégrale n’autorise pas le calcul du champ sur la nappe de courant. (Nous verrons qu’il existe une discontinuité finie de la composante tangentielle de $\overrightarrow{B}$ à la traversée de cette surface.)*
> - *Pour une schématisation filiforme, il est exclu de calculer le champ magnétique en un point du circuit : l’intégrale y est alors divergente.*

> [!note] Topographie du champ
> - Lignes de champ :
> 	- Définition :
> 	Le champ est continuellement tangent à des courbes appelées *lignes de champ* ([[#^figure5|fig. 5]]). Ces lignes sont orientées dans le sens du champ.
> 	- Équation d’une ligne de champ :
> 	Un déplacement élémentaire $d\overrightarrow{M}$ le long d’une ligne de champ est parallèle au champ $\overrightarrow{B}$. L’équation différentielle (vectorielle) d’une ligne de champ est : $d\overrightarrow{M}\wedge\overrightarrow{B} = \overrightarrow{0}$.
> 	Nous obtiendrons la ligne de champ issue d’un point initial donné par intégration de cette équation différentielle.
> - Visualisation d’une ligne de champ :
> 	- Expérimentalement :
> 	Il est possible de visualiser les lignes de champ d’un système de courants (ou d’aimants) en procédant de la manière suivante.
> 	Sur une plaque de verre ou de plexiglas, située dans la zone utile du champ magnétique, on saupoudre de la limaille de fer. Les grains de limaille (de forme allongée) sous l’action du champ magnétique se transforment en petits aimants (ou petites boussoles) qui s’orientent alors parallèlement à ce champ magnétique.
> 	Ces petits aimants s’alignant les uns derrière les autres concrétisent approximativement une ligne de champ ([[#^figure6|fig. 6]]). On obtient ainsi les spectres magnétiques des figures [[#^figure7|7]] et [[#^figure8|8]].
> 	- Par simulation :
> 	Lors d’un tracé de ligne de champ par simulation ([[#^figure9|fig. 9]]), l’équation différentielle $d\overrightarrow{M}\wedge\overrightarrow{B} = \overrightarrow{0}$ est résolue en partant d’un point donné de l’espace.
> - Tube de champ :
> L’ensemble des lignes de champ s’appuyant sur une courbe fermée (ou contour) $C$ engendre une surface $S$ appelée *tube de champ*, représenté sur la [[#^figure10|figure 10]].
> - Points de champ nul, points singuliers :
> Deux lignes de champ ne peuvent pas se couper, comme le suggère la [[#^figure11|figure 11]], en un point $M$ où le champ magnétique est défini et non nul. La direction du champ, donc le champ lui-même, ne serait pas définie en ce point.
> Si le champ est nul au point $M$, alors $M$ est appelé *point de champ nul* (ou point d’arrêt).

> [!note] Propriétés de symétrie du champ magnétique
> Comme en électrostatique, le calcul de la valeur du champ à partir des intégrales est souvent pénible ; nous rencontrerons des situations où la distribution de charges possède des symétries remarquables, qui peuvent simplifier considérablement la détermination du champ.
> - Symétrie plane :
> Supposons la distribution $\mathcal{D}$ invariante par une symétrie plane $\mathcal{S}$ par rapport à un plan $\Pi$.
> Plaçons-nous en un point $M$ du plan de symétrie. Considérons les contributions élémentaires $d\overrightarrow{B}_P(M)$ et $d\overrightarrow{B}_{P'}(M)$ au champ total des deux éléments de courants $d\overrightarrow{C}$ et $d\overrightarrow{C'}$ associés aux points $P$ et $P'$ symétriques l’un de l’autre par rapport à $\Pi$. La [[#^figure12|figure 12]] fait apparaître les différentes orientations de $d\overrightarrow{C}$ et $d\overrightarrow{C'}$ envisageables, et montre que $d\overrightarrow{B} + d\overrightarrow{B'}$ est perpendiculaire au plan $\Pi$.
> Nous pouvons ainsi conclure ([[#^figure13a|fig. 13 a]]) :
> ==**Le champ magnétique $\overrightarrow{B}$ est perpendiculaire à un plan-miroir $\Pi$ en chacun de ses points.**==
> Plus généralement, nous aurons ([[#^figure13b|fig. 13 b]]) :
> ==**Au point $M'$ symétrique d’un point $M$ par rapport à un plan-miroir $\Pi$, le champ magnétique $\overrightarrow{B'}$ est *l’opposé du symétrique* du champ $\overrightarrow{B}$ en $M$ par rapport à ce plan.**==
> 
> Remarque :
> Nous laissons le soin au lecteur de s’en convaincre en utilisant une méthode analogue à celle qui a été utilisée à ce propos pour le champ électrostatique au [[02-Champ électrostatique|chapitre 2]], ce qui est un peu fastidieux, et proposons au lecteur [[#^app2|l’application qui suit]] pour se convaincre des propriétés particulières de symétrie du produit vectoriel de deux vecteurs.

> [!note] Propriétés de symétrie du champ magnétique : Antisymétrie plane
> Pour une distribution $\mathcal{D}$ possédant un plan d’antisymétrie $\Pi^{*}$, et pour un point $M$ appartenant à ce plan, il suffit de changer le sens du champ élémentaire $d\overrightarrow{B}_{P'}$ dans les raisonnements précédents. Par conséquent ([[#^figure14a|fig. 14 a]]) :
> ==**Le champ magnétique $\overrightarrow{B}$ est contenu dans un plan-antimiroir $\Pi^{*}$ en chacun de ses points.**==
> Plus généralement ([[#^figure14b|fig. 14 b]]) :
> ==**Au point $M'$ symétrique du point $M$ par rapport au plan-antimiroir $\Pi^{*}$, le champ magnétique $\overrightarrow{B'}$ est le symétrique du champ $\overrightarrow{B}$ en $M$.**==
> 
> *Exemple : Considérons une spire circulaire d’axe $(Oz)$ parcourue par un courant $I$. Les lignes de champ seront dans des plans contenant l’axe $(Oz)$ qui sont des plans-antimiroirs de cette distribution. Nous choisirons donc le plan $(xOz)$ pour représenter quelques lignes du champ magnétique de la spire ([[#^figure9|fig. 9]]), dont nous pouvons ainsi illustrer les propriétés lors d’opérations de symétrie plane.*
> - *Les plans contenant l’axe $(Oz)$ de la spire sont des plans-antimiroirs.*
> *Sur l’axe $(Oz)$, le champ magnétique est parallèle à $\overrightarrow{e}_z$. Cette observation est en accord avec la valeur $\overrightarrow{B}(M) = \frac{\mu_0I}{2R}\sin^{3}\alpha\,.\overrightarrow{e}_z$ (1) que nous avons déjà calculée (cf. [[#^app3|Application 3]]).*
> *Au point $M'(x, 0, z)$ symétrique du point $M(-x, y, z)$ par rapport au plan-antimiroir $(yOz)$, le champ magnétique $\overrightarrow{B'}$ est le symétrique du champ $\overrightarrow{B}$ par rapport à ce plan.*
> - *Le plan $(xOy)$ de la spire est un plan-miroir.*
> *Sur la [[#^figure9|figure 9]], les lignes de champ coupent l’axe $(Ox)$ perpendiculairement. Le champ est identique aux points $A(0, 0, z_0)$ et $A'(0, 0, -z_0)$ (ce qui revient à changer $\alpha$ en $\pi - \alpha$ a dans l’expression (1)).*
> *Au point $M''(x, 0, -z)$ symétrique du point $M(x, 0, z)$, le champ $\overrightarrow{B''}$ est l’opposé du symétrique de $\overrightarrow{B}$ par rapport à $(xOy)$.*

> [!note] Propriétés de symétrie du champ magnétique
> - Invariance par translation :
> Lorsqu’une distribution $\mathcal{D}$ est invariante par une translation de $\Delta z$ parallèlement à l’axe $(Oz)$, un observateur percevra la même distribution s’il est au point de coordonnées cartésiennes $(x, y, z)$ ou en un point translaté du précédent de coordonnées $(x, y, z + n\Delta z)$, où $n$ est un entier. Le champ sera donc identique en ces deux points ([[#^figure15|fig. 15]]) : $\overrightarrow{B}(x, y, z + n\Delta z) = \overrightarrow{B}(x, y, z)$. Ce n’est possible que pour les distributions illimitées dans la direction de la translation.
> Pour une distribution invariante par (toute) translation selon la direction de l’axe $(Oz)$, le champ magnétique sera de la forme $\overrightarrow{B}(x, y, z) = \overrightarrow{B}(x, y)$.
> - Invariance par rotation :
> Pour une distribution $\mathcal{D}$ invariante par une rotation $\mathcal{R}$ d’angle $\alpha = \frac{2\pi}{n}$ ($n$ entier) autour de l’axe $(Oz)$, deux observateurs placés en $M$ et $M' = \mathcal{R}(M)$ percevront la même distribution ([[#^figure16|fig. 16]]).
> Le champ au point $M'$ est le même qu’au point $M$, à une rotation autour de $\overrightarrow{e}_z$ d’angle $\alpha$ près.
> *Remarque : Ce résultat est à rapprocher de l’étude faite dans l’[[#^app2|Application 4]], une rotation conserve le produit vectoriel.*

> [!note] Propriétés de symétrie du champ magnétique : Le champ magnétique est un vecteur axial
> Les études précédentes nous amènent à une conclusion simple : *lors d’une symétrie plane appliquée à la distribution de courants $\mathcal{D}$, le champ magnétique subit la même symétrie avec en plus un changement de signe.*
> Les opérations de symétrie, telles qu’une rotation autour d’un axe ou une translation, peuvent être vues comme le produit de deux symétries planes, ce qui a pour effet de supprimer le changement de signe.
> Nous appelons **vecteur axial** un vecteur dont le champ a cette propriété.
> Le vecteur champ magnétique est un vecteur axial à cause du produit vectoriel que l’on trouve dans l’expression de la loi de Biot et Savart. Il est facile de vérifier (cf. [[#^app2|Application 4]]) que, pour une symétrie par rapport à un plan $\Pi$ : $S(\overrightarrow{u}\wedge\overrightarrow{v}) = -S(\overrightarrow{u})\wedge S(\overrightarrow{v})$.
> *Pour qualifier cette propriété, nous trouvons aussi le terme « **pseudo-vecteur** », par opposition à un « vecteur-vrai » qui, comme le champ électrique, a les mêmes propriétés de symétrie que ses sources.*
> ==**Le champ magnétostatique est un objet tridimensionnel qui a les propriétés de symétrie d’un *vecteur axial* ou « *pseudo-vecteur* ».**==
> ==**Cela signifie que si les courants qui le créent subissent une symétrie plane par rapport à un plan, alors $\overrightarrow{B}$ subit une antisymétrie par rapport au même plan.**==

> [!note] Flux du champ magnétique : Le flux magnétique est conservatif : Flux du champ attribué à un élément de courant
> Envisageons un élément de courant $d\overrightarrow{C} = dC\,.\overrightarrow{e}_z$. Au point $M$ de coordonnées cylindriques $(r, \theta , z)$, le champ attribué à cet élément vaut : $d\overrightarrow{B}(M) = \frac{\mu_0\,dC}{4\pi}\overrightarrow{e}_z\wedge\frac{\overrightarrow{OM}}{\left\Vert OM \right\Vert^{3}} = \frac{\mu_0\,dC}{4\pi}\frac{\sin\alpha}{[r^{2} + z^{2}]^{2}}\overrightarrow{e}_{\theta}$.
> Les lignes de ce champ élémentaire sont des cercles centrés sur l’axe $(Oz)$. L’invariance par rotation autour de cet axe assure que $d\overrightarrow{B}\,.\overrightarrow{e}_{\theta}$ reste constant sur un tel cercle.
> Le tube de champ correspondant aux lignes s’appuyant sur une section droite d’aire $dS_{\theta}$ est un tore. Le flux du champ élémentaire $d\overrightarrow{B}$ est le même à travers toutes les sections de ce tore et vaut $(d\overrightarrow{B}\,.\overrightarrow{e}_{\theta})\,dS_{\theta}$.
> Observons sur la [[#^figure17|figure 17]] les lignes du champ $d\overrightarrow{B}$ traversant une surface fermée $S$. Un tube torique de champ découpe sur $S$ un nombre pair de sections (dans le cas simple représenté ce nombre est deux). Les contributions des flux « entrant dans $S$ » et « sortant de $S$ » sont identiques, au signe près.
> *Le flux du champ magnétostatique $d\overrightarrow{B}$ à travers une surface fermée $S$ est nul.*

> [!note] Flux du champ magnétique : Le flux magnétique est conservatif : Généralisation
> Pour une distribution de courants $\mathcal{D}$, le champ magnétique $\overrightarrow{B}$ en $M$ résulte de la superposition de champs élémentaires $d\overrightarrow{B}$, d’après la loi de Biot et Savart.
> La propriété précédente sera ainsi valable pour le champ total créé par la distribution. Nous pouvons donc affirmer que :
> ==**Le flux du champ magnétique sortant d’une surface fermée est nul.**==
> Rappelons que cela implique que le flux du champ magnétique est le même à travers toute section d’un même tube de champ ([[#^figure18|fig. 18]]) :
> ==**Le champ magnétique est à flux conservatif.**==
> Nous verrons ultérieurement que cette propriété reste valable, que le régime étudié soit indépendant du temps ou variable.
> *Remarque :*
> *Nous avons vu que les lignes du champ magnétique attribuées à un élément de courant sont des cercles, elles sont donc fermées. Il en est de même pour un fil rectiligne infini, ou pour une spire circulaire (cf. [[#^figure9|fig. 9]]). Nous pourrons admettre la généralisation de cette propriété à des champs magnétiques créés par des distributions quelconques. Ce comportement différencie encore fondamentalement un champ magnétostatique d’un champ électrostatique. Cette propriété est liée au fait que $\overrightarrow{B}$ est toujours à flux conservatif, alors que $\overrightarrow{E}$ n’est à flux conservatif que dans les régions vides de charges.*

> [!note] Flux du champ magnétique : Un exemple de canalisation du flux magnétique ; le solénoïde : Champ de quelques spires
> - Champ d’une spire :
> Rappelons les résultats obtenus dans l’[[#^app3|Application 3]].
> ==**Le champ magnétique d’une spire circulaire sur son axe est : $\displaystyle \overrightarrow{B}(M) = \mu_0\frac{I}{2R}\sin^{3}\alpha\,.\overrightarrow{e}_z$.**==
> ==**Au centre de la spire, ce champ est : $\displaystyle \overrightarrow{B}(O) = \mu_0\frac{I}{2R}\overrightarrow{e}_z$.**==
> La [[#^figure19|figure 19]] représente des lignes du champ d’une spire circulaire d’axe $(Oz)$ dans un plan contenant cet axe.
> Par rotation de l’une de ces lignes autour de l’axe de la spire, nous pouvons obtenir un tube de champ magnétique dont les sections perpendiculaires à $(Oz)$ sont circulaires. Considérons ce tube en pensant à la conservation du flux magnétique le long de celui-ci :
> 	- le tube est resserré lorsqu’il traverse la spire, qui sert de goulet d’étranglement canalisant le flux magnétique qui est intense dans cette zone ;
> 	- en s’éloignant de la spire, le tube s’évase rapidement, ce qui laisse prévoir une diminution rapide de l’intensité du champ ;
> 	- le tracé de $B_{z(axe)} = \frac{\mu_0I}{2R}\sin^{3}\alpha = \frac{\mu_0IR^{2}}{2[R^{2} + z^{2}]^{\frac{3}{2}}}$ en fonction de $z$ sur la [[#^figure20|figure 20]] confirme ces considérations qualitatives.
> - Amélioration de la canalisation du flux :
> Pour augmenter le champ et étendre la zone de concentration de son flux, nous pouvons songer à associer plusieurs spires de même axe parcourues par des courants de même sens.
> Les figures [[#^figure21a|21a]], [[#^figure21b|21b]], [[#^figure22a|22a]], [[#^figure22b|22b]], [[#^figure23a|23a]] et [[#^figure23b|23b]] rendent compte de l’association de deux, cinq puis dix spires identiques et régulièrement espacées.

> [!note] Flux du champ magnétique : Un exemple de canalisation du flux magnétique ; le solénoïde : Lignes de champ du solénoïde
# Définitions

# Diagrammes
Force de Laplace s’exerçant sur le rail $A_1A_2$
![[electromagnetisme1/attachments-electromagnetisme1/figure99.png]]^figure1

Élément de courant d’un courant filiforme : $d\overrightarrow{C} = Id\overrightarrow{l}$
![[electromagnetisme1/attachments-electromagnetisme1/figure100.png]]^figure2

Tube de courant mésoscopique considéré comme circuit filiforme : $d\overrightarrow{C} = \overrightarrow{j}d\tau$
![[electromagnetisme1/attachments-electromagnetisme1/figure101.png]]^figure3a

Ruban de courant mésoscopique considéré comme circuit filiforme : $d\overrightarrow{C} = \overrightarrow{j_s}dS$
![[electromagnetisme1/attachments-electromagnetisme1/figure102.png]]^figure3b

Champ magnétique d'une distribution de courants
![[electromagnetisme1/attachments-electromagnetisme1/figure103.png]]^figure4

Exemple de ligne de champ
![[electromagnetisme1/attachments-electromagnetisme1/figure105.png]]^figure5

Les éléments de la limaille de fer se comportent comme des petits aimants qui s’orientent parallèlement au champ magnétique
![[electromagnetisme1/attachments-electromagnetisme1/figure106.png]]^figure6

Tube de champ
![[electromagnetisme1/attachments-electromagnetisme1/figure110.png]]^figure10

Point de champ nul
![[electromagnetisme1/attachments-electromagnetisme1/figure111.png]]^figure11

![[electromagnetisme1/attachments-electromagnetisme1/figure112.png]]^figure12

Champ magnétique sur un plan de symétrie
![[electromagnetisme1/attachments-electromagnetisme1/figure113.png]]^figure13a

Champs en deux points symétriques
![[electromagnetisme1/attachments-electromagnetisme1/figure114.png]]^figure13b

Champ sur un plan d’antisymétrie
![[electromagnetisme1/attachments-electromagnetisme1/figure116.png]]^figure14a

Champs en deux points symétriques
![[electromagnetisme1/attachments-electromagnetisme1/figure117.png]]^figure14b

Invariance par translation discrète
![[electromagnetisme1/attachments-electromagnetisme1/figure118.png]]^figure15

Invariance par rotation avec $n = 6$
![[electromagnetisme1/attachments-electromagnetisme1/figure119.png]]^figure16

Lignes de champ traversant une surface fermée
![[electromagnetisme1/attachments-electromagnetisme1/figure120.png]]^figure17

Le flux de $\overrightarrow{B}$ à travers deux surfaces $S_1$ et $S_2$ s’appuyant sur un même tube de champ ne dépend pas du choix de ces surfaces $\Phi_1 = \Phi_2$
![[electromagnetisme1/attachments-electromagnetisme1/figure121.png]]^figure18
# Graphiques
Exemple : spectre magnétique d’un solénoïde (ensemble de spires)
![[electromagnetisme1/attachments-electromagnetisme1/figure107.png]]^figure7

Exemple : spectre magnétique d’un aimant
![[electromagnetisme1/attachments-electromagnetisme1/figure108.png]]^figure8

Lignes de champ du vecteur champ magnétique créé par une spire
![[electromagnetisme1/attachments-electromagnetisme1/figure109.png]]^figure9

 Lignes de champ magnétique d’une spire
 ![[electromagnetisme1/attachments-electromagnetisme1/figure122.png]]^figure19

Champ sur l’axe d’une spire
![[electromagnetisme1/attachments-electromagnetisme1/figure123.png]]^figure20

Lignes de champ magnétique d’un ensemble de deux spires parcourues par des courants identiques
![[electromagnetisme1/attachments-electromagnetisme1/figure124.png]]^figure21a

Allure de $B(z)$ dans le cas de deux spires parcourues par des courants identiques
![[electromagnetisme1/attachments-electromagnetisme1/figure125.png]]^figure21b

Lignes de champ magnétique d’un ensemble de cinq spires parcourues par des courants identiques
![[electromagnetisme1/attachments-electromagnetisme1/figure126.png]]^figure22a

Allure de $B(z)$ dans le cas de cinq spires parcourues par des courants identiques
![[electromagnetisme1/attachments-electromagnetisme1/figure127.png]]^figure22b

Lignes de champ magnétique d’un ensemble de dix spires parcourues par des courants identiques
![[electromagnetisme1/attachments-electromagnetisme1/figure128.png]]^figure23a

Allure de $B(z)$ dans le cas de dix spires parcourues par des courants identiques
![[electromagnetisme1/attachments-electromagnetisme1/figure129.png]]^figure23b
# Expériences

# Autres notes
> [!warning] Application 1 page 117
> ![[electromagnetisme1/attachments-electromagnetisme1/figure98.png]]
^app1

> [!warning] Application 3 page 121
> ![[electromagnetisme1/attachments-electromagnetisme1/figure104.png]]
^app3

> [!warning] Application 4 page 124
> ![[electromagnetisme1/attachments-electromagnetisme1/figure115.png]]
^app2

> [!warning] Isométrie
> Toute isométrie (transformation géométrique qui laisse invariantes les distances) peut se mettre sous la forme d'un produit de $n$ symétries planes.
> - Si $n$ est impair, l’isométrie est dite négative.
> - Si $n$ est pair, l’isométrie est dite positive.
> 
> Un vecteur polaire et un vecteur axial se distinguent par la transformation qu’ils subissent lors d’une isométrie négative.