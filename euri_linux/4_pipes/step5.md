El comando `grep` busca un patrón en un fichero. Se podría utilizar con `grep Fruta listaDeLaCompra`{{ execute }}

Además, si no metemos ningún fichero al comando `grep`, buscará el patrón por la entrada estándar. Podremos utilizar el comando con el siguiente *pipe*

`cat sstv | grep MHz`{{ execute }}

Y con el uso de los muy útiles *pipes*, podemos contar el número de resultados de lo que estamos buscando con `wc`

`cat sstv | grep MHz | wc`{{ execute }}

Existe un comando para ordenar el contenido de un fichero y pasarlo por la entrada estándar, este es `sort`. En cambio `uniq -c` escribe cuántas veces se repite de forma consecutiva cada lı́nea.

Usando los pipes podríamos hacer lo siguiente:

`sort votos | uniq -c`{{ execute }}

Otra forma muy útil para usar los *pipes* es con el comando `history`, que nos imprime por pantalla el historial de comandos. Si se nos ha olvidado cómo utilizamos un comando en el pasado, podremos buscarlo con `grep`

`history | grep cat`{{ execute }}

Si tenemos la salida de un comando que es muy grande, podemos redirigirlo hacia el programa `less` que nos lo pondrá por pantalla de forma más ordenada:

`ls -l | less`

Luego, contamos con algunos filtros que hemos visto, como el de `head` o `tail`, que podremos utilizar con los *pipes*.

`cat comida | head -7`{{ execute }}

Ejercicio -> ¿Cómo se consigue que solo salga *leche* y *tomate* en la salida estándar?
