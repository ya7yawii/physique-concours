---
titre: "[[02-Étude fréquentielle des systèmes linéaires]]"
tags:
  - passe-bas
  - passe-haut
  - passe-bande
  - déphaseur
  - coupe-bande
  - ordre-un
  - ordre-deux
  - caractère-dérivateur
  - caractère-intégrateur
crée: 23-11-2025, 14:22
---
# Formules
> [!note] Régime harmonique forcé
> - Condition d'apparition d'un régime harmonique forcé : ==**Un système linéaire stable soumis à une excitation sinusoïdale de pulsation $\omega$ admet une réponse sinusoïdale de même pulsation, dite réponse forcée. C'est la réponse effectivement observable après l'amortissement du régime libre.**==
> - Propriété des signaux sinusoïdaux : À une excitation sinusoïdale correspond, pour un système linéaire stable, une réponse forcée sinusoïdale. Une proposition logiquement équivalente est donc : ==**Si la réponse forcée à une excitation sinusoïdale n'est pas sinusoïdale, alors le système n'est pas linéaire. Nous disposons ainsi d'un critère pour tester la linéarité d'un système.**==
> Soumettons un système à une excitation sinusoïdale $e(t)=e_m\cos(\omega t)$ :
> 	- si le système est linéaire, la réponse permanente est sinusoïdale : $s(t)=s_m\cos⁡(\omega t+\phi_s)$ ;
> 	- si le système n'est pas linéaire, la réponse permanente est périodique sans être sinusoïdale. Le spectre de fréquence du signal s'est enrichi : il comportera plusieurs fréquences (sans que celles-ci incluent nécessairement $f = \frac{\omega}{2\pi}$​) ; en effet tout signal périodique est décomposable en série de Fourier : $\displaystyle s(t) = C_0 + \sum_{k}C_k\cos⁡(k\omega t+\phi_k)$.
> 	La présence de la composante $C_0$​ révèle un effet de ==**redressement partiel**== : le signal $s(t)$ n'est pas, comme $e(t)$, à valeur moyenne nulle ; la présence des harmoniques $C_k$​, d'ordre $k > 1$, révèle un effet de ==**distorsion harmonique**== ; celle-ci se chiffre par le taux de distorsion harmonique : $D_h = \frac{\sqrt{\displaystyle\sum_{k > 1}C_k^2}}{C_1}$. Plus le taux de distorsion harmonique $D_h$ est élevé, plus le caractère non linéaire du système et accentué. Évidemment pour un système linéaire, $D_h = 0$.

> [!note] Caractéristiques des fonctions de transfert harmoniques
> Pour réviser les notions de module et argument d'une fonction de transfert et le diagramme de Bode, on pourra se reporter à l'ouvrage H-Prépa, Électronique-Électrocinétique, 1re année, [[08-Fonctions de transfert des réseaux linéaires|chapitre 8]].

> [!note] Filtrage : Méthode générale d'étude
> Pour réviser cette méthode, on pourra se reporter à l'ouvrage H-Prépa, Électronique-Électrocinétique, 1re année, [[12-Analyse harmonique|chapitre 12]]. Elle est résumée sur la [[figure311.png|figure 3]].
^par1

> [!note] Système d'ordre 1
> - Passe-bas d'ordre 1 : L'étude dans ce chapitre est presque le même que celui des chapitres [[08-Fonctions de transfert des réseaux linéaires|8]] et [[12-Analyse harmonique|12]] de l'ouvrage H-Prépa, Électronique-Électrocinétique, 1re année. On ajoute que l'expression générale du filtre est $\displaystyle H(p) = \frac{1}{1 + \tau p}$ avec $\tau$ est la constante de temps du système. Le point de concours des asymptotes de la courbe de réponse en gain est appelé ==**point de cassure**==. En outre, pour la courbe de réponse en phase, quand $\omega$ croît de zéro à l'infini, la ==**rotation de phase**== est : $\Delta\phi = \phi_H - \phi_B = -\frac{\pi}{2} - 0 = -\frac{\pi}{2}$ avec $\phi_H$ la valeur asymptotique du déphasage en haute fréquence et $\phi_B$ celle en basse fréquence.
> L'application de la méthode étudiée au [[#^par1|paragraphe 1]] nous permet d'affirmer, grâce à l'analyse de Fourier :
> 	- dans la bande passante : seuls les harmoniques de rang élevé sont atténués, donc les discontinuités sont "filtrées" ;
> 	- en limite de bande passante : seuls la composante continue et quelques harmoniques sont transmis, ce qui déforme le signal ;
> 	- hors de la bande passante : les différents harmoniques sont tous atténués. Seule la composante continue est transmise.
> 
> - Passe-haut d'ordre 1 : L'étude dans ce chapitre est presque le même que celui des chapitres [[08-Fonctions de transfert des réseaux linéaires|8]] et [[12-Analyse harmonique|12]] de l'ouvrage H-Prépa, Électronique-Électrocinétique, 1re année. On ajoute que l'expression générale du filtre est $\displaystyle H(p) = \frac{\tau p}{1 + \tau p}$ avec $\tau$ est la constante de temps du système.
> Interprétations par l'analyse de Fourier : Pour un signal d'entrée dont la fréquence se situe :
> 	- hors de la bande passante : seuls les harmoniques de rang élevé sont transmises : le signal est très déformé ;
> 	- en limite de bande passante : le signal est encore très déformé ;
> 	- dans la bande passante : seule la composante continue est éliminée : nous récupérons la partie variable du signal d'entrée légèrement déformée.
> 
> - Déphaseur d'ordre 1 : Les ==**déphaseurs**==, ou ==**passe-tout**==, sont des systèmes qui n'introduisent aucune atténuation. Leur bande passante est $[0 ; +\infty[$. Ils sont uniquement caractérisés par leur courbe de réponse en phase ([[#^figure3|fig. 3]]).
> Établissons la fonction de transfert $H(p)$ d'un déphaseur d'ordre 1. Elle est de module 1 pour toutes les fréquences. Son numérateur et son dénominateur sont donc conjugués, soit ; $\displaystyle H(p) = \frac{1 - \tau p}{1 + \tau p}$. En régime harmonique, introduisons la pulsation réduite $x = \tau\omega = \frac{\omega}{\omega_0}$, il vient $\phi(x) = -2\arctan⁡(x)$. Nous obtenons ainsi immédiatement le tracé de la courbe de réponse en phase du déphaseur et celle de son diagramme asymptotique ([[#^figure3|fig. 3]]). Le point $A\left(0, -\frac{\pi}{2}\right)$ est centre de symétrie et point d'inflexion. Quand $\omega$ croît de zéro à l'infini, la rotation totale de phase est : $\Delta\phi = -\pi$.
> Actions sur un signal périodique ([[#^figure4|fig. 4]]) :
> Un filtre passe-tout, ou déphaseur, n'élimine aucune composante du signal :
> 	- la composante continue est transmise ;
> 	- les discontinuités sont transmises avec des valeurs opposées.
> Pour un signal périodique :
> 	- de fréquence très inférieure à $f_0$​ : le signal est transmis sans déformation, sauf au niveau des discontinuités ;
> 	- de fréquence très supérieure à $f_0$​​ : le signal de sortie est proche du signal d'entrée. Les composantes variables sont en opposition.
> 
> - Interprétation par l'analyse de Fourier :
> Le filtre passe-tout introduit un déphasage variable avec la fréquence. Un déphasage de $\pi$ se traduit par une inversion du signal.
> La composante continue est toujours transmise. Intéressons-nous à la composante variable. Pour un signal d'entrée :
> 	- de basse fréquence : le signal de sortie est retardé sans déformation ;
> 	- de fréquence $f_0$ : le signal est très modifié ;
> 	- de haute fréquence : la composante variable est inversée.

> [!note] Passe-bas d'ordre 2
> Les fonctions de transfert des systèmes linéaires d'ordre 2 ont pour dénominateur des polynômes de degré 2 en $p$.
> La fonction de transfert d'ordre 2 la plus simple est celle du passe-bas : $\displaystyle H(p) = \frac{1}{1 + 2\sigma\tau p + \tau^{2}p^{2}}​$ où $\tau$ est la constante de temps du système, $2\sigma$ son facteur d'amortissement, $Q = \frac{1}{2\sigma}$​ son facteur de qualité et $\omega_0 = \frac{1}{\tau}​$ sa pulsation propre.
> La pulsation réduite étant notée $x = \frac{\omega}{\omega_0}$​, la fonction de transfert s'écrit : $\underline{H}(j\omega_0 x) = \frac{1}{1 + 2\sigma(jx)+(jx)^{2}}$. Le dénominateur $D = 1 + 2\sigma(jx)+(jx)^{2}$ est un trinôme en $jx$ dont le discriminant réduit est $\Delta' = \sigma^{2} - 1$.
> - Premier cas $\Delta' > 0$ ($\sigma > 1$ ou $Q < \frac{1}{2}$) : Les racines de $D$ sont réelles et négatives. Il en résulte que $D(jx)$ peut être factorisé en un produit de deux binômes à coefficients réels positifs de degré 1 en $jx$ : $D = \left(1 - \frac{jx}{jx_1}\right)\left(1 - \frac{jx}{jx_2}\right) = \left(1 + \frac{jx}{x_{1}^{'}}\right)\left(1 + \frac{jx}{x_{2}^{'}}\right)$.
> Pour les constructions des diagrammes de Bode, il est utile de remarquer que $x_{1}^{'}x_{2}^{'} = 1$. La fonction de transfert du système s'analyse alors en un produit de deux fonctions de transfert de passe-bas d'ordre 1 : $\underline{H}(j\omega_0 x) = \frac{1}{\left(1 + \frac{jx}{x_{1}^{'}}\right)\left(1 + \frac{jx}{x_{2}^{'}}\right)} = \underline{H}_1(j\omega_0 x)\underline{H}_2(j\omega_0 x)$.
> Traçons, dans les mêmes axes de Bode, les diagrammes asymptotiques des réponses en gain $G_{A_1}(x)$ et $G_{A_2}(x)$ respectivement de $\underline{H}_1(j\omega_0 x)$ et de $\underline{H}_2(j\omega_0 x)$.
> Le diagramme asymptotique de la réponse en gain $G_A​(x)$ de $H(j\omega_0 x)$ s'obtient par addition des diagrammes asymptotiques précédentes ([[#^figure5|fig. 5a]]) : $G_A​(x) = G_{A_1}(x) + G_{A_2}(x)$. Cette construction s'effectue sans difficulté et avec précision. La courbe de réponse en gain $G(x)$ de $\underline{H}(j\omega_0 x)$ $(G(x) = G_1(x) + G_2(x))$ se trace en s'aidant du diagramme asymptotique $G_A(x)$.
> Nous procéderons de même pour le tracé du diagramme asymptotique $\phi_A(x)$ de phase et pour celui de la courbe de réponse en phase $\phi(x)$ ([[#^figure5|fig. 5b]]).
> ==**L'atténuation asymptotique en haute fréquence est de 40 dB par décade et la variation totale de phase est $-\pi$.**==
> - Deuxième cas $\Delta' = 0$ ($\sigma = 1$ ou $Q = \frac{1}{2}$) : Le dénominateur $D$ admet une racine réelle double $jx = -\sigma = -1$. La fonction de transfert $H(j\omega_0 x)$ du système s'analyse en le carré d'une fonction de transfert d'un passe-bas d'ordre 1 : $\underline{H}(j\omega_0 x) = \left(\frac{1}{1 + jx}\right)^{2} = \underline{H}_{1}^{2}(j\omega_0 x)$. Le diagramme de Bode correspondant se trace selon la méthode utilisée pour le cas précédent (fig. 6).
> ==**L'atténuation asymptotique haute fréquence est encore de 40 dB par décade et la variation totale de phase est $-\pi$ : ce sont deux caractéristiques des filtres passe-bas d'ordre 2.**==
> - Troisième cas $\Delta' < 0$ ($\sigma < 1$ ou $Q > \frac{1}{2}$) : Les racines du polynôme $D$ en $jx$ sont complexes et la fonction de transfert $H(j\omega_0 x)$ ne peut plus être décomposée en un produit de deux fonctions de transfert d'ordre un à coefficients réels. L'étude dans ce chapitre est presque le même que celui de [[09-Filtres du deuxième ordre|chapitre 9]] de l'ouvrage H-Prépa, Électronique-Électrocinétique, 1re année.

> [!note] Passe-haut d'ordre 2
> L'étude dans ce chapitre est presque le même que celui de [[09-Filtres du deuxième ordre|chapitre 9]] de l'ouvrage H-Prépa, Électronique-Électrocinétique, 1re année. On ajoute que l'expression générale du filtre est $\displaystyle H(p) = \frac{\tau^{2}p^{2}}{1 + 2\sigma\tau p + \tau^{2}p^{2}}$.

> [!note] Passe-bande d'ordre 2
> L'étude dans ce chapitre est presque le même que celui des chapitres [[09-Filtres du deuxième ordre|9]] et [[12-Analyse harmonique|12]] de  l'ouvrage H-Prépa, Électronique-Électrocinétique, 1re année. On ajoute que l'expression générale du filtre est $\displaystyle H(p) = \frac{2\sigma\tau p}{1 + 2\sigma\tau p + \tau^{2}p^{2}}$. Il faut ajouter que ==**quand $\omega$ varie de zéro à l'infini, la rotation de phase est $\Delta\phi = -\pi$**==. Il y a aussi la question de sélectivité du filtre : Le filtre est d'autant plus sélectif que la bande de fréquences transmises (autour de $f_0$) est peu étendue. En déterminant sa bande passante (voir [[09-Filtres du deuxième ordre|Chapitre 9]]), nous remarquons qu'==**un passe-bande est d'autant plus sélectif que son facteur d'amortissement $2\sigma$ est faible (ou que son facteur de qualité $Q$ est élevé).**==
> - Action sur un signal périodique d'un filtre passe-bande à bande large : Pour les schémas ([[#^figure6|fig. 6]]) $Q = 0,1$. Un filtre passe-bande à large bande a les propriétés suivantes :
> 	- il élimine la composante continue d'un signal ;
> 	- le signal de sortie ne présente pas de discontinuité ;
> pour un signal d'entrée périodique de fréquence :
> 	- très inférieure à la fréquence de coupure $f_B$​ : le signal de sortie est d'amplitude très faible sauf au niveau des discontinuités du signal (effet voisin de celui du filtre passe-haut) ;
> 	- comprise entre $f_B$​ et $f_H$​ : le signal de sortie est voisin de la partie variable du signal d'entrée ;
> 	- très supérieure à $f_H$​​ : le signal de sortie est d'amplitude très faible (effet identique à celui du filtre passe-bas, sauf vis-à-vis de la composante continue qui est éliminée).
> - Interprétation par l'analyse de Fourier : Pour le signal d'entrée de :
> 	- basse fréquence : seules les « hautes fréquences » situées dans la bande passante sont transmises. Le filtre se comporte comme un passe-haut d'ordre 1 ;
> 	- dans la bande passante : le continu et les harmoniques de rang élevé sont éliminés. Nous récupérons la partie variable du signal d'entrée, déformée ;
> 	- haute fréquence : le comportement vis-à-vis de ce signal est identique à celui d'un filtre passe-bas d'ordre 1.
> - Action sur un signal périodique d'un filtre passe-bande à bande étroite : Pour les schémas ([[#^figure7|fig. 7]]) $Q = 10$. Un filtre passe-bande, à bande étroite a les propriétés suivantes :
> 	- c'est un filtre sélectif ;
> 	- il ne transfère que les composantes sinusoïdales du signal d'entrée proche de sa fréquence de résonance, $f_0$ ;
> pour un signal d'entrée périodique de fréquence :
> 	- très inférieure à la fréquence de résonance $f_0$​, le signal de sortie est d'amplitude négligeable ;
> 	- voisine de $f_0$​, seule cette fréquence est transmise ; si un seul harmonique est dans la bande passante du filtre alors le signal de sortie est voisin d'une sinusoïde de fréquence $f_0$​ ;
> 	- très supérieure à $f_0$​ : le signal de sortie est d'amplitude négligeable.
>  - Interprétation par l'analyse de Fourier : Avec un coefficient de qualité de l'ordre de 10, seules les fréquences voisines de $f_0$​ sont transmises ; les autres étant « arrêtées ». Pour un signal d'entrée de :
> 	 - fréquence $f_0$​ : avec un coefficient de qualité de l'ordre 10, le signal de sortie est quasiment sinusoïdal de fréquence $f_0$​ ;
> 	 - haute fréquence : le signal de sortie est négligeable, car rien ne passe ;
> 	 - basse fréquence : le signal de sortie peut faire apparaître des oscillations amorties de fréquence $f_0$​.

> [!note] Coupe-bande d'ordre 2
> Le système étudié étant défini par la fonction de transfert : $\displaystyle H(p) = \frac{(1 + \tau^{2}p^{2})}{1 + 2\sigma\tau p + \tau^{2}p^{2}}$ ([[#^figure8|fig. 8]]). notons $\tau = \frac{1}{\omega_0}$ et $x = \frac{\omega}{\omega_0}$ la pulsation réduite. Il vient $\displaystyle \underline{H}(j\omega_0 x) = \frac{1 + (jx)^{2}}{1 + 2\sigma(jx) + (jx)^{2}}$.
> - Courbe de réponse en gain : il apparaît que la courbe de réponse en gain admet, en axes de Bode, l'axe des gains comme axe de symétrie et asymptote, puisque $G$ tend vers $-\infty$ quand $x$ tend vers 1.
> Enfin, quand $X$ tend vers $\pm \infty$, le gain tend asymptotiquement vers zéro : les asymptotes basse fréquence et haute fréquence sont respectivement les demi-axes des pulsations négatives et positives.
> Le tracé des courbes de réponse ([[#^figure8|fig. 8]]) montre que le système étudié est un coupe-bande d'ordre 2.
> ==**Ce coupe-bande est un réjecteur, car la pulsation centrale $\omega_0$ n'est pas transmise.**==
> - Courbe de réponse en phase : Décomposons la fonction de transfert sous la forme : $\displaystyle \underline{H}(j\omega_0 x) = \frac{1}{1 + 2\sigma(jx) + (jx)^{2}}(1 - x^{2}) = \underline{H}_1(j\omega_0 x)\underline{H}_2(j\omega_0 x)$. Nontons par $\phi_1(x)$ le déphasage introduit par le passe-bas d'ordre 2 et par $\phi_2(x)$ celui introduit par la fonction de transfert $\underline{H}_2(j\omega_0 x) = 1 - x^{2}$ :
> $$
> \phi_2(x) =
> \begin{cases}
> 0 & si & x < 1\\
> \pi & si & x > 1
> \end{cases}
> $$
> Le déphasage $\phi(x)$ introduit par le coupe-bande est égal à : $\phi(x) = \phi_1(x) + \phi_2(x)$.
> ==**Les courbes de réponse en phase du coupe-bande présentent une discontinuité de phase $\pi$ en $x = 1$**== ([[#^figure9|fig. 9]]).

> [!note] Déphaseur d'ordre 2
> Ces circuits ont des fonctions de transfert de la forme : $\displaystyle H(p) = \frac{1 - 2\sigma\tau p + \tau^{2}p^{2}}{1 + 2\sigma\tau p + \tau^{2}p^{2}}$ avec un numérateur conjugué du dénominateur.
> Nous pouvons le réaliser en branchant en cascade deux déphaseurs d'ordre 1 à A.O. dont le schéma est donné sur la [[#^figure10|figure 10]]. Dans ce cas, nous obtenons $\sigma = 1$.
> En régime harmonique, notons $x = \frac{\omega}{\omega_0}$ la pulsation réduite ; il vient $\displaystyle \underline{H}(j\omega_0 x) = \frac{(1 - x^{2}) - 2\sigma jx}{(1 - x^{2}) + 2\sigma jx}$. Le déphasage $\phi(x)$ introduit par le déphaseur est : $\phi(x) = 2\left[-\frac{\pi}{2} + \arctan\left(\frac{1 - x^{2}}{2\sigma x}\right)\right]$. La courbe de réponse en phase d'un déphaseur d'ordre 2 est donnée sur la [[#^figure11|figure 11]].
> ==**La rotation totale de phase, lorsque la fréquence varie de zéro à l'infini, est $\Delta\phi = -2\pi$.**==

> [!note] Systèmes linéaires d'ordre quelconque
> Considérons un système linéaire d'ordre quelconque dont la fonction de transfert est $H(p)$. Son diagramme de Bode se trace] en procédant comme suit (voir la méthode détaillée [ici](https://www.youtube.com/watch?v=BhCpNjElkiQ&t=44s)):
> - décomposons la fonction de transfert $H(p)$ en facteurs élémentaires d'ordre 1 et 2 dont nous connaissons le diagramme de Bode : $\displaystyle H(p) = \prod_{k}H_k(p)$ ;
> - traçons ensuite, dans les mêmes axes de Bode, les diagrammes asymptotiques $G_{A_k}$ des courbes $G_k = 20\log|H_k(p)|$ pour chacun de ces facteurs élémentaires ;
> - additionnons les diagrammes asymptotiques $G_{A_k}$, pour obtenir le diagramme asymptotique $G_A$ de la courbe de réponse en gain du systéme : $\displaystyle G_A = \sum_{k}G_{A_k}$.
> Connaissant le diagramme asymptotique de la réponse en gain, nous traçons cette dernière ;
> - nous procédons, selon la même méthode, pour le tracé du diagramme asymptotique $\phi_A$, de la courbe de réponse en phase : $\displaystyle \phi_A = \sum_{k}\phi_{A_k}$ et pour celui de la courbe de réponse en phase.

> [!note] Caractère intégrateur d'un filtre
> Cherchons a quelle condition un filtre quelconque a un caractère intégrateur pour un signal périodique.
> Remarquons d'abord qu'un filtre ne peut pas présenter de caractère intégrateur vis-a-vis d'un signal continu. En effet, la primitive d'une constante croît ou décroit linéairement en fonction du temps. La tension de sortie du filtre étant limitée, il y aurait alors saturation du signal de sortie.
> Nous nous limiterons donc a des signaux de valeur moyenne nulle.
> Soit $v_e(t)$ le signal (pulsation $\omega_0$) à l'entrée du filtre. Sa décomposition de Fourier s'écrit : $\displaystyle v_e(t) = \sum_{n>0}a_n\cos(n\omega_0t + \phi_n)$ et sa primitive de valeur moyenne nulle : $\displaystyle \int v_e dt = \sum_{n>0}\frac{a_n}{n\omega_0}\cos(n\omega_0t + \phi_n - \frac{\pi}{2})$.
> Pour chacun des harmoniques, le signal est déphasé de $-\frac{\pi}{2}$ et son amplitude est divisée par sa pulsation $n\omega_0$ ([[#^figure12a|fig. 12a]] et [[#^figure12b|b]]).
> 
> Les deux conditions pour qu'un filtre présente un caractère intégrateur sur un signal de fréquence $f_0$, sont donc :
> - un déphasage introduit par le filtre voisin de $-\frac{\pi}{2}$ (ou de $\frac{\pi}{2}$ s'il y a inversion du signal) ;
> - un gain $G_{dB} \approx 20\log\frac{\omega_c}{\omega}$ avec une pente de -20 dB par décade ($\omega_c$ est une pulsation caractéristique) pour tous les harmoniques d'amplitude importante du signal d'entrée, c'est-à-dire dans une bande de fréquences $[f_0 ; nf_0]$, ou $n$ représente le rang du dernier harmonique d'amplitude importante.
> Le signal de sortie est alors $v_s \approx \omega_c\int v_e dt$ si le déphasage est de $-\frac{\pi}{2}$ et $v_s \approx -\omega_c\int v_e dt$ s'il est de $\frac{\pi}{2}$.
> Cette condition est vérifiée pour les filtres passe-bas du premier ordre et passe-bande du deuxième ordre si $f_0$ est nettement supérieure à leur fréquence de coupure haute $f_H$ (en général, $f_0 > 10f_H$ suffit).

> [!note] Caractère dérivateur d'un filtre
> Cherchons a quelle condition un filtre quelconque a un caractère dérivateur pour un signal périodique.
> Soit $v_e(t)$ le signal (pulsation $\omega_0$) à l'entrée du filtre. Sa décomposition de Fourier s'écrit : $\displaystyle v_e(t) = \sum_{n>0}a_n\cos(n\omega_0t + \phi_n)$ et sa dérivée : $\displaystyle \dfrac{dv_e}{dt} = \sum_{n>0}n\omega_0a_n\cos(n\omega_0t + \phi_n + \frac{\pi}{2})$.
> Pour chacun des harmoniques, le signal est déphasé de $\frac{\pi}{2}$ et son amplitude multipliée par sa pulsation $n\omega_0$.
> 
> Les deux conditions pour qu'un filtre présente un caractère dérivateur sur un signal de fréquence $f_0$, sont donc :
> - un déphasage introduit par le filtre voisin de $\frac{\pi}{2}$ (ou de $-\frac{\pi}{2}$ s'il y a inversion du signal) ;
> - un gain $G_{dB} \approx 20\log\frac{\omega}{\omega_c}$ avec une pente de 20 dB par décade ($\omega_c$ est une pulsation caractéristique) pour tous les harmoniques d'amplitude importante du signal d'entrée, c'est-à-dire dans une bande de fréquences $[f_0 ; nf_0]$, ou $n$ représente le rang du dernier harmonique d'amplitude importante.
> Le signal de sortie est alors $v_s \approx \frac{1}{\omega_c}\dfrac{dv_e}{dt}$ si le déphasage est de $\frac{\pi}{2}$ et $v_s \approx -\frac{1}{\omega_c}\dfrac{dv_e}{dt}$ s'il est de $-\frac{\pi}{2}$.
> Cette condition est vérifiée pour les filtres passe-haut du premier ordre et passe-bande du deuxième ordre si $nf_0$ est nettement inférieure à leur fréquence de coupure basse $f_B$ ($n = 10$ et $nf_0 < \frac{f_B}{10}$ suffit en général, soit $f_0 < \frac{f_B}{100}$). La condition est plus contraignante que pour les intégrateurs, où $f_0 > 10f_B$ suffisait ([[#^figure13a|fig. 13a]] et [[#^figure13b|b]]).
> 
> Ce résultat peut être généralisé à des signaux non périodiques dont les temps de variations caractéristiques sont grandes devant $\frac{1}{f_B}$.
^par2

> [!note] Caractère dérivateur d'un filtre résonant
> Étudions la réponse d'un filtre passe-bande (R, L, C) de fréquence de résonance $f_0 = 1 kHz$ et de facteurs de qualité $Q = 0,5$ et $Q = 10$ à un signal triangulaire de fréquence $f = 50 Hz$.
> L'asymptote basse fréquence d'un filtre passe-bande est : $G_{dB} = 20\log\frac{f}{f_1}$ $(f_1 = Qf_0)$ et $\phi = -\frac{\pi}{2}$.
> Les conditions énoncées au [[#^par2|paragraphe précédent]] semblent être vérifiées :
> - les harmoniques d'un signal triangulaire sont en $\frac{1}{n^{2}}$, donc ceux de fréquence supérieure à $f_1$, sont négligeables ;
> - la forme asymptotique du diagramme de Bode pour $f \ll f_1$, correspond à un caractère dérivateur.
> 
> Le signal de sortie devrait être $v_s \approx \frac{1}{2\pi f_1}\dfrac{dv_e}{dt}$.
> Observons la [[#^figure14|figure 14]].
> Le résultat est conforme à l'étude du [[#^par2|paragraphe précédent]] pour un facteur de qualité $Q = 0,5$ : $v_s$ est un signal créneau d'amplitude 64 mV, ce qui correspond bien à $\frac{1}{2\pi f_1}\dfrac{dv_e}{dt}$ avec $\dfrac{dv_e}{dt} = 4$ volt par période. Le signal d'entrée est bien dérivé ([[#^figure15a|fig. 15a]]).
> 
> En revanche, pour $Q = 10$ : le signal de sortie est un créneau superposé à un système d'oscillations amorties, semblables aux oscillations libres de l' intensité dans un circuit (R, L, C) en série, de pseudo-fréquence voisine de 1 kHz. Le montage n'est pas dérivateur.
> La [[#^figure15b|figure 15b]] montre que le filtre de coefficient de qualité $Q = 10$ amplifie de façon trop importante les harmoniques de fréquences voisine de 1 kHz. Leur amplitude est non négligeable dans le signal de sortie et contribue aux oscillations amorties.
> Remarquons que l'amplitude de 3 mV du créneau est compatible avec la formule $\frac{1}{2\pi f_1}\dfrac{dv_e}{dt}$.
> ==**Un filtre passe-bande ne présente un caractère dérivateur a basse fréquence que s'il est peu sélectif $(Q \leqslant 1)$.**==
> Ce problème existe aussi pour tout filtre possédant une asymptote $G_{dB} = 20\log\frac{f}{f_c}$ et un pic de résonance aigué.
# Définitions
==**Notion de filtre**== :
De façon générale, un filtre (de gain) est un système dont le module de la fonction de transfert dépend, en régime harmonique, de la fréquence.
Nous élargirons la notion de filtre aux montages qui présentent un module de fonction de transfert constant mais qui introduisent une rotation de phase.

==**Filtres parfaits**== :
Un filtre parfait est un système dont la fonction de transfert permet :
- de transmettre, avec un retard mais sans déformation, les composantes sinusoïdales d'un signal dans certains domaines de fréquences constituant sa bande passante ;
- d'éliminer les composantes sinusoïdales situées dans sa bande coupée, c'est-à-dire à l'extérieur de sa bande passante ([[#^figure1|fig. 1]]).
Limitons-nous au cas d'un retard nul et d'une transmission sans atténuation et sans inversion de signe dans la bande passante. Ces conditions sont vérifiées si :
- le module de la fonction de transfert est 1 (donc de gain nul) dans sa bande passante et 0 dans la bande coupée ;
- le déphasage introduit est nul dans la bande passante.
Ces conditions ne peuvent pas être réalisées en pratique. Cependant, plus l'ordre d'un filtre est grand, plus ses caractéristiques pourront se rapprocher de celles d'un filtre idéal.
Les quatre types de filtres parfaits (fig. 2) sont :
- passe-bas : filtre de bande passante $[0 ; f_H​]$ ([[#^figure2|fig. 2a]]) ;
- passe-haut : filtre de bande passante $[f_B ; +\infty]$ ([[#^figure2|fig. 2b]]) ;
- passe-bande : filtre de bande passante $[f_B​ ; f_H​]$ $(f_H > f_B > 0)$ ([[#^figure2|fig. 2c]]) ;
- coupe-bande : filtre de bande coupée $[f_B​ ; f_H​]$ $(f_H > f_B > 0)$ ([[#^figure2|fig. 2d]]).
# Diagrammes
Exemple de déphaseur d'ordre 1 à A.O.
![[electronique2/attachments-electronique2/figure17.png]]^figure10
# Graphiques
Traitement d'un signal périodique par un filtre idéal
![[electronique2/attachments-electronique2/figure8.png]]^figure1

Définition et représentation fonctionnelle des filtres parfaits
![[electronique2/attachments-electronique2/figure9.png]]^figure2

Courbe de réponse en phase $\phi$ et diagramme asymptotique $\phi_A$ d'un déphaseur d'ordre 1
![[electronique2/attachments-electronique2/figure10.png]]^figure3

![[electronique2/attachments-electronique2/figure11.png]]
a. $f = \frac{f_0}{20}$ : (déphasage nul). Le signal est transmis avec un léger retard sans déformation importante. Un pic d'amplitude 1 V apparaît au niveau des discontinuités du créneau. b. $f = f_0$. Le signal de sortie est fortement déformé. Les discontinuités du signal de sortie sont opposées à celle du signal d'entrée (créneau). c. $f = 20f_0$. (déphasage de $-\pi$). Le signal de sortie est proche du signal d'entrée avec sa composante variable en opposition (composante continue identique) ^figure4

Diagramme de Bode : a. Courbe de réponse en gain G. b. Courbe en phase $\phi$
![[electronique2/attachments-electronique2/figure12.png]]^figure5

![[electronique2/attachments-electronique2/figure13.png]]
a. $f = \frac{f_0}{20}$ : signal hors dans la bande passante. Le signal n'est pas transmis. Il ne reste que des pics d'amplitude voisine de 1 V au niveau des discontinuités du signal créneau. b. $f = f_0$ : signal dans la bande passante. Le signal de sortie est déformé sauf au niveau des discontinuités du créneau, où il ne présente pas de discontinuités. Sa valeur moyenne est nulle. c. $f = 20f_0$ : signal hors de la bande passante. Le signal de sortie est d'amplitude négligeable. ^figure6

![[electronique2/attachments-electronique2/figure14.png]]
a. $f = \frac{f_0}{20}$ : signal hors dans la bande passante. Le signal n'est pas transmis. Il ne reste que des oscillations de faible d'amplitude semblables à celles du régime pseudo-périodique amorti dans le cas du créneau. b. $f = f_0$ : signal dans la bande passante. Le signal de sortie est sinusoïdal de fréquence $f_0$. c. $f = 20f_0$ : signal hors de la bande passante. Le signal de sortie est quasiment nul. ^figure7

Courbes de réponse en gain d'un coupe-bande d'ordre 2 pour différentes valeurs de $\sigma$ ( $< 1$)
![[electronique2/attachments-electronique2/figure15.png]]^figure8

Courbes de réponse en phase d'un coupe-bande d'ordre 2 et leurs diagrammes asymptotiques pour différentes valeurs de $\sigma$ ( $< 1$)
![[electronique2/attachments-electronique2/figure16.png]]^figure9

Courbes de réponse en phase et diagrammes asymptotiques d'un déphaseur d'ordre 2 $(\sigma < 1)$
![[electronique2/attachments-electronique2/figure18.png]]^figure11

Domaine intégrateur du filtre passe-bas
![[electronique2/attachments-electronique2/figure19.png]]^figure12a

Le domaine intégrateur du filtre passe-bande ($Q = 0,1$, $f_B = 0,1f_m$ et $f_H = 10f_m$) correspond à $f_0 > 10f_H$ (l'ensemble des harmoniques du signal étant de fréquence supérieure à $f_0$)
![[electronique2/attachments-electronique2/figure20.png]]^figure12b

Domaine dérivateur du filtre passe-haut
![[electronique2/attachments-electronique2/figure21.png]]^figure13a

Domaine dérivateur du filtre passe-bande ($Q = 0,1$, $f_B = 0,1f_m$ et $f_H = 10f_m$) correspond à $nf_0 < \frac{f_B}{10}$ avec $nf_0$ harmonique d'amplitude "encore" importante du signal
![[electronique2/attachments-electronique2/figure22.png]]^figure13b

Réponse d'un filtre passe-bande d'ordre 2 à un signal triangulaire de fréquence 50 Hz et d'amplitude 1 V (fréquence de résonance $f_0 = 1 kHz$). a. Pour un facteur de qualité $Q = 0,5$. b. Pour un facteur de qualité $Q = 10$
![[electronique2/attachments-electronique2/figure23.png]]^figure14

Réponse fréquentielle du filtre : analyse des harmoniques. $Q = 0,5$. Les harmoniques d'amplitude importante du signal de fréquence 50 Hz sont dérivés
![[electronique2/attachments-electronique2/figure24.png]]^figure15a

$Q = 10$. Les harmoniques de rang voisin de 20 du signal de fréquence 50 Hz ne sont pas suffisamment atténués
![[electronique2/attachments-electronique2/figure25.png]]^figure15b
# Expériences
> [!warning]
> La plupart des exemples de travaux pratiques sur les filtres de 1er et 2ème ordre se trouvent dans les chapitres [[08-Fonctions de transfert des réseaux linéaires|8]], [[09-Filtres du deuxième ordre|9]] et [[12-Analyse harmonique|12]]. On ajoute un TP sur le déphaseur à consulter dans ce [lien](http://psi2.nantes.free.fr/TP/ENONCES-ET-CORRIGES-TP/TP-ELECTRONIQUE/ENONCE-TP-ELECTRONIQUE/TP-4-ENONCE.pdf).
# Autres notes