Etude d'un algorithme de reconstruction par évolution de forme en tomographie par temps d'arrivée
=================================================================================================

Résumé
------

il s'agit, dans un premier temps, d'étudier de manière
théorique les propriétés de convergence d'un algorithme de
reconstruction tomographique par optimisation de forme (implanté à
l'aide de la technique des Level Sets), développé dans le cadre
d'une thèse récente. Dans un second temps, on cherchera à affiner
la dérivation de l'EDP d'évolution de forme employée dans cet
algorithme, voire à en proposer une alternative fondée sur
l'utilisation de la méthode de l'état adjoint, qui pourra être
intégrée dans l'algorithme de reconstruction.

 - Encadrant industriel : Pierre Charbonnier
 - Encadrant académique proposé : Zakaria Belhachmi


* Résumé étendu
---------------

Comme son nom l'indique, la reconstruction tomographique est un procédé qui
consiste à reconstruire des coupes d'un objet 2D ou 3D d'intérêt à partir de
mesures acquises autour de celui-ci. Dans la modalité d'imagerie qui nous
intéresse ici, on utilise comme données les temps de première arrivée d'une
onde ultra-sonore, en diverses positions de capteurs, et on cherche à
reconstituer une image scalaire qui correspond au champ de vitesse associé à
la propagation des ondes dans le milieu étudié. Ce type de méthode est
utilisé, par exemple, en géophysique ou en contrôle non destructif, pour
rechercher des objets enfouis ou des défauts.

Il s'agit d'un problème inverse mal posé qui nécessite donc
l'introduction de contraintes a priori permettant de régulariser la
solution. Dans notre cas, par exemple, on suppose que le champ de
vitesse est composée de deux régions de vitesse constante (un fond
et un objet à reconstruire), et que l'objet à reconstruire
appartient à un "dictionnaire" de formes de références, connues.

La reconstruction est rendue difficile par le caractère non
linéaire du problème direct associé : en effet, le trajet de
propagation des ondes, qui peut être déterminé par application du
principe de Fermat, dépend du champ de vitesse inconnu.

Dans le cadre de la thèse de Gil Gaullier (Laboratoires iCube et
ERA 27 IFSTTAR du Cerema, 2013), une méthode de reconstruction
originale, par évolution de forme, a été développée. A partir d'une
forme (champ de vitesse) initiale, l'algorithme proposé consiste à
alterner deux étapes, jusqu'à convergence :

 1. estimation des trajets de propagation des ondes à partir du
champ de vitesse courant (problème direct).

 2. optimisation des frontières de l'objet, de façon à minimiser
l'écart quadratique entre les temps mesurés et les temps calculés à
partir de la solution courante. De plus, on incorpore à ce critère
un terme a priori, qui contraint la forme en évolution à ressembler
à l'une des formes de référence. L'optimisation se fait grâce à la
méthode des Level-Sets (ensemble de niveaux).

Cet algorithme s'apparente, dans sa philosophie, à un algorithme de
point fixe. En pratique, sa convergence a toujours été observée.
Elle n'est toutefois pas démontrée théoriquement.

Le premier défi proposé est de faire le point de ce que l'on peut
établir mathématiquement sur la convergence d'un tel algorithme.

Le second objectif du projet est lié à l'étape 2 de l'algorithme.
Il s'agira d'en étudier la dérivation, en approfondissant plusieurs
points particuliers, et de proposer une alternative, fondée sur
l'utilisation de la méthode de l'état adjoint, qui pourra être
intégrée dans l'algorithme de reconstruction.

Référence
---------

 - Gil Gaullier, Modèles déformables contraints en reconstruction d'images de
tomographie non linéaire par temps d'arrivée, Thèse de doctorat, Université de
Strasbourg, septembre
2013.
