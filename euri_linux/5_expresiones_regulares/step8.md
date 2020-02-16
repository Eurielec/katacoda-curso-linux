**sed (stream editor)**

El programa `sed` es un editor no interactivo o editor de flujo. Que permite realizar transformaciones básicas de un flujo de entrada (un fichero o una entrada desde una tubería).

El formato (para substituciones) es el siguiente:

`sed [opciones] 's/REGEXP/reemplazo/flag' [fichero]`

Algunos comandos:
* `s` substitución
* `d` borrado
* `i\`, `a\`, añade antes/después de la línea afectada
* `c\` reemplaza la línea afectada

Algunas opciones:
* `-e` comando: añade comando
* `-i` edita el fichero in-place
* `-n` suprime la salida

Algunos flags:
* `g:` aplica los cambios globalmente (por defecto, sólo se cambia la primera aparición en cada línea)
* `p` imprime las líneas afectadas, incluso con la opción `-n`.
* `w fichero`: escribe las líneas con sustituciones al fichero indicado


**Importante recalcar que sed utilizar expresiones regulares antiguas**.

Un ejemplillo del uso de `sed`:

`printf "abajhbab" | sed -e "s/\(.\)\(.\)\1/X/g"`{{ execute }}
