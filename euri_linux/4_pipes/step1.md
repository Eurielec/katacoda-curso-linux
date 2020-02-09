El intérprete de comandos es quien normalmente se encarga de establecer la conexión entre la entrada y la salida estándar con los ficheros o con otros procesos. Se llama redirección a este cambio del origen y destino de las lecturas y escrituras. El usuario indica al intérprete de comandos las redirecciones que desea mediante unos convenios.

* `< fich1` hace que la entrada estándar sea `fich1`.
* `> fich2` hace que la salida estándar sea `fich2`. Si existe el fichero `fich2` se pierde su contenido previo. Si no existe el fichero, se crea.
* `>> fich2` hace que la salida estándar sea `fich2` . Si existe el fichero `fich2` no se pierde su contenido. Se escribe a continuación. Si no existe el fichero, se crea.
* `<< centinela` hace que la entrada estándar sean las lı́neas que vienen a continuación, terminando al encontrar *retornoDeCarro* centinela *retornoDeCarro*
* `com1 | com2` hace que la salida estándar de `com1` se lleve a la entrada estándar de `com2`. Esto se conoce como **pipe**
