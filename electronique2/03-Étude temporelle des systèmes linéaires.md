---
titre: "[[03-Étude temporelle des systèmes linéaires]]"
tags:
  - réponse-impulsionnelle
  - réponse-indicielle
  - erreur-statique
  - dépassement
  - temps-de-réponse
  - passe-bas
  - passe-haut
  - ordre-un
  - ordre-deux
crée: 25-11-2025, 14:12
---
# Formules
> [!note] Réponse impulsionnelle et indicielle
> Pour étudier la réponse d'un systéme linéaire, nous envoyons en entrée une excitation $e(t)$ de forme simple et connue (une fonction test) et nous observons la réponse $s(t)$.
> Nous allons étudier le cas de deux fonctions test importantes : l'impulsion et l'échelon.

> [!note] Réponse impulsionnelle d'un systéme linéaire
> La réponse impulsionnelle du système est sa réponse temporelle $s_{imp}(t)$ pour :
> - une entrée impulsion : $e(t) = t_0e_0\delta(t)$ (rappelons que $\delta(t)$$, impulsion unitaire de Dirac, est homogène à l'inverse d'une durée) ;
> - des conditions initiales telles que le système est au repos à la date $t = 0^-$ : $s_{imp}(0^-) = 0$ et toutes les dérivées $\left(\dfrac{d^{n}s}{dt^{n}}\right)_{\!t = 0^-} = 0$.
> 
> L'impulsion unitaire $\delta(t)$ tant nulle pour tout $t$ positif, la sortie $s(t)$ correspond donc au régime libre du système. L'impulsion fixe les valeurs initiales de $s(t)$ et de ses dérivées à $t = 0^{+}$.
> La principale difficulté revient donc à déterminer ces conditions initiales. L'exemple de l'[[#^demo1|application 1]] nous montre que le caractère non borné de l'impulsion (théoriquement infinie pendant une durée infiniment brève) peut rendre délicate cette opération.

> [!note] Réponse impulsionnelle et fonction de transfert
> Si $S_{imp}(p)$ et $E(p)$ sont les transformées de Laplace de $s_{imp}(t)$ et $e(t)$, nous pouvons écrire : $S_{imp}(p) = H(p)E(p) = t_0e_0H(p)$.
> La connaissance de la fonction de transfert $H(p)$ permet donc de déterminer $S_{imp}(p)$ Puis $s_{imp}(t)$.
> Réciproquement :
> La connaissance de la réponse impulsionnelle $s_{imp}(t)$ à l'impulsion $e(t) = t_0e_0\delta(t)$ permet de déterminer sa transformée de Laplace $S_{imp}(p)$ qui est proportionnelle a la fonction de transfert $H(p)$ : $H(p) = \frac{1}{t_0e_0}S_{imp}(p)$.
> En d'autres termes, la réponse impulsionnelle $s_{imp}(t)$ contient toutes les informations sur les interactions entre le système linéaire et l'extérieur.
> Remarques :
> - Nous pouvons envisager le cas où, dans le système d'unité utilisé, le produit $t_0e_0$ a pour valeur 1. Il est donc possible d'énoncer la règle :
> **La fonction de transfert $H(p)$ est égale à la réponse à une impulsion unitaire.**
> Cette formulation, plus simple, est en fait « dangereuse » a l'utilisation en raison de son inhomogénéité.
> - Expérimentalement, la valeur de $v_e$ ne peut être infinie. Si la durée de l'impulsion est très brève, l'amplitude du signal de sortie risque d'être trop faible pour permettre une étude précise. C'est pour cette raison que nous étudierons essentiellement la réponse à un échelon, ou réponse indicielle.

> [!note] Réponse indicielle d'un système linéaire
> La réponse indicielle du système est sa réponse temporelle $s_{ind}(t)$ pour :
> - une entrée échelon : $e(t) = e_0u(t)$ ;
> - des conditions initiales telles que le système est au repos à la date $t = 0^-$ : $s(0^-) = 0$ et toutes les dérivées $\left(\dfrac{d^{n}s}{dt^{n}}\right)_{\!t = 0^-} = 0$.
> 
> Si $S_{ind}(p)$ et $E(p)$ sont les transformées de Laplace de $s_{ind}(t)$ et $e(t)$, nous pouvons écrire : $S_{ind}(p) = H(p)E(p) = e_0\frac{H(p)}{p}$.
> La connaissance de la fonction de transfert $H(p)$ permet de déterminer $S_{ind}(p)$ et de remonter à la réponse indicielle $s_{ind}(t)$ en déterminant l'original de $S(p)$.
> Réciproquement :
> La connaissance de la réponse indicielle $s_{ind}(t)$ à l'échelon $e(t) = e_0u(t)$ permet de déterminer sa transformée de Laplace $S_{ind}(p)$ puis la fonction de transfert $H(p)$ en utilisant la relation : $H(p) = \frac{pS_{ind}(p)}{e_0}$.
> En d'autres termes, la réponse indicielle $s_{ind}(t)$ contient toutes les informations pour déterminer la réponse du système à une excitation quelconque.

> [!note] Relation entre réponse indicielle et réponse impulsionnelle
> Revenons à la définition de l'impulsion comme une limite : $\displaystyle \delta(t) = \lim_{\tau \rightarrow 0}\frac{u(t + \tau) - u(t)}{\tau}$.
> Une entrée impulsion peut donc s'écrire : $\displaystyle e(t) = e_0t_0\delta(t) = t_0\lim_{\tau \rightarrow 0}\frac{e_0u(t + \tau) - e_0u(t)}{\tau}$.
> Connaissant la réponse $s_{ind}(t)$ à l'échelon $e_0u(t)$, on peut appliquer le principe de superposition des réponses : $\displaystyle s_{imp}(t) = t_0\lim_{\tau \rightarrow 0}\frac{s_{ind}(t + \tau) - s_{ind}(t)}{\tau}$.
> $S_{ind}$ étant continue pour $t > 0$ (strictement) on peut écrire : $s_{imp}(t) = t_0\dfrac{ds_{ind}(t)}{dt}$.
> ==**La réponse impulsionnelle est (à constante multiplicative près) égale à la dérivée de la réponse indicielle.**==
> Remarques :
> - Nous pouvons aussi démontrer aisément ce résultat par la transformée de Laplace.
> - Si, dans le système d'unités utilisé, $e_0$ et $t_0$ ont une valeur unité, la relation s'exprime plus simplement :
> la réponse & une impulsion unitaire est égale à la dérivée de la réponse à un échelon unitaire.
> Il faut utiliser avec précaution cette relation simplifiée en raison de son inhomogénéité.
> - Plus généralement, nous pouvons montrer que si $s(t)$ est la réponse à $e(t)$, alors $\dfrac{ds}{dt}$ est la réponse à l'excitation $\dfrac{de}{dt}$ (pour un système initialement au repos).

> [!note] Réponse indicielle d'un passe-bas d'ordre 1
> Un système passe-bas d'ordre 1, initialement au repos, soumis à un signal échelon $e(t) = Eu(t)$ (où $u(t)$ est un échelon unitaire débutant à $t = 0$) a pour réponse : $s(t) = H_0E\left(1 - e^{-\frac{t}{\tau}}\right)$ avec $H_0$ est le [[#^info1|gain statique]] (pour $p = 0$).
> La représentation de la réponse $s(t)$ est donnée en **variables réduites** $x = \frac{t}{\tau}$ et $y(x) = \frac{s(t)}{H_0E}$, ce qui permet de conserver cette courbe pour tous les systèmes passe-bas d'ordre 1 ([[#^figure1|fig. 1]]).
> Il apparaît ainsi que :
> - la réponse $s(t)$ tend vers sa valeur asymptotique $H_0E$ sans jamais la dépasser ;
> - la tangente à l'origine des temps coupe l'asymptote en un point d'abscisse égale à la constante de temps $\tau$.
> Plus la constante de temps $\tau$ est faible, plus le régime permanent $s(t) = H_0E$ sera rapidement atteint. 
> 
> Erreur statique : L'erreur statique $\epsilon_s$, ou erreur de position, d'un système est l'écart $e(t) - s(t)$ en régime permanent, lorsque le signal d'entrée est un signal échelon $e(t) = Eu(t)$ : $\displaystyle \epsilon_s = \lim_{t \rightarrow \infty}[Eu(t) - s(t)]$.
> ==**Pour les systèmes d'ordre 1, l'erreur statique est $\epsilon_s = E(1 - H_0)$.**==
> L'erreur statique des systèmes d'ordre 1 est finie ; elle est nulle lorsque le gain statique $H_0$ est unitaire.
> 
> Temps de réponse : Le régime libre étant exponentiel, il ne s'éteint théoriquement qu'au bout d'un temps infini.
> Néanmoins, dans la pratique, pour chiffrer la rapidité avec laquelle le régime permanent est atteint, on utilise souvent le temps de réponse à 5 %, c'est-a-dire le temps $t_r$ ([[#^figure2|fig. 2]]) à partir duquel l'écart $|s(t) - s(\infty)|$ ne dépasse plus 5 % de réponse finale $s(\infty)$, lorsque le système est soumis à un échelon : $\displaystyle \left|\frac{s(t_r) - s(\infty)}{s(\infty)}\right| = e^{-\frac{t_r}{\tau}} = 0,05$.
> Graphiquement, cela revient à déterminer la date $t_r$, à laquelle la courbe $s(t)$ pénètre dans la bande $[0,95s(\infty) ; 1,05s(\infty)]$ pour ne plus la quitter.
> Comme $e^{-3} \approx 0,05$, il vient $t_r \approx 3\tau$.
> ==**Le temps de réponse $t_r$ à 5 % d'un système de premier ordre est sensiblement égal à trois fois sa constante de temps $\tau$ : $t_r = 3\tau$.**==
> Évidement, plus la constante de temps $\tau$ du système est faible, plus sa réponse est rapide.

> [!note] Réponse indicielle d'un passe-haut d'ordre 1
> Un passe-haut d'ordre 1 a pour fonction de transfert : $\displaystyle H(p) = \frac{S(p)}{E(p)} = \frac{H_0\tau p}{1 + \tau p}$ et pour équation différentielle : $\tau\dfrac{ds(t)}{dt} + s(t) = H_0\tau\dfrac{de(t)}{dt}$.
> Le système étant au repos $(s(0) = 0)$, soumettons-le à une excitation $e(t)$. Sa réponse $s(t)$ est liée à celle $s_1(t)$ du passe-bas d'équation : $\tau\dfrac{ds_1(t)}{dt} + s_1(t) = H_0e(t)$ soumis à la même excitation $e(t)$ avec les mêmes conditions initiales, par la relation : $s(t) = \tau\dfrac{ds_1(t)}{dt}$. A partir de la réponse indicielle du passe-bas, la réponse indicielle du passe-haut s'établit à : $s(t) = H_0Ee^{-\frac{t}{\tau}}$.
> Les [[#^figure3a|figures 3a]] et [[#^figure3b|b]] fournit le principe d'un montage expérimental permettant la comparaison des réponses d'un passe-bas et d'un passe-haut de même constante de temps, soumis à une même excitation, ainsi que les réponses correspondantes.

> [!note] Détermination des caractéristiques d'un passe-bas d'ordre 1
> La méthode est exposée sur un passe-bas, mais elle est facilement transposable au passe-haut.
> Comment reconnaître un passe-bas d'ordre 1 et comment déterminer, par un seul essai, sa fonction de transfert ?
> Le système étant au repos $s(0) = 0$, nous le soumettons a un signal échelon $e(t) = Eu(t)$.
> - Examinons sa réponse $s(t)$. Si sa tangente a l'origine ([[#^figure4|fig. 4]]) est de pente nulle, le système n'est pas d'ordre 1.
> Dans l'hypothèse d'un système d'ordre 1, nous procéderons comme suit :
> - nous relevons la valeur finale $s(\infty)$ et nous traçons, en fonction de $t$, la courbe $y(t) = \log(s(\infty) - s(t))$.
> Si la courbe est une droite ([[#^figure5|fig. 5]]), alors le système est d'ordre 1.
> - La constante de temps $\tau$ est déterminée par la pente de la courbe $y(t)$ : $\left|\dfrac{dy}{dt}\right| = \frac{0,43}{\tau}$ et le gain statique est $H_0 = \frac{s(\infty)}{E}$.
> Les caractéristiques $H_0$ et $\tau$ du système étant connues, sa fonction de transfert s'en déduit.

> [!note] Système linéaires d'ordre 2 : étude d'un passe-bas : Réponse indicielle
> Considérons un passe-bas d'ordre 2 défini par sa fonction de transfert : $\displaystyle H(p) = \frac{S(p)}{E(p)} = \frac{H_0}{1 + 2\sigma p + (\tau\sigma)^{2}}$. Son équation différentielle, en posant $\tau = \frac{1}{\omega_0}$, est : $\dfrac{d^{2}s(t)}{dt^{2}} + 2\sigma\omega_0\dfrac{ds(t)}{dt} + \omega_{0}^{2}s(t) = H_0\omega_{0}^{2}e(t)$, où $\omega_0$ est la pulsation propre, et $2\sigma$ le facteur d'amortissement (la quantité $Q = \frac{1}{2\sigma}$ est le facteur de qualité du système).
> Supposons qu'à l'instant initial le système soit au repos : $s(0) = 0$ et $\left(\!\dfrac{ds(t)}{dt}\!\right)_{\!t = 0} = 0$.
> Appliquons à son entrée un échelon d'amplitude E : $e(t) = Eu(t)$.
> La réponse du système est $s(t) = s_0(t) + s_1(t)$ où $s_0(t)$ est la solution générale de l'équation homogène décrivant la **réponse libre** et $s_1(t)$ une solution particulière de l'équation complète décrivant la **réponse forcée**.
> La réponse forcée étant $s_1(t) = H_0E$, déterminons la réponse libre du système.
> L'équation différentielle a pour équation caractéristique : $r^{2} + 2\sigma\omega_0r + \omega_{0}^{2} = 0$, dont le discriminant réduit est $\Delta' = \omega_0\sqrt{\sigma^{2} - 1}$, ce qui nous conduit à la discussion ci-dessous.
> - Premier cas : $\Delta' > 0$, soit $\sigma > 1$ : En déterminant les racines réels et négatives de l'équation caractéristique ainsi que les constantes d'intégration $A$ et $B$ à l'aide des conditions initiales : ==**la réponse du système est : $s(t) = H_0E\left[1 - e^{-\sigma\omega_0t}\left(ch(\omega t) + \frac{\sigma\omega_0}{\omega}sh(\omega t)\right)\right]$. Le système fonctionne en régime apériodique ([[#^figure6|fig. 6]]).**==
> - Deuxième cas : $\Delta' = 0$, soit $\sigma = 1$ : En déterminant la racine double de l'équation caractéristique ainsi que les constantes d'intégration $A$ et $B$ à l'aide des conditions initiales : ==**la réponse du système s'établit alors à : $s(t) = H_0E\left[1 - e^{-\omega_0t}(1 + \omega_0t)\right]$. Le régime correspondant est le régime critique dont la réalisation est tout à fait théorique. C'est encore un régime apériodique ([[#^figure7|fig. 7]]).**==
> - Troisième cas : $\Delta' < 0$, soit $\sigma < 1$ : En déterminant les racines complexes à parties réelles négatives de l'équation caractéristique ainsi que les constantes d'intégration $A$ et $B$ à l'aide des conditions initiales : ==**la réponse du système est : $s(t) = H_0E\left[1 - e^{-\sigma\omega_0t}\left(\cos(\omega t) + \frac{\sigma\omega_0}{\omega}\sin(\omega t)\right)\right]$. Le système est alors en régime pseudo-périodique ([[#^figure8|fig. 8]]).**==
> Remarque : Pour $\sigma = 0$, la réponse a pour équation : $s(t) = H_0E[1 - \cos(\omega_0t)]$, c'est-à-dire qu'elle est sinusoïdale à régime libre non transitoire et de valeur moyenne non nulle.

> [!note] Système linéaires d'ordre 2 : étude d'un passe-bas :
> - Erreur statique :
> Lorsque nous appliquons un échelon $e(t) = Eu(t)$ à l'entrée d'un système d'ordre 2, l'erreur statique $\epsilon_s$ est : $\displaystyle \epsilon_s = \lim_{t \rightarrow \infty}[Eu(t) - s(t)] = E(1 - H_0)$.
> L'erreur statique d'un système d'ordre 2 est finie et elle est nulle lorsque le gain statique $H_0$ est unitaire.
> Les systèmes passe-bas d'ordre 1 et 2 ont la même erreur statique.
> - Dépassement :
> En régime apériodique $(\sigma > 1)$ et en régime critique $(\sigma = 1)$, la réponse $s(t)$ croît vers sa valeur asymptotique $s(\infty) = H_0E$ sans jamais la dépasser. Il n'en est plus de même en régime pseudo-périodique $(\sigma < 1)$, où $s(t)$ dépasse sa valeur asymptotique.
> Déterminons, en régime pseudo-périodique, les valeurs extremums de $s(t)$ et les dates pour lesquelles ces valeurs sont atteintes. Ainsi, nous cherchons la dérivée de la variable réduite $y(t) = \frac{s(t)}{H_0E}$. Cette dérivée s'annule aux dates $t_k =\frac{k\pi}{\omega}$.
> La date du premier dépassement $t_p$ est appelée **temps de pic** : $t_p =\frac{\pi}{\omega}$.
> ==**Entre deux dépassements consécutifs ($k = 2n - 1$ et $k' = 2n + 1$) s'écoule une durée égale à la pseudo-période $T$ de la réponse : $T = \frac{2\pi}{\omega} = 2t_p$.**==
> Nous pouvons déterminer ainsi la valeur maximale de $s(t)$ atteinte au temps de pic $t_p$ : $s_{max} = s(t_p)$. ==**La valeur relative de ce dépassement maximal est : $\displaystyle D(\sigma) = \frac{s_{max} - H_0E}{H_0E} = e^{-\frac{\sigma\pi}{\sqrt{1 - \sigma^{2}}}}$**==.
> La [[#^figure9|figure 9]] donne la courbe $D(\sigma)$, où il apparaît que $D(\sigma)$ varie entre 1 pour $\sigma = 0$ et 0 pour $\sigma = 1$.
> - Temps de réponse à 5 % :
> Il s'agit de trouver la date $t_r$ à partir de laquelle la réponse $s(t)$ satisfait à la double condition ([[#^figure10|fig. 10]]) : $0,95 \leqslant \frac{s(t)}{H_0E} \leqslant 1,05$. Ce problème ne peut être résolu que par des méthodes numériques. Cette étude montre que ([[#^figure11|fig. 11]]) :
> ==**Le temps de réponse $t_r$ à 5 % est minimal pour $\sigma = 0,69$.**==

> [!note] Détermination des caractéristiques d'un système d'ordre 2
> Nous nous limiterons au cas le plus important, celui des passe-bas à facteur d'amortissement $(\sigma < 1)$.
> La détermination de ses caractéristiques s'effectue comme suit :
> - La valeur finale du premier dépassement $D = \frac{s_{max} - s(\infty)}{s(\infty)}$, nous en déduisons le facteur d'amortissement : $\sigma = \frac{|\ln(D)|}{\sqrt{\pi^{2} + \ln^{2}(D)}}$ ;
> - de la valeur de la pseudo-période $T = \frac{2\pi}{\omega} = \frac{2\pi}{\omega_0\sqrt{1 - \sigma^{2}}}$, qui est l'intervalle de temps qui s'écoule entre des points homologues (deux extrema de même nature, par exemple), nous en déduisons la pulsation propre : $\omega_0 = \frac{2\pi}{T\sqrt{1 - \sigma^{2}}}$.
> 
> Les caractéristiques $H_0$, $\sigma$ et $\omega_0$ du système étant connues, sa fonction de transfert en découle : $H(p) = \frac{H_0}{1 + 2\sigma\frac{p}{\omega_0} + \left(\frac{p}{\omega_0}\right)^{2}}$.
# Définitions

# Diagrammes
Montage expérimental
![[electronique2/attachments-electronique2/figure33.png]]^figure3a
# Graphiques
Réponse indicielle d'un système d'ordre 1 en variables réduites : $x = \frac{t}{\tau}$ et $y = \frac{s(t)}{H_0E}$
![[electronique2/attachments-electronique2/figure31.png]]^figure1

Temps de réponse $t_r$ d'un système
![[electronique2/attachments-electronique2/figure32.png]]^figure2

Réponses d'un passe-bas (sortie x) et d'un passe-haut (sortie y) de même constante de temps et soumis au même signal échelon $(\tau = RC)$
![[electronique2/attachments-electronique2/figure34.png]]^figure3b

Tangente à l'origine d'un passe-bas d'ordre 1 et d'un passe-bas d'ordre 2
![[electronique2/attachments-electronique2/figure35.png]]^figure4

Critère de reconnaissance d'un système d'ordre 1, dont la constante de temps est $\tau = 1 ms$
![[electronique2/attachments-electronique2/figure36.png]]^figure5

Réponse apériodique d'un système d'ordre 2 par différentes valeurs du facteur d'amortissement $(\sigma > 1)$
![[electronique2/attachments-electronique2/figure37.png]]^figure6

Réponse critique d'un système d'ordre 2 $(\sigma = 1)$
![[electronique2/attachments-electronique2/figure38.png]]^figure7

Réponse pseudo-périodique d'un système d'ordre 2 par différentes valeurs du facteur d'amortissement $(\sigma < 1)$
![[electronique2/attachments-electronique2/figure39.png]]^figure8

Variation de $D(\sigma)$ en fonction du facteur d'amortissement
![[electronique2/attachments-electronique2/figure40.png]]^figure9

Pour $t \geqslant t_r$, la réponse $\frac{s(t)}{H_0E}$ ne quitte plus la bande $[0,\!95\, ; 1,\!05]$
![[electronique2/attachments-electronique2/figure41.png]]^figure10

Pour des facteurs d'amortissement $\sigma > 0,\!69$, le temps de réponse $t_r$ est la date d'intersection de $s(t)$ avec $\mathcal{D}_2$
![[electronique2/attachments-electronique2/figure42.png]]^figure11
# Expériences
> [!warning]
> Voici des exemples de travaux pratiques qui abordent le sujet de ce chapitre : le [lien 1](https://fr.scribd.com/document/718822369/TP-1-Reponse-Temporelle-Et-Frequentielle) et les deux autres [lien 2](https://electrosttissemsilt.wordpress.com/wp-content/uploads/2020/05/tp04-asservissement-et-rc3a9gulation-3eme-annc3a9e-elec-2.pdf) et [lien 3](https://fac.umc.edu.dz/fstech/cours/Electronique/ST%202eme%20Ann%C3%A9e/TP%20systeme%20asservis%20L2Automatique/tp3automatique2019.pdf) font partie d'une majorité des TP qui utilisent le logiciel MATLAB au lieu d'une manipulation avec des composants électroniques.
# Autres notes
> [!warning] Application 1 page 89
> ![[electronique2/attachments-electronique2/figure26.png]]![[electronique2/attachments-electronique2/figure27.png]]![[electronique2/attachments-electronique2/figure28.png]]![[electronique2/attachments-electronique2/figure29.png]]![[electronique2/attachments-electronique2/figure30.png]]
^demo1

> [!warning] Gain statique
> En fait pour un passe-bas d'ordre 1, la fonction de transfert est : $\displaystyle H(p) = \frac{s(p)}{e(p)} = \frac{H_0}{1 + \tau p}$.
^info1