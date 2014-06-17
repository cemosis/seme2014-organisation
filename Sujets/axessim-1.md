Calcul de matrice d’impédance pour la simulation numérique des lignes de transmission multiples.
===============================================================================================

Résumé
------

## Problème Physique

On considère `N + 1` conducteurs (câbles et blindages) circulaires de rayon `ri`,
`i = 0···N`. Un conducteur entourant un ou plusieurs autres conducteurs est
appelé blindage. Le centre du conducteur wi est au point `Xi = (xi, yi)`. On
suppose que les conducteurs ne s’intersectent pas. On suppose que le
conducteur `w0` est un blindage qui entoure les autres conducteurs. Les
conducteurs sont perpendiculaires au plan `(x,y)` : le courant circule dans la
direction `z`. Lorsque des courants circulent dans les câbles, le modèle des
lignes de transmission per- met de calculer de façon approchée le couplage
entre les câbles. Ce modèle fait intervenir des équations différentielles sur
les courants et les tensions dans les conducteurs, dans la direction `z`, ainsi
que des matrices de couplages. Il est indis- pensable que ces matrices de
couplages respectent certaines propriétés physiques (positivité, par exemple),
sinon le modèle de transmission donnent rapidement des résultats complètement
faux.

## Cas des cables et des blindages

On considère maintenant la possibilité que certains conducteurs soient des
blin- dages qui entourent d’autres conducteurs. La présence d’un blindage
découple les EDPs entre l’intérieur et l’extérieur du blindage. Il faut
résoudre le problème précédent à l’intérieur du blindage. Il faut aussi
résoudre le problème précédent à l’extérieur du blindage, en considérant
celui-ci comme un unique conducteur. Pour calculer le courant du blindage, on
utilise la loi des noeuds. Pour calculer la tension on utilise la loi des
mailles. En procédant ainsi de l’intérieur vers l’ex- térieur, on peut
construire une matrice d’inductance globale prenant en compte tous les
conducteurs.  Malheureusement pour des raison numériques, cette matrices n’est
plus exacte- ment définie positive.

## Objectifs

Le but de la SEME est de chercher à identifier d’où vient le défaut de
positivité des matrices et à proposer une démarche pour résoudre ce problème.

Encadrants
----------

 - Encadrant industriel : Thomas Strub, C. Giraudon
 - Encadrant académique : Philippe Helluy

Documents
---------

 - plus d'informations dans ce [document](/Sujets/axessim1.pdf).
