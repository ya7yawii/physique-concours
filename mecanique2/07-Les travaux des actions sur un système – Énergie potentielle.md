---
titre: "[[07-Les travaux des actions sur un système – Énergie potentielle]]"
tags:
  - puissance
  - travail
  - énergie-potentielle
crée: 19-10-2025, 10:54
---
# Formules
Puissance d'un système de forces : $\displaystyle P = \sum_{i=1}^{N} \overrightarrow{f_i} . \overrightarrow{v}_i$

Travail d'un système de forces entre les instants $t_1$ et $t_2$ : $\displaystyle W(t_1, t_2) = \int_{t_1}^{t_2} \delta W$ avec $\displaystyle \delta W = P dt = \sum_{i=1}^{N} \overrightarrow{f_i} . \overrightarrow{v}_i dt = \sum_{i=1}^{N} \overrightarrow{f_i} . d\overrightarrow{OP_i}$

Force conservative : $\overrightarrow{f} = -\overrightarrow{grad}\,e_p$ ou encore $de_p = -\overrightarrow{f} . d\overrightarrow{OP}$ où la fonction $e_p(P)$ est ==**l'énergie potentielle**== de la force $\overrightarrow{f}$. On dit que la force $\overrightarrow{f}$ dérive de l'énergie potentielle $e_p$.

Énergie potentielle des forces extérieures conservatives : $\displaystyle E_{p\,ext} = \sum_{i=1}^{N} e_{p\,i\,ext}$ ; S'il existe pour chaque force $\overrightarrow{f}_{i\,ext}$ une fonction potentielle $e_{p\,i\,ext}$ telle que $\overrightarrow{f}_{i\,ext} = -\overrightarrow{grad}\,e_{p\,i\,ext}$. S'il existe plusieurs types de forces s'appliquant sur le système, il faut considérer la somme des énergies potentielles de chacun des types.

> [!note] Énergie potentielle des forces intérieures conservatives
> On suppose qu'il existe pour chaque force intérieure conservative $\overrightarrow{f}_{i \rightarrow j}$, exercée par le point $P_i$ sur le point $P_j$, une fonction énergie potentielle $e_p(P_i, P_j)$ telle que : $\overrightarrow{f}_{i \rightarrow j} = -\overrightarrow{grad}_{P_j}\,e_{p}(P_i, P_j)$ ou encore $de_p(P_i, P_j) = \overrightarrow{grad}_{P_j}\,e_{p}(P_i, P_j) . d\overrightarrow{P_jP_i}$ pour tout déplacement $d\overrightarrow{P}_j$ (Preuve : corrigé de la question 4 de la section "Tester ses connaissances" page 162) ; Soit l'opérateur gradient $\overrightarrow{grad}_{P_j}$ est formé par les dérivées des coordonnées du point $P_j$.
> Propriétés : $e_p(P_i, P_j) = e_p(P_j, P_i)$ et $\overrightarrow{grad}_{P_i}\,e_{p}(P_i, P_j) = -\overrightarrow{grad}_{P_j}\,e_{p}(P_i, P_j)$.
> L'énergie potentielle des forces extérieures $E_{p\,int}$ du système $(S)$ est alors définie par : $\displaystyle E_{p\,int} =\frac{1}{2} \sum_{i=1}^{N} \sum_{\substack{j=1\\i \neq j}}^{N} e_{p}(P_i, P_j)$.
> La présence du facteur 1 ⁄ 2 s'explique par le fait que sous les signes somme, on compte deux fois chaque couple de points en interaction. On peut aussi écrire cette somme en regroupant les deux termes associés à un même couple d'indice : $\displaystyle E_{p\,int} = \sum_{i=1}^{N} \sum_{j=1}^{j=i-1} e_{p}(P_i, P_j)$.

> [!note] Énergie potentielle totale
> L'énergie potentielle totale (ou énergie potentielle) est donnée par : $E_p = E_{p\,int} + E_{p\,ext}$.
> La puissance $P$ et le travail $W (t_1, t_2)$ d'un système de forces $\{\overrightarrow{f}_i\}_{i = 1\,\ldots\,N}$ dérivant d'une énergie potentielle $E_p$ s'expriment par :
> $P(t) = -\dfrac{dE_p}{dt}$ et $W (t_1, t_2) = -\Delta E_p = E_p(t_1) - E_p(t_2)$.

> [!note] Puissance et travail des actions exercées sur un solide
> Dans le cas d'un solide, la puissance des forces a une expression simple. Elle ne nécessite la connaissance que des grandeurs suivantes :
> - le torseur des actions extérieures : la résultante et le moment des actions $\{\overrightarrow{F}, \overrightarrow{M}_A\}$ ;
> - le torseur cinématique : la vitesse angulaire instantanée et la vitesse d'un point A lié au solide $\{\overrightarrow{\Omega}, \overrightarrow{v}(A)\}$.
> 
> Alors : $P = \overrightarrow{F} . \overrightarrow{v}(A) + \overrightarrow{\Omega}\, . \overrightarrow{M}_A$. Il est important de noter que le point de réduction doit être le même dans les deux termes du second membre. En revanche, on peut utiliser n'importe quel point du solide. L'expression de la puissance est le [[#^def1|comoment]] du torseur cinématique $\{\overrightarrow{\Omega}, \overrightarrow{v}(A)\}$ et du torseur des actions $\{\overrightarrow{F}, \overrightarrow{M}_A\}$.

> [!note] Puissance des actions intérieures à un solide
> Les actions intérieures à un solide ont une puissance nulle $P_{int} = 0$ parce que pour <mark style="color: red">tout système</mark>, et donc aussi pour le solide, la résultante et le moment sont nuls : $\overrightarrow{F}_{int} = \overrightarrow{0}$ ; $\overrightarrow{M}_{A\,int} = \overrightarrow{0}$.
> Le solide est un cas très particulier de système matériel. <mark style="color: red">L'absence de déformation</mark> au sein du solide est responsable de la nullité de la puissance des actions intérieures.
> On déduit aussi de la définition du solide (indéformabilité) que le travail des actions intérieures est nul.

Puissance des actions de la liaison rotule sur le solide : $P_{rotule} = \overrightarrow{M}_A . \overrightarrow{\Omega}$ ([[#^figure1|fig. 1]]).

Puissance des actions de la liaison pivot sur le solide : $P_{pivot} = \overrightarrow{\Omega}\, . \overrightarrow{M}_A = \Omega M_{Az}$ ([[#^figure2|fig. 2]]).

$\text{Liaison rotule parfaite} \, \Leftrightarrow P_{rotule} = 0 \Leftrightarrow \overrightarrow{M}_{A\,rotule} = \overrightarrow{0}$.

$\text{Liaison pivot parfaite} \, \Leftrightarrow P_{pivot} = 0 \Leftrightarrow M_{Az} = 0$.
# Définitions
==**Forces non conservatives**== :
Ce sont des forces qui n'admettent pas de fonction énergie potentielle. C'est le cas en particulier des forces de frottement, des réactions des supports, de la force de Lorentz (dans un champ électromagnétique non permanent), de la force d'inertie de Coriolis...
Dans ce cas, il faut calculer leur puissance et leur travail directement avec les deux premières formules de la section Formules.

==**Modèle des liaisons parfaites**== :
Une liaison est parfaite si la somme de la puissance des actions de cette liaison sur le solide et de la puissance des actions du solide sur cette liaison est nulle.
Dans le cas où le référentiel est lié à la liaison, cette dernière est parfaite si la puissance des actions de la liaison sur le solide est nulle.
# Diagrammes
![[mecanique2/attachments-mecanique2/figure32.png]]^figure1

![[mecanique2/attachments-mecanique2/figure33.png]]^figure2
# Graphiques

# Expériences

# Autres notes
> [!note] Comoment
> On appelle comoment le produit de deux torseurs. Pour plus d'infos sur le sujet, on peur consulter ce [lien](https://fr.wikipedia.org/wiki/Comoment).
^def1

> [!warning]
> La puissance des actions sur un solide dépend du référentiel d'étude alors que la puissance des actions intérieures est indépendante du référentiel. On peut trouver la preuve dans la section "tester ses connaissances" question 1 page 162.

> [!note] Énergie potentielle de pesanteur
> Pour un champ de pesanteur uniforme : $E_p = -M\overrightarrow{g} . \overrightarrow{AG}$ avec $A$ est un point fixe quelconque et $G$ est le centre de masse.