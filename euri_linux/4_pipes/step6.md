Comando `tee`

`who | tee tmp | wc -l | cat - tmp`{{ execute }}

Cuatro comandos trabajan en cadena. La salida de un comando sirve de entrada al siguiente.
* `who` describe las sesiones en el sistema.
* `tee tmp` saca dos copias de los caracteres que lee. Una copia va a la salida estándar, y la otra al fichero `tmp`.
* `wc -l` cuenta las lı́neas que le llegan.
* `cat - tmp` concatena lo que lee por la entrada estándar ( - ) con el fichero `tmp`.

El comando `tee` nos sirve para sacar dos copias de una información, una para su proceso inmediato.

Otro ejemplillo:

`cat votos | grep "nulo" | tee file2.txt | wc -l`{{ execute }}
