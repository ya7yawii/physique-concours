---
titre: "[[02-Modélisation linéaire des composants usuels]]"
tags:
  - caractéristique-statique
  - dipôle
  - résistance
  - condensateur
  - bobine
  - électromoteur
  - point-de-fonctionnement
crée: 06-11-2025, 13:31
---
# Formules
> [!note] Résistance statique, résistance dynamique
> La résistance statique $R_0$ d'un composant passif au point de fonctionnement $M(U, I)$ est le rapport $R_0 = \frac{U}{I}$.
> Son inverse $G_0 = \frac{1}{R_0}$ est la conductance statique du dipôle ([[#^figure3|fig. 3]]).
> La résistance dynamique du dipôle, au point de fonctionnement $M$, est $r = \left(\dfrac{dU}{dI}\right)_{\!M}$. C'est l'inverse de la pente $g = \left(\dfrac{dI}{dU}\right)_{\!M}$ de la caractéristique statique $I = f (U)$ du dipôle ([[#^figure3|fig. 3]]).
> Pour de petites variations de la tension $u$ et du courant $i$ au voisinage du point M, nous pouvons assimiler localement la caractéristique à sa tangente et écrire : $\delta u = u - U$, $\delta i = i - I$, $\delta u \approx r . \delta i$.
> Au voisinage du point $M$, les variations de tension et courant sont proportionnelles : la caractéristique a été linéarisée.

> [!note] Étude en régime variable
> Supposons que le comportement du composant est inchangé lorsqu'on passe d'un régime statique à un régime variable, ou dynamique, c'est-à-dire que l'on a : $i(t) = f(u(t))$.
> La linéarisation précédente peut alors être utilisée pour relier de petites variations des tension $u(t)$ et courant $i(t)$ au voisinage du point de fonctionnement : $u(t)  \approx U + r(i(t) - I)$.
> Cette extension est souvent acceptable pour une résistance et quelques autres composants dans des domaines de fréquences restreints. Cette extension n'est cependant pas généralisable et devra être vérifiée expérimentalement pour préciser son domaine de validité.
> En régime variable, la trace du spot d'un oscilloscope, dont les déplacements horizontal et vertical sont proportionnels à la tension $u(t)$ et au courant $i(t)$ respectivement, donne la caractéristique dynamique du dipôle ([[#^figure4a|fig. 4a]] et [[#^figure4b|4b]]).
> Comme nous venons de le signaler, celle-ci peut s'identifier, s'écarter un peu, ou même différer complètement de la caractéristique statique, suivant le composant étudié et le régime de fonctionnement utilisé.
> La géométrie de la caractéristique dépend donc de l'excitation utilisée : forme du signal, amplitude, domaine de fréquence. Ces indications doivent alors accompagner la caractéristique dynamique pour pouvoir l'analyser.

> [!note] Dipôle linéaire
> Un dipôle linéaire est décrit par une équation différentielle d'évolution linéaire à coefficients constants de la forme : $a_0u(t) + a_1 \dfrac{du(t)}{dt} + a_2 \dfrac{d^{2}u(t)}{dt^{2}} + \ldots + b_0i(t) + b_1 \dfrac{di(t)}{dt} + b_2 \dfrac{d^{2}i(t)}{dt^{2}} + \ldots = F(t)$.
> La caractéristique statique d'un dipôle linéaire est une droite.
> Le dipôle est passif si le second membre de son équation d'évolution est nul : $F(t) = 0$ (c'est le cas pour une résistance). Le dipôle linéaire passif est symétrique.
> Le dipôle est actif si le second membre $F(t)$ est non nul : nous parlerons alors de source.
> Si la fonction $F(t)$ est intrinsèque au dipôle, nous parlerons de <mark style="color: red">source indépendante</mark> (par exemple, l'équation $u(t) = U_0 \cos\omega t$ caractérise un générateur idéal de tension sinusoïdale).
> Si ce second membre est contrôlé par des tensions ou courants dans d'autres branches du circuit, nous parlerons de <mark style="color: red">source liée</mark> (c'est, par exemple, le cas pour un amplificateur opérationnel utilisé dans un montage amplificateur de tension).

> [!note] Éléments dipolaires passifs
> - Résistor ou conducteur (ohmique) : Un résistor suit à tout instant la loi d'Ohm : $u(t) = Ri(t)$ en convention récepteur avec $R$ est la résistance du résistor s'exprime en ohm ($\Omega$), et $G = \frac{1}{R}$ est sa conductance en siemens (S). La caractéristique statique d'un résistor et ses caractéristiques dynamiques sont confondues en une droite passant par l'origine. La puissance instantanée reçue par un résistor est toujours positive : $\mathcal{P}(t) = Ri^{2}(t)$. Le résistor absorbe donc de l'énergie, mais n'en restitue jamais au circuit ([[#^figure5|fig. 5]]) : en recevant de l'énergie, l'élément tend à s'échauffer, et transfère de la puissance thermique au milieu environnant. Cet effet est recherché dans le fonctionnement d'un radiateur électrique.
> - Bobine idéale : La représentation symbolique figure sur la [[#^figure6|figure 6]]. Le fonctionnement de cet élément est basé sur le phénomène d'induction électromagnétique : les variations du courant dans la bobine créent une tension aux bornes de l'élément : $u(t) = L\dfrac{di(t)}{dt}$ où $L$ est l'inductance de la bobine en henry (H). En régime statique $i = I$ et $u = 0$, la caractéristique statique est donc confondue avec l'axe vertical $(O, I)$. <mark style="color: red">En régime constant ou statique (permanent, indépendant du temps) une bobine idéale se comporte comme un simple fil</mark>. La puissance instantanée reçue par une bobine idéale est : $\mathcal{P}(t) = \dfrac{d}{dt}\left(\frac{Li^{2}(t)}{2}\right)$. La bobine accumule donc de l'énergie $\mathcal{E}(t) = \frac{1}{2}Li^{2}(t)$ lorsque le courant $i$ augmente, et peut la restituer si celui-ci diminue : la bobine est un élément de stockage d'énergie. <mark style="color: red">Le courant à travers une bobine idéale, ne peut pas subir de discontinuité</mark>.
> - Condensateur idéal : La représentation symbolique d'un condensateur parfait est donnée sur la [[#^figure7|figure 7]]. Le courant $i(t)$ qui traverse un condensateur idéal est, à tout instant, proportionnel à la dérivée de la tension $u(t)$ appliquée à ses bornes : $i(t) = \dfrac{dq(t)}{dt} = C\dfrac{du(t)}{dt}$ avec $C$ est la capacité du condensateur en farad (F). En régime statique, $u = U$ et $i = 0$, la caractéristique statique est donc confondue avec l'axe horizontal $(O, U)$. <mark style="color: red">En régime constant ou statique, un condensateur idéal se comporte comme un interrupteur ouvert</mark>. Une énergie $\mathcal{E}(t) = \frac{1}{2}Cu^{2}(t)$est emmagasinée dans le condensateur et sa valeur instantanée est déterminée par la valeur de la tension $u(t)$ à ses bornes. <mark style="color: red">La tension u(t) aux bornes d'un condensateur idéal, ainsi que sa charge q(t), ne peuvent pas subir de discontinuité</mark>.

Résistance d'un fil de section constante : $R = \frac{\rho L}{S} = \frac{L}{\gamma S}$ avec $\rho$ $(\text{en}\,\Omega . m)$ est résistivité du matériau et $\gamma = \frac{1}{\rho}$ $(\text{en}\,S . m^{-1})$ est sa conductivité.

> [!note] Modélisation des électromoteurs
> La modélisation des électromoteurs s'effectue en linéarisant (éventuellement par morceaux) leurs caractéristiques. La relation entre l'intensité $i$ du courant à travers l'électromoteur et la tension $u$ entre ses bornes ([[#^figure14|fig. 14]]) est de la forme : $\frac{u}{U_0} + \frac{i}{I_0} = 1$.
> Il est possible de reproduire une telle caractéristique affine par deux sortes d'associations de dipôles idéaux :
> - Modélisation de Thévenin : La caractéristique de l'électromoteur peut s'expliciter en : $u = U_0 - \frac{U_0}{I_0}i$. Cette caractéristique est identique à celle de l'association d'une source idéale de tension de f.e.m. $e = U_0$ en série avec un résistor de résistance $r = \frac{U_0}{I_0}$ ([[#^figure15|fig. 15]]).
> - Modélisation de Norton : La caractéristique de l'électromoteur peut aussi s'expliciter en : $i = I_0 - \frac{I_0}{U_0}u$. Cette caractéristique est identique à celle de l'association d'une source idéale de courant de c.e.m. : $\eta = I_0$ en parallèle avec un résistor de conductance $g = \frac{I_0}{U_0}$, ou de résistance $r = \frac{U_0}{I_0}$ ([[#^figure16|fig. 16]]).
> 
> La représentation d'un électromoteur réel par un modèle de Norton ou de Thévenin permet de prévoir son interaction avec le reste du circuit, mais <mark style="color: red">elle ne représente pas son fonctionnement interne</mark>.
> On remarque qu'en circuit ouvert ( i = 0 ) , un courant non nul circule à l'intérieur du modèle de Norton alors que tous les courants sont nuls dans le modèle de Thévenin ; ces deux représentations sont cependant équivalentes <mark style="color: red">vues de l'extérieur</mark>.
# Définitions
==**Point de fonctionnement**== :
Le point de fonctionnement est le point $M$ de coordonnées $(u, i)$ dans un plan où les tension et courant sont portés sur les axes de repérage ([[#^figure1|fig. 1]]).

==**Caractéristique statique**== :
<mark style="color: red">La caractéristique statique tension-courant du dipôle s'obtient en relevant l'ensemble de ses points (U, I) de fonctionnement statique.</mark>
La relation entre la tension $U$ et le courant $I$ peut dépendre de façon significative de certains ==**paramètres de fonctionnement**== du dipôle. Il en est ainsi de la température ambiante $T$ (pour un conducteur métallique, ou bien pour une thermistance ou une diode et plus généralement pour tous les composants à semi-conducteurs), de l'éclairement $E$ (photopile, photodiode, photorésistance), etc.
En faisant varier l'un des paramètres de fonctionnement, on obtient un ==**réseau de caractéristiques**== ([[#^figure2|fig. 2]]).

==**Dipôles symétriques, dipôles polarisés**== :
Pour un composant dipolaire symétrique, lorsque le point de fonctionnement $(U, I)$ est observé, le point $(-U, -I)$ existe aussi : la caractéristique est symétrique par rapport à l'origine. Le régime de fonctionnement du circuit n'est pas perturbé lorsqu'on permute les deux bornes de ce composant (une résistance, par exemple).
Une pile (bornes $\oplus$ et $\ominus$), une diode (qui ne laisse passer le courant que dans un sens), sont au contraire des composants non symétriques, ou polarisés.

==**Dipôles passifs, dipôles actifs**== :
Le dipôle est passif si sa caractéristique statique passe par l'origine. La thermistance, dont le réseau est tracé sur la [[#^figure2|figure 2]] en est un exemple.
Dans le cas contraire, ce composant est actif. Une batterie, pour laquelle la tension mesurée à courant nul est non nulle, est un composant actif.

==**Équation d'évolution**== :
<mark style="color: red">Les évolutions de u(t) et i(t) dans un dipôle sont reliées par une équation d'évolution, équation différentielle de la variable temps t. Cette équation fait intervenir les paramètres de fonctionnement (température, etc.). Elle rend compte du comportement physique du dipôle.</mark>
La résolution (analytique ou numérique) de cette équation permet de prédire le comportement du dipôle, et plus généralement celui d'un circuit électrique. La conception raisonnée de montages réalisant des fonctions précises est ainsi envisageable.
Pour certains dipôles, le comportement est délicat à étudier, dans la mesure où il fait intervenir les conditions d'expériences et les valeurs de $u(t)$ et $i(t)$, mais aussi la façon dont l'état $(u, i)$ a été atteint : le point de fonctionnement obtenu fait intervenir les états de fonctionnement antérieurs du circuit. Le composant a ainsi de la mémoire, et garde une trace de son histoire : on parle alors de comportement à hystérésis.

==**Intérêt de la notion d'éléments fondamentaux**== :
Les éléments que nous décrivons ici permettent de réaliser quelques opérations fondamentales : alimenter le circuit (sources), multiplier, intégrer ou dériver le signal électrique (courant, tension). Ce sont tous des dipôles linéaires.
En les associant, nous obtiendrons des circuits linéaires dont les équations d'évolution permettent :
- de réaliser des fonctions particulières ;
- de modéliser (et observer) la réponse d'un système (pas uniquement électronique) régi par la même équation d'évolution.

==**Éléments dipolaires actifs**== :
- Sources indépendantes : ==**Une source indépendante de tension**== est caractérisée par sa force électromotrice (f.e.m.) $e(t)$ telle que $u = e$, quel que soit le courant traversant la source. La caractéristique tension-courant d'une source de tension est donnée par [[#^figure8|figure 8]]. ==**Une source indépendante de courant**== est caractérisée par son courant électromoteur (c.e.m.) $\eta(t)$ tel que $i = \eta$, quelle que soit la tension aux bornes de la source. La caractéristique tension-courant d'une source de courant est donnée [[#^figure9|figure 9]].
- Sources commandées : Une source commandée ou liée est une source de tension (ou de courant) dont la (f.e.m.) (ou le c.e.m.) a une valeur déterminée par une grandeur électrique $u'(t)$ ou $i'(t)$, associée à un autre élément du réseau ([[#^figure10|fig. 10]]).

==**Amplificateur opérationnel idéal en régime linéaire**== :
Un A.O. idéal est un composant actif dont la représentation symbolique est donnée par la [[#^figure11|figure 11]].
Les intensités $i_+$ et $i_-$ arrivant sur les entrés + et – sont nulles. En régime linéaire, il est caractérisé par : $\epsilon = V_+ - V_- = 0$. La tension $v_s$ est fixée par le reste du circuit compte tenu des relations $i_+ = 0$, $i_- = 0$ et $\epsilon = 0$.

==**Différents types de résistances**== :
- Résistances non bobinées : Elles peuvent être soit agglomérées, soit à couche.
- Résistances bobinées.

==**Caractéristiques nominales d'une résistance**== :
- Valeur nominale : C'est la valeur $R_n$ pour laquelle le composant a été fabriqué.
- Tolérance : C'est la valeur maximale de l'écart relatif $\left|\frac{R - R_n}{R_n}\right|$ entre la valeur réelle $R$ de la résistance et sa valeur $R_n$.
- Puissance nominale : C'est la puissance que le composant peut dissiper en régime continu à la température nominale de service.

==**Caractéristiques tension-courant d'une résistance**== :
Lorsqu'une résistance est correctement utilisée, sa caractéristique statique est une droite passant par l'origine. Il en est de même pour les caractéristiques dynamiques si la fréquence d'utilisation n'est pas trop élevée. Dans ces conditions, ces composants ont une résistance dynamique égale à leur résistance statique.
Lorsque la fréquence s'élève, des effets inductifs et capacitifs se manifestent et peuvent modifier de façon sensible la valeur nominale des résistances. Pour des valeurs élevées de la fréquence, les caractéristiques dynamiques ne sont plus des droites.

==**Différents types de condensateurs**== :
- Condensateurs enroulés.
- Condensateurs multicouches.
- Condensateurs électrolytiques.

==**Caractéristiques nominales d'un condensateur**== :
- Valeur nominale : C'est la valeur $C_n$ de la capacité pour laquelle le condensateur a été fabriqué.
- Tolérance : C'est la valeur maximale de l'écart relatif $\left|\frac{C - C_n}{C_n}\right|$ entre la valeur réelle $C$ de la capacité et sa valeur nominale $C_n$.
- Tension maximale d'utilisation : C'est la tension maximale $V_m$ au-dessus de laquelle il y a risque de détérioration du diélectrique (phénomène de « claquage »).
- Résistance d'isolement ou résistance de fuite : C'est la résistance $R_i$ qu'oppose le diélectrique au passage du courant entre les deux armatures du condensateur.
- Tenue en fréquence : Les pertes d'énergie dans les isolants augmentent avec la fréquence et limitent l'emploi des condensateurs en H.F.

==**Modélisation large bande d'un condensateur**== :
La représentation d'un condensateur par un élément idéal n'est donc pas toujours suffisante, à très basse fréquence ou à très haute fréquence. On approche mieux le condensateur réel en associant des dipôles idéaux selon le schéma de la [[#^figure12|figure 12]].

==**Structures des bobines**== :
- Bobines linéaires.
- Bobines non linéaires.

==**Modélisation d'une bobine**== :
Il faut tenir compte de la résistance non nulle du bobinage ainsi que les effets capacitifs entre les spires du bobinage à haute fréquence. On obtient une approximation en ajoutant une résistance en série, une faible capacité et une grande résistance en parallèle ([[#^figure13|fig. 13]]).

==**Électromoteur**== :
Un électromoteur est un composant dipolaire non symétrique dont les bornes sont repérées par les symboles $\oplus$ (borne positive) et $\ominus$ (borne négative). La fonction d'un électromoteur est de réaliser des conversions d'énergie.

==**Caractéristique statique d'un électromoteur**== :
Les caractéristiques statiques des électromoteurs ne passent pas par l'origine. Cette particularité confère aux électromoteurs la propriété de posséder une tension $U_0$ en circuit ouvert non nulle et un courant $I_0$ de court-circuit non nul : un électromoteur est un dipôle actif.

==**Point de fonctionnement d'un circuit élémentaire**== :
Nous considérons le circuit élémentaire constitué d'un générateur et d'un récepteur ([[#^figure17|fig. 17]]). Nous supposons connues les caractéristiques de ces deux éléments. La tension $u$ et le courant $i$ sont communs aux deux dipôles, qui sont vus, l'un en convention générateur et l'autre en convention récepteur.
Si nous superposons les caractéristiques, nous constatons que les caractéristiques se coupent en un point ([[#^figure18|fig. 18]]). En ce point, $i$ et $u$ satisfont aux conditions imposées par les deux dipôles : c'est le ==**point de fonctionnement du circuit**==.
Nous disposons donc d'une méthode graphique pour déterminer $u$ et $i$.
# Diagrammes
En convention générateur, $u(t) = -Ri(t)$ . La puissance reçue $\mathcal{P} = -u(t)i(t) = +Ri^{2}(t)$ est toujours positive
![[electronique1/attachments-electronique1/figure26.png]]^figure5

Représentation d'une bobine idéale
![[electronique1/attachments-electronique1/figure27.png]]^figure6

Représentation symbolique d'un condensateur idéal
![[electronique1/attachments-electronique1/figure28.png]]^figure7

Source de tension commandée en tension
![[electronique1/attachments-electronique1/figure31.png]]^figure10

Amplificateur opérationnel idéal
![[electronique1/attachments-electronique1/figure32.png]]^figure11

Modélisation large bande d'un condensateur
![[electronique1/attachments-electronique1/figure33.png]]^figure12

Modélisation d'une bobine réelle en large bande
![[electronique1/attachments-electronique1/figure34.png]]^figure13

Modélisation d'un électromoteur linéaire par un électromoteur de Thévenin $u = e - ri$
![[electronique1/attachments-electronique1/figure36.png]]^figure15

Modélisation d'un électromoteur linéaire par un électromoteur de Norton $i = \eta - gu$
![[electronique1/attachments-electronique1/figure37.png]]^figure16

Circuit élémentaire
![[electronique1/attachments-electronique1/figure38.png]]^figure17
# Graphiques
Caractéristique statique d'un composant dipolaire
![[electronique1/attachments-electronique1/figure21.png]]^figure1

Réseau des caractéristiques statiques d'une thermistance : la résistance diminue rapidement avec la température
![[electronique1/attachments-electronique1/figure22.png]]^figure2

Conductances statique $G$ et dynamique $g$ au point de fonctionnement
![[electronique1/attachments-electronique1/figure23.png]]^figure3

Exemple de caractéristique dynamique d'un dipôle linéaires soumis à une excitation sinusoïdale, tracée sur un écran d'oscilloscope
![[electronique1/attachments-electronique1/figure24.png]]^figure4a

Caractéristique d'une diode (élément non linéaire) à fréquence élevée
![[electronique1/attachments-electronique1/figure25.png]]^figure4b

Caractéristique courant-tension d'une source de f.e.m. $e(t)$ en convention générateur
![[electronique1/attachments-electronique1/figure29.png]]^figure8

Caractéristique tension-courant et représentation symbolique d'une source de c.e.m. $\eta(t)$
![[electronique1/attachments-electronique1/figure30.png]]^figure9

Caractéristique tension-courant d'un électromoteur linéaire avec une convention générateur
![[electronique1/attachments-electronique1/figure35.png]]^figure14

Branchement d'un dipôle et d'un générateur
![[electronique1/attachments-electronique1/figure39.png]]^figure18
# Expériences
> [!warning]
> Voici un exemple de travaux pratiques qui aborde le sujet de ce chapitre : le [lien](https://fac.umc.edu.dz/st/TP1_Etude%20d'une%20diode%20%C3%A0%20jonction.pdf).
# Autres notes
