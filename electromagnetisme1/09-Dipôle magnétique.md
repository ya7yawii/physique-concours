---
titre: "[[09-Dipôle magnétique]]"
tags:
  - moment-dipolaire
  - champ-magnétique
crée: 11-01-2026, 13:29
---
# Formules
> [!note] Moment dipolaire
> - Moment magnétique d'un courant filiforme :
> ==**Le moment magnétique d'une boucle $\Gamma$ de courant d'intensité $I$ (orientée dans le sens du courant) et de vecteur surface $\overrightarrow{S}$ est : $\overrightarrow{\mathcal{M}} = I\overrightarrow{S}$.**==
> La norme du moment magnétique s'exprime en $A\,.m^{2}$.
> Dans le cas d'une spire circulaire de rayon $a$, parcourue par un courant d'intensité $I$ ([[#^figure2|fig. 2]]), le moment magnétique est : $\overrightarrow{\mathcal{M}} = I\pi a^{2}\,\overrightarrow{n}$.
> Sur la [[#^figure3a|figure 3a]], le plan $\Pi_1$ de la spire est un plan de symétrie de la distribution des courants et le moment magnétique $\overrightarrow{\mathcal{M}}$ est perpendiculaire à ce plan. Tout plan $\Pi_2$ contenant l'axe de la spire est un plan d'antisymétrie et le moment magnétique $\overrightarrow{\mathcal{M}}$ est contenu dans ce plan. Nous reconnaissons là deux proriétés caractéristiques des vecteurs axiaux.
> ==**Le moment magnétique $\overrightarrow{\mathcal{M}}$ d'un circuit filiforme est un vecteur axial.**==
> *Remarque :*
> *Nous verrons, plus loin, qu'une boucle élémentaire de courant de moment magnétique $\overrightarrow{\mathcal{M}}$ présente de fortes analogies de comportement avec un dipôle électrostatique de moment dipolaire $\overrightarrow{p}$. Des différences fondamentales distinguent cependant ces deux entités. Montrons ainsi que le moment dipolaire $\overrightarrow{p}$ est un vecteur polaire.*
> *En effet, tout plan $\Pi_1$ contenant le dipôle ([[#^figure3b|fig. 3b]]) est un plan de symétrie de la distribution de charges et le moment dipolaire $\overrightarrow{p}$ est contenu dans ce plan. Le plan médiateur $\Pi_2$ du dipôle est un plan d'antisymétrie et le moment dipolaire $\overrightarrow{p}$ est normal à ce plan. Nous reconnaissons là deux propriétés caractéristiques des vecteurs polaires.*
> - Moment magnétique d'une distribution de courants :
> Dans le cas d'une distribution de courants limités dans l'espace, la définition du moment magnétique sera généralisée en considérant qu'il s'agit d'un ensemble continu de boucles de courant filiformes (tubes de courants élémentaires) : $\displaystyle\overrightarrow{\mathcal{M}} = \int \overrightarrow{d\mathcal{M}}$.

> [!note] Champ magnétostatique créé par un dipôle : Approximation dipolaire
> Une boucle de courant crée, en tout point $M$ de l'espace, un champ magnétostatique donné par la loi de Biot et Savart.
> À grande distance de la boucle ($\frac{a}{r} \ll 1$ pour une spire circulaire de rayon $a$ ([[#^figure4a|fig. 4a]] et [[#^figure4b|b]]), *la norme du champ magnétique décroît en $\frac{1}{r^{3}}$*, comme il est possible de s'en convaincre en considérant l'expression du champ créé par une spire en un point de son axe (cf. [[07-Champ magnétique|chapitre 7]], Application 3) : $\overrightarrow{B}(M) = \frac{\mu_0I}{2R}\sin^{3}\!\alpha\,\overrightarrow{e}_z = \frac{\mu_0I}{2R}\frac{R^{3}}{(R^{2} + z^{2})^{\frac{3}{2}}}\overrightarrow{e}_z$.
> À grande distance $(z \gg R)$, l'expression précédente se simplifie en : $\overrightarrow{B}(M) = \frac{\mu_0I}{2R}\frac{R^{3}}{|z|^{3}}\,\overrightarrow{e}_z = \frac{\mu_0\overrightarrow{\mathcal{M}}}{2\pi|z|^{3}}\overrightarrow{e}_z$ puisque $\overrightarrow{\mathcal{M}} = I\pi R^{2}\,\overrightarrow{e}_z$.
> Il est possible de démontrer, qu'à grande distance d'une boucle de courant (approximation dipolaire), le champ magnétique $\overrightarrow{B}(M)$ créé par la boucle ne dépend que de $\overrightarrow{r} = \overrightarrow{OM}$, du moment magnétique $\overrightarrow{\mathcal{M}}$ et de l'angle $\theta = (\overrightarrow{\mathcal{M}}, \overrightarrow{r})$.
> ==**Dans l'approximation dipolaire, une boucle de courant est entièrement caractérisée par son moment magnétique $\overrightarrow{\mathcal{M}}$.**==
> De nouveau, cette propriété n'est pas sans rappeler celle du dipôle életrostatique qui est, lui aussi, entièrement caractérisé, pour ses effets à grande distance, par son moment dipolaire $\overrightarrow{p}$.
> Cette similitude fait souvent nommer une boucle élémentaire de courant, *dipôle magnétique*.

> [!note] Champ magnétostatique créé par un dipôle : Analogie avec le dipôle électrostatique
> Considérons un doublet de charges $-q$ et $+q$ (distantes de $a$) centré en $O$ et de moment dipolaire $\overrightarrow{p} = q\,a\,\overrightarrow{e}_z = p\,\overrightarrow{e}_z$. Tout plan contenant l'axe $(Oz)$ est un plan de symétrie. Les lignes de champ du vecteur $\overrightarrow{E}$, de révolution autour de l'axe $(Oz)$, sont contenues dans de tels plans. Quelques lignes de champ électrostatique sont représentées dans un plan contenant $(Oz)$ sur la [[#^figure5a|figure 5a]].
> Considérons à présent une spire circulaire de rayon $a$, d'axe $(Oz)$ et de moment dipolaire magnétique $\overrightarrow{\mathcal{M}} = I\pi a^{2}\,\overrightarrow{e}_z = \mathcal{M}\,\overrightarrow{e}_z$. Tout plan contenant l'axe $(Oz)$ est un plan d'antisymétrie. Les lignes de champ du vecteur axial $\overrightarrow{B}$, de révolution autour de l'axe $(Oz)$, sont contenues dans de tels plans. La [[#^figure5b|figure 5b]] représente quelques lignes de champ magnétostatique dans un plan contenant $(Oz)$.
> L'extension de la zone apparaissant sur ces figures est de l'ordre de $(10a)^{2}$. Les deux cartes de champ obtenues sont clairement distinctes, car les comportements des champs au voisinage de leurs sources sont très différents : le champ électrostatique diverge à partir de ses sources (les charges) alors que le champ magnétostatique tourbillonne autour des siennes (les courants).
> Si nous observons ces cartes de champ à une échelle beaucoup plus grande (zone de l'ordre de $(100a)^{2}$ nous obtenons dans les deux cas la même configuration des lignes de champ ([[#^figure6|fig. 6]]).
> ==**Le champ électrostatique d'un dipôle $\overrightarrow{p} = p\,\overrightarrow{e}_z$ et le champ magnétostatique d'un dipôle $\overrightarrow{\mathcal{M}} = \mathcal{M}\,\overrightarrow{e}_z$ ont le même comportement à grande distance $r \gg a$**==.

> [!note] Champ magnétostatique créé par un dipôle : Application au calcul du champ magnétostatique
> - Champ dipolaire :
> Le champ électrostatique d'un doublet de charges a pour coordonnées sphériques d'axe $(Oz)$ ([[#^figure7|fig. 7]]), dans l'approximation dipolaire : $E_r = \frac{1}{4\pi\epsilon_0}\frac{2p\cos\theta}{r^{3}}$, $E_{\theta} = \frac{1}{4\pi\epsilon_0}\frac{p\sin\theta}{r^{3}}$ et $E_{\varphi} = 0$.
> Du fait de l'analogie observée à grande distance des sources, nous supposerons que le champ $\overrightarrow{B}$ créé au point $M$ de coordonnées sphériques $(r, \theta, \varphi)$ par un dipôle $\overrightarrow{\mathcal{M}} = \mathcal{M}\,\overrightarrow{e}_z$ placé en $O$ est de la forme : $B_r = 2B_0\,a^{3}\frac{\cos\theta}{r^{3}}$, $B_{\theta} = B_0\,a^{3}\frac{\sin\theta}{r^{3}}$ et $B_{\varphi} = 0$.
> Le facteur $B_0$ est une constante homogène à un champ magnétique que nous allons déterminer.
> *Remarque : Il est possible d'obtenir ce résultat par développement du champ $\overrightarrow{B}$ créé par une spire en un point éloigné. Un tel calcul est assez fastidieux.*
> - Détermination du champ par identification :
> Pour trouver la constante $B_0$, nous pouvons comparer le champ dipolaire précédent avec le champ créé par une spire en un point très éloigné sur l'axe de celle-ci ([[#^figure8|fig. 8]]). Sur son axe $(Oz)$, le champ de la spire est : $\frac{a}{|z|} \ll 1$, $B(z) \approx \frac{\mu_0I}{2}\frac{a^{2}}{|z|^{3}} = \frac{\mu_0\mathcal{M}}{2\pi|z|^{3}}$.
> Identifiant cette valeur à $B_r = 2B_0\,\frac{a^{3}}{r^{3}}$, avec $r = |z|$ nous obtenons : $B_0\,a^{3} = \frac{\mu_0\mathcal{M}}{4\pi}$.
> Les composantes $B_r$ ,$B_{\theta}$ et $B_{\varphi}$, en coordonnées sphériques, du champ d'un dipôle magnétique placé en $O$ et de moment $\overrightarrow{\mathcal{M}} = \mathcal{M}\,\overrightarrow{e}_z$ sont donc :
> $$
> \begin{cases}
> B_r = \frac{\mu_0\mathcal{M}}{4\pi}\frac{2\cos\theta}{r^{3}}\\
> B_{\theta} = \frac{\mu_0\mathcal{M}}{4\pi}\frac{\sin\theta}{r^{3}}\\
> B_{\varphi} = 0
> \end{cases}
> $$
> ==**L'expression du champ magnétique du dipôle $\overrightarrow{\mathcal{M}}$ est en coordonnées sphériques d'axe $(O, \overrightarrow{\mathcal{M}})$ : $\displaystyle\overrightarrow{B}(M) = \frac{\mu_0}{4\pi}\frac{2\mathcal{M}\cos\theta . \overrightarrow{e}_r + \mathcal{M}\sin\theta . \overrightarrow{e}_{\theta}}{r^{3}}$. Son expression intrinsèque est donc : $\displaystyle\overrightarrow{B}(M) = \frac{\mu_0}{4\pi}\frac{\left[3(\overrightarrow{\mathcal{M}}\,.\overrightarrow{e}_r)\overrightarrow{e}_r - \overrightarrow{\mathcal{M}}\right]}{r^{3}}$.**==

> [!note] Comparaison des propriétés des champs $\overrightarrow{E}$ et $\overrightarrow{B}$ statiques
> À ce stade, nous pouvons résumer et comparer les propriétés des champs électrostatique et magnétostatique.
> ![[electromagnetisme1/attachments-electromagnetisme1/figure162.png]]![[electromagnetisme1/attachments-electromagnetisme1/figure163.png]]
# Définitions
> [!note] Surface associée à un contour
> Considérons un contour $\Gamma$ (fermé) orienté ([[#^figure1|fig. 1]]) et une surface $\overrightarrow{S}$ s'appuyant sur ce contour. L'orientation de la surface s'effectue en utilisant celle du contour (cf. [[08-Le théorème d'Ampère|chapitre 8]]) : un tire-bouchon tournant dans le sens choisi pour $\Gamma$ traverse $S$ dans le sens de ses vecteurs unitaires normaux $\overrightarrow{n}$.
> Nous appellerons *vecteur surface* $\overrightarrow{S}$ le vecteur défini par : $\displaystyle\overrightarrow{S} = \iint_S\overrightarrow{n}dS = \iint_Sd\overrightarrow{S}$.
> Le *vecteur surface* $\overrightarrow{S}$ ne dépend pas du choix de la surface utilisée pour le définir : il ne dépend que du contour $\Gamma$ et de son orientation.
> Le vecteur surface $\overrightarrow{S}$ est une grandeur caractéristique du contour $\Gamma$ orienté.
> Par exemple, le vecteur surface du contour circulaire de rayon $a$ de [[#^figure2|figure 2]] est : $\overrightarrow{S} = \pi a^{2}\,\overrightarrow{n}$.
# Diagrammes
Surface $S$ s'appuyant sur un contour $\Gamma$ orienté
![[electromagnetisme1/attachments-electromagnetisme1/figure151.png]]^figure1

Surface orientée d'un contour circulaire
![[electromagnetisme1/attachments-electromagnetisme1/figure152.png]]^figure2

Étude des symétries sur un dipôle magnétique
![[electromagnetisme1/attachments-electromagnetisme1/figure153.png]]^figure3a

Étude des symétries pour un dipôle électrostatique
![[electromagnetisme1/attachments-electromagnetisme1/figure154.png]]^figure3b

Boucle de courant
![[electromagnetisme1/attachments-electromagnetisme1/figure155.png]]^figure4a

Champ $\overrightarrow{B}(M)$ créé par une spire en un point de son axe
![[electromagnetisme1/attachments-electromagnetisme1/figure156.png]]^figure4b

![[electromagnetisme1/attachments-electromagnetisme1/figure160.png]]^figure7

![[electromagnetisme1/attachments-electromagnetisme1/figure161.png]]^figure8
# Graphiques
Lignes de champ électrostatique d'un doublet $-q$ et $+q$
![[electromagnetisme1/attachments-electromagnetisme1/figure157.png]]^figure5a

Lignes de champ magnétostatique d'une spire
![[electromagnetisme1/attachments-electromagnetisme1/figure158.png]]^figure5b

Ligne de champ d'un dipôle qu'il soit électrique ou magnétique
![[electromagnetisme1/attachments-electromagnetisme1/figure159.png]]^figure6
# Expériences

# Autres notes
