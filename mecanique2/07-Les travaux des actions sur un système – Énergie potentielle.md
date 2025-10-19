---
titre: "[[07-Les travaux des actions sur un système – Énergie potentielle]]"
tags:
aliases:
crée: 19-10-2025, 10:54
---
# Formules
Puissance d’un système de forces : $\displaystyle P = \sum_{i=1}^{N} \overrightarrow{f_i} . \overrightarrow{v}_i$

Travail d’un système de forces entre les instants $t_1$ et $t_2$ : $\displaystyle W(t_1, t_2) = \int_{t_1}^{t_2} \delta W$ avec $\displaystyle \delta W = P dt = \sum_{i=1}^{N} \overrightarrow{f_i} . \overrightarrow{v}_i dt = \sum_{i=1}^{N} \overrightarrow{f_i} . d\overrightarrow{OP_i}$

Force conservative : $\overrightarrow{f} = -\overrightarrow{grad}\,e_p$ ou encore $de_p = -\overrightarrow{f} . d\overrightarrow{OP}$ où la fonction $e_p(P)$ est ==**l'énergie potentielle**== de la force $\overrightarrow{f}$. On dit que la force $\overrightarrow{f}$ dérive de l'énergie potentielle $e_p$.

Énergie potentielle des forces extérieures conservatives : $\displaystyle E_{p\,ext} = \sum_{i=1}^{N} e_{p\,i\,ext}$ ; S'il existe pour chaque force $\overrightarrow{f}_{i\,ext}$ une fonction potentielle $e_{p\,i\,ext}$ telle que $\overrightarrow{f}_{i\,ext} = -\overrightarrow{grad}\,e_{p\,i\,ext}$. S’il existe plusieurs types de forces s’appliquant sur le système, il faut considérer la somme des énergies potentielles de chacun des types.

> [!note] Énergie potentielle des forces intérieures conservatives
> On suppose qu’il existe pour chaque force intérieure conservative $\overrightarrow{f}_{i \rightarrow j}$, exercée par le point $P_i$ sur le point $P_j$, une fonction énergie potentielle $e_p(P_i, P_j)$ telle que : $\overrightarrow{f}_{i \rightarrow j} = -\overrightarrow{grad}_{P_j}\,e_{p}(P_i, P_j)$ ou encore $de_p(P_i, P_j) = \overrightarrow{grad}_{P_j}\,e_{p}(P_i, P_j) . d\overrightarrow{P}_j$ pour tout déplacement $d\overrightarrow{P}_j$ ; Soit l'opérateur gradient $\overrightarrow{grad}_{P_j}$ est formé par les dérivées des coordonnées du point $P_j$.
> Propriétés : $e_p(P_i, P_j) = e_p(P_j, P_i)$ et $\overrightarrow{grad}_{P_i}\,e_{p}(P_i, P_j) = -\overrightarrow{grad}_{P_j}\,e_{p}(P_i, P_j)$.
> L’énergie potentielle des forces extérieures $E_{p\,int}$ du système $(S)$ est alors définie par : $\displaystyle E_{p\,int} =\frac{1}{2} \sum_{i=1}^{N} \sum_{\substack{j=1\\i \neq j}}^{N} e_{p}(P_i, P_j)$.
> La présence du facteur 1 ⁄ 2 s’explique par le fait que sous les signes somme, on compte deux fois chaque couple de points en interaction. On peut aussi écrire cette somme en regroupant les deux termes associés à un même couple d’indice : $\displaystyle E_{p\,int} = \sum_{i=1}^{N} \sum_{j=1}^{j=i-1} e_{p}(P_i, P_j)$.


# Définitions

# Diagrammes

# Graphiques

# Expériences

# Autres notes
