# Linux

Fundamentos del SO de Linux.

## Tabla de contenido
- [Lineas de comando](#lineas-de-comando).
 - [Interacción con archivos y carpetas](#interaccion-con-archivos-y-carpetas).
 - [Wildcards](#wildcards).
 - [Instalaciones](#instalaciones).
 - [Comprensión de archivos](#Compresion-de-archivos).
 - [Utilitaria](#utilitaria).
- [Directorios](#directorios).

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
| diff | Compara archivos o carpetas |
| diff -c | Proporciona una lista de las diferencias que se compone de 3 líneas de contexto antes y después de las líneas que difieren en contenido. |
| diff -r | Se utiliza para comparar recursivamente los subdirectorios, así como el directorio actual. |
| diff -i | Ignorar el caso de las letras. |
| diff -w | Ignorar la diferencia de espacios y tab.
| diff `<filename1> <filename2>` | Comparar dos archivos. |
| diff3 MY-FILE COMMON-FILE YOUR-FILE | Compara tres archivos al mismo tiempo. |



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

### Compresion de archivos

| Comando | Descripción |
| ----- | ---- |
| gzip | La utilidad de compresión más utilizado en Linux |
| bzip2 | Produce archivos significativamente menores que los producidos por gzip. |
| xz | La utilidad de compresión eficiente el espacio más utilizado en Linux. |
| zip | A menudo se requiere para examinar y descomprimir archivos de otros sistemas operativos. |


### Utilitaria

| Comando | Descripción |
| ----- | ---- |
| pipeline `$ command1 | command2 | command3` | Sirve para ejecutar diferentes comandos al mismo tiempo. |
| clear | Borra el historial de impresiones que tenga la consola. |
| df -Th | Muestra una estadísticas del uso de los archivos de sistema y su capacidad de espacio en disco. |
| ps | Produce una lista de los procesos junto con la información de estado del sistema. |
| nano | Editor de texto por defecto. |

## Directorios

La definición de directorios en Linux:

| Nombre directorio | Uso |
| ----- | ---- |
| / | La raiz del arbol de directorios del sistema |
| /bin /sbin | Contiene los binarios ejecutables, comandos esenciales que se utilizan en el modo de un solo usuario y comandos esenciales requeridos por todos los usuarios del sistema. el sbin se utiliza para binarios esenciales relacionados con la administración del sistema, tales como ifconfig y shutdown. |
| /dev | Contiene nodos de dispositivos, un tipo de pseudo-archivo utilizado por la mayoría de los dispositivos de hardware y software, a excepción de los dispositivos de red. |
| /var | Contiene archivos que se espera que cambien de tamaño y contenido cuando el sistema está en funcionamiento (var significa variable). |
| /etc | Es el home de los archivos de configuración del sistema. No contiene programas binarios, aunque hay algunas secuencias de comandos ejecutables |
| /boot | Contiene los pocos archivos esenciales necesarios para arrancar el sistema. |
| /lib | Contiene las librerias (código común compartida por las aplicaciones y necesario para ellos para correr) para los programas esenciales en / bin y / sbin |
| /media | Normalmente donde se encuentra en donde se montan los medios extraíbles, como CD, DVD y unidades USB. |
| /opt | Paquetes de aplicaciones de software opcionales. |
| /sys | Pseudo sistema de archivos virtual con información sobre el sistema y el hardware. Puede ser utilizado para modificar los parámetros del sistema y para fines de depuración. |
| /srv | Datos específicos del sitio servido por el sistema. rara vez se utiliza. |
| /usr | Multiusuario aplicaciones, servicios y datos. |
| /usr/include | Archivos de cabecera utilizados para compilar aplicaciones. |
| /usr/lib | Las librerias de programas en / usr/bin y /usr/sbin. |
| /usr/lib64 | Librerias de 64 bits para programas de 64 bits en /usr/bin y /usr/sbin. |
| /usr/sbin | Binarios del sistema no esenciales, tales como los demonios del sistema. |
| /usr/share | Los datos compartidos utilizados por las aplicaciones, generalmente independiente de la arquitectura. |
| /usr/src | El código fuente, por lo general para el núcleo de Linux. |
| /usr/X11R6 | Archivos de configuración de X Window. Generalmente obsoleto. |
| /usr/local | Los datos y programas específicos para la máquina local. Subdirectorios incluyen bin, sbin, lib, compartir incluir, etc. |
| /usr/bin | Este es el directorio principal de comandos ejecutables en el sistema. |