# comandos 

## Comando sudo

Abreviatura de superusuario do, sudo es uno de los comandos básicos más populares de Linux que te permite realizar tareas que requieren permisos administrativos o de root.

Al utilizar sudo, el sistema pedirá a los usuarios que se autentiquen con una contraseña. A continuación, el sistema Linux registrará una marca de tiempo como seguimiento. Por defecto, cada usuario root puede ejecutar comandos sudo durante 15 minutos por sesión.

Si intentas ejecutar sudo en la línea de comandos sin autenticarte, el sistema registrará la actividad como un evento de seguridad.

Esta es la sintaxis general:

sudo (comando)

También puedes añadir una opción, por ejemplo:

    -k o -reset-timestamp invalida el archivo timestamp.
    -g o -group=group ejecuta comandos como un nombre o ID de grupo especificado.
    -h o -host=host ejecuta comandos en el host.

## Comando pwd

Utiliza el comando pwd para encontrar la ruta de tu directorio de trabajo actual. Simplemente introduciendo pwd te devolverá la ruta actual completa, una ruta de todos los directorios que comienza con una barra oblicua (/). Por ejemplo, /inicio/nombredeusuario.

El comando pwd utiliza la siguiente sintaxis:

pwd [opción]

Tiene dos opciones aceptables:

    -L o -logical imprime el contenido de las variables de entorno, incluidos los enlaces simbólicos.
    -P o -physical imprime la ruta real del directorio actual.

## Comando cd

Para navegar por los archivos y directorios de Linux, usa el comando cd. Te pedirá la ruta completa o el nombre del directorio, dependiendo del directorio de trabajo actual en el que te encuentres.

Supongamos que estás en /home/nombredeusuario/Documentos y deseas ir a Fotos, un subdirectorio de Documentos. Para hacerlo, simplemente escribe el siguiente comando:

cd Fotos.

Otro escenario es si deseas ir a un directorio completamente nuevo, por ejemplo, /home/nombredeusuario/Peliculas. En este caso, debes escribir cd seguido de la ruta absoluta del directorio:

cd /home/nombredeusuario/Peliculas.

Hay algunos atajos para ayudarte a navegar rápidamente:

    cd ~[nombredeusuario] para ir directamente a la carpeta de inicio.
    cd .. para ir un directorio hacia arriba.
    cd- para ir al directorio anterior.

## Comando ls

El comando ls se usa para ver el contenido de un directorio. Por defecto, este comando mostrará el contenido de tu directorio de trabajo actual.

Si deseas ver el contenido de otros directorios, escribe ls y luego la ruta del directorio. Por ejemplo, para ver el contenido de la carpeta Documentos ingresa:

ls/inicio/nombredeusuario/Documentos

Hay variaciones que puedes usar con el comando ls:

    ls -R también listará todos los archivos en los subdirectorios.
    ls -a mostrará los archivos ocultos.
    ls -al listará los archivos y directorios con información detallada como los permisos, el tamaño, el propietario, etc.

## Comando cat

cat (abreviatura de concatenate, en inglés) es uno de los comandos más utilizados en Linux. Este lista, combina y escribe el contenido de los archivos en la salida estándar. Para ejecutar este comando, escribe cat seguido del nombre del archivo y su extensión. Por ejemplo:

cat archivo.txt.

Aquí hay otras formas de usar el comando cat:

    cat > nombredearchivo.txt crea un nuevo archivo.
    cat nombredearchivo1.txt nombredearchivo2.txt>nombredearchivo3.txt fusiona nombrearchivo1.txt y nombrearchivo2.txt y almacena el resultado en nombrearchivo3.txt.
    tac nombrearchivo.txt muestra el contenido en orden inverso.

## Comando cp

Utiliza el comando cp para copiar archivos o directorios y su contenido. Echa un vistazo a los siguientes casos de uso.

Para copiar un archivo del directorio actual a otro, introduce cp seguido del nombre del archivo y del directorio de destino. Por ejemplo:

cp nombrearchivo.txt /inicio/nombredeusuario/Documentos

Para copiar archivos en un directorio, introduce los nombres de los archivos seguidos del directorio de destino:

cp nombrearchivo1.txt nombrearchivo2.txt nombrearchivo3.txt /inicio/nombredeusuario/Documentos

Para copiar el contenido de un fichero a otro nuevo en el mismo directorio, introduce cp seguido del fichero de origen y del fichero de destino:

cp nombrearchivo1.txt nombrearchivo2.txt

Para copiar un directorio completo, pasa el indicador -R antes de escribir el directorio de origen, seguido del directorio de destino:

cp -R /inicio/nombredeusuario/Documentos /inicio/nombredeusuario/Documentos_backup
## Comando mv

El uso principal del comando mv es mover archivos, aunque también se puede usar para cambiar el nombre de los archivos. Además, no produce ninguna salida al ejecutarlo.

Simplemente escribe mv seguido del nombre del archivo y el directorio de destino. Por ejemplo, si quieres mover nombredearchivo.txt al directorio /inicio/nombredeusuario/Documentos:

mv nombrearchivo.txt /inicio/nombredeusuario/Documentos.

También puedes utilizar el comando mv para renombrar un archivo:

mv nombre_archivo_antiguo.txt nombre_archivo_nuevo.txt
## Comando mkdir

Utiliza el comando mkdir para crear uno o varios directorios a la vez y establecer los permisos para cada uno de ellos. El usuario que ejecuta este comando debe tener el privilegio de crear una nueva carpeta en el directorio principal o puede recibir un error de permiso denegado.

Esta es la sintaxis básica:

mkdir [opción] nombre_directorio

Por ejemplo, si deseas crear un directorio llamado Música:

mkdir Musica

Para crear un nuevo directorio llamado Canciones dentro de Música, utiliza este comando:

mkdir Musica/Canciones

El comando mkdir acepta muchas opciones, como:

    -p o -parents crean un directorio entre dos carpetas existentes. Por ejemplo, mkdir -p Musica/2020/Canciones creará el nuevo directorio «2020».
    -m establece los permisos del archivo. Por ejemplo, para crear un directorio con todos los permisos de lectura, escritura y ejecución para todos los usuarios, introduce mkdir -m777 nombre_directorio.
    -v imprime un mensaje para cada directorio creado.

## Comando rmdir

Para eliminar permanentemente un directorio vacío, utiliza el comando rmdir. Recuerda que el usuario que ejecuta este comando debe tener privilegios sudo en el directorio padre.

Por ejemplo, si deseas eliminar un subdirectorio vacío llamado personal1 y su carpeta principal mydir:

rmdir -p mydir/personal1
## Comando rm

El comando rm se utiliza para borrar archivos dentro de un directorio. Asegúrate de que el usuario que ejecuta este comando tiene permisos de escritura.

Recuerda la ubicación del directorio ya que esto eliminará el/los archivo(s) y no podrás deshacerlo.

Esta es la sintaxis general:

rm nombredearchivo

Para eliminar varios archivos, introduce el siguiente comando:

rm nombredearchivo1 nombredearchivo2 nombredearchivo3

Aquí tienes algunas opciones aceptables que puedes añadir:

    -i pide confirmación al sistema antes de borrar un archivo.
    -f permite al sistema eliminar sin confirmación.
    -r borra archivos y directorios de forma recursiva.


## comando touch

El comando touch permite crear un archivo vacío o generar y modificar una marca de tiempo en la línea de comandos de Linux.

Por ejemplo, introduce el siguiente comando para crear un archivo HTML llamado Web en el directorio Documentos:

touch /inicio/nombredeusuario/Documentos/Web.html
## Comando locate

El comando locate puedes encontrar un archivo en el sistema de base de datos.

Además, si añades el argumento -i, desactivará la distinción entre mayúsculas y minúsculas, por lo que podrás buscar un archivo aunque no recuerdes su nombre exacto.

Para buscar contenidos que contengan dos o más palabras, utiliza un asterisco (*). Por ejemplo:

locate -i escuela*nota

El comando buscará los archivos que contengan las palabras escuela y nota, tanto si utilizan mayúsculas como minúsculas.
## Comando find

Utiliza el comando find para buscar archivos dentro de un directorio específico y realizar operaciones posteriores. Ésta es la sintaxis general:

find [opción] [ruta] [expresión]

Por ejemplo, quieres buscar un archivo llamado notas.txt dentro del directorio inicio y sus subcarpetas:

find /inicio -name notas.txt

Aquí tienes otras variaciones al utilizar find:

    find -name nombredearchivo.txt para buscar archivos en el directorio actual.
    find ./ -type d -name nombredeldirectorio para buscar directorios.

## Comando grep

Otro comando básico de Linux en la lista es grep o impresión global de expresiones regulares. Te permite encontrar una palabra buscando entre todos los textos de un archivo específico.

Una vez que el comando grep encuentra una coincidencia, imprime todas las líneas que contienen el patrón específico. Este comando ayuda a filtrar archivos de registro de gran tamaño.

Por ejemplo, si deseas buscar la palabra azul en el archivo notepad.txt:

grep azul notepad.txt

La salida del comando mostrará las líneas que contengan azul.
## Comando df

Utiliza el comando df para informar sobre el uso del espacio en disco del sistema, mostrado en porcentaje y en kilobytes (KB). Esta es la sintaxis general:

df [opciones] [archivo]

Por ejemplo, introduce el siguiente comando si deseas ver el uso del espacio en disco del sistema del directorio actual en un formato legible para personas:

df -h

Estas son algunas variaciones:

    df -m muestra información sobre el uso del sistema de archivos en MBs.
    df -k muestra el uso del sistema de archivos en KBs.
    df -T muestra el tipo de sistema de archivos en una nueva columna.

## Comando du

Si quieres comprobar cuánto espacio ocupa un archivo o un directorio, utiliza el comando du. Gracias a este comando puedes identificar qué parte del sistema utiliza excesivamente el almacenamiento.

Recuerda que debes especificar la ruta del directorio cuando utilices el comando du. Por ejemplo, para comprobar /inicio/usuario/Documentos introduce:

du /inicio/usuario/Documentos

Añadiendo una bandera al comando du se modificará la operación, como por ejemplo:

    -s ofrece el tamaño total de una carpeta especificada.
    -m proporciona información sobre carpetas y archivos en MB.
    k muestra la información en KB.
    -h informa de la última fecha de modificación de las carpetas y archivos mostrados.

## Comando head

El comando head permite ver las diez primeras líneas de un texto. Añadiendo una opción se puede cambiar el número de líneas mostradas. El comando head también se utiliza para dar salida a datos canalizados a la CLI.

Esta es la sintaxis general:

head [opción] [archivo]

Por ejemplo, si quieres ver las diez primeras líneas de nota.txt, situado en el directorio actual:

head nota.txt

A continuación te indicamos algunas opciones que puedes añadir:

    -n o -lines imprime el primer número personalizado de líneas. Por ejemplo, introduce head -n 5 nombredearchivo.txt para mostrar las cinco primeras líneas de nombredearchivo.txt.
    -c o -bytes imprime el primer número personalizado de bytes de cada archivo.
    -q o -quiet no imprimirán cabeceras que especifiquen el nombre del archivo.

## Comando tail

El comando tail muestra las diez últimas líneas de un archivo. Permite a los usuarios comprobar si un archivo tiene datos nuevos o leer mensajes de error.

Este es el formato general:

tail [opción] [archivo]

Por ejemplo, si deseas ver las diez últimas líneas del archivo colores.txt:

tail -n colores.txt


