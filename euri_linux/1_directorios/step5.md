El comando `cd` se puede controlar de diferentes formas:

* `pwd`{{ execute }} Muestra el directorio actual
* `cd .`{{ execute }} Se mueve al directorio actual, no se mueve
* `cd ..`{{ execute }} Se mueve al directorio que precede al actual
* `cd -`{{ execute }} Se mueve al directorio anterior
* `cd /`{{ execute }} Se mueve al directorio raíz
* `cd`{{ execute }} Se mueve a `/home/tu_usuario`
* `cd ∼`{{ execute }} Se mueve a `/home/tu_usuario`
* `cd ∼usuario2`{{ execute }} Se mueve a `/home/usuario2`

*Pss*

La mayoría de las shell de Linux tienen una opción implícita que autocompleta tanto el nombre del comando como las rutas que se vayan pasando como argumentos.

Simplemente pulsando el **tabulador** se completará y en el caso de que haya varias coincidencias, las mostrará por pantalla esperando a que se introduzca algún carácter más con el que poder seguir completando. **¡Pruébalo!**
