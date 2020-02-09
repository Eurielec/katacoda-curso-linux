Ejecutaremos el siguiente comando:

`cat > carta`{{ execute }}

Como hemos visto, cuando el comando `cat` no tiene parámetros copia la entrada estándar a la salida estándar.

Pero en este caso se está redirigido la entrada estándar al fichero `carta`.

Ahora vamos a repetir el comando, `cat > carta`{{ execute }}

Veremos que el fichero ha sido sobrescrito por la sentencia anterior, y ha desaparecido lo que teniamos previamente en `carta`.

`(date ; who) > quienyCuando`{{ execute }} redirige la salida de los comandos `date` y `who` al fichero `quienyCuando`.

La redirección afecta a los dos comandos porque están encerrados entre paréntesis. La salida de `who` va a continuación de la salida de `date`.

`(date ; who) >> quienyCuando`{{ execute }} redirige la salida de los comandos `date` y `who` al fichero `quienyCuando` escribiendo a continuación de lo que habı́a. Tenemos ası́ dos fechas y dos listas de sesiones.

Juntando todo lo que hemos aprendido de redirecciones:

`cat << END > entrada`{{ execute }}

¿Puedes juntar los contenidos de dos ficheros en otro?, sólo utilizando redirecciones (con el comando `cat` sin ningún parámetro).
