---
titre: "[[07-Force centrale conservative. Mouvement newtonien]]"
tags:
aliases:
crée: 07-09-2025, 17:04
---
# Formules
Champ de forces centrales : $\overrightarrow{F} = F\overrightarrow{e_r}$  ; le support de la force $\overrightarrow{F}$ passe par le point fixe O.
> [!note] Champ de force centrale conservative
> Un champ de force centrale conservative est de la forme $\overrightarrow{F} = F(r)\overrightarrow{e_r}$ avec $F(r) = -\dfrac{\mathcal{E}_P(r)}{dr}$, $\mathcal{E}_P(r)$ désignant l’énergie potentielle (définie à une constante près) associée à ce champ de force.
> Il existe des champs de forces centrales non conservatifs ; c’est le cas de certaines forces de contact.
> La force est attractive lorsqu’elle est dirigée vers O, soit :$F(r) < 0$. L’énergie potentielle est alors une fonction croissante de la distance r au centre de force O.
> Elle est au contraire répulsive si $F(r) > 0$, donc lorsque l’énergie potentielle est une  fonction décroissante de la distance.

Loi de gravitation : $\displaystyle \overrightarrow{F}_{M_1\rightarrow M_2} = -G\frac{m_1m_2}{r^{2}}\overrightarrow{e_{12}}$ avec $\overrightarrow{F}_{M_1\rightarrow M_2}$ force de gravitation qui est attractive, $G = 6,\!672\hspace{0.3em} . 10^{-11} N . m^{2} . kg^{-2}$ est une constante universelle et $\overrightarrow{e_{12}}$  est le vecteur unitaire de l’axe $M_1M_2$ orienté de $M_1$ vers $M_2$.
> [!note]
> Cette loi, dite de gravitation universelle, a été formulée par Newton pour expliquer les orbites planétaires.
> La <mark style="color: red">masse pesante</mark> qui intervient dans l’expression de la force de gravitation est identique à la <mark style="color: red">masse inerte</mark> de la relation fondamentale de la dynamique. Il s’agit là d’un postulat supplémentaire, dont la validité est confirmée par toutes les expériences.

Le champ de gravitation engendré par un astre de masse $M_{astre}$, de centre d’inertie O, en un point M situé à l’extérieur de l’astre est : $\displaystyle \overrightarrow{\mathcal{G}}(M) = -GM_{astre}\frac{\overrightarrow{OM}}{OM^{3}} = -GM_{astre}\frac{\overrightarrow{e_r}}{r^{2}}$.
> [!note]
> Cette expression est exacte dans le cas d’un astre à symétrie sphérique, et constitue une bonne approximation du champ de gravitation si l’astre est quasi sphérique ou bien à distance r suffisamment grande par rapport à la dimension caractéristique R d’un astre peu régulier.

Champ de force centrale newtonien : $\displaystyle\overrightarrow{F} = -\alpha\frac{\overrightarrow{e_r}}{r^{2}}$.
Énergie potentielle associée au champ newtonien : $\mathcal{E}_P(r) = -\frac{\alpha}{r} + cte$.
> [!note]
> Le champ de force newtonien est attractif lorsque la constante d’interaction $\alpha$ est positive, répulsif au contraire.

> [!note] Mouvement à force centrale conservative
> Nous savons que lors d’un mouvement où il est soumis à un champ de force centrale, de centre O fixe, dans un référentiel galiléen, la trajectoire d’un point matériel est en général dans un plan (passant par O et perpendiculaire au moment cinétique constant $\overrightarrow{L_O}$).
> Pour repérer le mouvement du point matériel dans ce plan, il nous suffit de deux coordonnées. La force étant constamment radiale, nous ferons le choix des coordonnées polaires $(r, \theta)$ de centre O ([[#^figure1]]).
> En écrivant la relation fondamentale de la dynamique, en projection sur les deux vecteurs de la base locale, nous obtenons donc :
>$$  
\begin{cases}  
\displaystyle \ddot{r} - r\dot{\theta}^{2} = \frac{F(r)}{m} = -\frac{1}{m}\dfrac{d\mathcal{E}_P(r)}{dr} & \text{équation radiale}\\  
\displaystyle 2\dot{r}\dot{\theta} + r\ddot{\theta} = 0 & \text{équation orthoradiale}
\end{cases}  
>$$ 
> En remarquant que : $\displaystyle 2\dot{r}\dot{\theta} + r\ddot{\theta} = \frac{1}{r}\dfrac{d}{dt}(r^{2}\dot{\theta}$). En utilisant la loi des aires, nous pouvons ramener le système précédent aux équations suivantes :
>$$  
\begin{cases}  
\displaystyle \ddot{r} - \frac{C^{2}}{r^{3}} = \frac{F(r)}{m} = -\frac{1}{m}\dfrac{d\mathcal{E}_P(r)}{dr} \\  
\displaystyle \dot{\theta} = \frac{C}{r^{2}} 
\end{cases}  
>$$
>En multipliant les deux membres de l'équation radiale par $\dot{r}$, ce qui nous donne : $\displaystyle \dfrac{d}{dt}\left(\frac{1}{2}\dot{r}^{2} + \frac{1}{2}\frac{C^{2}}{r^{2}}\right) = \dfrac{d}{dt}\left(-\frac{1}{m}\mathcal{E}_P(r)\right)$ qui s’intègre par rapport au temps en : $\displaystyle \frac{1}{2}m\left(\dot{r}^{2} + \frac{C^{2}}{r^{2}}\right) + \mathcal{E}_P(r) = cte$ qui n’est rien d’autre que la traduction de la conservation de l’énergie mécanique $\mathcal{E}_M$ du mobile donc : $\displaystyle \dot{r} = \pm \sqrt{\mathcal{E}_M - \frac{mC^{2}}{2r^{2}} - \mathcal{E}_P(r)}$.
>Cette expression fait apparaître une équation différentielle d’ordre un, qui peut se prêter assez aisément à un calcul numérique (en utilisant la méthode de résolution d’Euler, par exemple). Ensuite, il suffirait de reporter $r(t)$ dans la seconde équation pour obtenir $\theta(t)$ par intégration par rapport au temps.
 
# Définitions

# Diagrammes

# Graphiques
Coordonnées polaires dans le plan de la trajectoire :
![[figure52.png]]^figure1
# Expériences

# Autres notes
