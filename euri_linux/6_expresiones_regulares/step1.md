Regular expressions are a language for describing strings of characters.

They first came into use with ed, a line-oriented editor. Later they were included in other commands. Following good programming methodology, they were not in the code of each command, but in a library of functions, and their behaviour was the same for different commands.

At a certain point, the functionality of regular expressions was rethought and a variant emerged. I will call these dialects *old regular expressions* and *modern regular expressions*. Both dialects share a set of rules.

**Common part

Valid for `grep`, `vi`, `sed`, `ed`, `more`, `egrep` and `awk`.

* c` - A non-special character is valid by itself. A character can be special in modern regular expressions, and non-special in older regular expressions, e.g. `|`.
* `.` - any character except line shift (ascii 10 decimal).
* `?` - Zero or a reference to the previous character.
* `*` - Represents any character string.
* ``` - ``` **Cancels** the meaning of special characters. This character, the inverse ( ```` ), is also a special character.
* ``^` - **Start of line**, something before the first character of a line.
* `$` - **Line end**, something after the last character of a line.
* `[abz]` - **Alternate characters**. `a` or `b` or `z`. In general, any of the characters in square brackets.
* `[i-n01]` - **Alternative**. Allows character ranges to be specified. In this case it specifies any lower case letter from `i` to `n`, or the digit `0`, or the digit `1`.
* `[^a-zA-Z]` - **Any character except the quoted characters and the line shift**. The character `^` immediately following `[`[` indicates complement of the named characters with respect to the character set without the line shift. The `^` character in another bracketed position represents itself.
* a*` - **Zero or more repetitions of a**. The asterisk indicates zero or more repetitions of the immediately preceding.
Las expresiones regulares son un lenguaje para describir cadenas de caracteres.

Se utilizaron por primera vez con ed, un editor orientado a líneas. Más tarde se incluyeron en otros comandos. Siguiendo una buena metodología de programación, no estaban en el código de cada comando, sino en una biblioteca de funciones, y su comportamiento era el mismo para diferentes comandos.

En un momento dado, se replanteó la funcionalidad de las expresiones regulares y surgió una variante. Llamaré a estos dialectos *expresiones regulares antiguas* y *expresiones regulares modernas*. Ambos dialectos comparten un conjunto de reglas.

**Parte común

Válida para `grep`, `vi`, `sed`, `ed`, `more`, `egrep` y `awk`.

* c` - Un carácter no especial es válido por sí mismo. Un carácter puede ser especial en expresiones regulares modernas, y no especial en expresiones regulares antiguas, por ejemplo `|`.
* `.` - Cualquier carácter excepto desplazamiento de línea (ascii 10 decimal).
* `?` - Cero o una referencia al carácter anterior.
* `*` - Representa cualquier cadena de caracteres.
* ``` - ``` **Cancela** el significado de los caracteres especiales. Este carácter, el inverso ( ```` ), también es un carácter especial.
* ``^` - **Inicio de línea**, algo antes del primer carácter de una línea.
* `$` - **Final de línea**, algo después del último carácter de una línea.
* `[abz]` - **Caracteres alternativos**. `a` o `b` o `z`. En general, cualquiera de los caracteres entre corchetes.
* `[i-n01]` - **Caracteres alternativos**. Permite especificar rangos de caracteres. En este caso especifica cualquier letra minúscula de `i` a `n`, o el dígito `0`, o el dígito `1`.
* `[^a-zA-Z]` - **Cualquier carácter excepto los caracteres entrecomillados y el desplazamiento de línea**. El carácter `^` inmediatamente después de `[`[` indica el complemento de los caracteres nombrados con respecto al conjunto de caracteres sin el desplazamiento de línea. El carácter `^` en otra posición entre corchetes se representa a sí mismo.
* a*` - **Cero o más repeticiones de a**. El asterisco indica cero o más repeticiones del inmediatamente anterior.
