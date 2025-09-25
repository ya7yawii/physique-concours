---
titre: "[[10-Système de deux points matériels]]"
tags:
aliases:
crée: 24-09-2025, 11:01
---
# Formules
> [!note] Repérage des positions
> Le barycentre des deux points matériels $M_1$ et $M_2$, de masse $m_1$ et $m_2$, est défini par : $m_1\overrightarrow{GM_1} + m_2\overrightarrow{GM_2} = \overrightarrow{0}$ ([[#^figure1]]).
> Les points matériels $M_1$ et $M_2$ peuvent être décrits par leur position absolue : $\overrightarrow{r_1} = \overrightarrow{OM_1}$ et $\overrightarrow{r_2} = \overrightarrow{OM_2}$ où O est l’origine d’un repère lié au référentiel d’étude.
> Ils peuvent aussi être décrits par la position de leur barycentre et leur position relative : $\displaystyle \overrightarrow{r_G} = \frac{m_1\overrightarrow{r_1} + m_2\overrightarrow{r_2}}{m_1 + m_2}$ et $\overrightarrow{r} = \overrightarrow{r_2} - \overrightarrow{r_1} = \overrightarrow{M_1M_2}$ ;
> leur position barycentrique se déduit de leur position relative par simple homothétie : $\displaystyle \overrightarrow{r_1}^{*} = \frac{-m_2}{m_1 + m_2}\overrightarrow{r}$ et $\displaystyle \overrightarrow{r_2}^{*} = \frac{m_1}{m_1 + m_2}\overrightarrow{r}$.

Quantité de mouvement (ou résultante cinétique) : $\overrightarrow{p} = M\overrightarrow{v_G}$ avec $M = m_1 + m_2$.

Moment cinétique en un point O : $\overrightarrow{L_O} = m_1\overrightarrow{OM_1} \wedge \overrightarrow{v_1} + m_2\overrightarrow{OM_2} \wedge \overrightarrow{v_2} = \overrightarrow{r_1} \wedge \overrightarrow{p_1} + \overrightarrow{r_2} \wedge \overrightarrow{p_2}$

Moment cinétique par rapport à un axe $\Delta = (O, \overrightarrow{e_{\Delta}})$ : $L_{\Delta} = \overrightarrow{L_O} . \overrightarrow{e_{\Delta}}$

Composition du moment cinétique : $\overrightarrow{L_{O'}} = \overrightarrow{L_O} + \overrightarrow{p} \wedge \overrightarrow{OO'}$.

Énergie cinétique : $\mathcal{E}_K = \frac{1}{2}m_1v_{1}^{2} + \frac{1}{2}m_2v_{2}^{2}$.

Champs de vitesse d’entraînement dans le référentiel barycentrique $\mathcal{R}^*$ : $\overrightarrow{v_e}^*(M) = \overrightarrow{v_G}$.

Champs d'accélération d’entraînement dans $\mathcal{R}^*$ : $\overrightarrow{a_e}^*(M) = \overrightarrow{a_G}$.

> [!warning]
> il n’y a pas d’accélération de Coriolis dans le référentiel barycentrique $\mathcal{R}^*$.

Moment cinétique barycentrique : $\overrightarrow{L_O}^* = \overrightarrow{L_{O'}}^* = \overrightarrow{L}^*$, le même en tout point de $\mathcal{R}^*$.

> [!note] Mobile fictif d’un système à deux corps dans $\mathcal{R}^*$
> Le moment cinétique et l’énergie cinétique barycentriques du système de deux points matériels (de masse $m_1$ et $m_2$) s’identifient à ceux qu’aurait le mobile fictif M en mouvement dans le référentiel barycentrique : $\overrightarrow{L}^* = \mu\overrightarrow{r} \wedge \dot{\overrightarrow{r}}$ et $\mathcal{E}_{K}^{*} = \frac{1}{2}\mu\dot{\overrightarrow{r}}^{2}$ avec $\overrightarrow{r} = \overrightarrow{GM}$ et la masse réduite $\mu = \frac{m_1m_2}{m_1 + m_2}$.

> [!note] Théorèmes de Kœnig
> 1. Le moment cinétique du système au point G est égal à son moment cinétique barycentrique : $\overrightarrow{L_G} = \overrightarrow{L}^*$.
> 2. Premier théorème de Kœnig : le moment cinétique en O du système S de masse M est la somme du moment cinétique barycentrique et du moment cinétique en O du point G affecté de toute la masse : $\overrightarrow{L_O} = \overrightarrow{L}^* + \overrightarrow{OG} \wedge M\overrightarrow{v_G}$.
> 3. Second théorème de Kœnig : l’énergie cinétique du système S est la somme de son énergie cinétique barycentrique et de l’énergie cinétique du point G affecté de toute la masse : $\mathcal{E}_K = \mathcal{E}_{K}^{*} + \frac{1}{2}Mv_{G}^{2}$.

Résultante des actions extérieures : $\displaystyle \overrightarrow{R} = \sum_{i} \overrightarrow{F}_{ext \rightarrow M_i} = \overrightarrow{R_{ext}} \quad (\overrightarrow{R_{int}} = \overrightarrow{0})$.
Moment des actions extérieures : $\displaystyle \overrightarrow{\mathcal{M}_O} = \sum_{i} \overrightarrow{OM_i} \wedge \overrightarrow{F}_{ext \rightarrow M_i} = \overrightarrow{\mathcal{M}_{ext \, O}} \quad (\overrightarrow{\mathcal{M}_{int \, O}} = \overrightarrow{0})$.
Loi de composition des moments : $\overrightarrow{\mathcal{M}_{O'}} = \overrightarrow{\mathcal{M}_O} + \overrightarrow{R} \wedge \overrightarrow{OO'}$.

> [!note] Cas des forces de pesanteur
> L’action de la pesanteur sur un système est équivalente à une force égale au poids total et appliquée au barycentre : le poids total est $\overrightarrow{P} = M \overrightarrow{g}$, le moment résultant en O des forces de pesanteur est $\overrightarrow{\mathcal{M}_O} = \overrightarrow{OG} \wedge \overrightarrow{P}$.
> Affirmer que « le poids s’applique en G » est un abus de langage, car le poids est une force répartie.
> Cette propriété n’est vraie que parce que le champ de pesanteur $\overrightarrow{g}$ est uniforme. Il faut bien se garder d’appliquer systématiquement en G toutes les forces réparties.

Théorème de la résultante cinétique (ou quantité de mouvement) : $\dfrac{d\overrightarrow{p}}{dt} = M\dfrac{d\overrightarrow{v_G}}{dt} = \overrightarrow{R_{ext}}$.

Théorème du moment cinétique en un point O fixe : $\dfrac{d\overrightarrow{L_O}}{dt} = \overrightarrow{\mathcal{M}}_{O_{ext}}$.

> [!note] Théorème du moment cinétique barycentrique
> $\dfrac{d\overrightarrow{L}^*}{dt} = \overrightarrow{\mathcal{M}}_{G_{ext}}$, nous pouvons lire ce résultat de deux façons qui sont assez surprenantes :
> - nous pouvons appliquer le théorème du moment cinétique dans le référentiel galiléen $\mathcal{R}$, comme si le point G était fixe... ce qui n’est pourtant pas le cas en général !
> - dans le référentiel barycentrique $\mathcal{R}^*$, le théorème du moment cinétique s’applique au point fixe G, comme si $\mathcal{R}^*$ était galiléen... ce qui n’est pourtant pas le cas en général !

Théorème scalaire du moment cinétique : $\dfrac{d\overrightarrow{L_{\Delta}}}{dt} = \overrightarrow{\mathcal{M}}_{\Delta_{ext}}$.

> [!note] Cas d’un référentiel non galiléen
> Dans un référentiel non galiléen, les résultats précédents sont applicables, à condition de comptabiliser les forces d’inertie agissant sur les points matériels comme des forces extérieures supplémentaires.

> [!note] Lois de conservation
> Si le système de points matériels est isolé, la résultante et le moment des actions extérieures sont nuls.
> Dans ces conditions, la quantité de mouvement totale $\overrightarrow{p} = M\overrightarrow{v_G}$ et le moment cinétique barycentrique $\overrightarrow{L}^*$  sont des constantes du mouvement.
> Le moment cinétique $\overrightarrow{L_O}$ en un point fixe du référentiel galiléen est lui aussi conservé.


# Définitions
==**Cinématique d’un système constitué de deux points matériels**== :
Décrite en terme de position barycentrique $\overrightarrow{r_G}$ et position relative $\overrightarrow{r}$ la cinématique du système fait apparaître :
- une translation d’ensemble associée au mouvement du point G ;
- une évolution de l’orientation de la position relative $\overrightarrow{r}$ : le système tourbillonne autour de son barycentre ;
- une évolution de la distance $r = \left\Vert\overrightarrow{r}\right\Vert$ : le système peut se dilater (ou se contracter).

==**Référentiel barycentrique (ou référentiel du centre de masse)**== :
$\mathcal{R}$ étant le référentiel d’étude (souvent galiléen (ou approximativement...)), le référentiel barycentrique $\mathcal{R}^*$ est le référentiel en translation à vitesse $\overrightarrow{v_G}$ par rapport à $\mathcal{R}$ dans lequel la résultante cinétique du système est nulle : $\overrightarrow{p}_{/\mathcal{R}^*} = \overrightarrow{p}^* = \overrightarrow{0}$, autrement dit le point G est fixe dans le référentiel barycentrique. Il faut noter que le mouvement de translation de $\mathcal{R}^*$ par rapport à $\mathcal{R}$ n’est pas nécessairement rectiligne uniforme.

==**Système isolé ou pseudo-isolé**== :
Le système de points matériels est isolé si chacun de ses éléments n’est soumis à aucune force extérieure.
C’est un cas théoriquement inaccessible à l’expérience (il est, par exemple, impossible d’éliminer les forces de gravitation). Il est moins irréaliste d’envisager un système pseudo-isolé tel que les forces extérieures s’annulent pour chacun de ses éléments.
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

