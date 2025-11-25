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

# Définitions

# Diagrammes

# Graphiques

# Expériences

# Autres notes
> [!warning] Application 1 page 89
> ![[electronique2/attachments-electronique2/figure26.png]]![[electronique2/attachments-electronique2/figure27.png]]![[electronique2/attachments-electronique2/figure28.png]]![[electronique2/attachments-electronique2/figure29.png]]![[electronique2/attachments-electronique2/figure30.png]]
^demo1