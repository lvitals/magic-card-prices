# Magic the gathering pricer
## Description
Simple API that can look for MTG card prices through some websites.

Some sites are scrapped, others are fetched by their API.

Suggestions, fixes, issues or feature requests, feel free to fork and make a pull request or create an issue on this repository issue tracker.

## API documentation
Still in development

You can check for a card as
```
ENDPOINT/:from_where/card/:card_name
```

```:from_where``` can be
```
ligamagic
```
In the future I pretend to add some new websites.

```:card_name``` should be urlencoded (and spaced replaced by a + sign instead of %20)
```
Blood+Moon
```

E.g. ~~(This link doesn't really exists, just for explanation :) )~~
```
http://localhost:3000/ligamagic/card/Blood+Moon
```

The output will be something like that:
```
{
  "status": "ok",
  "data": {
    "card": "Blood Moon",
    "title": "Lua Sangrenta",
    "subtitle": "Blood Moon",
    "image": "http://magic.objects.liquidweb.services/en106mma.jpg",
    "rare": "Rara",
    "currencies": [
      "BRL"
    ],
    "sets": [
      "mma",
      "9e",
      "8e",
      "ch",
      "dk"
    ],
    "prices": {
      "mma": {
        "BRL": [
          "189.90",
          "199.60",
          "225.96"
        ]
      },
      "9e": {
        "BRL": [
          "179.99",
          "196.49",
          "211.09"
        ]
      },
      "8e": {
        "BRL": [
          "180.45",
          "194.82",
          "200.87"
        ]
      },
      "ch": {
        "BRL": [
          "169.90",
          "191.99",
          "219.95"
        ]
      },
      "dk": {
        "BRL": [
          "215.00",
          "215.00",
          "215.00"
        ]
      }
    },
    "url": "http://ligamagic.com.br/?view=cards%2Fsearch&card=Blood+Moon"
  }
}
```

~~Notice that the price still not being fetched.... yet!~~

## How to run
To run this project is pretty simple:
- sudo npm install nodemon -g
- npm install
- nodemon index.js
