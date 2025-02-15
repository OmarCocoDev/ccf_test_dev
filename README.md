# Curso de GitHub

## Curso básico sobre los comandos en GitHub

### Configuración Básica de Git

1. Para comenzar a utilizar GitHub, lo primero que hay que hacer es registrarse o iniciar sesión;  para ello, hay que dirigirse a la siguiente página: https://github.com/
2. Una vez completado el registro o iniciada sesión, hay que instalar git (GitBash) en nuestro equipo.
3. Completada la instalación de GitBash, es necesario crear una carpeta en nuestro PC / Mac donde conectaremos el / los repositorio(s) de GitHub.
4. Utilizando la consola de GitBash, nos ubicamos dentro de la carpeta e introduciremos el siguiente comando para inicializar GitHub. <code>git init</code>

### Creación de un repositorio

1. GitHub crea una URL de cada repositorio creado en su plataforma, por ello es necesario crearlo o utilizar uno existente.
2. Teniendo la URL, el siguiente paso es establecer la conexión entre el repositorio remoto con nuestro equipo.
3. Dentro de GitBash en nuestro equipo nos situamos en la ruta de la carpeta creada previamente y colocamos los siguientes comandos:
4. <code>git config user.name "Nombre de usuario en GitHub"</code>
5. <code>git config user.email "Correo utilizado en GitHub"</code>
6. <code>git remote add origin "URL del repositorio"</code>

### Comandos básicos de GitHub (GIT ADD, GIT COMMIT, GIT PUSH, ETC)

El comando <code>git add nombre_archivo</code> se utiliza para indicar a GitHub que agregaremos un archivo al repositorio, solo se está notificado más no se está agregando.
Nota: Si se desean subir varios archivos, basta con agregrar un espacio y un punto al final del add, ejemplo: <code>git add .</code>

El comando <code>git commit -m "Comentario"</code> le indica a GitHub la confirmación para agregar el archivo al repositorio, junto con un comentario.

El comando <code>git push -u origin master</code> sube el archivo al repositorio indicado, la rama donde se subirá; en nuestro caso, usaremos la rama por defecto creada por GitHub que se llama "master".

El comando <code>git fetch</code> se utiliza para recuperar el nuevo trabajo realizado por otras personas.

El comando <code>git clone</code> se utiliza para copiar de forma completa un repositorio remoto a nuestro equipo.

El comando <code>git pull origin master</code> se utiliza para bajar los cambios hechos en el repositorio remoto, para ello se especifican 2 parametros, el primero especifica el alias que le hayamos dado al repositorio remoto (por convencion se suele nombrar "origin"), despues se debe especificar la rama (en este caso es "master").

El comando <code>git status</code> muestra el estado del directorio de trabajo y del repositorio.

### Branch (ramas)

El comando <code>git branch</code> lista las ramas que existen e indica en cual estamos situados.

El comando <code>git branch nueva_rama</code> tambien sirve para crear ramas, solo basta con agregar un espacio y colocar un nombre (Nota: No debe incluir espacios el nombre ademas se recomienda usar la notacion camello *CamelCase)

En caso de requerir cambiar el nombre de una rama, se utiliza el siguiente comando <code>git branch -m nombre_anterior nombre_nueva</code>

Para cambiar entre ramas se utiliza el siguiente comando <code>git checkout nombre_de_la_rama</code>

Si se desea eliminar una rama, se utiliza el siguiente comando <code>git branch -d rama_a_eliminar</code>

Al trabajar con varias ramas, es necesario saber cuales son las diferencias entre cada una de ellas, para ello se utiliza el comando <code>git diff primera_rama_a_comparar segunda_rama_a_comparar</code>

Si se requiere funcionar las ramas, se utiliza el siguiente comando <code>git merge rama_origen rama_destino</code> (Nota, para poder hacer el merge es necesario situase en la rama destino)

### Pull request

El comando git pull se emplea para extraer y descargar contenido desde un repositorio remoto y actualizar al instante el repositorio local para reflejar ese contenido, cuando el repositorio no es de nuestra autoria, debemos realizar lo siguientes pasos

1. Ubicar el repositorio en el que queramos contribuir
2. Teniendo el repositorio, hay que realizar un "Fork"
3. Despues de hacer realizado el fork, se procede a clonar el repositorio a nuestro equipo <code>git clone url_repositorio</code>
4. Teniendo el repositorio clonado, procedemos a crear una rama y trabajar en nuestra contribución
5. Agregamos nuestros cambios y los subimos
6. Accedemos a la URL del repositorio en el que estamos contribuyendo y podremos vizualizar nuestra rama y los commits, despues de ello pulsamos en "Contribute"
7. Nos pedira hacer el pull request (Hay que esperar la aprobación). 
8. Listo hemos hecho nuestro pull request

### Revertir cambios

En caso de querer eliminar un commit, se utiliza el comando <code>git reset</code>. Nota: Si necesitamos eliminar un archivo podemos utilizar el siguiente comando: <code>git rm --cached "<added_file_to_undo>"</code>

### Etiquetas (tag)

Git tiene la posibilidad de etiquetar puntos específicos del historial como importantes. Esta funcionalidad se usa típicamente para marcar versiones de lanzamiento (v1.0, por ejemplo).

Listar Tus Etiquetas: <code>git tag</code>

Para buscar etiquetas con un patrón particular. El repositorio del código fuente de Git, por ejemplo, contiene más de 500 etiquetas. Si sólo te interesa ver la serie 1.8.5, puedes ejecutar: <code>git tag -l 'v1.8.5*'</code>

#### Crear etiquetas

Git utiliza dos tipos principales de etiquetas: ligeras y anotadas.

Una etiqueta ligera es muy parecido a una rama que no cambia - simplemente es un puntero a un commit específico.

Sin embargo, las etiquetas anotadas se guardan en la base de datos de Git como objetos enteros. Tienen un checksum; contienen el nombre del etiquetador, correo electrónico y fecha; tienen un mensaje asociado; y pueden ser firmadas y verificadas con GNU Privacy Guard (GPG). 

Para crear una etiqueta anotada, se utiliza el siguiente comando: <code>git tag -a v1.4 -m 'my version 1.4'</code>. La opción -m especifica el mensaje de la etiqueta, el cual es guardado junto con ella. Si no especificas el mensaje de una etiqueta anotada, Git abrirá el editor de texto para que lo escribas.

Puedes ver la información de la etiqueta junto con el commit que está etiquetado al usar el comando: <code>git show v1.4</code>

Para crear una etiqueta ligera, utiliza el siguiente comando: <code>git tag v1.4-lw</code>

Para ver la etiqueta ligera, utiliza el siguiente comando: <code>git show v1.4-lw</code>

Para subir una etiqueta al repositorio remoto, utiliza el siguiente comando: <code>git push origin v1.4</code>
Nota: Para subir varias etiquetas, se usa el siquiente comando: <code>git push origin --tags</code>