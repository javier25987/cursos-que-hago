# Curso de git  

---
## Temario

1. Configuracion inicial
2. Comandos "git add" y "git commit"
3. Comandos "git restore", "git checkout" y mas
4. Comando "git diff"
5. Modificar y deshacer commits
6. Ramas "Branches"
7. Fusionar ramas "Merge"
8. Conflictos en un merge
9. Git ignore 
10. Alias en git
11. Git reflog
12. Introduccion a github
13. Crear y configurar un repositorio remoto
14. Git clone
15. Git push
16. Git pull & git fetch
17. Migrar repositorio local
18. Forks y contribuciones
19. Pull requests
20. Github issues
21. Buenas practicas en git 
* NOTAS DE EL CURSO

---

## Que es git?
Git es un sistema de control de versiones distribuido, esto significa que cada version 
de el proyecto esta distribuida en cada computadora de cada desarrollador asi cada persona
puede trabajar en el proyecto de forma independiente, en windows git se puede descargar por
su pagina oficial [Git](https://git-scm.com/ "https://git-scm.com/").

NOTA:  
A la hora de descargar git no hay configuraciones extra, en el instalador solo hay que 
presionar next.

```git 
$
```

---

## 1. Configuracion inicial.

En git hay que configurar nuestro correo electronico y nuestro alias con eso cuando 
haga un cambio este va a aparecer firmado por el alias y el correo de este usuario,
para configurar git lo mas recomendable es usar el bash de git y que tener en cuenta 
que existen 3 entornos de configuracion:

* local
* global
* system

### local
Esta configuracion se aplica unicamente a el repositorio actual.
### gobal
Esta configuracion se aplica a todos los repositorios de un usuario.
### system
Esta configuracion se aplica directamente a todo el computador (incluidos todos los
usuarios y todos sus repositorios).  

Lo mas comun es configurar git usando el global

```git 
$ git config --global
```

en este comando se puede remplazar el global por un "local" o "system" y esto tambien 
se puede hacer para todos los comandos de esta forma, lo primero es configurar el alias
de el usuario y su correo electronico, para esto se usan los comandos:

```git
$ git config --global user.name "nombre (alias) de el usuario"
```

```git
$ git config --global user.email "email de el usuario"
```

con estos comandos ya queda configurado en nombre y el email de el usuario, si se deseara
ver una lista de las configuraciones se puede hacer con el comando 

```git 
$ git config --global --list
```

el "--global" en el anterior comando es opcional se puede omitir en el comando y se mostraria
la configuracion general  

si se desea mejorar la conexion con un editor de codigo de usa el comando

```git
$ git config --global core.editor "code --wait"
```

en el anterior comando adentro de las comillas "code" es la palabra clave para refereirse a 
visual estudio code para cada editor hay que buscar la palabra clave y "--wait" hace que el
programa espere a cerrar el editor para aplicar los cambios. A la hora de querer bajar y subir
archivos a un servidor es recomendable usar el comando,

```git
$ git config --global core.autocrlf true
```

este comando es importante a la hora de subir y bajar archivos de un servidor ya que configura 
correctamente el salto de linea entre sistemas linux y windows, si se esta en un sistema linux
en lugar de "true" en el final de el comando lo ideal es escribir "input"

---

## que es un repositorio?

un repositorio es un lugar destinado para almacenar los archivos y demas elementos que vamos a
usar en git, en el uso habitual de git este suele ser una carpeta ubicada en la carpetya que se
usa para guardar el proyecto a su vez esta carpeta es el aera de trabajo que es de donde hacemos los
commits para guardarlos en el repositorio.  

---

## 2. Comandos "git add" y "git commit".

Los comandos "git add" y "git commit" respectivamente se aplican en un repositorio para añadir 
archivos a el area de guardado y para hacer un punto de guardado en el repositorio

### git add

el comando,

```git
$ git add <nombre de el archivo>
```

lo que hace es que añade un archivo a el area de guardado para que este despues despues sea añadido a 
un commit si se desean añadir todos los archivos de la carpeta a el area de guardado de usa,

```git
$ git add .
```

el area de guardado es el punto intermedio de los archivos para determinar si se hace un commit 
con ellos o no, para ver los archivos guardados en el area de guardado se usa el comando, 

```git
$ git status
```

de esta manera y diferenciado por colores se muestra el area de guardado y todos los archivos en ella.  

### git commit
Un commit es un punto de guardado que se hace en el repositorio, para realizar un comit este toma todos
los archivos de el area de guardado y junto a un mensaje realiza un punto de guardado

```git 
$ git commit -m "mensaje de el commit"
```

en este comando la sentencia "-m" hace referancia a el mensaje de el commit, por otro lado si se desea
hacer un commit con todos los archivos disponibles en el area de trabajo se añade la sentencia "-a" y 
esto hara un commit con todos los archivos de el area de trabajo.

## 3. Comandos "git restore", "git checkout" y mas.































## NOTAS DE EL CURSO
En la terminal los comandos "mkdir" y "rmdir" crean y eliminan carpetas respectivamente.  








