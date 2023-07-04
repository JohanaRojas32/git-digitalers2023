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
 ´´´sh
git log 
git lo --oneline      (menos info que el git log)

 ´´´´



