Ahora vamos a irnos a la ruta `/root/dos/libros` donde tendremos distintos ficheros.

`cd /root/dos/libros`{{ execute }}

Si listamos todos los ficheros en `/root/dos/libros` con `ls`{{ execute }} veremos que lo contienen algunos ficheros y un directorio.

En cambio, si los listamos con `ls -la`{{ execute }} veremos que tenemos ficheros *ocultos*.

Fíjate en las diferencias entre cada fichero, ¿Qué es cada cosa?

Los caracteres del principio de cada línea (e.g. «drwxr-xr-r») nos indican los permisos que tiene
cada archivo (la letra «d» indica que se trata de un directorio). Analicemos esta parte: si todos los
permisos estuviesen disponibles para todos los usuarios, tendríamos algo así:

`-rwxrwxrwx`

El carácter «r» significa que existe permiso de lectura (read), «w» permiso de escritura (write) y
«x» de ejecución. Los tres primeros caracteres indican los permisos que tiene el propietario; los tres
siguientes, los permisos del grupo; los tres últimos, los permisos del resto de usuarios. El quinto campo nos presenta el tamaño del objeto medido en caracteres. Los campos sexto, séptimo y octavo nos indican la fecha y hora de la última modificación del fichero.

Algunas versiones de ls presentan la fecha de última modificación con todo detalle cuando se pide con la opción `--full-time`

`ls -l --full-time`{{ execute }}

**¿Qué son los directorios `.` y `..`?**
