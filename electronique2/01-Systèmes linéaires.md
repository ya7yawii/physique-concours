---
titre: "[[01-Systèmes linéaires]]"
tags:
  - transformée-de-Laplace
  - fonction-de-transfert-opérationnelle
  - système-linéaire
  - impédance-opérationnelle
  - stabilité
  - systèmes-analogues
  - transformée-de-Fourier
crée: 22-11-2025, 13:47
---
# Formules
> [!note] Systèmes linéaires, continus et stationnaires
> ==**Un système est continu lorsque toutes les grandeurs, qui définissent son état, sont des fonctions continues du temps.**==
> Les systèmes continus sont définis par opposition aux ==**systèmes discrets**== (en temps ou en amplitude) qui sont séquentiels, échantillonnés, logiques, quantifiés, etc.
> Un système est linéaire lorsque la relation entre la grandeur d'entrée $e(t)$ et la grandeur de sortie $s(t)$ est une équation différentielle linéaire : $D_0s(t) + D_1\dfrac{ds(t)}{dt} + \cdots + D_n\dfrac{d^{n}s(t)}{dt^{n}} = N_0e(t) + N_1\dfrac{de(t)}{dt} + \cdots + N_m\dfrac{d^{m}e(t)}{dt^{m}}$.
> L'ordre du système linéaire est, par définition, l'ordre de son équation différentielle.
> ==**Un système linéaire est stationnaire, ou invariant dans le temps, si les coefficients $D_k$ et $N_j$ de son équation différentielle sont indépendants du temps.**==
> - Principe de superposition : Soit respectivement $s_1(t)$ et $s_2(t)$ les réponses du système aux excitations $e_1(t)$ et $e_2(t)$. Un système linéaire satisfait au principe de superposition, c'est-à-dire qu'à l'excitation : $e(t) = \lambda_1e_1(t) + \lambda_2e_2(t)$, où $\lambda_1$ et $\lambda_2$ sont des constantes, correspond la réponse : $s(t) = \lambda_1s_1(t) + \lambda_2s_2(t)$, les causes ajoutent leurs effets et les effets sont proportionnels aux causes.
> - Domaines de linéarité : Bien que les systèmes physiques ne soient jamais rigoureusement linéaires, il est cependant possible de les considérer comme tels si l'amplitude et la fréquence des signaux d'entrée sont comprises entre certaines limites qui définissent leurs ==**domaines de linéarité**==. Un exemple classique est celui du pendule simple, qui est un système linéaire quand ses oscillations sont de faible amplitude, les frottements solides étant négligés.
^par1

> [!note] Fonction de transfert d'un système linéaire : signaux sinusoïdaux
> Pour réviser cette notion, on pourra se reporter à l'ouvrage H-Prépa, Électronique-Électrocinétique, 1re année, [[06-Régime sinusoïdal forcé|chapitre 6]].

> [!note] Transformée de Laplace
> Associons à toute fonction $f(t)$ du temps, une fonction $F(p)$ de la variable complexe $p$ définie par : $\displaystyle F(p) = \int_{0_-}^{\infty}f(t)e^{-pt}dt$ sous réserve de convergence de l'intégrale. Cette dernière condition est physiquement peu contraignante.
> La fonction $F(p)$ est la transformée de Laplace de $f(t)$ et la fonction $f(t)$ est l'original de $F(p)$.
> Notons que la borne inférieure de l'intégrale de définition de la transformée de Laplace $F(p)$ est $0_-$. Par exemple, pour $f(t) = u(t)$ échelon débutant à $t = 0$, nous avons $f(0_-) = 0$ et $f(0_+) = 1$.
> - La somme des deux originaux $f_1(t) + f_2(t)$ se traduit par la somme de transformées $F_1(p) + F_2(p)$.
> - La multiplication de l'original $f(t)$ par une constante $a$ se traduit par la même opération sur la transformée $F(p)$ avec la même constante $a$.
> - La transformée de la dérivée de l'original est égale à $pF(p) - f(0_-)$. Dans l'hypothèse où $f(t)$ ainsi que ses dérivées successives $\dfrac{d^{m}f(t)}{dt^{m}}$ (pour $m = 0, \cdots, m = n - 1$) sont nulles à $t = 0_-$, il vient que la transformée de la dérivée $n^{ième}$ de l'original $\dfrac{d^{n}f(t)}{dt^{n}}$ est égale à $p^{n}F(p)$.
> - L'intégration entre $0_-$ et $t$ de l'original $f(t)$ équivaut à la division par $p$ de sa transformée $F(p)$.
> - Un original retardé de $\tau$ $(= f(t - \tau))$ se traduit par la multiplication de la transformée $F(p)$ par $e^{-p\tau}$ à la condition que $f(t) = 0$ pour $t < 0$.

> [!note] Quelques fonctions et transformées de Laplace utiles
> - L'échelon unité, est défini par $u(t) = 1$ pour $t > 0$. Sa transformée de Laplace est : $U(p) = \frac{1}{p}$.
> - Un échelon unité retardé de $\tau$ a pour transformée : $F(p) = \frac{e^{-p\tau}}{p}$.
> - Un créneau unité ([[#^figure2|fig. 2]]) de largeur $t_0$ est défini par : $e(t) = u(t) - u(t -t_0)$. Sa transformée de Laplace est égale à la différence entre les deux transformées précédentes : $E(p) = \frac{1 - e^{-pt_0}}{p}$.
> - L'impulsion unitaire de Dirac $\delta(t)$ ([[#^figure3|fig. 3]]) est égale à la limite pour $t_0 \rightarrow 0$ d'un créneau de largeur $t_0$ débutant à $t = 0$ et d'amplitude $\frac{1}{t_0}$. L'impulsion unitaire $\delta(t)$ est la dérivée de l'échelon unitaire $u(t)$. Nous en "déduisons" l'expression de sa transformée de Laplace $\Delta(p) = 1$. De point de vue dimensionnel, $\delta(t)$ a la dimension de l'inverse d'un temps.
> - La transformée $F(p)$ de $f(t) = e^{\alpha t}$ est égale à $\frac{1}{p - \alpha}$ à condition que $\mathcal{R}e(p) > \mathcal{R}e(\alpha)$.

> [!note] Fonction de transfert opérationnelle d'un signal quelconque (au 1ere année le signal est sinusoïdal)
> Considérons un système initialement au repos ($e(t)$ et $s(t)$ ainsi que leurs dérivées successives sont nulles à $t = 0_-$) dont l'équation différentielle est celui de [[#^par1|paragraphe 1]].
> La transformée de Laplace de l'équation différentielle s'écrit : $(D_0 + D_1p + \cdots + D_np^{n})S(p) = (N_0 + N_1p + \cdots + N_mp^{m})E(p)$, où $E(p)$ et $S(p)$ sont respectivement les transformées de Laplace de l'excitation $e(t)$ et de la réponse $s(t)$.
> Par définition, la fonction de transfert opérationnelle $H(p)$ du système est : $\displaystyle H(p) = \frac{S(p)}{E(p)} = \frac{N_0 + N_1p + \cdots + N_mp^{m}}{D_0 + D_1p + \cdots + D_np^{n}}$.
> Remarques :
> - La fonction de transfert est définie à l'aide d'un régime dont les conditions initiales sont nulles. Dans ce cas (fréquent) la réponse $s(t)$ du système s'obtient en cherchant l'original de $S(p)$.
> - Dans le cas d'une excitation sinusoïdale, nous retrouvons la définition de la fonction de transfert complexe en faisant $p=j\omega$.
> - Pour tenir compte de conditions initiales différentes il faut appliquer les formules de dérivation sous leurs formes complètes.
^par2

> [!note] Impédance opérationnelle
> Pour les systèmes électriques, par analogie avec la définition de l'impédance complexe $\underline{Z}(j\omega) = \frac{\underline{u}_m}{\underline{i}_m}$ d'un composant dipolaire linéaire passif, nous définirons son impédance opérationnelle par $Z(p) = \frac{U(p)}{I(p)}$ où $U(p)$ et $I(p)$ sont respectivement les transformées de Laplace de la tension $u(t)$ aux bornes du composant et de l'intensité $i(t)$ qui le traverse.
> Les impédances opérationnelles $Z(p)$ se déduisent des impédances complexes en remplaçant $j\omega$ par $p$ :
> - résistor : $Z(p) = \frac{U(p)}{I(p)} = R$ ; 
> - bobine : $Z(p) = \frac{U(p)}{I(p)} = Lp$ ;
> - condensateur : $Z(p) = \frac{U(p)}{I(p)} = \frac{1}{Cp}$.
> 
> Les lois d'association des impédances opérationnelles sont les mêmes que celles des impédances complexes vues en Première année. La détermination de la fonction de transfert opérationnelle se fait par la même méthode que celle de $\underline{H}(j\omega)$.

> [!note] Fonction de transfert et équation différentielle
> L'équation différentielle qui relie les grandeurs d'entrée $e(t)$ et de sortie $s(t)$ détermine la fonction de transfert. La réciproque est-elle toujours vraie ?
> Si le système est initialement au repos ($e(t)$, $s(t)$ et leurs dérivées nulles pour tout $t < 0$), il suffit, de connaître la fonction de transfert $H(p) = \frac{N(p)}{D(p)}$ pour déterminer $s(t)$. En effet, la transformée de Laplace $S(p)$ du signal de sortie est déterminée $S(p) = H(p)E(p)$ et il est possible d'en déduire $s(t)$.
> En revanche, avec des conditions initiales quelconques, un problème se pose si les polynômes $N(p)$ et $D(p)$ ne sont pas premiers entre eux ; dans ce cas, une simplification fait disparaître des termes et la fonction de transfert ne permet pas de déterminer la solution exacte.
> Ce cas est plutôt rare. Retenons donc que, "presque toujours", il est possible de retrouver l'équation différentielle en posant : $D(p)S(p) = N(p)E(p)$. En remplaçant à chaque fois $p^{n}$ par $\dfrac{d^{n}}{dt^{n}}$ on obtient l'équation différentielle en $s(t)$ et $e(t)$.

> [!note] Caractéristiques générales des fonctions de transfert
> - Ordre : ==**L'ordre de la fonction de transfert (de la [[#^par2|paragraphe 2]]) est égale au degré le plus élevé des polynômes $N$ et $D$ : ordre = sup(m, n).**==
> - Pôles et zéros : ==**Les racines de $N(p) = 0$ et de $D(p) = 0$ sont, respectivement et par définition, les zéros $z_j$ et les pôles $p_k$ de la fonction de transfert $H(p)$.**==
> En introduisant les zéros et les pôles d'une fonction de transfert, cette dernière peut s'écrire, avec A une constante réelle : $H(p) = A\frac{(p - z_1)(p - z_2)\cdots(p - z_m)}{(p - p_1)(p - p_2)\cdots(p - p_n)}$.
> L'ensemble des zéros et des pôles définit, au facteur $A$ près, la fonction de transfert du système.
> Les images des zéros et des pôles peuvent être placées dans le plan complexe ([[#^figure4|fig. 4]]). Les polynômes $N(p)$ et $D(p)$ sont à coefficients réels, donc les zéros et les pôles de la fonction de transfert sont soit réels, soit complexes conjugués. La configuration des zéros et des pôles dans le plan complexe admet l'axe des réels comme axe de symétrie.
> En regroupant, sous forme de produit, les facteurs dont les zéros sont conjugués tels que : $(p - z_j)(p - z_{j}^{*})$ et ceux dont les pôles sont conjugués tels que $(p - p_k)(p - p_{k}^{*})$, il est possible de décomposer les polynômes $N(p)$ et $D(p)$ en un produit de polynômes de degré un ou deux, à coefficients réels.
> Ainsi, la fonction de transfert $H(p)$ est factorisable sous la forme d'un produit de fonctions de transfert élémentaires $H_k(p)$ d'ordre 1 et 2 à coefficients : $\displaystyle H(p) = \prod_{k}H_k(p)$. Cette propriété établit l'importance des fonctions de transfert d'ordre 1 et 2 que nous allons étudier dans les chapitres qui suivent.

> [!note] Stabilité d'un système linéaire
> ==**Un système qui comporte une entrée et une sortie est stable si la réponse à toute excitation bornée est également bornée.**==
> Critère général de stabilité : Un système qui met en relation une grandeur d'entrée et une grandeur de sortie est caractérisé par sa fonction de transfert (de la [[#^par2|paragraphe 2]]).
> Ce système est stable si :
> - l'ordre du numérateur est au plus égal à celui du dénominateur : $m \leqslant n$ ;
> - les pôles (racines du dénominateur) sont à partie réelle strictement négative. Pour les systèmes d'ordre 1 et 2, cette dernière condition n'est réalisée que si tous les coefficients $D_i$ sont de même signe.

> [!note] Systèmes analogues
> ==**Deux systèmes de nature physiques différentes sont analogues lorsqu'ils sont régis par des systèmes d'équations différentielles de même forme.**==
> 
> Exemple : Analogie électromécanique de translation :
> Considérons le système mécanique ([[#^figure5|fig. 5a]]) dont l'équation est : $\displaystyle f(t) = m\dfrac{dv(t)}{dt} + hv(t) + k\int_{0}^{t}v(t)dt + f_k(0)$ avec $f_k(0)$ la force exercée par le ressort à l'instant initial.
> En comparant l'équation différentielle précédente à celle d'un circuit (R, L, C) en série ([[#^figure5|fig. 5b]]), excité par une f.e.m. $e(t)$ : $\displaystyle e(t) = L\dfrac{di(t)}{dt} + Ri(t) + \frac{1}{C}\int_{0}^{t}i(t)dt + u_C(0)$, nous constatons que le système mécanique et le système électrique sont régis par des équations différentielles de même forme. Ces analogies électromécaniques sont dites du type force-tension.
> Mais nous aurions pu considérer comme analogies ([[#^figure6|fig. 6]]), d'une part, le système mécanique précédent et, d'autre part, le circuit (G', L', C') en parallèle régi par l'équation différentielle : $\displaystyle \eta(t) = C'\dfrac{du(t)}{dt} + G'u(t) + \frac{1}{L'}\int_{0}^{t}u(t)dt + i_{L'}(0)$.
> Cette seconde analogie électromécanique est dite du type force-intensité.
> 
> Suivant la nature des systèmes examinés, nous parlerons d'analogies électromécaniques (de translation ou de rotation), d'analogies électroacoustiques, d'analogies électrothermiques, d'analogies électrohydrauliques, etc.

> [!note] Décomposition en série de Fourier d'un signal périodique
> Pour réviser cette notion, on pourra se reporter à l'ouvrage H-Prépa, Électronique-Électrocinétique, 1re année, [[12-Analyse harmonique|chapitre 12]].

> [!note] Généralisation : transformée de Fourier d'un signal non périodique
> Un signal physiquement réalisable ne peut être rigoureusement périodique : un signal périodique se répète indéfiniment alors qu'un signal réel a un début et une fin. Il est cependant possible de le décrire comme une superposition de signaux sinusoïdaux (ou, ce qui est équivalent, d'exponentielles complexes) à condition de remplacer la somme par une intégrale.
> Sous réserve de conditions mathématiques qui sont vérifiées pour les signaux physiquement réalisables, il est possible d'associer à un signal $s(t)$ une fonction $S(\omega)$ telle que : $\displaystyle s(t) = \sqrt{\frac{1}{2\pi}}\int_{-\infty}^{\infty}S(\omega)exp(j\omega t)d\omega$.
>  $S(\omega)$ est la transformée de Fourier, de $s(t)$. Nous admettrons qu'elle se calcule par : $\displaystyle S(\omega) = \sqrt{\frac{1}{2\pi}}\int_{-\infty}^{\infty}s(t)exp(-j\omega t)dt$.
>  Nous pouvons comprendre la transformée de Fourier comme une extension des séries de Fourier : à l'intervalle spectral $d\omega = 2\pi d\nu$, correspond une composante harmonique complexe élémentaire : $d\underline{s} = S(\omega)exp(j\omega t)d\omega$.
>  $S(\omega)$ est _a priori_ complexe, et contient donc une information d'amplitude (son module) et une information de phase (son argument).
>  - Spectre de fréquence : $S(\omega)$ transformée de Fourier de $s$, représente la distribution des pulsations (ou des fréquences) de $s(t)$.
>  Le tracé de la courbe $|S(\omega)|$ est donc une représentation du spectre de $s(t)$. A l'intervalle spectral $d\omega$, on associe une composante harmonique élémentaire de pulsation $\omega$ et d'amplitude élémentaire $ds_m = |S(\omega)|d\omega$.
>  - Signal sinusoïdal limité dans le temps : Dans ce cas, sa transformée de Fourier se décompose en deux pics de largeur $\Delta\omega = \frac{4\pi}{t_{fin} - t_{début}}$, centrés sur les pulsations $-\omega$ et $\omega$ ([[#^figure7|fig. 7]]).
>  Notons que $\Delta\omega$ est d'autant plus faible que $t_{fin} - t_{début}$ est grand, c'est-à-dire que l'extension temporelle du signal sinusoïdal est grande. Ce résultat très important sera aussi utilisé dans les cours sur les ondes et en l'optique ondulatoire.
>  Remarque : Cette séparation en deux pics de pulsation $\omega$ et $-\omega$ n'est qu'un artifice mathématique que l'on peut retrouver pour une fonction rigoureusement sinusoïdale : $s(t) = s_m\cos(\omega t + \varphi) = \frac{S_m}{2}\cos(\omega t + \varphi) + \frac{S_m}{2}\cos(-\omega t - \varphi)$.
# Définitions
==**Signal**== : Une grandeur physique mesurable

==**Système**== : Un dispositif dont l'état est déterminé par un ou plusieurs signaux.

==**Opérateur**== :
Un opérateur est un système qui établit une relation entre deux signaux ; la valeur de la grandeur (ou signal) de sortie $s(t)$ est déterminée par l'évolution de la grandeur (ou signal) d'entrée $e(t)$. Un opérateur est unidirectionnel si le signal de sortie est sans influence sur le signal d'entrée.
Ces définitions se généralisent à des opérateurs plus complexes comportant plusieurs signaux d'entrée et/ou plusieurs signaux de sortie.

==**Représentations d'un opérateur**== :
Un utilisateur ne s'intéresse pas au fonctionnement interne de l'opérateur, mais seulement à ses interactions avec l'extérieur. Nous allons donc utiliser des schémas simplifiés où l'opérateur est une « boîte noire ». Nous utiliserons deux types de représentations :
- La représentation unifilaire où les opérateurs d'un système sont représentés par des boîtes reliées par des fils qui symbolisent les signaux. Pour un opérateur unidirectionnel, des flèches indiquent les grandeurs d'entrée et de sortie.
- Les systèmes électriques ou électroniques se prêtent à une représentation bifilaire qui permet de visualiser à la fois les courants et les tensions d'entrée et de sortie.
La [[#^figure1|figure 1]] donne ainsi les différentes représentations d'un potentiomètre avec suiveur. La présence de l'A.O. monté en suiveur lui confère son caractère unidirectionnel.
- Le schéma expérimental est nécessaire pour réaliser concrètement l'opérateur à partir de composants.
- Le schéma bifilaire est suffisant pour déterminer toutes les grandeurs d'entrée et de sortie.
- Le schéma unifilaire est suffisant pour symboliser la relation entre les tensions d'entrée et de sortie, mais insuffisant pour caractériser complètement le comportement de l'opérateur dans un système plus complexe ; ainsi, il ne permet pas de prévoir la valeur du courant $i_e$.
Remarque : Le schéma dit « expérimental » est également symbolique : il ne décrit pas les multiples connexions internes à l'A.O. et ne fait pas mention de son alimentation.

==**Description fréquentielle d'un signal réel**== :
Pour un signal périodique de période $T$, la suite (infinie) des $A_n$​ et des $B_n$​ contient toutes les informations qui permettent de reconstituer le signal $s(t)$.
Pour un signal non périodique, la transformée de Fourier $S(\omega)$ de $s(t)$ contient toutes les informations relatives au signal $s(t)$.
==**Les coefficients de la série de Fourier (ou la transformée de Fourier pour un signal non périodique) constituent une description fréquentielle du signal dont la description temporelle est $s(t)$. Les deux descriptions, temporelle et fréquentielle, sont totalement équivalentes et la connaissance de l'une permet de déterminer complètement l'autre.**==
Si on adopte le point de vue temporel, la résolution de l'équation différentielle donne directement la forme de $s(t)$.
Si on adopte le point de vue fréquentiel, la fonction de transfert harmonique indique la façon dont le système agit sur le spectre en fréquence du signal.
# Diagrammes
Potentiomètre avec suiveur. a. Schéma expérimental. b. Schéma bifilaire. c. Schéma unifilaire
![[electronique2/attachments-electronique2/figure1.png]]^figure1

Systèmes analogues. a. Système mécanique. b. Système électrique.
![[electronique2/attachments-electronique2/figure5.png]]^figure5

Autres systèmes analogues. a. Système mécanique. b. Système électrique.
![[electronique2/attachments-electronique2/figure6.png]]^figure6
# Graphiques
Créneau $e(t)$ débutant à $t = 0$ avec une durée $t_0$ et une amplitude unité
![[electronique2/attachments-electronique2/figure2.png]]^figure2

Lorsque la durée $t_0$ du créneau $e(t)$ tend vers zéro, le signal $e(t)$ tend vers l'impulsion unité
![[electronique2/attachments-electronique2/figure3.png]]^figure3

Configuration des zéros ($\circ$) et des pôles ($\times$) de $H(p)$
![[electronique2/attachments-electronique2/figure4.png]]^figure4

Signal sinusoïdal (de pulsation $\omega_0$) limité dans le temps et sa transformée de Fourier
![[electronique2/attachments-electronique2/figure7.png]]^figure7
# Expériences

# Autres notes
