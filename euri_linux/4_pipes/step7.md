A la hora de ejecutar comandos, por defecto disponemos de tres "file streams"(o descriptores): **Entrada estándar** (standard input, standard in o stdin), **salida estándar** (standard output, standard out o stdout) y **salida de error estándar** (standard error o stderr). Usualmente stdin es el teclado y stdout y stderr se muestran en la terminal.

* `0` Entrada estándar (stdin)
* `1` Salida estándar (stdout)
* `2` Salida de errores estándar (stderr)

Si se desea redirigir stderr a otro fichero se debe emplear su descriptor de fichero (2), y el signo mayor que (« > »), seguido del nombre del fichero en el que se volcará stderr:

`ls -l /bin/bash /kaka > salida 2> error`{{ execute }}

Han aparecido dos ficheros, `salida` y `error` ¿Qué es cada uno?

Se puede emplear la notación 2>&1 para volcar stderr en el mismo fichero que stdout.

`ls -l /bin/bash /kaka > salida 2>&1`{{ execute }}

Bash implementa una notación simplificada de la instrucción anterior:

`ls -l /bin/bash /kaka >& salida`{{ execute }}
