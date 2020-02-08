Una cosa cursiosa

El comando `echo` imprime por pantalla lo que ingresemos. Por ejemplo `echo HOLA Mundo o0`{{ execute }}.

Pero sucede una cosa curiosa si ejecutamos `echo *`{{ execute }}

Aquı́ hay algo extraño. Si echo repite los parámetros esperamos que escriba un asterisco (\*). ¿Por qué sucede esto?

La clave está en que ha intervenido el *intérprete de comandos*. El intérprete de comandos ha substituido el asterisco por la lista ordenada (según el código ascii) de nombres de objetos que no empiezan por punto. Luego, el intérprete de comandos ha llamado al programa echo pasándole como parámetros esa lista de nombres.
