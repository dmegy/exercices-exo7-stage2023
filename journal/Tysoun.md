# Journal

## Date (chronologique inverse)

remarques etc.

Possibilité de mettre des screenshots : la syntaxe est :

![description](img/screenshot.png)

Si vous avez juste un peu de code à mettre, n'utilsez pas de screenshots, écrivez le code au format texte, comme ceci :

```javascript
const myArray = [];
```

On peut aussi inliner du `code` dans un paragraphe.

Et on peut mettre des liens cliquables, par exemple
[Syntaxe basique en markdown](https://www.markdownguide.org/basic-syntax/)

## 28 avril

Correction de la planche-extract-latex-manuel.html :

- selection utilisateur pour "Ouvrir avec overleaf"
- nom explicites pour fichiers sauvegardés
- historique (le pushState devien replaceState)
- titre doc ajouter
- ajout des vérifications du formulaire

## 27 avril

planche-extract-latex-manuel.html terminer.
![Interface proposé pour la planche](img/planche-extract-latex-manuel.png)

## 26 avril

L'exportation en LaTeX via github est complet (avec préambule + options utilisateurs), le LaTeX retourné est maintenant compilable.

## 25 avril

Début de l'implémentation de l'exportation en LaTeX via github (préambule).

## 24 avril

Le fetch avec les données de l'API, provoque une erreur de protocole avec le serveur.

## 21 avril

Objectif :
Sauvegarde des exos sur le disque format PDF
Planche fetch via extract5.php

Problème rencontré :
Pour la sauvegarde des exos sous format PDF, il faut récupérer la feuille d'exo de l'API ou bien convertir le latex du github ?
Le fetch de extract5.php pose des difficultés (pas de docs ?)

## 20 avril

Objectif :
Afficher correctement les exos par mail
Ajouter bouton ouvrir dans overleaf (DM : pas tt de suite je pense : voir d'abord ce que j'ai envoyé sur Teams : au lieu d'ouvrir le php dans un nouvel onglet, fetch et récupération de ce qui arrive pour affichage/sauvegarde)
Ajouter un bouton source des exos seuls qui va afficher la liste des exos concaténés dans un nouvel onglet

Synthèse :
Ajout de deux boutons, un pour visualiser le code LaTeX des exos et l'autre pour sauvegarder ce code
Amélioration du style de la page.

## A terminer : bouton pour sauvegarder le fichier pdf

## 19 avril

Objectif :
-1) et 2) mentionné le 18/04
Problème rencontrés :
-Ajouter la page en favoris avec un bouton, varie en les navigateurs utilisés
-Partager la planche, mailto à l'air d'être bloquer/le webmail ne s'ouvre pas (DM : ça marche chez moi : il faut juste que l'utilisateur ait un client mail installé, ou bien un onglet de webmail à qui il a donné l'autorisation d'intercepter les actions "mailto". On peut considérer que c'est ok)
Synthèse :
Le bouton ajouter la page en favoris pour résoudre le problème des différentes navigateurs lorsque l'utilisateur cliquera sur ajouter en favoris un pop up lui demandera d'exécuter le shortcut "Ctr+D". (DM : ok, on met juste le texte explicatif "Il est également possible de metre en favori ..."
Le bouton de partager la planche via mailto, il faut obligatoirement que l'utilisateur ai définie un webmail par défaut dans son navigateur.

    Fonction qui affiche correctement les exercices n'est pas encore propre.

## 18 avril

planceURLDynnamique.html presque finie, le champ permaLien ici :  
"https://phil1010.github.io/exercices-exo7/plancheURLDynamique.html?liste=6&titre=5&hautgauche=1&hautdroite=2&basgauche=3&basdroite=4"
peut être copier et coller dans une autre fenêtre, l'utilisateur retrouve les mêms informations saisis (hg,hd,bg,bd,titre).
Il faut encore la mise à jour URL pour les favoris.
Problème actuelle : "http://localhost/https://phil1010.github.io/exercices-exo7/plancheURLDynamique.html?liste=6&titre=5&hautgauche=1&hautdroite=2&basgauche=3&basdroite=4". L'URL générer contient une première partie qu'il faut split (pareil que pour le github : "https://phil1010.github.io/https://phil1010.github.io/exercices-exo7/plancheURLDynamique.html?liste=6&titre=5&hautgauche=1&hautdroite=2&basgauche=3&basdroite=4").
Solution (du coup en décrivant clairement le problème c'est pas si compliqué) : séparer avec une regex les deux liens

## 17 avril

Création index.html + début de la première planche sans overLeaf.
