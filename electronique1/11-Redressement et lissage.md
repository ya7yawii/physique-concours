---
titre: "[[11-Redressement et lissage]]"
tags:
  - diode
  - redresseur-simple-alternance
  - redresseur-double-alternance
  - détecteur-d-enveloppe
  - redressement
  - lissage
crée: 19-11-2025, 10:46
---
# Formules

# Définitions
==**Diode**== :
Une diode est un composant non linéaire qui ne laisse passer le courant que dans un sens comparable à une valve dans un circuit hydraulique.
Cette propriété est utilisée dans les redresseurs dont la fonction est de fournir une tension toujours positive à partir d'une tension alternative.
La tension redressée peut ensuite être « lissée » : alimentation en continu d'un appareil électrique à partir de la tension alternative du secteur, détection de la modulation d'amplitude d'une onde radio (AM).

==**Diodes à jonction**== :
Une diode à jonction est un monocristal de semiconducteur (Si, Ge) dans lequel la conductibilité passe du type P (les porteurs sont les trous) au type N (les porteurs sont des électrons libres) ([[#^figure1|fig. 1]]). Le type de conductibilité s'obtient par dopage, c'est-à-dire par addition d'impuretés de type convenable. L'interface des deux régions P et N constitue la jonction P-N, dont les propriétés remarquables sont exploitées dans de nombreux composants à semiconducteurs, dont les diodes à jonction et les transistors.

> [!note] Diodes de redressement : Caractéristiques
> - Modélisation du composant : La caractéristique statique théorique d'une diode à jonction est $\displaystyle I = I_s\left(e^{\frac{V}{\alpha U_T}} - 1\right)$ avec $I_s$ courant de saturation, $U_T$ tension thermodynamique fonction de la température et $\alpha$ constante sans dimension. Pour une diode au silicium : $I_s \approx 1 pF$, $U_T \approx 25 mV$ à $T = 27 \,\degree\! C$ et $1 \leqslant \alpha \leqslant 2$ selon le type de diode.
> La caractéristique statique réelle d'une diode diffère notablement de sa caractéristique théorique, car dès que $|V| > 20U_T$ environ, elle tend à devenir rectiligne ([[#^figure2|fig. 2]]). Cette particularité explique la modélisation connue de la caractéristique d'une diode ([[#^figure3|fig. 3]]) avec $V_D$ tension de seuil ($V_D \approx 0,6 V$ pour une diode au silicium et $V_D = 0,3 V$ pour une diode au germanium), $r_d = \left(\dfrac{dV}{dI}\right)_{V > 0}$ résistance dynamique en direct, de l'ordre de $10\Omega$, $R_i = \left(\dfrac{dV}{dI}\right)_{V < 0}$ résistance dynamique en inverse, de l'ordre de $100M\Omega$.
> - Limites d'utilisation : Le courant direct $I$ d'une diode doit être inférieur au courant direct maximal admissible $I_{d_M}$ courant au-delà duquel la puissance dissipée par effet Joule provoque la destruction thermique de la jonction P-N. Cette limite absolue d'utilisation varie de quelques 10 mA à quelques 10 A suivant le modèle de diode utilisé.
> La tension inverse maximale admissible $V_{i_M}$ est la tension inverse maximale que peut supporter la diode sans claquer, c'est-à-dire sans être détruite : elle varie, suivant le type de diodes, de 80 V à 500 V environ.

> [!note] Modèle de la diode idéale
> Une diode idéale est un élément dont la caractéristique a pour équation ([[#^figure4|fig. 4]]) : $I = 0$ si $V \leqslant 0$ et $V = 0$ si $I \geqslant 0$.
> Comparativement à une diode idéale, une diode réelle possède trois défauts :
> - existence d'une tension de seuil $V_D$ ;
> - résistance dynamique directe $r_d$ non nulle ;
> - résistance dynamique inverse $R_i$ non infinie.
> 
> Dans la suite de ce chapitre, nous ne tiendrons compte que du défaut principal des diodes, à savoir l'existence de la tension de seuil $V_D$. Ainsi, sauf spécification contraire, les diodes considérées sont des dipôles dont la caractéristique est représentée dans la [[#^figure5|figure 5]].

> [!note] Redressement simple alternance
> Un redresseur simple alternance est un quadripôle pour lequel : 
> $$
> v_s =
> \begin{cases}
> v_e & \,\text{si}\, v_e > 0\\
> 0 & \,\text{si}\, v_e < 0.
> \end{cases}
> $$
> Sa caractéristique $v_s = f(v_e)$ est représentée dans la [[#^figure6|figure 6]].

> [!note] Redresseur élémentaire simple alternance
> Réalisons le circuit de [[#^figure7|figure 7]], dans lequel $D$ est une diode de redressement, $R_u$ une résistance symbolisant un circuit d'utilisation et $v_e(t) = v_{e_m}\sin(\omega t)$ le signal sinusoïdal délivré par le G.B.F.
> Lorsque la diode conduit $(i(t) > 0)$, nous avons : $v_s(t) = v_e(t) - V_D = R_ui(t) > 0$.
> Quand l'inégalité précédente n'est pas satisfaite $(v_e(t) - V_D < 0)$, la diode est bloquée : $i(t) = 0$ et $v_s(t) = 0$. Comparativement au redresseur idéal, un tel redresseur possède le défaut d'avoir une tension de seuil $V_D$.
> 
> Réalisons le montage de [[#^figure7|figure 7]] avec les valeurs indiquées et observons les tensions $v_e(t)$ et $v_s(t)$ à l'oscilloscope en mode DC bicourbe ([[#^figure9|fig. 9]]). L'effet de seuil (existence d'une tension de seuil) est perceptible puisque $v_s(t)$ ne s'annule pas avec $v_e(t)$. Quand la diode conduit, elle forme avec la charge $R_u$ un diviseur de tension : cet effet est très marqué si $R_u$ est faible.
> Plaçons ensuite l'oscilloscope en mode $XY$ et observons la caractéristique du redresseur ([[#^figure8|fig. 8]]). Utilisons, pour ce tracé, la fréquence la plus basse possible afin d'avoir la caractéristique statique ou très basse fréquence du redresseur.
> La détermination de la tension de seuil du redresseur réalisé donne : $V_D = 0,5 V$.
> Appliquons des signaux en créneaux, puis triangulaires, et observons le signal de sortie $v_s(t)$ ([[#^figure10|fig. 10]]).
> Là encore, l'effet de seuil est perceptible ainsi que l'effet du diviseur de tension constitué par la diode et la charge $R_u$ (quand elle est de faible valeur).

> [!note] Redresseur simple alternance sans seuil
> Pour éliminer le défaut du redresseur précédent, à savoir l'existence d'un seuil $V_D$, réalisons le circuit de [[#^figure11|figure 11]] avec un amplificateur opérationnel supposé idéal.
> - Premier cas : La diode conduit. L'amplificateur opérationnel est en régime linéaire, car la boucle de rétroaction est fermée sur l'entrée inverseuse. Nous avons alors $\epsilon = 0$ et $v_s = v_e$. La diode étant passante, $i > 0$, il en résulte que $v_s = v_e = R_ui > 0$.
> En définitive, $v_s = v_e$ quand $v_e > 0$.
> En ne tenant compte que du principal défaut de la diode, à savoir sa tension de seuil $V_D$, nous avons à la sortie de l'amplificateur opérationnel : $v_{s_0} \approx v_s + V_D$.
> - Second cas : La diode est bloquée et l'amplificateur opérationnel est en boucle ouverte, c'est-à-dire en régime de saturation. Comme $i_- = 0$, la tension de sortie du redresseur est $v_s = 0$ et celle de l'amplificateur opérationnel $v_{s_0} < v_s = 0$, puisque la diode est bloquée. L'amplificateur opérationnel étant en régime de saturation, nous avons $v_{s_0} = -V_{sat}$, donc : $\epsilon < 0$ et $v_e < 0$.
> En conclusion $v_s = 0$ quand $v_e < 0$.
> 
> Remarque : Il est possible de raisonner ainsi :
> - si $v_e > 0$, la sortie $v_{s_0}$ a tendance à devenir rapidement positive, donc la diode est passante, la rétroaction existe sur l'entrée inverseuse. Nous sommes en présence d'un suiveur et $v_s = v_e$ ;
> - si $v_e < 0$, la sortie $v_{s_0}$ a tendance à devenir rapidement négative, donc la diode est bloquée, il n'y a aucun courant dans $R_u$, et $v_s = 0$.
> 
> Pour ce redresseur simple alternance sans seuil nous pouvons écrire : $v_s(t) = \frac{1}{2}(v_e(t) + |v_e(t)|)$.
> 
> Réalisons le montage de [[#^figure11|figure 11]], avec les valeurs indiquées et observons les tensions $v_e(t)$ et $v_s(t)$ à l'oscilloscope en mode DC bicourbe ([[#^figure12|fig. 12]]). Nous vérifions que le redressement se fait sans seuil.
> Observons ensuite les tensions $v_e(t)$ et $v_{s_0}(t)$ ([[#^figure13|fig. 13]]). Nous vérifions que l'A.O. est saturé négativement lorsque la diode est bloquée.
> Plaçons ensuite l'oscilloscope en mode $XY$ et observons la caractéristique $v_s = f(v_e)$ du redresseur réalisé. Utilisons, pour ce tracé, la fréquence la plus basse possible afin d'avoir la caractéristique statique ou très basse fréquence du redresseur ([[#^figure14|fig. 14]]).
> Par rapport à la caractéristique de [[#^figure9|figure 9]], nous vérifions l'absence de seuil.
> Pour des fréquences plus élevées $(f > 1 kHz)$ le tracé présente un phénomène d'hystérésis. Cela est dû à l'effet capacitif de la diode et surtout à la vitesse finie de balayage de l'A.O.
^par1

> [!note] Redressement double alternance
> ==**Un redresseur double alternance est un quadripôle pour lequel les tensions d'entrée $v_e(t)$ et de sortie $v_s(t)$ sont liées par la relation $v_s(t) = |v_e(t)|$.**==
> Sa caractéristique $v_s = f(v_e)$ est donnée dans la [[#^figure15|figure 15]]. D'un point de vue fonctionnel, un redresseur double alternance réalise la fonction valeur absolue.
> ==**Le redresseur double alternance d'une tension alternative double sa fréquence et double la valeur de sa composante continue par rapport à la même tension redressée simple alternance.**==

> [!note] Redresseur double alternance à pont de diodes
> Examinons le circuit de [[#^figure16|figure 16]], réalisé avec quatre diodes identiques (pont de Graetz), une résistance de charge $R_u$ modélisant un réseau d'utilisation et un générateur basse fréquence. Lorsque la tension $v_e(t) > 2V_D$, les diodes $D_1$ et $D_3$ conduisent et la tension de sortie est $v_s(t) = v_e(t) - 2V_D$. En revanche, lorsque la tension $v_e(t)$ est négative $v_e(t) < -2V_D$, ce sont les diodes $D_2$ et $D_4$ qui conduisent, et la tension de sortie $v_s(t) = -(v_e(t) - 2V_D)$. L'effet de seuil est important, puisqu'il est de l'ordre de $2V_D$.
> 
> Réalisons le circuit de [[#^figure16|figure 16]] avec les valeurs indiquées et observons à l'oscilloscope, en mode DC bicourbe, les tensions $v_e(t)$ et $v_{s_+}(t)$, puis les tensions $v_e(t)$ et $v_{s_-}(t)$ ([[#^figure17|fig. 17]]). Les tensions $v_{s_-}(t)$ et $v_{s_+}(t)$ sont des tensions redressées simple alternance délivrées par un redresseur possédant un seuil.
> L'observation simultanée des tensions $v_e(t)$ et $v_s(t)$ pose des problèmes de masse qu'il est possible de résoudre à l'aide d'un transformateur d'isolement ([[#^figure18|fig. 18]]).
> L'utilisation d'un transformateur d'isolement introduit souvent des distorsions dans les signaux du circuit secondaire. Il convient de travailler, avec un tel transformateur, à basse fréquence. La [[#^figure19|figure 19]] donne les variations de $v_e(t)$ et de $v_s(t)$ à $f = 200 Hz$.
> La [[#^figure20|figure 20]] fournit la caractéristique du redresseur et met en évidence la tension de seuil.
> Nous pouvons aussi nous affranchir du problème de masse en utilisant une sonde différentielle (cf. [[04-Principe des appareils de mesure|chapitre 4]]). Ce système ne présente pas les inconvénients du transformateur d'isolement.

> [!note] Redresseur double alternance sans seuil
> Un redresseur double alternance sans seuil se réalise à partir d'un redresseur simple alternance sans seuil. Il existe une grande variété de montages. Examinons le principe de l'un des plus simples.
> Soit $v_e(t)$ le signal à redresser et $v_s(t) = |v_e(t)|$ le signal redressé double alternance. Notons $v_r(t)$ le signal redressé simple alternance positif (cf. [[#^par1|paragraphe 1]]) ; nous avons : $v_r(t) = \frac{1}{2}(v_e(t) + |v_e(t)|)$, d'où $|v_e(t)| = 2v_r(t) - v_e(t)$.
> ==**Un redresseur double alternance sans seuil peut être réalisé à partir d'un redresseur simple alternance positif sans seuil et d'un soustracteur.**==
> Le redresseur utilisé est celui de [[#^figure11|figure 11]]. Vérifions que le soustracteur de [[#^figure21|figure 21]], réalise la fonction demandée.
> L'amplificateur opérationnel est en régime linéaire car la boucle de rétroaction aboutit à son entrée inverseuse, donc $v_- = v_+ = \frac{v_r}{2}$. La loi des nœuds appliquée à l'entrée inverseuse s'écrit : $\frac{v_e - v_-}{2R} - \frac{v_-}{R} + \frac{v_s - v_-}{2R} = 0$, d'où, en remplaçant $v_-$ par son expression en fonction de $v_r$ : $v_s(t) = 2v_r(t) - v_e(t)$.
> L'association de ces deux éléments donne le circuit de [[#^figure22|figure 22]].
> 
> Réalisons le circuit de [[#^figure22|figure 22]] avec les valeurs indiquées pour les composants et les signaux, et observons les tensions $v_e(t)$ et $v_s(t)$ à l'oscilloscope, en mode DC bicourbe ([[#^figure23|fig. 23]]). La tension $v_s(t)$ est bien la tension $v_e(t)$ redressée double alternance.
> Commutons en mode $XY$ et utilisons la fréquence la plus basse possible pour tracer la caractéristique statique ou basse fréquence $v_s = f(v_e)$ du redresseur réalisé ([[#^figure24|fig. 24]]). La tension de seuil a disparu.
> Utilisons des signaux en créneaux, puis triangulaires, de fréquence 200 Hz et observons le signal de sortie $v_s(t)$. À cette fréquence, le redressement n'est affecté d'aucun défaut notable.

> [!note] Redressement avec lissage
> Pour alimenter certains appareils, il est nécessaire de produire une tension continue à partir de la tension alternative sinusoïdale délivrée par le secteur. Les redresseurs étudiés fournissent bien une tension de signe constant, donc de valeur moyenne non nulle, mais non constante.
> Un lissage par condensateur permet d'obtenir une tension quasi constante, avec un faible taux d'ondulation.
> 
> Considérons le redresseur double alternance à pont de diodes de [[#^figure25|figure 25]] où un condensateur $C$ de forte capacité est placé en parallèle sur l'utilisation modélisée par la résistance $R_u$.
> La résistance $R$, de faible valeur, permettra d'examiner à l'oscilloscope le courant $i(t)$ débité par le pont redresseur.
> En régime établi, le condensateur $C$ stocke une partie de la charge débitée par le redresseur pendant sa période de conduction et la restitue ensuite dans l'utilisation $R_u$ pendant la période de blocage du redresseur. Le temps de circulation du courant à travers l'utilisation est alors prolongé et l'ondulation de la tension de sortie $v_s(t)$ est diminuée ([[#^figure26|fig. 26]]).
> Interprétons les courbes de [[#^figure26|figure 26]].
> - Pendant la période de conduction (c'est-à-dire de B à A sur le [[#^figure26|figure 26]]), le circuit ($R$, $R_u$, $C$) est excité par la tension de sortie $v(t)$ du redresseur dont l'amplitude est $v_{e_m} - 2V_D$. La loi des nœuds appliquée en $S$ donne : $i = C\dfrac{dv_s}{dt} + \frac{v_s}{R_u} = \frac{v - v_s}{R}$, soit : $\dfrac{dv_s}{dt} + \frac{v_s}{\tau} = \frac{v}{RC}$. La constante de temps $\tau = \frac{RR_u}{R + R_u}C \approx RC \approx 0,5 ms$ est faible devant la période $T \approx 5 ms$ du signal ; la quantité $\left|\dfrac{dv_s}{dt}\right| \approx \frac{|v_s|}{T}$ est donc négligeable devant $\frac{|v_s|}{\tau}$, ce qui permet d'estimer la tension aux bornes de la résistance $R_u$ pendant cette phase de conduction : $v_s(t) \approx \frac{\tau}{RC}v(t) \approx v(t)$.
> - Pendant la période de blocage du redresseur $(i = 0)$, le condensateur $C$ se décharge dans l'utilisation $R_u$ selon la loi : $C\dfrac{dv_s}{dt} + \frac{v_s}{R_u} = 0$ obtenue par application de la loi des nœuds en $S$. Ainsi, la loi de décharge du condensateur est une loi exponentielle du temps, de constante de temps $\tau' = R_uC$, grande devant la période $T$ du signal. La pente de l'exponentielle au début de cette période est $\dfrac{dv_s}{dt} = -\frac{v_s}{\tau'}$, en continuité avec celle de la sinusoïde décrivant le régime précédent, comme il est possible de le vérifier sur la [[#^figure26|figure 26]].
> Pour un même signal d'entrée, la période $T$ est deux fois plus faible avec un redresseur double alternance qu'avec un redresseur simple alternance.
> La condition $\tau' = R_uC \gg T$ est donc plus facile à obtenir avec un redresseur double alternance.
> 
> Réalisons le circuit de [[#^figure25|figure 25]] avec $C = 10 \mu F$ et $R = 47 \Omega$.
> Observons à l'oscilloscope, en mode DC bicourbe, la tension redressée filtrée $v_s(t)$ et le courant $i(t)$ délivré par le redresseur ([[#^figure26|figure 26]]). L'amplitude de l'ondulation $v_{ond}(t)$ est $\Delta v_s \approx 0,5 V$.
> Donnons à la capacité la valeur $C = 1 mF$. L'ondulation disparaît pratiquement ([[#^figure27|fig. 27]]) et l'amplitude de la tension redressée s'établit à $v_{s_0} \approx 2,95 V$.

> [!note] Détecteur d'enveloppe : Principe
> Nous étudions un signal (une tension) $u(t)$ de la forme : $u(t) = U(t)cos(\omega t + \varphi)$. $U(t)$, appelée enveloppe est une fonction lentement variable, de durée caractéristique $t_0$ très grande devant $T = \frac{2\pi}{\omega}$.
> Nous pouvons considérer que sur une durée grande devant $T$ mais petite devant $t_0$, $u(t)$ est pratiquement une fonction sinusoïdale d'amplitude $U(t)$ ; $u(t)$ est un signal pseudo-périodique modulé en amplitude.
> Nous pouvons réaliser un tel signal avec un multiplieur, système électronique qui délivre en sortie un signal proportionnel au produit de deux tensions d'entrée. Pour extraire l'enveloppe $U(t)$ de $u(t)$, nous utilisons le montage détecteur d'enveloppe dont le principe est représenté sur la [[#^figure28|figure 28]] où nous supposons la diode idéale.
> Lorsque la diode conduit, $u_s(t) = u(t)$. Cette situation se présente si $i > 0$, ce qui est toujours vérifié si $u(t)$ est positif et croissant.
> Lorsque la diode est bloquée, la capacité $C$ se décharge dans la résistance $R$ avec une constante de temps $\tau = RC$ :
> - si $\tau = RC \ll T$, $u_s(t)$ peut suivre toutes les variations de $u(t)$ ;
> - si $\tau = RC \gg T$, la capacité ne se décharge pratiquement pas pendant une pseudo-période et $u_s(t)$ reste très voisin de $U(t)$ ;
> - si $\tau = RC \gg t_0$, $u_s(t)$ reste quasi constant lorsque $U(t)$ décroît. $u_s(t)$ ne peut pas suivre les variations de $U(t)$.
> On en déduit que $u_s(t)$ est voisin de l'enveloppe $U(t)$ si $T \ll RC \ll t_0$ ([[#^figure29|fig. 29]]).
> 
> Le signal émis par une radio AM (modulation d'amplitude) est de cette forme.
> Une porteuse sinusoïdale de quelques centaines de kilohertz est modulée par le signal audio de fréquences comprises entre 20 Hz et 20 kHz (norme Hi-fi).
> Le récepteur détecte l'enveloppe du signal modulé, c'est-à-dire le signal audio qui est ensuite amplifié.

> [!note] Détecteur d'enveloppe : Réalisation expérimentale
> L'existence de la tension de seuil nous fait remplacer la diode par le montage redresseur monoalternance sans seuil ([[#^figure30|fig. 30]]).
> Le multiplieur fabrique un signal modulé $u(t)$, produit d'une fonction sinusoïdale de haute fréquence $u_p(t)$ appelée porteuse et d'un signal modulant $u_m(t)$ de basse fréquence dont les expressions peuvent s'écrire : $u_p(t) = u_{p_m}\cos(\omega_p t + \Phi_p)$ et $u_m(t) = U_0[1 + \alpha\cos(\omega_m t + \phi_m)]$ avec $\alpha < 1$.
> Le G.B.F. 1 délivre un signal $u_m(t)$ de fréquence voisine de 100 Hz. Il est possible d'obtenir une valeur de $\alpha$ comprise entre 0 et 1 en ajoutant une tension continue à la tension sinusoïdale, fonction généralement appelée offset sur les G.B.F.
> Le G.B.F. 2 délivre la porteuse $u_p(t)$ de fréquence $10 kHz$.
> Un choix de $R$ et $C$ tels que $RC \approx 1 ms$ est a priori satisfaisant pour obtenir une tension de sortie proche de l'enveloppe. Nous prendrons $C = 1 \mu F$ et $R$ voisin de $1 k\Omega$.
> 
> - Visualiser la porteuse sur l'oscilloscope et choisir $\alpha \approx 0,5$.
> - En mode bicourbe, visualiser simultanément le signal modulé $u(t)$ et le signal de sortie.
> 
> En faisant varier $R$ nous notons la valeur qui optimise la fonction de détection d'enveloppe. D'après les photographies de [[#^figure31|figure 31]], la valeur $R = 3 k\Omega$ semble être un bon compromis. On vérifie que si $R$ est trop faible, le signal de sortie conserve une partie des oscillations de la porteuse, et que si $R$ est trop grande, $u_s(t)$ s'écarte de l'enveloppe.
# Diagrammes
a. Structure théorique d'une jonction P-N. b. Structure d'une diode à jonction
![[figure267.png]]^figure1

Redresseur élémentaire simple alternance G.B.F. (2V~, 200 Hz) et $R_u = 10 k\Omega$
![[figure273.png]]^figure7

Redresseur simple alternance sans seuil G.B.F. (2V~, 200 Hz) et $R_u = 10 k\Omega$ et $V_{CC} = 15 V$
![[figure277.png]]^figure11

Redresseur double alternance à diodes (pont de Graetz). G.B.F. (2V~, 200 Hz) et $R_u = 10 k\Omega$
![[figure282.png]]^figure16

Le transformateur d'isolement sépare la masse circuit du G.B.F. de celle du redresseur. G.B.F. (2V~, 200 Hz) et $R_u = 10 k\Omega$
![[figure284.png]]^figure18

Soustracteur associé au redresseur monoalternance
![[figure287.png]]^figure21

Redresseur double alternance sans seuil. G.B.F. (2V~, 200 Hz), $R = 10 k\Omega$ et $R_u = 10 k\Omega$
![[figure288.png]]^figure22

Redressement double alternance et lissage de la tension vs par le condensateur C. G.B.F. (5V~, 200 Hz), $R = 47 \Omega$, $C = 10 \mu F$ et $R_u = 1 k\Omega$
![[figure291.png]]^figure25

Détecteur d'enveloppe
![[figure294.png]]^figure28

Détection de l'enveloppe de $u(t)$
![[figure296.png]]^figure30
# Graphiques
Caractéristique statique d'une diode à jonction à différentes températures
![[figure268.png]]^figure2

Modélisation de la caractéristique statique d'une diode avec limitations absolues en courant $I_{d_M}$ et en tension $V_{i_M}$
![[figure269.png]]^figure3

Caractéristique d'une diode idéale
![[figure270.png]]^figure4

Sauf spécification contraire, toutes les diodes considérées dans ce chapitre ont une caractéristique du type de celle représentée ci-dessus
![[figure271.png]]^figure5

Caractéristique de transfert d'un redresseur simple alternance
![[figure272.png]]^figure6

Caractéristique statique d'un redresseur élémentaire simple alternance
![[figure274.png]]^figure8

Variations de tension d'entrée $v_e(t)$ et de sortie $v_s(t)$ d'un redresseur élémentaire simple alternance
![[figure275.png]]^figure9

Tension de sortie d'un redresseur simple alternance pour des signaux d'entrée triangulaires de fréquence 200 Hz
![[figure276.png]]^figure10

Variations de la tension d'entrée $v_e(t)$ et de sortie $v_s(t)$ d'un redresseur simple alternance sans seuil
![[figure278.png]]^figure12

Variations de la tension d'entrée $v_e(t)$ d'un redresseur simple alternance sans seuil et de la tension de sortie $v_{s_0}(t)$ de son amplificateur opérationnel (en basse fréquence)
![[figure279.png]]^figure13

Caractéristique statique d'un redresseur simple alternance sans seuil
![[figure280.png]]^figure14

Caractéristique d'un redresseur double alternance
![[figure281.png]]^figure15

Variations des tensions dans un redresseur double alternance à diodes
![[figure283.png]]^figure17

Variations des tensions $v_e(t)$ et $v_s(t)$ dans un redresseur double alternance à pont de diodes
![[figure285.png]]^figure19

Caractéristique d'un redresseur double alternance à pont de diodes : il existe un seuil
![[figure286.png]]^figure20

Variations des tensions $v_e(t)$ et $v_s(t)$ aux bornes d'un redresseur double alternance sans seuil
![[figure289.png]]^figure23

Caractéristique du redresseur double alternance sans seuil
![[figure290.png]]^figure24

Courant $i(t)$ délivré par le redresseur bialternance et tension $v_s(t)$ redressée et filtrée par condensateur, en régime établi
![[figure292.png]]^figure26

Avec une capacité de filtrage suffisante, la tension redressée filtrée est quasi continue
![[figure293.png]]^figure27

Pourquoi choisir $t_0 \gg RC \gg T$ ?
![[figure295.png]]^figure29

$u_s(t)$ et $u(t)$. Les deux courbes ont été décalées pour plus de lisibilité. Dans le cas b., $u(t)$ suit presque exactement (à la précision du tracé) l'enveloppe $U(t)$
![[figure297.png]]^figure31
# Expériences
> [!warning]
> Voici des exemples de travaux pratiques qui abordent le sujet de ce chapitre : le [lien 1](https://www.studocu.com/row/document/ecole-nationale-des-sciences-appliquees/tp-redressement/tp1-redressement-simple-alternance/92934376), le [lien 2](https://www.studocu.com/row/document/ecole-nationale-polytechnique-alger/electronique-de-puissance-avancee/polycopie-menasria-azzeddine/63055851), le [lien 3](https://www.yumpu.com/fr/document/read/6395365/tp-electronique), le [lien 4](https://chamilo.univ-grenoble-alpes.fr/courses/UGA002054/document/TP-Eln1-POLY-2011-08-29.pdf), le [lien 5](https://jean-michel-laffaille-pagesperso.fr/JM_education/JM-edu/ElCinetique/elCinAsso/diode_TP3.pdf), le [lien 6](https://ft.univ-tlemcen.dz/assets/uploads/pdf/departement/gee/Manuel-TP-ELT-L2-ST-S4-Electricite.pdf), le [lien 7](https://dspace.univ-guelma.dz/jspui/bitstream/123456789/11214/1/polycopie_MENASRIA_Azzeddine.pdf), le [lien 8](http://roussetelec.free.fr/Files/tpalimentation.pdf), le [lien 9](https://fr.scribd.com/document/652709235/TP-7-Realisation-Detection-d-Enveloppe), le [lien 10](https://telum.umc.edu.dz/pluginfile.php/235212/mod_resource/content/4/TP_02_papier.pdf), le [lien 11](https://users.polytech.unice.fr/~ferrero/TPelec4/ep_unsa_elec4_tp_electronique_01_AM_2011.pdf), le [lien 12](https://www.alloschool.com/assets/documents/course-423/modulation-d-amplitude-cours-4-1.pdf), le [lien 13](http://h.pre.free.fr/wp-content/uploads/c3cours.pdf), le [lien 14](https://fr.scribd.com/document/834467441/TP-4-DEMODULATION-AM-241130-101243), le [lien 15](https://fr.scribd.com/document/716105221/TP2-demodulation-AM), le [lien 16](http://cedric.koeniguer.free.fr/polytech/elec/documents/TP/tp_diode.pdf), le [lien 17](http://boulant.nicolas.free.fr/cours/Terminale%20S/Travaux%20pratiques/Physique/TP_specialite/Radio_demodulation/TS_spe_demodulation_eleve.pdf), le [lien 18](https://toulouse-sgencfdt.fr/WORDPRESS_ITRF/wp-content/uploads/2022/01/filtre-radio.pdf), le [lien 19](http://venturi.marc.free.fr/TP/TP_Fascicule_premiere_periode.pdf), le [lien 20](http://lefevre.pc.free.fr/site_3/download/pdf/terminales/tpphysique/tsspetpp3.pdf).
# Autres notes
> [!warning]
> Une diode est un composant non linéaire. Il ne faut donc pas lui appliquer sans réfléchir les lois de l'électrocinétique linéaire.
> Une diode peut être modélisée par un composant linéaire par morceaux.