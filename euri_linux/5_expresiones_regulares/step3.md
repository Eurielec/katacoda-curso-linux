Ahora vamos a ver las siguientes expresiones regulares:

* `\(a*b\)` - **Una (sub)expresión marcada en la que cero o más caracteres `a` van seguidos de un carácter `b`**. Las (sub)expresiones se marcan poniéndolas entre `\(` y `\)`. Con expresiones regulares modernas se marca con `(` y `)`.
* `\2` - **Referencia a la segunda (sub)expresión marcada**. Cuando hacemos una referencia a una expresión marcada estamos diciendo: ‘*lo mismo, exactamente lo mismo que antes*’.

Por lo que:

`p.p.` - da positivo si encuentra *pepa*
`\(p.\)\1` - no se ajusta *pepa*, y sı́ *pepe*, **utilizando expresiones regulares antiguas**
`(p.)\1` - no se ajusta *pepa*, y sı́ *pepe*, **utilizando expresiones regulares modernas**

Podriamos comprobar que:

`printf "pepe\npepa\npipo\npapa\npepo\n" | egrep --color 'p.p.'`{{ execute }}
`printf "pepe\npepa\npipo\npapa\npepo\n" | egrep --color '(p.)\1'`{{ execute }}
`printf "pepe\npepa\npipo\npapa\npepo\n" | grep --color '\(p.\)\1'`{{ execute }}


Ahora bien. Si imprimimos el siguiente fichero:

`printf "aa aba apa aabs abba baab bab"`

¿Cómo se haría para imprimir sólo `abba` y `baab`?

Se podría hacer con `printf "aa aba aabs abba baab bab" | egrep --color "(.)(.)\2\1"`{{execute}}
