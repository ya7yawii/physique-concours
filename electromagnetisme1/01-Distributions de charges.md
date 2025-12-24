---
titre: "[[01-Distributions de charges]]"
tags:
  - distribution-de-charges
  - charge-volumique
  - charge-surfacique
  - charge-linéique
  - symétrie
  - invariance
  - échelle-mésoscopique
crée: 22-12-2025, 11:24
---
# Formules
Charge élémentaire : $e = 1,\!602\, . \,10^{-19}\,C$

> [!note] Charges volumiques
> La présence de charges dans un milieu est en général modélisée par une charge délocalisée, nivelée, décrite par la charge volumique $\rho$.
> Pour un milieu chargé de volume $V$, la distribution de charges $\mathcal{D}$ est définie par la donnée de $\rho$ à l'intérieur de la surface $S$ contenant $V$ ([[#^figure2|fig. 2]]).
> ==**La charge contenue dans un *volume élémentaire* $d\tau$ (petit à l'échelle macroscopique et de l'ordre de $l^{3}$) est : $dq = \rho d\tau$. La densité volumique $\rho$ est mesurée en $C\,.\,m^{-3}$.**==

> [!note] Charges surfaciques
> ==**La charge portée par une surface élémentaire $dS$ (petite à l'échelle macroscopique et de l'ordre de $l^{2}$) s'écrit alors $dq = \sigma dS$. La densité surfacique de charges $\sigma$ est mesurée en $C\,.\,m^{-2}$.**==

> [!note] Charges linéiques
> ==**La charge portée par une *longueur élémentaire* $dl$ est $dq = \lambda dl$. La densité linéique $\lambda$ est mesurée en $C\,.\,m^{-1}$.**==

> [!note] Distributions de matière
> La masse contenue dans un volume élémentaire $d\tau$ est : $dm = \mu d\tau$, la masse volumique $\mu$ est mesurée en $kg\,.\,m^{-3}$.

> [!note] Symétries des distributions de charges
> - Symétrie plane :
> ==**Une distribution est symétrique par rapport à un plan $\Pi$ si, $M$ et $M'$ étant deux points symétriques par rapport à $\Pi$, sa densité de charge vérifie : $\rho(M) = \rho(M')$.**==
> Le plan $\Pi$ de symétrie est aussi appelé *plan-miroir* ([[#^figure3|fig. 3]]).
> En coordonnées cartésiennes, une distribution de charges est symétrique par rapport au plan $\Pi = (xOy)$, lorsque : $\rho(x, y, z) = \rho(x, y, -z)$.
> - Antisymétrie plane :
> ==**Une distribution est antisymétrique par rapport à un plan $\Pi^{*}$ si, $M$ et $M'$ étant deux points symétriques par rapport à $\Pi^{*}$, sa densité de charge vérifie : $\rho(M) = -\rho(M')$.**==
> Le plan $\Pi^{*}$ est appelé *plan d'antisymétrie* ou *plan-antimiroir*.
> En coordonnées cartésiennes, une distribution de charges admet le plan $\Pi^{*} = (xOy)$ comme plan de symétrie, lorsque : $\rho(x, y, z) = -\rho(x, y, -z)$.
> - Invariance par translation :
> ==**Une distribution, illimitée dans la direction de l'axe $\Delta$, est invariante par translation suivant $\Delta$ si, pour tout point $M$ et son translaté $M'$, sa densité de charge vérifie : $\rho(M) = \rho(M')$**==.
> En coordonnées cartésiennes, si l'axe $(Oz)$ est pris comme axe $\Delta$, une telle distribution satisfait à l'égalité $\rho(x, y, z) = \rho(x, y, z')$ quel que soit $z$ et $z'$, donc la densité de charge est indépendante de la coordonnée $z$ : $\rho(x, y)$.
> La [[#^figure4|figure 4]] illustre ce cas : distribution de charges contenue dans un cylindre de génératrices parallèles à l'axe $(Oz)$, invariante par translation parallèlement à l'axe (Oz). Notons que tout plan perpendiculaire à cet axe constitue un plan de symétrie de la distribution.
> Remarque : Nous pourrons aussi rencontrer des cas de distributions invariantes par des translations discrètes le long d'un axe. Ces distributions présenteront un caractère périodique le long de l'axe, comme l'illustre la [[#^figure5|figure 5]].
> - Invariance par rotation :
> Une distribution est invariante par rotation autour d'un axe $(Oz)$ si la densité de charges est la même en un point $M$ de la distribution et en tout point $M'$ obtenu par rotation d'un angle quelconque de $M$ autour de l'axe. Notons $(r , \theta, z)$ les coordonnées cylindriques d'axe $(Oz)$ du point $M$. Pour une telle distribution, la répartition de charges ne doit pas dépendre de l'angle $\theta$.
> ==**La charge d'une distribution invariante par rotation autour d'un axe $(Oz)$ est telle que $\rho(r , \theta, z) = \rho(r , z)$.**==
> Remarquons que tout plan contenant l'axe de révolution $(Oz)$ est un plan de symétrie de la distribution de charges ([[#^figure6|fig. 6]]).
> Remarque : Nous pourrons aussi rencontrer des cas de distributions invariantes par des rotations discrètes autour d'un axe. Un ensemble de trois charges identiques occupant les trois sommets d'un triangle équilatéral est invariant par rotation d'angle $\alpha$ multiple entier de $\frac{2\pi}{3}$ autour de l'axe perpendiculaire au plan du triangle et passant par son centre.

> [!note] Distributions à symétries multiples
> Nous rencontrerons fréquemment des distributions invariantes vis-à-vis de plusieurs symétries élémentaires. Nous avons déjà remarqué que les distributions invariantes par translation, ou par rotation, possèdent une infinité de plans-miroirs.
> Nous citerons encore deux types de distributions de charges remarquables par leur degré de symétrie élevé. L'utilisation des propriétés précédentes permet de démontrer les propositions suivantes.
> - Distribution à symétrie cylindrique :
> La distribution à symétrie cylindrique est invariante par translation parallèlement à un axe noté $(Oz)$ (tout plan perpendiculaire à l'axe $(Oz)$ est plan de symétrie), et elle est de révolution autour de cet axe (tout plan contenant l'axe $(Oz)$ est plan de symétrie). Utilisant les coordonnées cylindriques d'axe $(Oz)$, nous avons ([[#^figure7|fig. 7]]) :
> ==**Distribution à symétrie cylindrique : $\rho(r, \theta, z) = \rho(r)$.**==
> - Distribution à symétrie sphérique :
> La distribution à symétrie sphérique est invariante par rotation autour de tous les axes passant par le centre de symétrie.
> Remarquons, de plus, que tout plan contenant l'origine est plan de symétrie de la distribution.
> Utilisant les coordonnées sphériques $r$, $\theta$ et $\phi$ avec l'origine au point centre de symétrie, nous avons ([[#^figure8|fig. 8]]) :
> ==**Distribution à symétrie sphérique : $\rho(r, \theta, \phi) = \rho(r)$.**==
# Définitions
> [!note] Conservation de la charge
> ==**Pour un système fermé, c'est-à-dire n'échangeant pas de matière avec l'extérieur, la charge électrique est constante et elle est la même pour tous les observateurs.**==

==**Échelle mésoscopique**== :
À l'échelle microscopique, la structure de la matière est discontinue. Les entités microscopiques sont considérées explicitement et cette particularité se prête mal à l'étude de leurs comportements d'ensemble.
À l'échelle macroscopique, la description des objets est imprécise et elle ne permet pas de prévoir leurs comportements.
Pour lever ce dilemme il est nécessaire d'introduire une troisième échelle, dite mésoscopique. Cette échelle, intermédiaire entre l'échelle microscopique de longueur caractéristique $d$ et l'échelle macroscopique de longueur caractéristique $D$, est définie par une longueur caractéristique $l$ satisfaisant à la double inégalité $d \ll l \ll D$.
Sous réserve de l'existence d'une telle échelle, il sera possible de donner une description locale des objets étudiés avec les deux avantages suivants :
- comme $l \gg d$, il est possible de définir convenablement la *grandeur locale moyenne* des grandeurs attachées aux entités microscopique, puisqu'un volume $l^{3}$ contient un très grand nombre de ces entités. Cette opération de lissage ou de nivellement fait de la valeur locale une grandeur variant continûment. Il est dès lors possible d'adopter une description des objets en *termes de milieux continus* ;
- comme $l \ll D$, le volume $l^{3}$ reste très petit à l'échelle macroscopique, et, de ce fait, la description locale est une description précise de l'objet étudié.
La [[#^figure1|figure 1]] résume les propriétés des trois échelles : microscopique, mésoscopique et macroscopique.
==**À une échelle macroscopique, les distributions de charges (entités microscopiques) seront représentées à l'aide d'une grandeur nivelée à une échelle mésoscopique : la densité de charges.**==
Remarque : La description des distributions de charges en termes mésoscopiques est la seule qui soit opératoire quand le nombre de charges est élevé. Mais nous perdons toute information sur le comportement individuel des entités microscopiques et nous devons nous contenter dès lors de leur comportement local d'ensemble.
# Diagrammes
Échelles microscopique $d$, mésoscopique $l$ et macroscopique $D$
![[electromagnetisme1/attachments-electromagnetisme1/figure1.png]]^figure1

Distribution volumique de charges
![[electromagnetisme1/attachments-electromagnetisme1/figure2.png]]^figure2

Distribution invariante par symétrie plane
![[electromagnetisme1/attachments-electromagnetisme1/figure3.png]]^figure3

Distribution invariante par translation
![[electromagnetisme1/attachments-electromagnetisme1/figure4.png]]^figure4

Distribution invariante par translation
![[electromagnetisme1/attachments-electromagnetisme1/figure5.png]]^figure5

Distribution invariante par rotation autour d'un axe $(Oz)$
![[electromagnetisme1/attachments-electromagnetisme1/figure6.png]]^figure6

Distribution à symétrie cylindrique
![[electromagnetisme1/attachments-electromagnetisme1/figure7.png]]^figure7

Distribution à symétrie sphérique
![[electromagnetisme1/attachments-electromagnetisme1/figure8.png]]^figure8
# Graphiques

# Expériences

# Autres notes
