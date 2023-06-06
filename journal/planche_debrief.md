# Débrief de planche

## Du 17 avril au 28 avril implémentation de plusieurs version de planche pour arriver à plancheModif.html :

- planche.html => page souche
- planche URLDynamique.html => ajout l'URL dynamique
- planche-fetcht-latex-github.html => ajout récupération de code LaTeX de github et non plus extract5.php + sauvegarde sur le disque du code LaTeX.
- planche-extract-latex-manuel.html => ajout code LaTeX avec préambule
- plancheModif.html => ajout envoie par mail

Les cas particuliers lié à la saisie de l'utilisateur (entre des lettres dans la liste des question, le numéro entrer est supérieur au numéro max des exos, nombre de caractçre max dans les différents champs,...). Tout ces cas sont géré dans la dernière version plancheModif.html.

![Page de plancheModif.html](/journal/img/plancheModifPage.png)

## Du 02 mai au 23 mai bloquage sur la compilation LaTeX de texlive.js pour arriver à planche_preview.html, planche_preview_v2.html et planche_recherche.html.

Planche preview utilise encore extract5.php pour la fonctionnalité ouvrir le PDF, contrairement à la v2.

![Page de planche_preview.html](/journal/img/page_planche_preview.png)
Cette page utilise extract5.php pour afficher le PDF.

![Page de planche_preview_v2.html](/journal/img/page_planche_preview_v2.png)
Cette page prévisualise d'abord la page ensuite propose à l'utilisateur de télécharger cette page dans son disque.

![Page de planche_recherche.html](/journal/img/page_planche_recherche.png)
Cette page propose la fonctionnalitée de la recherche des exos comme http://exo7.emath.fr/search.php
