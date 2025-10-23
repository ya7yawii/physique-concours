---
titre: "[[06-Énergie cinétique d'un système matériel]]"
tags:
  - énergie-cinétique
  - théorème-de-Kœnig
crée: 17-10-2025, 15:55
---
# Formules
Énergie cinétique d'un système discret : $\displaystyle E_c = \sum_{i=1}^{N} \frac{1}{2}m_i\overrightarrow{v}_i^{2}$.
Énergie cinétique d'un système continu pour une distribution volumique : $\displaystyle E_c = \iiint_{V} \frac{1}{2}\rho(P)\overrightarrow{v}^{2}(P)dV$ ou $\displaystyle E_c = \iiint_{V} \frac{1}{2}\overrightarrow{v}(P)d\overrightarrow{p}$ avec $d\overrightarrow{p} = \rho(P)\overrightarrow{v}(P)dV$ représente la quantité de mouvement de l'élément en P.
> [!warning]
> Dans le cas d'un solide, il est inutile de calculer l'une des deux intégrales ci-dessus. On utilise l'une des expressions ci-dessous.

Énergie cinétique d'un solide : $E_c = \frac{1}{2} (\overrightarrow{P} . \overrightarrow{v}(A) + \overrightarrow{\Omega} . \overrightarrow{\sigma}_A)$. Soient $\overrightarrow{P}$  la résultante cinétique, $\overrightarrow{v}(A)$ la vitesse d'un point ==**lié au solide**== (Il n'est pas nécessaire que A appartienne à la distribution de matière. Il suffit en effet que A soit fixe dans le référentiel lié au solide), $\overrightarrow{\Omega}$ le vecteur vitesse angulaire instantané et $\overrightarrow{\sigma}_A$ le moment cinétique en A.

> [!note] Énergie cinétique d'un solide au centre de masse
> En considérant $A = G$ dans l'expression précédente, on obtient l'expression générale $E_c = \frac{1}{2} (\overrightarrow{P} . \overrightarrow{v}(G) + \overrightarrow{\Omega} . \overrightarrow{\sigma}_G)$ ou encore $E_c = \frac{1}{2}M\overrightarrow{v}^{2}(G) + \frac{1}{2}J_G\overrightarrow{\Omega}^{2}$ où $J_G$ est le moment d'inertie du solide par rapport à l'axe $\Delta_G$, passant par G et orienté par le vecteur $\overrightarrow{\Omega}$.
> L'énergie cinétique est la somme de deux termes, correspondant à la décomposition du mouvement général d'un solide, soit :
> - une translation de vitesse $\overrightarrow{v}(G)$ dont l'énergie cinétique est $\frac{1}{2}M\overrightarrow{v}^{2}(G)$ ;
> - une rotation de vecteur vitesse angulaire $\overrightarrow{\Omega}$ autour d'un axe $\Delta_G$ passant par G, dont l'énergie cinétique est $\frac{1}{2}J_G\overrightarrow{\Omega}^{2}$.

> [!note] Cas particuliers importants
> - Si le solide est en translation alors $E_c = \frac{1}{2}\overrightarrow{P} . \overrightarrow{v}(A) = \frac{1}{2}M\overrightarrow{v}^{2}(G)$ ;
> - Si le solide est en rotation autour de A alors $E_c = \frac{1}{2}\overrightarrow{\Omega} . \overrightarrow{\sigma}_A = \frac{1}{2}J_{\Delta}\Omega^{2}$ avec $J_{\Delta}$ est le moment d'inertie par rapport à l'axe instantané de rotation $\Delta$ passant par A et dirigé par $\overrightarrow{\Omega}$ ;
> - Dans le référentiel barycentrique $(R^*)$, on a $E_c^* = \frac{1}{2}J_{\Delta_G}\Omega^{2}$ où l'axe de rotation $\Delta_G$ passe par G.

> [!note] Second théorème de Koenig
> Le second théorème de Koenig concerne l'énergie cinétique d'un système matériel. Il permet de décomposer l'énergie cinétique d'un système quelconque en deux termes, d'une part l'énergie cinétique du centre de masse, d'autre part l'énergie cinétique barycentrique.
> $$E_c = \frac{1}{2}M\overrightarrow{v}^{2}(G) + E_c^*$$
> - le terme $\frac{1}{2}M\overrightarrow{v}^{2}(G)$ représente l'énergie cinétique de translation globale du système ;
> - le terme $E_c^*$ représente l'énergie cinétique du mouvement des points du système autour du centre de masse.
> 
> Dans le cas d'un solide, $E_c^* = \frac{1}{2}J_{\Delta_G}\Omega^{2}$ alors on retrouve le résultat précédent $E_c = \frac{1}{2}M\overrightarrow{v}^{2}(G) + \frac{1}{2}J_{\Delta_G}\overrightarrow{\Omega}^{2}$. Les deux contributions à l'énergie cinétique font apparaître la décomposition du mouvement en une translation décrite par le centre de masse à la vitesse $\overrightarrow{v}(G)$ et une rotation du solide dans le référentiel barycentrique, autour de G et de vecteur vitesse angulaire $\overrightarrow{\Omega}$.


# Définitions

# Diagrammes

# Graphiques

# Expériences

# Autres notes
