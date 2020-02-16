Ahora veremos las siguientes expresiones regulares. Recuerda que en el *step 1* están las expresiones regulares más importantes.

* `[aeiou]` - cualquier vocal en minúsculas.

`printf "ae a b ab j e io o" | egrep --color '[aeiou]'`{{ execute }}

* `[^aeiou]` - cualquier carácter excepto las vocales en minúsculas.

`printf "ae a b ab j e io o" | egrep --color '[aeiou]'`{{ execute }}

* `[aeiou^]` y `[a^eiou]` - cualquier vocal en minúsculas o el acento circunflejo `^`.

`printf "ae a b ^^ ab j e io o ^" | egrep --color '[a^eiou]'`{{ execute }}

* `[a-z]{4,6}` - Entre 4 y 6 letras minúsculas consecutivas. Se pone entre `{` y `}` el mı́nimo y máximo de veces que se puede repetir lo anterior. En cambio, con expresiones regulares antiguas sería `[a-z]\{4,6\}` - Entre 4 y 6 letras minúsculas consecutivas. Se pone entre `\{` y `\}` el mı́nimo y máximo de veces que se puede repetir lo anterior.

`printf "aaaa aaaaaa aaaa aa aaaa aaaaaaaaa" | egrep --color '[a-z]{4,6}'`{{ execute }}

* `[a-z]\{7\}` - 7 letras minúsculas consecutivas.

`printf "aaaa aaaaaa aaaa aa aaaa aaaaaaaaa" | egrep --color '[a-z]{7}'`{{ execute }}

* `[a-zA-Z0-9]*` - una secuencia (quiza vacı́a) de letras y cifras. Es parecida a un identificador del lenguaje pascal.

`printf "b8 bB8a a90 a|5 ab6 # a7b a77b b77c bb aa 7b abc8 8@9 - @" | egrep --color '[a-zA-Z0-9]*'`{{ execute }}

* `[a-zA-Z][a-zA-Z0-9]*` - Una letra seguida de cero o más letras o cifras. Ésta es la forma de los identificadores del lenguaje pascal.

`printf "b8 bB8a a90 a|5 ab6 # a7b a77b b77c bb aa 7b abc8 8@9 - @" | egrep --color '[a-zA-Z][a-zA-Z0-9]*'`{{ execute }}
