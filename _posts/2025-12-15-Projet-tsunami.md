---
layout: post
title: Projet réalisé dans le cadre de ma formation consistant au développement d'un algorithme itératif visant à établir la localisation de la source d'un tsunami.
category: projet
image: /images/RMStsunami.png
---

<p style="text-align: justify; font-size: 17px;">
L’objectif de ce programme est d’obtenir la position de la source d’un tsunami, sa date et
son heure. Pour cela, nous allons utiliser une base de données indiquant le profil bathymétrique
et une loi reliant la vitesse d’une vague à la profondeur des océans (comme décrit dans l’état
de l’art). Ainsi, nous avons à notre disposition une grille décrivant la bathymétrie et une liste
de positions (longitude, latitude) et d’heures d’arrivée de la vague.
Nous avons donc tout d’abord représenté cette grille bathymétrique et positionné nos villes
grâce à leurs positions latitudinales et longitudinales. Nos données sont donc des valeurs de
bathymétrie associées à chaque pas de 5 minutes d’arc de longitude et de latitude.
</p>

[Rapport complet au format pdf]({{ site.baseurl }}/fichiers/rapport_python.pdf)