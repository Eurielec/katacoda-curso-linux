Vamos a ir repasando una a una algunas de las expresiones regulares más usadas.  Nos centraremos por ahora en las siguientes:

*  `.` - cualquier carácter, excepto el cambio de lı́nea (ascii 10 decimal).
* `?` - Cero o una referencia del caracter previo. **Se trata de una expresión regular moderna**.
* `*` - Representa cualquier string de caracteres

Cómo se trata de expresiones regulares modernas, utilizaremos `egrep`, la evolución de `grep`. A partir de este momento utilizaremos la opción de `egrep` para pintar los resultados, `--color`.

Podemos ver las diferencias de cada expresión regular con los siguientes ejemplos:

`printf "colour\ncolor\ncolouur\n" | egrep --color 'colou?r'`{{ execute }}

`printf "colour\ncolor\ncolouur\n" | egrep --color 'colou*r'`{{ execute }}

`printf "colour\ncolor\ncolouur\n" | egrep --color 'colo.r'`{{ execute }}

`printf "colour\ncolor\ncolouur\n" | egrep --color 'colou.r'`{{ execute }}

Las diferencias entre `?` y `.` pueden confundir un poco. Lo podemos ver mejor con el siguiente ejemplo:

`printf "error\neror\ner\n" | egrep --color 'er?or'`{{ execute }}

`printf "error\neror\ner\n" | egrep --color 'er*or'`{{ execute }}
