---
titre: "[[08-Conversions électromagnétiques de puissance]]"
tags:
aliases:
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

# Définitions

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
# Graphiques

# Expériences

# Autres notes
