La filosofía de consola de Linux es tener muchos pequeños programas (comandos) que cooperan entre ellos para producir un resultado complejo, en detrimento de un único programa muy complejo y con muchas opciones y modos de operación. Los pipes se crearon con el fin de simplificar la colaboración entre estas aplicaciones; hacen posible puentear la salida estándar de un programa a la entrada estándar de otro.

Los pipes se señalan con una barra vertical (« `|` ») entre los comandos:

`command1 | command2 | command3`

La instrucción anterior representa un pipeline y permite combinar la acción de múltiples comandos en uno solo. Esto es extraordinariamente eficiente porque tanto command1 como command2 no tienen que esperar a que el programa anterior del pipeline termine su ejecución para empezar a procesar los datos que reciben por *stdin*. Dicho de otra manera los programas se ejecutan en paralelo y eso acelera el procesamiento en plataformas multinúcleo/multiprocesador. Además el proceso se realiza al vuelo, no hay necesidad de almacenar el resultado de cada programa del pipeline en un fichero temporal, esto ahorra espacio en disco y reduce las operaciones de lectura/escritura en disco, el cual acostumbra a ser el cuello de botella del ordenador.
