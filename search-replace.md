# Chercher et remplacer : expressions regex utiles

## Plusieurs espaces par une seule

- **Chercher :** `[ <NBSP>]{2,}`
- **Remplacer :** `une espace normale`

## Trois points (ou plus) consécutifs en ellipse

- **Chercher :** `\.{3,}`
- **Remplacer :** `…`

## Espace devant une double ponctuation en espace fine

- **Chercher :** `(\s(!|\?|:|;))`
- **Remplacer :** `<THSP>$2`

## Espace fine avant un pourcentage

- **Chercher :** `((\d)\s*%)`
- **Remplacer :** `$2<THSP>%`

## Nombre : séparateur des milliers

_Remarque : la règle englobe les dates et ne fonctionne pas pour les nombres qui ont déjà une espace normale comme séparateur des millers._

- **Chercher :** `\d{1,3}(?=(\d{3})+(?!\d))`
- **Remplacer :** `$&<NBSP>`

## Nombre avec décimale : virgule au lieu du point

- **Chercher :** `(\d)\.(\d)`
- **Remplacer :** `$1,$2`
