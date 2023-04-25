# Journal

**17 avril :**
Création index.html + début de la première planche sans overLeaf.

**18 avril :**

COMMENTAIRES :

pour l'update du title, je propose que le title ait la forme suivante : "Feuille d'exercices Exo7 | [mon titre (celui écrti dans le champ de texte)] | Exercices no. [contenu du champ de texte avec la liste]" : ajouter la liste d'exercices permettra d'être plus explicite.

- pourquoi y at-il un bouton "mettre à jour l'URL et pourquoi renvoie-t-il vers l'API ?
- comme je disais, il faudrait que ça update la barre d'adresse en permanence, mais sans reload la page. On va scinder ça en deux tâches. J'aimerais donc:

  1. une page fonctionnelle et presque finale, avec le ccs materialize comme avant (mais mettre le link vers l'URL distante), aec le title qui update en permanence mais pas la barre d'adresse. En bas, il faudrait un bouton "copier l'adresse dans le presse-papier", et un bouton "mettre en favori" qui mette la bonne URL en favori, avec le bon title
  2. une deuxième version, qui update la barre d'URL en permanence. Ceci sera fait avec l'API History et Push State j(ai l'impresison qu'on ne peut pas faire autrement : j'ai juste googlé 'how to modify url without reloading". Cette deuxième version n'est pas prioritaire, sautez cette tâche pour l'instant.

- pas compris le truc avec la regex, je vais voir ça, on en reparle plus tard.

CONCLUSION : si tout va bien, on aura une première version qu'on peut embellir (je le ferai si besoin) puis pusher pour test en version réelle. Ensuite on passera à la suite, par exemple j'aimerais bien faire marcher l'ouverture sous overleaf, on verra si c'est possible.
planceURLDynnamique.html presque finie, le champ permaLien ici :  
"https://phil1010.github.io/exercices-exo7/plancheURLDynamique.html?liste=6&titre=5&hautgauche=1&hautdroite=2&basgauche=3&basdroite=4"
peut être copier et coller dans une autre fenêtre, l'utilisateur retrouve les mêms informations saisis (hg,hd,bg,bd,titre).
Il faut encore la mise à jour URL pour les favoris.
Problème actuelle : "http://localhost/https://phil1010.github.io/exercices-exo7/plancheURLDynamique.html?liste=6&titre=5&hautgauche=1&hautdroite=2&basgauche=3&basdroite=4". L'URL générer contient une première partie qu'il faut split (pareil que pour le github : "https://phil1010.github.io/https://phil1010.github.io/exercices-exo7/plancheURLDynamique.html?liste=6&titre=5&hautgauche=1&hautdroite=2&basgauche=3&basdroite=4").
Solution (du coup en décrivant clairement le problème c'est pas si compliqué) : séparer avec une regex les deux liens

**19 avril :**

Objectif :

-1. et 2. mentionné le 18/04
Problème rencontrés :

-Ajouter la page en favoris avec un bouton, varie en les navigateurs utilisés

-Partager la planche, mailto à l'air d'être bloquer/le webmail ne s'ouvre pas (DM : ça marche chez moi : il faut juste que l'utilisateur ait un client mail installé, ou bien un onglet de webmail à qui il a donné l'autorisation d'intercepter les actions "mailto". On peut considérer que c'est ok)

Synthèse :

Le bouton ajouter la page en favoris pour résoudre le problème des différentes navigateurs lorsque l'utilisateur cliquera sur ajouter en favoris un pop up lui demandera d'exécuter le shortcut "Ctr+D". (DM : ok, on met juste le texte explicatif "Il est également possible de metre en favori ..."
Le bouton de partager la planche via mailto, il faut obligatoirement que l'utilisateur ai définie un webmail par défaut dans son navigateur.
Fonction qui affiche correctement les exercices n'est pas encore propre.

**20 avril :**

Objectif :

Afficher correctement les exos par mail
Ajouter bouton ouvrir dans overleaf (DM : pas tt de suite je pense : voir d'abord ce que j'ai envoyé sur Teams : au lieu d'ouvrir le php dans un nouvel onglet, fetch et récupération de ce qui arrive pour affichage/sauvegarde)
Ajouter un bouton source des exos seuls qui va afficher la liste des exos concaténés dans un nouvel onglet

Synthèse :

Ajout de deux boutons, un pour visualiser le code LaTeX des exos et l'autre pour sauvegarder ce code
Amélioration du style de la page.
A terminer : bouton pour sauvegarder le fichier pdf

**21 avril :**

Objectif :
Sauvegarde des exos sur le disque format PDF
Planche fetch via extract5.php

Problème rencontré :
Pour la sauvegarde des exos sous format PDF, il faut récupérer la feuille d'exo de l'API ou bien convertir le latex du github ?
Le fetch de extract5.php pose des difficultés (pas de docs ?)

**24 avril :**

Le fetch avec les données de l'API, provoque une erreur de protocole avec le serveur.

**25 avril :**

Solution concernant extract5.php non trouvé...

**26 avril :**

Objectif : simuler le code LaTeX de l'API extract5.php

Concaténer le LaTeX complet des fiches d'exos via github (fiche complet des exos : préembule + les options sélectionnées par l'utilisateur).

Synthèse : version non fonctionnel, il manque les options sélectionnées par l'utilisateur.
