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

### Branch (ramas) en GitHub

El comando <code>git branch</code> lista las ramas que existen e indica en cual estamos situados.

El comando <code>git branch nueva_rama</code> tambien sirve para crear ramas, solo basta con agregar un espacio y colocar un nombre (Nota: No debe incluir espacios el nombre ademas se recomienda usar la notacion camello *CamelCase)

En caso de requerir cambiar el nombre de una rama, se utiliza el siguiente comando <code>git branch -m nombre_anterior nombre_nueva</code>

Para cambiar entre ramas se utiliza el siguiente comando <code>git checkout nombre_de_la_rama</code>

Si se desea eliminar una rama, se utiliza el siguiente comando <code>git branch -d rama_a_eliminar</code>

Al trabajar con varias ramas, es necesario saber cuales son las diferencias entre cada una de ellas, para ello se utiliza el comando <code>git diff primera_rama_a_comparar segunda_rama_a_comparar</code>

Si se requiere funcionar las ramas, se utiliza el siguiente comando <code>git merge rama_origen rama_destino</code>