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
# Diagrammes

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
# Expériences

# Autres notes
