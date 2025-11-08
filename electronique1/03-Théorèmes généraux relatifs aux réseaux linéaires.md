---
titre: "[[03-Théorèmes généraux relatifs aux réseaux linéaires]]"
tags:
aliases:
crée: 07-11-2025, 19:53
---
# Formules
> [!note] Association en série de dipôles linéaires
> Deux dipôles sont associés en série si une de leurs bornes est commune et s’ils sont parcourus par le même courant ([[#^figure1|fig. 1]]).
> - Association de résistors : $u = Ri$ avec $\displaystyle R = \sum_j R_j$.
> - Association de générateurs réels libres : $u = e - Ri$, avec $\displaystyle R = \sum_j R_j$ et $\displaystyle e = \sum_j \epsilon_j e_j$ où $\epsilon_j = 1$ si l'orientation de $e_j$ est identique à celle de $i$ et $\epsilon_j = -1$ dans le cas contraire.
> - Association de condensateurs idéaux : $i = C\dfrac{du}{dt}$, avec $\displaystyle \frac{1}{C} = \sum_j \frac{1}{C_j}$.
> - Association de bobines idéales : $u = L\dfrac{di}{dt}$, avec $\displaystyle L = \sum_j L_j$.

> [!note] Loi de Pouillet pour un circuit à une maille
> Considérons le circuit de la [[#^figure2|figure 2]]. Dans le cas où les dipôles sont des générateurs libres ou des résistors, l'intensité dans le circuit est donnée par : $i = \frac{\displaystyle \sum_j \epsilon_j e_j}{\displaystyle \sum_k R_k}$ avec $\epsilon_j = 1$ si $e_j$ est orienté dans le sens de $i$, et $e_j = -1$ sinon.

> [!note] Pont diviseur de tension
> Il est utile de savoir déterminer la différence de potentiel aux bornes d’un dipôle en fonction de celle aux bornes de l’association des dipôles en série ([[#^figure3|fig. 3]]). A partir de la figure, le pont diviseur de tension nous donne : $u_{BC} = \frac{R_2}{R_1 + R_2} u_{AC}$ si aucune intensité ne sort du pont diviseur.

> [!note] Association en parallèle de dipôles linéaires
> Des dipôles sont associés en parallèles s’ils sont reliés aux deux mêmes nœuds et donc soumis à la même différence de potentiel ([[#^figure4|fig. 4]]).
> - Association de résistors : $u = Ri$, avec $\displaystyle \frac{1}{R} = \sum_j \frac{1}{R_j}$, ou $i = Gu$, avec $\displaystyle G = \sum_j G_j$.
> - Association de générateurs : $i = \eta - \frac{u}{R} = \eta - Gu$, avec $\displaystyle \eta = \sum_j \epsilon_j \eta_j$ et $\displaystyle G = \frac{1}{R} = \sum_j G_j = \sum_j \frac{1}{R_j}$ où $\epsilon_j = 1$ si $\eta_j$ est de même sens que $i$, sinon $\epsilon_j = -1$.
> - Association de condensateurs idéaux : $i = C\dfrac{du}{dt}$, avec $\displaystyle C = \sum_j C_j$.
> - Association de bobines idéales : $\dfrac{di}{dt} = \frac{u}{L}$, avec $\displaystyle \frac{1}{L} = \sum_j \frac{1}{L_j}$.

> [!note] Pont diviseur de courant
> Étudions la relation entre l’intensité traversant un dipôle et l’intensité totale traversant l’association des dipôles en parallèle ([[#^figure5|fig. 5]]). A partir de la figure, le pont diviseur de courant nous donne : $i_2 = \frac{R_1}{R_1 + R_2}i = \frac{G_2}{G_1 + G_2}i$.

> [!note] Expression de la loi des nœuds en termes de potentiels pour un circuit composé de résistors et de générateurs (Exemple : Application 6 page 55)
> Pour calculer la différence de potentiel $u$ dans le montage de la [[#^figure6|figure 6]], on pose $u_M = 0$. Il reste deux potentiels inconnus : $u_A$ et $u_B$. Appliquons la loi des noeuds en termes de potentiels :
> - en A : $\frac{E - u_A}{2R} + \frac{0 - u_A}{2R} + \frac{u_B - u_A}{R} = 0$ ;
> - en B : $\frac{u_B - u_A}{R} + \frac{0 - u_B}{3R} - \eta = 0$.
> 
> Ces deux équations forme un système linéaire qu'on peut résoudre pour trouver $u_A$ et $u_B$ et ainsi déterminer $u = u_B - u_A$.
# Définitions

# Diagrammes
Association de dipôles
![[electronique1/attachments-electronique1/figure40.png]]^figure1

Maille analysée en une association en série de dipôles
![[electronique1/attachments-electronique1/figure41.png]]^figure2

Pont diviseur de tension
![[electronique1/attachments-electronique1/figure42.png]]^figure3

Association en parallèle de deux dipôles
![[electronique1/attachments-electronique1/figure43.png]]^figure4

Pont diviseur de courant
![[electronique1/attachments-electronique1/figure44.png]]^figure5

Montage d’étude
![[electronique1/attachments-electronique1/figure45.png]]^figure6
# Graphiques

# Expériences

# Autres notes
> [!warning]
> Si une source de tension idéale est associée en parallèle avec un dipôle (qui n'est pas assimilable à une source de tension), l'ensemble est équivalent à la source de tension seule.