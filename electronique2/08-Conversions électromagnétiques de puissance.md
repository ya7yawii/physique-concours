---
titre: "[[08-Conversions électromagnétiques de puissance]]"
tags:
  - force-de-lorentz
  - force-de-laplace
  - circuit-filiforme
  - induction-électromagnétique
  - force-électromotrice
  - loi-de-faraday
  - loi-d-ohm
  - conversion-électromécanique
  - transducteur-électromécanique
crée: 07-12-2025, 22:15
---
# Formules
Force de Lorentz : $\overrightarrow{F} = q(\overrightarrow{E} + \overrightarrow{v} \wedge \overrightarrow{B})$
Densité volumique de forces magnétiques : $\dfrac{d\overrightarrow{F}}{d\tau} = \overrightarrow{j}(M) \wedge \overrightarrow{B}(M)$ avec $d\tau$ est un élément de volume et $\overrightarrow{j}(M)$ est la densité volumique de courant.

> [!note] Circuits filiformes
> Tout élément de courant $id\overrightarrow{L}$ ([[#^figure1|fig. 1]]) placé dans un champ magnétique $\overrightarrow{B}$ est soumis à la force de Laplace : $d\overrightarrow{F_L} = id\overrightarrow{L} \wedge \overrightarrow{B}$ avec $i = \overrightarrow{j} . \overrightarrow{s}$ est l'intensité du courant.

> [!note] Induction électromagnétique : Mise en évidence
> Considérons un circuit $\mathcal{C}$ sans générateur placé dans le champ magnétique $\overrightarrow{B}$ créé par un aimant ([[#^figure2|fig. 2]]) ou par un circuit source $\mathcal{C}_s$ parcouru par un courant continu $i_s$ ([[#^figure3|fig. 3]]).
> Ainsi, un courant temporaire $i(t)$ est créé dans le circuit $\mathcal{C}$, sans générateur, lors de la variation du champ magnétique $\overrightarrow{B}$ :
> - soit par déplacement par rapport à $\mathcal{C}$ des sources de champ ;
> - soir par modification de la valeur de ces champs magnétiques.
> 
> Ce phénomène est le **phénomène d'induction électromagnétique**, et le courant $i(t)$ qui en résulte est le **courant induit**.
> Si le circuit $\mathcal{C}$ est ouvert, alors $i(t)$ est nul, mais la variation du champ magnétique $\overrightarrow{B}$ crée une **tension** $u(t)$ aux bornes de $\mathcal{C}$.

> [!note] Induction électromagnétique : Force électromotrice de déplacement
> Lors du déplacement d’un conducteur filiforme orienté de P vers Q de résistance R dans le référentiel $\mathcal{R}$ du laboratoire, chaque élément de circuit $d\overrightarrow{L}$ acquiert une vitesse d’entraînement $\overrightarrow{v}_e$ ([[#^figure4|fig. 4]]). Le conducteur devient alors le siège d’une f.e.m. d’induction $e$ ; cela signifie que, pour les calculs électrocinétiques, le conducteur est équivalent à un dipôle de Thévenin de résistance R et de f.e.m. $e$, orientée de P vers Q, comme sur la [[#^figure4|figure 4]] (cf. H-Prépa, Électromagnétisme, $2^{de}$ année).
> La f.e.m. induite qui apparaît dans le conducteur filiforme orienté de P vers Q est la circulation du champ électromoteur : $\overrightarrow{E_m}(M) = \overrightarrow{v}_e(M) \wedge \overrightarrow{B}(M)$,
> soit : $\displaystyle e(t) = \int_{P}^{Q} (\overrightarrow{v}_e \wedge \overrightarrow{B}) . d\overrightarrow{L}$, Cette f.e.m. est orientée dans le sens choisi pour l’orientation du circuit.

> [!note] Induction électromagnétique : Loi de Faraday
> La f.e.m. $e(t)$ induite dans un circuit constitué d’une seule maille est : $e(t) = -\dfrac{d\Phi}{dt}$, où $\Phi(t)$ est le flux total à travers le circuit, c’est-à-dire le flux du champ magnétique créé par les sources extérieures au circuit et par le circuit lui-même.
> Les orientations de la f.e.m. d'induction et du flux sont fixées par celle du circuit.
> Rigoureusement, la loi de Faraday ne concerne que les circuits où le flux peut être défini sans ambiguïté, il faut pour cela que le circuit soit filiforme et fermé.
> Il est cependant courant d’étendre la notion de flux à une portion (non fermée) de circuit dans le cas d’une bobine constituée de spires ; chaque spire, bien que ne constituant pas une courbe fermée au sens rigoureux, définit une surface et donc un flux. **Le flux à travers la bobine est alors la somme des flux à travers chaque spire.**

> [!note] Induction électromagnétique : Loi d'Ohm
> Rappelons la loi d’Ohm (cf. H-Prépa, Électromagnétisme, $2^{de}$ année) pour une portion du circuit ([[#^figure5|fig. 5a]]).
> Soit une portion du circuit $PQ$ (circuit orienté de $P$ vers $Q$ parcourue par une intensité éventuelle $i(t)$. Supposons que cette portion de circuit soit le siège d'une f.e.m. $e(t)$. Si $R$ représente la résistance ohmique du circuit, alors :
> La loi d’Ohm pour une portion de circuit $PQ$ s’écrit ([[#^figure5|fig. 5a]]) : $V_P - V_Q + e(t) = Ri(t)$.
> Si le circuit est fermé ([[#^figure5|fig. 5b]]), la loi d'Ohm s'écrit : $e(t) = Ri(t)$.

> [!note] Conversions électromécaniques de puissance : Mouvement d'un courant dans un champ magnétique permanent
> Considérons un circuit filiforme dont l’élément de courant $id\overrightarrow{L}$, placé en M, se déplace à la vitesse $\overrightarrow{v}_e$ dans un référentiel $\mathcal{R}$ où règne un champ magnétique permanent $\overrightarrow{B}$ ([[#^figure6|fig. 6]]). Sur cet élément de courant s’exerce la force de Laplace : $d\overrightarrow{F} = id\overrightarrow{L} \wedge \overrightarrow{B}$.
> Supposons, par simplicité, que tous les porteurs de charge sont de même type, de charge $q$ et de concentration volumique $n$. Soit $\overrightarrow{v}_r$ leur vitesse dans un référentiel $\mathcal{R}'$ lié au conducteur.
> Sur chacun des porteurs, s’exerce la force de Lorentz : $\overrightarrow{F} = q(\overrightarrow{v}_e + \overrightarrow{v}_r) \wedge \overrightarrow{B}$.
> En M, le **champ électromoteur** est $\overrightarrow{E_m} = \overrightarrow{v}_e \wedge \overrightarrow{B}$ et l'élément de courant $id\overrightarrow{L}$ est le siège d'une **f.e.m. induite élémentaire** : $de = (\overrightarrow{v}_e \wedge \overrightarrow{B}) . d\overrightarrow{L}$.

> [!note] Conversions électromécaniques de puissance : Bilan de puissance des forces de Lorentz
> Soit $d\tau$ le volume de l'élément de courant $id\overrightarrow{L}$. Les porteurs de charge, contenus dans $d\tau$, possèdent la vitesse $\overrightarrow{v} = (\overrightarrow{v}_e + \overrightarrow{v}_r)$ dans $\mathcal{R}$ et sont soumis à la force de Lorentz : $d\overrightarrow{F} = nqd\tau(\overrightarrow{v} \wedge \overrightarrow{B}) = nq(\overrightarrow{v}_e + \overrightarrow{v}_r) \wedge \overrightarrow{B}d\tau$, dont la puissance dans $\mathcal{R}$ est nulle : $d\mathcal{P} = (\overrightarrow{v}_e + \overrightarrow{v}_r) . d\overrightarrow{F} = nq(\overrightarrow{v}_e + \overrightarrow{v}_r) . [(\overrightarrow{v}_e + \overrightarrow{v}_r) \wedge \overrightarrow{B}]d\tau = 0$.
> **La puissance des forces de Lorentz est nulle**.
> Des quatre termes du développement du produit mixte ci-dessus, deux sont identiquement nuls : $nq(\overrightarrow{v}_e \wedge \overrightarrow{B}) . \overrightarrow{v}_e d\tau = 0$ et $nq(\overrightarrow{v}_r \wedge \overrightarrow{B}) . \overrightarrow{v}_r d\tau = 0$.
> Il reste après simplification : $d\mathcal{P} = nq(\overrightarrow{v}_e \wedge \overrightarrow{B}) . \overrightarrow{v}_r d\tau + nq(\overrightarrow{v}_r \wedge \overrightarrow{B}) . \overrightarrow{v}_e d\tau = 0$.
> En introduisant le vecteur densité de courant $\overrightarrow{j} = nq\overrightarrow{v}_r$, le premier terme s'écrit : $d\mathcal{P}_e = (\overrightarrow{v}_e \wedge \overrightarrow{B}) . \overrightarrow{j}d\tau = \overrightarrow{E_m} . id\overrightarrow{L} = i(\overrightarrow{E_m} . d\overrightarrow{L}) = ide$, où $\overrightarrow{E_m}$ est le champ électromoteur et $de$ la f.e.m. induite dans l'élément de courant considéré.
> Ce terme représente la puissance électrique fournie par la f.e.m. induite $e$ ([[#^figure7|fig. 7]]).
> Le second terme s'écrit : $d\mathcal{P}_L = (\overrightarrow{j}d\tau \wedge \overrightarrow{B}) . \overrightarrow{v}_e = (id\overrightarrow{L} \wedge \overrightarrow{B}) . \overrightarrow{v}_e = \overrightarrow{v}_e . d\overrightarrow{F_L}$, où $d\overrightarrow{F_L}$ est la force de Laplace appliquée à l'élément de courant. Ce terme représente la **puissance des forces de Laplace**.
> En définitive, le bilan de puissance effectué sur l'élément de courant $id\overrightarrow{L}$ s'écrit : $d\mathcal{P}_e + d\mathcal{P}_L = 0$ et en considérant la totalité du circuit filiforme, il vient : $\mathcal{P}_e + \mathcal{P}_L = 0$.
> ==**Lors du déplacement d'un circuit filiforme dans un champ magnétique permanent, la puissance électrique de la f.e.m. induite est opposée à la puissance mécanique des forces de Laplace : $\mathcal{P}_e + \mathcal{P}_L = 0$.**==
> Ce résultat établit le principe des conversions électromécaniques.

> [!note] Conversions électromécaniques de puissance : Conversion d'une puissance mécanique en puissance électrique
> Supposons que sous l’action d’une force extérieure $\overrightarrow{F}_{ext}$, un conducteur rectiligne $A_1A_2$ de longueur $L$ se déplace a la vitesse $\overrightarrow{v}_e$ dans le référentiel $\mathcal{R}$ où règne un champ magnétique $\overrightarrow{B}$ uniforme et permanent ([[#^figure8|fig. 8]]). ($\overrightarrow{A_1A_2}$, $\overrightarrow{v}_e$ et $\overrightarrow{B}$ sont supposés orthogonaux.)
> Le conducteur est le siège d’un champ électromoteur $\overrightarrow{E_m} = \overrightarrow{v}_e \wedge \overrightarrow{B} = Bv_e\overrightarrow{e_x}$ et d’une f.e.m. positive $\displaystyle e = \int_{A_1}^{A_2} \overrightarrow{E_m}d\overrightarrow{M} = Bv_eL$.
> Soit $r$ la résistance du conducteur.
> Ce dernier se comporte comme un **générateur** de résistance interne $r$ et de f.e.m. $e$ orientée de $A_1$ vers $A_2$ ([[#^figure9|fig. 9]]).
> En connectant ce générateur à sa charge constituée par un circuit extérieur, un courant $i$ le traverse de $A_1$ à $A_2$ et une tension $u = e - ri$ apparaît entre ses bornes $A_2$ et $A_1$.
> Dès lors, le conducteur est soumis à une force de Laplace : $\overrightarrow{F_L} = -BiL\overrightarrow{e_y}$ qui tend à s’opposer à son déplacement.
> Nous vérifions que la puissance mécanique des forces de Laplace $\mathcal{P}_L = \overrightarrow{F_L} . \overrightarrow{v}_e = -BiL\overrightarrow{v_e}$ $(< 0)$ est opposée à la puissance électrique fournie par la f.e.m. d’induction $\mathcal{P}_e = ei = BiL\overrightarrow{v_e}$ $(> 0)$ : $\mathcal{P}_L + \mathcal{P}_e = 0$.
> Notons par $\mathcal{E}_K$ l’énergie cinétique du conducteur $A_1A_2$. Le théorème de l'énergie cinétique, appliqué au conducteur, s’écrit : $\dfrac{d\mathcal{E}_K}{dt} = (\overrightarrow{F}_{ext} + \overrightarrow{F_L}) . \overrightarrow{v}_e - \mathcal{P}_{frot} = \overrightarrow{F}_{ext} . \overrightarrow{v}_e - ei - \mathcal{P}_{frot}$, où $\mathcal{P}_{frot}$ est la puissance dissipée par les frottements $(\mathcal{P}_{frot} > 0)$.
> **En régime établi**, pour lequel la vitesse $\overrightarrow{v}_e$ du conducteur est constante $\left(\dfrac{d\mathcal{E}_K}{dt} = 0\right)$, le bilan de puissance s’établit à : $\mathcal{P}_{mec\,ext} = \overrightarrow{F}_{ext} . \overrightarrow{v}_e = ei + \mathcal{P}_{frot}$.
> Le conducteur $A_1A_2$, qui se comporte comme un générateur vis-à-vis du circuit d'utilisation, fournit à ce dernier la puissance électrique utilisable : $\mathcal{P}_{élec} = ui = (e - ri)i = \mathcal{P}_{mec\,ext} - \mathcal{P}_{frot} - \mathcal{P}_{J}$, où $\mathcal{P}_{J} = ri^{2}$ est la puissance dissipée dans le conducteur par effet Joule.
> En définitive, le bilan de puissance en régime établi, s’écrit : $\mathcal{P}_{mec\,ext} - \mathcal{P}_{frot} = \mathcal{P}_{élec} + \mathcal{P}_{J}$.
> Ce bilan de puissance est celui d’une génératrice électrique. Aux phénomènes réversibles de nature électromagnétique réalisant la conversion électromécanique de puissance, se superposent deux phénomènes dissipatifs irréversibles (les frottements mécaniques et l'effet Joule) ([[#^figure10|fig. 10]]).

> [!note] Conversions électromécaniques de puissance : Conversion d'une puissance électrique en puissance mécanique
> Supposons maintenant que, sous l’action d’une tension $u_{ext}$ d’origine extérieure, ce même conducteur $A_1A_2$ soit parcouru par un courant $i$.
> Étant placé dans le champ magnétique $\overrightarrow{B}$ (permanent), il est soumis à la force de Laplace $\overrightarrow{F_L} = -BiL\overrightarrow{e_y}$ ([[#^figure11a|fig. 11a]]) qui l’entraîne à la vitesse $\overrightarrow{v}_e$ en lui fournissant la puissance mécanique positive : $\mathcal{P}_L = \overrightarrow{F_L} . \overrightarrow{v}_e = BiL\overrightarrow{v_e}$.
> Ce mouvement s’effectuant dans le champ magnétique $\overrightarrow{B}$, le conducteur est le siège d’un champ électromoteur : $\overrightarrow{E_m} = \overrightarrow{v}_e \wedge \overrightarrow{B}$ qui crée la f.e.m. d'induction : $\displaystyle e = e_{A_1A_2} = \int_{A_1}^{A_2}\overrightarrow{E_m} . d\overrightarrow{e} = -Bv_eL$, soit le schéma équivalent de [[#^figure11b|figure 11b]].
> On vérifie encore que la puissance mécanique des forces de Laplace $\mathcal{P}_L = \overrightarrow{F_L} . \overrightarrow{v}_e = BiL\overrightarrow{v_e}$ $(> 0)$ est opposée à la puissance électrique fournie par la f.e.m. d'induction $\mathcal{P}_e = ei = -BiL\overrightarrow{v_e}$ $(< 0)$ : $\mathcal{P}_L + \mathcal{P}_e = 0$.
> Le générateur extérieur doit appliquer une tension $u_{ext} = -e + ri$ aux bornes du conducteur pour maintenir le courant $i$ dans le circuit.
> Le conducteur $A_1A_2$ reçoit de ce générateur la puissance électrique d’origine extérieure : $\mathcal{P}_{élec\,ext} = u_{ext}i = -ei + ri^{2} = \mathcal{P}_L + \mathcal{P}_J$, où $\mathcal{P}_J = ri^{2}$ est la puissance dissipée par effet Joule dans le conducteur. Le théorème de l’énergie cinétique appliquée à la barre s'écrit : $\dfrac{d\mathcal{E}_K}{dt} = \mathcal{P}_L - \mathcal{P}_{mec} -\mathcal{P}_{frot}$, où $\mathcal{P}_{mec} = -\overrightarrow{F}_{ext} . \overrightarrow{v}_e$ est la puissance mécanique utilisable (puissance de la force $-\overrightarrow{F}_{ext}$ appliquée à la charge mécanique liée au conducteur) et $\mathcal{P}_{frot}$ est la puissance dissipée par les frottements.
> **En régime établi**, pour lequel la vitesse $\overrightarrow{v}_e$ du conducteur est constante $\left(\dfrac{d\mathcal{E}_K}{dt} = 0\right)$, il vient $\mathcal{P}_L = \mathcal{P}_{mec} + \mathcal{P}_{frot}$, ce qui conduit au bilan de puissance : $\mathcal{P}_{élec\,ext} - \mathcal{P}_J = \mathcal{P}_{mec} + \mathcal{P}_{frot}$.
> Ce bilan de puissance est celui d’un **moteur électrique** où il apparaît encore qu’aux phénomènes réversibles de nature électromagnétique réalisant la conversion électromagnétique de puissance, se superposent deux phénomènes dissipatifs irréversibles (les frottements mécaniques et l’effet Joule ([[#^figure12|fig. 12]]).
# Définitions
==**Transducteurs électromécaniques**== :
L’étude précédente a montré qu’il est possible de réaliser des conversions électromécaniques de puissance en utilisant les phénomènes d’induction électromagnétiques.
==**Le principe de ces conversions est traduit par la relation $\mathcal{P}_L + \mathcal{P}_e = 0$. Il exprime, qu’en présence d’un champ magnétique permanent, la puissance mécanique des forces de Laplace $\mathcal{P}_L$ est opposée à la puissance électrique $\mathcal{P}_e$ de la f.e.m. induite.**==
Ce résultat établi pour des champs permanents est valable aussi pour des champs tournants utilisés dans les machines étudiées au chapitre 10.
==**Un *transducteur électromécanique* est un dispositif pouvant réaliser soit la conversion d’une énergie mécanique (aux pertes par frottement près) en énergie électrique (aux pertes par effet Joule près), soit la conversion inverse d’une énergie électrique (aux pertes par effet Joule près) en énergie mécanique (aux pertes par frottement près).**==
Il existe une très grande variété de transducteurs électromécaniques, d’une importance pratique considérable : moteurs, dynamos, alternateurs, haut-parleurs, microphones, etc.
# Diagrammes
Force magnétique $d\overrightarrow{F}$ s'exerçant sur l'élément de courant $id\overrightarrow{L}$
![[electronique2/attachments-electronique2/figure213.png]]^figure1

Une modification de la position relative de l'aimant par rapport au circuit $\mathcal{C}$ crée un courant temporaire $i(t)$ dans ce circuit
![[electronique2/attachments-electronique2/figure214.png]]^figure2

Le circuit $\mathcal{C}$ est placé dans le champ magnétique $\overrightarrow{B}$ produit par le circuit source $\mathcal{C}_s$
![[electronique2/attachments-electronique2/figure215.png]]^figure3

Conducteur mobile et son équivalent électrocinétique $u = Ri - e$, ou encore $u + e =Ri$
![[electronique2/attachments-electronique2/figure216.png]]^figure4

a. Portion de circuit $PQ$ (orientation de $P$ vers $Q$). b. Circuit fermé
![[electronique2/attachments-electronique2/figure217.png]]^figure5

Élément de courant $id\overrightarrow{L}$ entraîné à la vitesse $\overrightarrow{v}_e$ dans le champ magnétique $\overrightarrow{B}$ : $id\overrightarrow{L} = \overrightarrow{j}sdL = \overrightarrow{j}d\tau$
![[electronique2/attachments-electronique2/figure218.png]]^figure6

Le générateur de f.e.m. $de$ fournit la puissance $ide$ au circuit électrique
![[electronique2/attachments-electronique2/figure219.png]]^figure7

Principe d'une conversion de puissance mécanique en puissance électrique
![[electronique2/attachments-electronique2/figure220.png]]^figure8

Circuit électrique équivalent
![[electronique2/attachments-electronique2/figure221.png]]^figure9

Conversion d'une puissance mécanique en puissance électrique
![[electronique2/attachments-electronique2/figure222.png]]^figure10

Principe d'une conversion de puissance mécanique en puissance électrique
![[electronique2/attachments-electronique2/figure223.png]]^figure11a

Schéma électrique équivalent : $u_{ext} - BLv_e = ri$
![[electronique2/attachments-electronique2/figure224.png]]^figure11b

Conversion d'une puissance mécanique en puissance électrique
![[electronique2/attachments-electronique2/figure225.png]]^figure12
# Graphiques

# Expériences

# Autres notes
