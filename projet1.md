---
title: Visualisation de terrain
subtitle: Chargement et analyse d'une Heightmap pour la visualiser  
layout: "page"
icon: fa-book
order: 2
---
<header>
<img class='image fit' src="assets/images/terrain/bandeau.png" alt="terrain banner" />
</header>

Projet de M2 (2018).
<h3>Buts du projet: (En cours)</h3>
* Manipuler le pipeline OpenGL
* Voxelliser un terrain et l'analyser pour une visualisation adaptée

<p style="color:green">Code: C++ / OpenGL - GLSL 3.3 </p>
<hr>
<br>
Etapes:
* Découper le terrain en régions
* Clipping des régions non visibles
* Analyse et tri par -matière- (texture) suivant certains critères (pente, hauteur...)
* Affichage par matière, régions
* Calcul et affichage de la shadowMap
* Modèle de l'eau

<div style="text-align:center;">
Affichage par régions et calcul de la shadowMap<br>
<img class='image' src="assets/images/terrain/terrainregions.png" alt="regions" />
<img class='image' src="assets/images/terrain/terrainshadow.png" alt="shadowmap" />
</div>
<br>
<div style="text-align:center;">
Tri et affichage par matières (textures) <br>
<img class='image' src="assets/images/terrain/terrainmat1.png" alt="matiere1" />
<img class='image' src="assets/images/terrain/terrainmat2.png" alt="matiere2" /><br>
<img class='image' src="assets/images/terrain/terrainmat3.png" alt="matiere3" />
<img class='image' src="assets/images/terrain/terrainmattot.png" alt="total matieres" />
</div>
<br>
<p style="text-align:center;">Application de réflexion/refraction (Fresnel effect), dudv map et normal map pour la distortion.</p>
<div class="embedresize">
<div>
    <video width="560" height="315" controls>
    <source src="assets/video/water.mp4" type="video/mp4">
    Your browser does not support the video tag.
    </video>
</div>
</div>
<br>

Etapes futures:
* Modèle de lumière différent par matière (shader)
* Ajout d'éléments dans le terrain (textures billboard)
* Ajout d'une cubemap
* Optimisation GL4+
