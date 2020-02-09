`touch` se emplea para establecer o actualizar las fechas de acceso o/y edición de un fichero. Por defecto resetea las fechas de acceso y edición a la fecha actual.

También es posible crear un fichero vacío empleando `touch`:

`touch myfile`{{ execute }}

Esto usualmente se realiza con el fin de crear un contenedor que posteriormente se llenará.

`touch` provee de múltiples opciones, pero he aquí la de interés: La opción `-t` permite modificar la fecha y hora de acceso y edición del fichero. El formato de fecha es el siguiente [[SS]AA]MMDDhhmm[.ss]

`touch -t 05200800 myfile`{{execute}}

Podremos ver la fecha del fichero con `ls -la`{{ execute }}
