# Linux

Fundamentos del SO de Linux.

## Tabla de contenido
- [Lineas de comando](#lineas-de-comando).

## Lineas de comando

| Comando | Descripción |
| ----- | ---- |
| whereis nombreDeLaApp | Muestra la ruta de una app especifica. |
| which nombreDeLaApp | Muestra la ruta de una app especifica. |
| shutdown -h | -r | Configurar el apagado del sistema, con opción de dar un aviso a los demás en la red local. |
| pwd | Muestra la ruta donde estás ubicado actualmente. |
| cd | Cambiar de directorio. |
| cd .. | Cambiar al directorio padre de la carpeta actual. |
| cd / | Cambia al directorio raíz. |
| ls | Lista todas las carpetas de la ruta actual. |
| ls -a | Lista todas las carpetas de la ruta actual y también las que están ocultas. |
| tree | Muestra las carpetas del sistema en arbol. |
| locate nombreBusqueda | Buscar un archivo, caperta, etc... que contenga la cadena argumentada. Si no genera resultados, pruebe primer con `sudo updatedb` y realice de nuevo la búsqueda. |
| cp valorACopiar destino | Copiar y pegar en una ruta o en un archivo nuevo. |
| pipeline `$ command1 | command2 | command3` | Sirve para ejecutar diferentes comandos al mismo tiempo. |

| Wildcard | Descripción |
| ----- | ---- |
| ? | Coincidir con cualquier caracter individual de la búsqueda. |
| * | Coincidir con cualquier cadena de caracteres de la búsqueda. |
| [set] | Coincidir con cualquier caracter en un conjunto de caracteres. Por ejemplo, [adf] podría coincidir cualquier ocurrencia con "a", "d" o "f" |
| [!set] | Coincidir con cualquier caracter que no esté en el conjunto de caracteres especificados |
| find | Buscar un archivo en un lugar especifico o por tamaño, nombre, byte, etc... |
