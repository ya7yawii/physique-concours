---
titre: "[[01-Électrocinétique. Cadre et concepts de base]]"
tags:
aliases:
crée: 05-11-2025, 19:49
---
# Formules
Intensité du courant : $\displaystyle i = \frac{\delta q}{\delta t}$.

Énergie potentielle d’un porteur de charge et potentiel : $\mathcal{E}_P = qv_{P}$ avec $v_{P}$ le potentiel en un point P d’un circuit électrique et $\mathcal{E}_P$ l’énergie potentielle d’un porteur de charge q qui se trouve au point P.

Tension entre deux points d’un circuit : $u_{AB} = v_A - v_B$ ; $u_{AB} = -u_{BA}$.
> [!note]
> Dans un schéma, le signe de la tension est indiqué par une flèche. Si la pointe de la flèche indique le point A, alors : $u = u_{AB} = v_A - v_B$.

> [!note] Potentiel en un point
> Nous pouvons décréter arbitrairement que le potentiel en un point est nul. Ce point détermine la masse du circuit. Sur la [[#^figure4|figure 4]], il s’agit du point M.
> Le potentiel en un point A est alors défini sans ambiguïté : $v_A = v_M + u_{AM}$, soit : $v_A = u_{AM}$

> [!note] Additivité des tensions
> Les tensions dans un circuit suivent une loi d’additivité. Reprenons le circuit représenté sur la [[#^figure4|figure 4]] : $u_{AB} = v_A - v_B = (v_A - v_C) + (v_C - v_D) + (v_D - v_B)$ d'où : $u_{AB} = u_{AC} + u_{CD} + u_{DB}$.
> Remarque : Il existe une similitude entre l’addition des tensions et celles des vecteurs : $\overrightarrow{AB} = \overrightarrow{AC} + \overrightarrow{CD} + \overrightarrow{DB}$.



# Définitions
==**Sens conventionnel du courant électrique**== :
Nous savons que le courant électrique résulte du déplacement de particules chargées (par exemple, les électrons) porteurs de charge. Il existe des particules de charge positive et des particules de charge négative.
Le sens conventionnel du courant est celui des porteurs de charges positives.

==**Conservation de la charge**== :
La charge électrique ne peut être ni créée, ni détruite : la conservation de la charge électrique est une loi fondamentale de la physique.
Un générateur ne crée aucune charge électrique, mais communique à ces dernières de l’énergie ; il met les charges en mouvement.

==**Sens du courant dans un circuit**== :
Le sens de déplacement des porteurs de charge mobiles dans un circuit est lié aux caractéristiques des éléments qui le constituent.
Dans le montage de la [[#^figure1|figure 1]], la pile joue le rôle d’une pompe à charge : en dehors de celle-ci, les électrons de conduction se déplacent du pôle $\ominus$ de la pile vers le pôle $\oplus$. Le courant électrique I engendré par ce déplacement est orienté dans le sens opposé.

==**Mesure du courant électrique**== :
Le courant électrique peut être mesuré à l’aide d’un ampèremètre. Cet appareil est polarisé, et possède une borne $\oplus$ et une borne $\ominus$ (souvent désignée par « COM »). Orienté dans le sens ➀ comme sur la [[#^figure2|figure 2]], il indiquera la valeur de $i_1$. Orienté en sens inverse ➁ ([[#^figure3|fig. 3]]), il indiquera la valeur de $i_2$.

==**Mesure de la tension**== :
Un voltmètre indique la valeur de la tension orientée de la borne $\ominus$ (souvent repérée par COM) à la borne $\oplus$. Si on inverse les bornes du voltmètre, celui-ci indique une valeur opposée, bien que la tension physique soit inchangée.
# Diagrammes
Sens conventionnel du courant dans les métaux dont les porteurs sont des électrons libres
![[electronique1/attachments-electronique1/figure1.png]]

Sens de déplacement des deux types de porteurs dans un semi-conducteur
![[electronique1/attachments-electronique1/figure2.png]]

Déplacement des charges de conduction et courant physique I résultant
![[electronique1/attachments-electronique1/figure3.png]]^figure1

Valeur lue à l’ampèremètre $i_1 = I$
![[electronique1/attachments-electronique1/figure4.png]]^figure2

Valeur lue à l’ampèremètre $i_2 = -I$
![[electronique1/attachments-electronique1/figure5.png]]^figure3

![[electronique1/attachments-electronique1/figure6.png]]^figure4
# Graphiques

# Expériences

# Autres notes
> [!warning] Ordre de grandeur à connaître
> Le nombre d’atomes de cuivre par mètre cube de métal est $n \approx 10^{29}\, atomes\, . m^{-3}$.