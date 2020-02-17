La herramienta `locate` realiza búsquedas en una base de datos de ficheros y directorios locales. Como podéis observar el resultado de esta orden nos devuelve el `path` absoluto de los ficheros o directorios que coinciden con el string que acompaña a la orden.

Veremos un par de ejemplos:

* `locate comoComunicarse.txt`{{execute}} Devolverá el path del fichero comoComunicarse.txt
* `locate *.txt`{{execute}} Devolverá todos los path de todos los ficheros que son notas de texto o .txt

También se puede emplear el sistema de pipes explicado anteriormente:
* `locate *.txt | grep c`{{execute}} En este caso nos devolverá los path de los ficheros .txt teniendo el patrón c (que contenga la letra c)
Quizás con el ejemplo anterior no le veas especial valor al uso de los pipes, pero si tienes que buscar por ejemplo toda la información sobre zip y que esté dentro del directorio bin es una herramienta muy útil ya que con la simple instrucción `locate zip | grep bin`{{execute}} obtendremos la ruta para acceder a los mismos

Es importante recalcar que la base de datos empleada por `locate` se crea y alcualiza con el programa `updatedb` y en la gran mayoría de distribuciones Linux ejecutan ese proceso una vez al día, pero como todo en Linux se puede ejecutar manualmente pero solo si tenemos permisos de root con `sudo updatedb`{{execute}}
