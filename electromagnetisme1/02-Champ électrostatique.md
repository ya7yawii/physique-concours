---
titre: "[[02-Champ électrostatique]]"
tags:
aliases:
crée: 24-12-2025, 10:58
---
# Formules
> [!note] Loi de Coulomb
> - Force d'interaction entre charges statiques :
> Cette force est répulsive si les charges sont de même signe, attractive sinon.
> ==**La force de Coulomb exercée par la charge $q_1$ sur la charge $q_2$ (les deux charges étant dans le vide) est $\displaystyle \overrightarrow{f}_{1 \rightarrow 2} = \frac{q_1q_2}{4\pi\epsilon_0}\frac{\overrightarrow{e}_{1 \rightarrow 2}}{(M_1M_2)^{2}}$.**==
> $\overrightarrow{e}_{1 \rightarrow 2}$ désigne le vecteur unitaire dirigé de $M_1$ vers $M_2$ ([[#^figure1|fig. 1]]).
> Elle est opposée à la force exercée par $q_2$ sur $q_1$ : $\overrightarrow{f}_{1 \rightarrow 2} = -\overrightarrow{f}_{2 \rightarrow 1}$ ; elle obéit au principe de l’action et de la réaction.
> La constante $\epsilon_0$, permittivité électrique du vide, est voisine de $\displaystyle\frac{1}{36\pi 10^{9}}$ et se mesure en $F\,.\,m^{-1}$, $F$ désignant le farad (unité de capacité).
> La permittivité électrique $\epsilon$ de l’air étant très voisine de $\epsilon_0$ ($\epsilon = \epsilon_0\epsilon_r$, avec $\epsilon_r = 1,\!0006$), la loi de Coulomb reste valable dans l'air.
> - Champ d’une charge ponctuelle :
> La force exercée par $q_1$ sur $q_2$ se met sous la forme : $\displaystyle \overrightarrow{f}_{1 \rightarrow 2} = q_2\overrightarrow{E}_{1}(M_2)$, avec $\displaystyle \overrightarrow{E}_{1}(M_2) = \frac{q_1}{4\pi\epsilon_0}\frac{\overrightarrow{M_1M_2}}{(M_1M_2)^{3}}$.
> $\overrightarrow{E}_{1}(M_2)$ est le champ électrostatique créé par la charge $q_1$ (charge source) au point $M_2$ dans le vide (ou dans l’air).
> Le champ créé par $q_1$ caractérise l’influence de celle-ci sur l’espace qui l’entoure.
> Ainsi, le champ électrostatique créé dans l’espace par une particule de charge $q$, immobile au point origine $O$ du repère de coordonnées sphériques, a pour expression ([[#^figure2|fig. 2]]) : ==**$\displaystyle\overrightarrow{E}(\overrightarrow{r}) = \frac{q}{4\pi\epsilon_0}\frac{\overrightarrow{e}_r}{r^{2}} = \frac{q}{4\pi\epsilon_0}\frac{\overrightarrow{r}}{r^{3}} = \frac{q}{4\pi\epsilon_0}\frac{\overrightarrow{OM}}{OM^{3}}$.**==

> [!note] Champs créés par des distributions de charges ponctuelles
> Utilisant le principe de superposition, nous avons immédiatement :
> ==**Le champ électrostatique $\overrightarrow{E}$ créé en $M$ par diverses charges $q_i$ situées aux points $P_i$ est donné par : $\displaystyle\overrightarrow{E}_{(q_i,\, i\, = \,1,\, \cdots, \,N)}(M) = \frac{1}{4\pi\epsilon_0}\sum_{i=1}^{N}q_i\frac{\overrightarrow{P_iM}}{P_iM^{3}}$.**==

> [!note] Champs créés par des distributions de charges
> Nous appliquerons le principe de superposition à une distribution de charges $\mathcal{D}$ après l’avoir décomposée en un ensemble de fragments élémentaires chargés (mésoscopiques) assimilés à des charges ponctuelles ([[#^figure3|fig. 3]]).
> Notons $P$ un point décrivant l’espace occupé par la distribution. Une partie élémentaire de $\mathcal{D}$, située au voisinage de $P$, contient une charge $dq_P$ et crée un champ élémentaire $d\overrightarrow{E}$ au point d’observation $M$. Nous obtenons le champ total créé en $M$ par la distribution $\mathcal{D}$ par superposition des champs de chacune de ses parties élémentaires selon : ==**$\displaystyle\overrightarrow{E}_{\mathcal{D}}(M) = \frac{1}{4\pi\epsilon_0}\sum_{P \in \mathcal{D}}dq_P\frac{\overrightarrow{e}_{P \rightarrow M}}{PM^{2}} = \frac{1}{4\pi\epsilon_0}\sum_{P \in \mathcal{D}}dq_P\frac{\overrightarrow{PM}}{PM^{3}}$.**==
> On écrira cette expression plus rigoureusement sous la forme : $\displaystyle\overrightarrow{E}_{\mathcal{D}}(M) = \frac{1}{4\pi\epsilon_0}\iiint \limits_{\mathcal{D}}\frac{\overrightarrow{PM}}{PM^{3}}dq_P$.
> Il nous reste à préciser l’élément d’intégration $dq_P$ en fonction de la nature de la distribution considérée.
> - Distribution volumique : ==**$\displaystyle\overrightarrow{E}_{\mathcal{D}}(M) = \frac{1}{4\pi\epsilon_0}\iiint\limits_{\mathcal{D}}\rho(P)\frac{\overrightarrow{PM}}{PM^{3}}d\tau$.**==
> -  Distribution surfacique : ==**$\displaystyle\overrightarrow{E}_{\mathcal{D}}(M) = \frac{1}{4\pi\epsilon_0}\iint\limits_{\mathcal{D}}\sigma(P)\frac{\overrightarrow{PM}}{PM^{3}}dS$.**==
> - Distribution linéique : ==**$\displaystyle\overrightarrow{E}_{\mathcal{D}}(M) = \frac{1}{4\pi\epsilon_0}\int\limits_{\mathcal{D}}\lambda(P)\frac{\overrightarrow{PM}}{PM^{3}}dl$.**==

> [!note] Le champ électrostatique est-il toujours défini ?
> Les expressions précédentes ne sont *a priori* applicables qu’aux cas des distributions d’extension finie (distributions physiques), pour assurer la convergence des intégrales. Il existe toutefois des cas de distributions d’extension infinie pour lesquels ces intégrales convergent.
> Dans le cas d’une distribution volumique de charges $\rho(P)$ finie, d’extension quelconque, l’intégrale dans l'expression de $\overrightarrow{E}(M)$ converge toujours, quelque soit le point $M$.
> Il n’en est plus de même pour les distributions surfaciques et linéiques : le champ $\overrightarrow{E}(M)$ n’est pas défini *sur* ces distributions.
> Prenons l’exemple de l’[[#^app1|Application]] 2 page 21.
> Dans cette application, il est impossible de calculer le champ électrique en un point du segment $AA'$.
> Il en est de même lors d’une distribution surfacique de charges.
> Rappelons que ces modélisations linéiques et surfaciques n’existent que parce que localement la densité volumique de charge $\rho$ est très grande, voire « infinie ».
> C’est le caractère « infini » de $\rho$ qui nous interdit de définir le champ électrostatique en un point d’une distribution linéique ou surfacique.
> ==**Le champ électrostatique en un point des sources n’est pas défini lorsque ces sources sont modélisées par une densité surfacique ou linéique des charges.**==

> [!note] Topographie du champ
> - Lignes de champ :
> ==**Le champ est continuellement tangent à des courbes appelées lignes de champ ([[#^figure4|fig. 4]]). Ces lignes sont orientées par le sens du champ.**==
> La définition des lignes de champ nous permet d’affirmer qu’un élément de longueur $d\overrightarrow{M}$ le long d’une ligne de champ est parallèle au champ $\overrightarrow{E}$. L’équation différentielle (vectorielle) d’une ligne de champ est donc : $d\overrightarrow{M} \wedge \overrightarrow{E} = \overrightarrow{0}$.
> Nous obtiendrons la ligne de champ issue d’un point initial donné par intégration de cette équation différentielle.
> Par exemple, en coordonnées cartésiennes, nous écrirons : $\frac{dx}{E_x} = \frac{dy}{E_y} = \frac{dz}{E_z}$.
> - Tube de champ :
> ==**L’ensemble des lignes de champ s’appuyant sur une courbe fermée (ou contour) $C$  engendre une surface appelée tube de champ, représentée sur la [[#^figure5|figure 5]].**==
> - Points de champ nul, points singuliers :
> *Deux lignes de champ ne se coupent pas en un point $M$ où le champ électrostatique est défini et non nul* ([[#^figure6|fig. 6]]) ; sinon la direction du champ, donc le champ lui-même, ne serait pas défini en ce point.
> Deux lignes de champ peuvent se couper en $M$ si :
> 	- le champ est nul au point $M$ : $M$ est appelé *point de champ nul* (ou *point d’arrêt*) ;
> 	- le champ n’est pas défini au point $M$ : il y a une charge ponctuelle en $M$, ou bien $M$ appartient à une surface ou à une ligne chargée.
> 
> 	Quelques lignes de champ d’un système de deux charges ponctuelles $q$ et $Q$ sont représentées sur les figures [[#^figure7|7a]] (cas $Q = 2q > 0$) et [[#^figure7|7b]] (cas $Q = -2q < 0$).
> 	Nous pouvons observer que les lignes de champ divergent à partir des charges positives, convergent vers les charges négatives, ou « aboutissent » à l’infini. Elles se coupent au niveau des charges ainsi qu’aux points de champ nul $A$ et $A'$.


# Définitions
==**Principe de superposition**== :
L’expérience conduit à postuler que les interactions électrostatiques ont des effets linéaires.
Par exemple, la force subie par une charge $q$ de la part d’un ensemble de $N$ charges $q_1, q_2, \cdots, q_N$ est la somme des $N$ forces qu’exercent individuellement les charges $q_i\,(i = 1, \cdots, N)$ lorsqu’elles sont mises seules en présence de la charge $q$. Le champ créé par les $N$ charges est donc la somme des $N$ champs créés par chaque charge.
Nous postulons donc la *linéarité des effets*, ce qui constitue **le principe de superposition**.
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
# Graphiques
Lignes de champ d’un système de deux charges ponctuelles $q$ et $Q$. a. $Q = 2q$. b. $Q = -2q$
![[electromagnetisme1/attachments-electromagnetisme1/figure16.png]]^figure7
# Expériences

# Autres notes
> [!warning] Application 2 page 21
> ![[electromagnetisme1/attachments-electromagnetisme1/figure12.png]]
^app1
