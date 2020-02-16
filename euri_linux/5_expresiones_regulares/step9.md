**Substituciones con `vi` o `sed`**

Las expresiones regulares exploran las lı́neas de izquierda a derecha. Entre las secuencias situadas más a la izquierda seleccionan la más larga. Por ejemplo, en una lı́nea tenemos alababa y queremos substituir los caracteres entre una `a` y una `b` inclusive por una `X` . Hay cinco posibles secuencias. Más tarde imponemos que no haya ninguna b en medio de la secuencia a substituir. Hay tres posibles secuencias.

`echo 'alababa' > ersed`{{ execute }}

`sed -e 's/a.*b/X/' ersed`

`sed -e 's/a[^b]*b/X/' ersed`


---

Se pueden poner referencias a subexpresiones marcadas en la segunda parte (segundo parámetro) de una substitución.

`echo 'a8b a6c b8b a98b' > solomon`{{ execute }}

`sed -e 's/a\([0-9]*\)b/A\1B/g' solomon`{{ execute }} substituye la secuencia: un carácter `a`, seguido de cifras (o ninguna), seguido de un carácter `b` por un carácter `A`, seguido de esas mismas cifras seguido de un carácter `B` (todas las veces que lo encuentre).

Ahora escribiremos otro fichero para ver otro comportamiento de `sed`:

`echo 'estafania' > christopher`{{ execute }}
`sed -e 's/\([aeiou][aeiou]\)/\1\1/g' christopher`{{ execute }}

El comando anterior duplica el primer par de vocales (consecutivas) que encuentre en cada lı́nea.

Podemos ejecutar el siguiente comando unas cuantas veces y pasará algo muy gracioso `sed -e 's/\([aeiou][aeiou]\)/\1\1/g' christopher >> christopher`
