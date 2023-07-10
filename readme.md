# Clase 06 - Git intro

## Configuracion inicial

´´´sh
git config --global user.name "Johana Rojas"
git config --global user.email "joohanarojas96@gmail.com"
´´´´

## Verificando la configuracion inicial, si quedo todo piola!

´´´sh
git config --get-regexp user
´´´´

## Iniciando un repositorio de git 

´´sh
git init
´´


## Areas del repositorio de GIT

3 areas

* Working Directory (WD): directrorio de trabajo donde se van agregando o quitando los archivos durante el desarrollo (escritorio de trabajo)

* Starting Area (SA): Area de control de cambios. Area de confirmacion intermedia. Area temporal/intermedia

* Local Repo (LR): Una caja donde voy guardando las fotos que voy sacando.


## Estado de los archivos

* untracked: Archivos que estan en el WD pero GIT no les esta dando seguimiento

* unmodified: Archivo que GIT ya esta siguiendo y con respecto al WD no fueron modificados

* modified: Archivos que se encuentran en el repositorio (estan siendo seguidos por GIT) pero difieren con lo que se encuentra en el area de trabajo WD

* staged: Archivos que estan en el area temporal intermedia



## ¿como chequeo el estado?

´´sh
git status
´´

## Para confirmar los cambios de un archivo (WD => SA)

´´´sh
git add <nombre del archivo>
git add README.MD   (ejemplo)
git add readme.md css.estilos.css  (si quiero agregar varios)
git add .     (con el punto . o el asterisco *  agrego todos los archivos que estan untracked, modified al SA.´)
´´´´


## Para hacer un commit (sacar la foto) (SA => LR)

´´´sh
git commit -m "Mensaje explicando que guarde en esa foto"
git commin -m "Agrego el readme.md"  (ejemplo)
´´´´

## Para ver las fotos (commits) que estan dentro del Local Repo
NOTA: SI SE ME BLOQUEA LA CONSOLA TENGO QUE PRESIONAR LA TECLA q (quit)

 ´´´sh
git log 
git lo --oneline      (menos info que el git log)

 ´´´´

 ## Si quiero ver los cambios entre el WD y el LP
NOTA: SI SE ME BLOQUEA LA CONSOLA TENGO QUE PRESIONAR LA TECLA q (quit)

 ´´´sh
 git diff
 ´´´


 ## Subir repositorio local al repositorio remoto

 # Cramos un repositorio remoto en Github

 ´´´sh
 Ponemos nombre del archivo y lo dejamos publico. ahi lo creamos.

 Despues copiamos el primer link que me da Github(del medio) y en GIT copiamos el link asi como esta, le damos enter. 
(!esto es para vincular mi repo local con el remoto, esta genereando la ruta que los vincula)

Despues hacemos lo mismo con el ultim link que me da Github(del medio) y lo volvemos a pegar en el GIT, damos enter. 
(Esto lo que hace es darle un alias =< dice add "origin" y una ruta... el nombre origin es el nombre de la ruta asi cada vez que necesitamos nombrarla no estamos copiando toda la ruta>)

 ´´´´

 ## pARA SUBIR EL local al remoto (subir la copia del local al remoto) tengo que hacer lo siguiente:

´´´sh
git push -u origin main      

(aca le estoy diciendo que suba lo de main al origin)
Ese "-u" lo que hace es que vincula automaticamente el origin con el main (el local con el remoto), entonces la proxima vez no necesitas aclarar, solo basta con poner:


git push
 
´´´´


## Trabajando con ramas

...

## Crear una rama 
´´´´sh
git branch <nombre-rama>
git branch info-rama
´´

## Si quiero ver las ramas que tengo 

´´´sh
git branch
´´

### Como cambiarnos de rama 

´´´sh
git switch <nombre-rama>
git switch info-branches
´´´´


## MERGE


## Como fusiono ramas, o sea junto ramas
**IMPORTANTE: Tengo que estar en la rama destino. si quiero traer de info branches a main, tengo que estar parado en main y de ahi ejecutar el siguiente comando:


´´´sh
git merge <nombre-rama>
git merge info branches
´´´´

## TIPOS DE MERGE

* Fast-forward : Es el mejor de los mundos, git se va a encargar de solucionar toda la fusion. No es necesario que intervenga el desarrollador.
* Recursiva: Es un algoritmo que suele solucionar el conflicto. Une automaticamente las ramas
* Manual (conflicto) : ocurre cuando hay modificaciones en las mismaas lineas del archivo. 


## Cambiar el nombre de la rama

´´ sh
git branch -m <nombre-rama-actual> <nombre-rama-nueva>
´´´´







