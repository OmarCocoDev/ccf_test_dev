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

### Comandos básicos de GitHub (GIT ADD, GIT COMMIT, GIT PUSH)

El comando <code>git add nombre_archivo</code> se utiliza para indicar a GitHub que agregaremos un archivo al repositorio.

Nota: Una buena práctica, antes de comenzar a interactuar con un repositorio, es revisar siempre el estatus de nuestros cambios entre el repositorio remoto y nuestro equipo (local). Para ello utilizaremos el siguiente comando: <code> git status</code>.