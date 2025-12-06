---
titre: "[[07-Conversion électromagnétique statique. Le transformateur]]"
tags:
  - transformateur
  - circuit-ferromagnétique
  - flux-magnétique
  - Courant-magnétisant
  - primaire
  - secondaire
  - rapport-de-transformation
  - cycle-d-hystérésis
  - pertes-fer
  - pertes-cuivre
  - Adaptation-d-impédance
crée: 03-12-2025, 15:56
---
# Formules

# Définitions
> [!note] Présentation du transformateur : Transport de puissance électrique
> L'énergie électrique est produite dans des centrales qui sont souvent éloignées du lieu d'utilisation. Il est donc nécessaire de transporter cette énergie avec un minimum de pertes.
> L'utilisation de très hautes tensions est nécessaire pour transporter l'énergie avec peu de pertes. Actuellement, le transport d'électricité sur de longues distances se fait sous des tensions comprises entre 200 kV et 400 kV, et l'intensité qui traverse les fils peut dépasser 400 A.
> Les alternateurs des centrales électriques ne peuvent pas fournir directement de telles tensions et celles-ci ne peuvent être utilisées directement par le consommateur. II est donc nécessaire :
> - d'élever la tension au niveau de la centrale électrique ;
> - d'abaisser la tension au niveau du lieu de consommation.
> 
> L'utilisation du courant alternatif et des transformateurs permet de réaliser ces opérations de façon simple. C'est la raison pour laquelle l'utilisation du courant alternatif a très rapidement supplanté celle du continu.
> Cependant, les progrès technologiques actuels permettent l'utilisation de très hautes tensions continues pour le transport d'énergie électrique sur de grandes distances (liaison France-Angleterre par exemple). En effet, la présence d'une capacité entre les conducteurs d'une ligne à haute tension empêche l'utilisation de l'alternatif pour le transport d'énergie électrique sur des grandes distances. Ces distances sont de l'ordre :
> - de la dizaine de kilomètre pour les lignes enterrées dont la capacité est grande ;
> - du millier de kilomètre pour les lignes aériennes.

> [!note] Présentation du transformateur : Utilisation des transformateurs
> Le transformateur est un appareil très courant. Nous en rencontrons de toutes les tailles : du transformateur utilisé dans le transport d'énergie électrique à haute tension de plusieurs tonnes au transformateur basse tension des adaptateurs secteur des petits appareils électriques d'une centaine de grammes.
> ==**- Le transformateur est un convertisseur d'énergie électrique. Il transfère, en alternatif et uniquement en alternatif, de la puissance électrique d'une source placée dans le circuit primaire, à une charge placée dans le circuit secondaire. Cette conversion s'effectue sans modification de fréquence et avec un excellent rendement énergétique : dans les transformateurs industriels, les pertes sont inférieures à 1 %.**==
> ==**- Comme elle se produit sans conversion d'énergie électromécanique, cette conversion est dite statique.**==
> 
> Cette conversion d'énergie est nécessaire dans deux cas.
> - Adaptation de la source à la charge : La tension délivrée (ou le courant) par la source n'est pas adaptée à la charge, est le cas le plus courant ([[#^figure1|fig. 1]]). Dans le cas du passage de la très haute tension (400 kV) à la moyenne tension (< 32 kV utilisée dans l'industrie) puis à la basse tension (220 V), le transformateur est **abaisseur de tension**. Dans le cas du passage de la moyenne tension (en sortie des alternateurs de centrale électrique) à la haute tension, le transformateur est **élévateur de tension**.
> - Isolation électrique entre la charge et la source : C'est le cas des installations en milieu humide (salles de bains par exemple). L'utilisation d'un transformateur d'isolement évite toute électrocution possible car aucune des deux bornes du secondaire n'est reliée à la Terre ([[#^figure2|fig. 2]]).
> ==**Un transformateur doit être adapté à la source et à la charge auxquelles il est relié. Pour cette raison, les constructeurs précisent les caractéristiques suivantes : la fréquence d'utilisation, la tension d'alimentation primaire, la tension de sortie à vide et la puissance apparente (ou l'intensité nominale).**==
> ==**La puissance apparente est le produit de l'intensité nominale (qui correspond aux conditions d'utilisation optimale du transformateur) par la tension de sortie à vide ; elle est exprimée en VA et non en watts.**==
> 
> Par exemple, un transformateur 220 V, 24 V, 100 VA doit être relié à une source de tension efficace 220 V, 50 Hz et fournit une intensité de $\frac{100}{24} = 4,2 A$ sous 24 V dans les conditions nominales.
> Nous n'étudierons que les transformateurs monophasés, c'est-à-dire ceux pour lesquels la source et la charge n'ont que deux bornes.

> [!note] Présentation du transformateur : Description
> Un transformateur est constitué d'un cadre ferromagnétique sur lequel sont bobinés deux enroulements électriquement indépendants : le primaire (relié à la source) et le secondaire (relié à la charge).
> Le circuit magnétique est constitué d'un matériau ferromagnétique, en général de minces tôles de fer au silicium d'épaisseur comprise environ entre 0,05 mm et 0,5 mm, isolées les unes des autres par du vernis ou par une oxydation superficielle, et fortement comprimées par un système de serrage.
> Chacun des circuits électriques est constitué de fil de cuivre ou d'aluminium émaillé ou enrubanné de coton, papier ou toile pour l'isolation électrique. Ces circuits sont noyés dans la résine ou imprégnés de vernis et comprimés pour résister aux efforts électromagnétiques.
> Dans les transformateurs de forte puissance, le circuit électrique est isolé du circuit ferromagnétique et de l'enveloppe extérieure par un diélectrique (de l'huile ou du pyralène, avant son interdiction). Ce fluide permet aussi d'évacuer vers l'extérieur la chaleur dissipée dans le transformateur ([[#^figure3|fig. 3]]).
> Pour notre étude expérimentale des propriétés du transformateur, nous utiliserons des transformateurs démontables ([[#^figure4|fig. 4]]) qui permettent de tester différents enroulements au primaire et au secondaire.

> [!note] Le circuit ferromagnétique : Les matériaux ferromagnétiques
> L'étude du magnétisme dans la matière se trouve dans le cours d'électromagnétisme (H-Prépa, Électromagnétisme, 2e année, chapitre 8). Nous ne rappelons ici que les résultats essentiels pour la compréhension du transformateur.
> Les sections sur le vecteur aimantation $\overrightarrow{M}$, les vecteurs excitation magnétique $\overrightarrow{H}$ et théorème d'Ampère et le caractéristique d'un matériau ferromagnétique n'apportent pas des informations importantes.
> - Classification des milieux ferromagnétiques : Les milieux ferromagnétiques sont classés en fonction : de la forme de leur cycle d'hystérésis ([[#^figure5|fig. 5]]). Si le cycle est étroit, le milieu est dit doux. Le champ coercitif est alors très faible (inférieur à $100 A . m^{-1}$). C'est le cas des alliages fer-silicium, ou fer-nickel, des carcasses de transformateur. Si le cycle est large, le milieu est dit dur. Le champ coercitif est alors important (supérieur à $1000 A . m^{-1}$). C'est le cas de l'acier (fer avec 1 % de carbone) et de tous les matériaux constituant les aimants.
> - Approximation linéaire : La relation entre $\overrightarrow{B}$ et $\overrightarrow{H}$ dans un matériau ferromagnétique est donc non linéaire.
> Pour un milieu doux, et en nous nous limitant aux faibles valeurs de B et de H, nous pouvons, en première approximation, négliger l'hystérésis et adopter la loi linéaire : $\overrightarrow{B} = \mu_0\mu_r\overrightarrow{H}$. Le coefficient sans dimension $\mu_r$ est appelé **perméabilité magnétique relative** du milieu. $\mu_r$ est égal à 1 pour le vide ou un milieu non magnétique et il est typiquement de plusieurs milliers pour un matériau ferromagnétique doux.

> [!note] Le circuit ferromagnétique : Canalisation du flux magnétique
> Nous raisonnons ici sur un matériau ferromagnétique dans l'approximation linéaire : $\overrightarrow{B} = \mu_0\mu_r\overrightarrow{H}$ avec $\mu_r \approx \,\text{quelques}\, 10^{3}$.
> - Circuit magnétique : Un circuit magnétique ([[#^figure6|fig. 6]]) est constitué par un tube ferromagnétique fermé ; le courant traversant une ou plusieurs bobines permet d'obtenir une excitation $\overrightarrow{H}$ et un champ $\overrightarrow{B}$ dans le matériau et dans le milieu environnant non magnétique (de l'air, en général).
> Le théorème d'Ampère s'écrit pour deux contours $\Gamma_1$ et $\Gamma_2$ situés respectivement à l'intérieur et à l'extérieur du circuit magnétique torique ([[#^figure7|fig. 7]]) : $\displaystyle Ni = \oint_{\Gamma_1}\overrightarrow{H}.d\overrightarrow{l} = \oint_{\Gamma_2}\overrightarrow{H}.d\overrightarrow{l}$.
> La circulation de $\overrightarrow{H}$ ayant la même valeur pour les courbes voisines $\Gamma_1$ et $\Gamma_2$ nous pouvons supposer que l'excitation magnétique $H$ est du même ordre de grandeur en deux points voisins situés à l'intérieur et à l'extérieur du matériau ferromagnétique.
> Or, $\overrightarrow{B} = \mu_0\overrightarrow{H}$ à l'extérieur et $\left\lVert\overrightarrow{B}\right\rVert \gg \mu_0\left\lVert\overrightarrow{H}\right\rVert$ à l'intérieur.
> Il est donc raisonnable d'admettre que :
> ==**Le champ magnétique à l'extérieur du circuit magnétique est négligeable devant le champ qui règne à l'intérieur. En première approximation, nous considérerons que le champ à l'extérieur est nul.**==
> Par ailleurs, nous savons que la composante normale du champ $\overrightarrow{B}$ est continue à l'interface entre les deux milieux. Si le champ à l'extérieur est nul la composante normale de $\overrightarrow{B}$ est également nulle à l'intérieur et $\overrightarrow{B}$ est donc tangent à la surface du circuit magnétique. En d'autres termes :
>==** Avec une excellente approximation, le circuit magnétique constitue un tube de champ magnétique : il a la propriété de canaliser les lignes de champ magnétique.**==
> ==**Cette propriété très importante est liée à la condition : $\left\lVert\overrightarrow{B}\right\rVert \gg \mu_0\left\lVert\overrightarrow{H}\right\rVert$ (ou $\mu_r \gg 1$ pour un milieu linéaire).**==
> Remarque :
> Nous pouvons faire une analogie avec un circuit électrique : Les lignes de courant électrique, tangentes au vecteur densité de courant $\overrightarrow{j}$, sont canalisées par un matériau conducteur entouré d'isolant.
> L'analogie entre les deux situations provient d'une identité formelle entre les équations locales :
> 	- Pour le système électrocinétique : $\overrightarrow{j} = \sigma \overrightarrow{E}$ avec $\sigma_{conducteur} \gg \sigma_{isolant}$ et $\overrightarrow{j}$ normal continu à l'interface.
> 	- Pour un circuit magnétique linéaire : $\overrightarrow{B} = \mu_0\mu_r\overrightarrow{H}$ avec $\mu_{r,\,fer} \gg \mu_{r,\,air} = 1$ et $\overrightarrow{B}$ normal continu à l'interface.
> - Flux magnétique commun : Nous savons que, d'après l'équation de Maxwell, $div\overrightarrow{B} = 0$, le flux du champ magnétique $\overrightarrow{B}$ a la même valeur à travers toute section d'un tube de champ. Cette propriété s'applique donc au circuit magnétique. Les fils de la bobine ne sont pas directement enroulés sur le circuit ferromagnétique. Il existe donc des lignes de champ magnétique extérieures ([[#^figure8|fig. 8]]). Mais comme la valeur du champ $\overrightarrow{B}$ est négligeable à l'extérieur, nous pouvons confondre le flux commun canalisé par le circuit magnétique avec le flux de $\overrightarrow{B}$ à travers toute spire de la bobine ; c'est l'approximation du circuit magnétique sans fuites.
> Dans l'approximation, généralement justifiée, du circuit magnétique sans fuites :
> 	- le flux du champ magnétique a la même valeur à travers toute section d'un circuit magnétique dans la mesure où on peut assimiler celui-ci à un tube de champ ;
> 	- ce flux, appelé flux magnétique commun $\Phi_c$, est aussi égal au flux du champ magnétique à travers toute spire des bobines enroulées sur le circuit magnétique.

> [!note] Le circuit ferromagnétique : Application du théorème d'Ampère et de la loi de Faraday au circuit magnétique d'un transformateur
> Toute l'étude théorique du transformateur repose sur l'application de deux lois étudiées en électromagnétisme : la loi de Faraday reliant la f.e.m. d'induction au flux $\left(e = -\dfrac{d\Phi}{dt}\right)$, et le théorème d'Ampère.
> - Modélisation d'un transformateur : Le circuit magnétique d'un transformateur ([[#^figure3|fig. 3]] et [[#^figure4|4]]) a en général une forme rectangulaire. Mais nous n'aurons en fait besoin que de la relation $\Phi_c(i_1, i_2)$ qui relie entre eux le flux commun et les courants qui circulent dans les enroulements. Nous symboliserons généralement le circuit magnétique par un circuit torique ([[#^figure9|fig. 9]]) pour lequel la fonction $\Phi_c(i_1, i_2)$ est identique à celle du circuit étudié. Nous verrons que la forme torique se prête à des calculs simplifiés.
> - Conventions d'orientation : Orientons de façon arbitraire le circuit magnétique.
> Ce choix permet de définir une orientation des enroulements primaire et secondaire : l'orientation des spires est choisie de telle sorte que la normale orientée est dans le sens choisi pour l'orientation du circuit magnétique ([[#^figure10|fig. 10]]).
> ==**Nous orienterons, dans cet ouvrage, les intensités dans les deux enroulements en fonction de ce choix : ainsi, la normale aux spires est orientée dans le sens choisi pour l'orientation du circuit magnétique.**==
> ==**Cette convention permet de définir une paire de bornes homologues du transformateur. Elle est composée de la borne du primaire et de celle du secondaire par où rentre un courant positif avec la convention d'orientation ci-dessus.**==
> ==**Cette paire homologue est conventionnellement marquée par des joints au niveau des bornes.**==
^par2

> [!note] Le circuit ferromagnétique : Application du théorème d'Ampère et de la loi de Faraday au circuit magnétique d'un transformateur : Courant magnétisant
> Dans le cas général d'un circuit magnétique de forme quelconque ([[#^figure11|fig. 11]]) appliquons le théorème d'Ampère sur une ligne de champ quelconque à l'intérieur du circuit ferromagnétique.
> L'intensité enlacée est égale à $N_1i_1 + N_2i_2$.
> La relation obtenue $\displaystyle \oint_{\substack{\text{lignes}\\ \text{de champ}}}\overrightarrow{H}.d\overrightarrow{l} = \oint_{\substack{\text{lignes}\\ \text{de champ}}}H.dl = N_1i_1 + N_2i_2$ montre que la circulation de l'excitation est indépendante de la ligne de champ choisie.
> Définissons le courant magnétisant $i_m$ par $i_m = i_1 + \frac{N_2}{N_1}i_2$.
> Nous remarquons que $\displaystyle \oint_{\substack{\text{lignes}\\ \text{de champ}}}H.dl = N_1i_m$.
> ==**Le courant magnétisant $i_m$ est l'intensité parcourant le primaire en l'absence de courant dans le secondaire créant la même excitation magnétique qu'au point de fonctionnement défini par les $i_1$ et $i_2$.**==
> Dans le cas particulier du circuit torique linéaire de longueur moyenne $l$ et de section droite d'aire $S$ nous pouvons supposer, en première approximation que :
> - toutes les lignes de champ sont des cercles de longueur voisine de $l$ ;
> - la norme B du champ $\overrightarrow{B}$ a la même valeur en tout point d'une section droite. Donc, si $\Phi_c$ désigne le flux commun: $B = \frac{\Phi_c}{S}$. $S$ étant uniforme, B est uniforme dans tout le volume du circuit magnétique ainsi que H. Le théorème d'Ampère s'écrit alors simplement : $Hl = N_1i_1 + N_2i_2$ d'où : $H = \frac{N_1i_1 + N_2i_2}{l} = \frac{N_1i_m}{l}$.
> Remarque : Si l'aire de la section droite n'est pas uniforme ([[#^figure12|fig. 12]]), B est plus intense dans les zones où $S$ est plus faible. Si le milieu est linéaire, $H$ est toujours proportionnelle $N_1i_m$ mais le coefficient de proportionnalité n'est plus aussi simple.

> [!note] Le circuit ferromagnétique : Application du théorème d'Ampère et de la loi de Faraday au circuit magnétique d'un transformateur :
> - Relation entre flux magnétique commun et courant magnétisant :
> La relation entre $\overrightarrow{H}$ et  $\overrightarrow{B}$ est une relation constitutive du matériau ferromagnétique. Elle permet de relier le flux commun $\Phi_c$ et le courant magnétisant $i_m$. Dans le cadre du modèle linéaire, elle a une expression simple : $\overrightarrow{B} = \mu_0\mu_r\overrightarrow{H}$, où $\mu_r$ est la perméabilité magnétique relative du milieu.
> Ainsi, pour un circuit torique et avec les mêmes hypothèses que précédemment : $\Phi_c = SB = \frac{\mu_0\mu_rN_1S}{l}i_m$.
> Pour un matériau linéaire, mais avec des approximations moins fortes, nous obtenons toujours une relation linéaire entre $\Phi_c$ et $i_m$.
> Mais, ce n'est pas le cas dans un transformateur, où la relation entre le flux magnétique commun et le courant magnétisant est non linéaire et présente même un phénomène d'hystérésis : la relation entre ces grandeurs est différente suivant le sens de variation du courant magnétisant ([[#^figure13|fig. 13]]).
> - Différence de potentiel aux bornes d'un enroulement :
> Chaque enroulement est caractérisé par sa résistance ($R_1$ ou $R_2$) et son nombre de spires ($N_1$ ou $N_2$).
> Étudions le primaire. Le flux total à travers l'enroulement est $\Phi_1 = N_1\Phi_c$.
> La loi de Faraday nous donne l'expression de la f.e.m. d'induction dans le primaire : $e_1 = -\dfrac{d\Phi_1}{dt} = -N_1\dfrac{d\Phi_c}{dt}$.
> La tension $u_1$, orientée comme sur la [[#^figure14|figure 14]] est donc : $u_1 = -e_1 = N_1\dfrac{d\Phi_c}{dt} + R_1i_1$.
> De même, aux bornes du secondaire : $u_2 = -e_2 = N_2\dfrac{d\Phi_c}{dt} + R_2i_2$.
> Peut-on négliger les termes ohmiques $R_1i_1$ et $R_2i_2$ ? Prenons l'exemple d'un transformateur dont le secondaire de résistance $R_2 = 10 \Omega$ alimente une résistance qui consomme une puissance moyenne de 110 W sous une tension efficace de 220 V. L'intensité efficace est donc de 0,5 A, soit $R_2I_{2,\,eff} = 5 V$.
> En première approximation, nous pouvons, dans ce cas, négliger $R_2i_2$ devant $u_2$ et écrire : $u_2 \approx N_2\dfrac{d\Phi_c}{dt}$.
> Cette approximation cesserait d'être valide si le même transformateur devait fournir une puissance nettement plus importante.
^par1

> [!note] Recherche du transformateur parfait
> Les relations entre les grandeurs caractéristiques du transformateur ne permettent pas une écriture simple des relations électriques reliant intensités et différences de potentiel des bobinages du transformateur.
> Nous devons donc introduire des hypothèses simplificatrices pour obtenir des relations simples.
> - Relation entre les tensions : Nous nous plaçons toujours dans l'hypothèse d'un circuit magnétique sans fuite. Les relations obtenues au [[#^par1|paragraphe précédent]] prennent une forme simple si $R_1$ et $R_2$ sont nulles.
> ==**Si le circuit magnétique est sans fuite et si la résistance des bobinages est négligeable, la différence de potentiel entre les bornes du circuit primaire vaut $u_1 = -e_1$, soit $u_1 = N_1\dfrac{d\Phi_c}{dt}$, et entre bornes du secondaire $u_2 = -e_2$, soit $u_2 = N_2\dfrac{d\Phi_c}{dt}$.**==
> ==**Le rapport $m = \frac{u_2}{u_1} = \frac{N_2}{N_1}$ est appelé *rapport de transformation*.**==
> ==**Il est indépendant de la charge branchée au secondaire du transformateur.**==
> Remarques :
> 	- Que se passe-t-il si un transformateur est alimenté avec une tension de valeur moyenne non nulle (tension continue par exemple) ?
> Une intensité continue dans un bobinage du circuit crée un flux magnétique commun constant. Il n'apparaît donc pas de f.e.m. aux bornes des bobines. La différence de potentiel est alors uniquement due à la résistance des circuits.
> **Les équations électriques du transformateur ne sont valables qu'en régime alternatif (c'est-à-dire pour des signaux de valeur moyenne nulle).**
> 	- Comment déterminer expérimentalement des bornes homologues ?
> En régime sinusoïdal, et avec les conventions adoptées, les tensions $u_1$ et $u_2$ sont en phase.
> Pour déterminer les bornes homologues d'un transformateur, il suffit donc de relier une borne de chaque enroulement à la masse, et de visualiser les tensions aux deux autres bornes à l'aide d'un oscilloscope. Si elles sont en phase, c'est que les bornes sont homologues ([[#^figure15|fig. 15]]).

> [!note] Recherche du transformateur parfait : Relation entre les courants : Expression approchée du rapport des intensités
> Une relation simple entre les intensités au primaire, au secondaire et les tensions correspondantes n'existe que dans le cas où le milieu magnétique est linéaire. Cette hypothèse n'est en général pas vérifiée, même approximativement. Nous devons chercher la modélisation du transformateur par une autre méthode.
> Déterminons l'ordre de grandeur du courant magnétisant dans un transformateur. Comment le mesurer ? En négligeant la résistance des enroulements, la tension au primaire vaut : $u_1 = N_1\dfrac{d\Phi_c}{dt}$.
> Le courant magnétisant ne dépend que de $\Phi_c$ et donc uniquement de la tension d'alimentation $u_1$ du primaire du transformateur, pas des intensités. Donc pour une tension d'alimentation fixée, le courant magnétisant est égal au courant parcourant le primaire du transformateur quand son secondaire est à vide.
> 
> Exemple : Prenons un transformateur 220 V // 12 V de puissance apparente 75 VA. Mesurons le courant efficace au primaire du transformateur, quand son secondaire est à vide. Nous trouvons environ 40 mA, soit $I_m = 40 mA$. Mesurons le courant efficace au primaire du transformateur chargé par un récepteur de résistance $2 \Omega$, ce qui correspond à une puissance dissipée voisine de 75 W. Nous trouvons environ 350 mA, soit $I_1 = 40 mA$. Le courant magnétisant représente environ 10 % du courant nominal du primaire.
> 	
> ==**En utilisation normale, le courant magnétisant est faible devant le courant au primaire (courant nominal).**==
> Si nous négligeons le courant magnétisant devant $i_1$, la relation : $i_2 = \frac{N_1}{N_2}(i_m - i_1)$ devient $i_2 = -\frac{N_1}{N_2}i_1$, soit $\frac{i_2}{i_1} = -\frac{N_1}{N_2} = -\frac{1}{m}$, (avec l'exemple précédent nous pourrions mesurer l'intensité efficace au secondaire : $I_2 = 6,2 A$).
> ==**Le rapport des intensités est égal à l'opposé de l'inverse du rapport de transformation si le courant magnétisant est négligeable devant le courant dans le primaire ce qui est généralement le cas avec un "bon" transformateur utilisé « normalement ».**==
> Cette relation n'est valable que si les intensités sont alternatives. N'oublions pas que la tension et l'intensité au secondaire sont dues à des phénomènes d'induction liés aux variations de la tension au primaire.

> [!note] Recherche du transformateur parfait : Relation entre les courants : Conditions de validité
> A quelle(s) condition(s) le courant magnétisant peut-il être négligé ?
> D'après le théorème d'Ampère appliqué à une ligne de champ $\Gamma$ : $\displaystyle i_m = \frac{1}{N_1}\oint_{\Gamma}Hdl$.
> Il y a donc deux façons de faire tendre $i_m$ vers 0 :
> - augmenter $N_1$ et donc, pour m donné, $N_2$. C'est une des raisons pour lesquelles les transformateurs usuels ont des enroulements de plusieurs centaines de spires ;
> - faire en sorte que H soit nul.
> 
> Nous pouvons obtenir $H = 0$ dans deux cas-limites :
> - si le secondaire, de résistance nulle, est court-circuité, nous pouvons écrire : $u_2 = 0 = N_2\dfrac{d\Phi_c}{dt}$ soit, en régime alternatif, $\Phi_c = 0$, $B = 0$ et $H = 0$ ;
> - si le milieu ferromagnétique est linéaire avec $\mu_r \rightarrow \infty$, alors H doit être nul pour conserver des valeurs bornées à B et $\Phi_c$.
> 
> ==**La relation $i_2 = -\frac{1}{m}i_1$ qui caractérise un transformateur idéal est rigoureusement vérifiée avec le modèle idéalisé d'un milieu linéaire de perméabilité relative $\mu_r$ tendant vers l'infini.**==
> ==**Elle est en fait applicable si :**==
> - ==**le nombre de spires des enroulements est suffisamment grand ;**==
> - ==**le secondaire, de résistance négligeable, débite sur une charge d'impédance suffisamment faible.**==
> 
> ==**Ces conditions sont généralement respectées par un transformateur dans ses [[#^def1|conditions nominales d'utilisation]].**==
> Remarque : Pour des courants donnés, les champs H et B sont d'autant moins intenses que $N_1$ et $N_2$ sont grands. Pour que la saturation du milieu ferromagnétique ne vienne pas diminuer les performances du transformateur, il faut limiter H et donc utiliser des enroulements comportant un nombre suffisant de spires.

> [!note] Le transformateur parfait : Modèle du transformateur parfait
> Le modèle du transformateur parfait ([[#^figure16|fig. 16]]) regroupe les hypothèses faites dans les paragraphes précédents : résistances nulles, circuit magnétique sans fuites et courant magnétisant négligeable.
> Le transformateur parfait est caractérisé uniquement par son rapport de transformation m. Les relations entre tensions et intensités sont : $u_2 = mu_1$ et $i_2 = -\frac{i_1}{m}$ (attention aux signes).
> Ces relations peuvent aussi s'écrire $u_1 = \frac{1}{m}u_2$ et $i_1 = -mi_2$.
> Un transformateur parfait est réversible (attention, pas au sens de la thermodynamique) : les rôles des circuits primaire et secondaire peuvent être permutées. Alors le rapport de transformation devient $\frac{1}{m}$.
> Avec le modèle du transformateur parfait, les équations reliant $u_1$, $u_2$, $i_1$ et $i_2$ sont linéaires ; le modèle est linéaire. Si le reste du circuit est composé d'éléments linéaires, les équations qui le régissent sont linéaires. Le circuit peu donc être étudié avec les techniques utilisées sur les circuits linéaires classiques. En particulier, nous utiliserons le régime sinusoïdal forcé et l'opérateur p.
> Les équations du transformateur parfait en notation opérationnelle s'écrivent : $U_2(p) = mU_1(p)$ et $I_2(p) = -\frac{I_1(p)}{m}$ et les grandeurs efficaces vérifiant $m = \frac{U_2}{U_1} = \frac{I_1}{I_2}$.

> [!note] Le transformateur parfait
> - Puissances instantanées : La puissance instantanée électrique reçue par le transformateur (**qu'il soit parfait ou non**) est la somme de la puissance reçue au primaire $u_1i_1$ et au secondaire $u_2i_2$ : $P = u_1i_1 + u_2i_2$ (attention aux signes qui dépendent encore de la convention choisie (cf. [[#^par2|paragraphe 2]])).
> Comme pour un transformateur parfait $u_2 = mu_1$ et $i_2 = -\frac{i_1}{m}$, cette puissance totale est nulle.
> ==**La puissance instantanée fournie au primaire du transformateur parfait est intégralement transférée à la charge par le secondaire. Il n'y a ni stockage, ni dissipation d'énergie dans un transformateur parfait.**==
> - Transfert d'impédance : Vu du primaire, l'ensemble {transformateur + charge} est équivalent a un dipôle dont les caractéristiques dépendent de la charge et du rapport de transformation. **Remplacer l'ensemble {transformateur + charge} par le dipôle équivalent est appelé transfert des caractéristiques de la charge au primaire.** Comment déterminer les caractéristiques de la charge transférée au primaire ? La caractéristique courant-tension de la charge donne la relation entre $u_2$ et $i_2$. Les équations couplant le primaire et le secondaire permettent de déterminer la relation entre $u_1$ et $i_1$.
> Plaçons-nous dans le cas d'un régime sinusoïdal forcé de pulsation $\omega$ et d'une charge représentée par un dipôle linéaire d'impédance $Z_c(p)$ ([[#^figure17|fig. 17]]). Les équations $U_2(p) = -Z_c(p)I_2(p)$, $U_2(p) = mU_1(p)$ et $I_1(p) = -mI_2(p)$ imposent la relation : $U_1(p) = \frac{Z_c(p)I_1(p)}{m^{2}}$.
> ==**L'impédance vue au niveau du primaire du transformateur est $\frac{Z_c(p)}{m^{2}}$, impédance de la charge $Z_c(p)$ (branchée au secondaire) divisée par le carrée du rapport m de transformation.**==
> L'impédance « vue » au primaire du transformateur parfait a le même argument que l'impédance de la charge. En particulier, une résistance est vue comme une résistance, un condensateur comme un condensateur et une bobine comme une bobine.

> [!note] Le transformateur parfait : Transfert de la source
> Inversement, vu du secondaire, l'ensemble {transformateur + source} est équivalent à un dipôle dont les caractéristiques dépendent de la source et du rapport de transformation.
> **Remplacer l'ensemble {transformateur + source} par le dipôle équivalent est appelé transfert des caractéristiques de la source au secondaire.**
> Plaçons-nous du point de vue de la charge et cherchons le dipôle équivalent au transformateur alimenté par un générateur. La relation entre la tension $u_1$ aux bornes du générateur et son courant de sortie $i_1$ fixe la relation entre $u_2$ et $i_2$.
> Dans le cas d'un régime sinusoïdal forcé de pulsation $\omega$, modélisons la source par un générateur de Thévenin de f.e.m. $E(p)$ et d'impédance $Z_s(p)$ en notation opérationnelle ([[#^figure18|fig. 18]]).
> Des relations $U_1(p) = E(p) - Z_s(p)I_1(p)$ définissant le générateur et l'ensemble des relations $U_2(p) = mU_1(p)$ et $I_2(p) = -\frac{I_1(p)}{m}$ caractéristiques du transformateur, nous déduisons : $U_2(p) = mE(p) + m^{2}Z_s(p)I_2(p)$.
> La source vue à travers le transformateur parfait est équivalente à un générateur de Thévenin de f.e.m. $mE(p)$ et d'impédance $m^{2}Z_s(p)$.
> ==**La source transférée au secondaire a pour f.e.m. $mE (p)$, et pour impédance $m^{2}Z_s(p)$ :**==
> - ==**la f.e.m. E(p) de la source (branchée au primaire) est multipliée par le rapport m de transformation ;**==
> - ==**l'impédance $Z_s(p)$ de cette source est multipliée par le carré du rapport m de transformation.**==

> [!note] Modélisation du transformateur réel
> Le modèle du transformateur ne rend pas parfaitement compte des caractéristiques du transformateur réel.
> Nous ne modéliserons que les corrections dues aux fuites magnétiques et à la résistance non nulle des bobinages.
> En effet, ils sont bien représentés dans un modèle linéaire du transformateur alors que les défauts liés au circuit ferromagnétique sont non linéaires.
> - Inductances de fuite : Une faible partie de champ magnétique créé par l'enroulement primaire n'est pas parfaitement canalisée par le circuit magnétique ([[#^figure19|fig. 19]]). Ces lignes de champ sont principalement situées à l'extérieur du noyau dans un milieu assimilable au vide. Leur contribution au flux magnétique à travers le primaire est donc bien représentée par une fonction linéaire de l'intensité $L_{f\,1}i_1$, où $L_{f\,1}$ est appelée **inductance de fuite du primaire**.
> Nous écrivons alors : $\Phi_1 = N_1\Phi_c + L_{f\,1}i_1$.
> De même, nous pouvons définir une **inductance de fuite $L_{f\,2}$ au niveau du secondaire** et écrire : $\Phi_2 = N_2\Phi_c + L_{f\,2}i_2$.
> Nous remarquons que le f.e.m. d'inductance au primaire est : $e_1 = -\dfrac{d\Phi_1}{dt} = -N_1\dfrac{d\Phi_c}{dt} - L_{f\,1}\dfrac{di_1}{dt}$ somme de la f.e.m. au primaire du transformateur parfait et de la f.e.m. aux bornes d'une inductance $L_{f\,1}$.
> ==**Pour modéliser les fuites de champ, il suffit de placer en série une inductance $L_{f\,1}$ (inductance de fuite du primaire) avec le primaire du transformateur parfait et une inductance $L_{f\,2}$ (inductance de fuite du secondaire) avec le secondaire du même transformateur parfait.**==
> - Résistance des bobinages : La résistance des bobinages provoque les chutes de tension $R_1i_1$ au primaire et $R_2i_2$ au secondaire.
> La tension aux bornes du primaire s'écrit : $u_1 = N_1\dfrac{d\Phi_c}{dt} + L_{f\,1}\dfrac{di_1}{dt} + R_1i_1$.
> La résistance des bobinages primaire et secondaire peut être modélisée par une résistance placée en série avec le primaire et le secondaire du transformateur parfait.
> - Modèles du transformateur réel : A partir du modèle ([[#^figure20|fig. 20]]) mettant en évidence les inductances de fuite et les résistances des bobinages, nous pouvons déterminer deux modèles équivalents en utilisant le transfert d'impédances.
> Nous obtenons donc les figures [[#^figure21|21]] et [[#^figure22|22]] correspondant à un transfert de toutes les impédances au primaire ou au secondaire du transformateur.
> Cette modélisation est souvent très insuffisante. Elle peut être améliorée en ajoutant un dipôle en parallèle sur le primaire du transformateur ([[#^figure23|fig. 23]]).
> Ce dipôle prend en compte les caractéristiques du circuit magnétique. Il ne peut malheureusement pas être modélisé par un élément linéaire. L'étude d'un circuit électrique comprenant des transformateurs nécessite souvent des moyens de calcul lourds.
^par4

> [!note] Étude expérimentale de l'hystérésis dans un transformateur : Observation du courant et de la tension du primaire
> Utilisant le montage du [[#^figure24|figure 24]] : observons simultanément l'intensité et la tension du primaire d'un transformateur à l'oscilloscope en l'absence de courant au secondaire (secondaire à vide).
> Pour des raisons de sécurité, il est nécessaire d'isoler le circuit étudié du secteur : **Il ne faut jamais relier un des fils du secteur 220 V à la masse d'un oscilloscope !**
> C'est pour ces raisons, que nous utilisons le montage du [[#^figure24|figure 24]], où le transformateur d'isolement isole le montage du secteur.
> Nous remarquons sur la [[#^figure25|figure 25]], qu'à une tension sinusoïdale correspond une intensité alternative non sinusoïdale et non symétrique.
> La caractéristique courant-tension du montage est donc non linéaire.

> [!note] Étude expérimentale de l'hystérésis dans un transformateur : Tracé du cycle d'hystérésis
> Comment pouvons-nous obtenir à partir de cette caractéristique les champs B et H dans la carcasse et tracer le cycle d'hystérésis B(H) ?
> Le modèle du transformateur torique permet de préciser les relations entre $H$, $B$, $u_2$ et $i_1$. Si $S$ est la section du noyau et $l$ sa longueur moyenne, $N_1$ et $N_2$ le nombre de spires au primaire et au secondaire ([[#^figure26|fig. 26]]), alors : $e_1 = -\dfrac{d\Phi_1}{dt} = -N_1S\dfrac{dB}{dt}$ ; $e_2 = -\dfrac{d\Phi_2}{dt} = -N_2S\dfrac{dB}{dt}$ ; $H = \frac{N_1i_1 + N_2i_2}{l} = \frac{N_1i_m}{l}$.
> Quand le secondaire est en circuit ouvert, ces expressions se simplifient, car $i_2 = 0$ : $u_2 = -e_2 = \dfrac{d\Phi_2}{dt} = N_2S\dfrac{dB}{dt}$ et $H = \frac{N_1i_1}{l}$.
> Nous admettons que ces résultats restent valables dans le cas d'un transformateur quelconque.
> Étudions le montage du [[#^figure27|figure 27]].
> Le transformateur à secondaire variable (ou un transformateur d'isolement suivi d'un autotransformateur ; figures [[#^figure28|28]] et [[#^figure29|29]]) permet d'isoler le circuit étudié du secteur et permet de choisir différentes amplitudes pour la tension au primaire. La tension aux bornes de la résistance $R_0$ est proportionnelle à l'intensité parcourant le primaire, donc à $H(t)$.
> Au niveau du secondaire, le pont diviseur $RC$ joue le rôle de pseudo-intégrateur. En effet, l'impédance d'entrée de l'oscilloscope de l'ordre du mégaohm peut être négligée par rapport à R et la constante de temps $RC = 0,22 s$ est grande devant la période (20 ms) du signal à 50 Hz.
> La tension aux bornes de C est : $U_C(t) \approx \frac{1}{RC}\int u_2 dt = \frac{N_2S}{RC}B(t)$, car la constante d'intégration est nulle (u_C et B(t) sont de valeur moyenne nulle). La tension aux bornes de $C$ est donc proportionnelle à $B(t)$.
> Il est possible de remplacer ce circuit "RC" par un intégrateur à amplificateur opérationnel, dont l'intérêt est son impédance de sortie quasiment nulle ([[#^figure30|fig. 30]]).
> Pour quelles raisons, l'utilisation du circuit secondaire pour mesurer B est-elle préférable à celle du primaire ?
> Nous avons choisi le circuit secondaire et non le primaire du transformateur pour mesurer le champ magnétique, car un courant circule dans le primaire (de l'ordre de l'ampère) et quasiment aucun dans le secondaire.
> - Ce courant du primaire provoque une chute de tension à cause de la résistance du bobinage.
> - Les bobinages du transformateur présentent une inductance de fuite. Le flux magnétique à travers le primaire diffère donc de $N_1SB$. En revanche, au secondaire, l'intensité est nulle et donc le flux de fuite l'est aussi.
> 
> Pour différentes valeurs de la tension d'alimentation du transformateur, nous obtenons une série de cycles symétriques par rapport à l'origine ([[#^figure31|fig. 31]]).
> Sauf sur les maquettes spécialement conçues pour le tracé des cycles d'hystérésis, le constructeur ne donne pas le nombre de spires des enroulements d'un transformateur. Les paramètres $S$ et $l$ sont compliqués à mesurer dans le cas d'un transformateur non démontable.
> Il est donc difficile de trouver les constantes de proportionnalité entre $u_C$ et $B$ et entre $R_0i_0$ et $H$.
> Pour le montage utilisé sur la [[#^figure31|figure 31]], les coefficients sont environ : $H = 100 A . m^{-1}$ pour $R_0i_1 = 0,5 V$ et $B = 1 T$ pour $u_C = 1 V$.
> Un transformateur démontable pour lequel ces paramètres sont aisément mesurables présente l'inconvénient de ne pas avoir un circuit magnétique continu ([[#^figure32|fig. 32]]). Cette discontinuité modifie de façon notable le cycle obtenu par la méthode utilisée ici ([[#^figure33|fig. 33]]).
^par3

> [!note] Étude expérimentale de l'hystérésis dans un transformateur : Interprétation des résultats
> Interprétons les courbes de [[#^figure31|figure 31]]. Les valeurs dépendent bien entendu du matériau ferromagnétique utilisé.
> - Caractère ferromagnétique : Un matériau ferromagnétique se caractérise par la grande valeur de son aimantation. La relation $\overrightarrow{B} = \mu_0(\overrightarrow{H} + \overrightarrow{M})$ devient, avec $M \gg H$ : $\overrightarrow{B} = \mu_0\overrightarrow{M}$.
> D'après la [[#^figure31|figure 31]], pour $B_{max} = 1T$, l'excitation maximale vaut environ $300 A . m^{-1}$ ce qui donne : $B \approx 2500\mu_0H$.
> L'hypothèse est donc confirmée. Si, pour un calcul approché, nous considérons le matériau comme linéaire, nous choisirons $\mu_r \approx 2500$.
> - Aimantation à saturation : Utilisons une tension d'alimentation nettement supérieure à la tension nominale du transformateur. Nous obtenons un cycle semblable à celui de [[#^figure34|figure 34]].
> Le cycle d'hystérésis $B(H)$ présente alors deux domaines (a) et (c) où M a atteint sa valeur maximale (aimantation à saturation) $M_{sat}$.
> Pour le domaine (a) : $B = \mu_0(H + M_{sat}) \approx \mu_0M_{sat} = B_{sat}$.
> D'après les mesures, nous trouvons $B_{sat} \approx 1,8 T$ (pour le transformateur étudié).
> Remarques :
> 	- Pour cet essai en dehors des conditions normales d'utilisation, il faut veiller à la valeur maximale du courant dans le primaire.
> 	- Quand l'aimantation atteint sa valeur de saturation, le noyau ferromagnétique canalise moins efficacement les lignes de champ. Le champ magnétique n'est plus uniforme et le protocole expérimental de relevé du cycle d'hystérésis ne donne plus de résultat précis.
> - Champ rémanent et excitation coercitive : La portion de cycle correspondant à la diminution de H à partir de sa valeur maximale (domaine (b) de [[#^figure34|figure 34]]) possède deux points remarquables :
> 	- le point $A_r$, pour lequel $H = 0$ et $B = B_r$ (champ rémanent) ;
> 	- le point $A_c$, pour lequel $B = 0$ et $H = -H_c$ ($H_c$ : excitation coercitive).
> 
> 	D'après la [[#^figure31|figure 31]], nous mesurons pour des valeurs suffisamment grandes de $H_{max}$ : $B_r$ de l'ordre de 1 T et $H_c$ de l'ordre de $150 A . m^{-1}$. Ces valeurs dépendent, bien évidemment, du matériau ferromagnétique utilisé.
> 	Remarque : On appelle souvent $H_c$ « champ coercitif ». Il existe en effet une autre convention, utilisée par les électrotechniciens, pour nommer les grandeurs magnétiques : $\overrightarrow{B}$ est désigné par « induction magnétique » et $\overrightarrow{H}$ par « champ magnétique ».

> [!note] Dissipation d'énergie dans la carcasse
> - Courants de Foucault : Le matériau ferromagnétique constituant la carcasse du transformateur est en général un bon conducteur ohmique (alliage à base de fer). Comme la carcasse est placée dans un champ magnétique variable, l'équation de Maxwell-Faraday, $rot\overrightarrow{E} = - \dfrac{\partial\overrightarrow{B}}{\partial t}$, impose un champ électrique non nul.
> Ce champ est la source de courants électriques d'autant plus intenses que la conductivité de la carcasse est grande.
> ==**Les courants créés par induction dans la masse d'un conducteur sont appelés courants de Foucault. Ils sont la source d'une dissipation d'énergie par effet Joule.**==
> Les pertes par courant de Foucault sont donc proportionnelles :
> 	- la conductivité $\gamma$ du milieu ;
> 	- au carré de la fréquence $f$ ;
> 	- au carré de la section $S$ des tôles ;
> 	- au carré de la valeur maximale du champ magnétique $B_0$.
> 
> 	Pour minimiser ces pertes dans une masse métallique importante, celle-ci doit être constituée de tôles peu épaisses parallèles au champ magnétique, isolées les unes des autres ([[#^figure35|fig. 35]]).
> - Pertes dues à l'hystérésis : Reprenons le modèle torique du [[#^par2|paragraphe précédent]], le secondaire étant ouvert. Supposons que les pertes par courant de Foucault et par effet Joule dans le primaire sont négligeables.
> La puissance $\mathcal{P}_H = u_1i_1$ dissipée dans le transformateur est alors uniquement due aux propriétés ferromagnétiques de la carcasse.
> D'après l'étude du [[#^par3|paragraphe précédent]], $H = \frac{N_1i_1}{l}$ et $u_1 = -e_1 = \dfrac{d\Phi_1}{dt} = N_1S\dfrac{dB}{dt}$ (en négligeant la résistance ohmique du primaire).
> Donc $\mathcal{P}_H = SlH\dfrac{dB}{dt}$. Comme le produit $Sl$ représente le volume V de la carcasse magnétique, la puissance $p_H$ dissipée par unité de volume de carcasse vaut $p_H = H\dfrac{dB}{dt}$.
> Si nous calculons l'énergie $e_H$ dissipée par unité de volume sur une période T : $\displaystyle e_H = \int_{t}^{t+T}H\dfrac{dB}{dt}dt = \oint_{cycle}HdB$. Cette intégrale représente l'aire du cycle d'hystérésis.
> ==**La densité volumique d'énergie dissipée par période, à cause des propriétés magnétiques de la carcasse, est égale à l'aire du cycle d'hystérésis et la puissance volumique moyenne est donnée par : $\displaystyle \langle p_H \rangle = f\oint_{cycle}HdB$, où $f$ est la fréquence.**==
> - Pertes fer : Les pertes dues aux courants de Foucault et à l'hystérésis de la carcasse ne dépendent que du champ magnétique à l'intérieur de la carcasse. Si la résistance et l'inductance de fuite du primaire sont faibles, la relation entre ce champ et la différence de potentiel aux bornes du primaire est indépendante du courant qui y circule. En effet, B et $u_1$ sont liés par : $u_1 \approx -e_1 = \dfrac{d\Phi_1}{dt} = N_1S\dfrac{dB}{dt}$.
> ==**Les pertes fer sont, par définition, la somme des puissances dissipées dans un transformateur à cause des courants de Foucault et de l'hystérésis de la carcasse.**==
> ==**Pertes fer = pertes par courant de Foucault + pertes par hystérésis.**==
> ==**En première approximation, ces pertes fer ne dépendent que de la tension d'alimentation du primaire du transformateur (fréquence et amplitude), et non du courant.**==

> [!note] Dissipation d'énergie dans la carcasse : choix du matériau
> Le matériau choisi pour constituer la carcasse doit être tel que :
> - les pertes par hystérésis soient minimales : le cycle à hystérésis doit être le plus étroit possible. Il faut choisir un milieu doux ;
> - les pertes par courant de Foucault soient faibles : la carcasse doit être soit feuilletée (ceci n'est efficace qu'à basse fréquence), soit réalisée dans un matériau isolant ;
> - l'aimantation à saturation soit grande : le champ magnétique dans le transformateur doit être inférieur à sa valeur à saturation pour un bon fonctionnement. La relation $u_1 \approx -e_1 = \dfrac{d\Phi_1}{dt} = N_1S\dfrac{dB}{dt}$ montre que : $U_{max} = N_1S\omega B_{max}$. Donc plus $B_{max}$ est important, plus le produit $N_1S$ peut être faible. L'encombrement et le prix du transformateur sont alors diminués.
> 
> Dans les transformateurs basse fréquence, les courants de Foucault sont limités par le feuilletage de la carcasse. Celle-ci est constituée de tôles en alliages à base de fer, soit :
> - au silicium, isolées par une oxydation thermique de leur surface ;
> - au silicium à grains orientés : les cristaux constituant la tôle sont orientés par laminage à froid. L'isolation est due à une couche de silicate de magnésium obtenue par un recuit des tôles ;
> - au nickel, très sensibles aux chocs.
> 
> Dans les transformateurs haute fréquence (transformateurs d'impulsion, transformateurs d'alimentation à découpage, transformateur pour signaux radioélectriques de fréquence allant jusqu'à 1 GHz), le feuilletage de la carcasse est insuffisant. Il est nécessaire d'utiliser des matériaux ferromagnétiques isolants : les ferrites.
> ==**Les carcasses de transformateurs doivent être réalisées avec des matériaux doux, pour limiter les pertes par hystérésis :**==
> - ==**pour une utilisation à basse-fréquence avec des tôles de matériaux doux isolées (tôles au silicium et réduire ainsi les pertes fer) ;**==
> - ==**à haute fréquence avec des ferrites douces.**==
> 
> Remarques :
> - Une ferrite est une céramique de formule $MeFe_2O$, où Me est une combinaison de métaux bivalents le plus couramment manganèse et zinc. Elle est obtenue par mélange de poudres d'oxydes et de carbonates de ces métaux broyés, puis mises en forme à l'aide d'un liant organique et ensuite frittées à 1200 °C environ.
> - Par rapport aux tôles silicium, les ferrites ont comme avantage leur caractère isolant, comme inconvénients leur aimantation faible, leur perméabilité relative faible, leur fragilité (matériau dur et cassant) et leur prix de revient élevé.

> [!note] Caractéristiques d'un transformateur
> Les mesures proposées ici utilisent un wattmètre, des ampèremètres et voltmètres efficaces. Le transformateur utilisé sera de préférence de puissance importante (300 VA par exemple) pour effectuer des mesures fiables en particulier lors de l'étude à vide.
> - Principe et utilisation du wattmètre : Un wattmètre mesure la puissance moyenne consommée par un dipôle par la mesure simultanée de l'intensité qui le traverse et de la tension à ses bornes ([[#^figure38|fig. 38]] et [[#^figure39|39]]).
> Ces grandeurs peuvent être non sinusoïdales et même non alternatives.
> En régime sinusoïdal, les mesures de la puissance $\mathcal{P}$, de la tension efficace $U$ et de l'intensité efficace $I$ permettent de calculer le facteur de puissance ou $\cos\varphi$ ($\varphi$ déphasage entre intensité et tension) par la relation $P = UI\cos\varphi$. Le wattmètre comprend deux circuits électriques : un circuit intensité et un circuit tension ([[#^figure37|fig. 37]]).
> L'utilisation d'un wattmètre électronique ([[#^figure37|fig. 37]]) est simple et pratiquement sans risque pour l'appareil. Il suffit de relier les deux fils provenant de la source et les deux fils allant vers la charge aux bornes prévues à cet effet. Le wattmètre affiche alors la puissance moyenne (ou puissance active) consommée par la charge.
> L'utilisation des anciens modèles analogiques ([[#^figure36|fig. 36]]) est plus complexe et non exempte de risques pour l'appareil. Il faut, en effet, choisir séparément les calibres tension et intensité (et non un hypothétique calibre puissance). Un éventuel dépassement de calibre (en intensité ou en tension) ne se manifeste pas nécessairement par un blocage de l'aiguille à droite de cadran ; l'utilisateur qui ne prend pas la précaution de contrôler l'intensité et la tension risque de ne pas détecter ce dépassement et de laisser l'appareil en surintensité ou en surtension. La [[#^figure39|figure 39]] donne les deux schémas de branchement pour la mesure de la puissance consommée par un dipôle.
> 	- Dans le montage amont ([[#^figure39|fig. 39a]]), le wattmètre mesure la somme des tensions aux bornes du dipôle et du circuit intensité. L'erreur introduite est faible dans les cas où la tension est grande et l'intensité faible. Dans les autres cas, on préférera le montage aval.
> 	- Dans le montage aval ([[#^figure39|fig. 39b]]), le wattmètre mesure la somme des intensités dans le dipôle et dans le circuit tension. L'erreur introduite est en général assez faible.

> [!note] Caractéristiques d'un transformateur : Étude à vide, pertes fer
> Utilisons le montage de [[#^figure40|figure 40]], sur lequel nous mesurons les tensions $U_{1V}$, $U_{2V}$, l'intensité $I_{1V}$ et la puissance $\mathcal{P}_{1V}$.
> Remarques :
> - L'intensité dans le primaire n'étant pas sinusoïdale, seule la valeur donnée par un ampèremètre efficace vrai est significative (RMS). En revanche, le principe du wattmètre lui permet de fonctionner avec des grandeurs non sinusoïdales.
> - La puissance mesurée par le wattmètre est la somme des pertes par effet Joule dans le primaire du transformateur et des pertes fer. Nous pouvons : négliger les pertes par effet Joule car le courant à vide est faible, et assimiler l'indication du wattmètre aux pertes fer.
> 
> Commentons les résultats obtenus lors des mesures ([[#^figure41|fig. 41]]).
> - Tension au secondaire : La courbe $U_{2V}$ en fonction de $U_{1V}$ est une droite, dont la pente est $m_V$, rapport de transformation à vide. Ceci correspond à la relation entre les tensions pour le transformateur parfait. Cette valeur permet de calculer le rapport du nombre de spires (rarement donné par le constructeur) : $m_V = \frac{N_2}{N_1}$.
> ==**A vide, un transformateur réel est parfait pour les tensions.**==
> - Intensité au primaire : La courbe donnant $I_{1V}$ en fonction de $U_{1V}$ n'est pas une droite : le transformateur ne peut pas être assimilé à un dipôle linéaire.
> - Puissance : La courbe de puissance en fonction du carré de la tension efficace $U_{1V}$ au primaire (ou $U_{2V}$ au secondaire) est proche d'une droite ([[#^figure42|fig. 42]]). Or, la valeur efficace $U_{2V}$ est proportionnelle à la valeur maximale $B_{max}$ du champ magnétique.
> ==**Les pertes fer sont sensiblement proportionnelles au carré du champ magnétique maximal $(B_{max})$ dans la carcasse ou au carré de la valeur efficace de la tension d'alimentation.**==
> Remarque : Une étude plus approfondie montrerait que les pertes par courant de Foucault $P_F$ sont en $B_{max}^{2}$ alors que celles par hystérésis $P_H$ en $B_{max}^{\eta}$ où $\eta$ est le coefficient de Steinmetz dont la valeur comprise entre 1,6 (matériaux massifs) et 2 (tôles) dépend de la nature de la carcasse : $\mathcal{P}_F = K_Ff^{2}B_{max}^{2}$ et $\mathcal{P}_H = K_HfB_{max}^{\eta}$.

> [!note] Caractéristiques d'un transformateur : Étude en court-circuit, pertes cuivre
> Lorsque le secondaire d'un transformateur est court-circuité, la tension appliquée au primaire doit être très inférieure à sa tension nominale d'utilisation. Dans le cas contraire, l'échauffement à l'intérieur des bobinages risque de les détruire.
> Sur le montage de [[#^figure43|figure 43]], nous alimentons donc le transformateur sous une tension inférieure à 10 % de sa valeur nominale.
> Nous mesurons simultanément les intensités au primaire $I_{1\,cc}$, au secondaire $I_{2\,cc}$ la tension au primaire $U_{1\,cc}$ et la puissance consommée $\mathcal{P}_{1\,cc}$.
> L'impédance de l'ampèremètre au secondaire doit être suffisamment faible pour que le fonctionnement du transformateur soit très proche de celui en court-circuit. Le wattmètre est branché en montage aval, car l'intensité mesurée est importante.
> Commentons les résultats obtenus lors des mesures ([[#^figure44|fig. 44]]).
> - Intensité au secondaire : La courbe donnant $I_{1\,cc}$ en fonction de $I_{2\,cc}$ est une droite. Le rapport $\frac{I_{1\,cc}}{I_{2\,cc}}$ est sensiblement constant et égal au rapport de transformation à vide $m_v$. Ceci correspond à la relation sur les intensités du transformateur parfait.
> ==**En court-circuit, un transformateur réel est parfait pour les courants.**==
> - Tension au primaire : La courbe $U_{1\,cc}$ en fonction de $I_{2\,cc}$ est une droite. La relation entre courant de court-circuit et tension de court-circuit est linéaire : dans ces conditions, le transformateur peut être assimilé à un dipôle linéaire.
> - Puissance : La courbe donnant la puissance $\mathcal{P}_{1\,cc}$ en fonction du carré de $I_{2\,cc}$ est une droite ([[#^figure45|fig. 45]]).
> ==**La puissance dissipée par effet Joule dans les enroulements est appelée perte cuivre. Elle est proportionnelle au carré du courant secondaire (ou primaire en court-circuit).**==
> 
> Comment pouvons-nous interpréter ces résultats ?
> La tension au secondaire est nulle, soit $u_2 = 0 = -e_2 + R_2i_2$. La chute de tension $R_2i_2$ est petite, donc la f.e.m. d'induction et le flux magnétique dans le transformateur sont faibles et le courant magnétisant est négligeable devant l'intensité au primaire.
> Le transformateur peut être considéré comme linéaire et le modèle donné au [[#^par4|paragraphe ci-dessus]] peut être utilisé ([[#^figure46|fig. 46]]).

> [!note] Caractéristiques d'un transformateur : Caractéristique en charge
> Une étude en charge complète nécessiterait de choisir une charge à caractère inductif ou capacitif ou purement résistif.
> Nous nous contenterons d'une charge résistive constituée d'un rhéostat. Dans ce cas, la puissance fournie à la charge est simplement $\mathcal{P}_2 = U_2I_2$.
> Un voltmètre et un ampèremètre placés au secondaire suffisent donc.
> Nous utilisons le montage de [[#^figure47|figure 47]] permettant de mesurer $I_1$, $U_1$, $\mathcal{P}_1$, $U_2$ et $I_2$ pour différentes valeurs de la résistance de la charge et nous réalisons le tableau suivant ([[#^figure48|fig. 48]]).
> m représente le rapport des tensions entre secondaire et primaire, x le rapport des intensités, $\eta$ le rendement et $\Delta U_2$ la chute de tension au secondaire (différence entre $U_{2V}$ à vide et $U_2$ en charge).
> Analysons les différentes courbes obtenues ([[#^figure49|fig. 49]]) pour ce transformateur de puissance nominale 300 VA.
> - A la puissance nominale, la chute de tension $\Delta U_2$ ne dépasse pas 5 % de la tension secondaire à vide.
> Le rapport de transformation m diminue faiblement quand l'intensité au secondaire augmente, ceci est dû à l'impédance non nulle des enroulements : $m = \frac{U_2}{U_1} < m_V = \frac{U_{2V}}{U_1} \approx \frac{N_2}{N_1}$.
> - Si le transformateur était idéal, le rapport des intensités serait égal à l'inverse du rapport des tensions à vide $I_1 = m_VI_2$.
> Plus l'intensité au secondaire augmente, plus $I_1$ se rapproche de la valeur $m_VI_2$. L'écart entre l'intensité réelle instantanée au primaire et sa valeur théorique correspond au courant magnétisant.
> Comme il est quasiment constant, l'écart entre la valeur réelle et la valeur théorique décroît quand $I_2$ augmente.
> Le rapport des intensités diminue pour tendre vers $m_V$ : $x = \frac{I_1}{I_2} > m_V \approx \frac{N_2}{N_1}$.
> ==**Le comportement du transformateur en charge est proche de celui du transformateur parfait au voisinage de son utilisation nominale.**==
> - Le rendement du transformateur augmente avec $I_2$ jusqu'au voisinage de la puissance nominale, au-delà il diminuerait. Il est proche de l'unité sauf pour des puissances faibles.

> [!note] Caractéristiques d'un transformateur : Adaptation d'impédance
> Dans quel cas une source alternative de résistance interne $R_1$ délivre-t-elle une puissance maximale dans un dipôle résistif de résistance $R_2$ ? Résoudre ce problème, c'est adapter l'impédance de la source et de la charge. Une façon de le faire est d'insérer entre la source et la charge un transformateur de rapport de transformation adaptée. L'utilisation d'un transformateur à secondaire variable permet de réaliser simplement cette adaptation.
> Réalisons le montage de [[#^figure50|figure 50]], où la résistance $R_2$ du rhéostat reste toujours inférieure à $R_1$.
> Faisons varier progressivement le rapport de transformation du transformateur en prenant soin de ne pas dépasser les intensités maximales autorisées dans les résistances. La puissance indiquée par le wattmètre passe par un maximum pour une valeur $m_0$ du rapport de transformation.
> Cette valeur n'étant pas connue, nous l'obtenons par une mesure à vide du rapport des tensions secondaire et primaire du transformateur.
> En réalisant les mesures correspondant à différentes valeurs de $R_2$, nous pouvons vérifier que $m_{0}^{2}$ est sensiblement égal à $\frac{R_2}{R_1}$ si le courant au primaire est grand devant le courant à vide du transformateur.
> Interprétons ce résultat.
> Si le courant au primaire est grand devant le courant à vide et les pertes négligeables, le transformateur peut être assimilé à un transformateur parfait.
> Le dipôle équivalent au générateur et la source, vu du secondaire, est alors un générateur de f.e.m. $mE$ et de résistance interne $m^{2}R_1$. La puissance dissipée dans $R_2$ vaut : $\mathcal{P}_2 = \frac{U_{2}^{2}}{R_2} = \frac{1}{R_2}\left(\frac{R_2mE}{m^{2}R_1 + R_2}\right)^{2} = \frac{1}{R_2}\left(\frac{R_2E}{mR_1 + \frac{R_2}{m}}\right)^{2}$.
> $\mathcal{P}_2$ est maximale si $mR_1 + \frac{R_2}{m}$ est minimal, soit : $R_1 - \frac{R_2}{m^{2}} = 0$ ou $m^{2} = m_{0}^{2} = \frac{R_2}{R_1}$.
> Remarquons que si $R_2$ était supérieure à $R_1$, l'adaptation d'impédance nécessiterait un transformateur survolteur $(m > 1)$.
# Diagrammes
Adaptation de la sortie à la charge
![[electronique2/attachments-electronique2/figure163.png]]^figure1

Transformateur d'isolement. Système dit à "double isolation"
![[electronique2/attachments-electronique2/figure164.png]]^figure2

Circuit magnétique torique
![[electronique2/attachments-electronique2/figure168.png]]^figure6

Deux contours $\Gamma_1$ et $\Gamma_2$
![[electronique2/attachments-electronique2/figure169.png]]^figure7

Circuit magnétique et lignes de champ $\overrightarrow{B}$. Le circuit magnétique est un tube de champ
![[electronique2/attachments-electronique2/figure170.png]]^figure8

Transformateur torique
![[electronique2/attachments-electronique2/figure171.png]]^figure9

Orientation des circuits. Mise en évidence des bornes homologues et de la convention d'orientation des intensités
![[electronique2/attachments-electronique2/figure172.png]]^figure10

Ligne de champ dans le circuit magnétique
![[electronique2/attachments-electronique2/figure173.png]]^figure11

Canalisation des lignes de champ magnétique
![[electronique2/attachments-electronique2/figure174.png]]^figure12

Courants et tensions
![[electronique2/attachments-electronique2/figure176.png]]^figure14

Représentations symboliques du transformateur parfait
![[electronique2/attachments-electronique2/figure178.png]]^figure16

Transfert d'impédance
![[electronique2/attachments-electronique2/figure179.png]]^figure17

Transfert de la source
![[electronique2/attachments-electronique2/figure180.png]]^figure18

Ligne de champ de fuite
![[electronique2/attachments-electronique2/figure181.png]]^figure19

Modèle du transformateur réel
![[electronique2/attachments-electronique2/figure182.png]]^figure20

Modèle du transformateur réel avec inductances de fuite et résistances des bobinages ramenées au primaire
![[electronique2/attachments-electronique2/figure183.png]]^figure21

Modèle du transformateur réel avec inductances de fuite et résistances des bobinages ramenées au secondaire
![[electronique2/attachments-electronique2/figure184.png]]^figure22

Modèle non linéaire d'un transformateur réel
![[electronique2/attachments-electronique2/figure185.png]]^figure23

Pour visualiser sur un oscilloscope l'intensité et la tension au primaire, il faut relier un transformateur d'isolement
![[electronique2/attachments-electronique2/figure186.png]]^figure24

Transformateur torique
![[electronique2/attachments-electronique2/figure188.png]]^figure26

Tracé du cycle d'hystérésis à l'oscilloscope
![[electronique2/attachments-electronique2/figure189.png]]^figure27

Un transformateur d'isolement et un autotransformateur peuvent remplacer le transformateur à secondaire variable
![[electronique2/attachments-electronique2/figure190.png]]^figure28

Un autotransformateur : a. Réalisation ; b. Schéma. Le circuit primaire correspond à la totalité des spires entre 1 et 2, et le secondaire aux spires comprises entre le curseur 3 et la borne 2
![[electronique2/attachments-electronique2/figure191.png]]^figure29

Un intégrateur à A.O. peut remplacer le circuit (R, C). Il présente l'avantage d'une impédance de sortie faible. R' doit être choisie en fonction de la tension au secondaire du transformateur
![[electronique2/attachments-electronique2/figure192.png]]^figure30

Entrefer dans un transformateur démontable. Les tôles du circuit ne sont pas parfaitement jointives
![[electronique2/attachments-electronique2/figure194.png]]^figure32

Représentation symbolique du wattmètre
![[electronique2/attachments-electronique2/figure198.png]]^figure38

Montages amont et aval. a. Montage amont ou longue dérivation. Le circuit tension est en amont du circuit intensité. b. Montage aval ou courte dérivation. Le circuit tension est en aval du circuit intensité
![[electronique2/attachments-electronique2/figure199.png]]^figure39

Étude à vide. L'ampèremètre $A_1$ mesure $I_{1V}$, le voltmètre $V_1$ mesure $U_{1V}$, le voltmètre $V_2$ mesure $U_{2V}$ ; le wattmètre mesure $\mathcal{P}_{1V}$
![[electronique2/attachments-electronique2/figure202.png]]^figure40

Étude en court-circuit. L'ampèremètre $A_1$ mesure $I_{1\,cc}$, l'ampèremètre $A_1$ mesure $I_{1\,cc}$, $A_2$ mesure $I_{2\,cc}$ ; le wattmètre mesure $\mathcal{P}_{1\,cc}$
![[electronique2/attachments-electronique2/figure205.png]]^figure43

Modèle linéaire du transformateur avec inductances de fuite et résistances des bobinages ramenées au secondaire
![[electronique2/attachments-electronique2/figure208.png]]^figure46

Étude en charge
![[electronique2/attachments-electronique2/figure209.png]]^figure47

Montage adaptateur d'impédance
![[electronique2/attachments-electronique2/figure212.png]]^figure50
# Graphiques
a. Transformateur basse tension. b. Transformateur haute tension 400-225 kV à la centrale nucléaire de Civaux
![[electronique2/attachments-electronique2/figure165.png]]^figure3

Transformateur expérimental
![[electronique2/attachments-electronique2/figure166.png]]^figure4

Cycle d'hystérésis. a. Milieu doux. b. Milieu dur
![[electronique2/attachments-electronique2/figure167.png]]^figure5

Cycle d'hystérésis. Le flux commun est choisi sinusoïdal, ce qui est le cas si la tension d'alimentation est sinusoïdale et la chute de tension ohmique négligeable
![[electronique2/attachments-electronique2/figure175.png]]^figure13

a. Recherche des bornes homologues avec un oscilloscope. b. Les bornes p et q sont homologues. c. Les bornes p et q ne sont pas homologues
![[electronique2/attachments-electronique2/figure177.png]]^figure15

Intensité et tension au primaire d'un transformateur
![[electronique2/attachments-electronique2/figure187.png]]^figure25

Cycles d'hystérésis. $u_C = 1 V$ correspond environ à $B = 1 T$ et $R_0i_1 = 0,5 V$ à $H = 100 A . m^{-1}$
![[electronique2/attachments-electronique2/figure193.png]]^figure31

Effets d'une modification de l'entrefer. a. Cycle sans entrefer. b. Cycle avec un entrefer de 0,1 mm (soit une feuille de papier)
![[electronique2/attachments-electronique2/figure195.png]]^figure33

Saturation. Ici $H_C \approx 150 A . m^{-1}$ ; $B_r \approx 1 T$ et $B_{sat} \approx 1,8 T$. Nous avons toujours : $u_C = 1 V$ qui correspond à environ $B = 1 T$ et $R_0i_1 = 0,5 V$ à $H = 100 A . m^{-1}$
![[electronique2/attachments-electronique2/figure196.png]]^figure34

Enchevêtrement des tôles de la carcasse. L'enchevêtrement des tôles limite les courants de Foucault sans créer d'entrefer important. L'isolant entre les tôles fait que la section effective du matériau magnétique est différente de la section de la carcasse. Le rapport de ces deux termes est le **foisonnement** du circuit magnétique (de l'ordre de 0,9)
![[electronique2/attachments-electronique2/figure197.png]]^figure35

Wattmètre analogique
![[electronique2/attachments-electronique2/figure201.png]]^figure36

Wattmètre électronique
![[electronique2/attachments-electronique2/figure200.png]]^figure37

Exemples de mesures
![[electronique2/attachments-electronique2/figure203.png]]^figure41

Puissance à vide en fonction de $U_{1}^{2}$
![[electronique2/attachments-electronique2/figure204.png]]^figure42

Exemple de mesures
![[electronique2/attachments-electronique2/figure206.png]]^figure44

Puissance en court-circuit en fonction de $I_{2\,cc}^{2}$
![[electronique2/attachments-electronique2/figure207.png]]^figure45

Mesure et exploitation de ces mesures
![[electronique2/attachments-electronique2/figure210.png]]^figure48

Exemple de courbe en fonction de l'intensité au secondaire. a. Tension au secondaire. b. Intensité au primaire. c. Rapports de transformateur : $m = \frac{U_2}{U_1}$ et $x = \frac{I_1}{I_2}$. d. Rendement
![[electronique2/attachments-electronique2/figure211.png]]^figure49
# Expériences
> [!warning]
> Voici des exemples de travaux pratiques qui abordent le sujet de ce chapitre : [lien 1](http://archive.univ-biskra.dz/moodle2023/pluginfile.php/661596/mod_resource/content/1/TP%20Electrotechnique%20Fondamentale%202.pdf), [lien 2](https://num.univ-biskra.dz/psp/exams/NjA4MjAyNC0wNi0yNSAxMTowNDoxMA==), [lien 3](https://www.ummto.dz/fs/wp-content/uploads/2022/02/Polycopie-de-TP-delectricite-SM.pdf), [lien 4](https://www.lias-lab.fr/perso/olivierbachelier/reserve_docs/TP_Elec2_MP.pdf), [lien 5](https://fr.scribd.com/document/700860453/TP-transfo), [lien 6](https://thesis.essa-tlemcen.dz/bitstream/handle/STDB_UNAM/398/TP%204%20%20le%20transformateur%20monophas%c3%a9.pdf?sequence=3&isAllowed=y).
# Autres notes
> [!warning] Application 1 page 215
> ![[electronique2/attachments-electronique2/figure162.png]]

> [!warning] Conditions nominales d'utilisation
> Les grandeurs nominales correspondent aux valeurs des paramètres (tension, courant, ...) dans les conditions d'utilisation optimales du transformateur, pour lesquelles il a été construit.
^def1
