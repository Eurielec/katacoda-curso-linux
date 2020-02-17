En cambio la herramienta `find` es sumamente útil para buscar ficheros en un directorio concreto. Lo que esta sentencia hace es recorrer el árbol de directorios a partir de uno o varios directorios indicados (o en el que estamos por defecto).

Las diferentes formas de uso de este comando son las siguientes:

* `find`{{execute}} listará todos los ficheros del directorio actual y sus subdirectorios y como extensión si sentenciamos `find \dos`{{execute}} realizará lo mismo pero en el directorio 'dos'.
* `find -name xxx` solo listará los ficheros con el patrón xxx en su nombre, podemos hacer por ejemplo `find -name comoComunicarse.txt`{{execute}} y vemos que nos lista los ficheros que tengan comoComunicarse.txt como nombre. Una función interesante es el uso de *iname* en vez de *name*, ya que la primera es insensible a mayúsculas, encontrándonos un resultado para `find -name comocomunicarse.txt`{{execute}} no nos devolverá resultado, pero `find -iname comoComunicarse.txt`{{execute}} sí.
* `find -type x` opción muy útil ya que nos permite filtrar los resultados por tipos de fichero: `find -type d` {{execute}} nos devolverá los directorios, `find -type |` los enlaces simbólicos y la opción `find -type f` mostrará todos los ficheros corrientes.
* Obviamente también podremos hacer combinación de todas las instrucciones anteriores como: `find /dos -name como -type f`{{execute}}.
