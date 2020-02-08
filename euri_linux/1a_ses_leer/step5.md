**Para ver ficheros medianos o grandes**

Si enviamos a pantalla un fichero grande, las lı́neas vuelan, pasan ante nuestros ojos sin que seamos capaces de leerlas. Aunque vayan despacio es posible que queramos examinar con cuidado una fórmula, una sentencia (¿judicial?, ¿informática?), ...

Queremos que hasta que no digamos: - más - la salida de caracteres por pantalla se detenga y no se pierda información por la parte superior de la pantalla. Ese “más” da nombre al comando que nos ayudará: `more`

`more cripto_gpg.md`{{ execute }}

Cuando tecleamos un espacio blanco, `more` presenta casi una pantalla nueva. Si tecleamos retorno de carro el texto avanza una lı́nea. Si tecleamos *eslás* (/) el cursor baja a la última lı́nea. Los siguientes caracteres que tecleamos aparecen en la última lı́nea. Cuando damos retorno de carro, `more` busca la secuencia indicada en el texto no presentado. La pantalla presenta en una de sus primeras lı́neas la tira de caracteres buscada. Un espacio blanco o un retorno de carro al final del fichero acaba la sesión con el comando `more`. Otra forma de acabar la sesión es tecleando `q` (de quit).

`less` es un comando que admite todas las posibilidades de `more` y acepta además otros movimientos. Para no obligar al usuario a aprender nuevas asociaciones letra - movimiento, `less` toma los movimientos del editor vi y los obedece.

`less cripto_gpg.md`{{ execute }}

TODO: PONER COSAS DE LESS
