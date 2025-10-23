---
titre: "[[05-Les actions sur un système]]"
tags:
  - actions
  - résultante
  - moment
  - couple-de-forces
  - liaison-pivot
  - liaison-rotule
  - tension
crée: 11-10-2025, 11:12
---
# Formules
> [!note]
> Le vecteur force apparaissant dans le principe fondamental de la dynamique est ici généralisé au cas d'un ensemble de points, discret ou continu. Ce vecteur force est remplacé par un ensemble de vecteurs appelé « actions sur le système ».
> Cet ensemble n'est pas équivalent, en général, à un seul vecteur s'appliquant sur le système en un seul point. C'est pourquoi on utilisera le terme d'«actions» ou d'«efforts» sur le système $(S)$. On déterminera plus loin sous quelles conditions les actions sont équivalentes à une force unique.

Résultante des actions : $\displaystyle \overrightarrow{F} = \sum_{i=1}^{N} \overrightarrow{f}_i$ avec $\overrightarrow{f}_i$ est la force exercée sur le point $P_i$ ; $\overrightarrow{f}_i = \overrightarrow{f}_{i\,ext} + \overrightarrow{f}_{i\,int}$.
> [!note]
> La définition de la résultante des actions sur les systèmes continus est analogue, l'intégrale remplaçant la somme et l'élément de force $d\overrightarrow{f}(P)$ que subit l'élément matériel en P remplaçant la force $\overrightarrow{f}_i$.

Résultante des forces extérieures : $\displaystyle \overrightarrow{F}_{ext} = \sum_{i=1}^{N} \overrightarrow{f}_{i\,ext}$ où $\overrightarrow{f}_{i\,ext} = \overrightarrow{f}_{(S')\rightarrow i} + \overrightarrow{f}_{i\,ie} + \overrightarrow{f}_{i\,ic}$ ; $\overrightarrow{f}_{(S')\rightarrow i}$, $\overrightarrow{f}_{i\,ie}$ et $\overrightarrow{f}_{i\,ic}$ sont définis dans la [[#^484f10|définition des actions extérieures]].

Résultante des [[#^9ef48c|forces d'interaction]] ==**sur le point $P_i$**== : $\displaystyle \overrightarrow{f}_{i \, int} = \sum_{j=1}^{N} \overrightarrow{f}_{j\rightarrow i}$.
> [!note] Propriétés des actions intérieures
> Les forces d'interaction vérifient la loi des actions réciproques ou $3^e$ loi de Newton :
> - $\overrightarrow{f}_{i \rightarrow j} = -\overrightarrow{f}_{j \rightarrow i}$ ;
> - $\overrightarrow{P_iP_j} \wedge \overrightarrow{f}_{j \rightarrow i} = \overrightarrow{0}$.
> 
> Par convention, on posera : $\overrightarrow{f}_{i \rightarrow i} = \overrightarrow{0}$ un point n'exerçant aucune force sur lui-même.
> Pour les systèmes continus, ces actions sont décrites par des éléments de force infinitésimaux : on écrit l'élément de force sur un élément infinitésimal de volume $d\tau$ repéré par le point $P$ dont l'origine est un autre volume $d\tau'$ autour d'un point $P'$ du système : $d\overrightarrow{f}_{P'\rightarrow P}$ ([[#^figure1|fig. 1]]).

> [!note]
> La résultante des forces intérieures à un système est nulle : $\overrightarrow{F}_{int} = \overrightarrow{0}$.
> Une conséquence de ce théorème est importante : la résultante des actions $\overrightarrow{F}$ s'exprime uniquement à partir des actions extérieures : $\overrightarrow{F} = \overrightarrow{F}_{ext}$.

> [!note] Principe des actions réciproques relatif à la résultante
> Soient à présent deux systèmes $(S_1)$ et $(S_2)$, formés respectivement de $N_1$ points notés $P_i$, $i = 1, \,\ldots, N_1$ et $N_2$ points notés $M_j$, $j = 1, \,\ldots, N_2$.
> Soient $\displaystyle \overrightarrow{F}_{1\rightarrow 2} = \sum_{i=1}^{N_1}\sum_{j=1}^{N_2} \overrightarrow{f}_{P_i\rightarrow M_j}$ la résultante des actions de $(S_1)$ sur $(S_2)$ et $\displaystyle \overrightarrow{F}_{2\rightarrow 1} = \sum_{i=1}^{N_1}\sum_{j=1}^{N_2} \overrightarrow{f}_{M_j\rightarrow P_i}$ la résultante des actions de $(S_2)$ sur $(S_1)$. Alors $\overrightarrow{F}_{1\rightarrow 2} = -\overrightarrow{F}_{2\rightarrow 1}$.
> Il s'agit d'une conséquence du principe fondamental de la dynamique énoncé en termes d'égalité de deux torseurs, respectivement [[#^info1|dynamique]] et des actions extérieures.

Moment des actions : $\displaystyle \overrightarrow{\Gamma}_A = \sum_{i=1}^{N} \overrightarrow{AP_i} \wedge \overrightarrow{f}_i$. On a aussi $\overrightarrow{\Gamma}_A = \overrightarrow{\Gamma}_{A\,ext} + \overrightarrow{\Gamma}_{A\,int}$ avec $\displaystyle \overrightarrow{\Gamma}_{A\,ext} = \sum_{i=1}^{N} \overrightarrow{AP_i} \wedge \overrightarrow{f}_{i\,ext}$ et $\displaystyle \overrightarrow{\Gamma}_{A\,int} = \sum_{i=1}^{N} \overrightarrow{AP_i} \wedge \overrightarrow{f}_{i\,int}$. A est appelé point de réduction et les dimensions du moment sont : $kg.m^{2}.s^{-2}$ ou $N.m$.
> [!note]
> Le moment des actions intérieures est nul : $\overrightarrow{\Gamma}_{A\,int} = \overrightarrow{0}$.
> Conséquence : le moment des actions sur un système est égal au moment des actions extérieures : $\overrightarrow{\Gamma}_{A} = \overrightarrow{\Gamma}_{A\,ext}$.

Relation de transport : $\overrightarrow{\Gamma}_B = \overrightarrow{\Gamma}_A + \overrightarrow{BA} \wedge \overrightarrow{F}$.
> [!note] Relation de transport
> On peut remarquer que ce théorème de transport est analogue à celui qu'on a établi pour le moment cinétique et pour le champ des vitesses d'un solide.
> La forme mathématique de cette relation est dans les trois cas rencontrés : $\overrightarrow{Moment}_B = \overrightarrow{Moment}_A + \overrightarrow{BA} \wedge \overrightarrow{Résultante}$. Cette relation décrit la propriété des champs de vecteur appelés « torseurs ». Par exemple, la vitesse d'un point d'un solide est un « moment » et le vecteur vitesse angulaire une « résultante » d'un torseur, appelé <mark style="color: red">torseur cinématique</mark> du solide.

> [!note] Équivalence entre un champ d'actions et une force
> Pour calculer le moment des actions, il faut en général connaître la répartition des actions individuelles sur les points matériels.
> En revanche, dans certains cas, il existe un point P tel que le moment des actions en un point A quelconque et la résultante vérifient : $\overrightarrow{\Gamma}_A = \overrightarrow{AP} \wedge \overrightarrow{F}$. On dit que les actions sont <mark style="color: red">réductibles à une force $\overrightarrow{F}$ appliquée en P</mark>. On montre que les conditions nécessaires et suffisantes sont les suivantes : $\overrightarrow{F} \neq \overrightarrow{0}$ et $\overrightarrow{F} . \overrightarrow{\Gamma}_A = 0$.

Principe des actions réciproques relatif au moment : $\overrightarrow{\Gamma}_{A\,1\rightarrow 2} = -\overrightarrow{\Gamma}_{A\,2\rightarrow 1}$. Il s'agit d'une conséquence du principe fondamental de la dynamique énoncé en termes d'égalité de deux torseurs, respectivement [[#^info1|dynamique]] et des actions extérieures.

> [!note] Couple de forces
> Les actions sur un système constituent un couple lorsque la résultante est nulle et le moment non nul ; $\overrightarrow{F} = \overrightarrow{0}$ et $\overrightarrow{\Gamma}_A \neq \overrightarrow{0}$. Le moment d'un couple ne dépend pas du point de réduction.
> Comme son nom l'indique, un couple peut se décrire par deux forces opposées appliquées en deux points différents ([[#^figure2|fig. 2]]). C'est l'ensemble de forces le plus simple qui puisse donner un couple.

Champ de pesanteur uniforme : $\displaystyle \overrightarrow{F} = \sum_{i=1}^{N} m_i\overrightarrow{g} = M\overrightarrow{g}$ et $\displaystyle \overrightarrow{\Gamma}_A = \sum_{i=1}^{N} \overrightarrow{AP_i} \wedge m_i\overrightarrow{g} = \left(\sum_{i=1}^{N} \overrightarrow{AP_i}\right) \wedge \overrightarrow{g} = M\overrightarrow{AG} \wedge \overrightarrow{g} = \overrightarrow{AG} \wedge M\overrightarrow{g}$ avec G est le centre de masse.

> [!note] Liaison rotule
> Un solide est lié à un support par une liaison rotule si dans le référentiel du support le solide possède un seul point de vitesse constamment nulle. On note ici ce point O. Le schéma de la liaison est donné sur la [[#^figure3|figure 3]].
> - La liaison permet un mouvement de rotation quelconque autour de O ;
> - La liaison maintient le point O fixe par rapport au support.
> 
> Le support définit un référentiel $(R_S)$. Dans ce référentiel, la vitesse du point O appartenant au solide est nulle : $\overrightarrow{v}(O)_{(R_S)} = \overrightarrow{0}$. En revanche, le vecteur vitesse angulaire instantané du solide $\overrightarrow{\Omega}_{(R_S)}$ est quelconque.
> Un solide lié à un support fixe par une liaison rotule subit de la part du support des actions de liaisons. Soit $d\Sigma$ un élément de la surface de contact $(\Sigma)$ entre l'axe du solide et le support ([[#^figure4|fig. 4]]). Ces actions se décrivent par une densité surfacique $\overrightarrow{f}_s(P)$ pour les points P de la surface de contact $(\Sigma)$. Soient $\overrightarrow{F}_{rotule}$ la résultante des actions de liaison et $\overrightarrow{\Gamma}_{rotule}$ le moment des actions de liaison en O. On a :
> $$
> \begin{cases}
> \displaystyle\overrightarrow{F}_{rotule} = \iint_{(\Sigma)} \overrightarrow{f}_s(P) d\Sigma\\
> \displaystyle\overrightarrow{\Gamma}_{O\,rotule} = \iint_{(\Sigma)} \overrightarrow{OP} \wedge \overrightarrow{f}_s(P) d\Sigma
> \end{cases}
> $$
> Modèle de la liaison rotule parfaite : La liaison rotule est parfaite s'il n'y a aucun frottement entre le support et le solide. Ainsi $\text{Liaison rotule parfaite} \Leftrightarrow \overrightarrow{\Gamma}_{O\,rotule} = \overrightarrow{0}$. En revanche, on ne peut rien dire de la résultante $\overrightarrow{F}_{rotule}$ qui reste une inconnue dynamique du système. Donc, les actions d'une liaison rotule parfaite sont équivalentes à une force $\overrightarrow{F}_{rotule}$ s'appliquant en O. On peut noter la correspondance entre les résultantes et moments dans $(R_S)$ : $\{\overrightarrow{\Omega} \, \text{quelconque} \,;\, \overrightarrow{v}(O) = \overrightarrow{0}\}$ et $\{\overrightarrow{F} \, \text{quelconque} \,;\, \overrightarrow{\Gamma}_{O} = \overrightarrow{0}\}$.

> [!note] Liaison pivot
> Un solide est lié à un support par une liaison pivot s'il existe un axe $\Delta$, lié au solide, fixe dans le référentiel du support ([[#^figure5|fig. 5]]). La liaison pivot ne permet que le mouvement de rotation du solide autour de $\Delta$.
> Soit un point $O$ de l'axe $\Delta$ et un système orthogonal d'axes où $\Delta = Oz$ : $(Ox, Oy, Oz = \Delta)$. Dans le référentiel $(R_S)$ du support, le mouvement du solide est décrit par les éléments cinématiques suivants : $\{\overrightarrow{\Omega} = \Omega\overrightarrow{e}_z \,;\, \overrightarrow{v}(O) = \overrightarrow{0}\}$.
> Comme dans le cas de la liaison rotule, les actions de liaison du support sur le solide sont réparties sur la surface de contact. Soient $\overrightarrow{F}_{pivot}$ la résultante de ces actions (du support sur le solide) et $\overrightarrow{\Gamma}_{O\,pivot}$ son moment en $O$ ([[#^figure6|fig. 6]]). Ainsi $\text{Liaison pivot parfaite} \Leftrightarrow \Gamma_{Oz} = 0$. Il est important de remarquer que même dans le cas de la liaison pivot parfaite, les actions de contact ne sont pas équivalentes à une force seule appliquée en un point. En effet, on n'a pas la propriété $\overrightarrow{F}_{pivot} . \overrightarrow{\Gamma}_{O\,pivot} = \overrightarrow{0}$ dans le cas général.

> [!note] Résultante et moment à l'équilibre
> Un système matériel est à l'équilibre si tous ses points sont immobiles et restent immobiles au cours du temps.
> L'équilibre d'un système se traduit sur la résultante et le moment des actions extérieures par les relations suivantes : $\overrightarrow{F}_{ext} = \overrightarrow{0}$ et $\overrightarrow{\Gamma}_{A\,ext} = \overrightarrow{0}$.
> Le moment des actions extérieures est nul par rapport à tout point A. Il suffit de le montrer pour un point arbitrairement choisi pour qu'il soit nul pour tous les autres.
# Définitions
==**Actions extérieures**== :
Dans un référentiel galiléen, une force est dite ==**extérieure**== à un système si elle est exercée par un système matériel $(S')$ situé à l'extérieur de $(S)$. Il s'agit dans ce cas d'une force d'interaction entre les deux systèmes : $\overrightarrow{f}_{(S')\rightarrow i}$.
Dans le cas d'un référentiel non galiléen, les forces ==**d'inertie d'entraînement $\overrightarrow{f}_{ie}$ et de Coriolis $\overrightarrow{f}_{ic}$**== sont considérées comme des forces extérieures, même s'il n'existe pas de système matériel qui en serait la cause.
Les forces exercées par les systèmes extérieurs (forces d'interaction) sont invariantes par tout changement de référentiel. Les forces d'inertie dépendent du référentiel d'étude. ^484f10

==**Actions intérieures**== :
Une force est dite intérieure au système $(S)$ si elle est exercée sur un point $P_i$ du système $(S)$ par un autre point $P_j$ de ce même système. Elle est notée $\overrightarrow{f}_{j\rightarrow i}$.
L'ensemble de ces forces $\{\overrightarrow{f}_{j\rightarrow i}\}_{i = 1,\, \ldots, N \,;\, j = 1,\, \ldots, N}$ constitue les actions intérieures. Ce sont des forces d'interaction.
Cette force peut être une force d'interaction à courte portée (Van der Waals, contact, pression) ou à longue portée (interaction gravitationnelle ou électromagnétique, dont les charges et les masses sont intérieures au système). ^9ef48c

> [!note] Tension dans une corde souple
> Une corde souple est un système matériel unidimensionnel (la section est négligeable) pouvant être décrit par une courbe $(C)$ et une masse linéique $\lambda(P)$, où $P$ est un point courant de $(C)$.
> Soit $s$ une abscisse curviligne (« la longueur de la corde ») le long de $(C)$. On appelle tension et on note $\overrightarrow{T}(s)$ la force exercée en un point d'abscisse curviligne s <mark style="color: red">par la corde au-delà de s sur la partie en deçà de s</mark>. Une corde souple exerce une tension $\overrightarrow{T}$ tangente à la corde au point où elle s'applique. La tension est dirigée vers la partie de corde qui exerce la force.
> Un élément de longueur $ds$ de la corde, compris entre les abscisses curvilignes $s$ et $s + ds$, subit les actions suivantes ([[#^figure7|fig. 7]) :
> - la tension de la corde $\overrightarrow{T}(s + ds)$ exercée par la corde au-delà de $s + ds$ ;
> - la tension de la corde $-\overrightarrow{T}(s)$ exercée par la corde en deçà de $s$ ;
> - les autres forces éventuelles $d\overrightarrow{f}$ (poids, force de Laplace, forces d'inertie...).
> 
> La corde en deçà de $s$ subit la tension $\overrightarrow{T}(s)$ de la part de l'élément ds, et exerce donc sur l'élément la force de tension $-\overrightarrow{T}(s)$, d'après le principe des actions réciproques.
# Diagrammes
![[mecanique2/attachments-mecanique2/figure25.png]]^figure1

![[mecanique2/attachments-mecanique2/figure26.png]]^figure2

![[mecanique2/attachments-mecanique2/figure27.png]]^figure3

![[mecanique2/attachments-mecanique2/figure28.png]]^figure4

![[mecanique2/attachments-mecanique2/figure29.png]]^figure5

![[mecanique2/attachments-mecanique2/figure30.png]]^figure6

![[mecanique2/attachments-mecanique2/figure31.png]]^figure7
# Graphiques

# Expériences
> [!warning]
> Tous les fascicules des travaux pratiques sur le sujet de ce chapitre, que j'ai trouvé sur internet, contiennent des parties sur d'autres sujets comme l'étude dynamique ou énergétique du solide. Pour plus d'information on peut consulter les liens suivants : [lien1](https://fr.scribd.com/document/610622048/TP-Meca-Solide-ENSA-BM-Version-22-23), [lien 2](https://fr.scribd.com/document/693626507/TP-de-Mecanique-Des-Solides-Rigides-2023-2024-Pour-Etudiant) et [lien 3](http://www.fsr.ac.ma/DOC/Cours_en_ligne/Printemp/LICENCES/LF/SMA/S4/Physique%206:%20M%C3%A9canique%20Du%20Solide/TP/Polycope%20Mec%206-12-20.pdf).
# Autres notes
> [!note] Torseur dynamique
> Cette notion de torseur dynamique n'est pas abordée dans le cours ainsi que sa relation avec le principe fondamental de la dynamique. Pour plus d'information sur le sujet, on peut visiter ce [lien](https://cahier-de-prepa.fr/psi-arago/download?id=1589).
^info1

> [!note] Expression de la résultante des actions $\overrightarrow{F}$ sur des systèmes continus
> - A une dimension : $\displaystyle \overrightarrow{F} = \int_{C} \overrightarrow{f}_{\lambda}(P)dl$ avec $\overrightarrow{f}_{\lambda}$ est la densité de force linéique.
> - A deux dimensions : $\displaystyle \overrightarrow{F} = \iint_{S} \overrightarrow{f}_{s}(P)dS$ avec $\overrightarrow{f}_{s}$ est la densité de force surfacique.
> - A trois dimensions : $\displaystyle \overrightarrow{F} = \iiint_{V} \overrightarrow{f}_{v}(P)d\tau$ avec $\overrightarrow{f}_{v}$ est la densité de force volumique.

> [!warning] Exercice 3 question 1 de section savoir appliquer le cours page 101
> Le champ de pesanteur peut s’exprimer à partir du théorème de Gauss. Ce théorème s’applique au champ gravitationnel car ce dernier obéit à la même loi mathématique que le champ électrostatique créé par une charge. Alors on a : $\displaystyle \iint_{\Sigma} \overrightarrow{g}.d\overrightarrow{\Sigma} = -4\pi GM_{intérieure}$ où $\Sigma$ est une surface fermée contenant la masse $M_{intérieure}$.