El *“path”* es el termino anglosajón empleado para describir la ruta a un fichero o directorio objetivo. Existen dos formas de identificar path:
* Path absoluto: Comienza en el directorio raíz y sigue el árbol de directorios rama por rama hasta alcanzar el directorio o fichero objetivo. Los paths absolutos siempre comienzan por /. Por ejemplo `cd /root/dos/otroDirectorio`{{ execute }}
* Path relativo: Comienza en el directorio actual de trabajo. Los paths relativos nunca comienzan por /. Por ejemplo `cd ~/dos/otroDirectorio`

Está permitido escribir múltiples barras oblicuas (`/` o *slash*) entre directorios y el fichero, el sis-
tema ignora los que hay en exceso. En resumen, `////usr//bin` es válido pues el sistema lo interpreta
como `/usr/bin`.

Con frecuencia es más cómodo emplear paths relativos pues requieren menos escritura. Su
principal ventaja es que disponemos de los siguientes atajos:

`.` Directorio actual
`..` Directorio padre del actual
`∼` Tu home (/home/tu_usuario)
`∼ usuario2` Home de usuario2 (/home/usuario2)

**Ejercicio** ->

Posicionate en `/root/dos/otroDirectorio`. Intenta ir a `/root/tres/casco`.

En principio hay 3 formas. Utilizando una ruta absoluta y utilizando ruta relativa con `~` o `../../`. ¿Hay alguna otra forma?
