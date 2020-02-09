**Hard links y soft links**

Para explicar esta sección, vamos dirigirnos a otra carpeta con `cd /root/dos/libros`{{ execute }}

`ln` se emplea para crear **enlaces duros** (*hard links*) y (con el parámetro -s) **enlaces simbólicos** (*soft links* o *symlinks*). Estos dos tipos de enlace son muy útiles en sistemas UNIX.

Vamos a crear un **hard link** a `comoComunicarse.txt` que se llame `ComoHablar.txt`. Lo haremos así:

`ln comoComunicarse.txt ComoHablar.txt`

Empleando `ls`{{ execute }} se observa que se ha creado un segundo fichero igual al primero. Sin embargo un análisis más minucioso de ambos ficheros muestra que esto no es del todo cierto.

`ls -li comoComunicarse.txt ComoHablar.txt`{{ execute }}

La opción `-i` de `ls` muestra en la primera columna el número de inodo, el cual es único para cada objeto. Este campo es igual en ambos ficheros, de lo que se deduce que hay un único objeto pero con dos nombres de fichero asociados a este.

Por otra parte, tenemos los **soft links**, o enlaces simbólicos. Los enlaces simbólicos se crean con la opción -s :

`ln -s comoComunicarse.txt comoExpresarse.txt`{{ execute }}

¿De qué se trata un enlace simbólico?

`ls -li comoComunicarse.txt comoExpresarse.txt`{{ execute }}

Constatamos que `comoExpresarse.txt` no es un fichero normal, pues claramente apunta a `comoComunicarse.txt` y tiene diferente numeración de inodo.

Los **enlaces simbólicos** no ocupan espacio extra en el sistema de ficheros (a menos que su nombre sea muy largo). Son muy útiles pues pueden modificarse fácilmente para apuntar a diferentes ficheros. Una forma fácil de alcanzar paths largos desde tu directorio home empleando un acceso directo es crear un enlace simbólico.

A diferencia de los hard links, los **soft links** pueden apuntar a ficheros en otros sistemas de ficheros (o particiones). Éstos pueden estar o no disponibles en este momento o incluso no existir. En el caso de que un enlace apunte a un fichero actualmente no disponible o que no exista, se obtiene un enlace roto, muerto o huérfano (*broken*, *orphaned*, *dead*, or *dangling link*).

Ejercicio - Crea un enlace simbólico en el home para r al directorio `/root/dos/otroDirectorio` más rápidamente.

Los enlaces duros son muy útiles pues ahorran espacio en disco, pero conviene ser cauteloso a la hora de usarlos. La principal razón es que si borras fichero1 o fichero2 del ejemplo de la sección anterior, el inodo que apunta al objeto en disco (y su correspondiente nombre de fichero) se conservarán, esto puede dar lugar a consecuencias indeseables si se vuelve a crear el fichero con el mismo nombre.

¿Qué pasa si eliminas un *hard link*?¿Se eliminan los dos?¿Qué pasa si modificas uno?¿Y con los enlaces simbólicos?
