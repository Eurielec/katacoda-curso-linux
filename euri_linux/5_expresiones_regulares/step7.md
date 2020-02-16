Si queremos utilizar el poder de las expresiones regulares con `ls` por ejemplo se haría así:

`ls | egrep '^a.txt'`{{ execute }} Busca ficheros que se llamen `a.txt`. En carácter `^` indica el inicio de linea.
`ls | egrep '^(a)(.)\1.txt'`{{ execute }} Busca ficheros que se llamen `a` seguido de un caracter y luego `a.txt`. Por ejemplo `aba.txt`

Crea algunos ficheros con diferentes nombres (usando el comando touch), y comprueba el uso de las expresiones regulares vistas anteriormente.

Psss... Que no termina ahí

Con las expresiones regulares podriamos eliminar ficheros que tienen un patrón en su nombre, utilizando pipes. Para eliminarlos sería con:

`ls | egrep '^a.txt' | xargs -d "\n" rm`{{ execute }}

Comprueba su uso
