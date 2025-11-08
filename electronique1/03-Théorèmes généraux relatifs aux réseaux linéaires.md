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

> [!note] Relation de Millman
> $\displaystyle \left(\sum_{k \neq j} \frac{1}{R_{kj}}\right)u_j = \sum_{k \neq j} \left(\frac{u_k + e_{kj}}{R_{kj}} + \eta_{kj}\right)$ avec les f.e.m. et c.e.m. comptés positivement quand ils sont dirigés vers le noeud d'étude.
> <mark style="color: red">En appliquant la loi des nœuds en termes de potentiels, les calculs sont souvent plus simples que ceux entraînés par l’application de la relation de Millman pour laquelle il faut faire attention à l’orientation des f.e.m. et c.e.m.</mark>
> En revanche, la relation de Millman peut être utilisée simplement et sans risque d’erreur dans le cas où les branches qui arrivent au nœud sont des résistors. Elle s’écrit alors : $u_j = \frac{\displaystyle \sum_{k \neq j} G_{kj}u_k}{\displaystyle \sum_{k \neq j} G_{kj}}$ avec $G_{kj} = \frac{1}{R_{kj}}$ : conductance du dipôle reliant le noeud $j$ au noeud $k$ ([[#^figure7|fig. 7]]). En d’autres termes : Le potentiel d’un nœud qui n’est relié qu’à des résistors est égal au barycentre des potentiels des nœuds auxquels il est relié, chaque potentiel étant affecté d’un coefficient égal à la conductance de la branche correspondante.

> [!note] Théorème de superposition pour les régimes continus
> En régime permanent, l’intensité qui parcourt les dipôles constituant un réseau linéaire et la différence de potentiel à leurs bornes sont les sommes de ces grandeurs obtenues dans les différents états du réseau où toutes les sources libres, sauf une, sont éteintes.
> L’intérêt de ce théorème est qu’un réseau à source unique peut en général se résoudre plus simplement que par la résolution d’un système d’équations.
> Lors de l’application du théorème de superposition, <mark style="color: red">nous ne pouvons éteindre que des sources libres</mark>.
> L’utilisation du théorème de superposition associé aux formules sur les ponts diviseurs évite souvent la résolution de systèmes d’équations à plusieurs inconnues.
> Dans le cas de sources liées, l’application du théorème de superposition n’est souvent pas plus simple que l’utilisation de la loi des nœuds en termes de potentiels.
> La linéarité des équations est aussi vraie en régime variable. Cependant l’application du théorème de superposition nécessite, dans ce cas, un traitement particulier des conditions initiales (charge des condensateurs, courant dans les bobines...).
> On prend l'application 8 page 58 comme exemple pour cette théorème : (Voici la corrigée) :
> Pour calculer la différence de potentiel $u$ dans le montage de la [[#^figure8|figure 8]], on n'éteint d'abord que la source de courant ([[#^figure9|fig. 9]]). En utilisant le pont diviseur de tension, nous trouvons : $u_1 = -\frac{1}{4}u_{AM}$. La résistance équivalente $R_1$ entre $A$ et $M$ est donnée par : $\frac{1}{R_1} = \frac{1}{2R} + \frac{1}{R + 3R}$. Sur le schéma équivalent ([[#^figure10|fig. 10]]), l'application du pont diviseur donne : $u_{AM} = E . \frac{R_1}{R_1 + 2R}$ et on trouve ainsi $u_1$.
> Ensuite, on n'éteint que la source de tension ([[#^figure11|fig. 11]]), la résistance équivalente à la partie grisée du circuit est $R' = 2R$. L’application de la tension du pont diviseur de courant donne : $i' = \frac{3R}{2R + 3R}\eta$, d'où $u_2 = -Ri'$.
> La <mark style="color: red">superposition</mark> des deux états donne : $u = u_1 + u_2$. 

> [!note] Résolution d'un réseau par équivalences successives
> - Associations de résistances et ponts diviseurs : Cherchons les intensités des courants dans le circuit représenté sur la [[#^figure12|figure 12]]. Pour cela, nous allons calculer $i_0$ puis en déduire les autres par divisions de courant. Entre les points $C$ et $C'$ , nous avons une résistance $2R + R$ en parallèle sur $6R$, soit une résistance équivalente : $R_{CC'} = 2R$. Nous remplaçons ce bloc de trois résistances par une résistance $R_{CC'} = 2R$ ([[#^figure13|fig. 13]]). Notons que cette équivalence n’est vraie que pour la partie gauche du circuit car les courants $i_3$ et $i_4$ ne sont plus distingués sur le circuit équivalent. En réitérant deux fois cette opération, nous obtenons successivement les résistances équivalentes : $R_{BB'} = 2R$ et $R_{AA'} = 2R$. $i_0$ se calcule à partir du circuit équivalent à maille unique ([[#^figure14|fig. 14]]) : $i_0 = \frac{e}{3R}$.


# Définitions
> [!note] Extinction d’une source libre
> - Une source de tension éteinte (sa f.e.m. est nulle) peut être remplacée par un court-circuit (ou un fil).
> - Une source de courant éteinte (son c.e.m. est nul) peut être remplacée par un circuit ouvert.
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

Définitions des diverses grandeurs pour l’application de la loi des nœuds en termes de potentiels ou du théorème de Millman
![[electronique1/attachments-electronique1/figure46.png]]^figure7

Montage d'étude
![[electronique1/attachments-electronique1/figure47.png]]^figure8

Montage après extinction de la source de courant
![[electronique1/attachments-electronique1/figure48.png]]^figure9

Pont diviseur
![[electronique1/attachments-electronique1/figure49.png]]^figure10

Montage après extinction de la source de tension
![[electronique1/attachments-electronique1/figure50.png]]^figure11

Exemple de circuit
![[electronique1/attachments-electronique1/figure51.png]]^figure12

Circuit équivalent
![[electronique1/attachments-electronique1/figure52.png]]^figure13

Circuit équivalent vu de la source
![[electronique1/attachments-electronique1/figure53.png]]^figure14
# Graphiques

# Expériences

# Autres notes
> [!warning]
> Si une source de tension idéale est associée en parallèle avec un dipôle (qui n'est pas assimilable à une source de tension), l'ensemble est équivalent à la source de tension seule.