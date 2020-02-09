Para listar el contenido de un directorio se utiliza el comando `ls`{{ execute }}, que mostrará por pantalla los
archivos presentes en el directorio actual.

Para listar el contenido de una ruta específica se lo pasamos como argumento `ls /root/dos/libros`{{ execute }}

El comando `ls`, tiene diferentes opciones:
* Con `ls -l`{{ execute }} listamos los archivos mostrando su tamaño, permisos y propietario.
* con `ls -a`{{ execute}} Lista todos los ficheros, incluso los ocultos. Los ficheros que comiencen con «.» (e.g. .bashrc, .config) son archivos ocultos y son útiles cuando tenemos archivos que queremos que estén en un determinado sitio pero no queremos que se muestren de forma normal. Generalmente esto se hace para mejorar la lectura de los elementos del directorio.
* Con `ls -r`{{ execute }} Lista los archivos siguiendo el orden inverso al normal. Si no se especifica nada, el orden siempre es alfabético. Con la opción -t el orden del listado es la fecha de la última modificación.
