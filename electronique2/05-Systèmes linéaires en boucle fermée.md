---
titre: "[[05-Systèmes linéaires en boucle fermée]]"
tags:
aliases:
crée: 29-11-2025, 10:49
---
# Formules
> [!note] Fonctions de transfert d'un système bouclé : Fonction d'asservissement
> - Fonction de transfert : Considérons le système représenté par le schéma fonctionnel de [[#^figure6|figure 6]]. La fonction de transfert relative à l'entrée principale est : $H(p) = \frac{S(p)}{E(p)} = \frac{G(p)}{1 + G(p)F(p)}$ où $G(p) = \frac{S(p)}{\epsilon(p)}$ correspond à la transmittance de la chaîne d'action et $F(p) = \frac{R(p)}{S(p)}$ à la transmittance de la chaîne de rétroaction.
> La fonction de transfert en boucle ouverte $T(p)$ est le produit des fonctions de transfert de la chaîne d'action $G(p)$ et de la chaîne de rétroaction $F(p)$ : $T(p) = \frac{R(p)}{\epsilon(p)} = G(p)F(p)$.
> Un système est à retour unitaire si $F(p) = 1$. $F(p)$ et $G(p)$ sont alors sans dimension. La fonction de transfert en boucle fermée d'un système à retour unitaire est ([[#^figure7|fig. 7]]) : $H(p) = \frac{S(p)}{E(p)} = \frac{G(p)}{1 + G(p)}$.
> - Cas d’une chaîne directe à grand gain : Dans la bande de pulsations (donc de fréquences) pour laquelle la fonction de transfert en boucle ouverte $T(j\omega)$ d’un système bouclé satisfait à l'inégalité  $|T(j\omega)| \gg 1$, nous avons : $\underline{H}(j\omega) = \frac{\underline{S}(j\omega)}{\underline{E}(j\omega)} = \frac{\underline{G}(j\omega)}{1 + \underline{G}(j\omega)\underline{F}(j\omega)} \approx \frac{1}{\underline{F}(j\omega)}$.
> Le système bouclé se comporte alors comme un système en chaîne ouverte dont la fonction de transfert ne dépend que des caractéristiques de sa chaîne de rétroaction.
> Ces dernières peuvent être fixées avec précision, ce qui n’est pas le cas des caractéristiques de la chaîne d’action qui dépendent généralement du point de fonctionnement, de la température, de la fréquence, etc.
> Les défauts de la chaîne d’action (décalages, dérives des composants, etc.) n’affectent plus de comportement du système bouclé.
> Cette propriété remarquable, qui conjugue stabilité de fonctionnement et insensibilité aux variabilités, est largement utilisée lors de la réalisation des systèmes asservis.
> - Condition de stabilité : Un système de fonction de transfert $H(p) = \frac{N(p)}{D(p)}$ est stable (cf. [[03-Étude temporelle des systèmes linéaires|chapitre 3]]), si :
> 	- le degré du polynôme $N(p)$ est au plus égal à celui du polynôme $D(p)$ ;
> 	- les pôles de $H(p)$, c’est-à-dire les zéros de $D(p)$, sont à partie réelle strictement négative. Pour qu’un système bouclé soit stable il est nécessaire que les zéros de $1 + T(p)$ soient à partie réelle strictement négative.
> - Précision : La précision $\epsilon_s(t)$ d’un système asservi est égale à la différence entre la valeur désirée $s_d(t)$ et la valeur réelle $s(t)$ de la grandeur de sortie : $\epsilon_s(t) = s_d(t) - s(t)$.
> La précision statique est égale la valeur prise par $\epsilon_s(t)$ en régime permanent. Pour préciser cette notion étudions un système où la grandeur d’entrée est égale à la valeur souhaitée de la grandeur de sortie et notons $G_0$ et $F_0$ les valeurs de $G(p)$ et $F(p)$ en régime permanent (soit $p = j\omega = 0$).
> La fonction de transfert en régime statique est : $H_0 = \frac{G_0}{1 + G_0F_0} = \frac{s}{s_d}$.
> La précision statique est donc : $\epsilon_{s,\,0} = s_d\frac{1 + G_0(F_0 - 1)}{1 + G_0F_0}$.
> Si, par exemple, la chaîne de rétroaction est unitaire $(F_0 = 1)$, la précision statique est d’autant plus grande que le gain statique de la chaîne d’action est grand.
> La précision dynamique $\epsilon_s(t)$, qui est plus délicate à étudier, dépend de la forme du signal envoyé en entrée.

> [!note] Fonctions de transfert d'un système bouclé : Fonction régulation
> L'entrée principale $e(t)$ étant nulle ([[#^figure8|fig. 8]]), la fonction de transfert relative à la perturbation $e_p(t)$ est : $H_p(p) = \frac{S(p)}{E_p(p)} = \frac{G_2(p)}{1 + G(p)F(p)}$ avec $G(p) = G_1(p)G_2(p)$ la transmittance de la chaîne d'action.
> Pour une fonction $G_2(p)$ imposée, l'influence d'une perturbation de pulsation $\omega$ est donc d'autant plus faible que le module $|T(j\omega)| = |G(j\omega)F(j\omega)|$ de la fonction de transfert en boucle ouverte est grand.

> [!note] Fonctions de transfert d'un système bouclé : Améliorations apportées par la rétroaction
> En boucle ouverte, la valeur de la grandeur de sortie dépend évidemment de la fonction de transfert $G(p)$. Analysons, pour un système en boucle fermée, les influences d’une modification des fonctions de transfert $H(p)$ et $G(p)$.
> Le système bouclé considéré est maintenant celui de [[#^figure9|figure 9]] : $S(p) = \frac{G(p)}{1 + G(p)F(p)}E(p)$ (1).
> - Sensibilité du système vis-a-vis des variations de $G(p)$ : Différentions l’expression (1) avec $E(p)$ et $F(p)$ constantes, nous obtenons : $\frac{\Delta S(p)}{S(p)} = \frac{\Delta G(p)}{G(p)} - \frac{F(p)\Delta G(p)}{1 + G(p)F(p)} = \frac{1}{1 + G(p)F(p)}\frac{\Delta G(p)}{G(p)}$. L'influence des variations de $G(p)$ sur la grandeur commandée $S(p)$ est réduite dans toute la bande de fréquences où $|G(j\omega)F(j\omega)| \gg 1$, c’est-à-dire, généralement, dans une très large bande de fréquences.
> Dans la bande de fréquences où $|T(j\omega)| = |G(j\omega)F(j\omega)| \gg 1$, les variations de $G(p)$ sont sans effet sur la grandeur commandée $S(p)$.
> Dans ce cas particulier, la courbe de réponse du système ne dépend que des éléments de la chaîne de rétroaction. Il est possible, par exemple, de remplacer l’élément amplificateur par un autre (de caractéristiques voisines) sans qu’il y ait de modifications perceptibles de la courbe de réponse.
> Cette propriété est très appréciée dans la pratique (construction en grande série et maintenance de systèmes à caractéristiques définies, etc.).
> - Sensibilité du système vis-à-vis des variations de $E(p)$ : Différentions l’expression (1) avec $E(p)$ et $G(p)$ constantes. Il vient : $\frac{\Delta S(p)}{S(p)} = -\frac{G(p)\Delta F(p)}{1 + G(p)F(p)} = -\frac{G(p)F(p)}{1 + G(p)F(p)}\frac{\Delta F(p)}{F(p)}$. La grandeur commandée $S(p)$ est très sensible aux variations de $F(p)$, et dans la bande de fréquences où $|T(j\omega)| \gg 1$, nous avons : $\frac{\Delta S(p)}{S(p)} = -\frac{\Delta F(p)}{F(p)}$.
> - Conclusion : ==**La grandeur de sortie d’un systéme bouclé est généralement peu sensible aux variations de la transmittance de chaîne d’action. En revanche, elle est très sensible aux variations de la transmittance de la chaîne de rétroaction.**==
> La chaîne d’action est une chaîne de puissance dont le rôle est de transmettre de la puissance, tandis que la chaîne de rétroaction est une chaîne de précision dont le rôle est de contrôler ce transfert de puissance.

> [!note] Circuits électroniques à rétroaction négative : Structure et nomenclature
> Pour les circuits électriques, la soustraction est opérée par une simple application des lois de Kirchhoff. La transcription du schéma fonctionnel unifilaire et du schéma bifilaire dépend de la nature des grandeurs d’entrée et de sortie de la chaîne d'action et de la chaîne de rétroaction.
> - Grandeurs d’entrée : ==**En entrée, l’association en série des chaînes d’action et de rétroaction réalise une soustraction de tension et l'association en parallèle une soustraction de courant.**==
> Lors d’une association en série, la grandeur d’entrée $\epsilon(t)$ de la chaîne d’action et celle de sortie $r(t)$ de la chaîne de rétroaction sont des **tensions** ([[#^figure10|fig. 10]]) : $\epsilon(t) = u_{\epsilon}(t)$ et $r(t) = u_{r}(t)$.
> En revanche, lors d’une association en parallèle, la grandeur d’entrée $\epsilon(t)$ de la chaîne d’action et celle de sortie $r(t)$ de la chaîne de rétroaction sont alors des courants ([[#^figure11|fig. 11]]) : $\epsilon(t) = i_{\epsilon}(t)$ et $r(t) = i_{r}(t)$.
> ==**La grandeur d’entrée est la grandeur qui est modifiée par l’association, en entrée, des quadripôles d’action et de rétroaction.**==
> - Grandeurs de sortie : ==**En sortie, le prélèvement d'une tension se fait en parallèle et celui d'un courant se fait en série.**==
> Lorsqu'en sortie les chaînes d'action et de rétroaction sont associées en parallèle ([[#^figure12|fig. 12]]), la grandeur de sortie est la tension $s(t) = u_s(t)$ et lorsqu'elles sont associées en série ([[#^figure13|fig. 13]]), la grandeur de sortie est le courant : $s(t) = i_s(t)$.
> ==**La grandeur de sortie est la grandeur qui est commune, en sortie, aux deux quadripôles d'action et de rétroaction.**==
> - Nomenclatures : Entre deux chaînes quadripolaires, quatre types d’association sont possibles ([[#^figure14|fig. 14]]). A chacune de ces associations correspond un type de circuit à rétroaction qu’il convient de nommer. Parmi les nomenclatures utilisées ([[#^figure15|fig. 15]]), nous ne retiendrons que les deux suivantes :
> 	- la nomenclature indiquant le type d’association en entrée et en sortie ;
> 	- la nomenclature indiquant la nature de la rétroaction, c’est-à-dire la grandeur $s(t)$ prélevée en sortie et la grandeur $e(t)$ réinjectée en entrée.

> [!note] Effets d'une rétroaction négative idéale
> - Définition : Une rétroaction est modélisée par un convertisseur qui transforme la grandeur de sortie $S(p)$ en grandeur réinjectée $R(p)$. Ce convertisseur est idéal :
> 	- s'il ne perturbe pas la grandeur de sortie $S(p)$ ;
> 	- si $R(p) = \alpha S(p)$, avec $\alpha$ constante indépendante des conditions d'utilisation.
> - Modification de l'impédance d'entrée : Nous étudions le cas d'une association série en entrée. Le circuit bouclé peut être modélisé comme indiqué sur la [[#^figure16|figure 16]]. La transmittance de la chaîne d'action est $G(p) = \frac{S(p)}{U_{\epsilon}(p)}$ et celle de la chaîne de rétroaction est $F(p) = \frac{U_r(p)}{S(p)} = \alpha$.
> L'association en série des chaînes en entrée nous permet d'écrire : $U_e(p) = U_{\epsilon}(p) + U_r(p) = U_{\epsilon}(p)[1 + F(p)G(p)]$, soit encore en divisant par $I_e(p)$, courant d'entrée commun aux deux chaînes : $Z_{e}^{'}(p) = Z_{e}(p)[1 + F(p)G(p)]$, où $Z_{e}^{'}(p)$ et $Z_{e}(p)$ sont respectivement l'impédance du circuit asservi et celle de la chaîne d'action.
> ==**Dans la bande de fréquences où $[1 + \underline{T}(j\omega)| = |1 + \underline{F}(j\omega)\underline{G}(j\omega)| > 1$, l'association en série, en entrée, des chaînes d’action et de rétroaction augmente l’impédance d’entrée : l’impédance d’entrée du circuit asservi est supérieure à celle de la chaîne d’action.**==
> Une étude similaire montre que :
> ==**Dans la bande de fréquences où $[1 + T(j\omega)| = |1 + F(j\omega)G(j\omega)| > 1$, l'association en parallèle, en entrée, des chaînes d’action et de rétroaction diminue l’impédance d’entrée ; l’impédance d’entrée du circuit asservi est inférieure à celle de la chaîne d'action.**==
> - Modification de l'impédance de sortie : Nous étudions le cas d'une association parallèle en sortie. Le circuit bouclé est alors modélisé comme indiqué sur la [[#^figure17|figure 17a]]. La transmittance de la chaîne d'action est $G(p) = \frac{U_s(p)}{\epsilon(p)} = \frac{\mu(p)}{Y_s(p) + Y_u(p)}$ et celle de la chaîne de rétroaction est $F(p) = \frac{R(p)}{U_s(p)} = \alpha$.
> Pour calculer l'impédance de sortie, supprimons le signal d'entrée $(E(p) = 0)$ et appliquons, en sortie, la tension $U_s(p)$ après avoir débranché la charge ([[#^figure17|fig. 17b]]).
> Le comparateur délivre alors le signal $\epsilon(p) = -R(p) = -\alpha U_s(p)$ et la chaîne d'action le signal : $I_s(p) = Y_s(p)U_s(p) - \mu(p)\epsilon(p) = U_s(p)[Y_s(p) + \alpha\mu(p)]$. En divisant par la tension de sortie $U_s(p)$, il vient : $Y_{s}^{'}(p) = Y_{s}(p)\left[1 + \frac{\alpha\mu(p)}{Y_{s}(p)}\right] = Y_{s}(p)[1 + F(p)G(p)_{Y_u = 0}]$, où $Y_{s}^{'}(p)$ est l'admittance de sortie du circuit asservi.
> ==**Dans la bande de fréquence où : $[1 + \underline{T}(j\omega)| = |1 + \underline{F}(j\omega)\underline{G}(j\omega)_{Y_u = 0}| > 1$, l'association en parallèle, en sortie, des chaînes d'action et de rétroaction diminue l'impédance de sortie.**==
> Une étude similaire montre que :
> ==**Dans la bande de fréquence où : $[1 + \underline{T}(j\omega)| = |1 + \underline{F}(j\omega)\underline{G}(j\omega)_{Z_u = 0}| > 1$, l'association en série, en sortie, des chaînes d'action et de rétroaction augmente l'impédance de sortie.**==

> [!note] Effets d'une rétroaction négative idéale : Élargissement de la bande passante
> Considérons le système en boucle fermée de [[#^figure9|figure 9]] où la transmittance de la chaîne de retour $F(p) = \frac{R(p)}{\epsilon(p)}$ est constante et réelle. Supposons que la transmittance de la chaîne directe soit d’ordre 1 : $G(p) = \frac{S(p)}{\epsilon(p)} = \frac{G_0}{1 + \tau_0p}$ et calculons celle de la chaîne en boucle fermée $H(p) = \frac{S(p)}{E(p)}$.
> L'application de la relation fondamentale des systèmes bouclés donne : $H(p) = \frac{G(p)}{1 + FG(p)} = \frac{G_0}{1 + FG(p) + \tau_0p}$, soit encore : $H(p) = \frac{H_0}{1 + \tau p}$ avec $H_0 = \frac{G_0}{1 + FG_0}$ et $\tau = \frac{\tau_0}{1 + FG_0}$.
> Les diagrammes asymptotiques des courbes de réponse en gain de la chaîne directe et de la chaîne en boucle fermée sont donnés sur la [[#^figure18|figure 18]].
> La chaîne bouclée possède :
> - une transmittance $H_0$, en bande passante, plus faible que celle $G_0$ de la chaîne directe, puisqu’elle est divisée par $[1 + FG_0]$ ;
> - une bande passante $\left[0\, ; \omega_H = \frac{1}{\tau} = \frac{1 + FG_0}{\tau_0}\right]$ plus large que celle de la chaîne d’action $\left[0\, ; \omega_G = \frac{1}{\tau_0}\right]$ puisqu'elle est multipliée par $[1 + FG_0]$.
> 
> Cependant, le facteur de mérite du système, à savoir le produit $G_0\omega_G = H_0\omega_H$ de sa transmittance en bande passante par la largeur de sa bande passante, est conservé.
> Ce résultat est très général en électronique.

> [!note] Effets d'une rétroaction négative idéale : Conclusion
> Un quadripôle est idéal vis-a-vis de son entrée s’il ne perturbe pas le système en amont, ce qui équivaut à une puissance nulle en entrée.
> - Si la grandeur d’entrée est une tension, le courant d’entrée doit être nul, ce qui nécessite une impédance d’entrée infinie.
> - Si la grandeur d’entrée est un courant, la tension d’entrée doit être nulle, ce qui nécessite une impédance d’entrée nulle.
> 
> Pour ce qui est de la sortie, un quadripôle est idéal si sa grandeur de sortie est indépendante de la charge.
> - Si la grandeur de sortie est une tension, l’impédance de sortie doit être nulle.
> - Si la grandeur de sortie est un courant, l’impédance de sortie doit être infinie.
> 
> L’étude précédente nous montre donc qu’une rétroaction idéale peut améliorer les caractéristiques d’entrée et de sortie du système bouclé.

> [!note] Oscillateurs quasi sinusoïdaux : Principe d'un oscillateur à réaction
> Illustrons la notion d’oscillateur à réaction (ou à rétroaction) par un exemple connu. Lorsqu’un microphone est placé au voisinage d’une enceinte acoustique, un sifflement est émis. C’est l’effet de Larsen ([[#^figure19|fig. 19]]). Analysons ce phénomène. L’enceinte émet un sifflement, qui est filtré, c’est-à-dire atténué et déformé, lors de sa propagation dans l'air et lors de sa conversion en tension par le microphone. Le signal délivré par ce dernier est amplifié, puis appliqué à nouveau à l’enceinte. Le sifflement est ainsi entretenu et la chaîne acoustique fonctionne en oscillateur à réaction.
> Les oscillateurs à réaction sont utilisés dans de très nombreux domaines de la physique : lasers, magnétrons des fours à micro-ondes, oscillateurs électriques, etc.
> - Structure d’un oscillateur à réaction : Le principe d’un oscillateur à réaction est donné sur la [[#^figure20|figure 20]] et son schéma fonctionnel sur la [[#^figure21|figure 21]]. Un oscillateur à réaction s’analyse en :
> 	- une chaîne d’action (ou directe) de transmittance $G(p)$. C’est une chaîne de puissance constituée d’amplificateurs ;
> 	- une chaîne de réaction (de rétroaction ou de retour) de transmittance $F(p)$. C’est une chaîne de précision réalisée avec un filtre.
> 	
> 	Dans un oscillateur à réaction, le soustracteur du schéma fonctionnel effectue une comparaison à zéro. Il est souvent avantageux d’attribuer à l'association chaîne de réaction-soustracteur, une transmittance $F'(p) = -F(p)$ comme indiqué sur la [[#^figure22|figure 22]].

> [!note] Oscillateurs quasi sinusoïdaux : Conditions théoriques d'oscillation sinusoïdales ou harmoniques
> A quelles conditions le circuit de [[#^figure22|figure 22]] peut-il être le siège d'oscillations sinusoïdales ?
> Supposons, qu'à l'instant t, le signal $s(t)$ délivré par la chaîne d'action soit sinusoïdal. Utilisons la notation complexe : $\underline{s}(t) = s_m e^{j\omega_0 t}$. Ce signal est filtré par la chaîne de réaction qui délivre : $\underline{r}^{'}(t) = \underline{F}^{'}(j\omega_0)\underline{s}(t) = |\underline{F}^{'}(j\omega_0)|s_m e^{j(\omega_0 t + \phi_r)}$, où $\phi_r = \arg[\underline{F}^{'}(j\omega_0)]$ est le déphasage apporté par la chaîne de retour.
> Le signal $\underline{r}^{'}(t)$ est ensuite amplifié par la chaîne d'action qui fournit le signal $\underline{s}^{'}(t)$ : $\underline{s}^{'}(t) = \underline{G}(j\omega_0)\underline{r}^{'}(t) = |\underline{G}(j\omega_0)||\underline{F}^{'}(j\omega_0)|s_m e^{j(\omega_0 t + \phi_r + \phi_a)}$, avec $\phi_a = \arg[\underline{G}(j\omega_0)]$.
> L'entretien des oscillations, qui se traduit par $\underline{s}^{'}(t) = \underline{s}(t)$, impose les deux conditions suivantes :
> - $|\underline{G}(j\omega_0)||\underline{F}^{'}(j\omega_0)| = 1$ ;
> - $\arg[\underline{G}(j\omega_0)] + \arg[\underline{F}^{'}(j\omega_0)] = n2\pi$ avec n entier.
> 
> De façon plus concise, avec les notations de [[#^figure22|figure 22]], ces conditions s’écrivent $\underline{G}(j\omega_0)\underline{F}^{'}(j\omega_0) = 1$ et avec celles de [[#^figure21|figure 21]] : $-\underline{G}(j\omega_0)\underline{F}(j\omega_0) = 1$.
> L'entretien des oscillations sinusoïdales à la fréquence $f_0$ exige que la boucle formée par la chaîne d'action, la chaîne de rétroaction et le soustracteur ait, à cette fréquence $f_0$, un gain nul et un déphasage multiple de $2\pi$.
^par1

> [!note] Oscillateurs quasi sinusoïdaux : Conditions d'oscillations
> Les conditions précédentes sont trop strictes pour être réalisables et, en outre, elles n’assurent pas l’apparition du signal.
> Examinons le mécanisme de formation du signal dans un oscillateur à rétroaction. Inéluctablement à cause du bruit, à un instant donné, une microtension éphémère apparaît dans le circuit. Modélisons cet effet sous la forme d’une perturbation $(E(p))$ injectée, à cet instant, dans le circuit étudié supposé sans bruit ([[#^figure23|fig. 23]]).
> Si le système est stable, le régime libre est transitoire et le microsignal disparaît : le régime permanent d’un tel système, en l’absence de commande, est le repos ([[#^figure24|fig. 24a]]).
> Pour qu’un signal non nul, oscillant ou non, existe dans le circuit, le système doit donc être instable et sa fonction de transfert : $H(p) = \frac{S(p)}{E(p)} = \frac{G(p)}{1 + F(p)G(p)} = \frac{G(p)}{1 - F'(p)G(p)}$ doit comporter au moins un pôle à partie réelle positive.
> Le système étant instable, deux situations peuvent se présenter :
> - le système évolue vers un état stable dans son domaine non linéaire. On observe alors une saturation permanente sans oscillation ([[#^figure24|fig. 24b]]) ;
> - le système évolue vers son domaine non linéaire sans état stable. Alors, dans ce cas, le système oscille ([[#^figure24|fig. 24c]]) et la condition précédente est satisfaite.
> 
> Un circuit bouclé fonctionne en oscillateur si :
> - les racines de $F'(p)G(p) = 1$ comportent des pôles à parties réelles positives ;
> - il n’existe pas d’état stable dans le domaine de fonctionnement non linéaire.

> [!note] Oscillateurs quasi sinusoïdaux : Oscillations quasi sinusoïdales
> Considérons un circuit dont la chaîne d'action est un amplificateur de transmittance constante $G(p) = G_0$, et dont la chaîne de retour est un passe-bande : $F'(p) = \frac{A_0}{1 + Q\left(\frac{p}{\omega_0} + \frac{\omega_0}{p}\right)}$.
> Examinons les critères d'oscillation du circuit.
> - Le passe-bande rejette le continu $F'(0) = 0$, donc un état saturé ne peut être stable.
> - La première condition ($F'(p)G(p) = 1$ comporte des pôles à parties réelles positives) implique que l'équation : $\left(\frac{p}{\omega_0}\right)^{2} + \frac{1 - G_0A_0}{Q}\left(\frac{p}{\omega_0}\right) + 1 = 0$ doit avoir ses racines à parties réelles positives. Le signe de la partie réelle des racines étant celui de $G_0A_0 - 1$, la condition examinée s'écrit : $G_0A_0 > 1$.
> - A quelle condition le signal est-il sinusoïdal ?
> En régime linéaire, nous pouvons utiliser la relation fondamentale des systèmes bouclés : $[1 - F'(p)G(p)]S(p) = G(p)E(p)$ qui s'écrit après la disparition de la perturbation $(E(p) = 0)$ : $[1 - F'(p)G(p)]S(p) = 0$.
> Cette dernière relation est équivalente à l'équation différentielle : $\frac{1}{\omega_{0}^{2}}\dfrac{d^{2}s(t)}{dt^{2}} + \frac{1 - G_0A_0}{Q\omega_0}\dfrac{ds(t)}{dt} + s(t) = 0$ dont la solution est de la forme $s(t) = \alpha_1e^{p_1t} + \alpha_2e^{p_2t}$ avec $p_1$ et $p_2$ racines de l'équation caractéristique : $\left(\frac{p}{\omega_0}\right)^{2} + \frac{1 - G_0A_0}{Q}\left(\frac{p}{\omega_0}\right) + 1 = 0$.
> Le signal $s(t)$ sera quasi sinusoïdal si la partie réelle des racines est positive et très proche de zéro. pour qu’ il en soit ainsi, il faut que $Q$ soit élevé et que $G_0A_0$ soit voisin de 1 (par valeur supérieure). Dans ces conditions : $p_1 = p_2 \approx j\omega_0$.
> 
> $G_0$ est l'amplification de la chaîne directe, $A_0$ l’amplification maximale du passe-bande et $Q$ son facteur de qualité alors :
> - la condition d’oscillation est $G_0A_0 > 1$ ;
> - la condition d’oscillation sinusoïdale est $G_0A_0 \approx 1$ avec $Q \gg 1$.
> 
> La fréquence $f_0$ des oscillations est celle de résonance du filtre.
> Remarques :
> - Les conditions théoriques du [[#^par1|paragraphe précédent]] sont vérifiées à la fréquence de résonance du filtre.
> - Ce sont les non-linéarités de la chaîne directe qui limitent l’amplitude du signal de sortie.
 

 




# Définitions
==**Système en boucle fermée**== :
Les systèmes peuvent être classés en deux catégories : les systèmes en boucle ouverte, qui fonctionnent en ignorant les effets de leurs actions, et les systèmes en boucle fermée, qui considèrent ces effets pour corriger leurs comportements de manière a réaliser, aussi fidèlement que possible, les opérations pour lesquelles ils ont été conçus. Les systèmes en boucle fermée sont irremplaçables dans toutes les situations où il est impossible de commander un système à l'aide d’un programme figé préalablement établi. Aussi se trouvent-ils, non seulement dans toutes les branches de l'industrie, mais encore dans tous les domaines du monde vivant. Les êtres vivants utilisent une multitude de boucles de rétroaction pour maintenir aux niveaux requis les flux de matière et d’ énergie. Ils emploient des processus bien plus élaborés où non seulement la rétroaction mais encore la mémorisation, l'apprentissage, l’auto-adaptation et l’intelligence sont en synergie.

==**Fonctionnement en boucle fermée : Principe de la boucle de rétroaction**== :
Très tôt s’est imposée l’idée qu’il fallait qu’un système comporte une boucle de rétroaction pour qu’il puisse prétendre à de bonnes performances dans des conditions d’utilisation variées.
Ces systèmes imitent grossièrement le comportement humain qui peut s’analyser, dans les cas simples, en trois démarches : observation, traitement de l'information recueillie et action.
Sur ce principe, les systèmes en boucle fermée, ou systèmes bouclés, seront construits selon le schéma fonctionnel de [[#^figure1|figure 1]]. L'originalité de ce schéma fonctionnel, par rapport à ceux que nous avons rencontrés jusqu’à présent, tient au bouclage qui permet au système d’examiner les effets de son action.
==**Un système bouclé contient au moins une boucle de rétroaction qui permet au système de considérer les effets de son action et d’adapter en conséquence, sans intervention extérieure, la commande en vue de l'objectif fixé.**==
Le meilleur véhicule de l’information est le signal électrique. Aussi dans la plupart des systèmes bouclés, la partie traitement de l'information est de nature électrique ou électronique sans préjuger de la nature des autres parties du système.

==**Structure générale d'un système linéaire bouclé**== :
==**Éléments constitutifs des systèmes bouclés**== :
Les systèmes en boucle fermée possèdent en commun un certain nombre d’éléments qui sont les capteurs, les actionneurs et les organes de traitement de l'information.
- Les capteurs : Ce sont des organes dont le rôle est de transformer une grandeur physique en une autre. Parmi les capteurs, citons :
	- les potentiomètres qui transforment une position en une tension électrique ;
	- les accéléromètres qui transforment une accélération en un déplacement (ou une tension électrique) ;
	- les thermocouples qui transforment une température en une tension électrique ;
	- les capteurs de vitesse qui transforment une vitesse de rotation en une tension électrique.
- Les actionneurs : Ce sont des organes de puissance qui commandent directement les systèmes à asservir et à réguler. Parmi les actionneurs usuels, citons les servomoteurs, les vérins et les amplificateurs de puissance. Dans ce dernier cas, les systèmes à commander sont de nature électrique ou électronique.
- Les organes de traitement de l'information : Ces organes, qui travaillent à faible ou moyenne puissance, ont pour rôle de traiter les informations fournies par les capteurs. L'un d'entre eux est inhérent à la structure des systèmes bouclés, il s’agit du comparateur, ou soustracteur, qui élabore l'écart (ou l’erreur) $\epsilon(t)$. Cet élément peut être réalisé de plusieurs manières selon la nature du système bouclé : différentiel mécanique, amplificateur différentiel, synchrodétecteur différentiel, circuit soustracteur, etc. Il peut même ne pas être matérialisé mais résulter d’une association convenable des circuits comme cela est le cas en électronique. Le niveau énergétique des informations est généralement faible par rapport à la puissance fournie par le système. Il convient alors de les amplifier. Ainsi, parmi les organes de traitement de l’information, se trouve des préamplificateurs et des amplificateurs. Pour améliorer les performances de certains systèmes bouclés, il est nécessaire d’associer aux amplificateurs des circuits correcteurs dont le rôle est de modifier la structure de l'information.
Le schéma fonctionnel général d'un système bouclé à une entrée $E(p)$ est donné sur la [[#^figure2|figure 2]].
==**Schémas fonctionnels d’un système bouclé linéaire**== :
En l’absence de perturbations ou lorsqu’on ne considère que la fonction asservissement, le schéma fonctionnel d’un système bouclé est représenté sur la [[#^figure3|figure 3]]. C’est son schéma fonctionnel asservissement.
Dans ce schéma fonctionnel, nous distinguons :
- la chaîne directe, ou chaîne d’action, de transmittance $G(p)$. Cette chaîne est une chaîne de puissance, car elle contient les amplificateurs et l’actionneur ;
- la chaîne de rétroaction ou encore chaîne de précision de transmittance $F(p)$, dont le rôle est de fournir une information aussi exacte que possible sur la grandeur de sortie $S(p)$.
Le schéma étudié ne comporte qu’une seule boucle de rétroaction qui permet de comparer l'entrée et la sortie du système. Une telle boucle est dite **boucle de rétroaction principale** pour la distinguer, éventuellement, des autres boucles qui pourraient se trouver à l’intérieur soit de la chaîne d’action, soit de la chaîne de rétroaction.
Lorsque les perturbations ne sont pas négligées, le schéma fonctionnel du système est donné sur la [[#^figure4|figure 4]].
Signalons que la difficulté pour l’établissement d’un tel schéma tient généralement à la détermination du point d’application de la perturbation.
Si l'objet de l’étude est la fonction de régulation (c’est-à-dire l’influence des perturbations sur la grandeur de sortie) d’un système bouclé, alors l'entrée principale est nulle $E(p) = 0$ et le schéma fonctionnel utilisé peut être simplifié ([[#^figure5|fig. 5]]). Nous remarquerons que le signal $\epsilon(p) = -R_p(p)$ a été changé en $\epsilon(p) = +R_p(p)$ et corrélativement l'additionneur, placé au point d’entrée de la perturbation, est devenu un comparateur. Un tel schéma est appelé schéma fonctionnel régulation.
# Diagrammes
Schéma fonctionnel du principe des systèmes en boucle fermée
![[electronique2/attachments-electronique2/figure78.png]]^figure1

Structure générale d'un système bouclé linéaire
![[electronique2/attachments-electronique2/figure81.png]]^figure2

Schéma fonctionnel asservissement d'un système bouclé
![[electronique2/attachments-electronique2/figure82.png]]^figure3

Schéma fonctionnel d'un système bouclé en présence de perturbations
![[electronique2/attachments-electronique2/figure83.png]]^figure4

Schéma fonctionnel régulation d'un système bouclé
![[electronique2/attachments-electronique2/figure84.png]]^figure5

Schéma fonctionnel asservissement du système bouclé étudié
![[electronique2/attachments-electronique2/figure85.png]]^figure6

Système bouclé à retour unitaire
![[electronique2/attachments-electronique2/figure86.png]]^figure7

Schéma fonctionnel régulation d'un système bouclé
![[electronique2/attachments-electronique2/figure89.png]]^figure8

Système en boucle fermée
![[electronique2/attachments-electronique2/figure90.png]]^figure9

En entrée, une association en série réalise une soustraction de tension
![[electronique2/attachments-electronique2/figure91.png]]^figure10

En entrée, une association en parallèle réalise une soustraction de courant
![[electronique2/attachments-electronique2/figure92.png]]^figure11

En sortie, un prélèvement de tension s'effectue en parallèle
![[electronique2/attachments-electronique2/figure93.png]]^figure12

En sortie, un prélèvement de courant s'effectue en série
![[electronique2/attachments-electronique2/figure94.png]]^figure13

Les quatre types d'association : a. association en série-parallèle ; b. association en parallèle-parallèle ; c. association en parallèle-série ; d. association en série-série
![[electronique2/attachments-electronique2/figure95.png]]^figure14

Nomenclatures : A mon avis pour parallèle-parallèle correspond courant-tension et pour série-série correspond tension-courant
![[electronique2/attachments-electronique2/figure96.png]]^figure15

Association en série, en entrée, des chaînes d'action et de rétroaction
![[electronique2/attachments-electronique2/figure97.png]]^figure16

a. Association en parallèle, en sortie, des chaînes d'action et de rétroaction. b. Pour calculer l'impédance de sortie, nous annulons $E(p)$, nous débranchons la charge et nous la remplaçons par un générateur de tension $U_s(p)$
![[electronique2/attachments-electronique2/figure98.png]]^figure17

Effet Larsen
![[electronique2/attachments-electronique2/figure100.png]]^figure19

Structure d'un oscillateur à réaction
![[electronique2/attachments-electronique2/figure101.png]]^figure20

Schéma fonctionnel d'un circuit linéaire bouclé
![[electronique2/attachments-electronique2/figure102.png]]^figure21

L'association de la chaîne de réaction et du soustracteur délivre un signal $R'(p) = -R(p)$
![[electronique2/attachments-electronique2/figure103.png]]^figure22

Microtension de bruit analysée comme une perturbation injectée dans un circuit sans bruit
![[electronique2/attachments-electronique2/figure104.png]]^figure23
# Graphiques
Diagrammes asymptotiques des courbes de réponse en gain de la chaîne en boucle fermée
![[electronique2/attachments-electronique2/figure99.png]]^figure18

Réponse d'un système à une perturbation éphémère : a. système stable ; b. système instable, à état stable dans son domaine non linéaire ; c. système instable, sans état stable dans son domaine non linéaire
![[electronique2/attachments-electronique2/figure105.png]]^figure24
# Expériences

# Autres notes
> [!warning] Un exemple de rétroaction linéaire : Application 1 page 152
> ![[electronique2/attachments-electronique2/figure79.png]]![[electronique2/attachments-electronique2/figure80.png]]

> [!warning] Application 2 page 156
> ![[electronique2/attachments-electronique2/figure87.png]]![[electronique2/attachments-electronique2/figure88.png]]