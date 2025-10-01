---
titre: "[[01-Cinématique]]"
tags:
  - position
  - vitesse
  - accélération
crée: 08-08-2025, 17:08
---
# Formules
**Vecteur position en coordonnées cartésiennes** :  $\overrightarrow{r} = \overrightarrow{OM} = x\overrightarrow{e_{x}} + y\overrightarrow{e_{y}} + z\overrightarrow{e_{z}}$

**Vecteur position en coordonnées cylindriques** :  $\overrightarrow{OM} = r\overrightarrow{e_{r}} + z\overrightarrow{e_{z}}$  ([[#^figure2]])

**Relations entre les coordonnées cylindriques et cartésiennes** : $\overrightarrow{e_r} = \cos\theta\overrightarrow{e_x} + \sin\theta\overrightarrow{e_y}$ ; $\overrightarrow{e_\theta} = -\sin\theta\overrightarrow{e_x} + \cos\theta\overrightarrow{e_y}$ ; $x = r\cos\theta$ ; $y = r\sin\theta$ ; $r = \sqrt{x^{2} + y^{2}}$.

**Vecteur position en coordonnées sphériques** :  $\overrightarrow{OM} = r\overrightarrow{e_{r}}$  ([[#^figure3]])

> [!note]
> La dérivée d'une grandeur vectorielle dépend du référentiel.

> [!note]
> La dérivation de produit entre un scalaire et un vecteur, de produit scalaire et de <mark style="color: red">produit vectoriel</mark> se fait comme la dérivation entre deux fonctions.

> [!warning]
>  Un vecteur de norme constante n'est pas pour autant constant, car son orientation peut varier.

> [!note]
> La dérivée d'un vecteur de norme constante est orthogonale à ce vecteur ou nulle. C'est le cas des vecteurs unitaires.

En coordonnées cylindriques, les vecteurs de la base locale dépendent de $\theta$ : $\displaystyle \left(\dfrac{d\overrightarrow{e_r}}{d\theta}\right)_{\hspace{-0.5em}/\mathcal{R}} = \overrightarrow{e_\theta}$ et $\left(\dfrac{d\overrightarrow{e_\theta}}{d\theta}\right)_{\hspace{-0.5em}/\mathcal{R}} = -\overrightarrow{e_r}$

**Vecteur vitesse en coordonnées cartésiennes** : $\overrightarrow{v}(M)_{\mathcal{R}} = \dot{x}\overrightarrow{e_{x}} + \dot{y}\overrightarrow{e_{y}} + \dot{z}\overrightarrow{e_{z}}$

**Vecteur vitesse en coordonnées cylindriques** : $\overrightarrow{v}(M)_{\mathcal{R}} = \dot{r}\overrightarrow{e_{r}} + r\dot{\theta}\overrightarrow{e_{\theta}} + \dot{z}\overrightarrow{e_{z}}$
> [!warning]
> Le terme $r\dot{\theta}\overrightarrow{e_{\theta}}$ vient du fait que $\overrightarrow{e_{r}}$ est fonction de $\theta$, et $\theta$ est fonction du temps.

> [!note]
> Le vecteur vitesse de M est égal à la somme des vecteurs vitesse que l'on obtient en ne faisant varier successivement qu'une seule de ses coordonnées. Cette propriété ne sera pas applicable à l'accélération.
> Exemple : composition des vitesses en coordonnées cylindriques
> - Si r varie seul, le mobile décrit une droite, soit : $\overrightarrow{v}(M)_{\mathcal{R}} = \overrightarrow{v}_{r} = \dot{r}\overrightarrow{e_{r}}$
> - Si $\theta$ varie seul, le mobile décrit un cercle avec la vitesse $r\dot{\theta}$ orientée selon $\overrightarrow{e_{\theta}}$, soit : $\overrightarrow{v}(M)_{\mathcal{R}} = \overrightarrow{v}_{\theta} = r\dot{\theta}\overrightarrow{e_{\theta}}$
> -  Si z varie seul, le mobile décrit une droite, soit : $\overrightarrow{v}(M)_{\mathcal{R}} = \overrightarrow{v}_{z} = \dot{z}\overrightarrow{e_{z}}$
> L'expression générale du vecteur vitesse permet de vérifier que : $\overrightarrow{v}(M)_{\mathcal{R}} = \overrightarrow{v}_{r} + \overrightarrow{v}_{\theta} + \overrightarrow{v}_{z}$

> [!warning]
> Seul un mouvement à la fois rectiligne et uniforme est non accéléré. Un mouvement uniforme (vitesse constante), mais non rectiligne est accéléré, car la direction du vecteur vitesse est variable.

**Vecteur accélération en coordonnées cartésiennes** : $\overrightarrow{a}(M)_{\mathcal{R}} = \ddot{x}\overrightarrow{e_{x}} + \ddot{y}\overrightarrow{e_{y}} + \ddot{z}\overrightarrow{e_{z}}$

**Vecteur accélération en coordonnées cylindriques** : $\overrightarrow{a}(M)_{\mathcal{R}} = (\ddot{r} - r\dot{\theta}^{2})\overrightarrow{e_{r}} + (r\ddot{\theta} + 2\dot{r}\dot{\theta})\overrightarrow{e_{\theta}} + \ddot{z}\overrightarrow{e_{z}}$

> [!warning]
> L'orientation de $\overrightarrow a$ pointe en permanence dans la concavité de la trajectoire.

> [!note]
> Pour un mouvement circulaire de centre $O$ et rayon $R$, nous avons, en coordonnées polaires : $\overrightarrow{v}(M)_{/\mathcal{R}} = R\dot{\theta}\overrightarrow{e_\theta}$ et $\overrightarrow{a}(M)_{/\mathcal{R}} = -R\dot{\theta}^{2}\overrightarrow{e_r} + R\ddot{\theta}\overrightarrow{e_\theta}$.
> Dans les cas du mouvement circulaire uniforme : $v = R\dot{\theta} = cte$ et $\overrightarrow{a}(M)_{/\mathcal{R}} = -R\dot{\theta}^{2}\overrightarrow{e_r} = -\frac{v^{2}}{R}\overrightarrow{e_r}$.

Équation de la trajectoire de phase du mobile en mouvement uniformément accéléré : $x = x_{0} + \frac{1}{2a}(v^{2} - v_{0}^{2})$ [[#^figure7]] 

Équation de la trajectoire de phase du mobile en mouvement oscillant : $(x - x_{e})^{2} + \left(\frac{v}{\omega_{0}}\right)^{2} = A^{2}$[[#^figure8]]
# Définitions
> [!note]
> En mécanique classique, le mouvement observé dépend de l'observateur. Par postulat, la durée des événements n'en dépend pas.

==**Référentiel d'observation**== :
L'ensemble rigide des points fixes pour un observateur, associé à une horloge, est par définition le référentiel de cet observateur

==**Trajectoire dans un référentiel**== :
$\mathcal{R}$ étant un référentiel et M un point mobile, il existe à chaque instant un point fixe de $\mathcal{R}$ dont la position coïncide avec celle de M. L'ensemble de ces points coïncidents forme dans une ligne continue appelée la trajectoire de M.
> [!note]
> La trajectoire n'est définie que pour un référentiel déterminé.

==**Espace des positions, trajectoire**== :
La trajectoire est constituée par l'ensemble des positions successives $\overrightarrow{OM}(t)$ du point mobile M étudié. Le vecteur vitesse est tangent à la trajectoire en chacun de ses points ([[#^figure4]]).

==**Espace des vitesses, hodographe**== :
L'hodographe du mouvement est constitué par l'ensemble des positions du point N défini
par : $\overrightarrow{ON} = \overrightarrow{v}(M)_{\mathcal{R}}$. L'accélération, qui peut être qualifiée de « vitesse de la vitesse », est tangente à l'hodographe en chacun de ses points ([[#^figure5]]). 
> [!warning]
> La courbe de la vitesse en fonction du temps est appelée elle aussi hodographe du mouvement.

==**Espace des phases, trajectoire de phase**== :
La trajectoire de phase est constituée par l'ensemble des des positions successives $\overrightarrow{OP} = (\overrightarrow{r} , \overrightarrow{v})$. Le point P est appelé ==point de phase== du système. Par souci de simplicité,  nous restreindrons les représentations des trajectoires de phase pour des systèmes à un degré de liberté, noté x. La trajectoire de phase est alors une courbe que nous tracerons dans le ==plan de phase== (O ; x , $v_{x}$) ([[#^figure6]]).
> [!note]
> Une trajectoire de phase fermée est la signature d'un mouvement périodique (elle est décrite en tournant dans le sens des aiguilles d'une montre).
# Diagrammes
![[mecanique1/attachments-mecanique1/figure1.png]]
> [!note]
> Pratiquement, retenons qu'une base orthonormée est directe s'il est possible de superposer les vecteurs $e_{1}$ , $e_{2}$ et $e_{3}$ respectivement au pouce, à l'index et au majeur de la main droite.
# Graphiques
Coordonnées cylindriques :
![[mecanique1/attachments-mecanique1/figure2.png]] ^figure2

Coordonnées sphériques :
![[mecanique1/attachments-mecanique1/figure3.png]]^figure3

Trajectoire dans l'espace des positions :
![[mecanique1/attachments-mecanique1/figure4.png]]^figure4

Hodographe dans l'espace des vitesses $\overrightarrow{ON}_{i} = \overrightarrow{v}_{i}$ :
![[mecanique1/attachments-mecanique1/figure5.png]]^figure5

Orientation des trajectoires dans le plan de phase :
![[figure6.png]]^figure6
Dans le demi-plan de phase $v_{x} > 0$ , l'abscisse x augmente lorsque le temps t croît, et dans le demi-plan $v_{x} < 0$, celle-ci diminue. Ceci nous permet de prévoir une orientation qualitative simple des trajectoires de phase dans ces deux demi-plans.

Trajectoires de phase pour des mouvements uniformément accélérés :
![[figure7.png]]^figure7
Ces trajectoires de phase, qui  décrivent une branche de parabole, sont obtenues pour les conditions initiales suivantes : $x_{0} = 0$ et $v_{0} = 0$ dans le cas ➀, $v_{0} = 0$ mais $x_{0} > 0$ pour le cas ➁, $x_{0} > 0$ et $v_{0} > 0$ pour le cas ➂, et enfin $x_{0} < 0$ et $x_{0} < 0$ dans le cas ➃.

Portrait de phase d'un oscillateur harmonique :
![[figure8.png]]^figure8
# Expériences
## Etude d'un mouvement rectiligne
> [!warning]
> Ce TP n'est pas dans le livre mais se trouve [en ligne](https://www.ummto.dz/fs/wp-content/uploads/2019/09/Ouvrir-Ici-.pdf). 

![[figure9.png]]
Il faut procéder comme suit :
- faites coulisser la bande de papier à l'intérieur de l'enregistreur sous le marteau et attachez-la au chariot à l'aide du ruban adhésif ;
- placez le chariot maintenu immobile prés de l'enregistreur ; mettez en marche l'enregistreur en le branchant à la source, puis lâchez le chariot (un étudiant du binôme doit se tenir prêt à recueillir le chariot en fin de parcours pour éviter sa chute). Le mouvement de chariot est ainsi enregistré ;
- tracer d'abord le graphe x(t) de la position du mobile par rapport à la position initiale en fonction du temps ;![[figure10.png]]
- pour déterminer la vitesse en fonction du temps :
	- soit mesurer la pente de la tangente au graphe x(t) à chaque instant;
	- soit mesurer la vitesse moyenne $V_{m} = \Delta x / \Delta t$ sur un certain intervalle de temps, puis l'assimiler à la vitesse instantanée au centre de l'intervalle.
- tracer le graphe v(t) de la vitesse instantanée en fonction du temps ;
- à partir du graphe v(t), tracer le graphe de l'accélération en fonction du temps ;
- écrire alors l'équation du mouvement du chariot et en préciser sa nature.
## Etude d'un mouvement circulaire
> [!warning]
> Ce TP n'est pas dans le livre mais se trouve [en ligne](https://fr.scribd.com/document/323990738/Polycopie-TP-Mecanique). 

![[figure11.png]]
La manipulation à faire est la suivante :
- un mobile se déplaçant sur une table horizontale à coussin d'air pour minimiser les frottements. Il est maintenu par un fil inextensible à un point fixe puis lancé perpendiculairement au rayon joignant l'origine au centre. L'enregistrement du mouvement de ce mobile peut se faire par l'enregistrement d'une vidéo avec une camera (webcam) placée en haut en aplomb de la table pour ensuite en tirer les positions avec un logiciel spécialisé à intervalles de temps réguliers $\Delta t$ ;
- à partir des positions, on doit tracer les vecteurs déplacements et déduire les vitesses puis tracer les vecteurs vitesses correspondants en un point sur deux ($M_{1}$, $M_{3}$,...) avec un choix de l'échelle. A partir de ces vecteurs vitesses, on doit ensuite tracer les vecteurs accélérations avec la même procédure basée sur l'approximation centrale, voir figure ci-dessous pour la construction géométrique ;![[figure12.png]]
- mesurer les angles $\theta(t)$ et la dérivée $\frac{d\theta}{dt}$.
# Autres notes
Les limites de la mécanique classique : 
- La mécanique classique ne permet pas d'expliquer et de prévoir les mouvements des très petits systèmes matériels, à l'échelle atomique.
- Elle postule que le repère de temps est le même pour tous les référentiels et que le temps s'écoule de la même manière dans des référentiels en mouvement les uns par rapport aux autres. Ce principe d'universalité du temps n'est plus applicable dans le cadre de la mécanique relativiste.

==**portrait de phase**== :
L'ensemble des trajectoires de phase (pour différentes conditions initiales du mouvement) constitue le portrait de phase.

> [!warning] Coordonnées sphériques
> Ce n'est pas obligatoire de retenir par cœur l'expression de l'accélération en coordonnées sphériques mais il faut savoir celle de la vitesse et comment passer des coordonnées sphériques au coordonnées cartésiennes.
> On a $\overrightarrow{OM} = r\overrightarrow{e_{r}} \Rightarrow \overrightarrow{v} = \dot{r}\overrightarrow{e_{r}} + r\dot{\overrightarrow{e_{r}}}$
> Or $\overrightarrow{e_{r}} = \sin\theta\cos\varphi \overrightarrow{e_{x}} + \sin\theta\sin\varphi\overrightarrow{e_{y}} + \cos\theta\overrightarrow{e_{z}}$
> Alors $\dot{\overrightarrow{e_{r}}} = \dot{\varphi}\sin\theta(-\sin\varphi\overrightarrow{e_{x}} + \cos\varphi\overrightarrow{e_{y}}) + \dot{\theta}(\cos\theta\cos\varphi\overrightarrow{e_{x}} + \cos\theta\sin\varphi\overrightarrow{e_{y}} - \sin\theta\overrightarrow{e_{z}})$
> D'où $\dot{\overrightarrow{e_{r}}} = \dot{\varphi}\sin\theta\overrightarrow{e_{\varphi}} + \dot{\theta}\overrightarrow{e_{\theta}}$
> Enfin ==**$\overrightarrow{v} = \dot{r}\overrightarrow{e_{r}} + r\dot{\theta}\overrightarrow{e_{\theta}} + r\dot{\varphi}\sin\theta\overrightarrow{e_{\varphi}}$**==. Pour voir une autre démonstration pour la vitesse en coordonnées sphériques, on peut consulter l'application 1 page 176.
> Voici quelques liens sur le sujet : [lien 1](https://mathworld.wolfram.com/SphericalCoordinates.html), [lien 2](http://gerald.philippe.free.fr/files/2010/MECPTQ_01%20Vitesse%20et%20acceleration%20en%20coordonnees%20spheriques.pdf), [lien 3](https://en.wikipedia.org/wiki/Spherical_coordinate_system#cite_note-Cameron2019-9), [lien 4](http://webetab.ac-bordeaux.fr/Etablissement/BDBorn/sections/postbac/prepasciences/physique/telech/docs20089/M8_2008-2009.pdf).