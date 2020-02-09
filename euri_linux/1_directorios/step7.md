El comando `cd` recuerda su última posición, y te permite volver a ella empleando `cd -`. Para recordar directorios anteriores disponemos de `pushd`. Este comando además de movernos al directorio deseado (como lo haría `cd`), almacena el directorio anterior en una pila. Para volver al último directorio insertado en la citada pila disponemos de `popd`. La pila de directorios puede mostrarse usando el comando `dirs`.

Te puedes ir a `/root/tres/pedal` con `pushd /root/tres/pedal`{{ execute }}, luego moverte a `/root/uno` con `pushd /root/uno`{{ execute }}.

Ahora puedes listar tu cola de directorios con `dirs`{{ execute }}

Y volver a donde estabas con `popd`{{ execute }}

Ejercicio-

Muévete por el sistema de ficheros con `pushd` y `popd`.
