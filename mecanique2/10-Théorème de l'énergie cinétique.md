---
titre: "[[10-Théorème de l'énergie cinétique]]"
tags:
  - énergie-cinétique
  - énergie-potentielle
  - énergie-mécanique
  - puissance
crée: 28-10-2025, 09:58
---
# Formules
Théorème de l'énergie cinétique pour un système fermé de points matériels : $E_c(t') - E_c(t) = W_{int} + W_{ext}$.

Théorème de la puissance cinétique pour un système fermé de points matériels : $\dfrac{dE_c}{dt} = P_{int} + P_{ext}$. Dans un référentiel non galiléen, le théorème de la puissance cinétique s'applique pourvu que l'on prenne en compte la puissance des forces d'inertie d'entraînement. Cependant, la puissance des forces d'inertie de Coriolis est nulle. Par ailleurs, la puissance des actions d'entraînement est nulle dans le référentiel barycentrique.

> [!note] Puissance des actions intérieures pour un système fermé de points matériels
> L'expression de la puissance des actions intérieures, $\displaystyle \sum_{i=1}^{N} \sum_{j=1}^{i-1} \overrightarrow{F}_{j \rightarrow i}\, . (\overrightarrow{v}_i - \overrightarrow{v}_j)$, est indépendante du référentiel considéré. On peut noter que la puissance des actions intérieures s'écrit $\displaystyle \sum_{i=1}^{N} \sum_{j=1}^{i-1} F_{j \rightarrow i}\, . \dfrac{dr_{ij}}{dt}$ où $F_{j \rightarrow i}$ désigne la projection de $\overrightarrow{F}_{j \rightarrow i}$ sur $\overrightarrow{u}_{i,j} = \frac{\overrightarrow{P_iP_j}}{\left\lVert \overrightarrow{P_iP_j} \right\rVert}$ et $r_{ij} = \left\lVert \overrightarrow{P_iP_j} \right\rVert$.

> [!note] Théorème de l'énergie cinétique appliqué à un solide
> Un solide est défini comme un système matériel indéformable. Il en résulte que la puissance des actions intérieures est nulle, puisque $dr_{ij} = 0$ pour tout couple de points matériels $P_i$, $P_j$ appartenant au solide.
> Ainsi, lorsque le système considéré est constitué d'un seul solide, la variation d'énergie cinétique entre deux instants est égale au travail des actions extérieures entre ces deux instants.

> [!note] Puissance des actions extérieures pour un solide
> La puissance des actions extérieures exercées sur le solide a pour expression (la même que celle définie au [[07-Les travaux des actions sur un système – Énergie potentielle|chapitre 7]]) : $P_{ext} = \overrightarrow{F}\,.\overrightarrow{v}(A,t) + \overrightarrow{\Omega}(t) . \overrightarrow{\Gamma}_A$.
> Lorsque les actions extérieures sont décrites par un glisseur, c'est-à-dire par un torseur de moment nul en un point, noté $A$, la puissance des actions associées au glisseur est alors égale à $\overrightarrow{F}\,.\overrightarrow{v}(A)$ où $\overrightarrow{F}$ est la résultante des actions extérieures. La puissance d'un glisseur est donc équivalente à celle d'une force unique appliquée en $A$.
> Lorsque les actions extérieures sont décrites par un couple, c'est-à-dire un torseur de résultante nulle, donc de moment identique en tout point, la puissance des actions extérieures ne fait intervenir que la composante de rotation du mouvement du solide. Considérons un système en rotation à la vitesse angulaire $\Omega$ autour d'un axe $\Delta$ passant par $A$. La puissance des actions extérieures est alors égale à $\Gamma_{\Delta}\Omega$ où $\Gamma_{\Delta}$ est la projection du moment en $A$ sur $\Delta$.
> Lorsque le solide de centre d'inertie $G$ est en translation, la puissance des actions extérieures a pour expression : $P_{ext} = \overrightarrow{F}\,.\overrightarrow{v}(G)$.
> Considérons un solide en rotation. Soit $A$ un point de l'axe $\Delta$ autour duquel le solide est en rotation. La puissance des actions extérieures est égale à : $P_{ext} = \overrightarrow{\Gamma}_A\,.\overrightarrow{\Omega} = \Gamma_{\Delta}\Omega$.

> [!note] Application du théorème de l'énergie cinétique pour un système de solides
> Alors que le théorème des actions réciproques indique que la somme des actions mécaniques entre les différents solides d'un système de solides est nulle, la puissance des actions mécaniques intérieures peut a priori être non nulle.
> La variation par unité de temps de l'énergie cinétique d'un <mark style="color: red">système de solides</mark> est égale à la somme de la puissance des actions extérieures et de celle des actions intérieures : $\displaystyle \dfrac{dE_c}{dt} = P_{ext} + \sum_{i=1}^{N} \sum_{\substack{j=1\\j \neq i}}^{N} P_{int[i \rightarrow j]}$ où $P_{int[i \rightarrow j]}$ est la puissance des actions mécaniques (intérieures) exercées par le solide $i$ sur le solide $j$.

> [!note] Glissement d'un solide sur un autre
> Un solide glisse sur une surface plane immobile dans le référentiel galiléen d'étude. Tous les points du solide ont la même vitesse que $G$, son centre d'inertie. Comme nous le verrons dans [[11-Actions de contact|le chapitre consacré aux actions de contact]], ces dernières sont décrites par un torseur de résultante $\overrightarrow{T} + \overrightarrow{N}$. La puissance des actions de contact exercées par le support sur le solide est égale à $\overrightarrow{T} ⋅ \overrightarrow{v}(G)$. Celle des actions de contact du solide sur le support, fixe, est nulle. La puissance des actions intérieures du système {solide + support} vaut ainsi $\overrightarrow{T} ⋅ \overrightarrow{v}(G)$ : elle est non nulle. D'après les lois de Coulomb, que nous énoncerons dans un  [[11-Actions de contact|chapitre ultérieur]], cette puissance est négative.

> [!note] Roulement d'un solide sur un autre
> Considérons deux solides $\Sigma_1$ sur $\Sigma_2$ en contact au point $I$. Les actions de contact se réduisent à un glisseur de moment nul en $I$. La puissance des actions de contact est égale au produit scalaire de la résultante des actions de contact et de la vitesse de glissement : $P_{contact} = \overrightarrow{T} . \overrightarrow{v}_g$.
> En cas de glissement, cette puissance est négative.
> <mark style="color: red">En l'absence de glissement, la puissance des actions de contact est nulle.</mark>.

> [!note] Définition énergétique d'une liaison parfaite
> <mark style="color: red">La puissance des actions de contact d'une liaison surfacique parfaite (il n'y a aucun frottement) est nulle</mark>. Considérons trois liaisons particulières :![[mecanique2/attachments-mecanique2/figure34.png]]
> Pour mettre à profit une hypothèse de liaison pivot parfaite, il est utile d'inclure l'axe dans le système dont on réalise l'étude énergétique.

> [!note] Action mécanique conservative et énergie potentielle
> Un solide est soumis à des actions mécaniques extérieures de résultante $\overrightarrow{F}$ et de moment $\overrightarrow{\Gamma}_O$ en $O$. Le travail fourni pour un déplacement élémentaire de translation $d\overrightarrow{G}$ et de rotation $d\theta\overrightarrow{e}_z$ est égal à : $\delta W = \overrightarrow{F} . d\overrightarrow{G} + \overrightarrow{\Gamma}_O . d\theta\overrightarrow{e}_z$.
> Si le travail entre deux points quelconques $A$ et $B$ est indépendant du chemin suivi, on peut définir une énergie potentielle dont dérivent les actions extérieures. On a alors pour tout déplacement élémentaire : $\delta W = -dE_p$.
> Une action mécanique est <mark style="color: red">conservative</mark> si elle dérive d'une énergie potentielle.
> Ainsi, dans un champ de pesanteur uniforme, le poids d'un système matériel de masse $M$ dérive d'une énergie potentielle de pesanteur $E_p = Mgz_G$ où $z_G$ désigne la position sur un axe vertical ascendant du centre d'inertie du système.
> Considérons un solide relié à un fil de torsion exerçant un couple $\Gamma \overrightarrow{e}_z$. La position du solide est repérée par un angle $\theta$. On suppose que le couple a un moment $\Gamma = – C\theta$ (couple de rappel). Cette action extérieure dérive alors de l'énergie potentielle : $E_p = \frac{1}{2}C\theta^{2}$.
> Il faut noter qu'une énergie potentielle est définie à une constante additive près.

> [!note] Énergie mécanique
> On appelle énergie mécanique la somme de l'énergie cinétique et de l'énergie potentielle de toutes les actions mécaniques conservatives.
> L'énergie mécanique d'un système est conservée si le système n'est soumis qu'à des actions mécaniques conservatives ou si les actions mécaniques non conservatives ne travaillent pas. En effet, on a alors, au cours d'une évolution élémentaire pendant la durée dt :
> $$
> \begin{align*}
> dE_m &= d(E_c + E_p)\\
> &= \delta W + dE_p\\
> &= 0
> \end{align*}
> $$
> Un système soumis à des actions mécaniques conservatives ou qui ne travaillent pas est dit <mark style="color: red">conservatif</mark>. Son énergie mécanique est conservée. L'énergie mécanique est alors une <mark style="color: red">intégrale première</mark> du mouvement.
# Définitions

# Diagrammes

# Graphiques

# Expériences
## Étude du volant de Maxwell
> [!warning]
> Ce TP n'est pas dans le livre mais se trouve dans les liens suivants : [lien 1](http://www.fsr.ac.ma/DOC/Cours_en_ligne/Printemp/LICENCES/LF/SMA/S4/Physique%206:%20M%C3%A9canique%20Du%20Solide/TP/Polycope%20Mec%206-12-20.pdf) page 26, [lien 2](https://www.ummto.dz/fs/wp-content/uploads/2019/09/Ouvrir-Ici-.pdf) page 36.

![[mecanique2/attachments-mecanique2/figure35.png]]
### Détermination du moment d'inertie de la roue de Maxwell
Afin de déterminer le moment d'inertie de la roue de Maxwell (sa masse étant de 0.436 kg), on étudie le chemin parcouru par le centre de gravité de la roue de Maxwell en fonction du temps. Pour ce faire, on varie la hauteur de chute séparant le point de départ de la roue du faisceau lumineux de la barrière lumineuse à fourchette, en déplaçant la barrière sur la tige (la hauteur est lue sur la règle graduée). Le rayon r de l'axe est r = 2.5 millimètres.
- Remplir le tableau (I) suivant :![[mecanique2/attachments-mecanique2/figure36.png]]
- Tracer le graphe $z=f(t)$ et le graphe $z=g(t^{2})$.
- A partir de ce $2^{ème}$ graphe et en utilisant la relation entre $z$ et $t^{2}$ de la théorie (obtenu en dérivant par rapport au temps l'expression de l'énergie mécanique conservée suivante : $E = -mgz(t) + \frac{1}{2}mv^{2}(t) + \frac{1}{2}\frac{J}{r^{2}}v^{2}(t)$), déterminer le moment d'inertie de la roue de Maxwell.
### Énergie potentielle
- En utilisant le tableau (I), tracer le graphe donnant l'énergie potentielle $E_p$ en fonction du temps : $E_p(t)=mgz(t)$.
### Vitesse instantanée de la roue de Maxwell
![[mecanique2/attachments-mecanique2/figure37.png]]
Pour déterminer la vitesse instantanée de la roue, il suffit de brancher le compteur en porte électronique (il faut alors shunter les douilles start-stop, jaune-jaune et blanc-blanc). Il faut veiller à ce que le circuit réagisse lors du passage du sombre au clair ; pour cela, on doit actionner le bouton Start-Invert.
La vitesse est obtenue en faisant : $v(t+\frac{\Delta t}{2}) = \frac{\Delta z}{\Delta t}$.
- Remplir le tableau (II) suivant :![[mecanique2/attachments-mecanique2/figure38.png]]
- Tracer le graphe $v=f(t)$.
### Énergie cinétique de translation
- En utilisant le tableau (II), tracer le graphe donnant l'énergie cinétique de translation $E_{CT}$ en fonction du temps : $E_{CT} = \frac{1}{2}mv^{2}(t)$.
### Énergie cinétique de rotation
- En utilisant le tableau (II) et la relation $v = \omega r$, tracer le graphe donnant l'énergie cinétique de rotation $E_{CR}$ en fonction du temps : $E_{CR} = \frac{1}{2}J\omega^{2}(t)$. Utiliser pour $J$ la valeur trouvée expérimentalement.
### Conclusion
- Quelle est la conclusion que vous déduisez en comparant les 3 tracés de graphes $E_P(t)$, $E_{CT}(t)$ et $E_{CR}(t)$?
# Autres notes
