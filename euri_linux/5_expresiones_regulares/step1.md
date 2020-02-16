Las expresiones regulares constituyen un lenguaje para describir tiras de caracteres.

Empezaron a usarse con ed, un editor orientado a lı́neas. Más tarde se incluyeron en otros comandos. Siguiendo una buena metodologı́a de programación, no estaban en el código de cada comando, sino en una biblioteca de funciones, y su comportamiento era el mismo para los distintos comandos.

En cierto momento se replantearon la funcionalidad de las expresiones regulares y surgió una variante. Llamaré a estos dialectos *expresiones regulares antiguas* y *expresiones regulares modernas*. Ambos dialectos comparten una serie de reglas.

**Parte común**

Válido para `grep`, `vi`, `sed`, `ed`, `more`, `egrep` y `awk`.

* `c` - Un carácter no especial vale por él mismo. Un carácter puede ser especial en expresiones regulares modernas, y no especial en expresiones regulares antiguas, por ejemplo `|`
*  `.` - cualquier carácter, excepto el cambio de lı́nea (ascii 10 decimal).
* `?` - Cero o una referencia del caracter previo.
* `*` - Representa cualquier string de caracteres
* `\$` - `\` **Cancela** significado de caracteres especiales. Este carácter, eslás inverso ( `\` ), es también carácter especial.
* `^` - **Inicio de lı́nea**, algo situado antes del primer carácter de una lı́nea.
* `$` - **Fin de lı́nea**, algo situado después del último carácter de una lı́nea.
* `[abz]` - **Alternativa de caracteres**. `a` o `b` o `z`. En general, cualquiera de los caracteres entre corchetes
* `[i-n01]` - **Alternativa**. Permite especificar rangos de caracteres. En este caso indica cualquier minúscula desde la `i` a la `n`, o la cifra `0`, o la cifra `1`.
* `[^a-zA-Z]` - **Cualquier carácter salvo los citados y el cambio de lı́nea**. El carácter `^` inmediatamente después de `[` indica complemento de los caracteres nombrados respecto del juego de caracteres sin el cambio de lı́nea. El carácter `^` en otra posición entre corchetes se representa a sı́ mismo.
* `a*` - **Cero o más repeticiones de a**. El asterisco indica cero o más repeticiones de lo inmediatamente anterior.

**Expresiones regulares antiguas**

Válido para `grep`, `vi`, `sed`, `ed`, y `more`.

* `\(a*b\)` - **Una (sub)expresión marcada en la que cero o más caracteres `a` van seguidos de un carácter `b`**. Las (sub)expresiones se marcan poniéndolas entre `\(` y `\)`.
* `\2` - **Referencia a la segunda (sub)expresión marcada**. Cuando hacemos una referencia a una expresión marcada estamos diciendo: ‘*lo mismo, exactamente lo mismo que antes*’.
* `\<` - **Comienzo de palabra, algo situado antes del primer carácter de una palabra**. Se considera palabra una secuencia de una o más letras, cifras y caracteres de subrayado. (Más que palabras me parecen identificadores del lenguaje *C*, o *awk*). Cada palabra incluirá el máximo de caracteres posibles.
* `\>` - **Fin de palabra**, algo situado después del último carácter de una palabra.
* `[a-z][a-z][a-z]` - Representa tres letras minúsculas cualesquiera.
* `\([a-z]\)\1\1` - Representa una letra minúscula repetida tres veces.

**Expresiones regulares modernas**

Válido para `egrep`, y `awk`

* `([ab]c)` - el paréntesis agrupa.
* `([0-9]_)*` - cero o más repeticiones de `[0-9]_` . En las expresiones regulares antiguas el asterisco sólo afectaba a un carácter o alternativa.
* `(bc)+` - una o más repeticiones de `bc`
* `[de]?` - cero o una vez lo anterior, es decir `d` o `e` o *nada*.
* `(a*)|(b*)` - alternativa: una secuencia de caracteres `a` , o una secuencia de caracteres `b` (incluyendo la secuencia vacı́a). En las expresiones regulares modernas el operador `*` tiene mayor prioridad que el operador `|` . La expresión anterior se puede escribir `a*|b*`
* `([a-z])\1\1` - Representa una letra minúscula repetida tres veces.
