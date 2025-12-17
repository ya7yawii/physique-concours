---
titre: "[[11-Conversion électronique statique]]"
tags:
aliases:
crée: 17-12-2025, 11:06
---
# Formules

# Définitions
==**Convertisseur statique**== :
Un convertisseur statique est un convertisseur utilisant des interrupteurs électroniques : il n'y a aucune conversion électromécanique.

> [!note] Conversion de puissance en continu
> - Puissance mises en jeu : L’électronique dite de puissance correspond à des puissances mises en jeu, de la centaine de watts à plusieurs centaines de kilowatts.
> 	- L'alimentation d’un micro-ordinateur ou d’une chaîne haute fidélité correspond à une puissance de 100 W à 500 W environ, celle d’un petit moteur (perceuse électrique, moteur de machine à laver) à une puissance de 500 W à 2 kW.
> 	- A l'autre extrémité de l’échelle des puissances, une motrice de T.G.V. consomme une puissance pouvant aller jusqu’à 8 MW sous 25 kV. Les moteurs utilisés dans l'industrie, les émetteurs de télédiffusion et les sonorisations de concerts correspondent couramment à des puissances de 100 kW.
> - Principe de la conversion de puissance : Imaginons un générateur continu et une charge adaptés. **Comment fournir à la charge une puissance réglable de zéro à sa valeur maximale avec un bon rendement ?**
> Ce problème est celui de la conversion de puissance en continu.
> Prenons le cas d’une charge résistive. Le plus simple est d’utiliser un rhéostat ([[#^figure1|fig. 1]]). Ce montage utilisable pour de faibles puissances n’est pas envisageable pour des puissances élevées : son rendement est très faible dès que la tension réglable est nettement inférieure à la tension d’alimentation.
> Une autre technique est de « hacher » la puissance délivrée par le générateur à la charge à l’aide d’un interrupteur ouvert et fermé de manière cyclique. La puissance est alors convertie sans pertes, car un interrupteur fonctionne en « tout ou rien » : soit la tension à ses bornes est nulle (interrupteur fermé), soit l’intensité le traversant est nulle (interrupteur ouvert).
> Dans les deux cas, la puissance qu’il dissipe est nulle.
^par1

> [!note] Conversion de puissance en continu
> - Principe du "hacheur" : Utilisons la technique envisagée au [[#^par1|paragraphe précédent]].
> L'interrupteur de [[#^figure2|figure 2]], appelé **hacheur**, « découpe » la tension continue. Il fonctionne à fréquence fixe avec une durée de conduction variable. Le rapport cyclique $\alpha$ est défini comme le rapport de cette durée sur la période du cycle ([[#^figure3|fig. 3]]).
> Quand l’interrupteur est fermé $u = E$ et $i = \frac{E}{R}$, quand il est ouvert $i = 0$ et $u = 0$. Calculons la puissance $p$ dissipée dans la résistance : $p = \frac{E^{2}}{R}$ quand l’interrupteur est fermé et $p = 0$ quand il est ouvert. Sa valeur moyenne est donc $\langle p \rangle = \frac{\alpha E^{2}}{R}$.
> Ce dispositif fournit une puissance réglable à la charge par une modification du rapport cyclique $\alpha$ avec un rendement égal à 1.
> Remarque : Les valeurs moyennes des grandeurs électriques $u(t)$ et $i(t)$ sont : $\langle u \rangle = \alpha E$ et $\langle i \rangle = \frac{\alpha E}{R}$.
> Nous pourrions penser que ce montage est effectivement équivalent en valeur moyenne à une source de f.e.m. $\alpha E$ alimentant la résistance $R$. Ce n'est pas le cas.
> En effet, la puissance moyenne dissipée dans la résistance est : $\langle p \rangle = \frac{\alpha E^{2}}{R} \neq \langle u \rangle \langle i \rangle$.
> La valeur moyenne d'un produit n'est pas égale au produit des valeurs moyennes.
> - Régime établi de commutation : L’analyse du fonctionnement des montages des figures [[#^figure3|3]] et [[#^figure4|4]] montre que l'interrupteur commandé permet de faire évoluer le système successivement suivant deux régimes différents de durées respectives $\alpha T$ et $(1 - \alpha)T$. Ces deux régimes se succèdent périodiquement puisque le hachage fonctionne à fréquence fixe.
> ==**Nous pouvons généraliser ce résultat aux dispositifs que nous allons étudier :**==
> ==**Les dispositifs de conversion de puissance fonctionnent en régime établi de commutation.**==
> ==**La période $T$ des cycles de fonctionnement est fixée.**==
> ==**La commutation sépare chaque cycle en régimes dont les durées sont régies par le rapport cyclique $\alpha$.**==
> Ainsi les grandeurs physiques, fonction du temps, des intensités et des tensions notamment, sont périodiques de période $T$. Cette propriété est très importante dans l'étude des régimes de commutation.

> [!note] Conversion électronique de puissance : Conversion électronique statique
> Il est impossible d’utiliser des interrupteurs mécaniques dans des hacheurs principalement à cause de leur inertie (ils ne peuvent pas fonctionner à des fréquences supérieures à une dizaine de hertz) et de leur durée de vie (quelques centaines de milliers de cycles au mieux).
> La conversion de puissance par hacheur a vu le jour grâce à la mise au point d'interrupteurs électroniques de puissance fiables dans les années 1960.
> Ceux-ci doivent présenter des caractéristiques adaptées aux circuits dans lesquels ils sont utilisés (tensions extrêmes admissibles de plusieurs kilovolts quand ils sont ouverts, courants extrêmes admissibles de plusieurs centaines d’ampères quand ils sont fermés pour les composants de puissance).
> Dans ce chapitre, nous étudierons le **convertisseur statique continu-continu** ([[#^figure5|fig. 5]]).
> ==**Un convertisseur utilisant des interrupteurs électroniques est appelé convertisseur statique, car il n’y a aucune conversion électromécanique. il est dit continu-continu si la source délivre une tension continue, et si la tension aux bornes de la charge est unidirectionnelle.**==
> D’autres dispositifs permettent une conversion électronique statique :
> - continu-alternatif (**onduleurs**) ;
> - alternatif-continu (**redresseurs**) ;
> - alternatif-alternatif (**gradateurs**).


# Diagrammes
Rhéostat. L'intensité est identique dans le générateur et le récepteur. Le rendement est donc égal au rapport $\frac{V_2}{V_1}$
![[electronique2/attachments-electronique2/figure280.png]]^figure1

Alimentation intermittente d'une résistance
![[electronique2/attachments-electronique2/figure281.png]]^figure2

Alimentation par une source de courant
![[electronique2/attachments-electronique2/figure284.png]]
La source de courant ne peut jamais être en circuit ouvert. Elle doit donc être périodiquement court-circuitée.
Quand l'interrupteur est fermé : $i = 0$, $u = 0$ et $p = 0$.
Quand l'interrupteur est ouvert : $i = I$, $u = RI$ et $p = RI^{2}$.
Les valeurs moyennes sont donc : $\langle i \rangle = (1 - \alpha)I$, $\langle u \rangle = (1 - \alpha)RI$ et $\langle p \rangle = (1 - \alpha)RI^{2}$.
Pendant la phase de court-circuit, le générateur ne fournit aucune puissance (la tension à ses bornes est nulle). Le rendement est donc égal à 1. ^figure4

Symbole d'un convertisseur continu-continu
![[electronique2/attachments-electronique2/figure285.png]]^figure5
# Graphiques
Rapport cyclique $\alpha$
![[electronique2/attachments-electronique2/figure283.png]]^figure3
# Expériences

# Autres notes
