Corrélation d'image pour la mesure de champs de déplacements d'une surface entre un état de référence et un état déformé
========================================================================================================================

Résumé
------

La corrélation d'images permet de mesurer les champs de déplacements d'une
surface entre un état de référence et un état déformé à partir de deux images
acquises dans les deux états. La surface de l'objet doit être recouverte d'un
motif aléatoire qui peut être soit naturel (mousse, laine de verre, ...) soit
créé (peinture crayon, ...).

D’un point de vue mathématique, on suppose que les images dans deux états
différents de l’objet s’écrivent : f(x) et g(x) , où x représente les
coordonnées en pixel dans l’image.  Si on appelle : u(x) le champ de
déplacement entre les deux images, la conservation locale de la luminance
s’écrit :
`
g(x) = f (x + u(x))
`
Si l’on suppose que les images sont différentiables, un développement de Taylor au premier
ordre conduit à
`
g(x) = f (x) + u(x) .  \nabla f(x)
`
Le calcul du champ de déplacement revient à minimiser globalement le résidu de corrélation
défini par :
`
\int_\Omega (g(x) - (f(x)+u(x) . \nabla f(x)))^2
`


Actuellement, nous utilisons une décomposition de type éléments finis du champ
de déplacement, sous la forme `\sum_i u_i \phi_i` où les `\phi i` sont une
base de fonctions élémentaires polynomiales de degré 1 définies sur un
maillage rectangulaire de la surface de l’objet. Cette écriture permet de
ramener la minimisation de la fonctionnelle à la résolution d’un ensemble de
systèmes linéaires.

Nous utilisons un algorithme itératif basé sur une décomposition multi-échelles des images;
une estimation initiale avec une faible résolution spatiale est effectuée et progressivement ce
calcul est itéré en modifiant l’échelle d’analyse, c'est-à-dire en augmentant la résolution
spatiale et la précision du calcul.

### Objectifs

Le fait d'impliquer une continuité des éléments peuvent introduire des erreurs lors de la
reconstruction 3D, si l'objet n'est pas continu.

Pourrait on ne plus utiliser une décomposition de type éléments finis, mais
des fonctions qui ne forcent pas la continuité des éléments, ou de réaliser
une « vraie » corrélation d'images ?

Encadrants
----------

 - Industriels: Stéphanie Jaminion
 - Académtiques: Cornel Murea & Zakaria Belhachmi
