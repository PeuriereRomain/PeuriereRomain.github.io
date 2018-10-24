---
title: Shooter 3D
subtitle: Jeu de type 'shooter' en 3D avec génération aléatoire du terrain
layout: "page"
icon: fa-book
order: 6
---

<header>
<img class='image fit' src="assets/images/fightMILK/bandeau.png" alt="shooter banner" />
</header>

Projet de L3 (2017), binôme.
<h3>Buts du projet:</h3>
* Réaliser un jeu 3D avec génération aléatoire du terrain
* Implémenter le clipping par octree

<p style="color:green">Code: C / OpenGL 1</p>

<div class="embedresize">
<div>
    <video width="560" height="315" controls>
    <source src="assets/video/fm.mp4" type="video/mp4">
    Your browser does not support the video tag.
    </video>
</div>
</div>
<br>
<hr>
<h3>Principe du jeu:</h3>
Obtenir un score maximal.<br>
Un point par collision vaisseau-ennemi(dommageable) ou munition-ennemi, le jeu s'arrête quand le joueur n'a plus de vie.<br>
Le joueur doit atterrir pour ramasser d'autres munitions.<br>
<br>

<div style="text-align:center;">
Terrain aléatoire (et paramétrable), arbres destructibles.<br>
<img class='image' src="assets/images/fightMILK/fm3.png" alt="terrain1" />
<img class='image' src="assets/images/fightMILK/fm5.png" alt="terrain2" />
<img class='image' src="assets/images/fightMILK/fm7.png" alt="terrain3" /><br>
</div>
<br>
6 déplacements possibles:
* Tangage gauche - droite
* Monter - Descendre
* Tourner gauche - droite

* Accélérer - Décélérer

<div style="text-align:center;">
<img class='image' src="assets/images/fightMILK/fm2.png" alt="terrain start" />
<img class='image' src="assets/images/fightMILK/fm6.png" alt="terrain mid" />
</div>
<br>
Simulation de gravité: les munitions retombent, les ennemis touchés chutent, la vitesse augmente lorsqu'on se dirige vers le sol.

<div style="text-align:center;">
Implémentation du clipping des objets par octree (accentué ici pour être visible)<br>
<img class='image' src="assets/images/fightMILK/fm8.png" alt="octree" />
<img class='image' src="assets/images/fightMILK/fm9.png" alt="clipping" />
</div>
