---
titre: "[[02-Modélisation linéaire des composants usuels]]"
tags:
aliases:
crée: 06-11-2025, 13:31
---
# Formules
> [!note] Résistance statique, résistance dynamique
> La résistance statique $R_0$ d’un composant passif au point de fonctionnement $M(U, I)$ est le rapport $R_0 = \frac{U}{I}$.
> Son inverse $G_0 = \frac{1}{R_0}$ est la conductance statique du dipôle ([[#^figure3|fig. 3]]).
> La résistance dynamique du dipôle, au point de fonctionnement $M$, est $r = \left(\dfrac{dU}{dI}\right)_{\!M}$. C’est l’inverse de la pente $g = \left(\dfrac{dI}{dU}\right)_{\!M}$ de la caractéristique statique $I = f (U)$ du dipôle ([[#^figure3|fig. 3]]).
> Pour de petites variations de la tension $u$ et du courant $i$ au voisinage du point M, nous pouvons assimiler localement la caractéristique à sa tangente et écrire : $\delta u = u - U$, $\delta i = i - I$, $\delta u \approx r . \delta i$.
> Au voisinage du point $M$, les variations de tension et courant sont proportionnelles : la caractéristique a été linéarisée.

> [!note] Étude en régime variable
> Supposons que le comportement du composant est inchangé lorsqu’on passe d’un régime statique à un régime variable, ou dynamique, c’est-à-dire que l’on a : $i(t) = f(u(t))$.
> La linéarisation précédente peut alors être utilisée pour relier de petites variations des tension $u(t)$ et courant $i(t)$ au voisinage du point de fonctionnement : $u(t)  \approx U + r(i(t) - I)$.
> Cette extension est souvent acceptable pour une résistance et quelques autres composants dans des domaines de fréquences restreints. Cette extension n’est cependant pas généralisable et devra être vérifiée expérimentalement pour préciser son domaine de validité.
> En régime variable, la trace du spot d’un oscilloscope, dont les déplacements horizontal et vertical sont proportionnels à la tension $u(t)$ et au courant $i(t)$ respectivement, donne la caractéristique dynamique du dipôle ([[#^figure4a|fig. 4a]] et [[#^figure4b|4b]]).
> Comme nous venons de le signaler, celle-ci peut s’identifier, s’écarter un peu, ou même différer complètement de la caractéristique statique, suivant le composant étudié et le régime de fonctionnement utilisé.
> La géométrie de la caractéristique dépend donc de l’excitation utilisée : forme du signal, amplitude, domaine de fréquence. Ces indications doivent alors accompagner la caractéristique dynamique pour pouvoir l’analyser.

> [!note] Dipôle linéaire
> Un dipôle linéaire est décrit par une équation différentielle d’évolution linéaire à coefficients constants de la forme : $a_0u(t) + a_1 \dfrac{du(t)}{dt} + a_2 \dfrac{d^{2}u(t)}{dt^{2}} + \ldots + b_0i(t) + b_1 \dfrac{di(t)}{dt} + b_2 \dfrac{d^{2}i(t)}{dt^{2}} + \ldots = F(t)$.
> La caractéristique statique d’un dipôle linéaire est une droite.
> Le dipôle est passif si le second membre de son équation d’évolution est nul : $F(t) = 0$ (c’est le cas pour une résistance). Le dipôle linéaire passif est symétrique.
> Le dipôle est actif si le second membre $F(t)$ est non nul : nous parlerons alors de source.
> Si la fonction $F(t)$ est intrinsèque au dipôle, nous parlerons de <mark style="color: red">source indépendante</mark> (par exemple, l’équation $u(t) = U_0 \cos\omega t$ caractérise un générateur idéal de tension sinusoïdale).
> Si ce second membre est contrôlé par des tensions ou courants dans d’autres branches du circuit, nous parlerons de <mark style="color: red">source liée</mark> (c’est, par exemple, le cas pour un amplificateur opérationnel utilisé dans un montage amplificateur de tension).

> [!note] Éléments dipolaires passifs
> - Résistor ou conducteur (ohmique) : Un résistor suit à tout instant la loi d’Ohm : $u(t) = Ri(t)$ en convention récepteur avec $R$ est la résistance du résistor s'exprime en ohm ($\Omega$), et $G = \frac{1}{R}$ est sa conductance en siemens (S). La caractéristique statique d’un résistor et ses caractéristiques dynamiques sont confondues en une droite passant par l’origine. La puissance instantanée reçue par un résistor est toujours positive : $\mathcal{P}(t) = Ri^{2}(t)$. Le résistor absorbe donc de l’énergie, mais n’en restitue jamais au circuit ([[#^figure5|fig. 5]]) : en recevant de l’énergie, l’élément tend à s’échauffer, et transfère de la puissance thermique au milieu environnant. Cet effet est recherché dans le fonctionnement d’un radiateur électrique.
> - Bobine idéale : La représentation symbolique figure sur la [[#^figure6|figure 6]]. Le fonctionnement de cet élément est basé sur le phénomène d’induction électromagnétique : les variations du courant dans la bobine créent une tension aux bornes de l’élément : $u(t) = L\dfrac{di(t)}{dt}$ où $L$ est l'inductance de la bobine en henry (H). En régime statique $i = I$ et $u = 0$, la caractéristique statique est donc confondue avec l’axe vertical $(O, I)$. <mark style="color: red">En régime constant ou statique (permanent, indépendant du temps) une bobine idéale se comporte comme un simple fil</mark>. La puissance instantanée reçue par une bobine idéale est : $\mathcal{P}(t) = \dfrac{d}{dt}\left(\frac{Li^{2}(t)}{2}\right)$. La bobine accumule donc de l’énergie $\mathcal{E}(t) = \frac{1}{2}Li^{2}(t)$ lorsque le courant $i$ augmente, et peut la restituer si celui-ci diminue : la bobine est un élément de stockage d’énergie. <mark style="color: red">Le courant à travers une bobine idéale, ne peut pas subir de discontinuité</mark>.
> - Condensateur idéal : La représentation symbolique d’un condensateur parfait est donnée sur la [[#^figure7|figure 7]]. Le courant $i(t)$ qui traverse un condensateur idéal est, à tout instant, proportionnel à la dérivée de la tension $u(t)$ appliquée à ses bornes : $i(t) = \dfrac{dq(t)}{dt} = C\dfrac{du(t)}{dt}$ avec $C$ est la capacité du condensateur en farad (F). En régime statique, $u = U$ et $i = 0$, la caractéristique statique est donc confondue avec l’axe horizontal $(O, U)$. <mark style="color: red">En régime constant ou statique, un condensateur idéal se comporte comme un interrupteur ouvert</mark>. Une énergie $\mathcal{E}(t) = \frac{1}{2}Cu^{2}(t)$est emmagasinée dans le condensateur et sa valeur instantanée est déterminée par la valeur de la tension $u(t)$ à ses bornes. <mark style="color: red">La tension u(t) aux bornes d’un condensateur idéal, ainsi que sa charge q(t), ne peuvent pas subir de discontinuité</mark>.


# Définitions
==**Point de fonctionnement**== :
Le point de fonctionnement est le point $M$ de coordonnées $(u, i)$ dans un plan où les tension et courant sont portés sur les axes de repérage ([[#^figure1|fig. 1]]).

==**Caractéristique statique**== :
<mark style="color: red">La caractéristique statique tension-courant du dipôle s’obtient en relevant l’ensemble de ses points (U, I) de fonctionnement statique.</mark>
La relation entre la tension $U$ et le courant $I$ peut dépendre de façon significative de certains ==**paramètres de fonctionnement**== du dipôle. Il en est ainsi de la température ambiante $T$ (pour un conducteur métallique, ou bien pour une thermistance ou une diode et plus généralement pour tous les composants à semi-conducteurs), de l’éclairement $E$ (photopile, photodiode, photorésistance), etc.
En faisant varier l’un des paramètres de fonctionnement, on obtient un ==**réseau de caractéristiques**== ([[#^figure2|fig. 2]]).

==**Dipôles symétriques, dipôles polarisés**== :
Pour un composant dipolaire symétrique, lorsque le point de fonctionnement $(U, I)$ est observé, le point $(-U, -I)$ existe aussi : la caractéristique est symétrique par rapport à l’origine. Le régime de fonctionnement du circuit n’est pas perturbé lorsqu’on permute les deux bornes de ce composant (une résistance, par exemple).
Une pile (bornes $\oplus$ et $\ominus$), une diode (qui ne laisse passer le courant que dans un sens), sont au contraire des composants non symétriques, ou polarisés.

==**Dipôles passifs, dipôles actifs**== :
Le dipôle est passif si sa caractéristique statique passe par l’origine. La thermistance, dont le réseau est tracé sur la [[#^figure2|figure 2]] en est un exemple.
Dans le cas contraire, ce composant est actif. Une batterie, pour laquelle la tension mesurée à courant nul est non nulle, est un composant actif.

==**Équation d’évolution**== :
<mark style="color: red">Les évolutions de u(t) et i(t) dans un dipôle sont reliées par une équation d’évolution, équation différentielle de la variable temps t. Cette équation fait intervenir les paramètres de fonctionnement (température, etc.). Elle rend compte du comportement physique du dipôle.</mark>
La résolution (analytique ou numérique) de cette équation permet de prédire le comportement du dipôle, et plus généralement celui d’un circuit électrique. La conception raisonnée de montages réalisant des fonctions précises est ainsi envisageable.
Pour certains dipôles, le comportement est délicat à étudier, dans la mesure où il fait intervenir les conditions d’expériences et les valeurs de $u(t)$ et $i(t)$, mais aussi la façon dont l’état $(u, i)$ a été atteint : le point de fonctionnement obtenu fait intervenir les états de fonctionnement antérieurs du circuit. Le composant a ainsi de la mémoire, et garde une trace de son histoire : on parle alors de comportement à hystérésis.

==**Intérêt de la notion d’éléments fondamentaux**== :
Les éléments que nous décrivons ici permettent de réaliser quelques opérations fondamentales : alimenter le circuit (sources), multiplier, intégrer ou dériver le signal électrique (courant, tension). Ce sont tous des dipôles linéaires.
En les associant, nous obtiendrons des circuits linéaires dont les équations d’évolution permettent :
- de réaliser des fonctions particulières ;
- de modéliser (et observer) la réponse d’un système (pas uniquement électronique) régi par la même équation d’évolution.

==**Éléments dipolaires actifs**== :
- Sources indépendantes : ==**Une source indépendante de tension**== est caractérisée par sa force électromotrice (f.e.m.) $e(t)$ telle que $u = e$, quel que soit le courant traversant la source. La caractéristique tension-courant d’une source de tension est donnée par [[#^figure8|figure 8]]. ==**Une source indépendante de courant**== est caractérisée par son courant électromoteur (c.e.m.) $\eta(t)$ tel que $i = \eta$, quelle que soit la tension aux bornes de la source. La caractéristique tension-courant d’une source de courant est donnée [[#^figure9|figure 9]].
- Sources commandées : Une source commandée ou liée est une source de tension (ou de courant) dont la (f.e.m.) (ou le c.e.m.) a une valeur déterminée par une grandeur électrique $u'(t)$ ou $i'(t)$, associée à un autre élément du réseau ([[#^figure10|fig. 10]]).

==**Amplificateur opérationnel idéal en régime linéaire**== :
Un A.O. idéal est un composant actif dont la représentation symbolique est donnée par la [[#^figure11|figure 11]].
Les intensités $i_+$ et $i_-$ arrivant sur les entrés + et – sont nulles. En régime linéaire, il est caractérisé par : $\epsilon = V_+ - V_- = 0$. La tension $v_s$ est fixée par le reste du circuit compte tenu des relations $i_+ = 0$, $i_- = 0$ et $\epsilon = 0$.
# Diagrammes
En convention générateur, $u(t) = -Ri(t)$ . La puissance reçue $\mathcal{P} = -u(t)i(t) = +Ri^{2}(t)$ est toujours positive
![[electronique1/attachments-electronique1/figure26.png]]^figure5

Représentation d’une bobine idéale
![[electronique1/attachments-electronique1/figure27.png]]^figure6

Représentation symbolique d’un condensateur idéal
![[electronique1/attachments-electronique1/figure28.png]]^figure7

Source de tension commandée en tension
![[electronique1/attachments-electronique1/figure31.png]]^figure10

Amplificateur opérationnel idéal
![[electronique1/attachments-electronique1/figure32.png]]^figure11
# Graphiques
Caractéristique statique d’un composant dipolaire
![[electronique1/attachments-electronique1/figure21.png]]^figure1

Réseau des caractéristiques statiques d’une thermistance : la résistance diminue rapidement avec la température
![[electronique1/attachments-electronique1/figure22.png]]^figure2

Conductances statique $G$ et dynamique $g$ au point de fonctionnement
![[electronique1/attachments-electronique1/figure23.png]]^figure3

Exemple de caractéristique dynamique d’un dipôle linéaires soumis à une excitation sinusoïdale, tracée sur un écran d’oscilloscope
![[electronique1/attachments-electronique1/figure24.png]]^figure4a

Caractéristique d’une diode (élément non linéaire) à fréquence élevée
![[electronique1/attachments-electronique1/figure25.png]]^figure4b

Caractéristique courant-tension d’une source de f.e.m. $e(t)$ en convention générateur
![[electronique1/attachments-electronique1/figure29.png]]^figure8

Caractéristique tension-courant et représentation symbolique d’une source de c.e.m. $\eta(t)$
![[electronique1/attachments-electronique1/figure30.png]]^figure9
# Expériences

# Autres notes
