###### Curso Git desde cero
Sistema de control de versiones para el mantenimiento eficiente y confiable de archivos.

###### Zonas de Git
1. Directorio de trabajo
2. Área de preparación
3. Directorio Git

####### Flujo de trabajo básico en Git
1. Modificas una serie de archivos en tu directorio de trabajo.
2. Preparas los archivos, añadiéndolos a tu área de preparación.
3. Confirmas los cambios, lo que toma los archivos tal y como están en el área de preparación y almacena esa copia instantánea de manera permanente en tu directorio de Git.

#######Configurando Git por primera vez

git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
git config --global core.editor nano
git config --list

#######Solicitar ayuda en Git

git help "comando"
git "comando" --help

#######Comando de Git 

* git init - crear el repositorio en la carpeta de trabajo

* git status - ver el estatus de los archivos

* git add - agregar archivos a la zona de preparacion.

* git add . - Para agregar todos los archivos a la zona de preparacion lo hacemos con el Punto (.). De esta manera incluimos todos los archivos.

* git add -A - Agrega al area de preparacion archivos que ya estemos siguiendo.

* git commit -m - agregar el archivo al repositorio de manera definitiva junto com un comentario entre comillas.

* git commit --amend - modifica el mensaje del commit mas reciente. tambien se puede utilizar para remplazar el commit mas reciente agregandole archivos adicionales. Estos archivos deben estar en el area de preparacion. al utilizar esta sentencia lo que lograresmos es remplazar tanto los archivos como la descripcion del commit.

* git commit -a -m "Comentario desciptivo" - agrega el archivo directamente al repositorio sin pasa por el area de preparacion de archivo. En otras palabras pasa del directorio de trabajo a el repositorio git de manera directa. Para que esto sea posible tenemos que seguir primero los archivos si no, no funcionra.

* git log -Este comando sirve para ver los commits en el repositorio.

* git log -- oneline - muestra el historial agregado en una sola linea. Se puede utilizar con --graph en combinacion.

* git log -- graph - muestra el historial de commit por ramificaciones graficas. Se puede utilizar con --oneline.

* git log -- decorate -  este comando sirve para ver las ramas y las etiquetas que conresponde a cada commit. Ojo para mostrar todos los commit independientemente del punto del tiempo en que estemos utilizaremos la bandera --all.

* git log -[numero de commit] - muestra el numero commit que se especifica.

* git log --before="Año-mes-dia"- muestra el historial de commit "ANTES DE" la fecha indicada se puede combinar con --after.

* git log --after="Año-mes-dia"- muestra el historial de commit "DESPUES" de la fecha indicada se puede combinar con --before.

* git log --pretty=format: parametros de formato - despues de los dos punto ubicados en la sentencia format tomara en cuenta los puntos y comas que se escriban entre la sentencia. Es importante que los parametros esten entre comillas.

* git diff - nos muestra cual es la diferencia entre el directorio de trabajo y los archivos confirmados en el commit. Tambien es utilizado para ver la diferencia entre dos commit de diferente linea de tiempo.

* git diff --staged - muestra la difenrencia estre el directorio de trabajo y el archivo de la zona de preparacion.

* git reset HEAD "nombre de archivo" - Con este comando sacamos el archivo de la zona de preparacion y lo devolvemos a la zona de trabajo.

* gitinore - series de archivos que vamos a ignorar que no queremos que sean rasteables. Este archivo en una carpeta y los archivos que queremos que se  ignoren los ponemos dentro de ese archivo.

* git checkout "Nombre de archivo" - recupera los archivos borrados de los archivos del directorio de trabajo pero que se encuentran en el repositorio de git y nos permiten ser recuperados. Ojo solo se pueden recuperar si estos archivos se encuentran en el repositorio de git guardados asea que se le hallan hecho commit a ese archivo. Este comando tambien se utiliza para pasar a otro commit en la linea de tiempo. Para volver al el punto "presente" se utiliza esta misma sentencia con el comando "master" 

* git rm "archivo" - elimina los archivos de directorio de trabajo y los coloca en el area de preparacion para ser confirmado para su posterios eliminacion. se peuede sacar del area de preparacion con la sentencia reset HEAD y devolverlo al arbol de carpetas con la sentencia checkout. Se confirma la eliminacion de archivo con el comando commit se recomienda como en todos los commit que se hace hacer una descripcion explicativa de el commit.

* git mv "archivo inicial" "nuevo nombre del archivo" - renombra un archivo o lo mueve de carpeta o directorio. Una ves renombrado el archivo pasa al area de preparacion donde tienen que ser confirmado con el comando commit para calidar el renombramirto o el cambio del directorio del archivo.

* git clone "Url del repositorio" - se clona un repositorio remoto por ejemplo en github. Se descargara en la carpeta donde se ejecute el comando git clone.

* git tag - lista todas las etiquetas que ya existen y los hace en orden alfabetico.  

* git tag [nombre]  - Existen dos tipos de etiqueta la etiqueta ligera que vendria siendo un apuntador a alias de el hast de commit. Esta sentencia se agrega al commit mas reciente

* git tag -a [nombre] -m[descripcion] - Las otras etiquetas son las etiquetas comentadas estas se guardan en la base de datos de git como objetos enteros tiene un checksum contiene el nombre del etiquetador, correo electronico y fecha es casi como un commit a demas tiene su respectivo cambio asociado.Esta sentencia se agrega al commit mas reciente.

* git tag [nombre] {hast} - Este comando sirve para agregar una etiqueta ligera a un commit en cualquier punto del tiempo.

* git tag -a [nombre] {hast} -m{ Descripcion } - Este comando sirve para agregar una etiqueta ligera a un commit en cualquier punto del tiempo.

* git tag -l "patron" - lista las etiquetas que coincida con el patron especificado.

*git show [hast] - Muestra los cambios del commit especificado.

#######Comando de la terminal en window

cls -limpiar pantalla 
dir - listar directorio
cd - Entrar al directorio 
findstr - buscar por cadena de texto especificando la busqueda 

