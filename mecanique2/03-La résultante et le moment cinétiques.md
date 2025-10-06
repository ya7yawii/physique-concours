---
titre: "[[03-La résultante et le moment cinétiques]]"
tags:
  - résultante
  - moment
  - cinétique
  - Kœnig
crée: 06-10-2025, 08:30
---
# Formules
Résultante cinétique du système discret de points matériels (ou quantité de mouvement totale du système): $\displaystyle\overrightarrow{P} = \sum_{i=1}^{N} m_i\overrightarrow{v}_i$.

Résultante cinétique pour une distribution continue de points matériels : $\displaystyle\overrightarrow{P} = \iiint_V \overrightarrow{v}(P)dm = \iiint_V \rho(P)\overrightarrow{v}(P)dV$ avec P étant le centre de masse des éléments infinitésimaux dV de masse $dm = \rho(P)dV$.

Résultante cinétique et centre de masse : $\overrightarrow{P} = M\overrightarrow{v}_G$ avec $\overrightarrow{v}_G = \dfrac{d\overrightarrow{OG}}{dt}$, G le centre de masse du système et $O$ un point quelconque fixe du référentiel d'étude.

Moment cinétique du système discret de points matériel : $\displaystyle\overrightarrow{\sigma}_A = \sum_{i=1}^{N} \overrightarrow{AP_i} \wedge \overrightarrow{p}_i = \sum_{i=1}^{N} \overrightarrow{AP_i} \wedge m_i\overrightarrow{v}_i$. Le moment cinétique nécessite, en plus de la définition du système et du référentiel, le choix d'un point de réduction « A ». Le point A est un point quelconque, fixe ou mobile dans $(R)$. Les dimensions du moment cinétique sont : $kg.m^{2}.s^{-1}$ ou encore $J.s$.

Moment cinétique pour une distribution continue de points matériels : $\displaystyle\overrightarrow{\sigma}_A = \iiint_V \rho(P)\overrightarrow{AP} \wedge \overrightarrow{v}(P)dV$.

Théorème de transport du moment cinétique : $\overrightarrow{\sigma}_B = \overrightarrow{\sigma}_A + \overrightarrow{BA} \wedge \overrightarrow{P}$.

> [!note] Référentiel barycentrique
> Le référentiel barycentrique $(R^*)$ du système $(S)$ est le référentiel <mark style="color: red">en translation</mark> par rapport à $(R)$ dans lequel G est <mark style="color: red">immobile</mark>. Il est souvent pratique d'utiliser pour $(R)$ et $(R^*)$ les mêmes vecteurs de base, par exemple $(\overrightarrow{e}_x, \overrightarrow{e}_y, \overrightarrow{e}_z)$.
> Conséquences directes :
> - Par définition du référentiel barycentrique, la vitesse de G et son accélération sont nulles dans $(R^*)$ $\overrightarrow{v}_{G}^{*} = \overrightarrow{0}$, $\overrightarrow{a}_{G}^{*} = \overrightarrow{0}$.
> - La translation des axes de $(R^*)$ par rapport à ceux de $(R)$ implique que le vecteur vitesse angulaire de $(R^*)$ par rapport à $(R)$ est nul : $\overrightarrow{\Omega}_{(R^*) ⁄ (R)} = \overrightarrow{0}$.
> 
> Composition des vitesses et des accélérations : $\overrightarrow{v}(P)_{(R)} = \overrightarrow{v}^{*}(P) + \overrightarrow{v}_G$ et $\overrightarrow{a}(P)_{(R)} = \overrightarrow{a}^{*}(P) + \overrightarrow{a}_G$ avec $\overrightarrow{v}_G$ et $\overrightarrow{a}_G$ sont les vecteurs vitesse et accélération de G dans $(R)$.
> Conséquences sur les grandeurs cinétiques :
> - La résultante cinétique dans $(R^*)$ est nulle : $\overrightarrow{P}^{*} = \overrightarrow{0}$.
> - Le moment cinétique barycentrique $\overrightarrow{\sigma}^{*}$ est <mark style="color: red">indépendant du point de réduction</mark>. On peut le calculer à partir de tout point, en particulier à partir du centre de masse G.

> [!note] Premier théorème de Koenig
> $\overrightarrow{\sigma}_A = M\overrightarrow{AG} \wedge \overrightarrow{v}_G + \overrightarrow{\sigma}^{*}$ ou encore $\overrightarrow{\sigma}_A = \overrightarrow{AG} \wedge \overrightarrow{P} + \overrightarrow{\sigma}^{*}$.
> Il ne faut pas confondre ces expressions avec un théorème de transport !
> Il faut bien noter que ceci est une relation entre vecteurs définis dans deux référentiels différents : $\overrightarrow{\sigma}_A$ et $\overrightarrow{P}$ dans $(R)$ et $\overrightarrow{\sigma}^{*}$ dans $(R^*)$.
> Une écriture particulièrement utile et importante de ce théorème est celle où le point de réduction est le centre de masse G : $\overrightarrow{\sigma}_G = \overrightarrow{\sigma}^{*}$. Il y a égalité entre le moment cinétique barycentrique et le moment cinétique en G dans $(R)$.
> Le théorème de Koenig permet de décomposer le moment cinétique en somme de deux termes :
> - $\overrightarrow{\sigma}^{*}$ est le moment cinétique barycentrique ;
> - $M\overrightarrow{AG} \wedge \overrightarrow{v}_G$ est le moment cinétique en A, dans $(R)$, d'un <mark style="color: red">point matériel</mark> de masse M en G.
> 
> On peut montrer que cette décomposition s'applique à d'autres grandeurs cinétiques comme la résultante et l'énergie cinétiques.
# Définitions
==**Système fermé**== :
Un système est dit fermé ce qui signifie que sa masse est constante.
# Diagrammes

# Graphiques

# Expériences

# Autres notes
