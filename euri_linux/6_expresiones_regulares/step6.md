Tenemos las siguientes expresiones regules, que está bien remalcarlas otra vez:
* `.*` - cualquier tira de caracteres (incluyendo la tira vacı́a o de longitud nula).
* `..*` - cualquier tira de caracteres (con al menos un carácter).

Podemos ver ahora los siguientes ejemplos.

* `\([0-9]\)\1` - Un número capicúa de dos cifras.

`printf "989 9 898 22 33 678" | egrep --color '([0-9])\1'`{{ execute }}

* `(.)\1` - dos caracteres *consecutivos* iguales.

`printf "aa\nab\nabahgj\njj" | egrep --color '(.)\1'`{{ execute }}

* `\(.\).*\1` - dos caracteres repetidos.

`printf "aa\nab\nabahgj\njj\nahjkla" | egrep --color '(.).*\1'`{{ execute }}

* `(..*)\1` - dos secuencias repetidas y consecutivas

`printf "aaaa\naaabbaabb\nabahgj\njj" | egrep --color '(..*)\1'`{{ execute }}

* `(..*).*\1` - dos secuencias repetidas

`printf "aaaa\naaabbaabb\nabahgj\njj" | egrep --color '(..*).*\1'`{{ execute }}

¿Cómo se buscaría un número de 5 cifras capicua?
¿Cómo se haría con 5 letras capicua?
