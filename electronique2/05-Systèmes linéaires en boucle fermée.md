---
titre: "[[05-Systèmes linéaires en boucle fermée]]"
tags:
aliases:
crée: 29-11-2025, 10:49
---
# Formules
> [!note] Fonctions de transfert d'un système bouclé : Fonction d'asservissement
> - Fonction de transfert : Considérons le système représenté par le schéma fonctionnel de [[#^figure6|figure 6]]. La fonction de transfert relative à l'entrée principale est : $H(p) = \frac{S(p)}{E(p)} = \frac{G(p)}{1 + G(p)F(p)}$ où $G(p) = \frac{S(p)}{\epsilon(p)}$ correspond à la transmittance de la chaîne d'action et $F(p) = \frac{R(p)}{S(p)}$ à la transmittance de la chaîne de rétroaction.
> La fonction de transfert en boucle ouverte $T(p)$ est le produit des fonctions de transfert de la chaîne d'action $G(p)$ et de la chaîne de rétroaction $F(p)$ : $T(p) = \frac{R(p)}{\epsilon(p)} = G(p)F(p)$.
> Un système est à retour unitaire si $F(p) = 1$. $F(p)$ et $G(p)$ sont alors sans dimension. La fonction de transfert en boucle fermée d'un système à retour unitaire est ([[#^figure7|fig. 7]]) : $H(p) = \frac{S(p)}{E(p)} = \frac{G(p)}{1 + G(p)}$.
> - Cas d’une chaîne directe à grand gain : Dans la bande de pulsations (donc de fréquences) pour laquelle la fonction de transfert en boucle ouverte $T(j\omega)$ d’un système bouclé satisfait à l'inégalité  $|T(j\omega)| \gg 1$, nous avons : $\underline{H}(j\omega) = \frac{\underline{S}(j\omega)}{\underline{E}(j\omega)} = \frac{\underline{G}(j\omega)}{1 + \underline{G}(j\omega)\underline{F}(j\omega)} \approx \frac{1}{\underline{F}(j\omega)}$.
> Le système bouclé se comporte alors comme un système en chaîne ouverte dont la fonction de transfert ne dépend que des caractéristiques de sa chaîne de rétroaction.
> Ces dernières peuvent être fixées avec précision, ce qui n’est pas le cas des caractéristiques de la chaîne d’action qui dépendent généralement du point de fonctionnement, de la température, de la fréquence, etc.
> Les défauts de la chaîne d’action (décalages, dérives des composants, etc.) n’affectent plus de comportement du système bouclé.
> Cette propriété remarquable, qui conjugue stabilité de fonctionnement et insensibilité aux variabilités, est largement utilisée lors de la réalisation des systèmes asservis.
> - Condition de stabilité : Un système de fonction de transfert $H(p) = \frac{N(p)}{D(p)}$ est stable (cf. [[03-Étude temporelle des systèmes linéaires|chapitre 3]]), si :
> 	- le degré du polynôme $N(p)$ est au plus égal à celui du polynôme $D(p)$ ;
> 	- les pôles de $H(p)$, c’est-à-dire les zéros de $D(p)$, sont à partie réelle strictement négative. Pour qu’un système bouclé soit stable il est nécessaire que les zéros de $1 + T(p)$ soient à partie réelle strictement négative.
> - Précision : La précision $\epsilon_s(t)$ d’un système asservi est égale à la différence entre la valeur désirée $s_d(t)$ et la valeur réelle $s(t)$ de la grandeur de sortie : $\epsilon_s(t) = s_d(t) - s(t)$.
> La précision statique est égale la valeur prise par $\epsilon_s(t)$ en régime permanent. Pour préciser cette notion étudions un système où la grandeur d’entrée est égale à la valeur souhaitée de la grandeur de sortie et notons $G_0$ et $F_0$ les valeurs de $G(p)$ et $F(p)$ en régime permanent (soit $p = j\omega = 0$).
> La fonction de transfert en régime statique est : $H_0 = \frac{G_0}{1 + G_0F_0} = \frac{s}{s_d}$.
> La précision statique est donc : $\epsilon_{s,\,0} = s_d\frac{1 + G_0(F_0 - 1)}{1 + G_0F_0}$.
> Si, par exemple, la chaîne de rétroaction est unitaire $(F_0 = 1)$, la précision statique est d’autant plus grande que le gain statique de la chaîne d’action est grand.
> La précision dynamique $\epsilon_s(t)$, qui est plus délicate à étudier, dépend de la forme du signal envoyé en entrée.


# Définitions
==**Système en boucle fermée**== :
Les systèmes peuvent être classés en deux catégories : les systèmes en boucle ouverte, qui fonctionnent en ignorant les effets de leurs actions, et les systèmes en boucle fermée, qui considèrent ces effets pour corriger leurs comportements de manière a réaliser, aussi fidèlement que possible, les opérations pour lesquelles ils ont été conçus. Les systèmes en boucle fermée sont irremplaçables dans toutes les situations où il est impossible de commander un système à l'aide d’un programme figé préalablement établi. Aussi se trouvent-ils, non seulement dans toutes les branches de l'industrie, mais encore dans tous les domaines du monde vivant. Les êtres vivants utilisent une multitude de boucles de rétroaction pour maintenir aux niveaux requis les flux de matière et d’ énergie. Ils emploient des processus bien plus élaborés où non seulement la rétroaction mais encore la mémorisation, l'apprentissage, l’auto-adaptation et l’intelligence sont en synergie.

==**Fonctionnement en boucle fermée : Principe de la boucle de rétroaction**== :
Très tôt s’est imposée l’idée qu’il fallait qu’un système comporte une boucle de rétroaction pour qu’il puisse prétendre à de bonnes performances dans des conditions d’utilisation variées.
Ces systèmes imitent grossièrement le comportement humain qui peut s’analyser, dans les cas simples, en trois démarches : observation, traitement de l'information recueillie et action.
Sur ce principe, les systèmes en boucle fermée, ou systèmes bouclés, seront construits selon le schéma fonctionnel de [[#^figure1|figure 1]]. L'originalité de ce schéma fonctionnel, par rapport à ceux que nous avons rencontrés jusqu’à présent, tient au bouclage qui permet au système d’examiner les effets de son action.
==**Un système bouclé contient au moins une boucle de rétroaction qui permet au système de considérer les effets de son action et d’adapter en conséquence, sans intervention extérieure, la commande en vue de l'objectif fixé.**==
Le meilleur véhicule de l’information est le signal électrique. Aussi dans la plupart des systèmes bouclés, la partie traitement de l'information est de nature électrique ou électronique sans préjuger de la nature des autres parties du système.

==**Structure générale d'un système linéaire bouclé**== :
==**Éléments constitutifs des systèmes bouclés**== :
Les systèmes en boucle fermée possèdent en commun un certain nombre d’éléments qui sont les capteurs, les actionneurs et les organes de traitement de l'information.
- Les capteurs : Ce sont des organes dont le rôle est de transformer une grandeur physique en une autre. Parmi les capteurs, citons :
	- les potentiomètres qui transforment une position en une tension électrique ;
	- les accéléromètres qui transforment une accélération en un déplacement (ou une tension électrique) ;
	- les thermocouples qui transforment une température en une tension électrique ;
	- les capteurs de vitesse qui transforment une vitesse de rotation en une tension électrique.
- Les actionneurs : Ce sont des organes de puissance qui commandent directement les systèmes à asservir et à réguler. Parmi les actionneurs usuels, citons les servomoteurs, les vérins et les amplificateurs de puissance. Dans ce dernier cas, les systèmes à commander sont de nature électrique ou électronique.
- Les organes de traitement de l'information : Ces organes, qui travaillent à faible ou moyenne puissance, ont pour rôle de traiter les informations fournies par les capteurs. L'un d'entre eux est inhérent à la structure des systèmes bouclés, il s’agit du comparateur, ou soustracteur, qui élabore l'écart (ou l’erreur) $\epsilon(t)$. Cet élément peut être réalisé de plusieurs manières selon la nature du système bouclé : différentiel mécanique, amplificateur différentiel, synchrodétecteur différentiel, circuit soustracteur, etc. Il peut même ne pas être matérialisé mais résulter d’une association convenable des circuits comme cela est le cas en électronique. Le niveau énergétique des informations est généralement faible par rapport à la puissance fournie par le système. Il convient alors de les amplifier. Ainsi, parmi les organes de traitement de l’information, se trouve des préamplificateurs et des amplificateurs. Pour améliorer les performances de certains systèmes bouclés, il est nécessaire d’associer aux amplificateurs des circuits correcteurs dont le rôle est de modifier la structure de l'information.
Le schéma fonctionnel général d'un système bouclé à une entrée $E(p)$ est donné sur la [[#^figure2|figure 2]].
==**Schémas fonctionnels d’un système bouclé linéaire**== :
En l’absence de perturbations ou lorsqu’on ne considère que la fonction asservissement, le schéma fonctionnel d’un système bouclé est représenté sur la [[#^figure3|figure 3]]. C’est son schéma fonctionnel asservissement.
Dans ce schéma fonctionnel, nous distinguons :
- la chaîne directe, ou chaîne d’action, de transmittance $G(p)$. Cette chaîne est une chaîne de puissance, car elle contient les amplificateurs et l’actionneur ;
- la chaîne de rétroaction ou encore chaîne de précision de transmittance $F(p)$, dont le rôle est de fournir une information aussi exacte que possible sur la grandeur de sortie $S(p)$.
Le schéma étudié ne comporte qu’une seule boucle de rétroaction qui permet de comparer l'entrée et la sortie du système. Une telle boucle est dite **boucle de rétroaction principale** pour la distinguer, éventuellement, des autres boucles qui pourraient se trouver à l’intérieur soit de la chaîne d’action, soit de la chaîne de rétroaction.
Lorsque les perturbations ne sont pas négligées, le schéma fonctionnel du système est donné sur la [[#^figure4|figure 4]].
Signalons que la difficulté pour l’établissement d’un tel schéma tient généralement à la détermination du point d’application de la perturbation.
Si l'objet de l’étude est la fonction de régulation (c’est-à-dire l’influence des perturbations sur la grandeur de sortie) d’un système bouclé, alors l'entrée principale est nulle $E(p) = 0$ et le schéma fonctionnel utilisé peut être simplifié ([[#^figure5|fig. 5]]). Nous remarquerons que le signal $\epsilon(p) = -R_p(p)$ a été changé en $\epsilon(p) = +R_p(p)$ et corrélativement l'additionneur, placé au point d’entrée de la perturbation, est devenu un comparateur. Un tel schéma est appelé schéma fonctionnel régulation.


# Diagrammes
Schéma fonctionnel du principe des systèmes en boucle fermée
![[electronique2/attachments-electronique2/figure78.png]]^figure1

Structure générale d'un système bouclé linéaire
![[electronique2/attachments-electronique2/figure81.png]]^figure2

Schéma fonctionnel asservissement d'un système bouclé
![[electronique2/attachments-electronique2/figure82.png]]^figure3

Schéma fonctionnel d'un système bouclé en présence de perturbations
![[electronique2/attachments-electronique2/figure83.png]]^figure4

Schéma fonctionnel régulation d'un système bouclé
![[electronique2/attachments-electronique2/figure84.png]]^figure5

Schéma fonctionnel asservissement du système bouclé étudié
![[electronique2/attachments-electronique2/figure85.png]]^figure6

Système bouclé à retour unitaire
![[electronique2/attachments-electronique2/figure86.png]]^figure7
# Graphiques

# Expériences

# Autres notes
> [!warning] Un exemple de rétroaction linéaire : Application 1 page 152
> ![[electronique2/attachments-electronique2/figure79.png]]![[electronique2/attachments-electronique2/figure80.png]]

> [!warning] Application 2 page 156
> ![[electronique2/attachments-electronique2/figure87.png]]![[electronique2/attachments-electronique2/figure88.png]]