---
titre: "[[Théorème du moment cinétique]]"
tags:
  - moment
  - cinétique
  - centrale
crée: 04-09-2025, 10:15
---
# Formules
Moment en un point : $\overrightarrow{\mathcal{M}_O} = \overrightarrow{OM} \wedge \overrightarrow{F}$
> [!note]
> Si la force $\overrightarrow{F}$ appliquée en un point M « passe par le point O », son moment en O est nul.

Moment par rapport à un axe : $\mathcal{M}_\Delta = \overrightarrow{\mathcal{M}_O}\hspace{0.4em}.\hspace{0.4em}\overrightarrow{e}$  avec $\Delta$ un axe passant par O, orienté selon la direction de son vecteur unitaire $\overrightarrow{e}$ ([[#^figure1]]).
> [!note]
> Le produit scalaire a la même valeur pour tout point O de $\Delta$.
> Le moment par rapport à un axe $\Delta$ d’une force « parallèle à » ou « passant par » cet axe est nul. 
> Nous pouvons retenir la règle de calcul :
> - $|\mathcal{M}_\Delta| = Fd$ ; où d la longueur du segment $H_1H_2$ (bras de levier) de la perpendiculaire commune à $\Delta$ et à D ([[#^figure1]]).
> - $\mathcal{M}_\Delta > 0$ si $\overrightarrow{F}$ « fait tourner » M autour de $\Delta$ dans le sens positif ;
> - $\mathcal{M}_\Delta < 0$ dans le cas contraire.
> 
> Cette règle de calcul peut s’appliquer à une force quelconque, en décomposant celle-ci en une force parallèle à $\Delta$ et une force orthogonale à $\Delta$.

Moment cinétique en un point : $\overrightarrow{L_O}(M)_{/\mathcal{R}} = \overrightarrow{OM} \wedge \overrightarrow{p} = m\overrightarrow{OM} \wedge \overrightarrow{v}$.
> [!note]
> D’après cette définition, nous voyons que le moment cinétique au point O est nul si le point matériel M semble se diriger vers O : sa vitesse «passe par O ».
> Si M est en ==**mouvement circulaire**== de centre O, de rayon r et de vitesse angulaire $\omega$, dans un plan dont le vecteur unitaire normal est $\overrightarrow{e_z}$, alors ([[#^figure2]]) : $\overrightarrow{L_O} = mr^{2}\omega\overrightarrow{e_z}$.

> [!note] Moment cinétique par rapport à un axe
> Le moment cinétique par rapport à l’axe $\Delta$, défini par le point O et le vecteur $\overrightarrow{e}$, du point matériel M dans le référentiel $\mathcal{R}$ est la projection du moment cinétique en O sur l’axe $\Delta$ : $\overrightarrow{L_\Delta}(M)_{/\mathcal{R}} = \overrightarrow{e} \hspace{0.4em} . \hspace{0.4em} \overrightarrow{L_O}(M)_{/\mathcal{R}}$.
> Cette grandeur est indépendante du choix du point O, point quelconque de l’axe $\Delta$.
> Le moment cinétique par rapport à l’axe $\Delta$ est nul si la vitesse du point matériel M « passe par l’axe $\Delta$ », ou si elle est parallèle à l’axe $\Delta$.

Théorème du moment cinétique en un point fixe O : $\overrightarrow{\mathcal{M}_O} = \left(\dfrac{d\overrightarrow{L_O}(M)_{/\mathcal{R}_g}}{dt}\right)_{\hspace{-0.7em}/\mathcal{R}_g}$, dans le référentiel galiléen $\mathcal{R}_g$.

Théorème du moment cinétique en en projection sur l’axe fixe $\Delta$ : $\mathcal{M}_\Delta = \left(\dfrac{dL_\Delta(M)_{/\mathcal{R}_g}}{dt}\right)_{\hspace{-0.7em}/\mathcal{R}_g}$, dans le référentiel galiléen $\mathcal{R}_g$.

Loi des aires : $\dfrac{d\mathcal{A}}{dt} = \frac{1}{2}r^{2}\dot{\theta} = \frac{C}{2}$ avec $\dfrac{d\mathcal{A}}{dt}$  appelée vitesse aréolaire, est constante pour un mouvement à force centrale.
> [!note]
> Cette loi vient de faite que La conservation de $\overrightarrow{L_O}$ se traduit par : $r^{2}\dot{\theta} = C$ et que l’aire $d\mathcal{A}$ « balayée par le rayon OM » est équivalente à celle du secteur circulaire de rayon r et d’angle $d\theta$ : $d\mathcal{A} = \frac{1}{2}r^{2}d\theta$ (voir [[#^demo1]]).
# Définitions
==**Force centrale**== :
Soit O un point fixe d'un référentiel galiléen $\mathcal{R}_g$. Le point matériel M est soumis à un champ de force centrale de centre O si, à chaque instant, la force $\overrightarrow{F}$ qui lui est appliquée est colinéaire à $\overrightarrow{OM}$.

==**Conservation du moment cinétique**== :
Pour un mouvement à force centrale, le moment cinétique $\overrightarrow{L_O}$ est conservé. La trajectoire du point matériel est contenue dans le plan contenant O et perpendiculaire à $\overrightarrow{L_O}$.
Si le moment cinétique est nul, la trajectoire est rectiligne, placée sur une droite passant par le point O.
# Diagrammes
Moment par rapport à un axe :
![[figure49.png]]^figure1

Moment cinétique en O pour un mouvement circulaire :
![[figure50.png]]^figure2
# Graphiques
Démonstration géométrique de l'aire du secteur circulaire :
![[figure51.png]]^figure3
# Expériences

# Autres notes
> [!note] Démonstration géométrique de l'aire du secteur circulaire ^demo1
> On évalue l'aire du secteur OMM', qui se confond avec l'aire du triangle OMM' ([[#^figure3]]) et qui est égale à un demi fois la base fois la hauteur.
> $OMM' =dA =\frac{1}{2}.OM.OM'.\sin(\widehat{MOM'})$.
> c'est-à-dire : $dA = \frac{1}{2}r(r + dr)\sin(d\theta)$.
> On peut négliger l'infiniment petit dr devant la quantité finie r, et confondre le sinus avec l'angle infiniment petit $d\theta$. On obtient donc : $dA = \frac{1}{2}r^{2}d\theta$. 