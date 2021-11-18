# Manual

Manual de conceptos y comandos basicos para las herramientas: Git, Fish shell, Docker, Vim

## Git:

Es un controlador de versiones de código fuente.

### Conceptos basicos de git:

- **Stage:** esta es el area donde se almacenan los archivos que van a ser usados en el siguiente commit.
- **Pull:** extrae archivos del repositorio guardandolos en local.
- **Commit:** es un comentario que se vincula a un cambio en los archivos que van a ser subidos.
- **Push:** sube los cambios del ultimo commit al repositorio.
- **Rama:** (branch) es una copia del separada de la versión principal del código.
- **Merge:** significa actualizar el código principal con los cambios de una rama.
- **Origin:** es la dirección del repositorio.
- **Clone:** crea una copia del repositorio de forma local.
- **.gitignore** archivo de configuracion de git que especifica los archivos que no seran incluidos al momento de hacer un commit, ejemplo:
    el siguiente código ignoraria la carpeta llamada node_modules,
    todos los archivos de cache de edicion de texto, todos los archivos de log
    y el archivo de variables de entorno
~~~
node_modules/
*.swp
*.log
VAR.ENV
~~~

### Comandos de git:

comandos mas comunes en git.

- `git init` inicializa un repositorio de git de forma local.
- `git remote` este comando sirve para administrar el origin de un repositorio las etiquetas soportadas son las siguientes.
  - `-v` lista los repositorios de origen a los que esta enlazado al proyecto.
  - `add` sirve para agregar una ruta de origen al proyecto ejemplo `git add origin [URL]`
  - `set-url` cambia el origen del repositorio (con este comando se puede actualizar el origen de una fuente de https a ssh) ejemplo `git remote set-url origin [URL]`
- `git add` permite añadir ficheros o archivos el stage, se puede especificar los nombres de cada archivo o agregarlos de forma masiva utilizando un punto "." ignorando aquellos que se encuentren especificados en el archivo de configuración del **".gitignore"**
- `git commit` este comando sirve para confirmar los cambios realizados anclandolos al comentario ingresado y guardando una bitacora con un id especifico la sintaxis del comando es la siguiente: `git commit -m '[comentario]'
- `git pull` extrae los cambios del repositorio
- `git push` inserta los cambios locales en el repositorio
- `git stage` sirve para deshacer los cambios realizados hasta el ultimo commit

## Fish Shell

Es una shell de linux mas amigable con el usuario que tiene funcionalidades que facilitan la manipulacion del sistema por medio de la terminal

### comandos basicos 

- `ls` sirve para listar los archivos disponibles en un directorio
- `cd` sirve para cambiar de directorio se utiliza escribiendo el comando seguido del repositorio al que se quiere mover para subir de directorio se utilizan dos puntos ".." su sintaxis es la siquiente: `cd [ruta del directorio]`
- `pwd` sirve para mostrar el directorio en el que se esta actualmente 
- `alias` sirve para crear una funcion simple y nombrarla su sintaxis es la siguiente: `alias [nombre de la funcion]='[comando a ser ejecutado]'`
- `funcsave` guarda un alias y lo hace permanente en el sistema su sintacis es la siguiente: `funcsave [nombre de la funcion]`
- `clear` limpia la pantalla de la consola
- `mkdir` crea un directorio su sintaxis es la siguiente `mkdir [nombre del directorio]`
- `rm` elimina archivos, para eliminar directorios se utiliza la etiqueta -r para indicar que sea recursivo ejemplo de la sintaxis `rm -r [nombre del directorio]`
- `cp` copia un archivo, su sintaxis es la siguiente `cp [nombre del archivo] [ruta del archivo]`, la ruta de el archivo puede especificar el nombre que se le dara a la copia de lo contrario si solo se especifica un directorio la copia tendra el mismo nombre que el archivo original es compatible con la etiqueta -r para copiar directorios de forma recursiva
- `mv` mueve un archivo de un lugar a otro la sintaxis es la misma que la de el comando cp con la diferencia que este elimina el archivo original se puede utilizar tambien para renombrar el archivo tambien es compatible con la etiqueta -r para mover directorios de forma recursiva
- `touch` se utiliza para crear un nuevo archivo
