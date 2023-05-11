# Utilisation de fetch

Ici, les différentes syntaxes utilisées (await ou .then(), par exemple), leurs avantages à l'usage, dans différentes situations.

Problèmes rencontrés : faire plusieurs fetch d'un coup, ou alors à la suite

problèmes de cross-origin, façons de gérer ça ?

Par exemple il y a des options pour gérer les en-têtes, parfois

Exemples courts de fetch, de fichiers texte, de json etc, pour se rappeler la syntaxe.

## Fetch avec then

```javascript
fetch(url, options)
  .then((response) => response.json())
  .then((data) => console.log(data))
  .catch((error) => console.error(error));
```



## Fetch avec await

await permet d'attendre la résolution de la promesse avant de la renvoyer.

```javascript
async function fetchSomeData(url) {
  try {
    const response = await fetch(url);
    if (!response.ok) {
      throw new Error(`HTTP error! Status: ${response.status}`);
    }
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}
```

## avantages de l'usage avec await
  Code plus lisible (on utilise pas une chaine de ".then()") Surtout pour la gestion d'erreurs (try-catch au lieu de plusieurs catch)


## désavantages de l'usage avec await
  Seulement utilisable dans une fonction async.
  Peut bloquer l'exécution globale lorsqu'on veut faire plusieurs fetch d'un coup -> application potentiellement lente. D'où l'utilisation de Promise.all()


## fichiers utilisant .then
  exercice-fetch-23.html
  exercice-fetch-random.html


## fichiers utilisant await
  exercice-fetch-liste-en-dur.html
  exercice-fetch-liste-GET.html
  exercice-fetch-variable-GET.html