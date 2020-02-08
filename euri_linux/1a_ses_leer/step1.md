Linux está provisto de comandos capaces de mostar el contenido de un fichero, crear un fichero o un fichero vacío, alterar los atriburos temporales (timestamp) de un fichero, y borrar o renombrar un fichero o directorio. Estos comandos, útiles en manejo de datos y ficheros, son los que posibilitan que los datos oportunos estén disponibles en una cierta localización. En esta sección se detalla todo lo relacionado con el manejo de ficheros.

Utilidades disponibles para visionar ficheros:
* `cat` Imprime el fichero entero en pantalla, se emplea para ficheros cortos pues no provee desplazamiento vertical
* `tac` Igual a cat salvo porque invierte el fichero linea a linea
* `less` Es un programa de visionado de documentos, se emplea en ficheros extensos pues dispone de desplazamiento, y funciones de búsqueda. Nota: Se emplea `/` para buscar un patrón hacia delante y `?` para buscarlo hacia atrás
* `tail` Imprime las últimas 10 lineas de un fichero, por defecto. Se puede alterar el número de lineas que muestra con, por ejemplo, `-n3` o `-3` para mostrar sólo 3 lineas.
* `head` El opuesto a tail, por defecto imprime las primeras 10 lineas
