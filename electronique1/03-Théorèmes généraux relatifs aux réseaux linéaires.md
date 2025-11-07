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


# Définitions

# Diagrammes
Association de dipôles
![[electronique1/attachments-electronique1/figure40.png]]^figure1

Maille analysée en une association en série de dipôles
![[electronique1/attachments-electronique1/figure41.png]]^figure2

Pont diviseur de tension
![[electronique1/attachments-electronique1/figure42.png]]^figure3
# Graphiques

# Expériences

# Autres notes
