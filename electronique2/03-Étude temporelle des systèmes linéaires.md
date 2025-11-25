---
titre: "[[03-Étude temporelle des systèmes linéaires]]"
tags:
aliases:
crée: 25-11-2025, 14:12
---
# Formules
> [!note] Réponse impulsionnelle et indicielle
> Pour étudier la réponse d’un systéme linéaire, nous envoyons en entrée une excitation $e(t)$ de forme simple et connue (une fonction test) et nous observons la réponse $s(t)$.
> Nous allons étudier le cas de deux fonctions test importantes : l'impulsion et l’échelon.

> [!note] Réponse impulsionnelle d’un systéme linéaire
> La réponse impulsionnelle du système est sa réponse temporelle $s_{imp}(t)$ pour :
> - une entrée impulsion : $e(t) = t_0e_0\delta(t)$ (rappelons que $\delta(t)$$, impulsion unitaire de Dirac, est homogène à l’inverse d’une durée) ;
> - des conditions initiales telles que le système est au repos à la date $t = 0^-$ : $s_{imp}(0^-) = 0$ et toutes les dérivées $\left(\dfrac{d^{n}s}{dt^{n}}\right)_{\!t = 0^-} = 0$.
> 
> L'impulsion unitaire $\delta(t)$ tant nulle pour tout $t$ positif, la sortie $s(t)$ correspond donc au régime libre du système. L’impulsion fixe les valeurs initiales de $s(t)$ et de ses dérivées à $t = 0^{+}$.
> La principale difficulté revient donc à déterminer ces conditions initiales. L'exemple de l'[[#^demo1|application 1]] nous montre que le caractère non borné de l'impulsion (théoriquement infinie pendant une durée infiniment brève) peut rendre délicate cette opération.

> [!note] Réponse impulsionnelle et fonction de transfert
> Si $S_{imp}(p)$ et $E(p)$ sont les transformées de Laplace de $s_{imp}(t)$ et $e(t)$, nous pouvons écrire : $S_{imp}(p) = H(p)E(p) = t_0e_0H(p)$.
> La connaissance de la fonction de transfert $H(p)$ permet donc de déterminer $S_{imp}(p)$ Puis $s_{imp}(t)$.
> Réciproquement :
> La connaissance de la réponse impulsionnelle $s_{imp}(t)$ à l'impulsion $e(t) = t_0e_0\delta(t)$ permet de déterminer sa transformée de Laplace $S_{imp}(p)$ qui est proportionnelle a la fonction de transfert $H(p)$ : $H(p) = \frac{1}{t_0e_0}S_{imp}(p)$.
> En d’autres termes, la réponse impulsionnelle $s_{imp}(t)$ contient toutes les informations sur les interactions entre le système linéaire et l’extérieur.
> Remarques :
> - Nous pouvons envisager le cas où, dans le système d'unité utilisé, le produit $t_0e_0$ a pour valeur 1. Il est donc possible d’énoncer la règle :
> **La fonction de transfert $H(p)$ est égale à la réponse à une impulsion unitaire.**
> Cette formulation, plus simple, est en fait « dangereuse » a l'utilisation en raison de son inhomogénéité.
> - Expérimentalement, la valeur de $v_e$ ne peut être infinie. Si la durée de l'impulsion est très brève, l'amplitude du signal de sortie risque d’être trop faible pour permettre une étude précise. C’est pour cette raison que nous étudierons essentiellement la réponse à un échelon, ou réponse indicielle.

> [!note] Réponse indicielle d’un système linéaire
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
> - Si, dans le système d’unités utilisé, $e_0$ et $t_0$ ont une valeur unité, la relation s’exprime plus simplement :
> la réponse & une impulsion unitaire est égale à la dérivée de la réponse à un échelon unitaire.
> Il faut utiliser avec précaution cette relation simplifiée en raison de son inhomogénéité.
> - Plus généralement, nous pouvons montrer que si $s(t)$ est la réponse à $e(t)$, alors $\dfrac{ds}{dt}$ est la réponse à l'excitation $\dfrac{de}{dt}$ (pour un système initialement au repos).

> [!note] Réponse indicielle d'un passe-bas d'ordre 1
> Un système passe-bas d'ordre 1, initialement au repos, soumis à un signal échelon $e(t) = Eu(t)$ (où $u(t)$ est un échelon unitaire débutant à $t = 0$) a pour réponse : $s(t) = H_0E\left(1 - e^{-\frac{t}{\tau}}\right)$ avec $H_0$ est le [[#^info1|gain statique]] (pour $p = 0$).
> La représentation de la réponse $s(t)$ est donnée en **variables réduites** $x = \frac{t}{\tau}$ et $y(x) = \frac{s(t)}{H_0E}$, ce qui permet de conserver cette courbe pour tous les systèmes passe-bas d’ordre 1 ([[#^figure1|fig. 1]]).
> Il apparaît ainsi que :
> - la réponse $s(t)$ tend vers sa valeur asymptotique $H_0E$ sans jamais la dépasser ;
> - la tangente à l’origine des temps coupe l’asymptote en un point d’abscisse égale à la constante de temps $\tau$.
> Plus la constante de temps $\tau$ est faible, plus le régime permanent $s(t) = H_0E$ sera rapidement atteint. 
> 
> Erreur statique : L'erreur statique $\epsilon_s$, ou erreur de position, d'un système est l'écart $e(t) - s(t)$ en régime permanent, lorsque le signal d'entrée est un signal échelon $e(t) = Eu(t)$ : $\displaystyle \epsilon_s = \lim_{t \rightarrow \infty}[Eu(t) - s(t)]$.
> ==**Pour les systèmes d'ordre 1, l'erreur statique est $\epsilon_s = E(1 - H_0)$.**==
> L'erreur statique des systèmes d'ordre 1 est finie ; elle est nulle lorsque le gain statique $H_0$ est unitaire.
> 
> Temps de réponse : Le régime libre étant exponentiel, il ne s’éteint théoriquement qu’au bout d’un temps infini.
> Néanmoins, dans la pratique, pour chiffrer la rapidité avec laquelle le régime permanent est atteint, on utilise souvent le temps de réponse à 5 %, c’est-a-dire le temps $t_r$ ([[#^figure2|fig. 2]]) à partir duquel l’écart $|s(t) - s(\infty)|$ ne dépasse plus 5 % de réponse finale $s(\infty)$, lorsque le système est soumis à un échelon : $\displaystyle \left|\frac{s(t_r) - s(\infty)}{s(\infty)}\right| = e^{-\frac{t_r}{\tau}} = 0,05$.
> Graphiquement, cela revient à déterminer la date $t_r$, à laquelle la courbe $s(t)$ pénètre dans la bande $[0,95s(\infty) ; 1,05s(\infty)]$ pour ne plus la quitter.
> Comme $e^{-3} \approx 0,05$, il vient $t_r \approx 3\tau$.
> ==**Le temps de réponse $t_r$ à 5 % d’un système de premier ordre est sensiblement égal à trois fois sa constante de temps $\tau$ : $t_r = 3\tau$.**==
> Évidement, plus la constante de temps $\tau$ du système est faible, plus sa réponse est rapide.


# Définitions

# Diagrammes

# Graphiques
Réponse indicielle d'un système d'ordre 1 en variables réduites : $x = \frac{t}{\tau}$ et $y = \frac{s(t)}{H_0E}$
![[electronique2/attachments-electronique2/figure31.png]]^figure1

Temps de réponse $t_r$ d'un système
![[electronique2/attachments-electronique2/figure32.png]]^figure2
# Expériences

# Autres notes
> [!warning] Application 1 page 89
> ![[electronique2/attachments-electronique2/figure26.png]]![[electronique2/attachments-electronique2/figure27.png]]![[electronique2/attachments-electronique2/figure28.png]]![[electronique2/attachments-electronique2/figure29.png]]![[electronique2/attachments-electronique2/figure30.png]]
^demo1

> [!warning] Gain statique
> En fait pour un passe-bas d'ordre 1, la fonction de transfert est : $\displaystyle H(p) = \frac{s(p)}{e(p)} = \frac{H_0}{1 + \tau p}$.
^info1