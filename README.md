# Linux

Fundamentos del SO de Linux.

## Tabla de contenido
- [Lineas de comando](#lineas-de-comando).
 - [Interacción con archivos y carpetas](#interaccion-con-archivos-y-carpetas).
 - [Wildcards](#wildcards).
 - [Instalaciones](#instalaciones).
 - [Utilitaria](#utilitaria).

## Lineas de comando

### Interaccion con archivos y carpetas

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
| find | Buscar un archivo en un lugar especifico o por tamaño, nombre, byte, etc... |
| cat  | Ver un archivo que no tan pesado (que no proporcione desplazamiento). |
| tac | Para ver un archivo desde la última linea en adelante (backwards). |
| less | Para ver el contenido de un archivo pesado. Proporciona scroll-back y opciones de búsqueda. Se debe presionar `q` para salir de la lectura. |
| tail | Muestra las últimas 10 lineas del archivo. Para cambiar la cantidad de lineas a mostrar, se coloca `-n` donde n es la cantidad de lineas a mostrar. |
| head | Muestras las primeras tres lineas del archivo. También se puede usar `-n` para definir la cantidad  de lineas a mostrar. |
| touch | Crea un archivo. |
| mkdir | Crea una carpeta. | 
| rmdir | Borra una carpeta (solo si está vacía). |
| mv | Renombra un archivo. |
| rm | Eliminar un archivo. |
| rm -f | Forzar eliminación de un archivo. |
| rm -i | Eliminar archivo pero primero solicita confirmación del usuario. |
| rm -rf | Fozar la eliminación del directorio y todo su contenido del arbol de archivos y carpetas que tenga dentro. |


### Wildcards


| Wildcard | Descripción |
| ----- | ---- |
| ? | Coincidir con cualquier caracter individual de la búsqueda. |
| * | Coincidir con cualquier cadena de caracteres de la búsqueda. |
| [set] | Coincidir con cualquier caracter en un conjunto de caracteres. Por ejemplo, [adf] podría coincidir cualquier ocurrencia con "a", "d" o "f" |
| [!set] | Coincidir con cualquier caracter que no esté en el conjunto de caracteres especificados |


### Instalaciones

| Comando | Descripción |
| ----- | ---- |
| sudo apt-cache search NombrePaquete | Busca el paquete de instalación y muestra una información preliminar del paquete. |
| sudo apt-get install NombrePaquete | Instala el paquete. |
| sudo apt-cache policy NombrePaquete | Imprime el estatus del paquete. |
| sudo apt-get remove NombrePaquete | Elimina el paquete. |
| sudo dpkg -L | Lista todos los paquetes instalados. |
| sudo apt-get upgrade | Actualiza los paquetes que tengan actualizaciones disponibles. |

### Utilitaria

| Comando | Descripción |
| ----- | ---- |
| pipeline `$ command1 | command2 | command3` | Sirve para ejecutar diferentes comandos al mismo tiempo. |
| clear | Borra el historial de impresiones que tenga la consola. |
| df -Th | Muestra una estadísticas del uso de los archivos de sistema y su capacidad de espacio en disco. |
| ps | Produce una lista de los procesos junto con la información de estado del sistema. |
