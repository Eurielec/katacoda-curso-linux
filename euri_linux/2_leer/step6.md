**Para ver parte del contenido**

A veces sólo nos interesa ver las primeras lı́neas de un fichero (unas pocas) y no hace falta hacer `more` seguido de `q` que nos mostrarı́a las 22 primeras lı́neas.

`head -8 taller_ropa.txt`{{ execute }}

`head -3 taller_ropa.txt` nos muestra las 3 primeras lı́neas del fichero nombrado. `head` toma por omisión 10 lı́neas.

En cambio `tail -6 taller_ropa.txt`{{ execute }} nos muestra las 6 últimas lı́neas del fichero nombrado. `tail` toma por omisión 10 lı́neas.
