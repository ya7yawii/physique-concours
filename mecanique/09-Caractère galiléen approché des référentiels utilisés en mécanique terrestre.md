---
titre: "[[09-Caractère galiléen approché des référentiels utilisés en mécanique terrestre]]"
tags:
aliases:
crée: 18-09-2025, 17:23
---
# Formules
> [!note] Relation fondamentale de la dynamique dans $\mathcal{R}_O$
> $m\overrightarrow{a}(M)_{/\mathcal{R}_O} = \overrightarrow{F_a} + m[\overrightarrow{\mathcal{G_T}}(M) + \overrightarrow{\mathcal{G_L}}(M) + \overrightarrow{\mathcal{G_S}}(M) + \cdots \,] - m\overrightarrow{a}(O)_{/\mathcal{R}_C}$ où le terme $m[\overrightarrow{\mathcal{G_T}}(M) + \overrightarrow{\mathcal{G_L}}(M) + \overrightarrow{\mathcal{G_S}}(M) + \cdots \,]$ traduit les forces gravitationnelles exercées par la Terre, la Lune, le Soleil, les autres planètes, le terme $- m\overrightarrow{a}(O)_{/\mathcal{R}_C}$ est la force d’inertie d’entraînement puisque le référentiel $\mathcal{R}_O$ est en translation dans $\mathcal{R}_C$ et $\overrightarrow{F_a}$ représente d’éventuelles forces appliquées résultant d’autres interactions matérielles avec le point M.
> Le mouvement du centre d’inertie O de la Terre peut être étudié dans le référentiel galiléen $\mathcal{R}_C$ en l’assimilant à un point matériel de masse $M_T$, soit : $M_T\overrightarrow{a}(O)_{/\mathcal{R}_C} = M_T[\overrightarrow{\mathcal{G_L}}(O) + \overrightarrow{\mathcal{G_S}}(O) + \cdots \,]$. En reportant dans l’équation du mouvement de la masse m, nous obtenons : $m\overrightarrow{a}(M)_{/\mathcal{R}_C} = \overrightarrow{F_a} + m\overrightarrow{\mathcal{G_T}}(M) + [(\overrightarrow{\mathcal{G_L}}(M) - \overrightarrow{\mathcal{G_L}}(O)) + (\overrightarrow{\mathcal{G_S}}(M) - \overrightarrow{\mathcal{G_S}}(O)) + \cdots \,]$. On nomme le terme $m[\overrightarrow{\mathcal{G}}_{autres \, astres}(M) - \overrightarrow{\mathcal{G}}_{autres \, astres}(O)]$ le terme différentiel (ou terme de marée). Le terme d’accélération différentielle dû à un astre A est défini par : $\overrightarrow{\gamma_A} = \overrightarrow{\mathcal{G_A}}(M) - \overrightarrow{\mathcal{G_A}}(O)$.
> Dans le domaine terrestre, le référentiel géocentrique $\mathcal{R}_O$ est remarquablement galiléen, si on néglige le terme différentiel de marée ; le seul champ gravitationnel à considérer est alors celui créé par la Terre (voir la [[#^demo1]]).

> [!note] Effet d’accélération différentielle
> Imaginons un vaisseau spatial « tombant en chute libre » (mouvement de translation) dans le champ gravitationnel de la Terre, en négligeant toute autre attraction.
> C désignant le centre d’inertie du vaisseau, la relation fondamentale de la dynamique appliquée à ce point matériel particulier dans le repère géocentrique de cet astre supposé galiléen donne : $\overrightarrow{a}(C) = \overrightarrow{\mathcal{G_T}}(C)$
> Dans le référentiel $\mathcal{R}_v$ lié au vaisseau, dont l’accélération d’entraînement est $\overrightarrow{a}(C)$, la relation fondamentale de la dynamique appliquée à un point-matériel s’écrit : $m\overrightarrow{a}(M)_{/\mathcal{R}_v} = \overrightarrow{F_a} + m\overrightarrow{\mathcal{G_T}}(M) - m\overrightarrow{\mathcal{G_T}}(C) = \overrightarrow{F_a} + \overrightarrow{\gamma_v}(M)$. Le terme $\overrightarrow{\gamma_v}(M)$ est le terme différentiel relatif à notre problème.
> Négligeant ici l’effet directionnel et posant $\overrightarrow{\mathcal{G_T}}(C) = -\mathcal{G}_0\overrightarrow{e_z}$ nous voyons que :
> $$
> \begin{align*}
> \overrightarrow{e_z}.\overrightarrow{\gamma_v}(M) &= \overrightarrow{e_z}.[\overrightarrow{\mathcal{G_T}}(M) - \overrightarrow{\mathcal{G_T}}(C)]\\
> &= GM_T\left(\frac{1}{OC^{2}} - \frac{1}{OM^{2}}\right)\\
> &= \frac{GM_T}{OC^{2}}\left(1 - \frac{OC^{2}}{OM^{2}}\right)\\
> &= \frac{GM_T}{OC^{2}}\left(1 - \frac{OC^{2}}{OC^{2} + 2OC\times CM + CM^{2}}\right)\\
> &= \frac{GM_T}{OC^{2}}\left(1 - \frac{1}{1 + 2 \frac{z}{OC} + \frac{z^{2}}{OC^{2}}}\right) \approx \frac{2GM_T}{OC^{2}}\frac{z}{OC} = 2\mathcal{G}_0\frac{z}{r}
> \end{align*}
> $$
> Ainsi le terme différentiel agit comme précisé sur la [[#^figure1]] : un point matériel plus éloigné de O que ne l’est C est repoussé vers le « haut » tandis qu’un objet plus proche est attiré vers le « bas » de la cabine.

# Définitions
==**Référentiel de Copernic $\mathcal{R}_C$**== :
Le référentiel de Copernic, noté $\mathcal{R}_C$, est défini par la donnée du repère $(C ; \overrightarrow{e}_{x_C}, \overrightarrow{e}_{y_C}, \overrightarrow{e}_{z_C})$, où C est le centre de masse (ou d’inertie) du système solaire, et les axes $(Cx_C)$, $(Cy_C)$ et $(Cz_C)$ liés aux directions de trois étoiles suffisamment éloignées pour pouvoir être considérées comme fixes. Pour des points matériels mobiles dans le système solaire, ce référentiel est galiléen avec une excellente précision.

==**Référentiel de Kepler $\mathcal{R}_K$**== :
Le référentiel de Kepler $\mathcal{R}_K$ se déduit du référentiel de Copernic par translation : l’origine d’un repère képlérien, encore appelé repère héliocentrique, est le centre d’inertie S du Soleil, et ses axes $(Sx_K)$, $(Sy_K)$ et $(Sz_K)$ peuvent être choisis parallèles à ceux d’un repère spatial de $\mathcal{R}_C$. L’approximation consistant à supposer que K est galiléen est en général excellente.

==**Référentiel géocentrique $\mathcal{R}_O$**== :
Un repère spatial lié au référentiel géocentrique $\mathcal{R}_O$ a son origine au centre d’inertie $O = T$ de la Terre, et ses axes $(Ox_O)$, $(Oy_O)$ et $(Oz_O)$ sont respectivement parallèles à ceux du référentiel de Copernic. Ce référentiel géocentrique n’est pas galiléen puisque $\mathcal{R}_O$ décrit dans $\mathcal{R}_C$ un mouvement de translation quasi circulaire.

==**Théorie statique des marées océaniques**== :
Simplifions le problème en oubliant :
- la rotation de la Terre,
- le terme de marée dû à la présence de la Lune et du Soleil.
Avec ces hypothèses simplificatrices, la Terre est recouverte d’une couche uniforme d’eau. Nous appelons théorie statique des marées l’explication du phénomène des marées basée sur ces hypothèses simplificatrices.
Les limites de cette approche sont les approximations concernant le mouvement de la Lune, le mouvement des masses océaniques (par exemple, les ==bourrelets océaniques== ne sont plus alignés avec O et la Lune) et la considération de phénomènes de propagation jointe aux conditions aux limites locales (relief des côtes).

==**Référentiel terrestre $\mathcal{R}_T$**== :
II s’agit du référentiel $\mathcal{R}_T$ lié à la Terre, en rotation à vitesse angulaire $\overrightarrow{\omega_T}$ constante autour de l’axe des pôles géographiques, noté par la suite $(Oz)$, qui est fixe dans le référentiel géocentrique $\mathcal{R}_O$.
# Diagrammes

# Graphiques
Vaisseau spatial en chute libre :
![[figure76.png]]^figure1
# Expériences

# Autres notes
==**Jour solaire**== : 
Le jour solaire est l’intervalle de temps entre deux passages consécutifs du soleil au méridien d’un lieu. Un jour solaire vaut 24 heures ou 86 400 s.

==**Jour sidéral**== :
Le jour sidéral est l’intervalle de temps entre deux passages consécutifs d’une étoile lointaine « fixe » au méridien d’un lieu. C’est donc la période de rotation de la Terre dans le référentiel géocentrique. Un jour sidéral vaut exactement 86 164 secondes, correspond à une rotation complète de la Terre sur elle-même.

> [!warning] Pourquoi néglige-t-on généralement le terme de marée dans $\mathcal{R}_O$? ^demo1
> La démonstration dans le livre n'est pas détaillé donc voici la démonstration complète dans ces captures d'écran extraites de ce [lien](https://webetab.ac-bordeaux.fr/Etablissement/BDBorn/sections/postbac/prepasciences/physique/telech/docs20089/M11_2008-2009_RefGeoTer.pdf).
> ![[figure72.png]]
> ![[figure73.png]]
> ![[figure74.png]]
> ![[figure75.png]]

==**Marée**== :
La marée est la variation du niveau de la mer due à l'action gravitationnelle de la lune et du soleil. A cause de l’influence de la présence de la Lune, il existe deux marées hautes et deux marées basses par jour (par exemple marées hautes espacées de 12 heures, la hauteur des marées étant plus importante à l’équateur). Le Soleil apporte une contribution non négligeable au phénomène de marées. Donc, Aux pleine Lune et nouvelle Lune, les marées sont les plus importantes possibles ; nous parlons de marées de vives eaux. Aux premier quartier et dernier quartier, les marées sont d’amplitude les plus faibles possible, nous parlons alors de marées de mortes eaux.