---
titre: "[[08-Le théorème d'Ampère]]"
tags:
aliases:
crée: 10-01-2026, 09:46
---
# Formules
> [!note] Circulation du champ d'un fil
> Sur les cartes de champ magnétique tracées au [[07-Champ magnétique|chapitre 7]], nous avons pu remarquer que les lignes de champ magnétique sont fermées. Ceci constitue une différence fondamentale avec le champ électrostatique : la circulation du champ magnétique sur un contour n’est pas nécessairement nulle.
> Nous utiliserons un cas élémentaire pour mettre en évidence cette propriété.
> - Champ créé par un fil rectiligne indéfini :
> Ce type de circuit modélise un circuit fermé comportant une portion rectiligne de longueur $L$ grande devant sa distance $r$ au point $M$ où est évalué le champ $\overrightarrow{B}(M)$. Notons $(r, \theta, z)$ les coordonnées cylindriques du point $M$. L’axe $(Oz)$ sera pris confondu avec le fil et son orientation sera celle du courant d’intensité $I$ ([[#^figure1|fig. 1]]). Tout plan contenant le fil est un plan de symétrie, donc le champ est orthoradial : $\overrightarrow{B}(M) = B_{\theta}(r, \theta, z) \overrightarrow{e}_{\theta}$.
> L’axe $(Oz)$ étant un axe de révolution, le champ ne dépend pas de la coordonnée $\theta$ : $\overrightarrow{B}(M) = B_{\theta}(r, z) \overrightarrow{e}_{\theta}$.
> Enfin, le système étant invariant dans toute translation parallèle à $(Oz)$, le champ ne dépend pas davantage de la coordonnée $z$ : $\overrightarrow{B}(M) = B_{\theta}(r) \overrightarrow{e}_{\theta}$.
> L’élément de courant $d\overrightarrow{C}$, situé en $P$, crée le champ élémentaire : $d\overrightarrow{B} = \frac{\mu_0}{4\pi}\frac{d\overrightarrow{C}\wedge\overrightarrow{e}_{PM}}{PM^{2}}$.
> De $\overrightarrow{OP} = (z + r\tan\alpha)\overrightarrow{e}_z$ il vient $d\overrightarrow{C} = Id\overrightarrow{P} = I\frac{rd\alpha}{\cos^{2}\alpha}\overrightarrow{e}_z$.
> Par ailleurs, $PM = \frac{r}{\cos\alpha}$ donc : $d\overrightarrow{B} = \frac{\mu_0I}{4\pi}\frac{d\alpha\overrightarrow{e}_z\wedge\overrightarrow{e}_{PM}}{r} = \frac{\mu_0I}{4\pi}\frac{\cos\alpha d\alpha}{r}\overrightarrow{e}_{\theta}$.
> Le champ créé par le fil indéfini s’établit à : $\displaystyle\overrightarrow{B} = \frac{\mu_0I}{4\pi r}\overrightarrow{e}_{\theta}\int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}\cos\alpha d\alpha = \frac{\mu_0I}{2\pi r}\overrightarrow{e}_{\theta}$ et les lignes de champ sont des cercles d’axe $(Oz)$.

> [!note] Circulation du champ d'un fil
> - Circulation élémentaire du champ :
> En coordonnées cylindriques, le déplacement élémentaire d’un point $M$ s’écrit : $d\overrightarrow{M} = dr\,.\overrightarrow{e}_r + rd\theta\,.\overrightarrow{e}_{\theta} + dz\,.\overrightarrow{e}_z$.
> La circulation élémentaire du champ magnétique du fil est donc : $dC = \overrightarrow{B}\,.d\overrightarrow{M} = \mu_0\frac{I}{2\pi}d\theta$.
> - Circulation du champ sur un contour enlaçant le fil :
> La [[#^figure2|figure 2]] représente un contour enlaçant le fil dans le sens direct ; *ce contour est donc orienté*. Lorsque le point $M (r, \theta, z)$ décrit le contour $\Gamma$, l’angle $\theta$ varie de $0$ à $2\pi$ par valeurs croissantes. La circulation du champ sur ce contour se déduit immédiatement du résultat précédent : ==**$\displaystyle C_{\Gamma} = \oint_{\Gamma}\overrightarrow{B}\,.d\overrightarrow{M} = \mu_0 I$.**==
> Si le contour enlace le fil dans le sens indirect, la circulation vaut $C_{\Gamma} = -\mu_0 I$.
> - Circulation du champ sur un contour n’enlaçant pas le fil :
> Si le contour n’enlace pas le fil ([[#^figure3|fig. 3]]), la variation de l’angle lorsque $M$ décrit le contour $\Gamma$ est globalement nulle, donc : ==**$\displaystyle C_{\Gamma} = \oint_{\Gamma}\overrightarrow{B}\,.d\overrightarrow{M} = 0$.**==

> [!note] Circulation du champ d'un fil : Lien avec le courant électrique traversant le contour
> Sur la [[#^figure4|figure 4]] est représentée une surface $S$ s’appuyant sur le contour $\Gamma$ et orientée par celui-ci : un tire-bouchon tournant dans le sens choisi pour $\Gamma$ traverse la surface $S$ dans le sens de son vecteur normal unitaire $\overrightarrow{n}$.
> - Si le contour enlace une fois le fil dans le sens direct ([[#^figure4|fig. 4]]), le courant $I$ traverse la surface $S$, selon le sens de $\overrightarrow{n}$. Dans ce cas, $C_{\Gamma} = \mu_0 I$.
> - Si le contour enlace une fois le fil dans le sens indirect, le même courant $I$ traverse la surface $S$, selon le sens de $-\overrightarrow{n}$. Dans ce cas, $C_{\Gamma} = -\mu_0I= \mu_0(-I)$.
> - Si le contour n’enlace pas le fil, le courant à travers la surface $S$ est nul, que la surface $S$ ait une forme simple ([[#^figure5|fig. 5]]) ou un peu plus compliquée ([[#^figure6|fig. 6]]). Dans ce dernier cas, le courant traverse deux fois $S$, mais dans des sens opposés.
> 
> Nous pouvons nous demander si ces résultats sont vrais pour tous les choix de surface $S$ s’appuyant sur le contour $\Gamma$. Considérons donc deux surfaces, telles que $S_1$ et $S_2$, s’appuyant sur $\Gamma$ et orientées par celui-ci ([[#^figure7|fig. 7]]).
> En *régime indépendant du temps*, l’intensité $I$ du courant a la même valeur en tout point du fil ; les courants qui traversent $S_1$ et $S_2$ sont donc égaux.
> - En conclusion, nous admettrons que la circulation du champ magnétique $\overrightarrow{B}(M)$ créé par un courant filiforme de forme quelconque, le long d’un contour $\Gamma$ peut s’écrire de façon générale : $\displaystyle C_{\Gamma} = \oint_{\Gamma}\overrightarrow{B}\,.d\overrightarrow{M} = \epsilon\mu_0 I$.
> $\epsilon = 1$, si le courant $I$ traverse une surface $S$ orientée par $\Gamma$ dans le sens du vecteur normal $\overrightarrow{n}$ ;
> $\epsilon = -1$, si le courant $I$ traverse une surface $S$ dans le sens de $-\overrightarrow{n}$ ;
> $\epsilon = 0$, si aucun courant ne traverse $S$.

> [!note] Théorème d'Ampère
> Nous admettons la généralisation des résultats précédents dans le cas d’une distribution de courants $\mathcal{D}$ dont le vecteur $\overrightarrow{j}$ est à flux conservatif.
> Dans ce contexte, le théorème d’Ampère (admis) s’énonce ainsi :
> ==**La circulation du champ magnétostatique $\overrightarrow{B}$ créé par un ensemble de courants sur un contour $\Gamma$ orienté, est égale à la somme des courants enlacés par multipliée par $\mu_0$ : $\displaystyle C_{\Gamma} = \oint_{\Gamma}\overrightarrow{B}\,.d\overrightarrow{M} = \mu_0\sum_k\epsilon_k I_k$.**==
>==**$\epsilon_k = 1$, si $I_k$ traverse $S$ orientée par $\Gamma$ dans le sens de $\overrightarrow{n}$.**==
> ==**$\epsilon_k = -1$, si $I_k$ traverse $S$ dans le sens de $-\overrightarrow{n}$.**==
> ==**$\epsilon_k = 0$, si $I_k$ ne traverse pas $S$.**==
> 
> Par exemple, sur la [[#^figure8|figure 8]], nous avons : $C_{\Gamma} = \mu_0(I_1 - I_2 + 2I_3)$. La circulation ne dépend pas de $I_4$.
> De façon plus générale, nous pouvons aussi écrire $\displaystyle C_{\Gamma} = \mu_0\iint_S\overrightarrow{j}\,\overrightarrow{n}\,dS$, le résultat ne dépendant pas du choix de la surface $S$ s’appuyant sur la courbe de circulation $\Gamma$.
> *Remarques :*
> - *Il faut garder à l’esprit que le théorème d’Ampère n’est rigoureusement valable que pour les régimes indépendants du temps, donc en magnétostatique. En particulier, dans des cas où les lignes de courant sont interrompues, donnant lieu à des accumulations de charges, nous ne pouvons pas l’appliquer. Nous pouvons en revanche l’employer dans l’approximation des régimes quasi permanents lorsque le vecteur $\overrightarrow{j}$ est à flux conservatif. L’étude plus complète de cette difficulté sera faite en seconde année.*
> - *Nous excluons les cas exotiques tels que le contour rencontrant un circuit filiforme, ou encore un contour pour lequel il est impossible de trouver simplement une surface s’appuyant dessus.*

> [!note] Conséquences du théorème d'Ampère
> Ayant postulé la loi de Biot et Savart, nous avons montré que le champ magnétostatique est :
> - un champ dont le flux à travers toute surface fermée est nul ;
> - un champ lié à ses sources, les courants, par le théorème d’Ampère.
> 
> Comme pour le champ électrostatique, nous résumerons ces propriétés en seconde année sous la forme de lois locales.
> Les outils dont nous disposons nous permettent cependant d’aborder l’étude complète du champ : évolution locale et discontinuités du champ, calcul de celui-ci...
> ==**Le théorème d’Ampère et la conservation du flux magnétique sont deux propriétés qui permettent l’étude complète du champ magnétostatique.**==

> [!note] Calcul d'un champ magnétique à l'aide du théorème d'Ampère : Principe du calcul
> Comme le théorème de Gauss, le théorème d’Ampère est de formulation remarquablement simple. Pour une distribution de courants connue, nous pourrons calculer la circulation du champ sur des contours convenablement choisis pour en déduire l’expression du champ. Il faut que le lien entre la circulation et le champ soit élémentaire : champ magnétique d’expression déjà très simplifiée, contour de géométrie simple.
> ==**Le théorème d’Ampère permet une détermination rapide du champ magnétostatique pour des distributions de courants de symétries élevées. Après détermination de la forme du champ à l’aide de considérations de symétrie, son application à un *contour orienté de géométrie adaptée aux symétries du problème* permet de déterminer l’amplitude du champ.**==
> Le principe du calcul correspondra à la démarche exposée, ci-dessous, dans le cas de distributions de courants à symétries élevées.
> - Première étape : considérations de symétries :
> Il faut obtenir, à l’aide des symétries de la distribution, la forme du champ magnétique :
> 	- utilisation de plans de symétrie ou d’antisymétrie pour déterminer sa direction ;
> 	- utilisation d’invariance par rotation ou translation pour réduire la dépendance de ses composantes vis-à-vis des coordonnées... (il faut penser à utiliser un système de coordonnées adapté à la symétrie du problème).
> - Deuxième étape : choix du « contour d’Ampère » :
> La forme obtenue pour le champ détermine le choix de la courbe de circulation, dite « contour d’Ampère », afin d’obtenir sans peine la circulation du champ magnétique.
> - Troisième étape : application du théorème d’Ampère :
> Elle achève la détermination du champ magnétique.

> [!note] Calcul d'un champ magnétique à l'aide du théorème d'Ampère : Distribution à géométrie plane : nappe plane infinie
> Nous nous intéressons à la détermination du champ créé par une nappe de courant infinie dans le plan $(xOy)$, avec $\overrightarrow{j}_S = j_S \overrightarrow{e}_x$ ([[#^figure9|fig. 9]]).
> Une telle nappe de courants résulte de la modélisation surfacique d’un ensemble de courants filiformes, rectilignes, infinis, jointifs, d’intensité $I$, disposés parallèlement à l’axe $(Ox)$. Notons $n$ le nombre de fils coupant, par unité de longueur, l’axe $(Oy)$, il vient : $j_S = n\,I$.
> - Considérations de symétrie :
> La distribution est invariante par symétrie par rapport à tout plan parallèle à $(xOz)$, donc $\overrightarrow{B}(x, y, z) = B(x, y, z)\overrightarrow{e}_y$. L’invariance du problème par translation parallèlement à $(Ox)$ ou bien $(Oy)$ nous permet la simplification supplémentaire : $\overrightarrow{B}(x, y, z) = B(z)\overrightarrow{e}_y$.
> Notons aussi que le plan $(xOy)$ est un plan de symétrie de la distribution.
> Au point $M'$ symétrique du point $M$ par rapport à ce plan, le champ $\overrightarrow{B'}$ est l’opposé du symétrique du champ $\overrightarrow{B}$ en $M$ : la fonction $B(z)$ est impaire.
> - Choix du « contour d’Ampère » :
> Un contour permettant un calcul aisé de la circulation doit posséder des côtés parallèles au champ, à $z = cte$, le caractère impair de $B(z)$ nous conduisant naturellement au choix du contour de [[#^figure9|figure 9]] : ce contour est constitué d’un rectangle de hauteur $2z$ suivant $(Oz)$, et de largeur $L$ suivant $(Oy)$ : l’orientation du contour apparaît en noir sur le schéma. La circulation du champ sur ce contour orienté est : $C = LB(z) + (-L) B(-z) = 2LB(z)$ (avec $z > 0$).
> - Champ magnétique :
> En appliquant le théorème d’Ampère à ce contour, nous avons (la normale à la surface est orientée suivant $-\overrightarrow{e}_x$ ) : $2LB(z) = -\mu_0\,j_S\,L$.
> Finalement le champ de la nappe est : $\overrightarrow{B} = -\frac{\mu_0\,j_S}{2}\,\text{signe}(z)\overrightarrow{e}_y$.
> 
> *Remarques :*
> - *En traversant la nappe de courant dans le sens de $\overrightarrow{e}_z$, le champ magnétique présente la discontinuité $\overrightarrow{B}(0_+) - \overrightarrow{B}(0_−) = \mu_0\,\overrightarrow{j}_S\wedge\overrightarrow{e}_z$.*
> - *La modélisation surfacique a considérablement simplifié le problème.*
> *Rigoureusement, pour un ensemble de courants filiformes identiques orientés selon $(Oy)$ et distants de $a$, les considérations de symétrie et d’invariance se limitent à la périodicité du champ : $\overrightarrow{B}(x, y, z) = \overrightarrow{B}(x + k\,a, y, z)$.*
> *Il est alors impossible d’utiliser le théorème d’Ampère pour calculer le champ.*
> *Une étude numérique montre que, l'écart relatif entre les deux calculs est inférieur à $10^{-3}$ dès que $z$ est supérieur à $1,5a$.*
# Définitions

# Diagrammes
Champ magnétique créé par l’élément de courant $d\overrightarrow{C}$ du fil infini
![[electromagnetisme1/attachments-electromagnetisme1/figure135.png]]^figure1

Contour $\Gamma$ enlaçant un fil dans le sens direct. (Remarquons que ce contour est orienté.)
![[electromagnetisme1/attachments-electromagnetisme1/figure136.png]]^figure2

Contour $\Gamma$ n’enlaçant pas le fil
![[electromagnetisme1/attachments-electromagnetisme1/figure137.png]]^figure3

Le courant $I$ traverse la surface $S$ s’appuyant sur le contour $\Gamma$ dans le sens de $\overrightarrow{n}$
![[electromagnetisme1/attachments-electromagnetisme1/figure138.png]]^figure4

Le courant $I$ ne traverse pas la surface $S$ s’appuyant sur le contour $\Gamma$
![[electromagnetisme1/attachments-electromagnetisme1/figure139.png]]^figure5

![[electromagnetisme1/attachments-electromagnetisme1/figure140.png]]^figure6

Courant traversant les deux surfaces s’appuyant sur $\Gamma$
![[electromagnetisme1/attachments-electromagnetisme1/figure141.png]]^figure7

La circulation de $\overrightarrow{B}$ sur le contour $\Gamma$ ne dépend que de $I_1$ , $I_2$ et $I_3$
![[electromagnetisme1/attachments-electromagnetisme1/figure142.png]]^figure8

Nappe plane infinie
![[electromagnetisme1/attachments-electromagnetisme1/figure143.png]]^figure9
# Graphiques

# Expériences

# Autres notes
