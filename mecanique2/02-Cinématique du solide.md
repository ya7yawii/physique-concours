---
titre: "[[02-Cinématique du solide]]"
tags:
  - formule-de-Varignon
  - glissement
  - roulement
  - pivotement
crée: 02-10-2025, 16:56
---
# Formules
> [!note] Formule de Varignon
> Si M et N sont deux points qui appartiennent <mark style="color: red">au même solide</mark>, alors leurs vitesses au même instant t sont liées par la formule de Varignon : $\overrightarrow{V}(N, t) = \overrightarrow{V}(M, t) + \overrightarrow{NM} \wedge \overrightarrow{\Omega}(t)$ qui s'écrit aussi $\overrightarrow{V}(N, t) = \overrightarrow{V}(M, t) + \overrightarrow{\Omega}(t) \wedge \overrightarrow{MN}$ avec $\overrightarrow{\Omega}(t)$ est le <mark style="color: red">vecteur rotation instantané</mark>, aussi appelé vecteur vitesse angulaire instantané.
> Le champ des vitesses d'un solide est ainsi décrit par un [[#^info|torseur]] dont les éléments de réduction sont le vecteur rotation instantané et la vitesse en un point du solide. La formule de Varignon n'est en fait rien d'autre qu'une relation de transport caractéristique des torseurs. Ainsi, l'hypothèse d'indéformabilité d'un solide impose une relation entre les vitesses au même instant de deux points appartenant au solide.
> À chaque instant, le mouvement d'un solide $(S)$ est déterminé par les deux vecteurs correspondant aux éléments de réduction du torseur cinématique. Il s'agit donc de 6 scalaires. On dit que le solide est un système à 6 degrés de liberté. Ces degrés de liberté sont répartis de la façon suivante :
> - 3 degrés de liberté de translation, associés aux trois coordonnées d'un point du solide ;
> - 3 degrés de liberté d'orientation, associés aux rotations d'axes liés au solide.
>
> Le champ des accélérations d'un solide n'est généralement pas décrit par un torseur.

> [!note] Cas particuliers de mouvements d'un solide
> - Solide en translation : un solide est en translation si le vecteur rotation instantané est constamment nul. La vitesse est alors la même en tout point du solide.
> - Solide en rotation autour d'un axe fixe :  Si un point du solide est sur l'axe de rotation, sa vitesse est nulle. Notons O un tel point. Le champ des vitesses s'écrit alors sous la forme $\overrightarrow{V}(M) = \overrightarrow{\Omega} \wedge \overrightarrow{OM}$. L'axe de rotation est dirigé selon le vecteur rotation instantané $\overrightarrow{\Omega}$ qui présente une direction fixe. Tous les points du solide décrivent des cercles de même axe, l'axe de rotation. Si aucun point du solide ne se trouve sur l'axe de rotation, on peut cependant considérer un point O de l'axe et retenir l'expression précédente pour le champ des vitesses du solide.
> - Solide en rotation autour d'un axe de direction fixe : Une importance particulière est accordée aux mouvements de rotation autour d'axes de direction fixe. Lorsqu'un solide est en rotation autour d'un axe de direction fixe, son mouvement se décompose en une rotation dans son référentiel barycentrique autour d'un axe de même direction et en une translation de son centre d'inertie G. Un tel mouvement est par exemple observé dans le cas d'une roue qui roule sur un plan. La roue présente alors, a priori, deux degrés de liberté. En effet, sa position à un instant donné est décrite par :
> 	- l'abscisse x du centre d'inertie G ;
> 	- l'angle $\theta = (\overrightarrow{e_x}, \overrightarrow{GM})$ où M est un point fixe sur la roue ([[#^figure1]]).
> - Mouvement général d'un solide : Le mouvement le plus général d'un solide est la composition, à chaque instant, d'une rotation à vitesse angulaire $\Omega$ autour de l'axe instantané de rotation et d'une translation à vitesse v le long de cet axe ([[#^figure2]]). L'axe instantané de rotation peut varier au cours du temps, à la fois dans le référentiel d'étude et par rapport au solide. On parle de mouvement hélicoïdal si $\overrightarrow{\Omega}$ et $\overrightarrow{v}$ sont constants.
> - Mouvement plan : Un solide est en mouvement plan si les vitesses de tous ses points sont colinéaires à un plan fixe donné, pendant toute la durée du mouvement. On représente alors communément ce champ des vitesses dans le plan ([[#^figure3]]).

> [!note] Vitesse de glissement
> Considérons un contact <mark style="color: red">ponctuel</mark>. Notons I le point de contact. Il est important de distinguer trois points qui ont des rôles différents, bien qu'ils soient confondus géométriquement :
> - le point I de l'espace qui est l'intersection des surfaces des deux solides ;
> - le point matériel $I_1$ appartenant au solide 1 et coïncidant, à l'instant t, avec I ;
> - le point matériel $I_2$ appartenant au solide 2 et coïncidant, à l'instant t, avec I ([[#^figure5]]).
> 
> On appelle vitesse de glissement de $\Sigma_2$ par rapport à $\Sigma_1$ la vitesse relative : $\overrightarrow{v}_{I_2} - \overrightarrow{v}_{I_1} = \overrightarrow{v}(I_2/\Sigma_1) \quad (I_j \in \Sigma_j)$.
> La vitesse de glissement est indépendante du référentiel d'étude. On peut, en particulier, la déterminer dans un référentiel attaché à l'un des solides.
> La vitesse de glissement est nécessairement dans le plan tangent commun aux deux solides. Dans le cas contraire, il y aurait rupture du contact ou interpénétration des solides.

> [!note] Roulement et pivotement
> Décrire le mouvement relatif d'un solide $\Sigma_2$ par rapport à un solide $\Sigma_1$ revient à préciser le mouvement de $\Sigma_2$ dans un référentiel attaché à $\Sigma_1$. Le vecteur instantané de rotation $\overrightarrow{\Omega}_{2/1}$ de $\Sigma_2$ dans un référentiel attaché à $\Sigma_1$ a deux composantes :
> - l'une normale au plan de contact entre les deux solides et qui correspond au mouvement de <mark style="color: red">pivotement</mark> ;
> - l'autre parallèle au plan de contact et qui correspond au <mark style="color: red">roulement</mark> ([[#^figure6]]).
> 
> La donnée de la vitesse de glissement et du vecteur instantané de rotation $\overrightarrow{\Omega}_{2/1}$ détermine complètement le champ des vitesses du solide $\Sigma_2$ dans un référentiel attaché à $\Sigma_1$.

> [!note] Roulement sans glissement
> Un solide $\Sigma_2$, en contact avec un solide $\Sigma_1$, roule sans glisser lorsqu'en tout point de contact la vitesse de glissement est nulle.

> [!note] Rappel des lois de composition des vitesses et des accélérations
> Soient $(R)$ le référentiel d'étude (référentiel absolu) et $(R')$ un référentiel en mouvement dans $(R)$ (référentiel relatif). Le mouvement de $(R')$ est caractérisé par le vecteur vitesse $\overrightarrow{V}(O', t)$ et le vecteur vitesse angulaire $\overrightarrow{\Omega}(t)$. Soit M un point matériel dont on étudie le mouvement dans chacun des référentiels.
> - Loi de composition des vitesses : $\overrightarrow{v}(M, t)_{(R)} = \overrightarrow{v}(M, t)_{(R')} + \overrightarrow{v}_e(M, t)$ où $\overrightarrow{v}_e(M, t)$, vitesse d'entraînement, est la vitesse d'un point lié à $(R')$ coïncidant avec M au temps t. On a : $\overrightarrow{v}_e(M, t) = \overrightarrow{V}(O', t) + \overrightarrow{MO'} \wedge \overrightarrow{\Omega}(t)$.
> - Loi de composition des accélérations : $\overrightarrow{a}(M, t)_{(R)} = \overrightarrow{a}(M, t)_{(R')} + \overrightarrow{a_e}(M, t) + \overrightarrow{a_c}(M, t)$ où $\overrightarrow{a_e}(M, t)$, accélération d'entraînement, c'est-à-dire l'accélération d'un point lié à $(R')$ coïncidant avec M au temps t, et $\overrightarrow{a_c}(M, t)$ est l'accélération de Coriolis. On a :
> $$
> \begin{align*}
> \overrightarrow{a_e}(M, t) &= \overrightarrow{a}(O', t)_{(R)} + \overrightarrow{\Omega} \wedge (\overrightarrow{\Omega} \wedge \overrightarrow{O'M}) + \dfrac{d\overrightarrow{\Omega}}{dt} \wedge \overrightarrow{O'M}\\
> \overrightarrow{a_c}(M, t) &= 2\overrightarrow{\Omega} \wedge \overrightarrow{v}(M, t)_{(R')}
> \end{align*}
> $$
> - Composition des vecteurs rotations : Soit $\overrightarrow{\Omega}_{\Sigma/(R')}$ le vecteur instantané de rotation d'un solide dans un référentiel $(R')$, lui-même en rotation de vecteur $\overrightarrow{\Omega}_{(R')/(R)}$ par rapport à un référentiel $(R)$. Le solide a alors pour vecteur instantané de rotation dans $(R)$ : $\overrightarrow{\Omega}_{\Sigma/(R)} = \overrightarrow{\Omega}_{\Sigma/(R')} + \overrightarrow{\Omega}_{(R')/(R)}$.
# Définitions
==**Cinématique**== :
La cinématique est l'étude du mouvement des systèmes matériels sans chercher à en expliquer les causes. Un solide présente en général six degrés de liberté. Son champ des vitesses est décrit par un « torseur cinématique ». Le mouvement relatif de deux solides en contact se décompose en glissement, roulement et pivotement. Le roulement sans glissement joue un rôle particulier dans de nombreux systèmes mécaniques.

==**Modèle du solide**== :
En mécanique, le solide est un système matériel ==**indéformable**==. La distance entre deux points quelconques du système est donc indépendante du temps.
Il s'agit d'un modèle. Soumis à des contraintes suffisamment importantes, un solide se déforme. La physique des matériaux s'intéresse à ces propriétés que nous ignorons dans tout ce cours de mécanique des solides.
Étant donné l'hypothèse d'indéformabilité, on peut définir un référentiel attaché à un solide $\Sigma$. On choisit ainsi quatre points $(O, A, B, C)$ d'un solide $\Sigma$ tels que le repère $(\overrightarrow{OA}, \overrightarrow{OB}, \overrightarrow{OC})$ soit orthonormé direct. Décrire le mouvement du solide dans un référentiel $(R)$ revient à décrire le mouvement du référentiel attaché au solide par rapport à $(R)$.

> [!note] Nature du contact entre deux solides
> Le contact entre deux solides peut se faire :
> - selon une surface (par exemple, lorsqu'un livre glisse sur une table plane) ;
> - selon une ligne (par exemple, lorsqu'un cylindre roule sur un plan) ;
> - en un point (par exemple, lorsqu'une boule est en mouvement sur une table) ([[#^figure4]]).
> 
> Les deux derniers cas sont en fait des modèles. Le contact réel se fait toujours selon une surface, de dimensions éventuellement très petites. On se ramènera cependant au cas d'un point de contact pour des systèmes dont on peut étudier la « trace » dans un plan (roue cylindrique).
> Sur les schémas précédents, on a représenté des liaisons unilatérales. Dans certains cas, le mouvement d'un solide par rapport à un autre est limité par d'autres contraintes que celles imposées par un simple contact. On définit ci-dessous les principales liaisons.
> ![[mecanique2/attachments-mecanique2/figure10.png]]
# Diagrammes
![[mecanique2/attachments-mecanique2/figure7.png]]^figure2

![[mecanique2/attachments-mecanique2/figure8.png]]^figure3

![[mecanique2/attachments-mecanique2/figure9.png]]^figure4

![[mecanique2/attachments-mecanique2/figure11.png]]^figure5

![[mecanique2/attachments-mecanique2/figure12.png]]^figure6
# Graphiques
![[mecanique2/attachments-mecanique2/figure6.png]]^figure1
# Expériences
## Système de transformation de mouvement (Système bielle manivelle)
> [!warning]
> Ce TP n'est pas dans le livre mais se trouve [en ligne](https://eltaiefmaher.wordpress.com/wp-content/uploads/2018/09/tp-mg-3.pdf).

![[mecanique2/attachments-mecanique2/figure13.png]]
La manivelle (1) est animée d'un mouvement de rotation continue autour de $\overrightarrow{z}$, qui se transforme en un mouvement de translation alternative de (3) suivant l'axe $\overrightarrow{x}$. Soit :
- $AB = L$ : la longueur de la bielle (2),
- $BC = R$ : la longueur de la manivelle (1),
- Condition initiale : à $t = 0 \Rightarrow X = 0, \, \beta = 0 \hspace{0.3em} \text{et} \hspace{0.3em} \alpha = 0$.
Les questions posées dans le TP sont les suivantes :
1. Trouver la relation entre les angles $\alpha$ et $\beta$.
2. Trouver l'expression de X en fonction de $\beta$, R et L.
3. Mesurer les valeurs de R et L directement sur le système bielle manivelle dont vous disposez, et les remplacer dans l'expression de la question précédente.
4. Sur le système bielle manivelle, faire varier $\beta$ de 0 à 360° avec un pas de 20°, relever à chaque fois la valeur de X théorique et compléter le tableau suivant : ![[mecanique2/attachments-mecanique2/figure14.png]]
5. Tracer sur le même papier millimétré les deux courbes (théorique et expérimentale) de $X = f(\beta)$. Commenter.
6. Si la manivelle (1) tourne à une vitesse $\overrightarrow{\Omega} = \dot{\beta}\hspace{0.3em}\overrightarrow{z}$, déterminer le torseur cinématique de la manivelle réduit au point C. $\{v_{1/0}\} = \prescript{}{C}{\left.\begin{cases} \overrightarrow{\Omega}(S/R)\\ \overrightarrow{V}(C \in S/R) \end{cases}\right\}}$. En déduire la vitesse linéaire du point B : $(\overrightarrow{V}_{B \in 1/0})$.
7. Déterminer l'expression de la vitesse linéaire $(\overrightarrow{V}_{A \in 2/0})$.
8. Pour $\dot{\beta} = 2\pi \, rad/s$, compléter le tableau suivant par les valeurs théoriques de $\overrightarrow{V}_{A \in 3/0}$. ![[mecanique2/attachments-mecanique2/figure15.png]]
9. Comparer ce système à celui du système à coulisse.
# Autres notes
> [!warning] Torseur cinématique
> Cette notion n'est pas abordée dans le cours ni dans les exercices mais pour le curieux on peut consulter le livre intitulé "Mécanique fondements et applications" de l'auteur José-Philippe PÉREZ (Chapitre 1 page 27) .
> Pour une définition plus "pratique", on peut visiter les liens suivants : [lien 1](https://sciencesindustrielles.com/Fiches/FICHE%20-%20Cin%C3%A9matique.pdf) et [lien 2](https://rtc.ma/pdfs/TSI/sup-crs/gm/Cineamtique%20Torseur%20Cinematique.pdf).
^info