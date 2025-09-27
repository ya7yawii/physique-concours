---
titre: "[[10-Système de deux points matériels]]"
tags:
  - barycentre
  - fictif
  - Kœnig
crée: 24-09-2025, 11:01
---
# Formules
> [!note] Repérage des positions
> Le barycentre des deux points matériels $M_1$ et $M_2$, de masse $m_1$ et $m_2$, est défini par : $m_1\overrightarrow{GM_1} + m_2\overrightarrow{GM_2} = \overrightarrow{0}$ ([[#^figure1]]).
> Les points matériels $M_1$ et $M_2$ peuvent être décrits par leur position absolue : $\overrightarrow{r_1} = \overrightarrow{OM_1}$ et $\overrightarrow{r_2} = \overrightarrow{OM_2}$ où O est l'origine d'un repère lié au référentiel d'étude.
> Ils peuvent aussi être décrits par la position de leur barycentre et leur position relative : $\displaystyle \overrightarrow{r_G} = \frac{m_1\overrightarrow{r_1} + m_2\overrightarrow{r_2}}{m_1 + m_2}$ et $\overrightarrow{r} = \overrightarrow{r_2} - \overrightarrow{r_1} = \overrightarrow{M_1M_2}$ ;
> leur position barycentrique se déduit de leur position relative par simple homothétie : $\displaystyle \overrightarrow{r_1}^{*} = \frac{-m_2}{m_1 + m_2}\overrightarrow{r}$ et $\displaystyle \overrightarrow{r_2}^{*} = \frac{m_1}{m_1 + m_2}\overrightarrow{r}$.

Quantité de mouvement (ou résultante cinétique) : $\overrightarrow{p} = M\overrightarrow{v_G}$ avec $M = m_1 + m_2$.

Moment cinétique en un point O : $\overrightarrow{L_O} = m_1\overrightarrow{OM_1} \wedge \overrightarrow{v_1} + m_2\overrightarrow{OM_2} \wedge \overrightarrow{v_2} = \overrightarrow{r_1} \wedge \overrightarrow{p_1} + \overrightarrow{r_2} \wedge \overrightarrow{p_2}$

Moment cinétique par rapport à un axe $\Delta = (O, \overrightarrow{e_{\Delta}})$ : $L_{\Delta} = \overrightarrow{L_O} . \overrightarrow{e_{\Delta}}$

Composition du moment cinétique : $\overrightarrow{L_{O'}} = \overrightarrow{L_O} + \overrightarrow{p} \wedge \overrightarrow{OO'}$.

Énergie cinétique : $\mathcal{E}_K = \frac{1}{2}m_1v_{1}^{2} + \frac{1}{2}m_2v_{2}^{2}$.

Champs de vitesse d'entraînement dans le référentiel barycentrique $\mathcal{R}^*$ : $\overrightarrow{v_e}^*(M) = \overrightarrow{v_G}$.

Champs d'accélération d'entraînement dans $\mathcal{R}^*$ : $\overrightarrow{a_e}^*(M) = \overrightarrow{a_G}$.

> [!warning]
> il n'y a pas d'accélération de Coriolis dans le référentiel barycentrique $\mathcal{R}^*$.

Moment cinétique barycentrique : $\overrightarrow{L_O}^* = \overrightarrow{L_{O'}}^* = \overrightarrow{L}^*$, le même en tout point de $\mathcal{R}^*$.

> [!note] Mobile fictif d'un système à deux corps dans $\mathcal{R}^*$
> Le moment cinétique et l'énergie cinétique barycentriques du système de deux points matériels (de masse $m_1$ et $m_2$) s'identifient à ceux qu'aurait le mobile fictif M en mouvement dans le référentiel barycentrique : $\overrightarrow{L}^* = \mu\overrightarrow{r} \wedge \dot{\overrightarrow{r}}$ et $\mathcal{E}_{K}^{*} = \frac{1}{2}\mu\dot{\overrightarrow{r}}^{2}$ avec $\overrightarrow{r} = \overrightarrow{GM}$ et la masse réduite $\mu = \frac{m_1m_2}{m_1 + m_2}$.

> [!note] Théorèmes de Kœnig
> 1. Le moment cinétique du système au point G est égal à son moment cinétique barycentrique : $\overrightarrow{L_G} = \overrightarrow{L}^*$.
> 2. Premier théorème de Kœnig : le moment cinétique en O du système S de masse M est la somme du moment cinétique barycentrique et du moment cinétique en O du point G affecté de toute la masse : $\overrightarrow{L_O} = \overrightarrow{L}^* + \overrightarrow{OG} \wedge M\overrightarrow{v_G}$.
> 3. Second théorème de Kœnig : l'énergie cinétique du système S est la somme de son énergie cinétique barycentrique et de l'énergie cinétique du point G affecté de toute la masse : $\mathcal{E}_K = \mathcal{E}_{K}^{*} + \frac{1}{2}Mv_{G}^{2}$.

Résultante des actions extérieures : $\displaystyle \overrightarrow{R} = \sum_{i} \overrightarrow{F}_{ext \rightarrow M_i} = \overrightarrow{R_{ext}} \quad (\overrightarrow{R_{int}} = \overrightarrow{0})$.
Moment des actions extérieures : $\displaystyle \overrightarrow{\mathcal{M}_O} = \sum_{i} \overrightarrow{OM_i} \wedge \overrightarrow{F}_{ext \rightarrow M_i} = \overrightarrow{\mathcal{M}_{ext \, O}} \quad (\overrightarrow{\mathcal{M}_{int \, O}} = \overrightarrow{0})$.
Loi de composition des moments : $\overrightarrow{\mathcal{M}_{O'}} = \overrightarrow{\mathcal{M}_O} + \overrightarrow{R} \wedge \overrightarrow{OO'}$.

> [!note] Cas des forces de pesanteur
> L'action de la pesanteur sur un système est équivalente à une force égale au poids total et appliquée au barycentre : le poids total est $\overrightarrow{P} = M \overrightarrow{g}$, le moment résultant en O des forces de pesanteur est $\overrightarrow{\mathcal{M}_O} = \overrightarrow{OG} \wedge \overrightarrow{P}$.
> Affirmer que « le poids s'applique en G » est un abus de langage, car le poids est une force répartie.
> Cette propriété n'est vraie que parce que le champ de pesanteur $\overrightarrow{g}$ est uniforme. Il faut bien se garder d'appliquer systématiquement en G toutes les forces réparties.

Théorème de la résultante cinétique (ou quantité de mouvement) : $\dfrac{d\overrightarrow{p}}{dt} = M\dfrac{d\overrightarrow{v_G}}{dt} = \overrightarrow{R_{ext}}$.

Théorème du moment cinétique en un point O fixe : $\dfrac{d\overrightarrow{L_O}}{dt} = \overrightarrow{\mathcal{M}}_{O_{ext}}$.

> [!note] Théorème du moment cinétique barycentrique
> $\dfrac{d\overrightarrow{L}^*}{dt} = \overrightarrow{\mathcal{M}}_{G_{ext}}$, nous pouvons lire ce résultat de deux façons qui sont assez surprenantes :
> - nous pouvons appliquer le théorème du moment cinétique dans le référentiel galiléen $\mathcal{R}$, comme si le point G était fixe... ce qui n'est pourtant pas le cas en général !
> - dans le référentiel barycentrique $\mathcal{R}^*$, le théorème du moment cinétique s'applique au point fixe G, comme si $\mathcal{R}^*$ était galiléen... ce qui n'est pourtant pas le cas en général !

Théorème scalaire du moment cinétique : $\dfrac{d\overrightarrow{L_{\Delta}}}{dt} = \overrightarrow{\mathcal{M}}_{\Delta_{ext}}$.

> [!note] Cas d'un référentiel non galiléen
> Dans un référentiel non galiléen, les résultats précédents sont applicables, à condition de comptabiliser les forces d'inertie agissant sur les points matériels comme des forces extérieures supplémentaires.

> [!note] Lois de conservation
> Si le système de points matériels est isolé, la résultante et le moment des actions extérieures sont nuls.
> Dans ces conditions, la quantité de mouvement totale $\overrightarrow{p} = M\overrightarrow{v_G}$ et le moment cinétique barycentrique $\overrightarrow{L}^*$  sont des constantes du mouvement.
> Le moment cinétique $\overrightarrow{L_O}$ en un point fixe du référentiel galiléen est lui aussi conservé.

> [!note] Puissance des forces intérieures
> La puissance des forces intérieures au système est : $\mathcal{P} = F_{1 \rightarrow 2}\dfrac{dr}{dt}$ en notant $\overrightarrow{M_1M_2} = r\overrightarrow{e_r}$ et $\overrightarrow{F_{1 \rightarrow 2}} = F_{1 \rightarrow 2}\overrightarrow{e_r}$. Nous savons que la résultante et le moment des actions intérieures sont nuls, mais la puissance des forces intérieures est en général non nulle si le système est déformable. En revanche, elle l'est pour un système rigide : $r = cte$.
> La puissance des forces intérieures au système ne dépend pas du référentiel.

> [!note] Théorèmes de la puissance et de l'énergie cinétique
> - Pour le système de points matériels, le théorème de la puissance cinétique s'écrit : $\dfrac{d\mathcal{E}_K}{dt} = \mathcal{P}_{ext} + \mathcal{P}_{int}$. Le travail des forces extérieures dépend, comme l'énergie cinétique, du référentiel. Pour un système rigide, on a $\mathcal{P}_{int} = 0$.
> - Le théorème de l'énergie cinétique s'écrit $\Delta\mathcal{E}_K = \mathcal{T}_{ext} + \mathcal{T}_{int}$ et fait intervenir le travail de toutes les forces entre l'état initial et l'état final du système. Comme la puissance, le travail des forces intérieures est indépendant du référentiel. Il est nul pour un système rigide.

> [!note] Énergie potentielle
> Nous avons discuté au [[07-Force centrale conservative. Mouvement newtonien|chapitre 7]] le caractère conservatif d'une force centrale. De même ici, la force d'interaction entre les points $M_1$ et $M_2$ est conservative lorsque : $\overrightarrow{F_{1 \rightarrow 2}} = F_{1 \rightarrow 2}(r)\overrightarrow{e_r} = -\dfrac{d\mathcal{E}_{P_{int}}(r)}{dr}\overrightarrow{e_r}$.
> L'énergie potentielle totale est $\mathcal{E}_P = \mathcal{E}_{P_{int}} + \mathcal{E}_{P_{ext}}$. Le travail de toutes les forces agissant sur le système s'écrit alors : $\mathcal{T} = -\Delta\mathcal{E}_P + \mathcal{T}_{NC}$ où $\mathcal{T}_{NC}$ désigne le travail des forces non conservatives, tant intérieures qu'extérieures (des forces de frottement visqueux, par exemple).

> [!note] Énergie mécanique
> L'énergie mécanique du système est la somme de son énergie cinétique et de son énergie potentielle : $\mathcal{E}_M = \mathcal{E}_K + \mathcal{E}_P = \mathcal{E}_K + \mathcal{E}_{P_{int}} + \mathcal{E}_{P_{ext}}$.
> Le théorème de l'énergie s'écrit alors : $\Delta\mathcal{E}_M = \mathcal{T}_{NC}$. Pour un système conservatif, l'énergie mécanique est une constante du mouvement. Donc l'équation $\mathcal{E}_M = cte$, appelée intégrale première de l'énergie, peut alors être utilisée pour obtenir l'évolution du système s'il possède un unique degré de liberté.

> [!note] Cas d'un système isolé
> Pour un système isolé, la quantité de mouvement totale se conserve : le barycentre G a un mouvement rectiligne uniforme.
> L'étude du mouvement relatif, en référentiel galiléen, du système à deux points matériels isolé se ramène à l'étude du mouvement du mobile fictif soumis à la force centrale $\overrightarrow{F_{1 \rightarrow 2}}$ : $\mu\dfrac{d^{2}\overrightarrow{r}}{dt^{2}} = F_{1 \rightarrow 2}\overrightarrow{e_r}$.
> Le moment cinétique du mobile fictif, égal au moment cinétique barycentrique $\overrightarrow{L}^* = \mu\overrightarrow{r} \wedge \dot{\overrightarrow{r}}$, est conservé. Alors, le mouvement du mobile fictif est plan, et satisfait la loi des aires.
> La conservation de l'énergie mécanique du système isolé, lorsque la force intérieure est conservative, est traduite par la conservation de l'énergie mécanique du mobile fictif : $\mathcal{E}_{M}^{*} = \frac{1}{2}\mu\dot{\overrightarrow{r}}^{2} + \mathcal{E}_{P_{int}}$, qui est l'énergie mécanique barycentrique du système.
> Les techniques d'étude des mouvements à force centrale sont applicables au mouvement du mobile fictif.
> Rappelons en particulier que le mouvement radial du mobile peut être discuté en utilisant la fonction énergie potentielle effective, car : $\mathcal{E}_{M}^{*} = \frac{1}{2}\mu\dot{r}^{2} + \mathcal{E}_{P_{eff}}(r) \geqslant \mathcal{E}_{P_{eff}}(r)$ avec $\mathcal{E}_{P_{eff}}(r) = \frac{\mu C^{2}}{2r^{2}} + \mathcal{E}_{P_{int}}(r)$ où C est la constante des aires associée au mouvement plan du mobile fictif.
> Dans le cas d'une force newtonienne, par exemple, nous savons que la trajectoire du mobile fictif sera une ellipse si $\mathcal{E}_{M}^{*} < 0$, une parabole pour $\mathcal{E}_{M}^{*} = 0$, et une branche d'hyperbole pour $\mathcal{E}_{M}^{*} > 0$.

> [!note] Intervention d'un champ de force extérieur
> Nous sommes ici dans le cas de l'intervention d'(au moins) un troisième corps qui vient perturber le système à deux corps auquel nous nous étions limités.
> La simplicité de la résolution du problème à deux corps vient du découplage des mouvements d'ensemble (barycentre) et relatif (mobile fictif). Mais le problème se complique dès qu'intervient (au moins) un troisième corps : on ne peut plus découpler les équations du mouvement par un changement de variable adéquat. On peut alors faire appel à des méthodes numériques, ou envisager des solutions approchées lorsque l'influence du troisième corps intervient sous la forme d'une petite perturbation de l'évolution du système binaire.
> Nous prenons comme exemple, l'influence d'un champ de gravitation extérieur uniforme :
> Notons $\overrightarrow{\mathcal{G}}(M_1) = \overrightarrow{\mathcal{G}}(M_2) = \overrightarrow{\mathcal{G}_0}$ le champ uniforme, les équations d'évolution sont ici :
> $$
> \begin{cases}
> m_1\dfrac{d^{2}\overrightarrow{r_1}}{dt^{2}} = \overrightarrow{F}_{ext \rightarrow 1} + \overrightarrow{F}_{2 \rightarrow 1} = m_1\overrightarrow{\mathcal{G}_0} + \overrightarrow{F}_{2 \rightarrow 1}\\
> m_2\dfrac{d^{2}\overrightarrow{r_2}}{dt^{2}} = \overrightarrow{F}_{ext \rightarrow 2} + \overrightarrow{F}_{1 \rightarrow 2} = m_2\overrightarrow{\mathcal{G}_0} + \overrightarrow{F}_{1 \rightarrow 2}
> \end{cases}
> $$
> La somme de ces équations nous donne le mouvement du barycentre : $M\dfrac{d\overrightarrow{v_G}}{dt} = \overrightarrow{R}_{ext} = M\overrightarrow{\mathcal{G}_0}$. Le mouvement du barycentre est donc un mouvement accéléré ($\mathcal{R}^*$ n'est plus galiléen) correspondant à une chute libre dans le champ de gravitation extérieur.
> Faisons maintenant apparaître l'évolution du mobile fictif :
> $$
> \begin{align*}
> \dfrac{d^{2}\overrightarrow{r}}{dt^{2}} &= \frac{\overrightarrow{F}_{ext \rightarrow 2}}{m_2} - \frac{\overrightarrow{F}_{ext \rightarrow 1}}{m_1} + \frac{1}{m}\overrightarrow{F}_{1 \rightarrow 2}\\
> &= \frac{m_2\overrightarrow{\mathcal{G}_0}}{m_2} - \frac{m_1\overrightarrow{\mathcal{G}_0}}{m_1} + \frac{1}{m}\overrightarrow{F}_{1 \rightarrow 2} = \frac{1}{m}\overrightarrow{F}_{1 \rightarrow 2}
> \end{align*}
> $$
> Le champ de gravitation uniforme est donc sans influence sur le mouvement relatif : nous sommes ramenés à l'étude du mouvement du mobile fictif, comme si le système était isolé.
# Définitions
==**Cinématique d'un système constitué de deux points matériels**== :
Décrite en terme de position barycentrique $\overrightarrow{r_G}$ et position relative $\overrightarrow{r}$ la cinématique du système fait apparaître :
- une translation d'ensemble associée au mouvement du point G ;
- une évolution de l'orientation de la position relative $\overrightarrow{r}$ : le système tourbillonne autour de son barycentre ;
- une évolution de la distance $r = \left\Vert\overrightarrow{r}\right\Vert$ : le système peut se dilater (ou se contracter).

==**Référentiel barycentrique (ou référentiel du centre de masse)**== :
$\mathcal{R}$ étant le référentiel d'étude (souvent galiléen (ou approximativement...)), le référentiel barycentrique $\mathcal{R}^*$ est le référentiel en translation à vitesse $\overrightarrow{v_G}$ par rapport à $\mathcal{R}$ dans lequel la résultante cinétique du système est nulle : $\overrightarrow{p}_{/\mathcal{R}^*} = \overrightarrow{p}^* = \overrightarrow{0}$, autrement dit le point G est fixe dans le référentiel barycentrique. Il faut noter que le mouvement de translation de $\mathcal{R}^*$ par rapport à $\mathcal{R}$ n'est pas nécessairement rectiligne uniforme.

==**Système isolé ou pseudo-isolé**== :
Le système de points matériels est isolé si chacun de ses éléments n'est soumis à aucune force extérieure.
C'est un cas théoriquement inaccessible à l'expérience (il est, par exemple, impossible d'éliminer les forces de gravitation). Il est moins irréaliste d'envisager un système pseudo-isolé tel que les forces extérieures s'annulent pour chacun de ses éléments.
# Diagrammes

# Graphiques
Barycentre, positions barycentriques :
![[figure82.png]]^figure1
# Expériences

# Autres notes
> [!warning] Application 3 page 235 : Machine d'Atwood
> Expliquer pourquoi $\dot{z_1} + \dot{z_2} = 0$ à partir de la figure suivante :
> ![[figure83.png]]
> On $d_1 + d_2 + d_0 = l$ avec $d_0$ est la longueur de la partie de fil tangente au poulie et l la longueur totale du fil. Or $z_1 - z_0 = d_1$ et $z_2 - z_0 = d_2$ donc $z_1 + z_2 = d_1 + d_2 + 2z_0$ et enfin $z_1 + z_2 = l - d_0 + 2z_0 = cte$ ce qui répond à notre question.

> [!warning] Application 4 page 236 : Glissades
> Expliquer comment trouver les expressions des $x_{2}^*$, $y_{2}^*$, $x_{2}$ et $y_{2}$ :
> On a $\dot{\theta} = \frac{v_0}{l} \Rightarrow \theta = \frac{v_0}{l}t + \frac{\pi}{2}$ or $x_{2}^* = -\frac{l}{2}\sin\theta$ et $y_{2}^* = -\frac{l}{2}\cos\theta$ alors $x_{2}^* = -\frac{l}{2}\cos\left(\frac{v_0 t}{l}\right)$ et $y_{2}^* = \frac{l}{2}\sin\left(\frac{v_0 t}{l}\right)$.
> Les expressions de $x_{2}$ et $y_{2}$ se déduisent de faite que $x_{2} = x_{2}^* + x_G$ et $y_{2} = y_{2}^* + y_G$.

> [!note] Troisième loi de Képler
> Pour un point matériel de masse $\mu$ évoluant dans le champ de force newtonien : $\overrightarrow{f} = -\frac{\alpha}{r^{2}}\overrightarrow{e_r}$, nous avons la loi de Képler suivante : $\frac{T^{2}}{a^{3}} = \frac{4\pi^{2}\mu}{\alpha}$.

> [!note] mobile fictif
> On appelle mobile fictif (ou mobile équivalent ou mobile réduit) un point matériel qui serait situé au point M tel que $\overrightarrow{GM} = \overrightarrow{M_1M_2} = \overrightarrow{r}$ et dont la masse serait égale à la masse réduite $\mu$.
> ![[figure84.png]]
> La méthode du mobile réduit ramène l'étude du problème à deux corps à celle du problème à un corps. On dit que l'on a procédé à la réduction canonique du problème à deux corps.