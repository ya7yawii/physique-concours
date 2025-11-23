---
titre: "[[02-Étude fréquentielle des systèmes linéaires]]"
tags:
aliases:
crée: 23-11-2025, 14:22
---
# Formules
> [!note] Régime harmonique forcé
> - Condition d'apparition d'un régime harmonique forcé : ==**Un système linéaire stable soumis à une excitation sinusoïdale de pulsation $\omega$ admet une réponse sinusoïdale de même pulsation, dite réponse forcée. C'est la réponse effectivement observable après l'amortissement du régime libre.**==
> - Propriété des signaux sinusoïdaux : À une excitation sinusoïdale correspond, pour un système linéaire stable, une réponse forcée sinusoïdale. Une proposition logiquement équivalente est donc : ==**Si la réponse forcée à une excitation sinusoïdale n’est pas sinusoïdale, alors le système n’est pas linéaire. Nous disposons ainsi d’un critère pour tester la linéarité d’un système.**==
> Soumettons un système à une excitation sinusoïdale $e(t)=e_m\cos(\omega t)$ :
> 	- si le système est linéaire, la réponse permanente est sinusoïdale : $s(t)=s_m\cos⁡(\omega t+\phi_s)$ ;
> 	- si le système n’est pas linéaire, la réponse permanente est périodique sans être sinusoïdale. Le spectre de fréquence du signal s’est enrichi : il comportera plusieurs fréquences (sans que celles-ci incluent nécessairement $f = \frac{\omega}{2\pi}$​) ; en effet tout signal périodique est décomposable en série de Fourier : $\displaystyle s(t) = C_0 + \sum_{k}C_k\cos⁡(k\omega t+\phi_k)$.
> 	La présence de la composante $C_0$​ révèle un effet de ==**redressement partiel**== : le signal $s(t)$ n’est pas, comme $e(t)$, à valeur moyenne nulle ; la présence des harmoniques $C_k$​, d’ordre $k > 1$, révèle un effet de ==**distorsion harmonique**== ; celle-ci se chiffre par le taux de distorsion harmonique : $D_h = \frac{\sqrt{\displaystyle\sum_{k > 1}C_k^2}}{C_1}$. Plus le taux de distorsion harmonique $D_h$ est élevé, plus le caractère non linéaire du système et accentué. Évidemment pour un système linéaire, $D_h = 0$.

> [!note] Caractéristiques des fonctions de transfert harmoniques
> Pour réviser les notions de module et argument d'une fonction de transfert et le diagramme de Bode, on pourra se reporter à l'ouvrage H-Prépa, Électronique-Électrocinétique, 1re année, [[08-Fonctions de transfert des réseaux linéaires|chapitre 8]].
# Définitions
==**Notion de filtre**== :
De façon générale, un filtre (de gain) est un système dont le module de la fonction de transfert dépend, en régime harmonique, de la fréquence.
Nous élargirons la notion de filtre aux montages qui présentent un module de fonction de transfert constant mais qui introduisent une rotation de phase.

==**Filtres parfaits**== :
Un filtre parfait est un système dont la fonction de transfert permet :
- de transmettre, avec un retard mais sans déformation, les composantes sinusoïdales d’un signal dans certains domaines de fréquences constituant sa bande passante ; • d’éliminer les composantes sinusoïdales situées dans sa bande coupée, c’est-à-dire à l’extérieur de sa bande passante (doc. 4).

Limitons-nous au cas d’un retard nul et d’une transmission sans atténuation et sans inversion de signe dans la bande passante. Ces conditions sont vérifiées si : • le module de la fonction de transfert est 1 (donc de gain nul) dans sa bande passante et 0 dans la bande coupée ; • le déphasage introduit est nul dans la bande passante.

Ces conditions ne peuvent pas être réalisées en pratique. Cependant, plus l’ordre d’un filtre est grand, plus ses caractéristiques pourront se rapprocher de celles d’un filtre idéal.

Les quatre types de filtres parfaits (doc. 5) sont : • passe-bas : filtre de bande passante [0 ; fHfH​] (doc. 5a) ; • passe-haut : filtre de bande passante [fBfB​ ; +∞+∞] (doc. 5b) ; • passe-bande : filtre de bande passante [fBfB​ ; fHfH​] (fH>fB>0fH​>fB​>0) (doc. 5c) ; • coupe-bande : filtre de bande coupée [fBfB​ ; fHfH​] (fH>fB>0fH​>fB​>0) (doc. 5d)
# Diagrammes

# Graphiques

# Expériences

# Autres notes
