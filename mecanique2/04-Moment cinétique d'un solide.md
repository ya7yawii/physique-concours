---
titre: "[[04-Moment cinétique d'un solide]]"
tags:
  - moment-cinétique
  - moment-d-inertie
  - théorème-d-Huygens
crée: 07-10-2025, 10:28
---
# Formules
> [!warning]
> Rappelons que le mouvement de rotation autour d'un axe de rotation de direction fixe se rapporte à l'étude d'un mouvement de rotation autour d'un axe fixe dans le référentiel barycentrique.

Moment d'inertie d'un système par rapport à un axe : $\displaystyle J_{\Delta} = \sum_{i=1}^{N} m_id_{i}^{2}$ où $d_i$ est la distance entre le point matériel $P_i$ de masse $m_i$ et l'axe $\Delta$. $J_{\Delta}$ dépend de la répartition de masse du solide et de l'axe $\Delta$. Le moment d'inertie s'exprime en $kg.m^{2}$.

> [!note] Théorème d'Huygens
> Soit G le centre de masse d'un système matériel ([[#^figure1]]) dont la masse totale est M. Soit $J_{\Delta_G}$ le moment d'inertie de ce solide par rapport à un axe $\Delta_G$ passant par G. On note $J_{\Delta_O}$ le moment d'inertie de ce solide par rapport à un axe $\Delta_O$ passant par un point O du solide et parallèle à $\Delta_G$. Alors les deux moments d'inertie sont reliés par : $J_{\Delta_O} = J_{\Delta_G} + Md^{2}$.

Exemples :
![[mecanique2/attachments-mecanique2/figure17.png]]
![[mecanique2/attachments-mecanique2/figure18.png]]
![[mecanique2/attachments-mecanique2/figure19.png]]
[[#^info1|Clique ici pour savoir la différence entre la sphère et la boule.]]

> [!note] Moment cinétique en un point d'un axe de rotation fixe :
> $$
> \begin{align*}
> \displaystyle\overrightarrow{\sigma}_O(t) &= \iiint_{(S)} \overrightarrow{OP} \wedge \overrightarrow{v}(P,t) dm\\
> &= \iiint_{(S)} \overrightarrow{OP} \wedge (\overrightarrow{\Omega}(t) \wedge \overrightarrow{OP}) dm\\
> &= \iiint_{(S)} [OP^{2}\overrightarrow{\Omega}(t) - (\overrightarrow{\Omega}(t).\overrightarrow{OP})\overrightarrow{OP}]dm
> \end{align*}
> $$
> avec $\overrightarrow{\Omega}(t)$ est le vecteur instantané de rotation, porté par $\overrightarrow{e}_z$ ([[#^figure2]]). Cette expression est obtenue en utilisant [[#^info2|la formule du double produit vectoriel]].
> Considérons deux axes $(Ox)$ et $(Oy)$ attachés au solide et tels que $(Oxyz)$ soit orthogonal direct ([[#^figure3|fig. 3]]). On obtient ainsi, en notant $(x, y, z)$ les coordonnées d'un point P du solide : $OP^{2} = x^{2} + y^{2} + z^{2}$ et $\overrightarrow{\Omega}(t) = \Omega(t) \overrightarrow{e}_z$. Ainsi, le moment cinétique en O, point de l'axe de rotation, a pour expression : $\displaystyle\overrightarrow{\sigma}_O(t) = \iiint_{(S)} (r^{2}\overrightarrow{\Omega} - \Omega z(x\overrightarrow{e}_x + y\overrightarrow{e}_y))dm$ en posant $r^{2} = x^{2} + y^{2}$ où r désigne alors la distance d'un point P du solide à l'axe de rotation $(Oz)$.
> Le moment cinétique se décompose en deux contributions que l'on note respectivement $\overrightarrow{\sigma}_{O,\parallel}(t)$ et $\overrightarrow{\sigma}_{O,\perp}(t)$. La première est parallèle à l'axe, la seconde lui est orthogonale. Leurs expressions sont respectivement :
> $$
> \begin{align*}
> \overrightarrow{\sigma}_{O,\parallel}(t) &= \left(\iiint_{(S)} r^{2}dm\right)\overrightarrow{\Omega} = J_{Oz}\overrightarrow{\Omega}\\
> \overrightarrow{\sigma}_{O,\perp}(t) &= -\Omega(t)\left(\iiint_{(S)} z\,x\,dm\,\overrightarrow{e}_x + \iiint_{(S)} z\,y\,dm\,\overrightarrow{e}_y\right)
> \end{align*}
> $$
> où $J_{Oz}$ est le moment d'inertie du solide par rapport à l'axe $(Oz)$ et les deux intégrales qui apparaissent dans l'expression de $\overrightarrow{\sigma}_{O,\perp}(t)$ sont appelées « produits d'inertie » par rapport au plan $(Oxz)$, respectivement $(Oyz)$.
> Il existe cependant des cas particuliers dans lesquels la composante orthogonale est nulle :
> - lorsque l'axe de rotation $(Oz)$ est un axe de symétrie de la distribution matérielle du solide ([[#^figure4|fig. 4]]).
> - Un second cas particulier est celui d'un solide dont la distribution de matière est confinée dans le plan orthogonal à l'axe $(Oz)$ en $O$ ([[#^figure5|fig. 5]]). Il s'agit bien sûr d'un modèle, retenu par exemple dans le cas d'un solide d'épaisseur très faible par rapport à ses deux autres dimensions.

Moment cinétique d'un solide par rapport à un axe de rotation : $\sigma_{Oz} = \overrightarrow{\sigma}_O . \overrightarrow{e}_z$, si $(Oz)$ est l'axe de rotation qui n'est pas toujours le cas.

Moment cinétique d'un solide par rapport à un axe de rotation fixe : $\sigma_{Oz} = J_{Oz}\Omega$, si $(Oz)$ est l'axe de rotation qui n'est pas toujours le cas.

> [!note] Rotation autour d'un axe de direction fixe
> Dans le cas d'un axe de direction fixe, le raisonnement précédent (en remplaçant O par G) peut être repris pour déterminer le moment cinétique barycentrique du solide. En effet, le mouvement du solide dans son référentiel barycentrique est une rotation autour de l'axe passant par son centre d'inertie et de même direction que l'axe instantané de rotation ([[#^figure6|fig. 6]]). Le moment cinétique barycentrique est en général la somme d'une composante parallèle à l'axe de rotation et d'une composante orthogonale à cet axe de rotation.

> [!note] Moment cinétique barycentrique d'un solide
> Dans le référentiel barycentrique $(R^*)$ du solide, le centre de masse G est au repos, et l'axe de rotation instantané passe donc par G. Notons $Gz$ cet axe. La projection du moment cinétique barycentrique $\overrightarrow{\sigma}^*$ sur l'axe $Gz$ fournit le moment cinétique scalaire $\sigma_{Gz}^*$ qui s'exprime par $\sigma_{Gz}^* = J_{Gz}\Omega$ avec $J_{Gz}$ est le moment d'inertie par rapport à l'axe $Gz$.
> Premier théorème de Koenig : c'est la même formule que dans le [[03-La résultante et le moment cinétiques|chapitre précédant]] : $\overrightarrow{\sigma}_A = \overrightarrow{AG} \wedge \overrightarrow{P} + \overrightarrow{\sigma}^{*}$. On sait aussi que dans le cas important $A = G$, on a $\overrightarrow{\sigma}_G = \overrightarrow{\sigma}^{*}$. Donc $\sigma_{Gz} = \sigma_{Gz}^* = J_{Gz}\Omega$, en se rappelant que $Gz$ n'est pas toujours l'axe de rotation.
# Définitions

# Diagrammes
![[mecanique2/attachments-mecanique2/figure16.png]]^figure1
# Graphiques
![[mecanique2/attachments-mecanique2/figure20.png]]^figure2

![[mecanique2/attachments-mecanique2/figure21.png]]^figure3

![[mecanique2/attachments-mecanique2/figure22.png]]^figure4

![[mecanique2/attachments-mecanique2/figure23.png]]^figure5

![[mecanique2/attachments-mecanique2/figure24.png]]^figure6
# Expériences
> [!warning]
> Tous les fascicules des travaux pratiques sur le sujet de ce chapitre, que j'ai trouvé sur internet, contiennent des parties sur d'autres sujets comme l'étude dynamique ou énergétique du solide. Pour plus d'information on peut consulter les trois TP dans ce [lien 1](http://www.fsr.ac.ma/DOC/Cours_en_ligne/Printemp/LICENCES/LF/SMA/S4/Physique%206:%20M%C3%A9canique%20Du%20Solide/TP/Polycope%20Mec%206-12-20.pdf), le TP n°3 dans ce [lien 2](https://ilm-perso.univ-lyon1.fr/~oramos/documents/TPMechanics/fasciculeTP.pdf), le TP n°1 dans ce [lien 3](https://elearning.esgee-oran.dz/pluginfile.php/16193/mod_page/content/68/Poly%20phys%20S3%20Khelloufi.pdf), le seul TP dans ce [lien 4](http://agregation.capes.free.fr/tp/rotationjmr.pdf), le seul TP dans ce [lien 5](https://ia601703.us.archive.org/12/items/hlbdfjhdfjh/M%C3%A9canique%20Solide/TP%20Th%C3%A9or%C3%A9me%20de%20Huygens.pdf) et le seul TP dans ce [lien 6](http://prepa.blois.free.fr/SITEMPSI/PhyMPSI/wa_files/EnonceTP28.pdf).  
# Autres notes
> [!warning] Différence entre une sphère et une boule
> La **sphère** est représent​ée par l'ensemble des points situés à une même distance du centre appelée «rayon».
> Quant à elle, la **boule** représente l'ensemble des points qui sont situés à une distance inférieure ou égale au rayon par rapport au centre.
> En d'autres mots, la sphère fait référence à la surface de la boule. Ainsi, le concept de sphère est associé à l'aire et celui de boule au volume.
^info1

> [!warning] Double produit vectoriel
> Les formules suivantes sont à connaître :
> $\overrightarrow{A} \wedge (\overrightarrow{B} \wedge \overrightarrow{C}) = (\overrightarrow{A} . \overrightarrow{C})\overrightarrow{B} - (\overrightarrow{A} . \overrightarrow{B})\overrightarrow{C}$
> $\overrightarrow{A} \wedge (\overrightarrow{B} \wedge \overrightarrow{C}) = (\overrightarrow{A} . \overrightarrow{C})\overrightarrow{B} - (\overrightarrow{B} . \overrightarrow{C})\overrightarrow{A}$
^info2

> [!note] moment d'inertie
> Du point de vue de la Dynamique, la masse est la propriété d'un objet qui s'oppose à la variation de son état de mouvement (sa vitesse). Dans la Dynamique de la rotation, le moment d'inertie possède un rôle équivalent : c'est la propriété d'un objet qui s'oppose à la variation de sa vitesse angulaire $\overrightarrow{\Omega}$.

> [!note] Cas général de l'expression du moment d'inertie
> L'expression de $J_{\Delta}$ dans ce chapitre est pour un système discret de points matériels. Alors on peut visiter le [lien suivant](https://rtc.ma/pdfs/TSI/spe-crs/gm/Grandeurs%20inertielles.pdf) pour apprendre comment trouver l'expression développée du moment d'inertie pour un système continu.

> [!warning] Exercice 2 question 8 de section savoir résoudre les exercices page 74
> Pour une force centrale newtonienne, on a utilisé la deuxième formule de Binet (rencontrée dans le [[07-Force centrale conservative. Mouvement newtonien|chapitre 7]] du livre intitulé "Mécanique") afin de démontrer que la trajectoire du mobile est une conique.