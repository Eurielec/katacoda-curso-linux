Redirección de la entrada estándar

Si escribimos el comando `cat` *a secas*, nos redirige la entrada estándar a la salida estándar. Pruébalo

`cat`{{ execute }}

Para salir, podemos pulsar *Ctrl-D*. Es importante recalcar lo siguiente:
* *Ctrl-D* Le envia la señal *EOF* a la entrada estándar. Y el programa `cat` lo interpreta para salirse
* *Ctrl-C* Aborta la aplicación
* *Ctrl-Z* La lleva al *background*

Con el comportamiento del comando `cat` podemos ver lo siguiente:

`cat < listaDeLaCompra`{{ execute }}

Cómo vemos, podemos ver el contenido del fichero `listaDeLaCompra` utilizando una redirección (normalmente no utilizará así).

Ahora veremos el siguiente comportamiento:

`cat << END`{{ execute }}

Prueba a escribir Algunas cosas por la entrada estándar, y prueba ahora a escribir *END*. ¿Qué ocurre?
