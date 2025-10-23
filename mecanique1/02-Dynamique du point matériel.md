---
titre: "[[02-Dynamique du point matériel]]"
tags:
  - principe-d-inertie
  - relation-fondamentale-de-la-dynamique
  - principe-de-l-action-et-de-la-réaction
  - force
crée: 11-08-2025, 11:17
---
# Formules
Quantité de mouvement (ou impulsion) : $\overrightarrow{p}(M)_{\mathcal{R}} =m\overrightarrow{v}(M)_{\mathcal{R}}$ 

Force de pesanteur (ou poids) : $\overrightarrow{P} = m\overrightarrow{g}$  où $g \approx 9,8 \ m.s^{-2}$

Réaction d'un support : $\overrightarrow{F}_{S \rightarrow M} = \overrightarrow{R}$ 

Tension d'un fil : $\overrightarrow{F}_{S_{1} \rightarrow S_{2}} = -T \overrightarrow{t}_{12}$ ou $\overrightarrow{F}_{S_{2} \rightarrow S_{1}} = T \overrightarrow{t}_{12}$ ([[#^figure1]])

Force de rappel élastique (ou loi de Hooke) : $T = k(l - l_{0})$ où k est la constante de **raideur du ressort**. 

> [!note] Relation fondamentale de la dynamique (deuxième loi de newton) :
> $\mathcal{R}_{g}$ étant un référentiel galiléen, M un point matériel de masse m et $\mathcal{E}$ l'ensemble de l'univers à l'exception de M, les forces appliquées à M et son mouvement sont liées par la loi :
> $$\overrightarrow{F}_{\mathcal{E} \rightarrow M} = m\overrightarrow{a}(M)_{\mathcal{R}_{g}}$$
> Cette relation s'appelle aussi le théorème de la quantité de mouvement lorsqu'elle s'écrit sous cette forme :
> $$\overrightarrow{F}_{\mathcal{E} \rightarrow M} = \left(\dfrac{d\overrightarrow{p}(M)_{\mathcal{R}_{g}}}{dt}\right)_{\mathcal{R}_{g}}$$

Principe de l'action et de la réaction (troisième loi de newton) :
$\overrightarrow{F}_{M_{1} \rightarrow M_{2}} = -\overrightarrow{F}_{M_{2} \rightarrow M_{1}}$ ; $\overrightarrow{F}_{M_{1} \rightarrow M_{2}} \wedge \overrightarrow{M_{1}M_{2}} = \overrightarrow{0}$.

Équation d'évolution d'un système mécanique : $\dfrac{d\overrightarrow{v}}{dt} = \frac{\overrightarrow{f}}{m}$
> [!warning]
> A partir de cet équation, on peut obtenir la vitesse, la position et la trajectoire de phase.

> [!note] Déterminisme mécanique :
> Les systèmes mécaniques ont une évolution unique pour des conditions initiales données.

Champ des forces : $\overrightarrow{f} = m\dfrac{d\overrightarrow{v}}{dt}$
> [!warning]
> A partir de cet équation, il est possible d'analyser le champ de forces auquel est soumis le mobile en observant son mouvement.

 Force dirigée selon (Ox) subie par l'oscillateur harmonique : $f_{x} = -m\omega_{0}^{2}(x-x_{e})$ [[#^figure2]]
 > [!note]
 > Cet équation peut être déduite de l'équation d'évolution : $\dfrac{d^{2}x}{dt^{2}} = -\omega_{0}^{2}(x-x_{e})$
# Définitions
==**Point matériel**== :
un objet ponctuel dont le repérage ne nécessite que la connaissance des trois coordonnées de sa position.
> [!warning]
> Le modèle du point matériel n'est pas toujours valide. La validité de cette modélisation ne dépend pas de la taille du solide, mais de sa nature, de son environnement et des hypothèses simplificatrices.

==**Inertie**== :  La résistance à toute variation de vitesse.
> [!note]
> Pour un point matériel, la propriété d'inertie est représentée par un scalaire positif appelé <mark style="color: red">masse</mark>.
> Plus la masse d'un point matériel est grande, plus il est difficile de modifier sa vitesse.
> La masse est invariante dans le temps et ne dépend pas du référentiel. C'est une caractéristique intrinsèque du point matériel.

> [!note] Principe d'inertie (première loi de Newton) :
> Il existe une classe de référentiels, appelés référentiels galiléens, par rapport auxquels un point matériel *isolé* (n'est soumis à aucune action mécanique) est en mouvement rectiligne uniforme.
> Dans la plupart des expériences courantes, le référentiel terrestre, lié à la surface de la Terre, peut être considéré comme galiléen.

> [!warning]
> Un point matériel isolé est une abstraction irréalisable, mais il se peut que les actions mécaniques se compensent exactement. Le point matériel est alors dit *pseudo-isolé* et il est possible de lui appliquer le principe d'inertie.

> [!note] Existence des liaisons : 
> La position d'un point matériel totalement libre est fonction de ses trois coordonnées, indépendantes entre elles. Nous dirons qu'un tel point matériel possède trois <mark style="color: red">degrés de liberté</mark>.
> Ce nombre est réduit s'il est imposé au point matériel de se déplacer sur une surface (deux <mark style="color: red">degrés de liberté</mark>) ou sur une courbe (un seul <mark style="color: red">degré de liberté</mark>).

> [!note] Réaction d'un support : 
> Le point matériel M est contraint de se déplacer sur un support S. Le support impose une trajectoire au point M ; pour cela, il exerce sur M une <mark style="color: red">force de liaison</mark> appelée « réaction du support ».
> La liaison est dite **unilatérale** si l'objet modélisé par le point matériel M est simplement posé sur la surface S. Le support repousse M, mais ne peut l'attirer.
> $\overrightarrow{n}$ étant le vecteur unitaire normal au support en M, cela se traduit par : $\overrightarrow{R}.\overrightarrow{n} \geqslant 0$.
> $\overrightarrow{R}$ est la somme d'une composante normale à S : $\overrightarrow{R_{\perp}}$ , et d'une composante tangentielle à S : $\overrightarrow{R_{\parallel}}$.
> La liaison est sans frottements si $\overrightarrow{R_{\parallel}} = \overrightarrow{0}$.

> [!note] Fil idéal :
> Un fil est idéal si sa masse est nulle (en fait négligeable) et s'il est parfaitement souple (sans raideur).
> S'il est tendu, seul dans l'espace, nous admettrons qu'il est rectiligne et que sa tension est uniforme (c'est-à-dire identique en tout point).
> Deux fils idéaux mis bout à bout et tendus sont équivalents à un fil unique et ont même tension.

> [!note] Poulie idéale :
> Une poulie est idéale s'il est possible de négliger son inertie et les frottements consécutifs à sa rotation.
> Nous admettrons qu'un fil idéal enroulé sur une poulie idéale conserve une tension uniforme.

==**Élasticité**== : C'est la propriété de certains matériaux de reprendre leur forme initiale après une déformation.

> [!note] Ressort idéal :
> Un ressort est idéal s'il est linéaire (c-à-d la déformation est supposée proportionnelle à sa cause) de masse négligeable. Cette dernière condition implique que la tension est uniforme.

> [!note] Principe des actions réciproques (troisième loi de Newton) :
> Soit deux points matériels $M_{1}$ et $M_{2}$ en interaction, en mouvement ou immobiles. Les forces d'interaction $\overrightarrow{F}_{M_{1} \rightarrow M_{2}}$ et $\overrightarrow{F}_{M_{2} \rightarrow M_{1}}$ sont opposées et colinéaires à l'axe ($M_{1}M_{2}$).

==**Système libre (ou autonome)**== : 
Le système étudié est libre lorsque les actions qu'il subit ne dépendent pas explicitement du temps : $f = f(x , v_{x})$.
Pour un système autonome, la nature des trajectoires de phase est donc une caractéristique du champ de forces dans lequel le point matériel évolue.
> [!note]
> Pour un système autonome, deux trajectoires de phase ne se coupent jamais.
# Diagrammes
Force de tension :
![[mecanique1/attachments-mecanique1/figure13.png]]^figure1
> [!note]
> Un fil souple tendu se sépare en deux parties $S_{1}$ et $S_{2}$ s'il est coupé en un point P. Il existe donc une force qui assure en chaque point la cohésion du fil.
> Si le fil est tendu, la tension T est positive.
> La tension T est relative à un point et, dans le cas général, varie le long du fil.
# Graphiques
Sens de parcours sur la trajectoire de phase :
![[mecanique1/attachments-mecanique1/figure14.png]]^figure2
# Expériences
## Détermination de l'accélération terrestre
> [!warning]
> Ce TP n'est pas dans le livre mais se trouve [en ligne](https://www.ummto.dz/fs/wp-content/uploads/2019/09/Ouvrir-Ici-.pdf).

### Détermination de g à partir de la période du pendule simple
![[mecanique1/attachments-mecanique1/figure15.png]]
Il faut procéder comme suit :
- Écarter le pendule simple de sa position d'équilibre (quelques degrés).
- A l'aide du chronomètre, déterminer la durée $t_1$ de 20 oscillations pour longueur du fil $l_1 = 100 \ cm$.
- Refaire les mêmes mesures en utilisant un pendule de longueur $l_2 = 75 \ cm$, puis un pendule de longueur $l_3 = 50 \ cm$.
- Compléter le tableau suivant en utilisant la formule $g = 4\pi^{2}\frac{1}{T^{2}}$ et en faisant un calcul d'erreurs sur g.
>[!warning]
>La formule de g est obtenue à l'aide de théorème du moment cinétique à voir dans la note [[06-Théorème du moment cinétique]].

![[mecanique1/attachments-mecanique1/figure16.png]]

### Détermination de g à partir de la chute libre
![[mecanique1/attachments-mecanique1/figure17.png]]
Ce dispositif permet de mesurer le temps de chute d'une bille emprisonnée puis libérée par un déclencheur. Cette mesure du temps est effectuée à l'aide d'un compteur digital relié au déclencheur (qui l'actionne au départ de la bille) et au réceptacle, qui arrête le compteur dés que la bille tombe sur l'assiette du réceptacle.
Il faut procéder comme suit :
- Pour différentes hauteurs du déclencheur supportant la bille métallique (à faire varier de 60 cm à 20 cm, par pas de 5 cm), déterminer le temps de chute donné par le compteur digital électronique.
- Dresser le tableau de mesures $z = f(t)$ et $z = f(t^2)$.
- Tracer alors les graphes caractéristiques $z = f(t)$ et $z = f(t^2)$. En déduire l'accélération de la pesanteur g à partir de la pente du droite d'équation $z = f(t^2)$.
- Comparer les résultats de g obtenus par les 2 méthodes. Quelle méthode convient le mieux?
# Autres notes
==**Point attracteur**== : 
Le système est toujours rappelé ("attiré") vers cette position.

==**points de rebroussement**== :
Pour un degré de liberté x, à ces points, la trajectoire de phase coupe l'axe (Ox). En ces points, la vitesse de système s'annule et change de signe. Nous voyons qu'en ces points, le système rebrousse chemin.
> [!note]
> Pour certains systèmes, la force, et donc l'accélération, pourrait s'annuler en ces points. Autrement dit : le système vient s'arrêter en ces points, qui ne sont plus des points de rebroussement mais des points d'arrêt.

> [!note] Validité de modèle du point matériel :
> Ce modèle est valable si les dimensions du corps physique sont faibles par rapport à la distance d'observation (de celui qui observe le mouvement).
> Par exemple, la navette spatiale peut-être assimilée à un point matériel pour un observateur terrestre mais pas pour son commandant de bord. En effet pour ce dernier, la navette a des dimensions spatiales, elle peut tourner sur elle-même etc…