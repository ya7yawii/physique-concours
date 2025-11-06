---
titre: "[[01-Électrocinétique. Cadre et concepts de base]]"
tags:
  - intensité
  - tension
  - lois-de-Kirchhoff
  - loi-des-noeuds
  - loi-des-mailes
  - puissance
  - générateur
  - récepteur
crée: 05-11-2025, 19:49
---
# Formules
Intensité du courant : $\displaystyle i = \frac{\delta q}{\delta t}$.

Énergie potentielle d'un porteur de charge et potentiel : $\mathcal{E}_P = qv_{P}$ avec $v_{P}$ le potentiel en un point P d'un circuit électrique et $\mathcal{E}_P$ l'énergie potentielle d'un porteur de charge q qui se trouve au point P.

Tension entre deux points d'un circuit : $u_{AB} = v_A - v_B$ ; $u_{AB} = -u_{BA}$.
> [!note]
> Dans un schéma, le signe de la tension est indiqué par une flèche. Si la pointe de la flèche indique le point A, alors : $u = u_{AB} = v_A - v_B$.

> [!note] Potentiel en un point
> Nous pouvons décréter arbitrairement que le potentiel en un point est nul. Ce point détermine la masse du circuit. Sur la [[#^figure4|figure 4]], il s'agit du point M.
> Le potentiel en un point A est alors défini sans ambiguïté : $v_A = v_M + u_{AM}$, soit : $v_A = u_{AM}$

> [!note] Additivité des tensions
> Les tensions dans un circuit suivent une loi d'additivité. Reprenons le circuit représenté sur la [[#^figure4|figure 4]] : $u_{AB} = v_A - v_B = (v_A - v_C) + (v_C - v_D) + (v_D - v_B)$ d'où : $u_{AB} = u_{AC} + u_{CD} + u_{DB}$.
> Remarque : Il existe une similitude entre l'addition des tensions et celles des vecteurs : $\overrightarrow{AB} = \overrightarrow{AC} + \overrightarrow{CD} + \overrightarrow{DB}$.

> [!note] Lois de Kirchhoff
> - Loi des nœuds : Cette loi est une conséquence de la conservation de la charge électrique dans l'A.R.Q.S. La charge électrique ne peut pas s'accumuler au niveau des conducteurs que sont les nœuds. Pour un nœud donné, la somme des courants $i_j$ qui y aboutissent est égale à la somme des courants $i_k$ qui en repartent ([[#^figure11|fig. 11]]) ; $\displaystyle \sum_j i_j = \sum_k i_k$. De façon plus générale : pour un noeud donné : $\displaystyle \sum_k \epsilon_k i_k = 0$, $\epsilon_k$ vaut 1 si le courant $i_k$ aboutit sur le nœud et $-1$ s'il en repart.
> - Loi des mailles : Cette loi est une conséquence de l'additivité des tensions. Pour une maille orientée : $\displaystyle \sum_k \epsilon_k u_k = 0$, $\epsilon_k$ vaut 1 si la tension $u_k$ est orientée dans le sens de la maille et $-1$ dans le cas contraire ([[#^figure12|fig. 12]]).

> [!note] Puissance échangée par un dipôle
> En convention générateur, les flèches représentant la tension et le courant sont dans le même sens. La quantité $\mathcal{P} = ui$ représente la puissance électrique cédée par le dipôle au reste du circuit.
> En convention récepteur, les flèches représentant la tension et le courant sont en sens inverses. La quantité $\mathcal{P} = ui$ représente la puissance électrique reçue par le dipôle.

> [!note] Fonctionnement générateur ou récepteur d'un dipôle
> En convention récepteur :
> - Si $\mathcal{P} = ui > 0$ : le dipôle a un comportement récepteur, il reçoit de l'énergie électrique.
> - Si $\mathcal{P} = ui < 0$ :  le dipôle a un comportement générateur, il fournit de l'énergie électrique.
> 
> Si on adopte la convention générateur cela revient à changer pour un même système le signe du produit $ui$. Les conclusions sont donc inversées.

> [!warning] Différence entre convention et comportement
> La convention récepteur (ou générateur) concerne l'orientation de la tension et du courant. Elle dépend de la personne qui étudie le circuit.
> Le caractère (ou comportement) récepteur (ou générateur) d'un dipôle est une donnée physique.
> Il convient de ne pas confondre les deux notions.
# Définitions
==**Sens conventionnel du courant électrique**== :
Nous savons que le courant électrique résulte du déplacement de particules chargées (par exemple, les électrons) porteurs de charge. Il existe des particules de charge positive et des particules de charge négative.
Le sens conventionnel du courant est celui des porteurs de charges positives.

==**Conservation de la charge**== :
La charge électrique ne peut être ni créée, ni détruite : la conservation de la charge électrique est une loi fondamentale de la physique.
Un générateur ne crée aucune charge électrique, mais communique à ces dernières de l'énergie ; il met les charges en mouvement.

==**Sens du courant dans un circuit**== :
Le sens de déplacement des porteurs de charge mobiles dans un circuit est lié aux caractéristiques des éléments qui le constituent.
Dans le montage de la [[#^figure1|figure 1]], la pile joue le rôle d'une pompe à charge : en dehors de celle-ci, les électrons de conduction se déplacent du pôle $\ominus$ de la pile vers le pôle $\oplus$. Le courant électrique I engendré par ce déplacement est orienté dans le sens opposé.

==**Mesure du courant électrique**== :
Le courant électrique peut être mesuré à l'aide d'un ampèremètre. Cet appareil est polarisé, et possède une borne $\oplus$ et une borne $\ominus$ (souvent désignée par « COM »). Orienté dans le sens ➀ comme sur la [[#^figure2|figure 2]], il indiquera la valeur de $i_1$. Orienté en sens inverse ➁ ([[#^figure3|fig. 3]]), il indiquera la valeur de $i_2$.

==**Mesure de la tension**== :
Un voltmètre indique la valeur de la tension orientée de la borne $\ominus$ (souvent repérée par COM) à la borne $\oplus$. Si on inverse les bornes du voltmètre, celui-ci indique une valeur opposée, bien que la tension physique soit inchangée.

==**Régime indépendant du temps**== :
L'électrocinétique est le domaine de l'électromagnétisme, où les manifestations du mouvement des porteurs sont étudiées en termes de courants et de tensions. Si ces grandeurs sont constantes dans le temps, nous parlerons de ==**régime constant ou de régime indépendant du temps**==, ou encore de ==**régime stationnaire**==. Ces grandeurs sont alors généralement notées avec des lettres majuscules.

==**Régimes variables**== :
Si les tensions $u(t)$ et les intensités $i(t)$ dépendent du temps, on est en ==**régime variable**==. Les intensités et les tensions sont des grandeurs qui se propagent dans les conducteurs avec une vitesse finie (de l'ordre de $c = 3\, . 10^{8}\, m\, .\, s^{–1}$ vitesse de la lumière dans le vide). Ainsi, rigoureusement il n'est plus possible de parler d'intensité $i(t)$ à un instant donné $t$ dans un circuit (même lorsque ce dernier ne présente [[#^def1|aucune dérivation]]), car sa valeur dépend du point où nous l'évaluons. Le temps de propagation de l'intensité dans un circuit de longueur $l$ est $\tau = \frac{l}{c}$, où $c$ est sa vitesse de propagation. Si les temps intervenant dans l'étude du circuit (période, temps de montée du signal, temps d'acquisition des mesures, etc.) sont grands devant $\tau$ , les phénomènes de propagation ne se manifestent pas et il sera pertinent de les négliger. Un régime variable permettant cette approximation est un ==**régime quasi permanent**== ou un ==**régime quasi stationnaire**==.
==**Dans l'approximation des régimes quasi stationnaires (A.R.Q.S.), tous les effets liés à la propagation des signaux sous forme de tensions ou de courants sont négligés**==.
Toutes les expériences de travaux pratiques d'électricité et d'électronique sont réalisées dans le cadre de l'A.R.Q.S.

> [!note] Expression de la conservation de la charge dans l'A.R.Q.S
> En A.R.Q.S., un fil conducteur reste électriquement neutre. Ainsi, dans un métal, la charge négative des électrons de conduction est exactement compensée par celle des charges fixes. Pour conserver cette neutralité il est nécessaire que la charge entrant par la section $S1$ soit égale à la charge sortant par la section $S2$ ([[#^figure5|fig. 5]]). En terme d'intensité cela se traduit par : $i_1 = i_2$.
> Dans l'A.R.Q.S., l'intensité est la même en tout point d'un [[#^def1|circuit sans dérivation]].

==**Fil de connexion**== :
Un fil de connexion est un fil conducteur dont la faible résistance est négligeable devant les autres résistances du montage. En utilisation normale, aux bornes d'un fil de connexion, la ddp est négligeable devant les autres ddp qui se manifestent dans le montage.

==**Masse signal et masse carcasse**== :
- La masse signal symbolisée par ![[electronique1/attachments-electronique1/figure8.png]] est une référence des potentiels pour un circuit donné.
-  La masse carcasse symbolisée par ![[electronique1/attachments-electronique1/figure9.png]]  est reliée à la terre : son potentiel est constant et sa valeur est souvent conventionnellement fixée à zéro. Cette distinction est importante lors de la réalisation de montages électriques.

==**Composant**== :
En électrocinétique, la connaissance du fonctionnement interne des composants n'est pas nécessaire. Chacun d'eux est considéré comme une boîte noire dont l'accès se fait par des bornes.
Nous distinguerons essentiellement deux familles de composants :
- Les dipôles : L'accès se fait par une paire de bornes ou de pôles. Leur représentation générale est le rectangle : ![[electronique1/attachments-electronique1/figure10.png]]. Si le fonctionnement du dipôle ne dépend pas du sens du courant, il est symétrique ; dans le cas contraire, il est dissymétrique.
- Les multipôles : L'accès se fait par plus d'une paire de bornes. En particulier de nombreux composants peuvent être représentés par des quadripôles avec une paire de bornes d'entrée et une paire de bornes de sortie ([[#^figure6|fig. 6]]).

==**Nœud**== :
Un nœud est un point de jonction entre au moins trois fils de connexion. Attention, un nœud électrique peut être graphiquement éclaté, il en est souvent ainsi pour la masse signal de nombreux montages ([[#^figure7|fig. 7]]).

==**Branche**== :
Une branche est constituée par un ensemble de dipôles montés en série entre deux nœuds ([[#^figure8|fig. 8]]). Deux dipôles sont montés en série lorsqu'ils ont une borne commune et lorsqu'ils sont traversés par le même courant. Ainsi aucun des dipôles représenté dans la [[#^figure9|figure 9]] n'est monté en série.

==**Maille**== :
Une maille est un ensemble de branches formant un contour fermé que l'on peut parcourir en ne passant qu'une fois par chaque nœud intermédiaire ([[#^figure10|fig. 10]]). Une maille peut être orientée (arbitrairement).

==**Réseau**== :
Un réseau, ou circuit, est un ensemble de composants reliés par des fils de connexion qui peut être analysé en termes de nœuds, branches et mailles.

==**Conventions d'orientation**== :
Considérons le circuit élémentaire constitué d'un générateur (imaginons une pile) et d'un autre dipôle appelé récepteur. Le même courant $i(t)$ parcourt tout le circuit ; il est positif dans le cas représenté ([[#^figure13|fig. 13]]).
- Du point de vue du générateur, les flèches représentant $u$ et $i$ sont dans le même sens. C'est la convention générateur ([[#^figure14|fig. 14]]).
- Du point de vue du récepteur, les flèches représentant u et i sont dans le sens inverse. C'est la convention récepteur ([[#^figure15|fig. 15]]).
# Diagrammes
Sens conventionnel du courant dans les métaux dont les porteurs sont des électrons libres
![[electronique1/attachments-electronique1/figure1.png]]

Sens de déplacement des deux types de porteurs dans un semi-conducteur
![[electronique1/attachments-electronique1/figure2.png]]

Déplacement des charges de conduction et courant physique I résultant
![[electronique1/attachments-electronique1/figure3.png]]^figure1

Valeur lue à l'ampèremètre $i_1 = I$
![[electronique1/attachments-electronique1/figure4.png]]^figure2

Valeur lue à l'ampèremètre $i_2 = -I$
![[electronique1/attachments-electronique1/figure5.png]]^figure3

![[electronique1/attachments-electronique1/figure6.png]]^figure4

Intensité $i_1$ à travers $S_1$ est égale à $i_2$ celle à travers $S_2$
![[electronique1/attachments-electronique1/figure7.png]]^figure5

Représentation d'un quadripôle
![[electronique1/attachments-electronique1/figure11.png]]^figure6

Différentes présentations graphiques des nœuds
![[electronique1/attachments-electronique1/figure12.png]]^figure7

Exemple de branche : les dipôles sont en série
![[electronique1/attachments-electronique1/figure13.png]]^figure8

Aucun de ces dipôles n'est monté en série
![[electronique1/attachments-electronique1/figure14.png]]^figure9

Exemple de maille orientée
![[electronique1/attachments-electronique1/figure15.png]]^figure10

Illustration de la loi des noeuds : $i_1 + i_3 + i_4 = i_2 + i_5$ ou : $i_1 - i_2 + i_3 + i_4 - i_5 = 0$
![[electronique1/attachments-electronique1/figure16.png]]^figure11

Illustration de la loi des mailles : $-u_1 - u_2 + u_3 - u_4 = 0$ ou encore $u_1 + u_2 + u_4 = u_3$
![[electronique1/attachments-electronique1/figure17.png]]^figure12

![[electronique1/attachments-electronique1/figure18.png]]^figure13

Convention générateur
![[electronique1/attachments-electronique1/figure19.png]]^figure14

Convention récepteur
![[electronique1/attachments-electronique1/figure20.png]]^figure15
# Graphiques

# Expériences
> [!warning]
> Voici quelques fascicules de travaux pratiques sur le sujet de l'électrocinétique : le [lien 1](https://fss.rnu.tn/useruploads/files/D%C3%A9partement%20Physique/2022-2023/Fascule%20electrocin%C3%A9tique%20finale(1).pdf).
# Autres notes
> [!warning] Ordre de grandeur à connaître
> Le nombre d'atomes de cuivre par mètre cube de métal est $n \approx 10^{29}\, atomes\, . m^{-3}$.

> [!warning] Circuit sans dérivation
> Un circuit sans dérivation est un circuit en série, où les composants (dipôles) sont connectés les uns à la suite des autres, formant ainsi une seule boucle.
^def1