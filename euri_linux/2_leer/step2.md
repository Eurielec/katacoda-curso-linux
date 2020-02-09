No conviene que enviemos cualquier fichero a pantalla sin cuidado. Algunos ficheros pueden enviarse a pantalla sin preocuparse. Todos sus caracteres son imprimibles. Otros ficheros conviene no enviarlos directamente a pantalla. Tienen caracteres no imprimibles.

Si se envı́a a pantalla un fichero con caracteres no imprimibles puede suceder que lo que veamos no se corresponda con el contenido, puede que la pantalla quede en un modo tal que todo lo que venga a continuación sea ilegible, o puede que quede bloqueada. Nada de esto es irreversible, pero es bastante molesto.

`cat /bin/ls`{{ execute }}

Con el comando `file` podemos ver que tipo de archivo se trata sin tener que abrirlo.

Ahora ejecutaremos `file *`{{ execute }}

El intérprete de comandos toma la lı́nea `file *` y substituye `*` por todos los elementos en el directorio.

El comando file intenta determinar el tipo de los objetos cuyos nombres aparecen como parámetros. La mayor parte de las veces los nombres corresponden a ficheros. Empieza observando si el fichero tiene caracteres no imprimibles.

Cuando el fichero tiene caracteres no imprimibles estudia sus dos o cuatro primeros octetos. Si esos primeros octetos toman unos valores reconocidos, `file` indica el tipo de objeto asociado.
