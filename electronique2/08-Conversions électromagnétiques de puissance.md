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
# Graphiques

# Expériences

# Autres notes
