Organisation de points dans des images
======================================

Résumé
------

HoloMap est une solution de mesure de forme d'objets dont la surface est réfléchissante
et peu rugueuse développée par Holo3 depuis 2002. Le principe général de mesure est la
déflectométrie (voir le document associé au sujet), c’est à dire l’observation d’une scène
connue par réflexion sur la surface à mesurer, l’image de la scène étant déformée par la
géométrie de la surface.

Une version d'HoloMap utilisant plusieurs caméras et plusieurs écrans est en cours de
développement. Elle a pour vocation de permettre la mesure de vitrages complexes (rayon de
courbure plus faibles que ceux que l'on pouvait mesurer jusqu' ici). L’image de la scène est
donc très déformée.

La scène observée est constituée d’un maillage régulier de marqueurs rectangulaires noirs
déposés sur une surface blanche constituée de morceaux de plans.

La mesure n’est possible que quand il est possible d’établir une correspondance entre le
marqueur (objet) et son image dans la vue caméra.

Plus la géométrie de la surface est complexe, plus l’organisation régulière des marqueurs est
perturbée dans la vue caméra.

C’est cette mise en correspondance que l’on souhaite améliorer.

Voici deux images illustrant tout cela

![Image1](/Images/holo3-2-img1.png) ![Image2](/Images/holo3-2-img2.png)

Encadrants
----------

 - Industriels: Vincent Chavidan
 - Académiques: Cornel Murea & Zakaria Belhachmi & Philippe Helluy

Documents
---------

 - plus de détails concernant le dispositif HoloMap sont disponibles [ici](/Sujets/holo3-2-hmap.pdf?raw=true)
