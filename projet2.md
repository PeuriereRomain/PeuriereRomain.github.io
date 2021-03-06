---
title: Pipe runner 3D
subtitle: Jeu de type 'runner' sur un tuyau généré aléatoirement
layout: "page"
icon: fa-book
order: 3
---
<header>
<img class='image fit' src="assets/images/pipeRunner/bandeau.png" alt="pipe banner" />
</header>

Projet de M1 (2018).
<h3>Buts du projet: </h3>
* Implémenter un jeu de runner 'infini' avec un tuyau généré aléatoirement
* Implémenter les collisions

<p style="color:green">Code: C++ / Framework OpenGL - GLSL 3.3</p>

<div class="embedresize">
<div>
    <video width="560" height="315" controls>
    <source src="assets/video/pipeRunner.mp4" type="video/mp4">
    Your browser does not support the video tag.
    </video>
</div>
</div>
<br>
<hr>
<h3>Principe du jeu:</h3>
Obtenir un score maximal.<br>
Il est possible de tourner autour du tuyau (gauche et droite) pour éviter les obstacles.<br>
Chaque checkpoint (triple anneau jaune) rajoute un point.<br>
Le nombre d'obstacles par chunk (entre 2 checkpoints jaunes) augmente à chaque checkpoint passé.

Etapes obligatoires:
* Génération du tuyau
* Déplacement d'un objet autour de celui-ci
* Placement d'obstacles
* Calcul d'intersections avec ceux-ci

<p style="color:blue">Améliorations personnelles:</p>
* Ajout d'une cubemap
* Elements rotatifs (double-torus) suivant le tuyau (rajoute les obstacles au loin)
* Shader de reflexion/refraction + Blinn-Phong, calcul de critères de visibilité (fog, angle...)
* Modèle de B.Walter pour le halo de lumière du vaisseau
* Ajout d'affichages 2D (texte)
* Ajout d'un écran de démarrage, possibilité de relancer le jeu

<div style="text-align:center;">
<img class='image' src="assets/images/pipeRunner/pipe_start.png" alt="pipe start" />
<img class='image' src="assets/images/pipeRunner/pipe_end.png" alt="pipe end" /><br>

<img class='image' src="assets/images/pipeRunner/pipe3.png" alt="pipe mid1" />
<img class='image' src="assets/images/pipeRunner/pipe4.png" alt="pipe mid2" />
</div>

<br>

<img class='image' src="assets/images/pipeRunner/pipe1.png" alt="pipe mid3" />
<img class='image' src="assets/images/pipeRunner/pipe2.png" alt="pipe mid4" />
<img class='image' src="assets/images/pipeRunner/vaisseau.png" alt="spaceship" />

Génération du tuyau :
* Génération de points le long d'un vecteur aléatoirement altéré
* Calcul de la courbe par algorithme de Chaikin
* Calcul des normales et rotations des segments
* Génération du tube grâce aux normales

Vaisseau, checkpoints et double-torus (rajoutant les obstacles au loin) créés sous Blender.
