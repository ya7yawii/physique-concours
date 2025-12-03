---
titre: "[[07-Conversion électromagnétique statique. Le transformateur]]"
tags:
aliases:
crée: 03-12-2025, 15:56
---
# Formules

# Définitions
> [!note] Présentation du transformateur : Transport de puissance électrique
> L'énergie électrique est produite dans des centrales qui sont souvent éloignées du lieu d'utilisation. Il est donc nécessaire de transporter cette énergie avec un minimum de pertes.
> L'utilisation de très hautes tensions est nécessaire pour transporter l’énergie avec peu de pertes. Actuellement, le transport d’électricité sur de longues distances se fait sous des tensions comprises entre 200 kV et 400 kV, et l’intensité qui traverse les fils peut dépasser 400 A.
> Les alternateurs des centrales électriques ne peuvent pas fournir directement de telles tensions et celles-ci ne peuvent être utilisées directement par le consommateur. II est donc nécessaire :
> - d’élever la tension au niveau de la centrale électrique ;
> - d’abaisser la tension au niveau du lieu de consommation.
> 
> L'utilisation du courant alternatif et des transformateurs permet de réaliser ces opérations de façon simple. C’est la raison pour laquelle l'utilisation du courant alternatif a très rapidement supplanté celle du continu.
> Cependant, les progrès technologiques actuels permettent l’utilisation de très hautes tensions continues pour le transport d’énergie électrique sur de grandes distances (liaison France-Angleterre par exemple). En effet, la présence d’une capacité entre les conducteurs d’une ligne à haute tension empêche l'utilisation de l'alternatif pour le transport d’énergie électrique sur des grandes distances. Ces distances sont de l’ordre :
> - de la dizaine de kilomètre pour les lignes enterrées dont la capacité est grande ;
> - du millier de kilomètre pour les lignes aériennes.

> [!note] Présentation du transformateur : Utilisation des transformateurs
> Le transformateur est un appareil très courant. Nous en rencontrons de toutes les tailles : du transformateur utilisé dans le transport d’énergie électrique à haute tension de plusieurs tonnes au transformateur basse tension des adaptateurs secteur des petits appareils électriques d’une centaine de grammes.
> ==**- Le transformateur est un convertisseur d’énergie électrique. Il transfère, en alternatif et uniquement en alternatif, de la puissance électrique d’une source placée dans le circuit primaire, à une charge placée dans le circuit secondaire. Cette conversion s’effectue sans modification de fréquence et avec un excellent rendement énergétique : dans les transformateurs industriels, les pertes sont inférieures à 1 %.**==
> ==**- Comme elle se produit sans conversion d’énergie électromécanique, cette conversion est dite statique.**==
> 
> Cette conversion d’énergie est nécessaire dans deux cas.
> - Adaptation de la source à la charge : La tension délivrée (ou le courant) par la source n’est pas adaptée à la charge, est le cas le plus courant ([[#^figure1|fig. 1]]). Dans le cas du passage de la très haute tension (400 kV) à la moyenne tension (< 32 kV utilisée dans l'industrie) puis à la basse tension (220 V), le transformateur est **abaisseur de tension**. Dans le cas du passage de la moyenne tension (en sortie des alternateurs de centrale électrique) à la haute tension, le transformateur est **élévateur de tension**.
> - Isolation électrique entre la charge et la source : C'est le cas des installations en milieu humide (salles de bains par exemple). L'utilisation d’un transformateur d’isolement évite toute électrocution possible car aucune des deux bornes du secondaire n’est reliée à la Terre ([[#^figure2|fig. 2]]).
> ==**Un transformateur doit être adapté à la source et à la charge auxquelles il est relié. Pour cette raison, les constructeurs précisent les caractéristiques suivantes : la fréquence d'utilisation, la tension d’alimentation primaire, la tension de sortie à vide et la puissance apparente (ou l'intensité nominale).**==
> ==**La puissance apparente est le produit de l’intensité nominale (qui correspond aux conditions d'utilisation optimale du transformateur) par la tension de sortie à vide ; elle est exprimée en VA et non en watts.**==
> 
> Par exemple, un transformateur 220 V, 24 V, 100 VA doit être relié à une source de tension efficace 220 V, 50 Hz et fournit une intensité de $\frac{100}{24} = 4,2 A$ sous 24 V dans les conditions nominales.
> Nous n’étudierons que les transformateurs monophasés, c’est-à-dire ceux pour lesquels la source et la charge n’ont que deux bornes.

> [!note] Présentation du transformateur : Description
> Un transformateur est constitué d’un cadre ferromagnétique sur lequel sont bobinés deux enroulements électriquement indépendants : le primaire (relié à la source) et le secondaire (relié à la charge).
> Le circuit magnétique est constitué d’un matériau ferromagnétique, en général de minces tôles de fer au silicium d’épaisseur comprise environ entre 0,05 mm et 0,5 mm, isolées les unes des autres par du vernis ou par une oxydation superficielle, et fortement comprimées par un système de serrage.
> Chacun des circuits électriques est constitué de fil de cuivre ou d’aluminium émaillé ou enrubanné de coton, papier ou toile pour l’isolation électrique. Ces circuits sont noyés dans la résine ou imprégnés de vernis et comprimés pour résister aux efforts électromagnétiques.
> Dans les transformateurs de forte puissance, le circuit électrique est isolé du circuit ferromagnétique et de l’enveloppe extérieure par un diélectrique (de l'huile ou du pyralène, avant son interdiction). Ce fluide permet aussi d’évacuer vers l’extérieur la chaleur dissipée dans le transformateur ([[#^figure3|fig. 3]]).
> Pour notre étude expérimentale des propriétés du transformateur, nous utiliserons des transformateurs démontables ([[#^figure4|fig. 4]]) qui permettent de tester différents enroulements au primaire et au secondaire.

> [!note] Le circuit ferromagnétique : Les matériaux ferromagnétiques
> L'étude du magnétisme dans la matière se trouve dans le cours d'électromagnétisme (H-Prépa, Électromagnétisme, 2e année, chapitre 8). Nous ne rappelons ici que les résultats essentiels pour la compréhension du transformateur.
> Les sections sur le vecteur aimantation $\overrightarrow{M}$, les vecteurs excitation magnétique $\overrightarrow{H}$ et théorème d'Ampère et le caractéristique d'un matériau ferromagnétique n'apportent pas des informations importantes.
> - Classification des milieux ferromagnétiques :


# Diagrammes
Adaptation de la sortie à la charge
![[electronique2/attachments-electronique2/figure163.png]]^figure1

Transformateur d'isolement. Système dit à "double isolation"
![[electronique2/attachments-electronique2/figure164.png]]^figure2
# Graphiques
a. Transformateur basse tension. b. Transformateur haute tension 400-225 kV à la centrale nucléaire de Civaux
![[electronique2/attachments-electronique2/figure165.png]]^figure3

Transformateur expérimental
![[electronique2/attachments-electronique2/figure166.png]]^figure4
# Expériences

# Autres notes
> [!warning] Application 1 page 215
> ![[electronique2/attachments-electronique2/figure162.png]]